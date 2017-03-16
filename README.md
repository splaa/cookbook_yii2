
# mysql #

mysql -г root -p
SHOW DATABASES ;
create database yii_rusakov character set utf8 collate utf8_general_ci;
SHOW DATABASES ;






# cookbook_yii2 #


cookbook_yii2" >> README.md
git init
git add README.md
git commit -m "first commit"
git remote add origin https://github.com/splaa/cookbook_yii2.git
git push -u origin master
…or push an existing repository from the command line


git remote add origin https://github.com/splaa/cookbook_yii2.git
git push -u origin master

копируем все содержимоетекущей папки на уровень выше ( mv * ../ )

создаём символьную ссылку на папку web( sudo ln -s test/web test.dev ) для Mac OS

создаём файл echo "# cookbook_yii2" >> README.md



Заметил что время выводится в записях с разницей на 1 час от того, которое указываю при создании записи. Эта проблема связана с временной зоной. И надо её прописать в конфиге. Добавил в массив components в formatter параметр 'timeZone'

'formatter' => [
               'class' => 'yii\i18n\Formatter',
               'defaultTimeZone' => 'Europe/Kiev',
               'timeZone' => 'GMT+2',
               'dateFormat' => 'd MMMM yyyy',
               'datetimeFormat' => 'd-M-Y H:i:s',
               'timeFormat' => 'H:i:s', 
        ],
Без 'timeZone' => 'GMT+3', время опережало установленное на 1 час.



https://habrahabr.ru/post/323416/    - Yii2, быстрый старт. Самый простой сайт на Yii2 со статическими страницами без использования БД 
