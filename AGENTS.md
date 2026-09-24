# Agentes da demo

Este repositório usa agentes como **perfis/prompt files** para demonstrar agentic workflows em gestão de projetos com GitHub.

> A Action dispara. O agente interpreta. O humano decide.

## Agentes disponíveis

| Agente | Arquivo | Função |
|---|---|---|
| Planning Agent | `.github/agents/planning-agent.md` | Transforma tema em plano, fases, tarefas e critérios de aceite. |
| Project Health Agent | `.github/agents/project-health-agent.md` | Analisa bloqueios, riscos, atrasos e dependências. |
| Report Agent | `.github/agents/report-agent.md` | Gera relatórios semanais para grupo e stakeholders. |
| Weekly Project Reporter Agent | `.github/agents/weekly-project-reporter.agent.md` | Analisa issues, bloqueadores, riscos e dependências para apoiar o relatório semanal. |

## Como usar na demo

1. Abra o workflow **Weekly project report** em GitHub Actions.
2. Execute o workflow manualmente.
3. Abra a issue de relatório criada automaticamente.
4. Copie o prompt de `.github/prompts/weekly-project-report.prompt.md`.
5. Use o prompt no Copilot Chat para refinar o relatório e gerar plano de recuperação.

## Observação importante

Estes arquivos não aparecem como um “agente instalado” em uma tela especial do GitHub. Eles funcionam como **perfis de agente versionados no repositório**, que podem ser usados pelo Copilot Chat, por workflows e pela narrativa da demo.

Isso é intencional para mostrar o conceito de agentic workflow de forma simples e rastreável.

