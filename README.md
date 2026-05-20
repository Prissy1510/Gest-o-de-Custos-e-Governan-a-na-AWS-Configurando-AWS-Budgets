# 💰 Gestão de Custos e Governança na AWS: Configurando AWS Budgets

## ⚠️ O Problema: O "frio na barriga" da conta na Nuvem
Para quem está começando na nuvem, um dos maiores receios é o modelo de "pague pelo que usar". Esquecer uma instância ligada ou configurar um serviço de forma errada pode gerar surpresas desagradáveis na fatura ao final do mês. 💸

Sem um mecanismo de fiscalização, a conta pode sair do controle antes mesmo de você perceber.

---

## 🎯 O Objetivo do Projeto
Este laboratório foca na implementação de uma **"Rede de Segurança Financeira"**. O objetivo foi configurar o **AWS Budgets** para atuar como um fiscal financeiro em tempo real, monitorando os gastos da conta e disparando alertas automáticos sempre que os limites definidos forem atingidos ou previstos.

---

## 🏗️ Arquitetura da Solução
Abaixo, o desenho da arquitetura que ilustra o fluxo de monitoramento e notificação:

![Arquitetura do Projeto](./img/Captura%20de%20Tela%20(1701).png)

### 🛠️ Como funciona o fluxo:
1.  **AWS Budgets:** Monitora constantemente o faturamento da conta frente ao orçamento estipulado.
2.  **Thresholds (Gatilhos):** Define camadas de alerta (ex: 50%, 80% do uso).
3.  **Amazon SNS:** O serviço de notificações da AWS entra em ação por trás dos panos para disparar os alertas.
4.  **E-mail:** O usuário recebe a notificação instantânea para tomar uma ação antes que o custo exceda o planejado.

---

## 🚀 Implementação e Boas Práticas

### 1. Criação do Orçamento Personalizado
Acesse o painel de **Billing and Cost Management** e configurei um orçamento de custo mensal. Para este ambiente de estudos, o limite fixo foi estabelecido em **US$ 10,00**.

### 2. Configuração de Alertas Inteligentes
Em vez de esperar o gasto total, configurei alertas em camadas baseados em percentuais:
*   **Alerta de 50%:** Aviso preventivo quando o gasto atinge $5,00.
*   **Alerta de 80%:** Alerta crítico quando o gasto atinge $8,00.
*   **Alerta de Previsão (Forecasted):** Se a AWS prever que o ritmo atual de uso vai estourar o limite até o fim do mês, sou notificada imediatamente.

### 3. Validação do "Fiscal Financeiro"
O orçamento foi criado e validado com sucesso no console, garantindo que a conta agora possui governança e monitoramento ativo.

![Orçamento Ativo no Console](./img/Captura%20de%20Tela%20(1368).png)

---

## 📈 Aprendizados Adquiridos
*   **Cultura FinOps:** Compreensão de que a gestão de custos é parte integrante da arquitetura de nuvem.
*   **Governança:** Como aplicar travas de segurança para ambientes de testes e produção.
*   **Autonomia com Segurança:** Agora posso explorar outros serviços da AWS (como Lambda, EC2 e SQS) com a tranquilidade de que serei avisada se algo sair do esperado.# Gest-o-de-Custos-e-Governan-a-na-AWS-Configurando-AWS-Budgets
