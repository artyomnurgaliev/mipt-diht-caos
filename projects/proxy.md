# HTTP-прокси сервер

Цель - реализовать веб-сервер для протокола `HTTP/1.1`, который умеет обслуживать с минимальными задержками 100К одновременных соединений, выдавать статические страницы, и перенаправлять запросы на другие веб-серверы, кэшируя их выдачу.

В качестве эталонной реализации можно рассматривать сервер [Nginx](http://nginx.org).

Реализованный сервер, помимо реализации основной функциональности, должен предполагать, что он работает без пользовательского интерфейста, то есть должны быть предусмотрены механизмы для управления запущенным сервером.

# Пререквизиты, необходимые для выполнения проекта

 1. Работа со строками
 2. Работа с нитями
 3. Работа с сигналами
 4. Работа с файловыми дескрипторами
 5. Работа с сокетами
 6. Мультиплексирование ввода-вывода


# Стек технологий

Разрешается использовать только стандартную библиотеку Си или C++.

# Критерии оценивания

 * **3 балла.** Реализован сервер, который выдает статические страницы. Должна быть реализована функциональность для конфигурирования, запуска и остановки сервера
 * **5 баллов.** Сервер умеет перенапралять запросы другим серверам
 * **8 баллов.** Реализованы кеширование ответов пенераправленных запросов и балансировка нагрузки
 * **+1 балл.** Корректно используется несколько ядер процессора
 * **+1 балл.** Поддерживается запись логов сервера, информативность которой можно настраивать