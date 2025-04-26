
Aws Organization, deixa eu poder criar contas secundarias, como dividir conta de produção, e QA, funciona como uma herança de POO


Policy - Permissões que o usuario tem, por exemplo administrator, elas são um JSON, com um objeto statement que tem os campos, effect, action e resources, que diz, se eu permito ou não algo, qual ação, como visualizar, criar, e em qual recurso, como s3.

ARN: Aws resource number -> numero de identificação de um serviço 


AWS funciona como se fosse uma API gigante, 

.aws/credentials -> Arquivo sensivel, onde fica chaves de acessos, 


Para se comunicar com a AWS, temos que ter duas chaves, a estática(USER), e a dinamica(ROLE -> AssumedRole)

AKIA -> Inicio estática idade vitalicia 
	-> Publica(AWS_Acess_Key_ID)
	-> Privada (AWS_Secret_Acess_Key)

ASIA  -> Inicio dinâmica dura em média 1h
	-> Publica(AWS_Acess_Key_ID)
	-> Privada (AWS_Secret_Acess_Key)
	->  AWS_Session_Token


aws sts -> gerencia tokens da aws


bucket -> serviço utilizado para fazer upload de arquivos


ec2 -> serviço para criar uma maquina virtual

URI -> s3://nomedobucket/nomedoarquivo


Problemas de segurança:

https://nomedobucket.s3.amazonaws.com/nomedoarquivo: OBJECT URL

Desbloquear todo o acesso publico, é acessavel por qualquer pessoa que tentar entrar, porém AWS criou a ACL, porque muita gente estava configurando errado. Se permitir a acl, e editar ela, ai sim, será possivel ser acessado por qualquer usuario. 

--no-sign-request -> interagir sem senha

--profile nome da conta -> interagir com uma conta já criada

grayhat warfare -> listar buckets abertos

grepgit -> pegar dados de repositorios git


Subdomain takeover de S3


168.254.169.254 -> IMDsv2 (Serviço de metadados da AWS)

TOKEN=`curl -X PUT "http://169.254.169.254/latest/api/token" -H "X-aws-ec2-metadata-token-ttl-seconds: 21600"`

curl -H "X-aws-ec2-metadata-token: $TOKEN" http://169.254.169.254/latest/meta-data/


procurar por iam

conseguimos gerar um ID, um session, e um token, pegando o security_credentials, da role que temos, e com isso, temos uma chave dinamica,


Se tiver dentro de uma instancia ec2, e você tiver algum perfil iam vinculado, eu consigo acessar esses dados, e me passar por você interagindo com a api da aws, utilizando exports na aws cli 

sts get-caller-identity, sem passar profile