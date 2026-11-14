# Fluxo-oficina-bpmn

# Estudo de Caso: Sistema de Gestão de Ordem de Serviço (Oficina Mecânica)

**Autor:** Guilherme Francisco  
**Curso:** Análise e Desenvolvimento de Sistemas (ADS)  
**Foco:** Levantamento de Requisitos, Regras de Negócio e Modelagem de Processos (BPMN)

---

## 1. Contextualização do Problema
Uma pequena rede de oficinas mecânicas enfrenta dificuldades no controle de entrada e saída de veículos. Atualmente, os registros são feitos manualmente em papel ou cadernos, o que ocasiona perda de informações, falta de histórico de manutenções anteriores e falhas na comunicação com o cliente sobre a conclusão do serviço.

**Objetivo:** Estruturar a especificação inicial de um sistema simples para digitalizar o cadastro de clientes/veículos, gerenciar Ordens de Serviço (OS), manter o histórico de atendimentos e notificar o cliente automaticamente ao término do conserto.

---

## 2. Casos de Uso (Use Cases)

* **UC01 - Cadastrar Cliente e Veículo**
  * **Ator:** Funcionário (Atendente)
  * **Descrição:** O funcionário registra os dados pessoais do cliente (nome, telefone/WhatsApp) e as informações do veículo (placa, modelo, ano) no sistema no momento da chegada à oficina.
* **UC02 - Gerar Ordem de Serviço (OS)**
  * **Ator:** Funcionário (Atendente)
  * **Descrição:** O funcionário abre uma nova OS vinculada ao veículo cadastrado, descrevendo o problema relatado pelo cliente e os valores estimados/acordados.
* **UC03 - Executar Conserto e Finalizar Serviço**
  * **Ator:** Mecânico
  * **Descrição:** Após realizar a manutenção, o mecânico atualiza o status da OS para "Pronto", registra os serviços efetivamente executados e dispara a notificação de retirada para o cliente.

---

## 3. Requisitos Funcionais (RF)

* **RF01 - Registro Cadastral:** O sistema deve permitir o cadastro, consulta e edição de clientes e seus respectivos veículos.
* **RF02 - Emissão de Ordem de Serviço:** O sistema deve gerar uma OS numerada contendo os dados do cliente, veículo, relato do defeito, serviços realizados e valores cobrados.
* **RF03 - Gestão de Status:** O sistema deve permitir a alteração do status da OS (ex.: *Em Análise*, *Em Manutenção*, *Pronto*).
* **RF04 - Histórico de Manutenções:** O sistema deve armazenar todas as Ordens de Serviço concluídas vinculadas à placa do veículo para consultas futuras.
* **RF05 - Notificação ao Cliente:** O sistema deve enviar um aviso automático (via WhatsApp ou SMS) ao cliente assim que o status da OS for alterado para "Pronto".

---

## 4. Regras de Negócio (RN)

* **RN01 - Vínculo Obrigatório:** Não é permitido abrir uma Ordem de Serviço sem que haja um cliente, um veículo e a descrição inicial do problema devidamente registrados.
* **RN02 - Gatilho de Notificação:** O aviso de retirada só deve ser disparado automaticamente ao cliente no momento em que o status da OS mudar para "Pronto".
* **RN03 - Integridade e Auditoria (Histórico):** Ordens de Serviço finalizadas não podem ser excluídas do banco de dados, garantindo respaldo histórico e financeiro em caso de contestações ou garantia de serviço.
* **RN04 - Lançamento de Valores:** Toda OS finalizada deve conter o detalhamento dos valores de peças e mão de obra antes de ser encerrada.

---

## 5. Requisitos Não Funcionais (RNF)

* **RNF01 - Disponibilidade:** Por tratar-se de uma operação de atendimento presencial, o sistema não exige disponibilidade 24/7, devendo operar de forma estável em horário comercial (segunda a sábado, das 08h às 18h).
* **RNF02 - Usabilidade:** A interface deve ser simples e intuitiva, permitindo que atendentes e mecânicos realizem cadastros e atualizações de status com poucos cliques.
* **RNF03 - Segurança e Backup:** Os dados de clientes e o histórico de serviços devem possuir rotinas diárias de backup para evitar perdas de registros.

---

## 6. Modelagem do Processo de Negócio (BPMN)

O fluxo abaixo representa a interação entre as três raias principais do processo (**Cliente**, **Funcionário** e **Mecânico**), desde a entrega do veículo até a notificação de retirada:

# INFELIZMENTE O SOFTWARE TEVE ERRO E NÃO ESTÁ SALVANDO O FIM DA TASK DO MECÂNICO CORRETAMENTE!!!!

<img width="1008" height="1796" alt="BPMN-oficina" src="https://github.com/user-attachments/assets/dfb9a6ad-99e1-4437-aab0-68e5579fdd78" />




