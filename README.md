# Примеры тестов с использованием Ruby

### Что использую в примерах:
Ruby - это динамический, объектно-ориентированный язык программирования.
Ruby широко используется для написания автоматизированных тестов благодаря своей простоте и гибкости.

Gemfile используется для управления зависимостями проекта в Ruby. Он содержит список всех гемов (библиотек) Ruby, которые необходимы для работы проекта. Gemfile позволяет установить все необходимые гемы одной командой, а также контролировать их версии. Это помогает обеспечить совместимость между различными компонентами проекта и упрощает управление зависимостями.

Cucumber используется в тестировании для создания и автоматизации тестовых сценариев на основе языка Gherkin. Gherkin позволяет описывать поведение приложения в виде простых и понятных для всех участников проекта текстовых сценариев, которые можно использовать как документацию и как набор тестов.

Cucumber облегчает коммуникацию между разработчиками, тестировщиками и заказчиками, так как все они могут четко понимать, что должно происходить в приложении в каждом конкретном случае. Кроме того, Cucumber позволяет быстро создавать и изменять тестовые сценарии без необходимости переписывать код тестов.

Использование Cucumber также помогает повысить качество тестирования, так как позволяет проверять приложение на соответствие требованиям заказчика и на соответствие бизнес-логике.

HTTParty - это библиотека Ruby, которая предоставляет простой интерфейс для выполнения HTTP-запросов. Она позволяет легко отправлять запросы и получать ответы, а также обрабатывать ошибки. HTTParty может использоваться для тестирования веб-приложений, например, для проверки ответов на запросы и проверки правильности работы API.

RSpec используется для проверки результатов тестов. Например, в коде используется метод expect, который является частью RSpec.

Библиотека RestClient позволяют отправлять HTTP-запросы из Ruby-кода.

## WorkWithAPI_BD
В этом примере показывается работа Ruby с базой данных SQLite, использующего Cucumber для тестирования. В нем определены два сценария для тестирования создания записи в таблице Users и просмотра пользователей из таблицы Users. В файле env.rb указано имя базы данных SQLite. В файле database_steps.rb определены шаги для создания пользователей и вывода пользователей таблицы.
Этот проект является автоматизированным тестированием базы данных SQLite с помощью Cucumber и RSpec.

**Алгоритм:**
1) Создать папку проекта с названием "WorkWithAPI_BD"

2) В папке проекта выполнить команду:
```
bundle init
```
:white_check_mark: Результат: Создается файл Gemfile.
! Gemfile - это файл, который используется в проектах Ruby для управления зависимостями и установки необходимых гемов (библиотек) для работы приложения.

3) В папке проекта, в файле Gemfile прописать:
```
source 'https://rubygems.org'
gem 'cucumber'
gem 'sqlite3'
gem 'rspec'
```
4) Выполнить команду:
```
bundle install
```
:white_check_mark: Результат:
Будут установлены все гемы, перечисленные в Gemfile, и их зависимости. Если указаны версии гемов, то будут установлены именно эти версии. Если версии не указаны, то будет установлена последняя стабильная версия гема. Кроме того, будет создан файл Gemfile.lock, который содержит точные версии всех установленных гемов и их зависимостей. Этот файл необходим для обеспечения совместимости версий гемов между разными средами разработки и на разных этапах разработки проекта.

5) Выполнить команду:
```
cucumber --init
```
:white_check_mark: Результат:
При выполнении команды cucumber --init будет создан файл features/support/env.rb, который содержит настройки окружения для запуска тестов с использованием Cucumber. В этом файле будут подключены необходимые библиотеки и определены настройки для запуска тестов, такие как путь к файлам с описанием шагов и путь к директории с тестами. Также будут созданы директории features/step_definitions и features/support, которые содержат файлы с описанием шагов и настроек окружения соответственно.
!Эту команду нужно выполнить, когда только создается проект. У нас в проекте уже создан каркас и файлы наполнены кодом,поэтому эту команду не нужно выполнять, НО нужно выполнить команду:
```
bundle install
```
:white_check_mark: Результат:
В проект, в папку vendor, установятся гемы,описанные в Gemfile, которые нужны для проекта.

6) После описания сценариев в файле db.feature и шагов в файле db_steps.rb, можно запустить тесты командой:
```
cucumber
```
____
## WorkWithAPI_APITest-HttParty
Этот проект является автоматизированным тестированием API NASA EPIC: в этом примере тесты на Ruby, с использованием Cucumber+HttParty проверяют, что при использовании правильного API ключа, запрос к эндпоинту "/EPIC/api/natural/images" возвращает статус 200 и тело ответа содержит поля "date" и "image".

***Пояснение:***
Httparty - это более простая и легковесная библиотека, которая предоставляет удобный интерфейс для отправки запросов и получения ответов. Она поддерживает большинство HTTP-методов (GET, POST, PUT, DELETE) и может работать с JSON и XML форматами данных. Httparty также предоставляет удобные методы для работы с заголовками и параметрами запроса.

**Алгоритм:**
1) Создать папку проекта с названием "WorkWithAPI_APITest-HttParty"

2) В папке проекта, выполнить команду:
```
bundle init
```
:white_check_mark: Результат: Создается файл Gemfile.
В данном случае, cucumber для написания BDD-тестов, rspec для проверки результатов тестов и httparty для отправки HTTP-запросов к API.

3) В папке проекта, в файле Gemfile прописать:
```
source 'https://rubygems.org'
gem 'cucumber'
gem 'rspec'
gem 'httparty'
```

4) В папке проекта, выполнить команду:
```
bundle install
```
:white_check_mark: Результат: В папку проекта, устанавливаются гемы, которые будут использоваться.

5) В папке проекта features, создать файл api.feature
***Пояснение:*** В этом файле,на языке Gherkin, описываются сценарии, которые будут проверяться.

6) В папке проекта step_definitions, создать файл api_steps.rb
***Пояснение:*** В этом файле, описывается реализация шагов сценария.
____
## WorkWithAPI_Gemfile,Cucumber
В этом примере, тесты на Ruby, с использованием Cucumber+RestClient проверяют, что при использовании правильного API ключа, запрос к эндпоинту "/EPIC/api/natural/images" возвращает статус 200 и тело ответа содержит поле "lunar_j2000_position"

***Пояснение:***
RestClient - это более мощная библиотека, которая предоставляет больше возможностей для настройки запросов и обработки ответов. Она также поддерживает большинство HTTP-методов и может работать с различными форматами данных. RestClient позволяет настраивать заголовки, параметры запроса, тело запроса и другие параметры. Она также поддерживает авторизацию и работу с прокси-серверами.
Файл config.yml содержит URL и apikey для удобства разработки и сопровождения кода тестов.

**Алгоритм:**
1) Создать папку проекта с названием "WorkWithAPI_Gemfile,Cucumber"

2) В папке проекта, выполнить команду:
```
bundle init
```
:white_check_mark: Результат: Создается файл Gemfile.
! Gemfile - это файл, который используется в проектах Ruby для управления зависимостями и установки необходимых гемов (библиотек) для работы приложения. В этом файле перечислены все необходимые зависимости проекта. В данном случае, gem 'cucumber' используется для написания и запуска BDD-тестов, gem 'rspec' используется для проверки ответа от сервера после отправки запроса с помощью RestClient, gem 'rest-client' используется для отправки HTTP-запросов и получения ответов, gem 'webmock' используется для имитации ответов на запросы в тестах. Каждый из этих гемов используется в соответствующих файлах (например, cucumber в api.feature, rspec в api_steps.rb и т.д.).

3) В папке проекта, в файле Gemfile прописать:
```
source 'https://rubygems.org'
gem 'cucumber'
gem 'rspec'
gem 'rest-client'
```

4) В папке проекта, выполнить команду:
```
bundle install
```
:white_check_mark: Результат: В папку проекта, устанавливаются гемы, которые будут использоваться.

5) В папке проекта features, создать файл api.feature
***Пояснение:*** В этом файле,на языке Gherkin, описываются сценарии, которые будут проверяться.

6) В папке проекта step_definitions, создать файл api_steps.rb
***Пояснение:*** В этом файле, описывается реализация шагов сценария.

7) В файле env.rb прописывается строка:
```
require 'rest-client'
```
***Пояснение:*** Здесь я показываю альтернативу: RestClient может быть уже установлен в системе или на сервере, где будет запускаться проект. В таком случае, нет необходимости устанавливать его через Gemfile. Кроме того, это может быть выбором разработчика или команды, которая предпочитает не использовать Gemfile для определенных зависимостей.
____
