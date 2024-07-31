import { Telegraf, Markup } from 'telegraf'
import { message } from 'telegraf/filters'

const token = '6908588510:AAGJ8Lhf_ItjNl9gQoCnK7IejRWQHWpPfiE'
const webAppUrl = 'https://vk.com/'

const bot = new Telegraf(token)

bot.command('start', (ctx) => {
  ctx.reply(
    'Добро пожаловать! Нажмите на кнопку ниже, чтобы запустить приложение',
    Markup.keyboard([
      Markup.button.webApp('Отправить сообщение', `${webAppUrl}/feedback`),
    ])
  )
})

bot.launch()
