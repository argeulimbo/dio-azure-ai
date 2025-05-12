# [Bootcamp Bradesco DIO] Serviços Cloud de Inteligência Artificial


### Capacidades de processamento de linguagem natural no Azure - Análise de texto e resposta a perguntas
* Analisando texto: "Passei férias maravilhosas na frança"
 - Idioma predominante: Português
 - Sentimento: 0,88 (positivo)
 - Frases-chave: "férias maravilhosas"
 - Entidades: França

* Serviço de Bot do Azure
 - Plataforma baseada em nuvem para desenvolvimento e gerenciamento de bots
 - Integração com AI language e outros serviços
 - Conectividade através de vários canais

* Compreensão da linguagem coloquial
 Exemplo: "Acenda a Luz."
    - entidade: luz
    - intencional: [imagem de lâmpada]

* Reconhecimento e síntese de fala
 - Use recursos de conversão de texto em fala do Serviço de Fala para gerar fala audível a partir de texto.
- - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - -

## [ Azure Cognitive Search: AI Search para indexação e consulta de Dados ]

* Soluções de Pesquisa Cognitiva do Azure
 - Ingestão de dados
    -> Azure Blob Storage containers 
    -> Azure Data Lake Storage Gen2
    -> Azure Table Storage

 - Enriquecimento de índice de IA: torna o conteúdo mais útil para fins de pesquisa
    -> Permite uma compreensão mais profunda
    -> Visão, Processamento de Linguagem Natural, etc
    -> A indexação torna o conteúdo pesquisável
 - O conteúdo enriquecido é criado por conjuntos de habilidades como:
    -> Reconhecer entidades no texto
    -> Traduzir texto
    -> Avalie o sentimento
 - Um conjunto de habilidades produz documentos enriquecidos 
    -> Consumido durante a indexação
    -> Os dados serializados são passados ao mecanismo de pesquisa para indexação
- - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - -

## [ Fundamentos da IA Generativa ]
Temas abordados: I. Conceitos básicos de IA gerativa, II. Conceitos básicos do Serviço OpenAI do Azure, III. Explorando a IA Gerativa Responsável

* O que é IA generativa?
IA: imita o comportamento humano usando aprendizado de máquina para interagir com o ambiente e executar tarefas sem instruções explícitas sobre o que gerar.
IA generativa: cria conteúdo original, como IA gerativa que foi incorporada a aplicativos de chat. Os aplicativos de IA gerativa usam entrada em linguagem  natural e retornam respostas apropriadas em uma variedade de formatos: 
 - Geração de linguagem natural
 - Geração de código
 - Geração de imagem
## [ Fundamentos da IA Generativa ]
Temas abordados: I. Conceitos básicos de IA gerativa, II. Conceitos básicos do Serviço OpenAI do Azure, III. Explorando a IA Gerativa Responsável
* O que é IA generativa?
IA: imita o comportamento humano usando aprendizado de máquina para interagir com o ambiente e executar tarefas sem instruções explícitas sobre o que gerar.
IA generativa: cria conteúdo original, como IA gerativa que foi incorporada a aplicativos de chat. Os aplicativos de IA gerativa usam entrada em linguagem  natural e retornam respostas apropriadas em uma variedade de formatos: 
 - Geração de linguagem natural
 - Geração de código
 - Geração de imagem

* Modelos de linguagem grandes
Os aplicativos de IA gerativa são alimentados por LLMs (modelos de linguagem grandes),  que são um tipo especializado de modelo de machine learning que pode ser usado para executar tarefas de PLN (processamento de linguagem natural), incluindo:
 - Determinar sentimento ou classificar de outra forma o texto em idioma natural
 - Resumir um texto
 - Comparar várias fontes de texto quanto à similaridade semântica
 - Geração de nova linguagem natural

 [ Transformador ]
 A arquitetura do modelo do transformador consiste em dois componentes principais ou blocos
 - um bloco codificador que cria representações semânticas do vocabulário de treinamento
 - um bloco decodificador que gera novas sequências de linguagem
 - o texto é tokenizado para que cada palavra/frase seja representada por um token numérico exclusivo
 - inserções (valores de vetor com várias dimensões) são atribuídas ao token
 - as camadas de atenção examinam cada token por vez e determinam valores incorporados que refletem os relacionamentos semânticos entre tokens
 - no Decodificador, essas relações são usadas para prever a sequência mais provável de tokens
 
 01 - Tokenização
 A primeira etapa no treinamento de um modelo de transformador é decompor o texto de treinamento em tokens. Frase de exemplo:
 "Eu ouvi um cachorro latir alto para um gato"
 "EU"=1 "ouvi"=2 "um"=3 "cachorro"=4 "latir"=5 "alto"=6 "para"=7 "gato"=8
A frase é representada -> [1 2 3 4 5 6 7 3 8]
Logo, os elementos que se repetem são tokenizados apenas uma vez

 02 - Inserções
 As relações entre tokens são capturadas como vetores, são inserções

 03 - Atenção
 Capture a força das relações entre tokens usando a técnica de atenção
 - Meta: prever o token após "cachorro"
 - Represente "Ouvi um cachorro" como vetores
 - Atribua mais peso a "ouvi" e "cachorro"
 Exemplo prático: "Ouvi um cachorro latir" - frase válida, requer ATENÇÃO ao validar, pois "Ouvi um cachorro MIAR" já não faria sentido

[ Copilots ou Copilotos ]
 São frequentemente integrados a outros aplicativos e fornecem uma maneira para os usuários obterem ajuda com tarefas comuns a partir de um modelo generativo de IA. Pode ser criado por DEV's e enviam prompts para grandes modelos de linguagem e gera-se conteúdo para uso em aplicativo
 - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - -

## [ Conceitos Básicos do Serviço OpenAI do Azure ]
O serviço OpenAI é a solução de nuvem da Microsofot para implantar, personalizar e hospedar modelos de linguagem grandes. Segurança corporativa com RBAC (controle de acesso baseado em função) e redes privadas. Sendo possível usar vários métodos para desenvolver soluções do Azure OpenAI como:
 1. Estúdio de IA do Azure,
 2. API REST,
 3. SDKs com suporte e CLI do Azure.

 * Modelos que o OpenAI do Azure tem suporte: GPT4, GPT 3.5, Incorporações(conjunto de modelos que podem converter texto em um formulário de vetor numérico para facilitar a similaridade de texto), DALL-E (visualização ou versão prévia, não tem SLA)

 * Funcionalidades de linguagem natural do OpenAI do Azure
Os modelos de GPT (transformadores pré-treinados generativos) são excelentes para entender e criar linguagem natural, por exemplo: 
    "Escreva instruções de receita para uma torta de frutas com base nestes ingredientes: 
       - Strawberries, Blueberries, Farinha, Ovos, Leite"
 Exemplo de resposta gerada: 
  "Instruções: ... " Ele gera a receita em si.
Os modelos GPT traduzem linguagem natural ou trechos de código em código, a geração do código vai além de só escrever o código a partir de prompts em linguagem natural.
- - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - -

### [ Explorando Recursos de IA Generativa com Copilot e OpenAI ]
*IA Generativa Responsável*
As quatro fases do processo para desenvolver e implemenar um plano de IA responsável são -> Identificar, Medida, Mitigar e Operar.

a) Identificar
 Possíveis danos relevantes para a solução planejada

b) Medida
 A presença desses danos nas saídas pela solução

c) Mitigar
 Os danos em várias camadas em sua solução para minimizar a presença e impacto deles

d) Operar
 A solução com responsabilidade definindo e seguindo um plano de implantação e de preparação operacional

