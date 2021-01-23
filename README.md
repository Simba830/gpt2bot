# gpt2bot

<img src="https://github.com/polakowo/gpt2bot/blob/master/logo.png?raw=true" width=128>

```
User >>> Can we achieve singularity?
Bot >>> What does this mean?
User >>> Can computers become smarter than humans?
Bot >>> Is there any evidence that this is possible?
User >>> It must be doable
Bot >>> But... how?
User >>> I want to find out, that's why I created you
Bot >>> You created me?
User >>> You're my bot
Bot >>> You monster
```

gpt2bot is a multi-turn Telegram chatbot powered by neural networks. 

The bot uses [DialoGPT](https://arxiv.org/abs/1911.00536) - a large-scale pretrained 
dialogue response generation model, which was trained by Microsoft on 147M multi-turn 
dialogue from Reddit discussion thread. The human evaluation results indicate that its 
quality is comparable to human response quality under a single-turn conversation Turing test.

The bot can also use any other text generator supported by [transformers](https://huggingface.co/transformers/).

To further improve dialog generation, the bot uses [DialogRPT](https://arxiv.org/abs/2009.06978) - 
a set of dialog response ranking models trained on 100+ millions of human feedback data.
  
## How to use?

### 1. Create a Telegram bot

- Register a new Telegram bot via BotFather (see https://core.telegram.org/bots)

### 2. Deploy the bot

#### Google Colab

[A Colab interactive notebook](https://colab.research.google.com/github/polakowo/gpt2bot/blob/master/Demo.ipynb)

#### Locally

To get started, first clone this repo:

```
$ git clone https://github.com/polakowo/gpt2bot.git
$ cd gpt2bot
```

Create and activate a conda env:

```
$ conda create -n gpt2bot python=3.7.6
$ conda activate gpt2bot
```

Or a venv (make sure your Python is 3.6+):

```
$ python3 -m venv venv
$ source venv/bin/activate  # Unix
$ venv\Scripts\activate  # Windows
```

Install the requirements:

```
$ pip install -r requirements.txt
```

Set your parameters such as API token in chatbot.cfg:

```
$ nano chatbot.cfg
```

Run the chatbot:

```
$ python run_telegram_bot.py
```

### 3. Start chatting!

![](telegram_bot.gif)

Just start texting. Append "@gif" for the bot to also generate a GIF. To reset, type "/start".

Icon made by [Freepik](https://www.freepik.com) from [Flaticon](https://www.flaticon.com/)
