# JDCP-6_E.Orlov_Homework13
Домашнее задание по теме «Внедрение системы контроля версий»
## Демонстрация работы SalesManager
### Краткое описание:
В классе **`Main`** менеджеру продаж передаётся некий произвольный список различных целых чисел,

а класс **`SalesManager`** по запросу ***`salesManager.max()`*** возвращает из этого списка число максимального размера.

## Условия задачи

### Задача 1 (обязательная):

Ваш отдел решил автоматизировать часть задач из отдела продаж, и начать решили с написания простого инструмента анализа статистики продаж. Перед вами даже первая версия такого сервиса:

```java
public class SalesManager {
    protected int[] sales;

    public SalesManager(int[] sales) {
        this.sales = sales;
    }

    public int max() {
        int max = -1;
        for (int sale : sales) {
            if (sale > max) {
                max = sale;
            }
        }
        return max;
    }
}
```
Вам доверили этот сервис “заверсионировать” - так программисты говорят, когда имеют ввиду создание репозитория и подключения его к проекту для контролирования его версий.
### Что вам нужно:
1. Создать публичный репозиторий на гитхаб
1. Создать локальный репозиторий, инициализировав его прямо в корне папки проекта идеи
1. Связать публичный репозиторий с локальным
1. Создать файл `.gitignore`, вписав туда правила, перечисленные выше в чеклисте для этой задачи
1. Создать в папке `src` переданный вам класс
1. Сделать коммит
1. Добавить класс `Main`, в котором вы продемонстрируете работу класса `SalesManager`
1. Добавить файл `README.md`, в котором вы опишите как же работает этот менеджер продаж (не забудьте про [правила форматирования текста](https://www.markdownguide.org/basic-syntax/) в этом файле)
1. Сделать второй коммит
1. Запушить все изменения на гитхаб, убедиться что не подхватился никакой мусор, а текст в ридми красиво отображается