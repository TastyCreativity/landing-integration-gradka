
Разгортванне шаблона градкі на асноўным дамене.

1. Заходзім у адмінку Друпала па адрасу http://falanster.by/be/user -> уваход у сістэму.
    У вас павінны быць логін і пароль (выдаюцца адміністратарамі Фаланстэра)
2. Па першае заходзім на старонку http://falanster.by/be/admin/config/content/ckeditor/edit/Full
3. Унізе націсківаем "Прасунутыя наладкі"
4. У поле Custom JavaScript configuration дадаем наступныя строкі, калі іх няма
    config.allowedContent = true;
    config.extraAllowedContent = 'p(*)[*]{*};div(*)[*]{*};li(*)[*]{*};ul(*)[*]{*}';
    CKEDITOR.dtd.$removeEmpty.i = 0;
    CKEDITOR.dtd.$removeEmpty.span = 0;
    CKEDITOR.dtd.a.div = 1;
    CKEDITOR.dtd.a.p = 1;
    CKEDITOR.dtd.a.img = 1;
    CKEDITOR.dtd.a.h3 = 1;	
    Гэта не дазволіць рэдактару змяняць верстку пры рэдагаванні кантэнта праз рэдактар. Інакш некаторыя тэгі могуць згубіцца.
5. Націскваем кнопку Адправіць.
6. Далей ідзем па адрасу https://github.com/TastyCreativity/landing-integration-gradka
    Тут павінна ляжаць апошняя версія тэмы для старонак Градкі.
    Націсківаем кнопку Download і атрымліваем архіў з файламі тэмы.
    (Калі ў вас усталяваны git, то каманда git clone https://github.com/TastyCreativity/landing-integration-gradka.git дазваляе атрымаць лакальную копію рэпазіторыя.)
7. Распакоўваем скачаны архіў.
8. Цяпер нам патрэбны sftp дасяг непасрэдна да сэрвера Фаланстэра.
9. Ветліва пішам адміністратарам Фаланстэра з запытам на рэквізіты доступа к сэрверу.
10. У вас запросяць ssh ключ, каб раздаць вам неабходныя правы.	


------Далей ідзе гайд толькі пад Windows---------------------------------------------------------------------------------


11. Качаем https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html і адчыняем архіў. Тулза PAGENT дазваляе рабіць генерацыю ключэй і падтрымлівае працу з імі.
12. Запускае PAGENT і дадаем туды свой прыватны ключ.
12. Далей патрэна усталяваць кліент, які зможа падключацца к сэрверу Фаланстэра з вашым ключом.
    (Прыклад https://winscp.net/eng/download.php)
13. Пасля інсталяцыі winscp запускаем яе. Туды трэба ўвесці дадзеныя па доступу, атрыманыя ад адміністратараў.
    Пратакол доступа SFTP. 
    
--------------------------------------------------------------------------------------------------------------------------
-------Частка далей пойдзе і для Unix-сістэм------------------------------------------------------------------------------


14. Пераходзім у каталог на сэрвере /home/falanster/web/falanster.by/public_html/sites/all/themes.
15. Туды капіруем файлы тэмы, якія мы загрузілі раней з git рэпазіторыя у кроках 6-7.
16. Далей зноў адчыняем http://falanster.by/be. Калі вы не ў адмінке, трэба зайсці. Крок 1.
17. У левым верхнім углу наводзім курсор на Малюнак хаты і націсківаем Flush all caches ў выпадаючым меню.
18. Усе, тэма ўсталявана, квест завершаны. Засталося не шмат да пабеды.
19. Адчыняем у браузеры http://falanster.by/be/creativecommons
20. Калі ўсе выглядае добра, больш дзеянняю не патрабуецца. 
21. Інакш трэба заліць кантэнт.
23. Кантэнт ляжыць у рэпазіторыі https://github.com/tastycreativity/gradka/ у файлах index.html і index-en.html. (для розных моў)
22. Адчыняем старонку http://falanster.by/be/node/1099/edit.
23. У рэдактар капіруем тое, што знаходзіцца, паміж тэгамі <body></body> (іх не уключаем) у файле index.html.
    Змяняем страку
    <a class="nav-link" href="index-en.html">EN</a>
    на
    <a class="nav-link" href="https://ftest.falanster.by/en/creativecommons">EN</a></li>
24. Націсківаем кнопку "Адправіць".
25. Далей адчыняем у браузеры http://falanster.by/en/node/1136/edit
26. У рэдактар капіруем тое, што знаходзіцца, паміж тэгамі <body></body> (іх не уключаем) у файле index-en.html.
    Змяняем страку
    <li class="nav-item language-switcher item"><a class="nav-link language-switcher item_active" href="index.html">BY</a></li>
    на
    <li class="nav-item language-switcher item"><a class="nav-link" href="https://ftest.falanster.by/be/creativecommons">BY</a></li>

    Змяняем страку
    <li class="nav-item language-switcher item"><a class="nav-link" href="index-en.html">EN</a></li>
    на
    <li class="nav-item language-switcher item"><a class="nav-link language-switcher item_active" href="index-en.html">EN</a></li>
27. Націсківаем кнопку "Адправіць".
28. Правяраем сайт. Калі усе добра вы - маладзец, калі не, паўтарыце яшчэ раз, удачы. 

