# `ОбщегоНазначения.ОписаниеСвойствОбъекта` (`Common.ObjectPropertiesDetails`) 

Описание функции:

> Возвращает таблицу значений с описанием требуемых свойств всех реквизитов объекта метаданных.
> Получает значения свойств стандартных реквизитов и пользовательских реквизитов (созданных в режиме конфигуратора).

## Помощник ввода в строковых литералах

Поддержка ввода имен свойств, доступных для передаваемого тип объекта метаданных.


Пример:

```bsl
	МДО = Метаданные.Справочники.Товары;
	Таблица = ОбщегоНазначения.ОписаниеСвойствОбъекта(МДО, "Имя, <Ctrl+Space>);
```


## Типизация возвращаемых значений

Функция возвращает таблицу с типизированными колонками на основе типов свойств метаданного.

Пример:

```bsl
	Таблица = ОбщегоНазначения.ОписаниеСвойствОбъекта(Метаданные.Справочники.Товары, "Имя, Синоним, Справка");
	Для каждого Элемент из Таблица Цикл
		Имя = Элемент.Имя;
	КонецЦикла;
```


### Вычисление значений параметров

Для функций поддерживается вычисление контента строк переданных через локальные переменные, с вычислением бинарных операций (конкатенация строк) в рамках одной процедуры.

```bsl
	МДО = Метаданные.Справочники.Товары;
	ИменаСвойств = "Имя, МногострочныйРежим, Синоним, Справка";
	Таблица = ОбщегоНазначения.ОписаниеСвойствОбъекта(МДО, ИменаСвойств);
```

