#WhereToGo (Android application)











Стороннее программное обеспечение, обеспечивающее работу приложения:

1) База данных: 

СУБД: MySQL 5.5. 

Движок для хранения таблиц – InnoDB.

Количество таблиц: 2 (первая содержит - данные о пользователе, вторая - комментарии и оценки).

	Поля таблицы User: 

	а) user_id - идентификатор пользователя (INTEGER NOT NULL PRIMARY KEY) 

	б) user_name - имя пользователя (VARCHAR 20)

	в) password - пароль для авторизации (VARCHAR 20)


	Поля таблицы Place

	a) user_id (INTEGER NOT NULL PRIMARY KEY)

	б) place_id (INTEGER NOT NULL FOREIGN KEY)

	в) place_name (VARCHAR 20)

	г) address (VARCHAR 20)

	д) comment_exist (BOOLEAN)

	е) mark_exist (BOOLEAN)



	Поля таблицы Comment

	а) Id_Comment (PRIMARY KEY)

	б) place_id (INTEGER NOT NULL FOREIGN KEY REFERENCES Place)

	в) description_comment

	г)comment_count
	

	Поля таблицы Comment

	а) Id_mark (PRIMARY KEY)

	б) place_id (INTEGER NOT NULL FOREIGN KEY REFERENCES Place)

	в) value_of_mark

	г)mark_count
