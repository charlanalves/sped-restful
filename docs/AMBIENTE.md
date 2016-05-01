# RestNFe
# Gestão de Ambiente Operacional
Neste bloco estão contidos os métodos necessários para a gestão das condições operacionais do sistema.

## Ambiente
Retorna qual o ambiente que está ativo no sistema

**GET:** http://dominio/restnfe/usuario/$id/ambiente
Retorno de status HTTP: 200

Retorno:
```json
    {
      "bStat": true,
      "tpAmb": "2",
      "descricao": "homologação"
    }
```

##Editar Ambiente
Especifica em qual ambiente o aplicativo deve operar.

>**ATENÇÃO:**
>Cuidado ao editar ou modificar o ambiente, pois os dados enviados ao embiente de produção e aceitos terão validade fiscal.

**POST:** http://dominio/restnfe/usuario/$id/ambiente
tpAmb = tipo de ambiente 1-produção ou 2-homologação
>Se nenhum dado for passado o comando será ignorado.

Parametros:
```json
  {
    "tpAmb" : "2"
  }
```

Retorno de status HTTP: 200

Retorno:
```json
    {
      "bStat": true,
      "tpAmb": "2",
      "descricao": "homologação"
    }
```

## Contingência
Checa se está ativada a contingência

**GET:** http://dominio/restnfe/usuario/$id/contingencia

Retorno de status HTTP: 200

Retorno:
```json
    {
      "bStat": true,
      "tipo": "",
      "motivo": "",
      "hora": ""
    }
```
>Caso retornem dados vazios então a emissão é **"normal"** e não contingência, de outra forma serão retornados os dados da contingência.


## Ativar Contingencia

Ativa o modo de contingência SVC-AN ou SVC-RS, dependendo do estado do emissor.

**POST:** http://dominio/restnfe/usuario/$id/contingencia

>O parametro motivo é obrigatório

Parametros:
```json
  {
    "motivo" : "motivo declarado para a entrada em contigencia"
  }
```

Retorno de status HTTP: 200

Retorno:
```json
    {
      "bStat": true,
      "tipo": "SVCAN",
      "motivo": "motivo declarado para a entrada em contigencia",
      "hora": "2016-04-21T13:33:14-03:00"
    }
```

## Desativar Contingência
Desativa o modo de contingência SVC-AN ou SVC-RS. Para desativar o modo de contingência mantenha o campo motivo em "branco" (vazio)

**DELETE:** http://dominio/restnfe/usuario/$id/contingencia

Retorno de status HTTP: 200

Retorno:
```json
    {
      "bStat": true,
      "tipo": "",
      "motivo": "",
      "hora": ""
    }
```

## Modelo de NFe
Retorna o modelo base setado no sistema.
>Existem dois modelos possiveis para NFe o modelo "55", para NFe, e o modelo "65", para NFCe.

**GET:** http://dominio/restnfe/usuario/$id/modelo

Retorno de status HTTP: 200

Retorno:
```json
    {
      "bStat": true,
      "modelo": "55"
    }
```
>O modelo indicado por esse método é apenas um indicativo referente à maior quantidade de operações. Mas de forma operar da aplicação é "inteligente" o suficiente para tratar cada caso, sejam do modelo "55" ou do modelo "65" direcionando todas as operações aos webservices corretos.

## Editar Modelo de NFe

**POST:** http://dominio/restnfe/usuario/$id/modelo
Parametros:
```json
  {
    "modelo" : "55"
  }
```

Retorno de status HTTP: 200

Retorno:
```json
    {
      "bStat": true,
      "modelo": "55"
    }
```

## Protocolo SSL
Este método retorna o protocolo setado para uso na comunicação SOAP

**GET:** http://dominio/restnfe/usuario/$id/protocolssl

Retorno de status HTTP: 200

Retorno:
```json
    {
      "bStat": true,
      "ssl": "SSLv3"
    }
```

## Editar Protocolo SSL
Este método força o uso de um determinado protocolo de criptografia "https"
>Algumas vezes ocorre do servidor estar "mal configurado" ou por problemas durante o "handshake" entre o cliente cURL e o servidor. E devido a isso o PHP não consegue identificar qual é o protocolo a ser usado naquele caso e de forma automática.
>Então é necessário **FORÇAR** um determinado protocolo para que a operação seja realizada.

**POST:** http://dominio/restnfe/usuario/$id/protocolssl
Parametros:
```json
  {
    "ssl" : "TLSv1"
  }
```

Retorno de status HTTP: 200

Retorno:
```json
    {
      "bStat": true,
      "ssl": "TLSv1"
    }
```

