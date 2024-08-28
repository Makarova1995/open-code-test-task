# Open-code-test-task
Провести тестирование программы, выводящей дату время из указанного диапазона.  Написать тестовую документация для данного приложения.  Локализовать и описать найденные баги.

-[Чек-лист](Chec-list.md)



# Чек-лист для проверки  




| Проверка 	| Пример 	| Ожидаемый результат 	|
|---	|---	|---	|
| **Проверка достоверности оформления даты** 	|  	|  	|
|     Ввести дату в   формате DD.MM.YYYY - DD.MM.YYYY    	|     01.01.2020 -   01.01.2021    	|     Система   примет такую дату    	|
|     Ввести дату в   формате DD.MM.YY - DD.MM.YY    	|     01.01.20 -   01.01.21    	|     Система   выдаст ошибку    	|
|     Ввести дату в   формате YYYY.MM.DD - YYYY.MM.DD    	|     2020.01.01 -   2021.01.01    	|     Система   выдаст ошибку    	|
|     Ввести дату в   формате MM.DD.YYYY-MM.DD.YYYY    	|     01.13.2020 -   01.14.2021    	|     Система   выдаст ошибку    	|
|     Ввести дату в   формате dd.mm.YYYY- dd.mm.YYYY    	|     1.1.2020-1.1.2021    	|     Система   выдаст ошибку    	|
|     **Проверка достоверности значений**   	|  	|  	|
|     Ввести дату в формате DD.MM.YYYY - DD.MM.YYYY    	|     01.01.2020 -   01.01.2021    	|     Система   примет такую дату    	|
|     Ввести одинаковую дату в оба   поля    	|     01.01.2020 -   01.01.2020    	|     Система   примет такую дату    	|
|     Ввести   конечную дату раньше начальной даты    	|     01.01.2021 -   01.01.2020    	|     Система   выдаст ошибку    	|
|     Ввести в поле   буквенное дату    	|     Ноль   один.Ноль один.Две тысячи двадцать     -   Ноль один.Ноль один.Две   тысячи двадцать один    	|     Система   выдаст ошибку    	|
|     Ввести одно   валидную дату, во второе не валидную     	|     01.01.2020 -   2021.01.01    	|     Система   выдаст ошибку    	|
|     Ввести в поле   несуществующую дату    	|     32.13.2020 -   31.13.2021    	|     Система   выдаст ошибку    	|
|     Ввести в поле   дату римскими цифрами    	|     I.I.MMXX -   I.I.MMXXI    	|     Система   выдаст ошибку    	|
|     Проверить   нижнюю границу даты     	|     00.00.0000 -   00.00.0000    	|     Система   выдаст ошибку    	|
|     Проверить   верхнюю границу даты     	|     99.99.9999 -   99.99.9999    	|     Система   выдаст ошибку    	|
|     Оставить поле   конечная дата пустым    	|     01.01.2020 -    	|     Система   выдаст ошибку    	|
|     Оставить поле   начальная дата    	|     -01.01.2021    	|     Система   выдаст ошибку    	|
|     Оставить оба   поля пустыми     	|          	|     Система   выдаст ошибку    	|
|     **Проверка на валидность   разделителя**     	|          	|          	|
|     Ввести дату с разделителями (.)    	|     01.01.2020 -   01.01.2021    	|     Система   примет такую дату    	|
|     Ввести дату с   разделителями (/)    	|     01/01/2020 -   01/01/2021    	|     Система   выдаст ошибку     	|
|     Ввести дату с   разделителями (")    	|     01"01"2020   - 01"01"2021    	|     Система   выдаст ошибку     	|
|     Ввести дату с   разделителями (,)    	|     01,01,2020 -   01,01,2021    	|     Система   выдаст ошибку     	|
|     Ввести дату с   разделителями (_)    	|     01_01_2020–01_01_2021    	|     Система   выдаст ошибку    	|
|     Ввести дату с   разделителями (-)    	|     01-01-2020 –   01-01-2021    	|     Система   выдаст ошибку    	|
|     Ввести   значение без разделителя    	|     01012020 -   01012021    	|     Система   выдаст ошибку     	|


# Тест кейсы для проверки



        
####            1.Тест-кейс (Сгенерировать дату и время)
***Предварительные шаги:***
1.	Перейти по ссылке https://disk.yandex.ru/d/gu99s3Gh7zmfTA
2.	Открыть папку CALENDAR_1.1.rar
3.	Скачать файл CALENDAR_1.1.exe 
4.	Открыть файл CALENDAR_1.1.exe на компьютере

   
***Шаги:*** 
1.	В поле «Введите начальную дату в формате d.m.y (01.01.2010)» ввести дату 01.01.2020
2.	Нажмите Enter
3.	В поле «Введите конечную дату в формате d.m.y (01.01.2018)» ввести дату 01.01.2021
4.	Нажмите Enter


***Ожидаемый результат:***
Система сгенерирует рандомно дату и время из данного промежутка.







 ####       2.Тест-кейс (Проверка генирирования даты и времени с невалидными значениями)

***Предварительные шаги:***
1.	Перейти по ссылке https://disk.yandex.ru/d/gu99s3Gh7zmfTA
2.	Открыть папку CALENDAR_1.1.rar
3.	Скачать файл CALENDAR_1.1.exe 
4.	Открыть файл CALENDAR_1.1.exe на компьютере

***Шаги:***
1.	В поле «Введите начальную дату в формате d.m.y (01.01.2010)» ввести дату 1.1.2020
2.	Нажмите Enter
3.	В поле «Введите конечную дату в формате d.m.y (01.01.2018)» ввести дату 1.1.2021
4.	Нажмите Enter

***Ожидаемый результат:***
Система выдаст ошибку «Введенные значения неверные. Попробуйте еще раз»










# Локализация и оформление бага
  
#### Название: Неверный формат даты и времени.

***Предварительные шаги:***
1.	Перейти по ссылке https://disk.yandex.ru/d/gu99s3Gh7zmfTA
2.	Открыть папку CALENDAR_1.1.rar
3.	Скачать файл CALENDAR_1.1.exe 
4.	Открыть файл CALENDAR_1.1.exe на компьютере

***Шаги для воспроизведения:***
1.	В поле «Введите начальную дату в формате d.m.y (01.01.2010)» ввести дату 01.01.2020
2.	Нажмите Enter
3.	В поле «Введите конечную дату в формате d.m.y (01.01.2018)» ввести дату 01.01.2021
4.	Нажмите Enter

***Результат:***
Система сгенерировала рандомно дату и время из данного промежутка в формате YYYY-MM-DD HH:MI:SS.000, неизвестный формат исчисления времени

***Ожидаемый результат:***
Система сгенерирует рандомно дату и время из данного промежутка в формате DD.MM.YYYY HH:MI:SS (общепринятым для страны Россия), в 24-часовой формате исчисления времени.





        

### Название: Система принимает невалидное значение даты.

***Предварительные шаги:***
1.	Перейти по ссылке https://disk.yandex.ru/d/gu99s3Gh7zmfTA
2.	Открыть папку CALENDAR_1.1.rar
3.	Скачать файл CALENDAR_1.1.exe 
4.	Открыть файл CALENDAR_1.1.exe на компьютере

***Шаги для воспроизведения:***
1.	В поле «Введите начальную дату в формате d.m.y (01.01.2010)» ввести дату 1.1.2020
2.	Нажмите Enter
3.	В поле «Введите конечную дату в формате d.m.y (01.01.2018)» ввести дату 1.1.2021
4.	Нажмите Enter

***Результат:***
Система сгенерирует рандомно дату и время из данного промежутка.

***Ожидаемый результат:***
Система выдаст ошибку «Введенные значения неверные. Попробуйте еще раз»


