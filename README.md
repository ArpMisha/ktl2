# ktl2
"корпоративный каталог" создан для хранения информации по сетям, информационным системам и активам организации
с возможностью ознакомится с ней в удобном формате в браузере.
Использую:
- феймворк flask (python)
- bootstrap 4 (html/css)
- немного js
- база данных - postresql
- прокси - nginx
- docker
- ansible

для того чтобы развенуть "корпоративный каталог" на удаленном сервере необходимо следующее:
1) на сервере, где разворачивается приложение:
  git clone https://github.com/ArpMisha/ktl2.git
запомнить ip-адрес
2) на ПК с которого будем запускать ansible:
  git clone https://github.com/ArpMisha/ktl2.git
  заменить в файле cluster.ini ip-адрес на ip сервера из пункта 1
3) ansible-playbook -i cluster.ini all.yml -kK # эта команда запустит конфиг, не забудьте ввести пароль для shh и пароль администратора 
