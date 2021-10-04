# Typical HTTP Verbs:

Get - Read from Database - Ler do banco de dados
Put - Update/Replace row in Database - Atualizar / substituir linha no banco de dados
Patch - Update/Modify row in Database - Atualizar / modificar linha no banco de dados
Post - Creat a new record in the database - Crie um novo registro no banco de dados
Delete - Delete form the database - Excluir do banco de dados

# Verbos HTTP:

GET
O método GET solicita a representação de um recurso específico. Requisições utilizando o método GET devem retornar apenas dados.

HEAD
O método HEAD solicita uma resposta de forma idêntica ao método GET, porém sem conter o corpo da resposta.

POST
O método POST é utilizado para submeter uma entidade a um recurso específico, frequentemente causando uma mudança no estado do recurso ou efeitos colaterais no servidor.

PUT
O método PUT substitui todas as atuais representações do recurso de destino pela carga de dados da requisição.

DELETE
O método DELETE remove um recurso específico.

CONNECT
O método CONNECT estabelece um túnel para o servidor identificado pelo recurso de destino.

OPTIONS
O método OPTIONS é usado para descrever as opções de comunicação com o recurso de destino.

TRACE
O método TRACE executa um teste de chamada loop-back junto com o caminho para o recurso de destino.

PATCH
O método PATCH é utilizado para aplicar modificações parciais em um recurso.

# Maturidade de Richardson para APIs REST

## Níveis:

### Nível 0 — POX

Esse é considerado o nível mais básico e uma API que implementa apenas esse nível não pode ser considerada REST. Nesse nível os nomes dos recursos não seguem qualquer padrão e estão sendo usados apenas para fazer invocação de métodos remotos. Nesse nível usamos o protocolo HTTP para comunicação, mas sem seguir qualquer tipo de regras para implementar os métodos.

### Nível 1 — Recursos (Resources)

Nesse nível fazemos uso de recursos para modelar a API, para representar cada recurso fazemos uso de substantivos no plural. No exemplo do crud de cliente, os recursos seriam identificados pelo substantivo “clientes”.
Um detalhe interessante é que no nível 1 já usamos os verbos HTTP de forma correta, já que se os verbos não fossem usados, as rotas de pesquisar, alterar e incluir ficariam ambíguas.

### Nível 2 — Verbos HTTP

Como já foi adiantado no nível 1, o nível 2 se encarrega de garantir que os verbos HTTP sejam usados de forma correta. Os verbos mais utilizados são GET, POST, PUT e DELETE.
Os métodos GET, PUT e DELETE são considerados idempotente. Um método é considerado idempotente quando uma requisição idêntica pode ser executada várias vezes sem alterar o estado do servidor.

### Nível 3 — HATEOAS

O nível 3 é sem dúvidas o menos explorado, muitas APIs existentes no mercado não implementam esse nível.
HATEOAS significa Hypermedia as the Engine of Application State. Uma API que implementa esse nível fornece aos seus clientes links que indicarão como poderá ser feita a navegação entre seus recursos. Ou seja, quem for consumir a API precisará saber apenas a rota principal e a resposta dessa requisição terá todas as demais rotas possíveis.

# Pirâmide de Testes

A pirâmide de testes é uma ilustração que permite visualizar de forma simples os tipos de testes, seus níveis, velocidades, complexidades e “custos”. Além disso ela busca dar um direcionamento em relação a quantidade de testes a ser implementados em cada nível.

# Importancia de Testes

✓ Sistema testado de ponta a ponta!!

✓ Evolução segura: sem quebrar funcionalidades!

✓ Teste também é forma de documentação!

✓ Integração contínua (CI)

✓ Deploy contínuo: (CD)
