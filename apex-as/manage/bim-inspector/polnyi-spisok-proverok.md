# Проверки

Проверки разделены на четыре группы:

* **Naming Convention**
* **Quality Requirements**
* **Rooms Counting**
* **Additional Suggestions**

## 📛 Naming Convention

Правила наименования элементов в соответствии со стандартом Apex.

### Materials

Если в проекте существуют материалы, наименование которых не соответствует актуальному Стандарту – они попадают в отчет.

Опции решения проблемы:

* \*\*\*\*[**More Info**](opcii-resheniya.md#more-info)\*\*\*\*
* \*\*\*\*[**Select Name**](opcii-resheniya.md#select-name)\*\*\*\*
* \*\*\*\*[**Delete with Replacement**](opcii-resheniya.md#delete-with-replacement)\*\*\*\*

### Material Classes

Проверка на соответствие правилу наименование класса материала. Запуск проверки только в случае успешного прохождения **Materials.**

Опции решения проблемы:

* \*\*\*\*[**More Info**](opcii-resheniya.md#more-info)\*\*\*\*
* \*\*\*\*[**Set Material Class**](opcii-resheniya.md#set-material-class)\*\*\*\*

### Fill Patterns

На соответствие правилу наименования образца штриховки.

Опции решения проблемы:

* \*\*\*\*[**Select Name**](opcii-resheniya.md#select-name)\*\*\*\*

### Filled Regions

На соответствие правилу наименования штриховой области. Запуск проверки только в случае успешного прохождения **Fill Patterns.**

### Walls : Basic Walls

Соответствие правилу наименования стен. Запуск проверки только в случае успешного прохождения **Materials** и **Material Classes.**

Опции решения проблемы:

* \*\*\*\*[**Rename**](opcii-resheniya.md#rename)\*\*\*\*
* \*\*\*\*[**Rename with a Comment**](opcii-resheniya.md#rename-with-a-comment)\*\*\*\*

### Floors

На соответствие правилу наименования полов. Запуск проверки только в случае успешного прохождения **Materials** и **Material Classes.**

Опции решения проблемы:

* \*\*\*\*[**Rename**](opcii-resheniya.md#rename)\*\*\*\*
* \*\*\*\*[**Rename with a Comment**](opcii-resheniya.md#rename-with-a-comment)\*\*\*\*

### Roofs : Basic Roofs

На соответствие правилу наименования крыш. Запуск проверки только в случае успешного прохождения **Materials** и **Material Classes.**

Опции решения проблемы:

* \*\*\*\*[**Rename**](opcii-resheniya.md#rename)\*\*\*\*
* \*\*\*\*[**Rename with a Comment**](opcii-resheniya.md#rename-with-a-comment)\*\*\*\*

### Levels

На соответствие правилу наименования уровней.

## 💪 Quality Requirements

Группа проверок связанных с качеством построения модели.

### Non Structural Elements

На соответствие значения параметра **FAM\_DuplicatesSS** назначению элементов.

Опции решения проблемы:

* \*\*\*\*[**Set No**](opcii-resheniya.md#set-no)\*\*\*\*

### Structural Elements

Проверка на соответствие значения параметра **FAM\_DuplicatesSS** назначению элементов.

Опции решения проблемы:

* \*\*\*\*[**Set Yes**](opcii-resheniya.md#set-yes)\*\*\*\*

### Filled Regions. W/o pattern

У штриховой области отсутствует образец штриховки.

### Import Symbols. Unlinked

DWG используется как Import, а не как Link.

Опции решения проблемы:

* \*\*\*\*[**Delete**](opcii-resheniya.md#delete)\*\*\*\*

### Levels. Same elevation: &lt;elevation&gt;

Уровни с идентичной высотной отметкой.

### Line Patterns. IMPORTs

Образцы линий попавшие в проект в результате операции **Import CAD.**

### RVT Links. Workset

Связанный RVT файл находится в рабочем наборе с неподходящим именем.

Опции решения проблемы:

* \*\*\*\*[**Create WS / Move-to-Existing**](opcii-resheniya.md#create-ws-move-to-existing)\*\*\*\*
* \*\*\*\*[**Rename Workset**](opcii-resheniya.md#rename-workset)\*\*\*\*

## 🏘️ Rooms Counting

Группа проверок связанных с квартирографией.

### Rooms. Type to Name Matching

Проверка на соответствие значения параметра **ROM\_RoomType** названию помещения.

### Rooms. Type

Проверка на соответствие значения параметра **ROM\_RoomType** назначению помещения.

Опции решения проблемы:

* \*\*\*\*[**Select Type**](opcii-resheniya.md#select-type)\*\*\*\*

### Rooms. Flat Number

Проверка значений параметра **ROM\_NumberFlat**. Значение должно быть натуральным числом в диапазоне от 1 до 9999.

### Flat &lt;Key&gt;. Room numbers \(&lt;number of rooms&gt;\)

Список помещений, номера которых внутри квартиры не являются последовательными

### **Flat** &lt;Key&gt;**. Inconsistent**

Проверка квартиры на "связанность" помещений.

Если  не все помещения в квартире имеют связь с остальными помещениями \(например, "пропала" дверь\), это будет отражено в результатах проверки. 

![](../../../.gitbook/assets/image%20%2840%29.png)

{% hint style="info" %}
Во избежание ложноположительных срабатываний, не используйте значения параметра **ROM\_RoomType** зарезервированные за помещениями квартир у помещений квартирами не являющимися.
{% endhint %}

## 🦄 Additional Suggestions

Дополнительный проверки. Могут занимать значительное время. По умолчанию отключены.

### Families. Update needed

Поиск загруженных семейств для которых в библиотеке Apex имеются обновленные версии.



