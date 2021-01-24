---
title: Əmr Sətri İnterfeysi
isChild: true
anchor:  command_line_interface
---

## Əmr Sətri İnterfeysi {#command_line_interface_title}

PHP-nin veb tətbiqetmələr yazmaq üçün yaradılmasına baxmayaraq, o, əmr sətri interfeysi (Command Line Interface - CLI) 
proqramlarının yazılması üçün də faydalıdır. Əmr sətri PHP proqramları test, yerləşdirmə və tətbiqetmənin idarə olunması 
kimi ümumi tapşırıqları avtomatlaşdırmağa kömək edə bilər. 

CLI PHP proqramları güclüdür. Çünki siz proqramınızın kodunu onun üçün veb-interfeys 
yaratmadan və qorumadan birbaşa istifadə edə bilərsiniz. Sadəcə olaraq CLI PHP skriptlərinizi 
ümumi kök direktoriyasına **yerləşdirmədiyinizdən** əmin olun! 

PHP-ni əmr sətrinizdən işə salmağa çalışın: 

{% highlight console %}
> php -i
{% endhighlight %}

`-i` seçimi PHP konfiqurasiyanızı eynilə [`phpinfo()`][phpinfo] funksiyası kimi çap edəcəkdir. 

`-a` seçimi ruby IRB-nin və ya python-nun interaktiv örtüyünə bənzər bir interaktiv örtük təmin edir. Bir sıra digər 
faydalı [əmr sətri seçimləri][cli-options] də var. 

Gəlin sadə bir "Hello, $name" CLI proqramı yazaq. Sınamaq üçün aşağıda göstərildiyi kimi `hello.php` 
adlı bir fayl yaradın. 

{% highlight php %}
<?php
if ($argc !== 2) {
    echo "Usage: php hello.php <name>.\n";
    exit(1);
}
$name = $argv[1];
echo "Hello, $name\n";
{% endhighlight %}

PHP skriptinizin işlədiyi arqumentlərə əsasən iki xüsusi dəyişən qurur. [`$argc`][argc] arqument *sayını* ehtiva edən 
tam ədəd (integer) dəyişəni, [`$argv`][argv] isə hər bir arqumentin *dəyərini* ehtiva edən bir massiv (array) dəyişənidir. 
İlk arqument həmişə PHP skript faylınızın adıdır. İndiki halda `hello.php`. 

`exit()` ifadəsi əmrinizin uğursuz sonlandığını örtüyə bildirmək üçün sıfır olmayan bir rəqəmlə istifadə olunur. 
Tez-tez istifadə olunan çıxış kodlarına [burada][exit-codes] baxmaq olar. 

Əmr sətrindən yuxarıdakı skriptimizi çalışdırmaq üçün:

{% highlight console %}
> php hello.php
Usage: php hello.php <name>
> php hello.php world
Hello, world
{% endhighlight %}


 * [PHP-ni əmr sətrindən işə salmaq haqqında öyrən][php-cli]

[phpinfo]: https://secure.php.net/function.phpinfo
[cli-options]: https://secure.php.net/features.commandline.options
[argc]: https://secure.php.net/reserved.variables.argc
[argv]: https://secure.php.net/reserved.variables.argv
[exit-codes]: https://www.gsp.com/cgi-bin/man.cgi?section=3&amp;topic=sysexits
[php-cli]: https://secure.php.net/features.commandline.options
