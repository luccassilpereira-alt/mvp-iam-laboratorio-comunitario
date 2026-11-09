# Sistema de Gestão de Identidades e Acessos (IAM) — Laboratório Comunitário

MVP desenvolvido para otimizar o controle de acesso, autenticação de operadores e alocação de computadores em tempo real na Associação Comunitária de Inclusão Digital de Guaianases.

## Arquitetura e Tecnologias
- **Padrão Arquitetural:** MVC (Model-View-Controller)
- **Back-end:** Python 3.x + Flask (`Werkzeug.security` / `bcrypt`)
- **Banco de Dados:** SQLite3 (Relacional Embarcado)
- **Front-end:** HTML5, Vanilla JavaScript e Tailwind CSS (Foco em Acessibilidade WCAG AA)

## Requisitos do MVP
- **RF01:** Gestão de contas e perfis de acesso (`aluno`, `instrutor`, `coordenador`).
- **RF02:** Check-in rápido de alunos por matrícula com bloqueio de sessão duplicada.
- **RF03:** Encerramento de sessão ativa (Check-out) e liberação de equipamento.
- **RF04:** Painel visual (Dashboard) de ocupação do laboratório em tempo real.
- **RNF01 / RNF02:** Hashes de senha com `bcrypt`, queries parametrizadas (prevenção contra SQL Injection) e escape de templates contra XSS (OWASP).
- **RNF03:** Tempo de carregamento inferior a 2,5 segundos e navegação via teclado.

## Estrutura do Repositório
```text
├── app.py                 # Controller principal e rotas Flask
├── database.py            # Model e inicialização do banco SQLite
├── requirements.txt       # Dependências do projeto
├── templates/             # Views (HTML5 + Tailwind CSS)
│   └── prototipo.html     # Interface unificada do MVP
└── README.md              # Documentação do projeto