## Fluxo do Sistema

### Objetivo
Descrever o fluxo principal do sistema de **[NOME DO SISTEMA]**, desde a entrada do usuário até a finalização do processo.

### Atores
- Usuário/Cliente
- Frontend
- API
- Banco de Dados
- Operador/Admin (se existir)

### Regras principais
- [Regra 1 - um técnico precisa obter 1 skill]
- [Regra 2]
- [Regra 3]

### Fluxo principal (passo a passo)
1. O usuário inicia **[ação inicial]** no Frontend.
2. O sistema realiza **coleta de dados** (formulário, contexto e metadados).
3. A API recebe e valida **[validações]**.
4. Se **[condição]**, então **[ação]**.
5. Caso contrário, **[alternativa]**.
6. O sistema persiste os dados no **Banco de Dados**.
7. O usuário recebe **[confirmação/erro]**.

### Fluxograma
```mermaid
flowchart TD
  %% Nós
  A([Início]):::start
  B["Frontend<br/>Entrada do Usuário"]:::ui
  C["Coleta de Dados<br/>formulário + contexto"]:::proc
  D["API<br/>Validação e regras"]:::api
  E{Condição válida?}:::decision
  F["Persistência<br/>Salvar no Banco"]:::db
  G["Resposta ao Usuário"]:::ui
  H["Tratamento de erro<br/>e correção"]:::warn
  I([Fim]):::endc

  %% Fluxo
  A --> B --> C --> D --> E
  E -- Sim --> F --> G --> I
  E -- Não --> H --> C

  %% Estilo (moderno e limpo)
  classDef start fill:#0f172a,stroke:#0f172a,color:#ffffff,stroke-width:2px;
  classDef endc fill:#0f172a,stroke:#0f172a,color:#ffffff,stroke-width:2px;
  classDef ui fill:#e2e8f0,stroke:#94a3b8,color:#0f172a,stroke-width:1px;
  classDef proc fill:#dbeafe,stroke:#60a5fa,color:#0f172a,stroke-width:1px;
  classDef api fill:#ecfeff,stroke:#22d3ee,color:#0f172a,stroke-width:1px;
  classDef decision fill:#fef3c7,stroke:#f59e0b,color:#0f172a,stroke-width:1px;
  classDef db fill:#dcfce7,stroke:#22c55e,color:#0f172a,stroke-width:1px;
  classDef warn fill:#fee2e2,stroke:#ef4444,color:#0f172a,stroke-width:1px;
```
