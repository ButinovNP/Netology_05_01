
## Домашнее задание к занятию "5.1. Введение в виртуализацию. Типы и функции гипервизоров. Обзор рынка вендоров и областей применения."

---

## Задача 1

Опишите кратко, как вы поняли: в чем основное отличие полной (аппаратной) виртуализации, паравиртуализации и виртуализации на основе ОС.

### Решение:
- Полная виртуализация: Гипервизоры работают на аппаратном уровне без необходимости установки ОС на хост. Они сами являются ОС.
- Паравиртуализация: Гипервизорам необходима ОС для доступа к аппаратным ресурсам хоста.
- Виртуализация на уровне ОС: позволяет запускать изолированные и безопасные ВМ на одном хосте, но не позволяет запускать ОС с ядрами, отличными от типа ядра хостовой ОС.
Таким образом, отличие типов виртуализации состоит в том, каким образом гипервизор получает доступ к аппаратным ресурсам хоста.


## Задача 2

Выберите один из вариантов использования организации физических серверов, в зависимости от условий использования.

Организация серверов:
- физические сервера,
- паравиртуализация,
- виртуализация уровня ОС.

Условия использования:
- Высоконагруженная база данных, чувствительная к отказу.
- Различные web-приложения.
- Windows системы для использования бухгалтерским отделом.
- Системы, выполняющие высокопроизводительные расчеты на GPU.

Опишите, почему вы выбрали к каждому целевому использованию такую организацию.

### Решение:
- Высоконагруженная база данных, чувствительная к отказу - физические сервера.
- Различные web-приложения - виртуализация уровня ОС.
- Windows системы для использования бухгалтерским отделом - паравиртуализация.
- Системы, выполняющие высокопроизводительные расчеты на GPU - физические сервера.


## Задача 3

Выберите подходящую систему управления виртуализацией для предложенного сценария. Детально опишите ваш выбор.

Сценарии:

1. 100 виртуальных машин на базе Linux и Windows, общие задачи, нет особых требований. Преимущественно Windows based инфраструктура, требуется реализация программных балансировщиков нагрузки, репликации данных и автоматизированного механизма создания резервных копий.
2. Требуется наиболее производительное бесплатное open source решение для виртуализации небольшой (20-30 серверов) инфраструктуры на базе Linux и Windows виртуальных машин.
3. Необходимо бесплатное, максимально совместимое и производительное решение для виртуализации Windows инфраструктуры.
4. Необходимо рабочее окружение для тестирования программного продукта на нескольких дистрибутивах Linux.

### Решение:
1. VMware - наиболее подходит под указанный сценарий.
2. KVM - бесплатный, с открытым исходным кодом, позволяет получить высокую производительность.
3. Microsoft Hyper-V Server - бесплатен и полностью совместим с Windows инфраструктурой, так как разработан корпорацией Microsoft (разработчиком Windows).
4. Xen - так как более стабилен чем KVM.



## Задача 4

Опишите возможные проблемы и недостатки гетерогенной среды виртуализации (использования нескольких систем управления виртуализацией одновременно) и что необходимо сделать для минимизации этих рисков и проблем. Если бы у вас был выбор, то создавали бы вы гетерогенную среду или нет? Мотивируйте ваш ответ примерами.

### Решение:
Гетерогенная среда виртаулизации - довольно сложна в управлении, требует специалистов различного профиля и, следовательно, является дорогостоящей - это и есть её основной недостаток.

Для минимизации этого риска - следует избегать создания и использования гетерогенной среды виртуализации.

При наличии выбора лично у меня - я бы отказался от создания гетерогенной среды виртуализации, постарался бы понять необходимые задачи и выбрать гибридное решение, обеспечивающее реализацию текущих задачь, упрощающее управление инфраструктурой и её масштабируемость.
