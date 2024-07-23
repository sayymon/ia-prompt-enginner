# Engenharia de prompt para uso otimizado das IA's Generativas

A engenharia de prompts é uma disciplina relativamente nova para desenvolver e otimizar prompts para usar eficientemente modelos de linguagem (LMs) para uma ampla variedade de aplicativos e tópicos de pesquisa.

As habilidades imediatas de engenharia ajudam a entender melhor os recursos e as limitações dos modelos de linguagem grandes (LLMs)

Os pesquisadores usam a engenharia de prompt para melhorar a capacidade dos LLMs em uma ampla gama de tarefas comuns e complexas, como resposta a perguntas e raciocínio aritmético. 

Os desenvolvedores usam engenharia de prompt para projetar técnicas de prompt robustas e eficazes que fazem interface com LLMs e outras ferramentas.

## O que é um prompt?

Um prompt consiste em dois componentes principais: instrução e contexto.

### Instrução

A instrução é a parte escrita do prompt que declara a tarefa e o objetivo do modelo. Por exemplo, você quer que o modelo escreva, revise, crie ou algo mais? Qual é o seu objetivo ao usar o modelo? Que tipo de informação o modelo deve usar ou evitar?

As instruções devem ser claras e específicas, para que o modelo saiba exatamente o que você espera dele. Por exemplo, se quiser que o modelo escreva um resumo de um artigo, você deve incluir o artigo, o tamanho do resumo desejado e os pontos principais a serem incluídos.

### Contexto

O contexto é a parte do prompt que fornece informações para a saída do modelo. 

Por exemplo, quem é seu público-alvo e que tom você deseja usar? Sua saída é para uso pessoal ou profissional? 

Você quer que o modelo produza uma explicação simples ou complexa de um tópico? Você está tentando persuadir usando pathos, ethos ou logos?

#### Diferença entre Pathos, Ethos e Logos
- Pathos: Apela às emoções e sentimentos do público. Na IA, isso significa criar respostas que ressoem emocionalmente com os usuários.
- Ethos: Refere-se à credibilidade e autoridade. Em IA, isso pode ser visto em sistemas que fornecem informações baseadas em fontes confiáveis e estabelecem confiança com os usuários.
- Logos: Baseia-se na lógica e razão. Na IA, isso envolve fornecer respostas claras, racionais e baseadas em dados.****

O contexto deve ser relevante e apropriado, para que o modelo possa adequar a saída às suas necessidades. 

Por exemplo, se quiser que o modelo ajude a criar um plano de treinamento sobre a utilização da IA em uma sessão de estudo, você deve informar o nível de experiência dos leitores, o estilo e o formato do plano e todas as informações que deseja que os alunos recebam.

### Dados de entrada 

É a entrada complementar a pergunta para a qual estamos interessados em encontrar uma resposta ou gerar um resultado através dos dados inseridos seja texto, Imagem/video ou audio

### Indicador de saída 

Indica o tipo ou formato da saída, podemos alem da pergunta referencias como o resultado deve ser apresentado, texto, json, tabela grafico

## Tipos de Prompt 

### Prompt de continuidade para previsão de textos contextualmente relevantes

Exemplo, se inserirmos este texto "Qual é a primeira coisa que vem à sua mente quando eu digo <prompt>?". 
 
Como resposta, o modelo fornecerá a você uma continuação do <prompt>. 
 
Com uma frase inicial da literatura popular, o modelo pode prever a próxima parte do texto. 

Isso ilustra a proficiência da IA generativa na previsão de textos contextualmente relevantes.

### Prompts Diretos 

São instruções claras e específicas, como “Resuma este artigo em 100 palavras”.

### Prompts de Contexto

Incluem informações adicionais para fornecer contexto, como “Considerando a crise climática atual, descreva as possíveis soluções”.

### Prompts de Exemplos

Fornecem exemplos para guiar a resposta, como “Aqui está um exemplo de um bom resumo: [exemplo]. Agora, resuma este artigo”.

### Prompts de Tarefas

Especificam uma tarefa a ser realizada, como “Escreva um código em Python para calcular a média de uma lista de números”.

## Principais Tecnicas

### Especificidade

Quanto mais específico for o prompt, mais precisa será a resposta. Por exemplo, ao invés de “Explique a teoria da relatividade”, use “Explique a teoria da relatividade de Einstein em termos simples para um estudante do ensino médio”.

### Contextualização

Adicionar contexto relevante pode ajudar a IA a entender melhor a solicitação. Por exemplo, “No contexto da pandemia de COVID-19, quais são os impactos econômicos mais significativos?”.

### Iteração

Refinar os prompts com base nas respostas recebidas pode melhorar a qualidade das respostas. Isso envolve ajustar e testar diferentes versões do prompt.

### Uso de Exemplos

Fornecer exemplos claros e relevantes pode guiar a IA a produzir respostas mais alinhadas com o esperado.

### Ajuste de Parâmetros

Modificar parâmetros como temperatura e top-k sampling pode influenciar a criatividade e a precisão das respostas geradas.


## Dicas 

### Comece Simples

Ao começar a criar prompts, você deve ter em mente que é realmente um processo iterativo que requer muita experimentação para obter os melhores resultados. 

Usar um playground simples como [OpenAI](https://platform.openai.com/playground/chat?models=gpt-4o) ou [Cohere's](https://dashboard.cohere.com/playground/chat) é um bom ponto de partida.

Você pode começar com prompts simples e continuar adicionando mais elementos e contexto à medida que busca melhores resultados.

O controle de versão do seu prompt ao longo do caminho é vital por esse motivo. Ao ler o guia, você verá muitos exemplos em que a especificidade, a simplicidade e a concisão geralmente lhe darão melhores resultados.

Quando você tem uma grande tarefa que envolve muitas subtarefas diferentes, pode tentar dividir a tarefa em subtarefas mais simples e continuar aumentando conforme obtém melhores resultados. Isso evita adicionar muita complexidade ao processo de design do prompt no início.

### Capriche na instrução

Você pode criar prompts eficazes para várias tarefas simples usando comandos para instruir o modelo sobre o que deseja alcançar, como "Escrever", "Classificar", "Resumir", "Traduzir", "Ordenar" etc.

Tenha em mente que você também precisa experimentar muito para ver o que funciona melhor. Experimente instruções diferentes com palavras-chave, contextos e dados diferentes e veja o que funciona melhor para seu caso de uso e tarefa específicos. Normalmente, quanto mais específico e relevante for o contexto para a tarefa que você está tentando executar, melhor. Abordaremos a importância da amostragem e da adição de mais contexto nos próximos guias.

Outros recomendam que as instruções sejam colocadas no início do prompt. Também é recomendado que algum separador claro como "###" seja usado para separar a instrução e o contexto.


### Evite Imprecisões
Dadas as dicas acima sobre como ser detalhado e melhorar o formato, é fácil cair na armadilha de querer ser muito inteligente sobre os prompts e potencialmente criar descrições imprecisas. 

Geralmente é melhor ser específico e direto. A analogia aqui é muito semelhante à comunicação eficaz - quanto mais direta, mais eficaz a mensagem é transmitida.

Por exemplo, você pode estar interessado em aprender o conceito de engenharia de prompt. Você pode tentar algo como:

Explique o conceito de engenharia de prompt. Mantenha a explicação curta, apenas algumas frases, e não seja muito descritivo.

Não está claro no prompt acima quantas frases usar e qual estilo. Você ainda pode obter uma boa resposta com o prompt acima, mas o melhor prompt seria aquele que é muito específico, conciso e direto ao ponto. Algo como:

Use 2 a 3 frases para explicar o conceito de engenharia de prompt a um aluno do ensino médio.

### Descreva o que Fazer e/ou não fazer?

Outra dica comum ao criar prompts é evitar dizer o que não fazer, mas dizer o que fazer. 

Isso incentiva mais especificidade e concentra-se nos detalhes que levam a boas respostas do modelo.

Aqui está um exemplo de um chatbot de recomendação de filme falhando exatamente no que eu não quero que ele faça por causa de como escrevi a instrução -- focando no que não fazer.

Prompt:

```
O agente a seguir recomenda filmes para um cliente. NÃO PEÇA INTERESSES. NÃO PEÇA INFORMAÇÕES PESSOAIS.
Cliente: Por favor, recomende um filme baseado nos meus interesses.
```

Saída:

```
Claro, posso recomendar um filme baseado em seus interesses. Que tipo de filme você gostaria de assistir? Você prefere ação, comédia, romance ou outra coisa?
```

Aqui está um prompt melhor:

Prompt:

```
O agente a seguir recomenda filmes para um cliente. O agente é responsável por recomendar um filme dos principais filmes de tendências globais. Deve abster-se de perguntar aos usuários sobre suas preferências e evitar pedir informações pessoais. Se o agente não tiver um filme para recomendar, ele deve responder "Desculpe, não foi possível encontrar um filme para recomendar hoje.".
Cliente: Por favor, recomende um filme baseado nos meus interesses.
Agente:
```

Saída:

```
Desculpe, não tenho nenhuma informação sobre seus interesses. No entanto, aqui está uma lista dos principais filmes de tendências globais no momento: [lista de filmes]. Espero que encontre algo que goste!
```


## Referencias

https://platform.openai.com/docs/guides/prompt-engineering/six-strategies-for-getting-better-results
https://help.openai.com/en/articles/6654000-best-practices-for-prompt-engineering-with-the-openai-api
https://www.promptingguide.ai/pt





