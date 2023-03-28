---
title: "Efficient Communication : A Guide to Integrating Appian with Telegram"
datePublished: Tue Mar 28 2023 14:25:16 GMT+0000 (Coordinated Universal Time)
cuid: clfsco5y2000809mjeqq9f76n
slug: integrating-appian-with-telegram
cover: https://cdn.hashnode.com/res/hashnode/image/stock/unsplash/3pwMu6uVsJI/upload/04aae6ad7543cea72f73086b7402aeb5.jpeg
tags: integration, telegram, low-code, telegram-bot, appian

---

Telegram is a popular messaging app that offers advanced features such as encryption, file sharing, and bots.

Appian is a low-code platform that allows businesses to create custom enterprise applications quickly and efficiently.

In this article, we will discuss the steps to integrate Appian with Telegram.

Step 1: Create a Telegram Bot

A bot is a special type of account that can send and receive messages automatically. In Telegram search for BotFather, enter /start to start the conversation.

Enter /newbot, give a name for it(name will be displayed in the chat), and give a username which should end with "bot".

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680008273837/b24f2203-e206-4f87-b987-cfc7691a02aa.png align="center")

Once you have created the bot, Telegram will provide you with an API key. This key is required to integrate Telegram with Appian.

Step 2: Get ChatID

Search and send a message to the bot created above in Telegram.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680012836660/82da6ea6-c951-4986-99b0-8aafb0a479a0.png align="center")

Create an Appian Integration object with below values.

URL input - [https://api.telegram.org/bot&lt;your-bot-API-key&gt;/getUpdates](https://api.telegram.org/bot1991219914:AAF92YPGD1sH_mResdZf5sjMNgbV_RJhGtg/getUpdates)

Method - GET

Test the integration.

Save the below highlighted id from the response, this is also called chat id and used to send the message.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680012054250/1caf31fa-0790-49af-a1c1-931d7ace4a1c.png align="center")

Step 3: Send message

Create another integration object with below values.

URL input - [https://api.telegram.org/bot&lt;your-bot-API-key&gt;/sendMessage](https://api.telegram.org/bot1991219914:AAF92YPGD1sH_mResdZf5sjMNgbV_RJhGtg/getUpdates)

Method - GET

Query Parameters:

text - "Message to reply"

chat\_id - id from step2

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680011530888/baaf93c2-e24c-49e4-870c-2e772cfb5ba8.png align="center")

If the integration is working correctly, the message should be received in Telegram..

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680011667483/7c0eb6cb-da53-4f99-a29f-afcc3973e092.png align="center")

Once the integration is complete, you can use it to receive notifications, and send messages directly from Appian to Telegram.

In conclusion, integrating Appian with Telegram is a simple and effective way to improve communication and collaboration within your organization.