Задание 1, Определить алгоритм наилучшего сжатия данных в zfs. вывод в консоли по ходу выполнения task1.txt
            Создаем 4 zpool командой zpool create
            Командой zfs set compression настраиваем различные алгоритмы сжатия для файловых систем
            Размещаем эталонный файл на каждой из файловых систем
            Оцениваем размер эталонного файла на каждой из файловых систем, исходя из этого понимаем, какой алгоритм сжимает лучше
            По параметру compressratio команды zfs get можно оценить коэфициент сжатия.
Задание 2, Определить настройки импортированного пула. вывод в консоли по ходу выполнения task2.txt
            Загружаем архив с эксопртом пула и распаковываем
            Командой zpool import -d оцениваем возможностьимпорта пула, узнаем его структуру, имя и id
            Командой zpool import -d с указанием имени или id пула импортируем его
            Теперь можно узнать интересующие параметры файловой системы командой zfs get с указанием интересуещего параметра, либо вывести все параметры zfs get all 
Задание 3, Работа со снапшотом. вывод в консоли по ходу выполнения task3.txt
            Загружаем ранее созданный файл снапшота.
            Восстанавливаем файловую систему из снапшота командой zfs recieve в качестве источника указываем файл снапшота, в качестве приемника файловую систему
            Теперь можно увидеть файлы и каталоги полученные из снапшота.
