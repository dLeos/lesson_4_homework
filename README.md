# ProjectT 2015 v2 - Домашнее задание #4
## Задание 1.
Выполено в домашнем задании №2.

## Задание 2.
1. почему защита 1 уровня "что-нибудь потестировать" не работает?

Защита 1 уровня "что-нибудь потестирую!" не работает, потому что такие тесты очень обрывчаты и всегда неравномерно находятся, что-то прверяется лчуше, что-то хуже. 
В результате:
 - часть ошибок не находится;
 - целостности в таком тестировании нет;
 - в таких тестах присутсвует предвзятость.

2. почему не помогает просто написать больше тестов?

Защита 2 уровня "Давайте напишем тесты!" не работает, потому что при увеличении числа тестов 
 - целостности все равно нет;
 - часть ошибок все равно будет пропускаться;
 - сил затрачено намного больше.

3. зачем нужно анализировать?

Защита 3 уровня "Давайте анализировать!" позволяет разобраться в архитектуре, сделать тесты более адаптивными, и сократить их количество. 
В результате пропускается меньше ошибок.

4. перечислите какие шаги нам нужноп выполнять, чтобы спроектировать хорошую защиту от багов? иными словами, опишите стратегию действий

Стратегия действий:
 - проанализировать продукт, внешние условия;
 - понять цели тестирования;
 - согласовать и учитывать все внешние потребности;
 - понять какие тесты нужны.

5. что мы должны сделать в рамках анализа? то есть что будет на выходе нашего анализа?

Анализ:
 - карта функционала и карта архитектуры;
 - статистика по истории ошибок;
 - риски возникновения новых ошибок; 
 - приоритет (важность) функционала;
 - критичность потенциальных ошибок.

Результаты анализа:
 - понимание того, что и как надо тестировать;
 - приоритеты с точки зрения пользователей и с точки зрения рисков.

6. зачем расставлять приоритеты? от чего зависит приоритет функциональности? на основании чего можно определить приоритет функциональности?

Приоритеты зависят от потребностей пользователей и от истории возникновения ошибок.
Приоритеты позволяют определить порядок тестирования (например, если какой-то функционал не важен, пользователю он не нужен, и ошибки там бывают не особо часто, то его можно тестировать позже).

7. какие бывают внещние факторы, которые могут повлиять на тестирование? зачем учитывать внешние факторы?

Внешние факторы:
 - длительность итераций;
 - регулярность публичных релизов;
 - ограничение по времени на тестирование;
 - допустимость и недопустимость ошибок;
 - возможности автоматизации.
Внешние факторы влияют на процесс тестирования, например, из-за ограничений по времени необходимо расставлять приоритеты тестирования, чтобы не упустить более важные ошибки.

8. охаректеризуйте разные комплекты тестов (зачем? как выбрать тесты в комплект? как часто прогонять? в чем задача каждого набора? нужно проводить для одной сборки или можно на нескольких? и тд): BVT, UAT, FTP? какие интересные особенности для каждого комплекта вы запомнили?

Комплекты тестов:
 - BVT (Build Verification Test) - позволяет быстро оценить качество ПО, найти более критичные ошибки сразу, иметь статистику стабильности продукта. Ищутся только важные и опасные ошибки за минимальное время. Их важно согласовывать с коллегами и  автоматизировать при малейшей возможности. 
 - FTP (Full Test Path) - позволяет собрать полную информацию о продукте, который тестируется, полный контроль качества продукта. Сюда входят все возможные и невозможные тесты (даже если у нас нет ресурсов на их прохождение).
 - UAT (User Acceptance Test) - позволяет определить готов ли продукт к релизу. Сюда входят тесты, необходимые для успешного использования продукта пользователями, при условии, что эти тесты укладываются в критерии сроков на тестирование.

Сначала используются BVT тесты (они самые маленькие и ловят самые большие ошибки), затем UAT тесты (они чуть по-больше и ловят менее крупные ошибки), потом FTP тесты (они ловят оставшиеся самые маленькие ошибки).

9. что делать, если пропустили баг в релиз

В случае если пропущена ошибка:
 - понять почему пропустили ошибку;
 - понять насколько критична ошибка;
 - определить какой из наборов (BVT, FTP, UAT) расширять;
 - расширить первоначальный анализ.
