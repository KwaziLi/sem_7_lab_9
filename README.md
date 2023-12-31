# Текст задания

Создайте одномодульный Java-проект, сборка которого управляется Maven. Это должно быть консольное Spring Boot приложение, которое принимает в качестве аргумента командной строки название факультета, института или название кафедры со страницы https://atlas.herzen.spb.ru/faculty.php.

Если речь идёт о конкретной кафедре, нужно извлечь URL со ссылкой на эту кафедру из атрибута href HTML элемента:

```<a class="alist" href="..."> название кафедры</a>```


Затем нужно распарсить уже страницу этой кафедры и распечатать на экране или записать в CSV файл все данные из таблицы преподавателей на страницы кафедры.

Если речь идёт о названии факультета или института, то надо в цикле распарсить всен страницы кафедр и получить данные о всех преподавателях.

Рекомендации:

Воспользуйтесь видео рядом с этим заданием в курсе.
Установите WSL (Windows for Linux) - подсистему Windows для Linux и установите подходящий для себя дистрибутив Linux, напрмер Arch Linux или Ubuntu.
Вместо WSL можете установить Git Bash (https://git-scm.com/) или Cygwin (https://www.cygwin.com/) для эмулятора командной строки Bash Linux.
Установите SDKMAN (https://sdkman.io/) внутри командной строки Bash.
Используйте команду sdk чтобы установить нужные версии Java (JDK), Maven и Spring Boot CLI (инструмент командной строки Spring Boot для быстрой генерации проектов). Например:

`sdk install java 17.0.9-oracle`

`sdk install maven 3.9.5`

`sdk install springboot 3.1.5`

Сгенерируйте базовый проект с помощью консольной команды spring init --build maven --force.
Используйте JSoup (https://jsoup.org/), чтобы парсить целевой сайт. добавьте его в секцию dependencies в pom.xml
Настройте IntelliJ Idea на те дистрибутивы JDK и Maven, которые вы установили с помощью SDKMAN.
Опционально можно доставить библиотеки для SDKMAN, написанные на Rust (https://github.com/sdkman/sdkman-cli-native).
