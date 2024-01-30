Seguindo após entender o conteúdo da aula [[5 Flow 2]].



## O que são Logical Fields?
Eles são representações lógicas dos campos das Entidades (Vemos em  [[4.3 Mapeamento de entidades]] ). Que são representados geralmente por nossas tabelas no nosso banco de dados Oracle.


###### Criando um Logical Field:
Para criamos os campos lógicos de uma entidade, devemos seguir o caminho:

Aba lateral esquerda -> Configurações -> Data model -> List Entities -> Entidade -> 
03 Logical Fields.

Chegando nessa página, devemos clicar em gerar campos lógicos (generate logical fields).

Feito isso, abre uma janela em que devemos adicionar o sufixo do nosso campo lógico, a pasta, domínio e tags.

###### Em sufixo:
devemos colocar o que representa esse campo lógico e a entidade, ou seja, o nome da tabela dessa entidade.

###### Em pasta:
Por motivos de organização, devemos criar uma nova pasta na raiz da nossa aplicação (root), onde todas os nossos logical fields serão armazenados.

###### Em Domínio e tags:
basicamente é obrigatório ter um domínio, então devemos adicionar ou criar dependendo da nossa aplicação. E em tags, seguindo a mesma tags dos outros objetos da sua aplicação.


## Para quê servem os Logical Fields?
Os logical fields, servem para criar visões de gráficos e representar as informações das colunas da tabela no portal da aplicação.


###### Criando um logical field que representa uma fórmula:
Podemos na nossa lista de logical fields, copiar um existente e alterá-lo em função de criar um novo logical field (que não mais representa um campo da nossa entidade), que agora representa uma fórmula entre um ou mais campos (por ex com do vídeo, a diferença entre o campo de dívida e pagamento).

> [!NOTE] Nota
> É importante que o nosso novo logical field tenha o mesmo tipo do resultado da nossa fórmula