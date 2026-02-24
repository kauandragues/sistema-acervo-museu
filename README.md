# Sistema de Acervo — TCC

Projeto de sistema web para gerenciamento de acervo (obra e usuários), desenvolvido como trabalho final de curso. A aplicação foi implementada com PHP, HTML, CSS e JavaScript com foco em operações básicas de CRUD, autenticação e controle de privilégios administrativos.

## Visão geral

O sistema permite:
- Listar e buscar obras no acervo.
- Cadastrar, editar e excluir obras (área administrativa).
- Gerenciar usuários (bloquear/desbloquear, cadastrar).
- Favoritar/desfavoritar obras (funcionalidade de usuário).

## Tecnologias

- PHP (arquivos .php)
- MySQL (ou MariaDB) para persistência
- HTML, CSS, JavaScript para interface
- Estrutura simples para execução local em Apache/XAMPP

## Requisitos

- PHP 7.4+
- Servidor web (Apache via XAMPP, WAMP ou similar)
- MySQL/MariaDB

## Instalação rápida (modo local)

1. Instale um stack local (recomendado: XAMPP).
2. Copie a pasta do projeto para a pasta pública do servidor (por exemplo, `htdocs/tcc`).
3. Crie um banco de dados no MySQL (por exemplo, `tcc_db`) e importe o dump SQL fornecido (se houver).
4. Atualize as credenciais de conexão em `connection/conectar.php` para apontar para seu servidor MySQL:

```php
// exemplo em connection/conectar.php
$host = 'localhost';
$user = 'root';
$pass = '';
$dbname = 'tcc_db';
```

5. Acesse a aplicação no navegador: `http://localhost/tcc/` (ou o caminho onde você colocou o projeto).

## Estrutura principal do projeto

- `index.php` — página inicial pública
- `login.php` — página de autenticação
- `acervo.php` — listagem pública de obras
- `acervoAdmin.php` — visão do acervo para administradores
- `indexAdmin.php` — painel administrativo
- `indexLogado.php` — painel para usuário autenticado
- `gerenciarObra.php` — CRUD de obras (admin)
- `cadastrarObra.php`, `alterarObra.php`, `excluirObra.php` — operações de obra
- `gerenciarUsuario.php` — gerenciamento de usuários (admin)
- `favoritar.php`, `desfavoritar.php` — ações de favorito
- `connection/conectar.php` — arquivo de conexão com o banco (configurar credenciais aqui)
- `css/`, `js/`, `images/` — recursos de front-end

Ver o código-fonte para detalhes de cada página e fluxos.

## Uso básico

1. Acesse `login.php` e entre com uma conta criada (ou crie uma via `cadastrarLogin.php`, se disponível).
2. Para administrar o acervo, entre com um usuário com privilégios administrativos e acesse `indexAdmin.php`.
3. Usuários comuns podem navegar pelo acervo em `acervo.php` e favoritar obras.

