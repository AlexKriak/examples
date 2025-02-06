# Примеры кода
- example_yii2 содержит демо-часть системы для работы с входящими документами, с использованием системы событий (паттерн Команда).
  
Пример состоит из:
* DocumentInController - контроллер для реализации основных CRUD операций и других вспомогательных задач;
* DocumentInWork - модель, наследующая автогенерирумую модель Gii и расширяющий функционал базового класса;
* DocumentInService - сервис реализующий взаимодействие с классами файловой системой;
* EventTrait - реализован основноый функционал, таких как запись и выполнение/не выполнение событий;
* EventInterface - содержит набор методов, которые должен реализовать класс событий;
* InOutDocumentCreateEvent, InOutDocumentDeleteEvent, InOutDocumentLinkedEvent, InOutDocumentUpdateEvent - имплементируют интерфейс и реализуют стандартное взаимодействие с данными в базе.
--------------------------------------------

- example2_yii2 содержит подсистему для организации работы с файлами в системе.

Пример состоит из:
* DocumentController - пример контроллера, который является базовым для большинства документных контроллеров в системе;
* FileService - бизнес логика, для взаимодействия с файловым хранилищем;
* FilesRepository - репозиторий, для взаимодействия с таблицей, хранящей информацию о файлах в системе;
* FileCreateEvent, FileDeliteEvent - события на создание и удаление файлов.
--------------------------------------------

- unit_test_example3_yii2 содержит пример юнит теста.

Пример состоит из:
* VisitCreateTest - основной класс теста;
* VisitCreateData - провайдер данных для теста;
* VisitRepository - один из репозиториев для взаимодействия с таблицей журналов посещений. Репозиторий инкапсулирует собственный провайдер данных;
* VisitProviderInterface - контракт для провайдеров данных типа visit
* VisitProvider - основной провайдер для взаимодействия с базой данных
* VisitMockProvider - провайдер для mock-тестирования
