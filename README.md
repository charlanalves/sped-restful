# RestNFe

>NOTA:este projeto está apenas na fase de dellineamento sem nenhuma estrutura construida ainda.

RestFul Service para gestão das NFe

A intenção por trás dessa aplicação é montar um servidor RestFul que poderá ser acessado pelos **"Usuários"** cadastrados e fazer todo os processos de gestão das NFe, como:

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
- Armazenamento e backup de NFe e outros documentos (emitidos e recebidos)
- Envio de emails com a NFe, CCe ou Cancelamento

## [Instalação](docs/INSTALL.md)

## [Configuração](docs/CONFIGURE.md)

## [Gestão de Usuários](docs/USUARIOS.md)
Esses métodos alteram os dados do usuário do sistema e seus recursos.

1. [Listar Usuários](docs/USUARIOS.md#listar-usuários)
2. [Cadastrar Usuários](docs/USUARIOS.md#cadastrar-usuários)
2. [Editar Usuário](docs/USUARIOS.md#editar-usuário)
3. [Deletar Usuário](docs/USUARIOS.md#deletar-usuário)
4. [Dados do Certificado](docs/USUARIOS.md#dados-do-certificado)
5. [Upgrade de certificado digital do *"Usuário"*](docs/USUARIOS.md#upgrade-do-certificado)

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

## [Acesso aos Documentos Emitidos](docs/STORAGE.md)

1. [Lista NFe emitidas](docs/STORAGE.md)
2. [Download NFe emitida](docs/STORAGE.md)
3. [Download CCe emitida](docs/STORAGE.md)
4. [Danfe](docs/STORAGE.md#danfe)
5. [Danfce](docs/STORAGE.md#danfce)
6. [DaCCe](docs/STORAGE.md#dacce)

## [Acesso aos dados de LOG](docs/LOG.md)
Esses métodos permitem o acesso aos dados de LOG destinados a auxiliar o desenvolvedor ou o usuário a encontarr a causa de problemas.

1. [Listar Log](docs/LOG.md)
2. [Limpar LOGs](docs/LOG.md#limpar)

## [Segurança e Acessos](docs/SECURITY.md)
