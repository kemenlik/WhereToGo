#WhereToGo (Android application)











###Стороннее программное обеспечение, обеспечивающее работу приложения:

**Описание базы данных**: 

СУБД: MySQL 5.5 

Движок для хранения таблиц – InnoDB. Данный движок поддерживает внешние ключи, транзакции, и поддерживается практически всеми видами СУБД.

Имя базы данных: Places

Количество таблиц: 4 (первая содержит - данные о пользователе, вторая - информация о заведении, третья - информация о комментариях, четвертая - информация о оценки).

	Поля таблицы User: 

	а) user_id - идентификатор пользователя (INTEGER NOT NULL PRIMARY KEY) 

	б) user_name - имя пользователя (VARCHAR 20)

	в) password - пароль для авторизации (VARCHAR 20)


	Поля таблицы Place:

	a) user_id (INTEGER NOT NULL PRIMARY KEY)

	б) place_id (INTEGER NOT NULL FOREIGN KEY)

	в) place_name (VARCHAR 20)

	г) address (VARCHAR 20)

	д) comment_exist (BOOLEAN)

	е) mark_exist (BOOLEAN)



	Поля таблицы Comment:

	а) Id_Comment (PRIMARY KEY)

	б) place_id (INTEGER NOT NULL FOREIGN KEY REFERENCES Place)

	в) description_comment (VARCHAR)

	г) comment_count (INTEGER NOT NULL)
	

	Поля таблицы Mark:

	а) Id_mark (PRIMARY KEY)

	б) place_id (INTEGER NOT NULL FOREIGN KEY REFERENCES Place)

	в) value_of_mark (INTEGER NOT NULL)

	г) mark_count (INTEGER NOT NULL)







###Выбор системы непрерывной интеграции (далее СНИ)

	В работе принято решение пользоваться кафедральной СНИ Jenkins, так как она является простой в использовании, и обеспечивает разработчиков нужным функционалом.



### Черновики интерфейса приложения:
