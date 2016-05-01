# Sped-RestFul

>NOTA:este projeto está apenas na fase de dellineamento sem nenhuma estrutura construida ainda.

RestFul Service para gestão das NFe

A intenção por trás dessa aplicação é montar um servidor RestFul que poderá ser acessado pelos **"Emitentes"** cadastrados e fazer todo os processos de gestão das NFe, como:

- Digitação de NFe e seu armazenamento em base de dados
- Gestão das NFe emitidas e Recebidas de Terceiros
- Envio de lote de NFe (incluindo a conversão de TXT para xml e assinatura)
- Busca do Status dos Webservices das SEFAZ
- Busca do Status da NFe (por recibo ou chave)
- Cancelamento de NFe
- Emissão de Carta de Correção
- Inutilização de Faixa de Numeros de NFe
- Validação de NFe recebida de Terceiros
- Consultas de NFe e outros documentos destinados ao usuário
- Manifestação de Destinatário
- Download de NFe
- Impressão da DANFE e DACCE

Serviços opcionais
- Armazenamento e backup de NFe e outros documentos (emitidos e recebidos) em arquivo
- Envio de emails com a NFe, CCe ou Cancelamento

## [Instalação](docs/INSTALL.md)

## [Configuração](docs/CONFIGURE.md)

## [Gestão de Emitente](docs/EMITENTE.md)
Esses métodos alteram os dados do Emitente do sistema e seus recursos.

O sistema deve permitir multiplos emitentes.

1. [Listar Emitente](docs/EMITENTE.md#listar-usuários)
2. [Cadastrar Emitente](docs/EMITENTE.md#cadastrar-usuários)
2. [Editar Emitente](docs/EMITENTE.md#editar-usuário)
3. [Deletar Emitente](docs/EMITENTE.md#deletar-usuário)
4. [Dados do Certificado](docs/EMITENTE.md#dados-do-certificado)
5. [Upgrade de certificado digital do *"Emitente"*](docs/EMITENTE.md#upgrade-do-certificado)

## [Gestão do Ambiente Operacional](docs/AMBIENTE.md)
Esses metodos alteram o ambiente operacional do sistema.

1. [Ambiente](docs/AMBIENTE.md#ambiente)
2. [Editar Ambiente](docs/AMBIENTE.md#editar-ambiente)
3. [Contingência](docs/AMBIENTE.md#contingência)
4. [Ativar Contingência](docs/AMBIENTE.md#ativar-contingência)
5. [Desativar Contigência](docs/AMBIENTE.md#desativar-contingência)
6. [Modelo de NFe](docs/AMBIENTE.md#modelo-de-nfe)
7. [Editar Modelo de NFe](docs/AMBIENTE.md#editar-modelo-de-nfe)
8. [Protocolo SSL](docs/AMBIENTE.md#protocolo-ssl)
9. [Editar Protocolo SSL](docs/AMBIENTE.md#editar-protocolo-ssl)

## [Gestão de NFe](docs/GESTAO.md)

A gestão permite a busca das NFe registrados no sistema bem como suas informações basicas e recuperação quando necessário.

1. [Lista NFes](docs/GESTAO.md#listar)


## [Emissão de NFe](docs/EMISSAO.md)

A emissão recebe os dados brutos da interface e grava em base de dados como rascunho (em Digitação) e permite as ações subsequentes.

1. [Carrega NFe](EMISSAO.md#load)



## [Acesso à SEFAZ](docs/SEFAZ.md)
Esses métodos interagem com o SEFAZ e retornam os resultados dessa interação.

1. [Status SEFAZ](docs/SEFAZ.md#status-sefaz)
1. [Consulta de Cadastro](docs/SEFAZ.md#consulta-de-cadastro)
2. [Envio de Lote](docs/SEFAZ.md#envio-de-lote)
3. [Status NFe Recibo (situação da NFe pelo recibo)](docs/SEFAZ.md#status-nfe-recibo)
4. [Status NFe Chave (situação da NFe pela Chave)](docs/SEFAZ.md#status-nfe-chave)
5. [Cancelar NFe](docs/SEFAZ.md#cancelar-nfe)
6. [Inutilizar Faixa](docs/SEFAZ.md#inutilizar-faixa)
7. [Validar NFe](docs/SEFAZ.md#validar-nfe)
8. [Carta de Correção](docs/SEFAZ.md#carta-de-correção)
9. [Consulta Destinados](docs/SEFAZ.md#consulta-destinados)
10. [Manifestação de Destinatário](docs/SEFAZ.md#manifestação-de-destinatário)
11. [Download de NFe](docs/SEFAZ.md#download-de-nfe)

## [Envios de Email aos Destinatários](docs/EMAILS.md)

1. [Enviar Email NFe](docs/EMAILS.md#enviar-nfe)
2. [Enviar Email CCe](docs/EMAILS.md#enviar-cce)
3. [Enviar Email Cancelamento](docs/EMAILS.md#enviar-cancelamento)

## [Acesso e Impressão dos Documentos Emitidos](docs/STORAGE.md)

1. [Lista NFe emitidas](docs/STORAGE.md)
2. [Download NFe emitida](docs/STORAGE.md)
3. [Download CCe emitida](docs/STORAGE.md)
4. [Danfe](docs/STORAGE.md#danfe)
5. [Danfce](docs/STORAGE.md#danfce)
6. [DaCCe](docs/STORAGE.md#dacce)

## [Acesso aos dados de LOG](docs/LOG.md)
Esses métodos permitem o acesso aos dados de LOG destinados a auxiliar o desenvolvedor ou o usuário a encontarr a causa de problemas.

1. [Listar Log](docs/LOG.md#listar)
2. [Limpar Logs](docs/LOG.md#limpar)

## [Segurança e Acessos](docs/SECURITY.md)
