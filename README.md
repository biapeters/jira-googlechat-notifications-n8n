# 🚀 Notificação de Comentários Jira → Google Chat (n8n)

## 🧠 Descrição  
Este fluxo do **n8n** automatiza o envio de notificações para o **Google Chat** sempre que um **novo comentário é adicionado a um ticket no Jira**.  
A automação identifica o responsável pelo chamado e envia a mensagem diretamente para o espaço correspondente no Chat, garantindo uma comunicação rápida e eficiente entre os membros da equipe.

---

## ⚙️ Funcionalidades  
- Recebe dados do **Jira** via **Webhook**.  
- Identifica o **responsável pelo ticket (Assignee)**.  
- Monta uma mensagem personalizada com informações do chamado.  
- Envia a notificação para o **Google Chat** do responsável.  

---

## 🧩 Estrutura do Workflow  
1. **Webhook** → Recebe a requisição do Jira Automation.  
2. **Switch** → Verifica quem é o responsável pelo ticket.  
3. **Set (Texto)** → Monta a mensagem formatada com emojis e informações úteis.  
4. **HTTP Request** → Envia a mensagem ao respectivo espaço do Google Chat.

---

## 🧾 Exemplo de mensagem enviada  
🔥 **Atualização no seu chamado!** 🔥  
O ticket **STI-18450** (*Teste Notificação Jira*) recebeu um novo comentário.  
👉 [Acesse o chamado](https://exemplo.atlassian.net/browse/TESTE-001)  
Status: **Aberto**

---

## 🛠️ Configuração
1. **Importe o arquivo JSON** no n8n (`Notificacao_Comentarios_Jira_Chat_Google_Anonimizado.json`).  
2. Crie um **Webhook Trigger** no Jira Automation que envie os dados para o endpoint gerado pelo n8n.  
3. Atualize as **URLs dos Webhooks do Google Chat** dentro dos nós `HTTP Request` com os links dos seus espaços.  
4. Ative o workflow.  

---

## 🧰 Tecnologias utilizadas  
- [n8n.io](https://n8n.io)  
- Jira Automation  
- Google Chat Webhooks  

---

⚠️ **Atenção:** este repositório contém apenas a estrutura do fluxo.  
As URLs de integração com o Google Chat e tokens de autenticação foram removidos por segurança.  
Antes de usar, adicione seus próprios Webhooks válidos no n8n.
