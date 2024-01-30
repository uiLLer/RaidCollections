Seguindo após entender o conteúdo da aula [[6 Logical Fields]].

Nessa aula, veremos como criar uma tela, visões de datalist e entre outros elementos gráficos.

## O que é um Smart Content?
basicamente, o smart content é o conteúdo e tela da nossa página, é nele onde fazemos nossas exibições gráficas baseadas nos dados do nosso Oracle e também visualizar/comandar o nossos fluxos de dados da aplicação.

###### Como criar um Smart Content:
Para começo de conversa, iremos seguir o seguinte caminho:

Aba lateral esquerda -> Smart Content -> New Content

Após seguir esse caminho, nós acabamos de criar um novo conteúdo (Smart Content). Na nossa menu da direita, temos uma lista de componentes que podemos adicionar no nosso smart content.

```
Data list: visão tabular
Chart: visão gráfica

Restriction: filtro de dados nas telas
Date: filtro de data
Action bar: controle de ação, tanto para tela quando para os fluxos
```

Além desses conteúdos citados, podemos alterar o nosso layout de exibição, que define como está organizado nossos componentes do nosso smart content.

###### Configurando nosso smart content:

Podemos após criado, alterar o nome, descrição.
Podemos criar secções, ou seja, ao invés de criar mais de um smart content para um conteúdo específico, podemos particionar nosso smart content em várias outras telas.


## Adicionando componentes na nossa tela:
para adicionar, basta selecionar no nosso menu o componente que queremos adicionar

###### Adicionando um Datalist:
após adicionar o nosso datalist via menu, devemos selecionar qual entidade iremos representar. Nisso podemos selecionar os logical fields para serem vistos na nossa tabela.
No nosso datalist, podemos mudar a formatação da tabela e adicionar filtros (geralmente não usamos esse filtro, utilizamos um que filtra todos os componentes de uma vez)

> [!NOTA] Nota:
> Essa visão de datalist pode acabar sendo custosa, a nível de memória, se no nossa entidade tiver uma alta quantidade de registros.

###### Adicionando um Chart (Gráfico):
Ao adicionar um chart a nossa tela, devemos informar quais os logical fields vamos representar no gráfico. Depois podemos mudar a máscara dos dados, nome de apresentação dos logical fields e qual vai ser o tipo do gráfico.
Geralmente nós colocamos o gráfico acima do datalist, para apresentação ao cliente.

###### Adicionando um filtro de data(Date):
Ele é responsável por filtrar todos os conteúdos da tela pela data (no nosso exemplo, ele vai filtrar o datalist e o chart)

###### Adicionando um filtro de dados(Restriction):
Ele assim como o Date, filtra todos os conteúdos da tela, mas não especificamente pela data. Podemos filtrar por um outro logical field (como exemplo, para cpf ou cnpj).
Dentro do nosso restriction, podemos realizar uma ação após adicionar um filtro (abrir outra página, atualizar)

###### Adicionando um ActionBar:
Um ActionBar é responsável por adicionar botões de ação, como de atualizar uma página, abrir outra e etc...

###### Criar uma variável
Na parte de opções -> variáveis, podemos criar uma variável local, que quando executada uma ação em um botão. Podemos mudar/atribuir um valor á variável(No vídeo usamos o botão de atualizar criado no action bar para além de atualizar a página, usando em "the following action" a opção "atribuir variável") 

###### Adicionando um Forms:
Basicamente é um formulário (não ironicamente), e ele é uma forma do usuário que tem acesso á tela, enviar informações para serem gravadas no banco de dados da aplicação. 
dentro do foms dá para criar campos de texto, numéricos, combobox(seletor de uma lista), data e etc. Em cada campo podemos destinar onde será gravado isso, para que fluxo mandamos e etc...

###### Adicionando um File Upload:
Assim como o forms, é mais uma forma do usuário interagir/inserir dados no nosso banco de dados. Nesse caso, será o envio de um arquivo a um diretório do nosso servidor.