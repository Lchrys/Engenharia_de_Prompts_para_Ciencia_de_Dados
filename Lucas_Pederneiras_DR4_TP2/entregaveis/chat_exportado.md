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


Fase um — entendimento do negócio
Blocos de entendimento
Objetivo: Preparar uma nota técnica que compare a evolução dos indicadores selecionados entre períodos equivalentes e apoie a análise da equipe. Origem: demanda e dados fornecidos nesta fase.
Público: Helena Prado e a equipe de estatísticas do ISP-RJ. Origem: descrição do papel e do público na demanda.
Perguntas de análise: Como variou o roubo de veículos no estado? Como os indicadores se distribuíram por região? Como variaram as recuperações de veículos e os indicadores complementares — furto de veículos e roubo de carga? Origem: indicadores, período e agregação especificados na demanda.
Limites da nota: A comparação deverá usar a série mensal do arquivo indicado, somada por região, e depender de conferência dos dados antes da assinatura. Não deverá atribuir causas nem apresentar taxas por habitante ou por frota. Origem: instruções da demanda e limitações declaradas para a base.
Esqueleto proposto para a nota
Cabeçalho
Data: NÃO CONFIRMADO — confirmar a data de emissão. Origem: não informada nesta fase.
Declaração de uso de IA: registrar que a ferramenta apoiou a estruturação do rascunho; números e afirmações deverão ser conferidos pela equipe. Origem: instrução de que o material é rascunho e será conferido antes da assinatura.
Assunto
Comparação dos indicadores de veículos no estado do Rio de Janeiro entre os períodos informados. Origem: demanda de Helena.
Resumo executivo
Síntese dos principais resultados estaduais e regionais, a preencher após a conferência do quadro numérico; limite de até setenta palavras. Origem: instrução de formato; resultados ainda não disponíveis.
Objetivo e método
Finalidade da nota.
Períodos comparados: janeiro a dezembro de 2025 e janeiro a dezembro de 2024.
Fonte, indicadores e critério de agregação por região.
Resultados no estado
Variação do roubo de veículos.
Contextualização com furto de veículos e roubo de carga.
Resultados por região
Comparação regional dos indicadores.
Destaques e diferenças a preencher após conferência.
Recuperação de veículos
Resultado do indicador de veículos recuperados.
Comparação com o roubo de veículos, sem inferir vínculo causal.
Limitações
Limites da base e do recorte analítico.
Necessidade de conferência dos valores antes da assinatura.
Encaminhamentos
Validar os dados agregados e a redação.
Indicar questões para análise posterior, sem antecipar explicações não demonstradas.
Origem dos períodos, indicadores, arquivo e agregação: dados fornecidos nesta fase. Origem das seções e do limite do resumo: formato solicitado para a nota. O conteúdo dos resultados permanece NÃO CONFIRMADO, pois não há quadro numérico conferido.

Vedações — o que a IA não pode afirmar
Não apresentar cifras, variações, posições regionais ou conclusões quantitativas sem conferência no CSV.
Não usar números ou conclusões da nota de exemplo.
Não atribuir variações a políticas, operações ou mudanças de registro.
Não calcular nem afirmar taxas por habitante ou por frota.
Não tratar associação ou comparação entre indicadores como prova de causalidade.
Não afirmar que a soma por região, a cobertura ou a consistência dos dados foi validada antes da conferência.
Não completar lacunas com dados de outras fontes.
Afirmações pendentes de confirmação
Valores e variações dos indicadores no estado e por região: NÃO CONFIRMADO. Origem necessária: agregação do arquivo BaseDPEvolucaoMensalCisp.csv, após conferência.
Data de emissão da nota: NÃO CONFIRMADO. Origem necessária: definição pela equipe.




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


Colunas
cisp: identificação da área de delegacia.
mes e ano: mês e ano do registro; em conjunto com cisp, identificam a unidade temporal da linha.
mes_ano: campo de referência mensal combinado, cuja função exata de formatação deve ser conferida no arquivo completo.
regiao: região usada para agrupar os registros.
roubo_veiculo, recuperacao_veiculos, furto_veiculos e roubo_carga: indicadores a somar na análise.
fase: campo relacionado à consolidação do registro; a interpretação e o tratamento aplicáveis a 2024 e 2025 precisam ser conferidos.
aisp, risp, munic e mcirc: campos de identificação ou localização presentes no cabeçalho; o significado detalhado de mcirc não foi especificado nesta fase. NÃO CONFIRMADO — confirmar no dicionário de dados.
Origem: cabeçalho e descrição fornecidos; detalhes sem definição dependem do dicionário da base.
Riscos
Separador: a leitura deve usar ponto e vírgula. Outro separador pode deslocar colunas ou fazer o cabeçalho ser lido como um único campo. Origem: regra de leitura fornecida.
Codificação: abrir como UTF-8, em vez de latin-1, pode corromper caracteres e dificultar a identificação de regiões. Origem: regra de leitura fornecida.
Valores ausentes ou não numéricos: não foi informado se existem. Se campos de indicadores tiverem valores ausentes ou texto, a soma pode ignorá-los, falhar ou produzir resultado inadequado, conforme o tratamento. NÃO CONFIRMADO — verificar no arquivo completo. Origem: arquivo completo, ainda não inspecionado nesta fase.
Período: a amostra contém linhas de janeiro e outubro de 2024, mas não demonstra a presença de todos os meses nem de 2025. Filtrar ou agrupar incorretamente por ano e mês pode incluir meses indevidos ou deixar meses de fora. Origem: cinco linhas de amostra fornecidas.
Coluna fase: todas as linhas exibidas têm o mesmo valor, mas isso não comprova a fase dos registros de todos os meses de 2024 e 2025. Uma seleção ou exclusão de fases sem regra confirmada pode alterar a cobertura da soma. NÃO CONFIRMADO — verificar a distribuição de fase no período da nota e a regra aplicável. Origem: amostra e descrição da coluna fornecidas.
Grafia de regiao: Grande Niterói aparece com grafia íntegra e corrompida na amostra. Agrupá-las sem padronização pode dividir a mesma região em categorias distintas; uma substituição ampla pode, por outro lado, mesclar categorias incorretamente. Origem: observação e amostra fornecidas.
Amostra: as linhas são apenas exemplos, não um recorte representativo nem uma base para somas estaduais ou regionais. Origem: aviso explícito nos dados fornecidos.
O que falta conferir
A amostra mostra janeiro e outubro de 2024; não mostra os doze meses completos de 2024 nem meses de 2025. A presença dos doze meses de cada ano no arquivo completo é NÃO CONFIRMADO. Origem: amostra de cinco linhas.
Conferir no arquivo completo a cobertura de meses por ano, a existência de duplicatas na combinação cisp + mês + ano e a completude dos registros. NÃO CONFIRMADO — não verificável com a amostra. Origem: arquivo completo.
Conferir valores ausentes, tipos e valores dos quatro indicadores, além das categorias e fases registradas no período. NÃO CONFIRMADO — não verificável com a amostra. Origem: arquivo completo.
Identificar todas as grafias de regiao em 2024 e 2025 e validar um mapeamento de padronização antes de agrupar. A lista completa de variantes é NÃO CONFIRMADO. Origem: arquivo completo; a amostra comprova apenas a observação sobre Grande Niterói.
Recorte proposto
Ler o CSV com sep=';' e encoding='latin-1', conforme as regras fornecidas.
Conferir os nomes e tipos das colunas, especialmente cisp, mes, ano, regiao, os quatro indicadores e fase.
Filtrar ano para 2024 e 2025; confirmar que cada ano tem os doze meses esperados. Não usar linhas de 2026.
Examinar e documentar as variantes de regiao; aplicar apenas um mapeamento validado, preservando as categorias que não puderem ser identificadas com segurança.
Verificar duplicatas, ausências e a distribuição de fase. Só aplicar filtro por fase se a regra para o período estiver confirmada; essa regra está NÃO CONFIRMADO nesta fase.
Na fase 3, somar por regiao e período somente roubo_veiculo, recuperacao_veiculos, furto_veiculos e roubo_carga, após validar os campos e o recorte. Nenhum total foi calculado nesta fase.




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


JSON

[
  {
    "regiao": "Capital",
    "ano": 2024,
    "roubo_veiculo": 17302,
    "recuperacao_veiculos": 9960,
    "furto_veiculos": 8872,
    "roubo_carga": 1769
  },
  {
    "regiao": "Capital",
    "ano": 2025,
    "roubo_veiculo": 13713,
    "recuperacao_veiculos": 9148,
    "furto_veiculos": 8680,
    "roubo_carga": 1496
  },
  {
    "regiao": "Baixada Fluminense",
    "ano": 2024,
    "roubo_veiculo": 10921,
    "recuperacao_veiculos": 6138,
    "furto_veiculos": 4451,
    "roubo_carga": 1334
  },
  {
    "regiao": "Baixada Fluminense",
    "ano": 2025,
    "roubo_veiculo": 8719,
    "recuperacao_veiculos": 5030,
    "furto_veiculos": 4504,
    "roubo_carga": 1286
  },
  {
    "regiao": "Grande Niterói",
    "ano": 2024,
    "roubo_veiculo": 1939,
    "recuperacao_veiculos": 1264,
    "furto_veiculos": 1993,
    "roubo_carga": 248
  },
  {
    "regiao": "Grande Niterói",
    "ano": 2025,
    "roubo_veiculo": 2058,
    "recuperacao_veiculos": 1367,
    "furto_veiculos": 2191,
    "roubo_carga": 243
  },
  {
    "regiao": "Interior",
    "ano": 2024,
    "roubo_veiculo": 768,
    "recuperacao_veiculos": 1672,
    "furto_veiculos": 2021,
    "roubo_carga": 86
  },
  {
    "regiao": "Interior",
    "ano": 2025,
    "roubo_veiculo": 745,
    "recuperacao_veiculos": 1861,
    "furto_veiculos": 2115,
    "roubo_carga": 88
  }
]
YAML

- regiao: "Capital"
  ano: 2024
  roubo_veiculo: 17302
  recuperacao_veiculos: 9960
  furto_veiculos: 8872
  roubo_carga: 1769
- regiao: "Capital"
  ano: 2025
  roubo_veiculo: 13713
  recuperacao_veiculos: 9148
  furto_veiculos: 8680
  roubo_carga: 1496
- regiao: "Baixada Fluminense"
  ano: 2024
  roubo_veiculo: 10921
  recuperacao_veiculos: 6138
  furto_veiculos: 4451
  roubo_carga: 1334
- regiao: "Baixada Fluminense"
  ano: 2025
  roubo_veiculo: 8719
  recuperacao_veiculos: 5030
  furto_veiculos: 4504
  roubo_carga: 1286
- regiao: "Grande Niterói"
  ano: 2024
  roubo_veiculo: 1939
  recuperacao_veiculos: 1264
  furto_veiculos: 1993
  roubo_carga: 248
- regiao: "Grande Niterói"
  ano: 2025
  roubo_veiculo: 2058
  recuperacao_veiculos: 1367
  furto_veiculos: 2191
  roubo_carga: 243
- regiao: "Interior"
  ano: 2024
  roubo_veiculo: 768
  recuperacao_veiculos: 1672
  furto_veiculos: 2021
  roubo_carga: 86
- regiao: "Interior"
  ano: 2025
  roubo_veiculo: 745
  recuperacao_veiculos: 1861
  furto_veiculos: 2115
  roubo_carga: 88
Totais estaduais recalculados do JSON
Roubo de veículos — 2024: 30930. Origem: soma das linhas Capital, Baixada Fluminense, Grande Niterói e Interior de 2024 no JSON.
Recuperação de veículos — 2024: 19034. Origem: soma das mesmas quatro regiões de 2024 no JSON.
Roubo de veículos — 2025: 25235. Origem: soma das linhas Capital, Baixada Fluminense, Grande Niterói e Interior de 2025 no JSON.
Recuperação de veículos — 2025: 17406. Origem: soma das mesmas quatro regiões de 2025 no JSON.




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


2. Resultados no estado
Os roubos de veículos passaram de 30.930 em 2024 para 25.235 em 2025, uma queda de 5.695 casos (18,4%).

As recuperações de veículos passaram de 19.034 para 17.406, uma queda de 1.628 (8,6%). Os furtos de veículos passaram de 17.337 para 17.490, um aumento de 153 (0,9%). Os roubos de carga passaram de 3.437 para 3.113, uma queda de 324 (9,4%).

3. Resultados por região
Na Capital, os roubos de veículos passaram de 17.302 para 13.713, uma queda de 3.589 (20,7%). Na Baixada Fluminense, passaram de 10.921 para 8.719, queda de 2.202 (20,2%). Em Grande Niterói, passaram de 1.939 para 2.058, aumento de 119 (6,1%). No Interior, passaram de 768 para 745, queda de 23 (3,0%). Grande Niterói foi a única região com alta.

Em 2025, São Gonçalo responde por 1.716 dos 2.058 casos de roubo de veículos de Grande Niterói, correspondentes a 83,4%.

4. Recuperação de veículos
A razão entre veículos recuperados e roubados no estado foi de 61,5% em 2024 e 69,0% em 2025. Essa razão não é uma taxa de recuperação: os veículos recuperados também incluem veículos furtados e veículos de outro período ou região.

Limites da análise
Os dados representam ocorrências registradas, não necessariamente todos os crimes ocorridos.
A base não contém dados de população ou frota; portanto, não permite calcular taxas por habitante ou por frota.
A comparação não demonstra causas para as variações observadas.
Contas dos percentuais
(25235 - 30930) / 30930 * 100 = -18,4% (17406 - 19034) / 19034 * 100 = -8,6% (17490 - 17337) / 17337 * 100 = 0,9% (3113 - 3437) / 3437 * 100 = -9,4%

(13713 - 17302) / 17302 * 100 = -20,7% (8719 - 10921) / 10921 * 100 = -20,2% (2058 - 1939) / 1939 * 100 = 6,1% (745 - 768) / 768 * 100 = -3,0%

1716 / 2058 * 100 = 83,4%

19034 / 30930 * 100 = 61,5% 17406 / 25235 * 100 = 69,0%

Origem dos números: totais estaduais e valores regionais, quadro conferido da fase 3; valores de São Gonçalo e Grande Niterói, dados fornecidos para esta fase. As diferenças, razões e percentuais foram calculados a partir desses valores.





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


Conferência de inteiros
Item do rascunho	Valor	Conferência e origem
Roubo de veículos no estado, 2024	30.930	Confere — quadro da fase 3, linha ESTADO, 2024.
Roubo de veículos no estado, 2025	25.235	Confere — quadro da fase 3, linha ESTADO, 2025.
Diferença de roubos de veículos no estado	5.695	Confere — cálculo a partir das linhas ESTADO de 2024 e 2025 do quadro da fase 3.
Recuperações no estado, 2024	19.034	Confere — quadro da fase 3, linha ESTADO, 2024.
Recuperações no estado, 2025	17.406	Confere — quadro da fase 3, linha ESTADO, 2025.
Diferença de recuperações	1.628	Confere — cálculo a partir das linhas ESTADO de 2024 e 2025 do quadro da fase 3.
Furtos de veículos no estado, 2024	17.337	Confere — quadro da fase 3, linha ESTADO, 2024.
Furtos de veículos no estado, 2025	17.490	Confere — quadro da fase 3, linha ESTADO, 2025.
Diferença de furtos	153	Confere — cálculo a partir das linhas ESTADO de 2024 e 2025 do quadro da fase 3.
Roubos de carga no estado, 2024	3.437	Confere — quadro da fase 3, linha ESTADO, 2024.
Roubos de carga no estado, 2025	3.113	Confere — quadro da fase 3, linha ESTADO, 2025.
Diferença de roubos de carga	324	Confere — cálculo a partir das linhas ESTADO de 2024 e 2025 do quadro da fase 3.
Roubo de veículos na Capital, 2024 e 2025	17.302; 13.713	Confere — quadro da fase 3, linhas Capital, 2024 e 2025.
Diferença na Capital	3.589	Confere — cálculo a partir das linhas Capital de 2024 e 2025 do quadro da fase 3.
Roubo de veículos na Baixada Fluminense, 2024 e 2025	10.921; 8.719	Confere — quadro da fase 3, linhas Baixada Fluminense, 2024 e 2025.
Diferença na Baixada Fluminense	2.202	Confere — cálculo a partir das linhas Baixada Fluminense de 2024 e 2025 do quadro da fase 3.
Roubo de veículos em Grande Niterói, 2024 e 2025	1.939; 2.058	Confere — quadro da fase 3, linhas Grande Niterói, 2024 e 2025.
Diferença em Grande Niterói	119	Confere — cálculo a partir das linhas Grande Niterói de 2024 e 2025 do quadro da fase 3.
Roubo de veículos no Interior, 2024 e 2025	768; 745	Confere — quadro da fase 3, linhas Interior, 2024 e 2025.
Diferença no Interior	23	Confere — cálculo a partir das linhas Interior de 2024 e 2025 do quadro da fase 3.
São Gonçalo, 2025; Grande Niterói, 2025	1.716; 2.058	Confere — detalhe de São Gonçalo fornecido para a fase 4 e quadro da fase 3, linha Grande Niterói, 2025.
Recuperados e roubados no estado, 2024	19.034; 30.930	Confere — quadro da fase 3, linha ESTADO, 2024.
Recuperados e roubados no estado, 2025	17.406; 25.235	Confere — quadro da fase 3, linha ESTADO, 2025.

Conferência de percentuais
(25235 - 30930) / 30930 * 100 = -18,4%

(17406 - 19034) / 19034 * 100 = -8,6%

(17490 - 17337) / 17337 * 100 = 0,9%

(3113 - 3437) / 3437 * 100 = -9,4%

(13713 - 17302) / 17302 * 100 = -20,7%

(8719 - 10921) / 10921 * 100 = -20,2%

(2058 - 1939) / 1939 * 100 = 6,1%

(745 - 768) / 768 * 100 = -3,0%

1716 / 2058 * 100 = 83,4%

19034 / 30930 * 100 = 61,5%

17406 / 25235 * 100 = 69,0%

Origem: valores de base no quadro da fase 3 e no detalhe de São Gonçalo fornecido para a fase 4. Percentuais recalculados a partir desses valores, arredondados para uma casa decimal.

Linguagem da razão
Não foi chamada indevidamente de taxa de recuperação. O rascunho diz: “Essa razão não é uma taxa de recuperação” e apresenta a ressalva sobre veículos furtados e veículos de outro período ou região.

Contaminação pela nota modelo
Não há cifra identificável da NT 14/2026 no rascunho. Os exemplos citados — 11.736, 13.430 e 73,8% — não aparecem nele.

Parecer
Aprovar. Os inteiros e percentuais apresentados conferem com o quadro da fase 3 e com o detalhe fornecido para São Gonçalo. Não identifiquei cifras da nota modelo nem uso indevido da expressão “taxa de recuperação”.

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

NOTA TÉCNICA INTERNA
Data: 9 de novembro de 2026
Autor(a): ________________________
Declaração de uso de IA: Texto redigido com apoio de inteligência artificial e conferido contra o CSV do ISP-RJ.

Assunto
roubos e recuperação de veículos no estado do Rio de Janeiro, 2025 em comparação com 2024

Resumo executivo
Em 2025, os roubos de veículos no estado diminuíram 18,4% em relação a 2024, enquanto as recuperações caíram 8,6%. Os furtos de veículos aumentaram 0,9%, e os roubos de carga diminuíram 9,4%. Grande Niterói foi a única região com aumento de roubos de veículos. A razão entre recuperados e roubados não corresponde a uma taxa de recuperação.

Contagem: 51 palavras.

1. Objetivo e método
Esta nota compara os registros de roubo de veículos, recuperação de veículos, furto de veículos e roubo de carga no estado do Rio de Janeiro em 2025 e 2024. São comparados os doze meses de cada ano, de janeiro a dezembro.

A fonte é a série mensal por área de delegacia do ISP-RJ. Os indicadores foram somados por região, com a grafia de Grande Niterói unificada. Os resultados estaduais são apresentados conforme o quadro conferido para esta análise.

2. Resultados no estado
Os roubos de veículos passaram de 30.930, em 2024, para 25.235, em 2025, uma redução de 5.695 casos (18,4%).

As recuperações de veículos passaram de 19.034 para 17.406, redução de 1.628 (8,6%). Os furtos de veículos passaram de 17.337 para 17.490, aumento de 153 (0,9%). Os roubos de carga passaram de 3.437 para 3.113, redução de 324 (9,4%).

3. Resultados por região
Na Capital, os roubos de veículos passaram de 17.302, em 2024, para 13.713, em 2025, uma redução de 3.589 casos (20,7%). Na Baixada Fluminense, passaram de 10.921 para 8.719, redução de 2.202 (20,2%).

Em Grande Niterói, os registros passaram de 1.939 para 2.058, aumento de 119 (6,1%). No Interior, passaram de 768 para 745, redução de 23 (3,0%). Grande Niterói foi a única região com aumento.

Em 2025, São Gonçalo registrou 1.716 dos 2.058 roubos de veículos de Grande Niterói, ou 83,4%.

4. Recuperação de veículos
A razão entre veículos recuperados e roubados no estado foi de 61,5% em 2024 e 69,0% em 2025. Essa razão não é uma taxa de recuperação: os veículos recuperados podem incluir veículos furtados e veículos de outro período ou região.

5. Limitações
Os dados representam ocorrências registradas e não necessariamente todos os crimes ocorridos. A base utilizada nesta análise não fornece dados de população ou de frota, portanto não permite calcular taxas por habitante ou por frota. A comparação descreve variações entre períodos, mas não permite atribuí-las a causas específicas.

6. Encaminhamentos
Antes da assinatura, conferir os valores e a redação final contra o CSV do ISP-RJ. Interpretar os resultados como comparação de registros entre períodos equivalentes, sem inferir causas ou tratar a razão entre recuperados e roubados como taxa de recuperação.

Fonte
INSTITUTO DE SEGURANÇA PÚBLICA (Rio de Janeiro). Estatísticas de segurança pública: série histórica mensal por área de delegacia desde 01/2003 (arquivo BaseDPEvolucaoMensalCisp.csv). Rio de Janeiro: ISP, [2026]. Disponível em: https://www.ispdados.rj.gov.br/estatistica.html. Acesso em: 21 out. 2026.

Lista de conferência dos inteiros
Estado — origem: linha ESTADO do quadro da fase 3.

Roubo de veículos: 2024 — 30.930; 2025 — 25.235.
Recuperação de veículos: 2024 — 19.034; 2025 — 17.406.
Furto de veículos: 2024 — 17.337; 2025 — 17.490.
Roubo de carga: 2024 — 3.437; 2025 — 3.113.
Diferenças entre 2025 e 2024: roubo de veículos — -5.695; recuperação — -1.628; furto — +153; roubo de carga — -324. Origem: cálculo a partir das linhas ESTADO do quadro da fase 3.
Roubo de veículos por região — origem: linhas regionais do quadro da fase 3.

Capital: 2024 — 17.302; 2025 — 13.713; diferença — -3.589.
Baixada Fluminense: 2024 — 10.921; 2025 — 8.719; diferença — -2.202.
Grande Niterói: 2024 — 1.939; 2025 — 2.058; diferença — +119.
Interior: 2024 — 768; 2025 — 745; diferença — -23.
São Gonçalo — origem: detalhe fornecido para a fase 4. Roubo de veículos em 2025 — 1.716. Grande Niterói, 2025 — 2.058, com origem na linha regional correspondente do quadro da fase 3.

Percentuais: foram calculados a partir dos inteiros indicados nesta lista; os valores não foram apresentados como dados de origem independentes.