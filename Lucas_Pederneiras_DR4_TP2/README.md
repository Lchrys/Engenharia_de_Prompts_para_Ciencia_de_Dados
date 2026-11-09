# TP2 - Nota técnica de roubo de veículos no RJ (2025 em comparação com 2024)

## Sobre o trabalho

Este trabalho é um exercício da disciplina Engenharia de Prompts para Ciência de Dados. Ele responde a uma pergunta prática: um assistente de IA generativa pode ajudar a redigir uma nota técnica sem comprometer a precisão dos números?

O cenário é fictício. A analista Helena Prado, da equipe de estatísticas do Instituto de Segurança Pública do Estado do Rio de Janeiro (ISP-RJ), pede uma nota técnica sobre roubo de veículos no estado, comparando 2025 com 2024, no formato de uma nota modelo. Ela quer ver o caminho inteiro: o chat com todos os prompts, a nota pronta em Word e uma previsão do consumo de tokens. Os dados, ao contrário do cenário, são reais e públicos.

O autor atua como analista de dados que atende a essa demanda. Helena conhece a base e os indicadores, mas não é especialista em IA. Por isso, os prompts precisam ser compreensíveis para ela, e ela precisa saber em quais pontos pode confiar nas respostas e em quais deve conferir. A conferência dos números é responsabilidade do autor. A nota só é assinada depois de conferida contra o CSV.

## Dados

- Fonte: série mensal por área de delegacia (CISP) do ISP-RJ, arquivo `BaseDPEvolucaoMensalCisp.csv` (cerca de 7 MB, mais de 38 mil linhas e 65 colunas).
- Leitura: separador ponto e vírgula e codificação latin-1.
- Indicadores usados: `roubo_veiculo`, `recuperacao_veiculos`, `furto_veiculos` e `roubo_carga`.
- Recorte: os doze meses de 2024 e os doze meses de 2025, somados por região (coluna `regiao`).
- O CSV não entra inteiro no chat. Só entram o recorte necessário, uma amostra e o quadro já conferido.

## Como o trabalho foi conduzido

A análise foi feita em um único chat, seguindo as seis fases do CRISP-DM:

1. Entendimento do negócio.
2. Entendimento dos dados.
3. Preparação dos dados.
4. Modelagem (análise).
5. Avaliação, com um papel de revisor independente. Se houvesse problema, o trabalho voltaria à fase anterior.
6. Implantação e comunicação, com a redação da nota e do resumo executivo.

Cada prompt foi escrito por inteiro pelo autor, com os blocos PAPEL, CONTEXTO, TAREFA (em passos curtos), DADOS, EXEMPLO DE FORMATO e FORMATO. Os blocos aplicam os cinco princípios do prompting: dar direção, especificar o formato, fornecer exemplos, avaliar a qualidade e dividir o trabalho. Em todos os prompts, a IA deve indicar a origem de cada número ou escrever "NÃO CONFIRMADO".

## Entregáveis

| Arquivo | Conteúdo |
|---|---|
| `entregaveis/chat_exportado.md` | Exportação do chat com todos os prompts e respostas. |
| `entregaveis/Nota_Tecnica_Roubo_Veiculos_2025x2024.docx` | Nota técnica em Word: resumo executivo de até 70 palavras e seções de 1 a 6 (objetivo e método, resultados no estado, resultados por região, recuperação de veículos, limitações e encaminhamentos). O cabeçalho traz o nome do autor, a data e a declaração de uso de IA. |
| `entregaveis/Previsao_Tokens.docx` | Previsão do consumo de tokens: medição na nota modelo, tabela por fase, comparação com a janela de contexto, estimativa para o CSV e comparação entre o previsto e o real. |
| `codigo/analise_tp2.ipynb` | Código que lê o CSV, monta o quadro por região e ano, valida o JSON e o YAML, confere os números da nota e mede os tokens. |

Arquivos de apoio:

| Arquivo | Conteúdo |
|---|---|
| `prompts/roteiro_prompts_crispdm.md` | Roteiro dos prompts usados em cada fase. |
| `entregaveis/correcoes_modelo.md` | Registro dos erros do modelo e das correções. |
| `saidas/` | Quadro por região e ano em JSON e YAML (8 registros: 4 regiões e 2 anos). |

## Resultados conferidos

Os totais do estado, conferidos contra o CSV, são:

| Indicador | 2024 | 2025 |
|---|---|---|
| Roubo de veículos | 30.930 | 25.235 |
| Veículos recuperados | 19.034 | 17.406 |
| Furto de veículos | 17.337 | 17.490 |
| Roubo de carga | 3.437 | 3.113 |

A razão entre veículos recuperados e veículos roubados não é tratada como taxa de recuperação. A nota não atribui as variações a causas, e a base não permite calcular taxas por habitante ou por frota.

## Como reproduzir a conferência

Instale as dependências de `requirements.txt` (`pandas`, `tiktoken` e `pyyaml`), coloque o CSV em `data/BaseDPEvolucaoMensalCisp.csv` e execute o `codigo/analise_tp2.ipynb` de cima para baixo.

## Ferramentas de IA

**No chat do caso (o objeto do estudo):**

- Ferramenta: ChatGPT (OpenAI).
- Modelo: GPT-6 Astra.
- Data de uso: 09/11/2026.

**Na produção deste repositório (código, roteiro e documentação):**

- **Claude Sonnet 5.5 (Cursor):** discussão do trabalho, estruturação, desenho e revisão dos prompts e revisão do código.
- **Grok 4.6 (Cursor):** escrita do código (`analise_tp2.ipynb`) e deste `README.md`.

Os números da nota foram conferidos pelo autor contra o CSV do ISP-RJ antes da assinatura. A IA não substitui essa conferência. Ela não pode afirmar causas, taxas por habitante ou por frota, nem cifras que não estejam na base.
