# ДЗ использование VisualCode

#### Разбор программы, данные из консоли:

```sh
Please open 'ru.netology.JvmExperience' in VisualVm
22:45:38.620193: loading io.vertx
22:45:38.895243100: loaded 529 classes
```

## Heap (Куча)

![1 фото](https://github.com/SadovskiiAleks/studyJVM/blob/main/1%20%D1%84%D0%BE%D1%82%D0%BE.jpg)
![2 фото](https://github.com/SadovskiiAleks/studyJVM/blob/main/2%20%D1%84%D0%BE%D1%82%D0%BE.jpg)
> На данном этапе было объявлено 529 новых классов. Объекты данных классов сохранились в «куче»

## Metaspase
![3 фото](https://github.com/SadovskiiAleks/studyJVM/blob/main/3%20%D1%84%D0%BE%D1%82%D0%BE.jpg)
> Добавлены сразу данные по классам (по графикам можно понять, что объявленные объекты класса пустые т. к. Metaspase увеличилось на тоже количество байт)

## Classes
![4 фото](https://github.com/SadovskiiAleks/studyJVM/blob/main/4%20%D1%84%D0%BE%D1%82%D0%BE.jpg)
> По данному графику видно что система добавила классы в объявленном количестве

==========================================
# Разбор следущих данных:

```sh
22:45:41.908267300: loading io.netty
22:45:42.407945800: loaded 2117 classes
```

## Heap (Куча)
![5 фото](https://github.com/SadovskiiAleks/studyJVM/blob/main/5%20%D1%84%D0%BE%D1%82%D0%BE.jpg)

> Куча кратно увеличилась при создании загрузке классов

## Metaspase
![6 фото](https://github.com/SadovskiiAleks/studyJVM/blob/main/6%20%D1%84%D0%BE%D1%82%D0%BE.jpg)
> Данные по классам не изменились. Предполагаю, что метод просто загрузил новые объекты существующих классов 

## Classes
![7 фото](https://github.com/SadovskiiAleks/studyJVM/blob/main/7%20%D1%84%D0%BE%D1%82%D0%BE.jpg)
> Произошло кратное увеличение количества классов. Видно, что количество прибавленных совпадает.

==========================================
# Разбор следущих данных:

```sh
22:45:45.415317400: loading org.springframework
22:45:45.606515400: loaded 869 classes
```
## Heap (Куча)
![8 фото](https://github.com/SadovskiiAleks/studyJVM/blob/main/8%20%D1%84%D0%BE%D1%82%D0%BE.jpg)
> Зафиксирован непонятный обвал кучи, возможно отработал сборщик мусора (Garbage Collector ). Почти 120 000 000 B было зарезервировано под объекты которые никому не нужны.

## Metaspase

![9 фото](https://github.com/SadovskiiAleks/studyJVM/blob/main/9%20%D1%84%D0%BE%D1%82%D0%BE.jpg)

> Добавленна новая партия неизвестных(с точки зрения JVM) классов

## Classes
![10 фото](https://github.com/SadovskiiAleks/studyJVM/blob/main/10%20%D1%84%D0%BE%D1%82%D0%BE.jpg)
> Появление классов в штатном режиме


==========================================
# Разбор следущих данных:

```sh
22:45:48.608371900: now see heap
22:45:48.608371900: creating 5000000 objects
22:45:48.835265900: created
```

## Heap (Куча)
![11 фото](https://github.com/SadovskiiAleks/studyJVM/blob/main/11%20%D1%84%D0%BE%D1%82%D0%BE.jpg)
> добавлено большое место для новых объектов

## Metaspase
![12 фото](https://github.com/SadovskiiAleks/studyJVM/blob/main/12%20%D1%84%D0%BE%D1%82%D0%BE.jpg)
> отслеживается разница при добавлении объектов и создании классов. В метаспейс прирост небольшой

## Classes
> В классах изменений нету, добавлен только 1 класс. 

==========================================
# Разбор следущих данных:

```sh
22:45:51.848514500: creating 5000000 objects
22:45:52.009424700: created
```
## Heap (Куча)
![13 фото](https://github.com/SadovskiiAleks/studyJVM/blob/main/13%20%D1%84%D0%BE%D1%82%D0%BE.jpg)
 > Резкий прирост кучи обусловленный количеством созданных объектов
 
## Metaspase
> Тут изменений нету

## Classes

> В классах изменений нету, добавлен только 1 класс.

==========================================
# Разбор следущих данных:

```sh
22:45:55.064171: creating 5000000 objects
22:45:55.197089800: created
```
## Heap (Куча)
![14 фото](https://github.com/SadovskiiAleks/studyJVM/blob/main/14%20%D1%84%D0%BE%D1%82%D0%BE.jpg)
 > Резкий прирост кучи обусловленный количеством созданных объектов
 
## Metaspase
> Тут изменений нету

## Classes
> В классах изменений нету, добавлен только 1 класс.

==========================================
# Завершение программы:

```sh
BUILD SUCCESSFUL in 54s
2 actionable tasks: 1 executed, 1 up-to-date
22:45:58: Execution finished ':JvmExperience.main()'.
```

