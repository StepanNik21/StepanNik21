import { Telegraf, Eggs } from 'telegraf'
import { message } from 'telegraf/filters'

const token = 7449889863:AAE5Z9ItGyZdjbRlmqoQNHu7puJm0ZVr0Hk
const webAppUrl = https://t.me/clickeggs

const bot = 7449889863:AAE5Z9ItGyZdjbRlmqoQNHu7puJm0ZVr0Hk

bot.command('start', (ctx) => {
  ctx.reply(
    'Добро пожаловать! Нажмите на кнопку ниже, чтобы запустить приложение',
    Markup.keyboard([
      Markup.button.webApp('Отправить сообщение', `${webAppUrl}/feedback`),
    ])
  )
})

bot.launch()
