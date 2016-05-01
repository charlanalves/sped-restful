# Sped-RestFul

# Instalação

A instalação pode ser feita pelo git:
```bash
git clone git@github.com:robmachado/restnfe.git <nome da pasta>
```
Após o Git ter instalado criado a pasta e baixado os arquivos, vá para a pasta criada.
```bash
cd <nome da pasta>
```
E instale todas as dependências com o composer:
```bash
composer install
```

## Pré-Requisitos
- PHP 5.6 ou maior
- php-curl
- php-gd
- php-mcrypt
- php-mbstring
- php-xml

## Dependências

Todas as dependências estão disponíveis no [Packgist](https://packagist.org/), e inclusas no arquivo composer.json

### Produção

- "laravel/lumen-framework": "5.2.*"
- "vlucas/phpdotenv": "~2.2"
- "nfephp-org/nfephp": "4.0.*"

### Desenvolvimento

- "phpunit/phpunit": "4.*"
- "fzaninotto/faker": "~1.4"
- "scrutinizer/ocular": "~1.1"
- "squizlabs/php_codesniffer": "~2.3"
