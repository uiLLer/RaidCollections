Seguindo após entender o conteúdo da aula [[7 Smart Content - Telas]].

Nessa aula, veremos sobre as conexões ORACLE e suas finalidade, registros de tabelas do nosso raid


## Conexões Oracle:

###### COREAPP:
Serve de comunicação entre a aplicação e o portal do raid, utilizando o esquema de grants e sinônimos

###### COREADM:
Onde vão estar a maioria dos dados e objetos do sistema

###### PORTALADM:
Onde vamos visualizar informações de permissões de usuários, raid e dados de usuários e grupos de usuários.

###### PORTALAPP:
É uma camada de comunicação entre o portal adm e o raid

###### DAT:
Onde vão estar as principais informações do negócio do cliente e algumas tabelas já prontas para modelar a soluções para o cliente(basicamente é onde estão tabelas do cliente)

## Informações guardadas nas tabelas:

###### ACM_T_CASE:
Onde estão os casos que foram criados no raid, que é um estudo de algum comportamento criado no raid.
Como por exemplo quando um cliente acerta um certo limite de dívida e isso dispara uma caso de tratamento por alguma entidade, tipo enviar um email de cobrança.

###### AF_T_OBJ_SPEC:
É onde estão registrados todos os objetos criados no raid (logical fields, telas e etc...) junto com a descrição e outras informações. Podemos buscar se um objeto existe ou não, basta fazer um pesquisa nessa tabela

###### AF_T_OBJ:
Carrega a definição do objeto em um .xml e também guarda as versões e respectivas definições.

###### BPM_C_RUNNING_FLOWS:
que mostra os flow que estão em execução
###### DP_C_COTROL:
Dados do flux de controle, que executam os fluxos de carga e outros processos.

###### DP_C_INPUT:
Onde tem um resumo de quanto dados foram executados em um fluxo de carga e o status dele.

	[...]