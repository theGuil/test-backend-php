# 🚀 Configuração Laravel no ChromeOS (Linux Penguin)

## 1. Instalar SQLite3

```bash
sudo apt update
sudo apt install sqlite3
```

## 2. Instalar PHP 8.2 e Extensões

```bash
sudo apt update && sudo apt install php php-cli php-common php-xml php-zip php-curl php-mbstring php-sqlite3 unzip sqlite3 -y
```

## 3. Instalar Composer

```bash
curl -sS https://getcomposer.org/installer | php
sudo mv composer.phar /usr/local/bin/composer
```

## 4. Instalar Laravel Installer

```bash
composer global require laravel/installer
```

## 5. Configurar Variáveis de Ambiente (PATH)

```bash
echo 'export PATH="$PATH:$HOME/.config/composer/vendor/bin"' >> ~/.bashrc
source ~/.bashrc
```

## 6. Criar Projeto e Banco de Dados

```bash
laravel new meu-projeto
cd meu-projeto
touch database/database.sqlite
php artisan migrate
```

### Instalação do SQLite

Para instalar o SQLite no Linux (Ubuntu/Debian/Penguin), execute:

```bash
sudo apt update
sudo apt install sqlite3
```

### Start server

```bash
php artisan serve
```

### Resetar as migrations (apaga todas as tabelas)

```bash
php artisan migrate:reset
```

### Resetar as migrations (recria as tabelas)

```bash
php artisan migrate
```

### Cria usuários no banco de dados apartir da seed

```bash
php artisan dd:seed
```

### Cria usuários no banco de dados apartir da seed

```bash
php artisan route:list --path=api
```
