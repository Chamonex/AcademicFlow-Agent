# AcademicFlow-Agent

Sistema colaborativo baseado em agentes de IA utilizando arquitetura ReAct com LangGraph para auxiliar no planejamento de eventos acadêmicos.

## Sobre o Projeto

O AcademicFlow-Agent é um protótipo de agente colaborativo capaz de auxiliar grupos durante o planejamento de eventos acadêmicos. O sistema utiliza um fluxo ReAct (Reason + Act), permitindo que o modelo de linguagem decida entre responder diretamente ao usuário ou executar ferramentas específicas para organizar informações do projeto.

O agente pode:

- Registrar tarefas;
- Registrar decisões importantes;
- Atualizar seções de documentos colaborativos;
- Consultar o estado atual do planejamento;
- Auxiliar participantes durante discussões e organização do evento.

O foco principal do projeto é demonstrar a construção de agentes inteligentes utilizando LangGraph, integração com LLMs locais e uso de ferramentas em tempo de execução.

---

## Arquitetura

O sistema foi desenvolvido utilizando:

- ReAct Agent Pattern
- LangGraph State Graph
- Tool Calling
- LLM local com Ollama
- Memória simples em estrutura Python

Fluxo principal:

1. Usuário envia uma mensagem;
2. O agente interpreta a intenção;
3. Decide entre:
   - responder diretamente;
   - chamar ferramentas;
4. O estado do projeto é atualizado;
5. O agente retorna uma resposta contextualizada.

---

## Funcionalidades

### Registro de tarefas
Permite adicionar tarefas com responsável, prazo e status.

### Registro de decisões
Armazena decisões importantes tomadas pelo grupo.

### Documento colaborativo
Criação e atualização de seções do planejamento do evento.

### Consulta do quadro do projeto
Resumo completo do estado atual do planejamento.

### Fluxo ReAct
O agente decide dinamicamente quando utilizar ferramentas.

---

## Tecnologias Utilizadas

- Python
- LangGraph
- LangChain
- Ollama
- Llama 3.2
- HTTPX

---

## Estrutura do Projeto

```bash
academicflow-agent/
│
├── React_Project.py
├── README.md

```

---

## Como Executar

### 1. Instalar dependências

```bash
pip install langgraph langchain-ollama langchain-core httpx
```

### 2. Instalar o modelo local

```bash
ollama pull llama3.2
```

### 3. Iniciar o Ollama

```bash
ollama serve
```

### 4. Executar o projeto

```bash
python main.py
```

---

## Exemplo de Uso

```text
Grupo: Criar tarefa para reservar o auditório até sexta.
Agente: Tarefa registrada com sucesso.
```

```text
Grupo: Qual o estado atual do projeto?
Agente: Exibe tarefas, decisões e seções registradas.
```

---

## Conceitos Demonstrados

- Arquitetura de Agentes de IA
- ReAct Pattern
- Tool Calling
- State Management
- Planejamento colaborativo assistido por IA
- Integração de LLM local
- Fluxos multi-step com LangGraph

---

## Possíveis Melhorias Futuras

- Persistência em banco de dados;
- Interface web;
- Múltiplos agentes especializados;
- Integração com calendário;
- Sistema de autenticação;
- Memória vetorial;
- Upload de arquivos e atas.
