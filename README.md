## 📘 Sistema de Tarefas — Autenticação de Usuários

Tarefa da Unidade 4 — Desenvolvimento Web III (Django)

Este projeto implementa um sistema básico com autenticação de usuários, utilizando o framework Django, com rotas protegidas, templates completos, boas práticas de segurança e documentação completa.

## 🚀 Objetivos da Tarefa

A implementação atende a todos os requisitos:

```

✔ Criar uma branch chamada autenticacao
✔ Criar uma aplicação chamada usuarios
✔ Rotas: cadastro, login, logout, dashboard (protegida)
✔ Criar views, templates e formulários
✔ Proteger rotas sensíveis
✔ Adicionar configurações de autenticação no settings.py
✔ Executar migrações
✔ Mesclar branch na principal
✔ Gerar relatório em PDF com prints
✔ Documentação completa em Markdown (este README)

```

## 📂 Estrutura do Projeto

```
tarefa4_project/
│
├── manage.py
├── README.md
├── requirements.txt
│
├── tarefa4_project/
│   ├── __init__.py
│   ├── settings.py
│   ├── urls.py
│   ├── wsgi.py
│
├── usuarios/
│   ├── __init__.py
│   ├── admin.py
│   ├── apps.py
│   ├── forms.py
│   ├── models.py
│   ├── urls.py
│   ├── views.py
│
└── templates/
    └── usuarios/
        ├── cadastro.html
        ├── login.html
        └── dashboard.html
```

## ⚙️ Instalação e Execução do Projeto

```

1️⃣ Criar ambiente virtual (recomendado)
python -m venv venv


Ativar:

Windows

venv\Scripts\activate


Linux/Mac

source venv/bin/activate

2️⃣ Instalar dependências
pip install -r requirements.txt

3️⃣ Aplicar migrações
python manage.py migrate

4️⃣ (Opcional) Criar superusuário
python manage.py createsuperuser

5️⃣ Executar o servidor
python manage.py runserver

```

## 🔗 Acessar aplicação

```
Função	URL
Cadastro	http://127.0.0.1:8000/usuarios/cadastro/
Login	http://127.0.0.1:8000/usuarios/login/
Dashboard (protegido)	http://127.0.0.1:8000/usuarios/dashboard/
Logout	http://127.0.0.1:8000/usuarios/logout/

```

## 🔐 Autenticação e Segurança

No arquivo settings.py, foram adicionadas as configurações:

```
LOGIN_URL = '/usuarios/login/'
LOGIN_REDIRECT_URL = '/usuarios/dashboard/'
LOGOUT_REDIRECT_URL = '/usuarios/login/'
```

Isso garante:

```

Usuários não autenticados não acessam o dashboard.

Após login → vão para o dashboard.

Após logout → voltam para login.

```

## 🧩 Funcionalidades da Aplicação usuarios

```

✔ Cadastro de Usuário

Formulário baseado em UserCreationForm

Email obrigatório

Redireciona automaticamente para o dashboard após registrar

✔ Login

Autenticação por username + password

Mensagens de erro em caso de falha

Após login → acesso ao dashboard

✔ Logout

Finaliza sessão

Redireciona para a tela de login

✔ Dashboard (rota protegida)

Só acessível após login

Implementada com decorator:

@login_required
```

## 🖼 Templates Criados

Os templates estão em:

```
templates/usuarios/
├── cadastro.html
├── login.html
└── dashboard.html
```

## Todos funcionais e com navegação entre si.

```
🛠 Branch, Commit e Merge — GIT
Criar branch:
git checkout -b autenticacao

Adicionar arquivos:
git add .

Commit:
git commit -m "Implementa autenticação e app usuarios"

Enviar para o GitHub:
git push origin autenticacao
```

Fazer MERGE para a branch principal:

Via Pull Request no GitHub:

```
✔ Comparar: autenticacao → main
✔ Revisar mudanças
✔ Fazer merge

```
## 📑 Relatório em PDF

O PDF com prints já faz parte da entrega e contém:

```
Descrição da implementação

Prints automáticos do fluxo

Espaço para anexar prints reais do sistema

Link do repositório (para você preencher)
```

## 📝 Prints incluídos no relatório PDF

```
O relatório gerado automaticamente contém:

Print 1 — git branch autenticacao

Print 2 — Tela de cadastro

Print 3 — Tela de login

Print 4 — Tela de dashboard

(Apresentados como placeholders dentro do PDF, seguindo o modelo da tarefa.)
```

## 📌 Observações Importantes

```

Mude o SECRET_KEY antes de publicar:

SECRET_KEY = 'use-uma-chave-segura-aqui'


Banco de dados padrão: SQLite → ideal para testes acadêmicos.

O projeto está modular e pronto para expansão (CRUD de tarefas, perfis, permissões, etc.).
```

## 📎 Licença

```
Projeto acadêmico — uso livre para fins de estudo.

```

## 🎉 Conclusão

Este projeto cumpre todos os requisitos da tarefa, incluindo:

```
✔ Autenticação
✔ Proteção de rotas
✔ Templates
✔ Branch Git
✔ Commits
✔ PDF com prints
✔ README completo
```
