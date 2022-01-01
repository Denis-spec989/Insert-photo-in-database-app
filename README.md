# Приложение для добавления изображения в базу данных 
____
Приложение позволяет добавлять выбранное изображение в базу данных на сервере. Просмотр добавленного изображения возможен с помощью [приложения](https://github.com/Denis-spec989/Image-reader-in-database). 
___
## Оглавление
1. [Описание приложения](#anchor2)
2. [Демо проекта](#anchor)
3. [Используемые технологии в проекте](#anchor3)
4. [Техническое описание проекта](#anchor1)
___
<a id="anchor2"></a>
### 1.Описание приложения
Данное приложения для добавления изображения в базу данных было написано на open-source среде разработки **Apache Netbeans IDE** с использованием **Java SE 16** и драйверов для работы **JDBC**-Microsoft JDBC Driver for SQL Server(Type 4). Установка и настройка проекта будет указана в пункте [Техническое описание проекта](#anchor1)

**Цель проекта** - программное добавления локальных данных (фотографии с вашего компьютера) на удаленный сервер с установленной базой данных(в нашем случае локальный сервер с установленной базой данных) 
___
<a id="anchor"></a>
### 2.Демо проекта 
**Запускаем приложение для просмотра изображений**
![avat](https://sun9-35.userapi.com/impg/KdiiohGplsB_1coXGLqEaUGPvqJ4Y9mJbfTQ-w/lECB8DV2NCg.jpg?size=1919x1029&quality=96&sign=56fa1a9c2d3358cfe6b4a28dc0b67019&type=album)
В нашей базе данных уже лежат фотографии.(Эти фотографии добавлялись при предыдущих тестах программы)

**Добавим еще одну фотографию**.
![avat](https://sun9-13.userapi.com/impg/HhdWJohLLF3QaKwLBPgECgOZhQz7u9iOaOrNZA/9l33-ICbats.jpg?size=450x253&quality=96&sign=fdfedcc0ea2436654f40388fdf17fd65&type=album)

**Просмотрим где лежит наше изображение**.
![avat](https://sun9-32.userapi.com/impg/nt3Vic7u7wEiTiESNqx_VcLDVX_vUlCOLO30Ig/8GguT1ZcizA.jpg?size=737x216&quality=96&sign=85dd7eb6c50502257040b9a137d254da&type=album)

**Внесем название и полный путь изображения в программу.**
```Java
package photoinsertapp;

/**
 *
 * @author Denis
 */
public class PhotoInsertApp {

  
     public static void main(String[] args) {
        // Сохранение выбранного изображения в базу//Saving the selected image to the demonstration data base on Microsoft SQL Server 2019 Express
       MySQL.putPhoto("testphoto1","C:\\Users\\Denis\\photos\\testphoto1.jpg");
    }
}
```

**Запустим программу для просмотра изображения и убедимся , что добавлено корректно**
![avat](https://sun9-38.userapi.com/impg/ndhSPTzY0YnrKjBE1R59dCmpkxz2iR7cenN95g/mCSjnOYJ98k.jpg?size=1915x1025&quality=96&sign=9802672de10d2234597297960c78d37e&type=album)
**Все работает :blush:**
___
### 3.Используемые технологии в проекте
<a id="anchor3"></a>
:heavy_check_mark: JDBC
:heavy_check_mark: SQL-запросы
:heavy_check_mark: Java Stream API
:heavy_check_mark: Java Class File
___
<a id="anchor1"></a>
### 4.Техническое описание проекта
Для запуска программы нам необходимо установить Microsoft® SQL Server® 2019 Express и демонстрационную базу данных AdventureWorks. Инструкцию по установке можно скачать по [ссылке](https://drive.google.com/drive/folders/1nQEl9x66AHRCO1gxrRqVQUeVNUiVg4Q_?usp=sharing).
После инсталяции и настройки СУБД с БД , можете загрузить свою фотографию в свою базу данных на локальном сервере по [демо](#anchor).
Вы можете добавлять фотографии в базу данных , установленную на другом компьютере, для этого следует поменять url.
```
url="jdbc:sqlserver://127.0.0.1\\SQLExpress;database=AdventureWorks";
```
___
Автор: Игнатов Денис
e-mail: proanglerdenis@gmail.com


