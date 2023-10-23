#############################
в папке Email_comfig должны находиться три файла:
#############################
1) const_email.py - файл с константами 
#############################
1.1) указатель на файл с настройками доступа
INI_QUEUE_FILE_NAME =
1.2) количество проверяемых инфраструктур / очередей:
QUEUE_AMOUNT =
1.3) настройки email оправителя отчётов:
SMTP_EMAIL_SERVER =
EMAIL_LOGIN =
EMAIL_PASSWORD_OUT_APPLICATIONS =
1.4) email получателя технических отчётов:
EMAIL_NAME_TO =
1.5) email получателей тревожных сообщений:
email_name_alarm_list = []
#############################
#############################
2) set_queue.ini - файл с настройками доступа к Rabbit MQ:
#############################
2.1) заголовок комплекта данных:
[SET_x]
2.2) содержимое комплекта:
SERVER_IP
SERVER_PORT
USER_NAME
USER_PASSWORD
#############################
#############################
3) control_value.py - файл с пороговыми значениями проверок:
3.1) кортеж queue_control_values = ( 
memory free, % 
free disk space, GB
   )
3.2) словарь limit_value_messages = {
   "название очереди": пороговое значение кол-ва сообщений в очереди
   }
#############################
#############################