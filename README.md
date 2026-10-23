# ADK Streaming

Agente simples construído com o Google Agent Development Kit (ADK) para
responder perguntas usando a Busca do Google como fonte de grounding.

## Requisitos

- Python 3.10 ou superior
- Uma chave da Google AI API

## Instalação

Clone o repositório e crie um ambiente virtual:

```bash
git clone https://github.com/crocha12/adk-streaming.git
cd adk-streaming
python -m venv .venv
source .venv/bin/activate
pip install google-adk
```

No Windows PowerShell, ative o ambiente com:

```powershell
.venv\Scripts\Activate.ps1
```

## Configuração

Copie o arquivo de exemplo para `.env` e informe sua chave:

```bash
cp app/.env.example app/.env
```

Edite `app/.env` e substitua `PASTE_YOUR_ACTUAL_API_KEY_HERE` pela sua chave
da Google AI API. O arquivo `.env` está ignorado pelo Git e não deve ser
publicado.

## Execução

A partir da raiz do projeto, execute o agente com:

```bash
adk web app
```

Em seguida, abra o endereço indicado pelo ADK no navegador e selecione o
agente `google_search_agent`.

## Estrutura

```text
app/
├── .env.example
└── google_search_agent/
    ├── __init__.py
    └── agent.py
```
