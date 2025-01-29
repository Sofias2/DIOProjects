### Deploy

Precisa ter o acesso de admin o suficiente para lançar o recurso do OpenAI no Azure.

Azure Open-AI -> create -> Subscription -> resource group -> region (East US 2)-> Name -> Princing Tier - o modelo que determina o preço e não a instancia

Network -> All network (recomendado criar uma Virtual Network)

como dar deploy -> vai clicar no modelo -> implantar

### O que é playground?

- Server para ser um ambiente de testes
- ter feedback rapido, desenvolver prompts e preparar modelos


modelo de linguagem faz a analise de probabilide primeiro, gera as opções de token e uma das opções vai ser selecionada

o mesmo prompt pode gerar respostas diferentes

### Tokenização

depende da linguagem, no portgues acaba comendo algumas palavras assim gera mais tokens ao inves de gerar token de uma palavra só gera 2 tokens de uma palavra em si

gpt não vê string, ele tenta completar o proximo token

numero ele tenta pegar como texto

nicode -> uma maneira que se códifica muita coisa, se códifica por partes

os emojis são separados quando se seleciona cor e genero

tiktoken -> é a maneira que se transforma texto em numero(token)

### Parametros

**System Message**
modela - defini o contexto inicial do modelo com definição de comportamento, instruções base e limites

**shots(exemplos)**: são as maneiras de como a llm tem que se comportar

tipos:

**zero-shot**

- sem exemplos, resposta direta, baseado apenas no prompt

**one-shot**

- um exemplo


**Temperatura**

configuração de pegar as palavras na criação de texto, o quao randomico é as ligações.

medidas:

**temperatura-0:** respostas muito previsíveis, determinísticas

**temperatura-1:** respostas muito improváveis, sem sentido

**Top-p** 

quais palavras podem ser usadas na possivel escolha, seleciona as opções que vão passar para frente.

medidas:

**top-p 0.1:** só considera o primeiro eixo de palavras provaveis até dar 10% das possibilidades

**top-p 0.9:** considera muitas palavras até dar o eixo de 90% das possibilidades

**Frequency Penalty**
a penalidade por frequencia, repetição de texto/tokens

**Presence Penalty**
a penalidade por presencia, que tema esta sendo descrito, o tema descrito.

**Melhores Praticas**

- começar com defaults
- ajustar um parâmetro por vez
- documentar resultados
- alterar baseado em feedback