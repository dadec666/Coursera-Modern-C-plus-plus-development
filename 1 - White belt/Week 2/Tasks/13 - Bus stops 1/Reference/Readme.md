Пожалуй, самое сложное в этой задаче — внимательно прочитать условие и аккуратно реализовать все его требования, выбрав при этом правильные контейнеры.

Поскольку необходимо было получать как список остановок для конкретного автобуса, так и список автобусов для конкретной остановки, логичнее всего было определить два словаря — buses_to_stops и stops_to_buses со строковыми ключами и значениями типа vector<string>.

Ответы на большинство запросов вынесем в отдельные функции: это позволит повысить читаемость кода. Заметьте, что при этом не всегда удаётся передавать словари по константным ссылкам: это происходит из-за того, что использование квадратных скобок (например, в коде stops_to_buses[stop]) теоретически может изменить словарь. В этой ситуации стоило бы использовать метод at вместо квадратных скобок — мы рассмотрим его в следующем курсе.