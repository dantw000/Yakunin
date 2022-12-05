1. Открыть терминал
2. Выполнить обновление с помощью команд update и upgrate. Ждем когда выполнится.
![Image](https://user-images.githubusercontent.com/113884916/205575293-8410e78e-90b7-4886-998a-c74570326f7c.png)
3. Распаковка пакетов с помощью кода:
sudo apt-get install build-essential libreadline-dev zlib1g-dev flex bison libxml2-dev libxslt-dev libssl-dev
libxml2-утилиты xsltproc ccache
![Image](https://user-images.githubusercontent.com/113884916/205577215-fb23c5a3-37c8-4234-999c-8bca87276ecb.png)
4. Скачивание postgresql, распаковка и установка
curl -O https://ftp.postgresql.org/pub/source/v11.5/postgresql-11.5.tar.gz
gunzip postgresql-11.5.tar.gz
tar -xvf postgresql-11.5.tar
![Image](https://user-images.githubusercontent.com/113884916/205635116-2b88cc3d-72a9-44e2-ab49-c8326bf9dcdc.png)
Переходим в дирекорию и начинаем конфигурацию
cd postgresql-11.5
./configure --prefix=/local/apps/postgresql/pgsql115/ --with-pgport=5432
![Image](https://user-images.githubusercontent.com/113884916/205636734-34837013-083b-4f54-9413-a2f8763d6b85.png)
![Image](https://user-images.githubusercontent.com/113884916/205637786-210d6ffa-a126-4806-b490-88a1f5aca107.png)
НАСТРОЙКА POSTGRESQL В UBUNTU
1.После установки переключиться на пользователя postgres с помощью команды:
sudo -i -u postgres

После переключения на пользователя postgres, войти в консоль управления:
psql
![Image](https://user-images.githubusercontent.com/113884916/205638890-d8b08cde-793d-4844-8bdf-af89bb387e8e.png)
Посмотреть информацию о соединении:
\conninfo
![Image](https://user-images.githubusercontent.com/113884916/205638997-407228c6-9e88-4dd1-9535-bcd3bf3bc859.png)
Чтобы выйти:
\q

Чтобы вернуться в свою директорию:
выход
   УСТАНОВКА PGADMIN4 В UBUNTU
1. ПРОВЕРКА СИСТЕМНЫХ ТРЕБОВАНИЙ
Для того чтобы проверить состояние службы Postgresql выполните такую команду:

systemctl status postgresql
В поле status должно быть слово ative, выделенное зеленым цветом.
![Image](https://user-images.githubusercontent.com/113884916/205639544-71f4327c-6bd7-4846-bffd-ac027d8d877a.png)
2. ДОБАВЛЕНИЕ РЕПОЗИТОРИЯ

Сначала установить публичный ключ при помощи команды:

sudo wget https://www.pgadmin.org/static/packages_pgadmin_org.pub | sudo apt-ключ добавить packages_pgadmin_org.pub
После этого добавить запись о репозотории pgAdmin в файл /etc/apt/sources.list.d/pgadmin4.list:

эхо "деб https://ftp.postgresql.org/pub/pgadmin/pgadmin4/apt /$(lsb_release -cs) pgadmin4 main" > sudo tee >>/etc/apt/sources.list.d/pgadmin4.list
Обновить:
sudo apt update

3. УСТАНОВКА PGADMIN4
Чтобы начать установку pgAdmin4:

sudo apt устанавливает pgadmin4
![Image](https://user-images.githubusercontent.com/113884916/205640705-8383414f-a0be-4529-a00f-e18620b94a80.png)
4. НАСТРОЙКА PGADMIN4
Чтобы запустить её откройте главное меню и введите в строке поиска pgAdmin, а затем кликните по иконке программы.





