
# AWS Step Functions

Repositório organizado contendo anotações e insights adquiridos durante a prática. Com o tema "Explorando Workflows Automatizados com AWS Step Functions. Desafio do curso [DIO - Santander Code Girls - 2025](https://web.dio.me/track/santander-code-girls-2025).

## AWS Step Functions 
- [Documentação AWS - Saiba mais sobre máquinas de estado no Step Functions](https://docs.aws.amazon.com/pt_br/step-functions/latest/dg/concepts-statemachines.html)

O Step Functions é baseado em máquinas de estado, também chamadas de fluxos de trabalho. Os fluxos de trabalho são compostos por uma série de etapas orientadas por eventos.

Com o AWS Step Functions, podemos criar fluxos de trabalho para criar aplicativos distribuidos, automatizar processos, orquestrar microsserviços e criar pipelines de daos e aprendizado de máquina. 

Um fluxo de trabalho no Step Functions é chamado de máquina de estado. Ele é composto por estados, e cada estado representa uma etapa do processo.

Tipos de fluxo de trabalho:
- Fluxo de Trabalho Padrão: são ideais para fluxos de trabalho auditáveis e de longa duração, pois mostram o histórico de execução e aa depuração visual. Tem a execução de fluxo de trabalho única e podem durar até um ano.
- Fluxo de Trabalho Expresso: são ideais para high-event-rate cargas de trabalho, como processamento de dados de streaming e ingestão de dados de IoT. Tem execução at-least-once de fluxo de trabalho e podem ser executados por até cinco minutos.

No console do Step Functions, é possivel visualizar, editar, examinar o etado de cada etapa no fluxo de trabalho para garantir que a aplicação seja executada en ordem e conforme o esperado. Você define um fluxo de trabalho usando a Amazon States Language, também conhecida como ASL. Opcionalmente, você pode usar o Workflow Studio, um designer visual de fluxo de trabalho, para criar e editar seus fluxos de trabalho.

Com o AWS Step Functions, você paga por cada transição de um estado para o próximo. O faturamento é medido por transição de estado, e você não paga por tempo ocioso, independentemente da duração de cada estado (até um ano).

Quando você executa um fluxo no Step Functions, ele cria uma execução (instância do workflow).
Você pode monitorar o status dessa execução e, se ocorrer um erro, o próprio fluxo pode detectar e reagir a ele (por exemplo, fazendo retry ou redirecionando para outra etapa).

1. Orquestrar tarefas: permite criar fluxos de trabalho que executam várias etapas em uma ordem definida.
2. Escolher tarefas com base em dados: usando o estado Choice, é possível fazer com que o Step Functions tome decisões com base na entrada do estado.
3. Tratar erros (Retry/Catch): é possível repetir ou capturar tarefas com falha e executar etapas alternativas automaticamente.
4. Adicionar seres humanos no processo: é possível incluir etapas manuais para revisão ou aprovação no meio do processo.
5. Processar dados em etapas paralelas: usando um estado Parallel, o Step Functions pode processar dados de entrada em etapas paralelas.
6. Processar elementos de dados de modo dinâmico: usando um estado Map, o Step Functions pode executar um conjunto de etapas do fluxo de trabalho em cada item em um conjunto de dados. As iterações são executadas em paralelo, o que possibilita o processamento rápido de um conjunto de dados.

- [O WorkShop AWS Step Functions](https://catalog.workshops.aws/stepfunctions/pt-BR)

## Referências
- [Documentação AWS - O que é o Step Functions?](https://docs.aws.amazon.com/pt_br/step-functions/latest/dg/welcome.html)
- [Recursos do AWS Step Functions](https://aws.amazon.com/pt/step-functions/features/#topic-0)
- [Aulas do Curso da DIO - Santander Code Girls](https://web.dio.me/track/santander-code-girls-2025) 
