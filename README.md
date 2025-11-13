# Sistema de Tarefas — Autenticação (Tarefa 4)

Projeto Django de exemplo para a disciplina Desenvolvimento Web II — Tarefa 4.

## Estrutura
- `tarefa4_project/` — projeto Django
- `usuarios/` — aplicação usuários com rotas de autenticação
- `templates/usuarios/` — templates `cadastro.html`, `login.html`, `dashboard.html`
- `manage.py` — utilitário Django
- `requirements.txt` — dependências

## Funcionalidades implementadas
1. Branch requisitada: crie localmente uma branch chamada `autenticacao` e faça commits.
2. Aplicação `usuarios` com rotas:
   - `/usuarios/cadastro/` — cadastro de usuário (registro com `UserCreationForm`)
   - `/usuarios/login/` — formulário de login
   - `/usuarios/logout/` — logout
   - `/usuarios/dashboard/` — página protegida (apenas para usuários autenticados)
3. Configurações em `settings.py`:
   - `LOGIN_URL = '/usuarios/login/'`
   - `LOGIN_REDIRECT_URL = '/usuarios/dashboard/'`
   - `LOGOUT_REDIRECT_URL = '/usuarios/login/'`
4. Proteção de rotas: `@login_required` em `dashboard`.
5. Instruções para executar (local):
   ```bash
   python -m venv venv
   source venv/bin/activate   # ou venv\Scripts\activate no Windows
   pip install -r requirements.txt
   python manage.py migrate
   python manage.py createsuperuser   # opcional
   python manage.py runserver
   ```
6. Git (exemplo de comandos):
   ```bash
   git checkout -b autenticacao
   git add .
   git commit -m "Implementa app usuarios e autenticação"
   git push origin autenticacao
   # depois, abrir merge request / pull request para a branch principal
   ```
## Observações
- Substitua `SECRET_KEY` em `settings.py` por uma chave segura antes de publicar.
- O banco de dados padrão é SQLite (`db.sqlite3`) — suficiente para testes locais.
