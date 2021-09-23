Работа со сценариями
========
Юнит тесты — это неотъемлемая часть любого качественного продукта, однако на этом труд QA-инженера не заканчивается. 
Порой куда более важной задачей является проверка функционала, который включает в себя множество шагов и интеракций. 
Именно в данной ситуации небольшие тесты объединяются в **позитивные** и **негативные** тестовые сценарии.

**Позитивные** — проверяют что функционал работает так, как мы ожидаем и приводит пользователя в нужное нам состояние.

**Негативные** — позволяют удостовериться, что некорретные действия пользователя не нарушают работоспособность системы.

BDD подход
========
**Behavior Driven Design** — это подход, позволяющий описывать тестовые сценарии на понятном языке как разработчику автотестов, 
так и бизнесу. В примере, который содержит данный репозиторий, используется тестовый фреймворк **Cucumber**, разработанный для 
реализации BDD подхода. С помощью его внутренней нотации **Gherkin** (src/test/resources/features/scenario.feature) описываются тестовые сценарии и их шаги, затем они имплементируются и запускаются.

Page Object Model паттерн
========
К сожалению, тестовый фреймворк решает не все проблемы, связанные с организацией логики тестов. Во время автоматизации тестирования 
веб-страниц (и не только их) появляются сложности с внесением изменений, расширением и поддержкой тестов. Для того чтобы 
избежать этих проблем, следует использовать паттерн **Page Object Model**. Суть проста — всю логику взаимодествия с элементами 
конкретной страницы следует вынести в отдельный класс, который будет являться абстракицей над этой страницей (классы ChooseCityPage и CityMenuPage).

Домашнее задание к вебинару: 
========
Для выбранного веб-сайта продумать негативный и позитивный тестовые сценарии и реализовать их с использованием **Cucumber**.

Критерии оценивания:
========
* 0 баллов — не выполнено ничего.
* 1 балл — описанны тестовые сценарии, тесты запускаются и проходят.
* 2 балла — описанны тестовые сценарии, тесты запускаются и проходят, логика взаимодействия со элементами страниц инкапсулирована с помощью паттерна Page Object Model.

