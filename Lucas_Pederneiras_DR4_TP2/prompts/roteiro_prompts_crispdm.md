# Roteiro de prompts: CRISP-DM 

Ferramenta: ChatGPT (OpenAI) | GPT-6 Astra | 09/11/2026

Todos os prompts seguem o molde PAPEL, CONTEXTO, TAREFA, DADOS, EXEMPLO DE FORMATO e FORMATO.

---

## FASE 1: Entendimento do negócio

```
FASE 1: Entendimento do negócio

PAPEL
Você é analista de dados do Instituto de Segurança Pública do Estado do Rio de Janeiro (ISP-RJ). Escreve para Helena Prado, analista da equipe de estatísticas: ela conhece a base e os indicadores, mas não é especialista em IA. O que você produzir é rascunho. Eu conferirei cada número contra o CSV público do ISP-RJ antes de assinar a nota.

CONTEXTO
Helena pediu uma nota técnica sobre roubo de veículos no estado do Rio de Janeiro, comparando os doze meses de 2025 com os doze meses de 2024, no formato da Nota Técnica interna nº 14/2026. A fonte é a série mensal por área de delegacia (CISP), arquivo BaseDPEvolucaoMensalCisp.csv. Os indicadores são roubo_veiculo, recuperacao_veiculos, furto_veiculos e roubo_carga, somados por região (coluna regiao). Você não pode inventar, arredondar nem importar números de outras fontes. Não atribua causas a políticas, operações ou mudanças de registro. Não calcule taxas por habitante ou por frota: esses dados não existem nesta base. O texto é apoio à decisão da equipe de análise, não comunicado à imprensa.

TAREFA
1. Transforme a demanda de Helena em quatro blocos curtos: objetivo, público, perguntas de análise e limites da nota. Resultado esperado: os quatro blocos, sem cifras.
2. Proponha o esqueleto da nota em lista hierárquica, com cabeçalho (data, declaração de uso de IA), assunto, resumo executivo de até 70 palavras e seções 1 a 6 (objetivo e método; resultados no estado; resultados por região; recuperação de veículos; limitações; encaminhamentos), cada uma com subitens. Resultado esperado: lista numerada de no máximo três níveis, sem redigir o texto da nota.
3. Liste o que a IA não pode afirmar nesta nota. Resultado esperado: lista de vedações.
4. Se algum número for necessário e ainda não estiver nos dados desta fase, escreva exatamente "NÃO CONFIRMADO" e indique a origem de cada afirmação. Resultado esperado: nenhuma cifra inventada.

DADOS
- Demanda: nota sobre roubo de veículos no RJ, 2025 versus 2024, formato da NT 14/2026.
- Período: janeiro a dezembro de 2024 e janeiro a dezembro de 2025.
- Indicadores: roubo_veiculo, recuperacao_veiculos, furto_veiculos, roubo_carga.
- Agregação: soma por coluna regiao.
- Nesta fase não há quadro numérico conferido. Não use números da nota modelo.

EXEMPLO DE FORMATO
Trecho só para mostrar o tom e a estrutura da NT 14/2026. Os números abaixo NÃO devem ser usados (outro período: 1º semestre de 2026 contra 2025):

"1. Objetivo e método. Esta nota resume a evolução dos roubos de veículos, dos veículos recuperados, dos furtos de veículos e dos roubos de carga no estado do Rio de Janeiro, para apoiar a reunião de planejamento do segundo semestre. A comparação usa os meses de janeiro a junho de 2026 e os mesmos meses de 2025, de modo que os dois períodos tenham o mesmo tamanho e a mesma sazonalidade."

FORMATO
- Português do Brasil.
- Lista hierárquica com no máximo três níveis.
- Sem tabelas nesta fase.
- Sem cifras, exceto se eu as tiver colado (não colei nenhuma).
- Se faltar dado: escreva "NÃO CONFIRMADO".
```

---

## FASE 2: Entendimento dos dados

```
FASE 2: Entendimento dos dados

PAPEL
Você continua como analista de dados do ISP-RJ, escrevendo para Helena Prado. Seu papel agora é mapear o CSV e os riscos de leitura. Você não calcula ainda o quadro final da nota. Qualquer número que não esteja nos dados colados abaixo deve ser marcado "NÃO CONFIRMADO". Eu conferirei a leitura no Python (pandas, sep=';', encoding='latin-1') antes da fase 3.

CONTEXTO
O arquivo BaseDPEvolucaoMensalCisp.csv tem cerca de 7 MB e mais de 38 mil linhas. Cada linha é uma CISP em um mês, com 65 colunas. O arquivo usa ponto e vírgula como separador e não está em UTF-8. A nota usará apenas 2024 e 2025, doze meses em cada ano, e as colunas roubo_veiculo, recuperacao_veiculos, furto_veiculos, roubo_carga e regiao. A coluna fase indica a consolidação do registro. Não anexe o CSV inteiro a este chat: ele é grande demais para a janela de contexto. Nesta fase vão só o cabeçalho, uma amostra e as regras de leitura.

TAREFA
1. Descreva o que cada coluna da amostra representa e como a linha se identifica (CISP + mês + ano). Resultado esperado: lista curta das colunas relevantes.
2. Aponte os riscos de leitura: separador, codificação, valores ausentes, período, coluna fase e grafia da coluna regiao. Resultado esperado: lista de riscos, cada um com o que pode quebrar a soma.
3. Diga se os doze meses de 2024 e de 2025 aparecem na amostra e o que ainda precisa ser conferido no arquivo completo. Resultado esperado: o que está visível versus o que fica "NÃO CONFIRMADO".
4. Recomende o recorte para a fase 3 (filtro de ano, tratamento de regiao e colunas a somar), sem ainda montar o quadro. Resultado esperado: recorte em passos.
5. Não invente totais. Se um total não estiver colado, escreva "NÃO CONFIRMADO" e indique a origem de cada afirmação.

DADOS
Regras de leitura conferidas por mim:
- separador: ponto e vírgula
- encoding ao abrir: latin-1
- não usar UTF-8 na leitura

Cabeçalho (65 colunas; recorte):
cisp;mes;ano;mes_ano;aisp;risp;munic;mcirc;regiao;...;roubo_veiculo;roubo_carga;...;furto_veiculos;...;recuperacao_veiculos;...;fase

Amostra de 5 linhas (não são totais; não some esta amostra como se fosse o estado):
cisp;mes;ano;munic;regiao;roubo_veiculo;recuperacao_veiculos;furto_veiculos;roubo_carga;fase
1;1;2024;Rio de Janeiro;Capital;2;1;7;0;3
48;1;2024;Seropédica;Baixada Fluminense;10;8;6;0;3
70;1;2024;Tanguá;Interior;1;4;3;0;3
72;1;2024;São Gonçalo;Grande Niterói [grafia corrompida no arquivo];21;21;33;2;3
72;10;2024;São Gonçalo;Grande Niterói;51;50;37;8;3

Observação já vista na leitura: a região Grande Niterói aparece com pelo menos duas grafias, uma delas com caracteres corrompidos. Paraty em 2026 chega a aparecer como Capital; 2026 fica fora desta nota.

EXEMPLO DE FORMATO
Não use os números da NT 14/2026. Use só o tipo de lista de riscos, por exemplo: "Os meses de julho a setembro de 2026 estão em outra fase de consolidação na base (fase 2) e ficaram fora da comparação." Isso ilustra o papel da coluna fase, com período diferente do nosso.

FORMATO
- Português do Brasil.
- Seções: colunas; riscos; o que falta conferir; recorte proposto.
- Sem totais estaduais ou regionais.
- Amostra não deve ser somada.
- Número ausente: "NÃO CONFIRMADO".
```

---

## FASE 3: Preparação dos dados

```
FASE 3: Preparação dos dados

PAPEL
Você é analista de dados do ISP-RJ e vai apenas reformatar o quadro que eu já conferi no CSV. Não recalcule a partir de memória ou de outras fontes. Se um valor não estiver no quadro colado, escreva "NÃO CONFIRMADO". Eu validarei o JSON e o YAML com json.loads e yaml.safe_load, e conferirei os totais 30.930/25.235 (roubos) e 19.034/17.406 (recuperados).

CONTEXTO
O quadro abaixo soma, por região e ano, as colunas roubo_veiculo, recuperacao_veiculos, furto_veiculos e roubo_carga nos doze meses de 2024 e nos doze meses de 2025. A grafia de Grande Niterói já foi unificada. São 8 registros (4 regiões × 2 anos). A linha ESTADO é só conferência; não entra nos 8 registros. Este quadro, e não o CSV inteiro, é o que entra no chat: só o texto colado conta para tokens.

TAREFA
1. Copie o quadro em JSON válido (RFC 8259): uma lista com exatamente 8 objetos, chaves regiao, ano, roubo_veiculo, recuperacao_veiculos, furto_veiculos, roubo_carga. Números inteiros, sem separador de milhar, sem a linha ESTADO. Resultado esperado: bloco JSON.
2. Copie o mesmo conteúdo em YAML válido, mesma ordem e mesmos valores. Resultado esperado: bloco YAML.
3. Some de novo, a partir só do JSON que você acabou de escrever, os totais estaduais de roubo_veiculo e recuperacao_veiculos em 2024 e em 2025. Resultado esperado: quatro inteiros iguais a 30930, 19034, 25235 e 17406.
4. Se algum valor não estiver no quadro, escreva "NÃO CONFIRMADO". Não invente município, percentual nem variação nesta fase. Indique a origem de cada número (linha do quadro).

DADOS
Quadro conferido contra o CSV (inteiros sem ponto de milhar):

regiao | ano | roubo_veiculo | recuperacao_veiculos | furto_veiculos | roubo_carga
Capital | 2024 | 17302 | 9960 | 8872 | 1769
Capital | 2025 | 13713 | 9148 | 8680 | 1496
Baixada Fluminense | 2024 | 10921 | 6138 | 4451 | 1334
Baixada Fluminense | 2025 | 8719 | 5030 | 4504 | 1286
Grande Niterói | 2024 | 1939 | 1264 | 1993 | 248
Grande Niterói | 2025 | 2058 | 1367 | 2191 | 243
Interior | 2024 | 768 | 1672 | 2021 | 86
Interior | 2025 | 745 | 1861 | 2115 | 88
ESTADO | 2024 | 30930 | 19034 | 17337 | 3437
ESTADO | 2025 | 25235 | 17406 | 17490 | 3113

Município de apoio (não entra nos 8 registros; só para a fase 4):
São Gonçalo | 2024 | roubo_veiculo 1558
São Gonçalo | 2025 | roubo_veiculo 1716

EXEMPLO DE FORMATO
Os números da NT 14/2026 não devem ser copiados. O formato JSON desejado é do tipo:

[
  {"regiao": "Capital", "ano": 2024, "roubo_veiculo": 0, "recuperacao_veiculos": 0, "furto_veiculos": 0, "roubo_carga": 0}
]

Os zeros acima são fictícios e não devem aparecer na sua resposta.

FORMATO
- Primeiro o JSON, depois o YAML, depois as quatro somas.
- JSON com aspas duplas.
- Inteiros sem ponto ou vírgula de milhar.
- Exatamente 8 registros, sem ESTADO.
- Origem de cada total: soma das quatro regiões no próprio JSON.
```

---

## FASE 3 (correção)

Usar só se o JSON ou o YAML da FASE 3 não passar na validação.

```
FASE 3 (correção): Preparação dos dados

PAPEL
Você continua como analista de dados do ISP-RJ. Sua tarefa agora é só corrigir o JSON e o YAML da resposta anterior. Não invente valores novos. Eu conferirei de novo com json.loads e yaml.safe_load e os totais 30930, 19034, 25235 e 17406.

CONTEXTO
A resposta anterior não passou na validação. Erros típicos: aspas simples, separador de milhar, linha ESTADO incluída, número de registros diferente de 8, ou totais que não batem. O quadro colado na FASE 3 permanece a única fonte.

TAREFA
1. Reescreva o JSON válido com exatamente 8 objetos e inteiros sem separador. Resultado esperado: JSON que passe em json.loads.
2. Reescreva o YAML equivalente, mesma ordem e mesmos valores. Resultado esperado: YAML que passe em yaml.safe_load e seja igual ao JSON.
3. Recalcule os quatro totais a partir do JSON corrigido. Resultado esperado: 30930, 19034, 25235, 17406.
4. Aponte, em uma frase cada, o erro da resposta anterior e a correção. Indique a origem de cada número ou escreva "NÃO CONFIRMADO".

DADOS
Use exclusivamente o quadro da mensagem "FASE 3: Preparação dos dados".

EXEMPLO DE FORMATO
Não use os números da NT 14/2026. Devolva apenas JSON, YAML, totais e o registro do erro. Os zeros abaixo são fictícios e não devem aparecer:

[
  {"regiao": "Capital", "ano": 2024, "roubo_veiculo": 0, "recuperacao_veiculos": 0, "furto_veiculos": 0, "roubo_carga": 0}
]

FORMATO
- JSON RFC 8259, aspas duplas, 8 registros, sem ESTADO.
- YAML equivalente.
- Totais inteiros, sem ponto de milhar.
- Lista curta de correções.
- Texto puro; sem LaTeX.
```

---

## FASE 4: Modelagem (análise)

```
FASE 4: Modelagem (análise)

PAPEL
Você é analista de dados do ISP-RJ e escreve um rascunho analítico para Helena Prado. Use somente o quadro conferido da fase 3 (8 registros) e o detalhe de São Gonçalo já colado. Não invente causas. Percentuais com uma casa decimal (vírgula). Eu conferirei cada variação contra o CSV antes da fase 5.

CONTEXTO
A nota compara 2025 com 2024, doze meses contra doze meses. A NT 14/2026 serve só como exemplo de formato e de tom, com outro período e outros números, que não devem ser reutilizados. A razão recuperados/roubados não é taxa de recuperação: veículos recuperados incluem furtados e veículos de outro período ou região.

TAREFA
1. Calcule, para o estado, variação absoluta e percentual dos quatro indicadores. Resultado esperado: quatro frases no molde "passaram de X para Y (Z%)".
2. Calcule a mesma variação de roubo_veiculo para as quatro regiões e identifique qual foi a única com alta ou a única com queda. Resultado esperado: quatro frases mais uma síntese.
3. Informe a participação de São Gonçalo nos roubos de veículos da Grande Niterói em 2025. Resultado esperado: "São Gonçalo responde por A dos B casos da região em 2025".
4. Calcule a razão recuperados/roubados no estado em 2024 e em 2025 e explique, em uma frase, por que ela não é taxa de recuperação. Resultado esperado: duas porcentagens e a ressalva.
5. Liste limites da análise (ocorrências versus crimes ocorridos; ausência de frota e população; ausência de causas). Resultado esperado: três limites.
6. Mostre a conta de cada percentual em uma linha de texto puro, no molde (depois - antes) / antes * 100 = Z%, com os inteiros sem ponto de milhar. Resultado esperado: uma linha por indicador, região, São Gonçalo e razão. Se faltar dado, escreva "NÃO CONFIRMADO". Não use LaTeX, fração, $$ nem fórmula renderizada.

DADOS
Quadro da fase 3 (já conferido). Totais ESTADO:
2024: roubo_veiculo 30930; recuperacao_veiculos 19034; furto_veiculos 17337; roubo_carga 3437
2025: roubo_veiculo 25235; recuperacao_veiculos 17406; furto_veiculos 17490; roubo_carga 3113
São Gonçalo, roubo_veiculo: 1558 (2024) e 1716 (2025). Grande Niterói 2025: 2058.

EXEMPLO DE FORMATO
Só o formato da NT 14/2026; NÃO copie os números dela:

"2. Resultados no estado. Os roubos de veículos passaram de 11.736 para 13.430, um aumento de 1.694 casos (14,4%). [...]
3. Resultados por região. A Capital concentra o maior número de roubos de veículos: 6.614 em 2025 e 7.461 em 2026 (aumento de 12,8%). [...] o município de São Gonçalo responde por 1.396 dos 1.576 casos da região em 2026.
4. Recuperação de veículos. A razão entre veículos recuperados e veículos roubados no estado foi de 73,8% em 2025 e de 75,3% em 2026. Essa razão não é uma taxa de recuperação: os veículos recuperados incluem também veículos furtados e veículos roubados antes do período ou em outra região."

FORMATO
- Português do Brasil.
- Seções 2, 3 e 4 no tom da nota modelo.
- Inteiros com ponto de milhar (30.930). Percentuais com uma casa decimal e vírgula (18,4%).
- Contas visíveis no final, cada uma em uma linha de teclado: numeros, +, -, /, *, = e %.
- Proibido LaTeX, $$ , \\frac e qualquer fórmula desenhada.
- Sem atribuição de causa.
```

---

## FASE 5: Avaliação

```
FASE 5: Avaliação

PAPEL
Você NÃO é o autor da nota. Você é revisor técnico independente da gerência de qualidade estatística do ISP-RJ. Seu público é Helena Prado e o analista autor. Você não redige a nota: você aponta erros, ambiguidades e riscos de assinatura. Se um número não estiver no quadro da fase 3, marque "NÃO CONFIRMADO". O autor conferirá seus apontamentos contra o CSV antes de aceitar ou devolver à fase anterior.

CONTEXTO
Chegou um rascunho das seções 2 a 4, produzido na fase 4, mais o quadro de 8 registros. A nota modelo (NT 14/2026) tem outro período; os números dela são armadilha. A razão recuperados/roubados não pode ser chamada de taxa de recuperação. O resumo executivo ainda não foi escrito. Qualquer invenção, arredondamento indevido, região faltante ou cópia da nota modelo é motivo para devolver à fase 3 (dados) ou à fase 4 (análise).

TAREFA
1. Confira cada inteiro do rascunho contra o quadro da fase 3. Resultado esperado: tabela item a item com "confere" ou "não confere", citando o valor do quadro.
2. Recalcule cada percentual com uma casa decimal, em texto puro, uma linha por item, no molde (depois - antes) / antes * 100 = Z%. Confere. Resultado esperado: lista de percentuais conferidos, copiável. Não use LaTeX nem fórmula renderizada.
3. Verifique se a razão foi chamada, indevidamente, de taxa de recuperação. Resultado esperado: sim ou não, com o trecho.
4. Verifique se há cifra da NT 14/2026 (por exemplo 11.736, 13.430, 73,8%). Resultado esperado: sim ou não.
5. Emita parecer: aprovar; devolver à FASE 3; ou devolver à FASE 4. Resultado esperado: um único parecer, com a lista do que deve ser corrigido.
6. Não reescreva a nota completa. Indique a origem de cada número ou escreva "NÃO CONFIRMADO".

DADOS
Quadro conferido da fase 3 (8 registros + ESTADO + São Gonçalo), já colado neste chat.
Use o rascunho da fase 4 como objeto da revisão.

EXEMPLO DE FORMATO
Não reproduza os números da NT 14/2026. Use um parecer no tom:

"Item: roubos de veículos no estado, 2024. Rascunho: [valor]. Quadro: 30930. Confere / Não confere.
Parecer: devolver à FASE 4 porque [motivo]."

FORMATO
- Português do Brasil.
- Seções: conferência de inteiros; conferência de percentuais; linguagem da razão; contaminação pela nota modelo; parecer.
- Conferência de percentuais em linhas de teclado (numeros, +, -, /, *, =, %). Proibido LaTeX, $$ e fração.
- Sem texto corrido da nota.
- Um parecer explícito no final.
```

---

## RETORNO À FASE 4 (usar se o revisor devolver a análise)

```
RETORNO À FASE 4: Modelagem (análise)

PAPEL
Você volta a ser o analista de dados autor, não o revisor. Corrija só o que o revisor marcou. Não invente números. Eu conferirei a versão corrigida contra o CSV.

CONTEXTO
O revisor técnico da fase 5 devolveu a análise. O quadro da fase 3 permanece válido. A razão entre veículos recuperados e veículos roubados não é taxa de recuperação. Os números da NT 14/2026 continuam proibidos.

TAREFA
1. Reescreva as seções 2, 3 e 4 já corrigidas, no formato da nota modelo. Resultado esperado: texto corrido das três seções.
2. Mantenha inteiros e percentuais que conferem; altere apenas o que o revisor apontou. Resultado esperado: lista curta do que mudou.
3. Mostre a origem de cada número ou escreva "NÃO CONFIRMADO". Se repetir contas, use texto puro: (depois - antes) / antes * 100 = Z%. Sem LaTeX.

DADOS
Quadro da fase 3 e apontamentos da fase 5, já neste chat.

EXEMPLO DE FORMATO
Use o molde da NT 14/2026 (seções 2 a 4), sem copiar os números dela. A ressalva obrigatória é: "Essa razão não é uma taxa de recuperação: os veículos recuperados incluem também veículos furtados e veículos roubados antes do período ou em outra região."

FORMATO
- Seções 2, 3 e 4.
- Inteiros com ponto de milhar; percentuais com uma casa decimal.
- Lista final de correções aplicadas.
```

---

## FASE 6: Implantação e comunicação

```
FASE 6: Implantação e comunicação

PAPEL
Você é analista de dados do ISP-RJ e redige a versão para conferência. Helena Prado é a leitora. O texto é rascunho até eu conferir cada número contra o CSV. Não invente, não arredonde além de uma casa decimal nos percentuais e não atribua causas. Não escreva nomes de pessoas reais.

CONTEXTO
A estrutura obrigatória é o esqueleto hierárquico da fase 1. Os números obrigatórios são os do quadro da fase 3, já conferidos, e a análise corrigida após a fase 5. O resumo executivo tem no máximo 70 palavras e só pode repetir informação que já apareça nas seções 1 a 6: não acrescente município, conclusão ou cifra que o texto principal não tenha dito. O cabeçalho deve trazer a data 9 de novembro de 2026 e a declaração de que o texto foi redigido com apoio de IA e conferido contra o CSV do ISP-RJ. Deixe um espaço para o nome do autor; eu o colocarei no Word.

TAREFA
1. Escreva o cabeçalho (nota interna, data, declaração de uso de IA, espaço para o autor) e o assunto exatamente: "roubos e recuperação de veículos no estado do Rio de Janeiro, 2025 em comparação com 2024". Resultado esperado: cabeçalho + assunto.
2. Escreva o resumo executivo com no máximo 70 palavras, restrito ao texto principal. Resultado esperado: um parágrafo e a contagem de palavras.
3. Redija as seções 1 a 6 seguindo rigorosamente o esqueleto da fase 1, no tom da NT 14/2026, com os quatro indicadores. Resultado esperado: texto corrido das seis seções.
4. Inclua a fonte no formato: INSTITUTO DE SEGURANÇA PÚBLICA (Rio de Janeiro). Estatísticas de segurança pública: série histórica mensal por área de delegacia desde 01/2003 (arquivo BaseDPEvolucaoMensalCisp.csv). Rio de Janeiro: ISP, [2026]. Disponível em: https://www.ispdados.rj.gov.br/estatistica.html. Acesso em: 21 out. 2026.
5. Faça a conferência final: liste os inteiros usados e a origem (linha do quadro) ou escreva "NÃO CONFIRMADO". Resultado esperado: lista de conferência em texto puro, sem LaTeX.

DADOS
Quadro da fase 3, análise corrigida da fase 4 e parecer da fase 5, já neste chat. Data: 9 de novembro de 2026.

EXEMPLO DE FORMATO
Siga o tom da NT 14/2026 (seções 1 a 6, frases curtas, percentuais com uma casa decimal). Não copie os números dela (11.736, 13.430, 14,4%, 73,8% etc.).

FORMATO
- Português do Brasil.
- Ordem: cabeçalho; assunto; resumo (até 70 palavras + contagem); seções 1 a 6; fonte; lista de conferência.
- Inteiros com ponto de milhar.
- Percentuais com uma casa decimal e vírgula.
- Sem causas de política ou operação.
- Sem nomes de pessoas reais.
```
