# RestNFe

## Gestão de Usuários
Atraves desses serviços é possivel incluir, modificar ou remover os usuários da aplicação.
O usuário é uma referência a empresa emitente de NFe e todos os dados são obrigatórios.
>Além dos dados do usuário também devem ser passados o certificado digital, após o usuário haver sido cadastrado com sucesso.

## Listar Usuários
Serão retornados quantos usuários estiverem cadastrados.
>Somente o administrador do sistema tem acesso a essa lista.

**GET:** http://dominio/restnfe/usuario

Retorno de status HTTP: 200 (Success)

Retorno:

```json
    {
        "bStat": true,
  	    "users": [
  		    {
                "id": "",
    			"nome" : "",
    			"razao": "",
    			"logradouro": "",
    			"numero": "",
    			"complemento": "",
    			"municipio": "",
    			"UF": "",
    			"cep": "",
    			"logo": "",
    			"cnpj": "",
    			"ie": "",
    			"im": "",
    			"CNAE": "",
    			"CSC": "",
    			"CSC_id": "",
    			"IBPT": "",
    			"email": "",
    			"pass": "",
    			"smtp": "",
    			"port": "",
    			"ssl": "",
    			"fromname": "",
    			"replyto": ""
  			}
        ]
    }
```

## Cadastrar Usuários

> O cadastro de novos usuários somente poderá ser feito pelo próprio administrador do sistema.

**POST:** http://dominio/restnfe/usuario

> Todos os parametros são considerados obrigatórios e devem existir mesmo que como uma string vazia.

Parametros:
```json
  {
    "nome" : "",
    "razao": "",
    "logradouro": "",
    "numero": "",
    "complemento": "",
    "municipio": "",
    "UF": "",
    "cep": "",
    "logo": "",
    "cnpj": "",
    "ie": "",
    "im": "",
    "CNAE": "",
    "CSC": "",
    "CSC_id": "",
    "IBPT": "",
    "email": "",
    "pass": "",
    "smtp": "",
    "port": "",
    "ssl": "",
    "fromname": "",
    "replyto": ""
  }
```
Retorno de status HTTP: 200 (Success)

Retorno:
```json
	{
        "bStat": true,
        "id": "",
    	"token": ""
    }
```


## Editar Usuário

> A edição dos dados do usuário poderá der feita a partir da autenticação do próprio usuário ou do administrador do sistema

$id = id do usuário

**PUT:** http://dominio/restnfe/usuario/$id

> Todos os parâmetros são considerados obrigatórios e devem existir mesmo que como uma string vazia.

Parâmetros:
```json
  {
    "nome" : "",
    "razao": "",
    "logradouro": "",
    "numero": "",
    "complemento": "",
    "municipio": "",
    "UF": "",
    "cep": "",
    "logo": "",
    "cnpj": "",
    "ie": "",
    "im": "",
    "CNAE": "",
    "CSC": "",
    "CSC_id": "",
    "IBPT": "",
    "email": "",
    "pass": "",
    "smtp": "",
    "port": "",
    "ssl": "",
    "fromname": "",
    "replyto": ""
  }
```
Retorno de status HTTP: 200 (Success)

Retorno:
```json
	{
        "bStat": true,
        "id": "",
    	"token": ""
    }
```

## Deletar Usuário

> A remoção do usuário somente poderá ser feita com a autenticação do administrador do sistema.

**DELETE:** http://dominio/restnfe/usuario/$id

Retorno de status HTTP: 200 (Success)

Retorno:
```json
	{
    	"bStat": true
    }
```

## Dados do Certificado

> Os dados referentes ao certificado digital atual, poderão ser obtidos pelo próprio usuário ou pelo administrador apenas.

**GET:** http://dominio/restnfe/usuario/$id/certificado

$id = id do usuário

Retorno de status HTTP: 200 (Success)

Retorno:
```json
	{
        "bStat": true,
        "validade": "2016-04-21",
        "timestamp": "1461207600",
        "cnpj": "99999999999999"
    }
```

## Upgrade do Certificado

> A inclusão ou renovação do certificado digital poderá ser feita apenas pelo próprio usuário ou pelo administrador.

$id = id do usuário

**POST:** http://dominio/restnfe/usuario/$id/certificado

Parametros:

pfx = certificado pfx comprimido com gzip e convertido para base64

senha = password de segurança do certificado

cadeia = cadeia de certificação do certificado digital, comprimido com gzip e convertido para base64

>O certificado pfx é **"OBRIGATÓRIO"**, bem como a **"SENHA"**, já a cadeia de certificação completa poderá ou não ser necessária para algum SEFAZ. Se não for necessária deixar string vazia.

```json
	{
        "pfx": "",
    	"senha": "",
        "cadeia": ""
    }
```
Retorno de status HTTP: 200 (Success)

Retorno:
```json
	{
    	"bStat": true
    }
```



