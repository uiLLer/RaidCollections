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

## Informações  mais importantes guardadas nas em tabelas:

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
Dados dos fluxos de controle, que executam os fluxos de carga e outros processos.

###### DP_C_INPUT:
Onde tem um resumo de quanto dados foram executados em um fluxo de carga e o status dele.

## Significados por Siglas das tabelas:

###### ACM e ACT:
são referenciadas à casos abertos por usuários, um processo de análise de dados e dependendo dessa análise, algum casos podem ser gerados para os colaboradores analisarem e realizarem alguma ação.
###### AF:
São de objetos relacionados com o sistema

###### APP:
criadas por algum projeto específico do cliente

###### BPM RUNNING FLOWS:
relacionadas a execução de fluxo

###### BSCKPI:
São relacionadas a indicadores da aplicação e pontuação

###### CBPM:
Tabelas de estatísticas de execução de fluxo

###### CFG:
São tabelas de parâmetros

COB:
São tabelas utilizadas para resolução de cliente "COB de colaborador"

###### DM_TRANSACTION:
São tabelas de transação de dados de controle e estatística

###### DP_C:
São tabelas de controle de carga

###### EH:
São tabelas de envento

###### GEN:
São tabelas geradas para implementar algumas soluções dos clientes

###### ICS:
fazem parte de algumas tabelas prontas para a solução do cliente (como exemplificado no nosso curso, a tabela final utilizada para registrar os dados)

######  RCT:
Mais tabelas criadas para soluções de clientes

###### SC, SCH, NFE, INT:
tabelas pré-determinadas do sistema

###### VW:
são tabelas utilizadas como base para uma view.
(vale ressaltar que tanto como tabelas podem ser representadas como entidades, view também podem ser mapeadas como etidade)


### Significados dos componentes de nomenclatura de uma tabela de cliente:
`SEF: Secretaria da Fazenda`
`X: indica que o objeto vai ter dados bastante completos (customizada e criada manualmente contento bastante informação específico)`
`T: indica que é uma tabela`
`R: indica que é uma tabela de referência`
`VW: indica que está relacionada com alguma view`
`L: indica que é uma tabela de ligação`
`H: indica que é uma tabela de histórico`

## Views Materializadas do raid:
### O que são views materializadas?
São views que são guardadas na memória, pois o essa view possui uma grande gama de dados, tornando como um agente que retarda o processamento da aplicação. Por isso, elas são guardadas na memória temporariamente para rápido acesso

### Quando usar uma view materializada?
Geralmente nós utilizamos dependendo do caso do cliente. Usamos por meio de atualização periódica, para facilitar o acesso de dados, usamos para tabelas que não estão constantemente em atualização (como exemplo, um relatório enorme de funcionários/serviços da empresa, que não está constantemente em atualização (possamos definir que a view seja materializada diariamente ou semanalmente).

## Procedures e Funções:
São algoritmos que interagem com o banco. Procedures não retornam um valor, já funções como normalmente reconhecidas retornam.

## Triggers:
São gatilhos para execução de uma ação (geralmente para update)