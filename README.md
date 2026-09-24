# Trabalho em Grupo com IA

Este repositório é uma demonstração acadêmica de como usar GitHub Copilot, GitHub Issues, GitHub Projects, GitHub Actions e workflows agentic para organizar um trabalho em grupo.

## Cenário da demo

Um grupo de estudantes recebeu o tema:

> O impacto da inteligência artificial na educação superior

O grupo precisa transformar esse tema em um plano claro, dividir responsabilidades, acompanhar o avanço e gerar relatórios semanais.

## Objetivo

Mostrar como o GitHub pode ser usado como um ambiente de gestão de projetos, mesmo fora de projetos tradicionais de software.

Com apoio de IA, o grupo pode:

- transformar um tema amplo em plano de trabalho;
- criar tarefas claras com critérios de aceite;
- distribuir responsabilidades;
- acompanhar status em um GitHub Project;
- identificar bloqueios;
- gerar relatórios semanais;
- manter histórico e rastreabilidade das decisões.

## Fluxo sugerido

1. Definir o tema do trabalho.
2. Pedir ao GitHub Copilot para criar um plano inicial.
3. Transformar o plano em issues.
4. Organizar as issues em um GitHub Project.
5. Usar labels, milestones e campos customizados.
6. Registrar atualizações nas issues.
7. Usar Actions e agentes para gerar relatórios e detectar riscos.

## Estrutura do repositório

```text
README.md
docs/
  plano-do-projeto.md
  referencias.md
  roteiro-apresentacao.md
  relatorio-semanal.md
.github/
  ISSUE_TEMPLATE/
    tarefa-academica.yml
    bloqueio.yml
  workflows/
    agentic-weekly-report.yml
    weekly-report.yml
    issue-triage.yml
  agents/
    planning-agent.md
    project-health-agent.md
    report-agent.md
    weekly-project-reporter-agent.md
```

## Agentes da demo

| Agente | Função |
|---|---|
| Planning Agent | Transforma o tema em objetivos, fases, tarefas e critérios de aceite. |
| Project Health Agent | Analisa bloqueios, riscos, atrasos e dependências. |
| Report Agent | Gera relatório semanal para o grupo e stakeholders. |
| Weekly Project Reporter Agent | Analisa issues, bloqueadores, riscos e dependências para apoiar o relatório semanal. |

## Relatório semanal com agente

O workflow **Agentic weekly project report** é o fluxo principal para a demo. Ele pode ser executado:

- automaticamente toda sexta-feira;
- manualmente pela aba **Actions**;
- manualmente com um título customizado.

Ele gera uma issue de relatório e também pode salvar uma cópia em `docs/reports/`.

O workflow **Weekly project report** pode ser executado manualmente ou por agenda. Ele cria uma issue de relatório com:

- indicadores gerais do projeto;
- principais avanços;
- bloqueadores;
- riscos;
- dependências críticas;
- tarefas que precisam de atenção;
- plano de recuperação sugerido;
- prompt para refinar a análise com Copilot.

Na demo, a narrativa é:

> A Action dispara. O agente interpreta. O humano decide.

## Como usar com GitHub Copilot

Use este prompt inicial no Copilot Chat:

```text
Somos um grupo de 5 estudantes e precisamos entregar um trabalho acadêmico em 3 semanas sobre:
"O impacto da inteligência artificial na educação superior".

Crie um plano de projeto com objetivo geral, objetivos específicos, divisão de responsabilidades, tarefas, prazos, critérios de aceite, riscos e sugestões de acompanhamento semanal.
```

Depois, peça:

```text
Transforme este plano em GitHub Issues. Para cada issue, gere título, descrição, checklist, critérios de aceite, labels e milestone sugerida.
```

## Mensagem principal da demo

> A IA não faz o trabalho pelo grupo. Ela ajuda o grupo a transformar uma ideia inicial em um projeto organizado, rastreável e acompanhável.
