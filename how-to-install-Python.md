# Установка интерпретатора Python и необходимых библиотек

Наиболее оптимальный способ установить на рабочий компьютер Python с необходимым окружением – воспользоваться программным продуктом Anaconda. Помимо собственно интерпретатора языка Python она содержит систему по управления библиотеками conda (установка, удаление, обновление библиотек и проч.). ПО Anaconda работает на всех основных операционных системах: Windows, MacOS, Linux.

Мы будем использовать минимальную установку Anaconda, т.н. Minicoda, а потом установим те библиотеки, которые нам будут необходимы. Тем самым мы сэкономим место на жёстком диске.

Для установки необходимо зайти по [ссылке](https://docs.conda.io/projects/miniconda/en/latest/) (сайт conda.io) и скачать версию для своей операционной системы (для MacOS выбрать файл с расширением .pkg). 

Базово работа с Miniconda основана на работе с командной строкой. Это не страшно, нам понадобиться всего-навсего 2-3 команды

Попробуйте самостоятельно установить Miniconda (при установки используйте предлагаемы настройки по умолчанию) и обновить пакеты до последних версий по следующей инструкции.

* Windows: в меню Пуск после установки появиться Miniconda3. Зайдите туда и запустить Anaconda Prompt Shell. Окно с командной строкой. Введите команду conda update --all (двойное тире!) и нажмите Enter. На предлагаемый вопрос нужно ответить y [yes]. После обновления выполните команду exit (выйти из командной строки)

* MacOs: запустите Терминал (Launchpad -> Другие -> Терминал). В Терминале введите команду conda update --all (двойное тире!) и нажмите Enter. На предлагаемый вопрос нужно ответить y [yes]. После обновления выполните команду exit (выйти из Терминала). После этого Терминал можно закрыть (Cmd + Q)

# Установка основных библиотек

В командной строке (Anaconda PowerShell Prompt в Windows, Terminal в MacOS) выполнить следующие команды (это нужно сделать только один раз!)

- `conda install -c plotly plotly`
- `conda install pandas numpy scipy statsmodels openpyxl`
- `conda install -c anaconda jupyter jupyterlab pandas-datareader`
- `conda install -c conda-forge yfinance matplotlib linearmodels seaborn sklearn`

# Обновление установленных библиотек

В командной строке (Anaconda PowerShell Prompt в Windows, Terminal в MacOS) выполнить `conda update --all`