# lead-Automation-Workflow
Automates lead processing, filtering, and categorization based on region and interest. Stores leads in different spreadsheets and sends customized email + internal notifications.


## 📁 Files included in this repository

lead-automation-workflow.json: n8n workflow file to import

Workflow-automation.png: visual representation of the flow

## 📌 How the workflow works (ENGLISH)

1. Webhook - Receive data: Entry point, receives lead data from a form.

2. Filter data - Required fields: Validates and filters the required fields only.

3. Validation - Required fields: Checks if all required fields are filled; otherwise, it stops the process.

4. Stop and Error: Stops the flow if required fields are missing.
or
4. Filter data - Date: Extracts only the submission date.

5. Filter countries: Filters based on the lead's country.

6. Switch - Countries: Routes the lead to a specific spreadsheet by continent.

7. Google Sheets - Europe/Asia/Other: Appends lead data to the respective sheet based on continent.

8. Switch - Interest: Based on the interest (exchange, graduation, postgraduate), chooses the correct email message.

9. Send email - Lead interchange / graduation / postgraduate: Sends a custom email via Gmail.

10. Internal notification: Sends an internal Telegram notification about the new lead.

11. End: Ends the flow.

## 📌 Como o fluxo funciona (PORTUGUÊS)

1. Webhook - Recebe dados: Ponto de entrada, recebe os dados do lead via formulário.

2. Filtro - Campos obrigatórios: Valida e filtra apenas os campos importantes.

3. Validação - Campos obrigatórios: Verifica se todos os campos obrigatórios foram preenchidos. Se não, para o processo.

4. Parar e Erro: Finaliza o fluxo se campos obrigatórios estiverem ausentes.
ou
4. Filtro - Data: Extrai apenas a data do envio.

5. Filtro - Países: Filtra com base no país do lead.

6. Switch - Países: Direciona o lead para a planilha correta com base no continente.

7. Google Sheets - Europa/Ásia/Outro: Adiciona os dados do lead na aba correta.

8. Switch - Interesse: De acordo com o interesse (intercâmbio, graduação, pós), escolhe o e-mail certo.

9. Envio de e-mail - Intercâmbio / graduação / pós: Envia um e-mail personalizado via Gmail.

10. Notificação interna: Envia uma notificação interna via Telegram avisando sobre o novo lead.

11. Final: Finaliza o fluxo.

## 🛠️ Tools used / Ferramentas utilizadas

**n8n** (open source automation platform)

**Google Sheets** (data storage)

**Gmail** (email sending)

**Telegram** (internal notifications)

**Custom JavaScript Function** (continents classification logic)

## 📸 workflow preview
![Workflow preview](./Workflow-automation)


## 👉 How to use this project

Import the .json file into your n8n instance.

Create connections to Gmail, Google Sheets, and Telegram.

Replace the spreadsheet and email data with your own.

Activate the Webhook to start receiving leads.

## ✔️ Author

Created by Vitorfab as a learning and portfolio project.

Feel free to clone, study or adapt this workflow for your own automations!


