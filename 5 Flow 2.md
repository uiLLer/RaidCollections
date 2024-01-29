Seguindo após entender o conteúdo da aula [[4.4 Fluxo de Controle]]. Veremos nessa aula o Flow do tipo Geral, mais exemplos de utilização e tipos de tasks, uma definição de Lookup, chamada de fluxo dentro de outro e Agendamento de execução de fluxo (scheduler)

Começamos a aula com um exemplo de flow
de proposito geral (GR) de um fluxo que gera um arquivo.

A execução desse fluxo começa via um scheduler ou uma tela smart content.
No nosso exemplo, ele começa com uma task de SQL, realizando um select.

#### Task SQL:
A tesk sql basicamente é utilizada para a execução de um select no banco de dados, informamos o usuário da conexão. Podemos fazer nossa seleção utilizado um SQL bruto ou também podemos adicionar expressões java (que a utilização é explica na aba lateral de expressões).
É importante marcar a opção de múltiplos resultados, para receber todas as linhas do seu select.

> [!NOTA] Nota
> Cada linha do resultado do select passará individualmente no fluxo, deve-se fazer um join para juntar todos os registros. 


#### Task File Generator:
Essa task, basicamente, cria um arquivo. 
Devemos informar o caminho juntamente com o nome do arquivo.
Podemos adicionar uma configuração de cabeçalho(utilizando as variáveis criadas numa task de transformação específica para header) e de linha (com as variáveis da task de transformação de detalhe de linha).


#### Task XLS:
basicamente funciona do mesmo jeito da file generator, mas para arquivos XLS(excel) e adicionando a função de carregar um (ler um arquivo XLS e carregar os dados para o nosso fluxo)

#### Task IF (condicional):
Ela basicamente faz a separação por condicionais (if).
Se sabemos qual o nome da variável do flow, podemos escrever diretamente(ao invés de procurar pela aba de expressões) "{Flow::<nome_do_campo>}".

> [!NOTE] Nota:
> Vale ressaltar que podemos fazer uma condional diretamente na task transform

#### Lookup:
uma lookup é uma verificação que fica armazenada na memória, por fim de fazer um balanceamento de memória. Quando colocamos para fazer uma verificação via select no nosso banco de dados, demandamos abrir uma conexão, verificar uma condicional para cada registro e fechar conexão, o que para nível de milhares de registros, pode ocasionar um overfow de memória ou uma sobrecarga na aplicação.


#### Chamada de um fluxo dentro de outro:
podemos por meio da task flow, fazer a chamada de um outro fluxo dentro do nosso atual. Como exemplificado no vídeo, por meio do fluxo geral podemos chamar a execução do fluxo de controle que controla nosso fluxo de carga (criado na aula [[4.1 Fluxo de Carga de Dados]]


#### Agendamento de execução de um fluxo (Scheduler):

Um scheduler é responsável por fazer uma execução sistematizada/agendada sem a necessidade do comando de um utilizador.
Podemos definir o período de execução, diário, semanal, etc... Horários e entre outras configurações como mencionadas no vídeo (Não é algo muito complexo, por isso a breve explicação).