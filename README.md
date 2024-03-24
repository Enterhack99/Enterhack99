from telegram.ext import Updater, CommandHandler, MessageHandler, Filters

TOKEN = '7106508635:AAFeWRTZlm5ngxVvASc9v89YZfVd2PPn6Lg'

def start(update, context):
    update.message.reply_text("Привет! Я бот, который готов работать и помочь вам начать зарабатывать на Notcoin.")

def echo(update, context):
    update.message.reply_text(update.message.text)

def main():
    updater = Updater(TOKEN, use_context=True)
    dp = updater.dispatcher

    dp.add_handler(CommandHandler("start", start))
    dp.add_handler(MessageHandler(Filters.text & ~Filters.command, echo))

    updater.start_polling()
    updater.idle()

if __name__ == '__main__':
    main()
