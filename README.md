# 🎫 Movidesk API Automation

> Automação completa de tickets e fluxos de atendimento via API REST do Movidesk — desenvolvida para operações de Mercado de Capitais em ambiente bancário.

![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=flat&logo=python&logoColor=white)
![REST API](https://img.shields.io/badge/REST-API-009688?style=flat)
![Status](https://img.shields.io/badge/status-production-brightgreen)

---

## 📌 Sobre o Projeto

Este projeto automatiza a gestão de tickets no Movidesk, cobrindo criação, atualização, consulta e envio de anexos via API REST. Foi desenvolvido para suportar operações fiduciárias e de fundos de investimento (FIP), eliminando processos manuais repetitivos da equipe de atendimento.

**Impacto real:** reduziu em mais de 60% o tempo gasto com abertura e atualização manual de chamados.

---

## ⚙️ Funcionalidades

- ✅ **GET** — Consulta de tickets por filtros (status, categoria, responsável, data)
- ✅ **POST** — Criação automática de tickets com campos customizados
- ✅ **PATCH** — Atualização de status, prioridade e responsável
- ✅ **Anexos** — Upload de arquivos binários (PDF, Excel) vinculados ao ticket
- ✅ **Logging** — Registro de todas as operações em arquivo `.log` com timestamp
- ✅ **Agendamento** — Compatível com `schedule` ou Task Scheduler do Windows

---

## 🚀 Como Usar

### 1. Clone o repositório
```bash
git clone https://github.com/yaneskenazi/movidesk-automation.git
cd movidesk-automation
```

### 2. Instale as dependências
```bash
pip install -r requirements.txt
```

### 3. Configure as credenciais
Crie um arquivo `.env` na raiz:
```env
MOVIDESK_TOKEN=seu_token_aqui
BASE_URL=https://api.movidesk.com/public/v1
```

### 4. Execute
```bash
python main.py
```

---

## 🗂️ Estrutura do Projeto
movidesk-automation/
│
├── main.py
├── config.py
├── requirements.txt
├── .env.example
│
├── services/
│   ├── ticket_service.py
│   ├── attachment_service.py
│   └── filter_service.py
│
├── models/
│   └── ticket.py
│
└── logs/
└── automation.log

---

## 🛡️ Segurança

- Token de API carregado via variável de ambiente (nunca hardcoded)
- Arquivo `.env` incluído no `.gitignore`
- Logs não contêm dados sensíveis de clientes

---

## 🧰 Tecnologias

| Tecnologia | Uso |
|---|---|
| Python 3.10+ | Linguagem principal |
| `requests` | Chamadas HTTP |
| `python-dotenv` | Gerenciamento de credenciais |
| `schedule` | Agendamento de tarefas |
| `logging` | Registro de operações |

---

## 📄 Licença

MIT License — livre para uso e adaptação.

---

> Desenvolvido por **Yan Eskenazi** · [LinkedIn](https://linkedin.com/in/yaneskenazi)
