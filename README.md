
## Task 28012019: ##

Инсталиране на WordPress 5.0.3 върху CentOS 7 сървър, със следните изисквания:
- PHP 7.2 работещо като PHP-FPM
- Nginx 1.15.
- MariaDB 10.3, която не слуша на socket, а на IP адрес 127.0.0.1
- Без SSL.

__За целта използваме базов deploy scirpt :__
[STACK](https://github.com/rusk0/Documentation/blob/master/28012019)


## Task 2801201901: ##
Отделяне на цялото статично съдържание на сайта към отделен под домейн, например cdn.failovete.com
 Cross-Origin Resource Sharing (CORS).
Lets Encrypt сертификат. 
 да няма уеб сървър на http порт, а само на https порта.
лимит за не повече от 100 едновременни отворени ресурса т.е. картинки, css, js и други от един IP адрес.

**За целта e необходимо да позволим зареждането на ресурси от друг източник, както и да конфигурираме надеждно синхронизиране между двата сървъра. [CORS+SYNC](https://github.com/rusk0/Documentation/blob/master/2801201902) - Тук можем да намерим информация за Cross Origin хедърите, както и как ще става синхронизацията между основния и static сървъра. ** създаваме proxy_pass (CORS не е необходим, тъй като браузъра не знае за static сървъра) или rewrite(CORS е необходим, тъй като браузъра знае за втория сървър) директива за статичните файлове.**

Стъпките за залагане на сертификата, конфигуриране на автоматично подновяване и "rate limit" към nginx :
[LE+Nginx conf](https://github.com/rusk0/Documentation/blob/master/2801201901) **




## Task 2801201902: ##
Инсталиране на git server, проект WordPress.

**Конфигурацията е извършена по следния начин :**
[GitWeb](https://github.com/rusk0/Documentation/blob/master/2801201903-easy)


## Task 2801201903: ##
https://github.com/rusk0/Documentation



