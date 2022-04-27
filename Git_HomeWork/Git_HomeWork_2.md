Termial. HW_2

 1. Сделать папку dir_1 - mkdir dir_1
 2. Зайти в папку dir_1 - cd dir_1
 3. Создать папку inner_dir_1 - mkdir inner_dir_1
 4. Посмотреть где ты находишься - pwd
 5. Находясь в папке dir_1 создать пустой текстовый файл tf_1.txt - touch tf_1.txt
 6. Находясь в папке dir_1 через команду cat создать текстовый файл tf_2.txt со следующими строками:
- the first 1
- the second 2
- the third 3

cat > tf_2.txt
the first 1
the second 2
the third 3

 7. Зайти в папку inner_dir_1 - cd inner_dir_1
 8. Через cat сделать текстовый файл tf_3.txt c любыми строками - `cat > tf_3.txt
                                                                  qwe
                                                                  asd
                                                                  zxc`

 9. Через cat добавить в текстовый файл tf_3.txt строку “the second 2” - cat >> tf_3.txt
                                                                         the second 2

 10. Через cat добавить в текстовый файл tf_3.txt строку “the sec 2” - cat >> tf_3.txt
                                                                       the sec 2

 11. Через cat добавить в текстовый файл tf_2.txt строку “the sec 3” - cat >> ../tf_2.txt
                                                                       the sec 3

 12. Через cat добавить в текстовый файл tf_3.txt строку “the SeCoNd 2” - cat >> tf_3.txt
                                                                          the SeCoNd 2

 13. Через cat добавить в текстовый файл tf_2.txt строку “the seConD 2” - cat >> ../tf_2.txt
                                                                          the seConD 2
 
 14. Сделать текстовый файл tf_4.txt в котором будет 15 строк. - vim tf_4.txt
                                                                 создать строку и с помощью "14yy" добавить остальные

 15. Сделать текстовый файл tF_5.txt в котором будет 13 строк. - vim tf_5.txt
                                                                 создать строку и с помощью "12yy" добавить остальные
 16. Вывести список всех файлов в папке. - find . -type f
                                           ./tf_3.txt
                                           ./tf_4.txt
                                           ./tF_5.txt

 17. Выйти из папки inner_dir_1 - cd ..
 18. Вывести содержимое файла tf_3.txt в терминал. - cat ./inner_dir_1/tf_3.txt
                                                     qwe
                                                     asd
                                                     zxc
                                                     the second 2
                                                     the sec 3
                                                     the SeCoNd 2

 19. Найти путь к файлу tf_4.txt - 

 20. Очистить файл tf_4.txt от содержимого без удаления самого файла. - > tf_4.txt

 21. Найти путь к файлам у которых есть  “tf” в названии. - find -name "tf*"
                                                            ./inner_dir_1/tf_3.txt
                                                            ./inner_dir_1/tf_4.txt
                                                            ./tf_1.txt
                                                            ./tf_2.txt

 22. Найти путь к файлам у которых есть  “tf” в названии и буквы в любом регистре. - find -iname "tf*"
                                                                                     ./inner_dir_1/tf_3.txt
                                                                                     ./inner_dir_1/tf_4.txt
                                                                                     ./inner_dir_1/tF_5.txt
                                                                                     ./tf_1.txt
                                                                                     ./tf_2.txt
                              
 23. Найти строки в файлах где есть комбинация букв “sec” в текущей папке. - grep sec *
                                                                             grep: inner_dir_1: Is a directory
                                                                             tf_2.txt:the second 2
                                                                             tf_2.txt:the sec 3

 24. Найти строки в файлах где есть комбинация букв “sec” в любом регистре в текущей папке - grep -i sec *
                                                                                             grep: inner_dir_1: Is a directory
                                                                                             tf_2.txt:the second 2
                                                                                             tf_2.txt:the sec 3
                                                                                             tf_2.txt:the seConD 2

 25. Найти строки в файлах где есть только комбинация букв “sec” в текущей папке - grep -w sec *
                                                                                   grep: inner_dir_1: Is a directory
                                                                                   tf_2.txt:the sec 3

 26. Найти строки в файлах где есть только комбинация букв “sec” в любом регистре в текущей папке - grep -w -i sec *
                                                                                                    grep: inner_dir_1: Is a directory
                                                                                                    tf_2.txt:the sec 3

 27. Найти строки в файлах где есть комбинация букв “second” в текущей папке - grep second *
                                                                               grep: inner_dir_1: Is a directory
                                                                               tf_2.txt:the second 2

 28. Найти строки в файлах где есть комбинация букв “second” в любом регистре в текущей папке - grep -i second *
                                                                                                grep: inner_dir_1: Is a directory
                                                                                                tf_2.txt:the second 2
                                                                                                tf_2.txt:the seConD 2

 29. Найти строки в файлах где есть комбинация букв “second” во всех папках ниже уровнем - grep -r second
                                                                                           inner_dir_1/tf_3.txt:the second 2
                                                                                           tf_2.txt:the second 2

 30. Найти только путь и название файла в строках которых есть комбинация букв “second” в текущей папке - grep -l second *
                                                                                                          grep: inner_dir_1: Is a directory
                                                                                                           tf_2.txt

 31. Найти все строки во всех файлах где нет комбинации “second” - grep -r -v second
                                                                   inner_dir_1/tf_3.txt:qwe
                                                                   inner_dir_1/tf_3.txt:asd
                                                                   inner_dir_1/tf_3.txt:zxc
                                                                   inner_dir_1/tf_3.txt:the sec 3
                                                                   inner_dir_1/tf_3.txt:the SeCoNd 2
                                                                   inner_dir_1/tf_4.txt:
                                                                   inner_dir_1/tF_5.txt:ojwd
                                                                   inner_dir_1/tF_5.txt:sgfbv
                                                                   inner_dir_1/tF_5.txt:adfvc
                                                                   inner_dir_1/tF_5.txt:adfv
                                                                   inner_dir_1/tF_5.txt:gfb
                                                                   inner_dir_1/tF_5.txt:edsf
                                                                   inner_dir_1/tF_5.txt:dsfv
                                                                   inner_dir_1/tF_5.txt:dsfvc
                                                                   inner_dir_1/tF_5.txt:fd
                                                                   inner_dir_1/tF_5.txt:jh
                                                                   inner_dir_1/tF_5.txt:thgnb
                                                                   inner_dir_1/tF_5.txt:dfvc
                                                                   inner_dir_1/tF_5.txt:fdvc
                                                                   inner_dir_1/tF_5.txt:
                                                                   tf_2.txt:the first 1
                                                                   tf_2.txt:the third 3
                                                                   tf_2.txt:the sec 3
                                                                   tf_2.txt:the seConD 2
 

 32. Найти только название и путь к файлам где нет комбинации “second” - grep -l -r -v second
                                                                         inner_dir_1/tf_3.txt
                                                                         inner_dir_1/tf_4.txt
                                                                         inner_dir_1/tF_5.txt
                                                                         tf_2.txt

 33. Вывести в терминал 4 последних строк любого текстового файла - tail -n4 inner_dir_1/tF_5.txt
                                                                    jh
                                                                    thgnb
                                                                    dfvc
                                                                    fdvc

 34. Вывести в терминал 4 первые строки любого текстового файла. - head -n4 inner_dir_1/tF_5.txt
                                                                   ojwd
                                                                   sgfbv
                                                                   adfvc
                                                                   adfv
 35. Команда в одну строку. Создать папку и создать текстовый файл с содержимым. - mkdir 0101; cat > 02.txt
 36. Команда в одну строку. Переместить в любую одну папку текстовые файлы у которых в содержимом есть слово “sec” - mv $(grep -wlr sec) ./inner_dir_2
 37. Команда в одну строку. Скопировать в любую одну папку текстовые файлы у которых в содержимом есть слово “sec” - mv $(grep -wlr sec) ./inner_dir_3
 38. Команда в одну строку. Найти все строки c “sec” во всех текстовых файлах, скопировать и вставить эти строки в один новый созданный текстовый файл. - grep -hr sec > tf_6.txt

 39. Команда в одну строку. Удалить текстовые файлы у которых в содержимом есть слово “sec” - rm $(grep -wrl sec)

 40. Просто вывести в терминал строку “Good job!!” - echo "Good job!"