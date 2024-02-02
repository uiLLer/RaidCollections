

10 - Atividade do Curso RAID.docx


Atividade Final do Curso RAID.
O objetivo dessa atividade é colocar em prática os tópicos e ensinamentos abordados no curso RAID.

Essa atividade consiste em carregar dados sobre seu assunto pré-determinado (solicitar para jonatan.campos@sortech.com.br) e apresentá-los em uma tela na plataforma RAID.
Orientações Gerais:  
	A)  Os objetos criados na plataforma devem conter no final do nome a identificação do seu usuário.
	B) Adicionar a TAG CURSO_RAID aos objetos criados na plataforma RAID.
	C)  Criar um .docx contendo os comandos SQL e Linux utilizados, lista de objetos criados na plataforma RAID e uma breve explicação de como foi realizado o processo de carga.
	D) Enviar o documento .docx para o e-mail jonatan.campos@sortech.com.br para avaliação.
Será analisada a capacidade de interpretação, qualidade e progresso das etapas realizadas, engajamento e redação.

Etapas da atividade de carga de dados.
1. Criar um arquivo .csv com dado do assunto elencado com as seguintes diretrizes.
a. 10 a 20 linhas de dados e um cabeçalho;
b. 5 a 10 colunas;
c. Colunas com os tipos de dados String, date, integer e double;
2. Criar uma pasta no Linux e fazer o upload do arquivo para a pasta.
3. Criar uma tabela Oracle para guardar as informações do arquivo.
a. Criar Tabela na conexão CBCOREADM;
b. Criar Grants de SELECT, INSERT, DELETE e UPADTE da tabela para a conexão CBCOREAPP;
c. Criar Sinônimo na conexão CBCOREAPP para a tabela criada na conexão CBCOREADM.
4. Criar e atribuir permissões para seu usuário na plataforma RAID e utilizá-lo nas seguintes atividades;
5. Criar uma Entidade e Logical Fields pelo menu Data Model para representar a tabela Oracle criada;
6. Realizar a carga do arquivo CSV utilizando a plataforma RAID criando os seguintes tipos de objetos do menu Smart Dada Stream:
a. Format;
b. Stream;
c. Loading Flow;
d. Loading Process;
e. Control Flow;
7. No Loading Flow conter as seguintes diretrizes:
a. Criar variáveis para utilizar no flow;
b. Conter task transform com pelo menos 5 fórmulas para enriquecer os dados;
Conter task dump para salvar os dados na entidade;
c. Um IF;

8. Criar uma tela pelo Menu Smart Content para apresentação dos dados carregados na tabela Oracle com os seguintes componentes:
a. 1 Título;
b. 1 Datalist;
c. 1 Gráfico;
d. 1 Filtro de data (data picker);
e. 1 Filtro de dados (restriction);
f. 1 Botão para atualizar a página.
9. Adicionar o Smart Content criado a página Atividades no menu do RAID e adicionar a permissão de visualização para o USER.