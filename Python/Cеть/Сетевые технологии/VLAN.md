**VLAN (Virtual Local Area Network)** — это технология виртуальных локальных сетей, позволяющая логически разделять одну физическую сеть на несколько изолированных сетевых сегментов. Используя **VLAN**, устройства в одной физической сети могут быть сгруппированы в несколько виртуальных сетей, что повышает управляемость, безопасность и гибкость сети.

`VLAN`

**Пример использования:** В компании могут быть несколько отделов (бухгалтерия, IT, продажи), и для их изоляции создаются **VLAN**. Трафик каждого отдела передается только между участниками этой **VLAN**, даже если они физически подключены к одному коммутатору.

#### Основные принципы работы VLAN

- **Логическое разделение**: Устройства, подключенные к одному коммутатору или сети, могут быть разделены на различные **VLAN**, как будто они находятся в разных физических сетях, даже если используют одни и те же порты.

- **Изоляция трафика**: Устройства в одной **VLAN** не могут напрямую общаться с устройствами из другой **VLAN** без маршрутизации через устройство сетевого уровня (маршрутизатор).

- **Маркировка трафика (VLAN Tagging)**: Чтобы различать трафик из разных **VLAN** на одном физическом канале, используется тегирование кадров на основе стандарта **IEEE 802.1Q**. Этот тег добавляется в заголовок Ethernet-кадра и несет информацию о том, к какому **VLAN** относится этот кадр.

#### Типы VLAN

- **Управляющая VLAN (Management VLAN)**: Используется для управления сетевыми устройствами (коммутаторами, маршрутизаторами).

- **Гостевая VLAN**: Для устройств, которые должны иметь ограниченный доступ к сети.

- **VLAN данных**: Для обычных устройств пользователей, которые передают пользовательские данные.

- **VLAN голосовой связи (Voice VLAN)**: Предназначен для разделения трафика VoIP, чтобы повысить его приоритет и улучшить качество связи.

#### Преимущества VLAN

- **Безопасность**: Позволяет изолировать трафик между различными группами пользователей или отделами, снижая риски атак внутри сети.

- **Управляемость**: Проще управлять трафиком и разделять его по группам, таким как отделы компании.

- **Снижение широковещательного трафика**: **VLAN** ограничивает действие широковещательных сообщений в пределах одной **VLAN**, уменьшая нагрузку на сеть.

## Магистральные каналы (Trunk)

**Магистральный канал (Trunk)** — это специальное соединение между коммутаторами или коммутатором и маршрутизатором, которое позволяет передавать трафик нескольких **VLAN** одновременно через один физический канал. **Trunk** связывает сети **VLAN** друг с другом, обеспечивая передачу трафика из разных **VLAN** по одному каналу, используя тегирование.

#### Основные принципы работы магистрального канала:

- **Тегирование VLAN (802.1Q)**: Трафик каждой **VLAN** маркируется дополнительным тегом (802.1Q), который добавляется к каждому кадру. Этот тег несет информацию о том, из какой **VLAN** идет трафик, и используется для разграничения кадров из разных **VLAN** на магистральном канале.

- **Несколько VLAN на одном физическом канале**: Вместо создания отдельных физических соединений для каждой **VLAN**, магистральный канал позволяет использовать одно физическое соединение для передачи трафика множества **VLAN**.

- **Untagged трафик (Native VLAN)**: Это **VLAN** по умолчанию, которая используется для передачи нетегированного трафика на магистральном канале. Обычно Native **VLAN** применяется для административного или управления.

#### Преимущества магистральных каналов:

- **Экономия ресурсов**: Использование одного физического соединения для нескольких **VLAN** снижает количество необходимых физических соединений между коммутаторами.

- **Производительность**: Магистральные каналы могут обеспечивать более высокие скорости передачи данных за счет агрегирования каналов или использования технологий, таких как **EtherChannel** (объединение нескольких физических каналов в один логический).

- **Гибкость**: **Trunk** легко масштабируется и позволяет динамически добавлять новые **VLAN** без необходимости изменения физической инфраструктуры.

#### Пример использования:

В корпоративной сети может быть несколько **VLAN**, например, **VLAN** 10 (для отдела продаж) и **VLAN** 20 (для отдела IT). Для связи коммутаторов, обслуживающих эти **VLAN**, создается магистральный канал, через который передается трафик обеих **VLAN**. Коммутаторы помечают трафик с **VLAN** 10 и **VLAN** 20 с помощью тегов 802.1Q и передают их по одному физическому соединению.