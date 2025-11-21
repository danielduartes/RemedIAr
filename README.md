# 💊 RemedIAr - Assistente Farmacêutico no WhatsApp

O **RemedIAr** é um chatbot inteligente para WhatsApp desenvolvido para auxiliar no uso correto de medicamentos. Ele combina visão computacional e processamento de linguagem natural para ler bulas oficiais e ajudar o usuário a gerenciar seu tratamento.

## ✨ Funcionalidades

O projeto possui três funcionalidades principais:

### 1. 📷 Identificação por Foto
O usuário envia uma foto da caixa do remédio. O sistema identifica o medicamento e retorna as informações essenciais (indicação, posologia básica, etc.) extraídas diretamente da **bula oficial**.

### 2. 💬 Tira-Dúvidas (Bula IA)
O usuário pode fazer perguntas em texto natural sobre um medicamento (ex: *"Esse remédio dá sono?"* ou *"Posso tomar com leite?"*). O bot consulta a base de dados oficial da bula e responde com precisão e segurança.

### 3. ⏰ Lembretes Visuais
Sistema de agendamento para tomar a medicação.
* **Diferencial:** No horário programado, o usuário recebe a notificação acompanhada da **foto da caixa do remédio** (previamente enviada), facilitando a identificação visual para idosos ou pessoas com muitas prescrições.

---

## 🛠️ Tecnologias Utilizadas

* **Linguagem:** Python 3.13.5
* **Interface:** WhatsApp (via WWeb.js)
* **IA / LLM:** OpenAI GPT-4 (para interpretação de texto e imagem)
* **OCR:** GPT Vision (para leitura da caixa)
* **Banco de Dados:** ChromaDB (para salvar os agendamentos)
* **Bibliotecas Principais:**
    * `requests`
    * `schedule` / `apscheduler`

---

## 🚀 Como Rodar o Projeto

### Pré-requisitos
* Python 3.8 ou superior instalado.
* Conta configurada na API do WhatsApp escolhida.
* Chaves de API para o modelo de IA (ex: OpenAI API Key e Google Clouds).

No **primeiro terminal**, configure o servidor que processa as imagens e textos:

1. **Instale as dependências:**
   ```bash
   # Crie a venv (se ainda não criou)
   python -m venv venv
   
   # Ative a venv
   # Windows:
   .\venv\Scripts\Activate
   # Linux/Mac:
   source venv/bin/activate

   # Instale os pacotes
   pip install -r requirements.txt

2. **Execute o script do chatbot:**
   ```bash
   # node chatbot/chatbot.js

3. **Execute o backend:**
   ```bash
   # python app.py
