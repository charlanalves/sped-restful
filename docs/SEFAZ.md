# Sped-RestFul

# Acessos a SEFAZ

## Consulta de Cadastro

**PUT:** http://dominio/restnfe/sefaz/cadastro


## Status da NFe

#### Dados de status da NFe pelo numero do recibo de entrega do lote

$id = numero do recibo

**GET:** http://dominio/restnfe/sefaz/recibo/$id

Retorno de status HTTP: 200 (Success)

Retorno:
```json
    {   "bStat": true,
        "versao": "",
        "tpAmb": "",
        "cStat": "",
        "verAplic": "",
        "xMotivo": "",
        "dhRecbto": "",
        "cUF": "",
        "nRec": "",
        "aProt":
            [
                {
                    "chNFe": "",
                    "dhRecbto": "",
                    "nProt": "",
                    "digVal": "",
                    "cStat": "",
                    "xMotivo": ""
                },
                {
                    "chNFe": "",
                    "dhRecbto": "",
                    "nProt": "",
                    "digVal": "",
                    "cStat": "",
                    "xMotivo": ""
                }
            ]
    }
```
Como se trata de uma busca pelo recibo de lote e um lote pode conter muitas NFe então a variável aProt[] é um array que pode conter vários retornos de 0 até 50.


### Dados de status da NFe pelo numero da chave de 44 digitos

$id = chave de 44 digitos da NFe

**GET:** http://dominio/restnfe/sefaz/chave/$id

Retorno de status HTTP: 200 (Success)

Retorno:
```json
    {   "bStat": false,
        "versao": "",
        "tpAmb": "",
        "cStat": "",
        "verAplic": "",
        "xMotivo": "",
        "dhRecbto": "",
        "cUF": "",
        "chNFe": "",
        "aProt": [
        	{   "chNFe": "",
                "dhRecbto": "",
                "nProt": "",
                "digVal": "",
                "cStat": "",
                "xMotivo": ""
                }
        ],
        "aCanc": [
            {   "tpAmb": "",
                "verAplic":"",
                "cStat":"",
                "xMotivo":"",
                "cUF":"",
                "chNFe":"",
                "dhRecbto":"",
                "nProt":""
            }
        ],
        "aEvent": [
            {   "tpAmb": "",
                "verAplic": "",
                "cOrgao": "",
                "cStat": "",
                "xMotivo": "",
                "chNFe": "",
                "tpEvento": "",
                "xEvento":"",
                "nSeqEvento":"",
                "cOrgaoAutor":"",
                "dhRegEvento":"",
                "CNPJDest":"",
                "emailDest":"",
                "nProt":"",
                "chNFePend":""
                }
        ]
    }
```
Nesse caso a pesquisa é feita sobre uma única NFe então devido a isso as variáveis aProt[0] e aCanc[0] são arrays com um único conteúdo, pois somente haverá um protoco e um póssivel cancelamento. Já no caso dos eventos a variável array aEvent[] poderá ter multiplos resultados de 0 até alguns.

