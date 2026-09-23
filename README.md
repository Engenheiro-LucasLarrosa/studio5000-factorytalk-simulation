# rockwell-automation-simulation-lab
Laboratório de automação industrial com Studio 5000, Logix Emulate e FactoryTalk View ME. Sequenciamento, simulação de processo, contagem de produção e controle de nível com PID.
# Rockwell Automation Simulation Lab

Projeto que desenvolvi para praticar programação de CLP e manter contato com diferentes recursos do ecossistema Rockwell Automation.

A ideia foi criar uma pequena célula de envase totalmente simulada, permitindo testar lógicas e conceitos de automação sem necessidade de hardware físico.

## O que tem no projeto

A aplicação possui:

- Sequenciamento automático da célula
- Simulação de movimentação e envase das peças
- Contagem de produção
- Contagem de peças aprovadas e rejeitadas
- Geração simulada de rejeições
- Simulação do nível de um tanque
- Controle de nível utilizando PID
- Programação em Ladder e Function Block
- IHM desenvolvida no FactoryTalk View ME
- Alteração de Setpoint pela IHM
- Trend para acompanhamento de SP, PV e CV

Todo o comportamento da máquina foi simulado dentro do CLP, então é possível executar o projeto utilizando o Logix Emulate sem precisar de hardware físico.

## Estrutura do projeto

A lógica foi separada em diferentes áreas para facilitar os testes e a organização:

- Main Program
- Sequencer
- Motor
- I/O Simulation
- PID Control
- Process Simulation

A simulação do processo gera o comportamento necessário para que a lógica de controle e a IHM possam funcionar como se existisse uma pequena máquina conectada ao CLP.

## Controle de nível

O projeto também possui uma malha de controle de nível utilizando PID.

Fluxo simplificado:

Setpoint → PID → Válvula → Processo simulado → Nível do tanque → Feedback

Pela IHM é possível alterar o Setpoint e acompanhar a resposta através do Trend utilizando:

- SP — Setpoint
- PV — Process Variable
- CV — Control Variable

## Softwares utilizados

- Studio 5000 Logix Designer — v32
- Studio 5000 Logix Emulate 5570 — v32.11
- FactoryTalk View Studio Machine Edition — v10.00.00 (CPR 9 SR 10)
- RSLinx Classic Gateway — v4.12.00 (CPR 9 SR 11)

## Arquivos

Os arquivos necessários para abrir e testar o projeto estão disponíveis neste repositório.

### PLC

Projeto do Studio 5000 / Logix Designer.

### HMI

Projeto do FactoryTalk View Machine Edition.

## Observação

Esse projeto foi desenvolvido como laboratório de estudos e testes.

A ideia é justamente poder alterar lógicas, testar sequências, modificar parâmetros do PID e experimentar diferentes soluções de automação em um ambiente totalmente simulado.
