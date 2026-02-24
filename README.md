# Sistema de Acervo de Museu

Projeto de sistema web para gerenciamento de acervo (obra e usuários), desenvolvido como trabalho final de curso. A aplicação foi implementada com PHP, HTML, CSS e JavaScript com foco em operações básicas de CRUD, autenticação e controle de privilégios administrativos.

## Visão geral
<img width="1366" height="933" alt="image" src="https://github.com/user-attachments/assets/46a16e15-88eb-4ff2-89d0-fcd70d6198c7" />

O sistema permite:
- Listar e buscar obras no acervo.
<img width="947" height="934" alt="image" src="https://github.com/user-attachments/assets/1b4da220-4ed4-4a4b-bd99-c0cf1d72c326" />

- Cadastrar, editar e excluir obras (área administrativa).
<img width="1006" height="943" alt="image" src="https://github.com/user-attachments/assets/aca6dba1-94cc-4e73-8975-0b2756a6d54f" />

- Gerenciar usuários (bloquear/desbloquear, cadastrar).
<img width="1319" height="945" alt="image" src="https://github.com/user-attachments/assets/1e89072b-6d18-424e-b51e-92b562873619" />

- Favoritar/desfavoritar obras (funcionalidade de usuário).
<img width="1341" height="857" alt="image" src="https://github.com/user-attachments/assets/7bc60bbe-3fca-431f-a998-f9ce70716c96" />

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

