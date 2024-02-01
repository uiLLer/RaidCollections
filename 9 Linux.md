Seguindo após entender o conteúdo da aula [[8 Oracle]].
Nessa aula veremos os principais conteúdos de pastas e a navegação pelo servidor linux das nossas aplicações.

Configs:
configuração da instalação das instâncias, não utilizamos muito durante do dia a dia.

Data:
Se refere a algum tipo de dado de arquivo que vai ser carregado ou lido pelo sistema (onde colocamos o input de dados)

Interface:
geralmente onde ficam arquivos que vão ser criados por alguma interface de cobrança de alguma aplicação

Licence:
São licenças específicas para quando se instala a aplicação e precisa ser renovado a licença

Software:
geralmente não vamos usar essa pastas após a instalação

Util:
São alguns comandos que colocamos como atalho para executar uma função para gerenciamento da aplicação (algum sql ou script usado periodicamente)

/servers:
onde tem os serviços da instância do portal e do produto 
O portal se diz respeito a conexão dos usuários via navegador.
Dentro da pasta portal, tem a pasta de binários, que são alguns scripts que são usados para criação da instância e manutenção de instância. Tem a parte da instância e a de log, que são todos os logs da instância.
A parte mais importante é a da instância, dentro da instância de portal temos as pastas:

`(~/prd/CB80/servers/portal/instances/Portal/)`

`backup, para salvar algum estado da instância antes de algum update;`

`bin, que contém alguns scripts, que contém dois comando de start e stop. Para baixar ou subir a instância em memória, para alguma manutenção o correção;`

`config, que diz a respeito de licenças, registros e configurações do xml do produto referentes a parâmetros de configuração de instâncias do portal;`

`log que podemos usar o comando 'tail' para visualizar algum arquivo de auditoria;`
`log/catalina.out, que se refere a um arquivo de log da instância do portal (quem conectou/saiu da sessão);`

`patch, que são patchs de atualização do sistema, onde se precisa abrir algum chamado de alguma feature que não existe no sistema para os responsáveis pela manunteção;`

`~/prd/CB80/servers/portal/instances/Portal/portal-servers/web: que refere-se a possibilitar ao usuários acessar via navegador a aplicação`.

### ~/prd/CB80/servers/product:
`/bin: scripts referentes a instalação e manutenção de instâncias do produto;`

`/patch: corretivas ou atualizações do produto;`

`/software: referente a alguns arquivos utilizados na instalação do produto;`

`/instances/CB: onde está o core do produto;`

`/instances/CB/bin: onde tem scripts importantes do produto;`

`/instances/CB/config: onde tem arquivos de configuração do produto;`

`/instances/CB/log tail CB.log: um aquivo de log que registra os eventos que estão acontecendo na aplicação (por ex quando dá algum erro de fluxo);`

`/instances/CB/data/file-repository: uma pasta para onde vão os arquivos que são feitos o upload através de uma tela na aplicação (que fica dentro do CB ou do RAS);`

`/instances/CB/export: é uma pasta customizada criada para manutenção;`

`/instances/CB/patch: diz respeito a arquivos de configuração da aplicação para fazer algum update na aplicação.`


Dentro do no CB também temos alguns arquivos que referem-se ao conexão Oracle (que não necessariamente precisa estar dentro dessa mesma máquina) e o Java, já que a aplicação é toda baseada em java.
