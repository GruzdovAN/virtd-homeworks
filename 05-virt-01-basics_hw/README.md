

# Домашнее задание к занятию 1.  «Введение в виртуализацию»


## Задача 2

Выберите один из вариантов платформы в зависимости от задачи. Здесь нет однозначно верного ответа так как все зависит от конкретных условий: финансирование, компетенции специалистов, удобство использования, надежность, требования ИБ и законодательства, фазы луны.

Тип платформы:

- физические сервера;
- паравиртуализация;
- виртуализация уровня ОС;

Задачи:

- высоконагруженная база данных MySql, критичная к отказу;
- различные web-приложения;
- Windows-системы для использования бухгалтерским отделом;
- системы, выполняющие высокопроизводительные расчёты на GPU.

Объясните критерии выбора платформы в каждом случае.

## Задача 2 ответ

Для решения каждой из задач выбор платформы будет зависеть от различных критериев, таких как производительность, надежность, управляемость, безопасность, стоимость и требования к ИБ. Давайте рассмотрим каждый случай:

*Высоконагруженная база данных MySql, критичная к отказу:*

Выбор: Физические сервера или виртуализация уровня ОС.
Обоснование: Для высоконагруженных баз данных, особенно критичных к отказу, может быть предпочтительнее использование физических серверов или виртуализации уровня ОС, чтобы обеспечить максимальную производительность, предсказуемость ресурсов и изоляцию от других приложений.

*Различные web-приложения*:

Выбор: Виртуализация уровня ОС или паравиртуализация.
Обоснование: Для веб-приложений, требующих гибкости масштабирования и изоляции, можно использовать виртуализацию уровня ОС или паравиртуализацию. Это позволяет эффективно использовать ресурсы сервера и обеспечивать изоляцию между приложениями.

*Windows-системы для использования бухгалтерским отделом:*

Выбор: Виртуализация уровня ОС или паравиртуализация.
Обоснование: Для Windows-систем, используемых бухгалтерским отделом, можно использовать виртуализацию уровня ОС или паравиртуализацию в зависимости от требуемой изоляции и управляемости. Это позволяет эффективно управлять ресурсами и обеспечивать безопасность данных.

*Системы, выполняющие высокопроизводительные расчёты на GPU:*

Выбор: Физические сервера.
Обоснование: Для систем, требующих высокой производительности GPU, обычно предпочтительнее использовать физические сервера с высокопроизводительными графическими процессорами. Виртуализация может ввести дополнительные накладные расходы на производительность из-за виртуализации аппаратных ресурсов.
Выбор платформы также может зависеть от доступности ресурсов, экспертизы в области управления конкретной платформой, требований к масштабируемости и гибкости, а также сроков и бюджета проекта.

## Задача 3

Выберите подходящую систему управления виртуализацией для предложенного сценария. Опишите ваш выбор.

Сценарии:

1. 100 виртуальных машин на базе Linux и Windows, общие задачи, нет особых требований. Преимущественно Windows based-инфраструктура, требуется реализация программных балансировщиков нагрузки, репликации данных и автоматизированного механизма создания резервных копий.
2. Требуется наиболее производительное бесплатное open source-решение для виртуализации небольшой (20-30 серверов) инфраструктуры на базе Linux и Windows виртуальных машин.
3. Необходимо бесплатное, максимально совместимое и производительное решение для виртуализации Windows-инфраструктуры.
4. Необходимо рабочее окружение для тестирования программного продукта на нескольких дистрибутивах Linux.

## Задача 3 решение

Для каждого из предложенных сценариев выбор системы управления виртуализацией может быть различным. Давайте рассмотрим каждый случай:

*1. 100 виртуальных машин на базе Linux и Windows, общие задачи:*

Выбор: VMware vSphere.
Обоснование: VMware vSphere предоставляет широкий спектр функций для управления виртуализированной инфраструктурой, поддерживает как Linux, так и Windows виртуальные машины, имеет инструменты для программного балансирования нагрузки, репликации данных и создания резервных копий.

*2. Виртуализация небольшой инфраструктуры на базе Linux и Windows:*

Выбор: KVM (Kernel-based Virtual Machine).
Обоснование: KVM является частью ядра Linux и предоставляет хорошую производительность для виртуализации. Он бесплатен и имеет открытый исходный код, что делает его привлекательным для небольших инфраструктур.

*3. Виртуализация Windows-инфраструктуры:*

Выбор: Microsoft Hyper-V.
Обоснование: Microsoft Hyper-V является интегрированным решением для виртуализации Windows-инфраструктуры. Он бесплатен, легко устанавливается на Windows-сервера и обеспечивает хорошую совместимость с Windows-средой.

*4. Рабочее окружение для тестирования на нескольких дистрибутивах Linux:*

Выбор: VirtualBox.
Обоснование: VirtualBox - это бесплатное и легкое в использовании решение для виртуализации. Оно поддерживает различные дистрибутивы Linux и обладает простым интерфейсом, что делает его отличным выбором для тестирования программного обеспечения.

## Задача 4

Опишите возможные проблемы и недостатки гетерогенной среды виртуализации (использования нескольких систем управления виртуализацией одновременно) и что необходимо сделать для минимизации этих рисков и проблем. Если бы у вас был выбор, создавали бы вы гетерогенную среду или нет?

## Задача 4 решение

Использование гетерогенной среды виртуализации, где применяются различные системы управления виртуализацией одновременно, может привести к нескольким проблемам и рискам:

1. **Сложность управления:** Каждая система управления виртуализацией имеет свои собственные интерфейсы и методы управления, что может создавать сложности при администрировании и мониторинге всей инфраструктуры.

2. **Неоднородность конфигураций:** Разные системы виртуализации могут предоставлять различные возможности и уровни поддержки, что может привести к неоднородности конфигураций и усложнить стандартизацию и обеспечение безопасности.

3. **Интеграционные проблемы:** Различные системы виртуализации могут иметь разные протоколы и методы коммуникации, что может создавать проблемы при интеграции с другими сервисами и инструментами в вашей инфраструктуре.

4. **Усложнение масштабирования:** При необходимости масштабирования инфраструктуры могут возникнуть дополнительные сложности из-за различий в процессах управления и конфигурации разных систем виртуализации.

5. **Повышенный риск сбоев:** Использование нескольких систем виртуализации одновременно увеличивает вероятность возникновения ошибок и сбоев из-за сложностей в управлении и интеграции.

Для минимизации рисков и проблем в гетерогенной среде виртуализации необходимо:

1. **Стандартизация и автоматизация:** Создание стандартов конфигурации и процессов управления для всех систем виртуализации, а также автоматизация задач управления и мониторинга.

2. **Централизованное управление:** Использование централизованных систем управления, которые могут обеспечивать единый интерфейс для управления всей инфраструктурой.

3. **Интеграция и API:** Использование API и интеграционных инструментов для обеспечения совместимости и взаимодействия между разными системами виртуализации.

4. **Обучение и поддержка персонала:** Обеспечение достаточного обучения и поддержки для администраторов, чтобы они могли эффективно управлять гетерогенной средой.

Если бы у меня был выбор, я бы стремился к минимизации гетерогенности в среде виртуализации, предпочитая использовать единые и согласованные решения, чтобы упростить управление, обеспечить единый стандарт и уменьшить риски возникновения проблем. Однако, в некоторых случаях использование различных систем виртуализации может быть необходимо из-за специфических требований или ограничений.