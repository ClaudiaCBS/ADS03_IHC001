<div align="center">

# ADS03_IHC001

Repositório para as atividades em GRUPO da disciplina Interação Humano Computador (NLI).

## Professor Giuliano Bertoti

| Partipantes | Github |
| -------- |-------- |
| Claudia Secco | <a href="https://github.com/ClaudiaCBS" target="_blanck"><img src = "https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white" target="_blank"></a> |
| Joice Araujo | <a href="https://github.com/Joice-Araujo" target="_blanck"><img src = "https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white" target="_blank"></a> |
| Mateus de Sousa | <a href="https://github.com/MateusdiSousa" target="_blanck"><img src = "https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white" target="_blank"></a> |

</div>

# ChatBot no Telegram com Python
Para criar um chatbot no Telegram usando Python, você pode seguir os passos abaixo. Vamos usar a biblioteca python-telegram-bot, que simplifica a criação de bots no Telegram.

<span id="1">

## 1. Crie um Bot no Telegram:

* Abra o aplicativo Telegram e procure o bot chamado "BotFather".
* Inicie uma conversa com o BotFather e siga as instruções para criar um novo bot. Anote o token gerado pelo BotFather, pois você precisará dele para interagir com a API do Telegram.

## 2. Instale a biblioteca python-telegram-bot:

Você pode instalar a biblioteca python-telegram-bot usando o pip.

```cmd
pip install pytelegrambotapi
```

<span id="2">

## 3. Crie o código do seu bot:

```cmd
import telebot
from telebot import types

# Substitua 'TOKEN' pelo token gerado pelo BotFather.
token = 'SEU_TOKEN_AQUI'

bot = telebot.TeleBot(token)

# Função de comando "/start"
@bot.message_handler(commands=['start'])
def start(message):
    bot.reply_to(message, "Olá! Eu sou um ChatBot. Como posso ajudar?")

# Função de eco para mensagens de texto
@bot.message_handler(func=lambda message: True)
def echo_all(message):
    bot.reply_to(message, message.text)

# Inicia o bot
bot.polling()
```

Neste código de exemplo, criamos um bot que responde ao comando /start com uma saudação e ecoa mensagens de texto que recebe.

## 4. Execute o seu bot:

Execute o seu script Python. Se tudo estiver configurado corretamente, o bot estará ativo e pronto para receber comandos e mensagens.

## 5. Teste o seu bot:

Abra o Telegram e inicie uma conversa com o seu bot. Você pode enviar comandos, mensagens de texto e assim por diante.

Este é um exemplo básico de como criar um chatbot no Telegram usando Python. Você pode expandir as funcionalidades do seu bot adicionando mais manipuladores para diferentes comandos e mensagens.

Certifique-se de ler a documentação oficial da biblioteca python-telegram-bot para obter mais informações sobre como criar bots mais complexos: 
<a href="#1"> https://python-telegram-bot.readthedocs.io/en/stable/ </a>
