---
title: Kod Üslubu Bələdçisi
anchor: code_style_guide
---

# Kod Üslubu Bələdçisi {#code_style_guide_title}

PHP ictimaiyyəti saysız-hesabsız kitabxanalardan, freymvorklərdən və komponentlərdən ibarət olub, böyük və müxtəlifdir. 
PHP proqramçılarının bunlardan bir neçəsini seçərək tək bir layihədə birləşdirməsi adi bir haldır. 
Proqramçıların layihələr üçün müxtəlif kitabxanaları qarışdırıb, onları bir-birinə uyğunlaşdırmasını 
asanlaşdırmaq üçün PHP kodunun ümumi bir kod üslubunda olması vacibdir. 

[Framework Interop Group][fig] bir sıra üslub tövsiyələri təklif və təsdiq etmişdir. 
Bunlardan kod üslubuna aid olanlar [PSR-1][psr1], [PSR-12][psr12] və [PSR-4][psr4]-dür. Bu tövsiyələr sadəcə olaraq 
Drupal, Zend, Symfony, Laravel, CakePHP, phpBB, AWS SDK, FuelPHP, Lithium və s. kimi bir çox layihələrin qəbul etdiyi 
bir sıra qaydalardan ibarətdir. Onları layihələrinizdə istifadə edə və ya öz şəxsi üslubunuzdan istifadə etməyə 
davam edə bilərsiniz. 

İdeal olaraq, yazdığınız PHP kod hər hansı bir tanınmış standarta riayət etməlidir. Bu PSR-lardan hər hansı biri və ya 
PEAR və ya Zend tərəfindən hazırlanmış kodlaşdırma standartlarından biri ola bilər. Bu o deməkdir ki, digər proqramçılar 
kodunuzu asanlıqla oxuya və onunla işləyə, müxtəlif komponentlərdən ibarət tətbiqetmələr isə çox sayda kənar kodlarla 
işləsər belə onlar arasında daha çox uyğunluq əldə edilə bilər. 

* [PSR-1 haqqında oxu][psr1]
* [PSR-12 haqqında oxu][psr12]
* [PSR-4 haqqında oxu][psr4]
* [PEAR Coding Standards haqqında oxu][pear-cs]
* [Symfony Coding Standards haqqında oxu][symfony-cs]

Kodunuzun bu tövsiyələrdən hər hansı biri ilə uyğunluğunu yoxlamaq üçün [PHP_CodeSniffer][phpcs]-dən istifadə edə bilərsiniz. 
[Sublime Text][st-cs] kimi mətn redaktorları isə sizə plaginlər vasitəsilə real zamanda məlumat verəcək. 

Aşağıdakı alətlərdən birini istifadə edərək kod üslubunu avtomatik olaraq düzəldə bilərsiniz: 

- Bunlardan biri, çox yaxşı sınaqdan keçmiş kod bazasına malik olan [PHP Coding Standards Fixer][phpcsfixer]-dir. 
- Bundan başqa, PHP_CodeSniffer-ə daxil olan [PHP Code Beautifier and Fixer][phpcbf] kodunuzda müvafiq düzəlişlər etmək üçün istifadə edilə bilər. 

phpcs-i əmr sətrindən işə sala bilərsiniz: 

    phpcs -sw --standard=PSR1 file.php

O sizə səhvləri və onları necə düzəltmək lazım olduğunu göstərəcək. 
Bu əmri git hook-a əlavə etmək də faydalı ola bilər. 
Bu yolla, seçilmiş standart üzrə pozuntular olan branch-lar, bu pozuntular aradan qaldırılmayana qədər 
repozitoriyaya düşə bilməyəcəklər. 

Əgər sizdə PHP_CodeSniffer varsa kod üslubunda olan problemləri [PHP Code Beautifier and Fixer][phpcbf] ilə 
avtomatik olaraq düzəldə bilərsiniz: 

    phpcbf -w --standard=PSR1 file.php

Digər bir seçim isə [PHP Coding Standards Fixer][phpcsfixer]-dən istifadə etməkdir. 
O sizə problemləri düzətməmişdən öncə kod strukturunda hansı səhvlərin olduğunu göstərəcəkdir. 

    php-cs-fixer fix -v --rules=@PSR1 file.php

Bütün simvollar və kod infrastrukturu üçün ingilis dilinə üstünlük verilir. Şərhlər kod bazasə üzərində işləyən 
hazırkı və gələcək insanlar üçün asanlıqla başa düşülə bilən istənilən dildə yazıla bilər. 

Və sonda, təmiz PHP kodu yazmaq üçün əlavə bir yaxşı mənbə [Clean Code PHP][cleancode]-dir. 

[fig]: https://www.php-fig.org/
[psr1]: https://www.php-fig.org/psr/psr-1/
[psr12]: https://www.php-fig.org/psr/psr-12/
[psr4]: https://www.php-fig.org/psr/psr-4/
[pear-cs]: https://pear.php.net/manual/en/standards.php
[symfony-cs]: https://symfony.com/doc/current/contributing/code/standards.html
[phpcs]: https://pear.php.net/package/PHP_CodeSniffer/
[phpcbf]: https://github.com/squizlabs/PHP_CodeSniffer/wiki/Fixing-Errors-Automatically
[st-cs]: https://github.com/benmatselby/sublime-phpcs
[phpcsfixer]: https://cs.sensiolabs.org/
[cleancode]: https://github.com/jupeter/clean-code-php
