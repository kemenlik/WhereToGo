#WhereToGo (Android application)











###Стороннее программное обеспечение, обеспечивающее работу приложения

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



### Черновики интерфейса приложения
1.	Главный экран приложения:
	http://i067.radikal.ru/1310/ec/d60b98634656.jpg
2.	После нажатия по зданию появляется список заведений:
	http://s020.radikal.ru/i706/1310/b3/13c62543b504.jpg,
	http://s019.radikal.ru/i625/1310/14/2d17c0aeff06.jpg
3.	После нажатия по названию заведения, из предложенного списка, появится информация об этом заведении (Адрес, оценка и комментарии):
	http://s020.radikal.ru/i720/1310/df/b30e21b6f254.jpg





### Используемые в приложении API

В приложении WhereTOGo для отображения карт города Томска используется Google maps api.Google maps Api обладает мощными возможностями для отображения карт.

	
	Версия API: v2
	
**Возможности Google maps, которые были применены в приложении**:

	а) Отображение карты г. Томска
	
	б) Нанесение маркеров на месте расположения заведения
	
	в) Возможность добавления информации о заведении
	
	г) Масштабирование карты
	
	
	
