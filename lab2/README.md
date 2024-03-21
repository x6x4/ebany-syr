
Библиотека регулярных выражений

Разработать библиотеку для работы с регулярными выражениями. В качестве алфавита могут использовать любые печатные символы, метасимволы экранируются символами ‘%s%’, где s – экранируемый символ.

Регулярный выражения должны поддерживать следующие операции:

Операция ‘или’: r1|r2 (метасимвол ‘|’)

Операция ‘конкатенация’: r1r2

Операция ‘замыкание Клини’: r… (метасимвол ‘…’)

Операция ‘опциональная часть’: r? (метасимвол ‘?’)

Операция ‘повтор выражения’: r{x} (метасимвол ‘{х}’, где x – количество повторов)

Операция ‘именованная группа захвата’: (<name>r) (метасимвол ‘(<name>)’, name – имя группы захвата)

Операция ‘выражение из именованной группы захвата’: <name> (метасимвол ‘<name>’, name – имя группы захвата)

В регулярных выражениях могут использоваться операторные скобки (r), определяющие приоритет операторов. (метасимвол ‘( )’)

Библиотека должна поддерживать следующие операции:

match – проверка соответствия строки регулярному выражению с перегрузкой без доступа и с доступом к группам захвата через специальный объект (через итератор и оператор индексации).

Регулярные выражения могут быть заранее скомпилированы в ДКА непосредственно без построения НКА (РВ->ДКА->минимальный ДКА), т.е. должен поддерживаться метод compile(), при этом допустим вызов операций с регулярными выражениями, как со скомпилированным объектом, так и со строковым представлением.

Для скомпилированных автоматов библиотека должна поддерживать операцию восстановления регулярного выражения методом исключения состояний.

Библиотека должна поддерживать операцию построения разности языков, задаваемых регулярными выражениями (скомпилированными ДКА).

Библиотека должна поддерживать операцию построения дополнения к языку, задаваемому регулярным выражением (скомпилированным ДКА).