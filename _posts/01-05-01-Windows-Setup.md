---
title: Windows-da Quraşdırma
isChild: true
anchor:  windows_setup
---

## Windows-da Quraşdırma {#windows_setup_title}

İkili faylları [windows.php.net/download][php-downloads] saytından yükləyə bilərsiniz. 
PHP quraşdırıldıqdan sonra onu hər yerdən icra edə bilmək üçün [PATH][windows-path] dəyişənini PHP qovluğunun kökünə 
(php.exe yerləşdiyi yerə) təyin etmək tövsiyə olunur. 

Öyrənmək və lokal tərtibat üçün PHP 5.4+ ilə daxili veb-serverdən istifadə edə bilərsiniz. Belə ki, onu konfiqurasiya 
etmək üçün narahat olmağa ehtiyac yoxdur. 
Tam bir server və MySQL-i özündə birləşdirən universal bir həll istəyirsinizsə, o zaman [Web Platform Installer][wpi], 
[XAMPP][xampp], [EasyPHP][easyphp], [OpenServer][openserver] və [WAMP][wamp] kimi alətlər Windows tərtibat mühitini qurmağa 
və onun sürətli işləməsinə kömək edəcəklər. 
Buna baxmayaraq bu alətlər istehsal mühitindən bir az fərqli olurlar. Buna görə, əgər Windows-da işləyib 
Linux-a yerləşdirirsinizsə mühit fərqlərinə diqqət yetirin.

İstehsal sisteminizi Windows-da işə salmaq lazımdırsa, IIS7 sizə ən stabil və yaxşı performası verəcəkdir. 
PHP-nin konfiqurasiyasını və idarə edilməsini asanlaşdırmaq üçün [phpmanager][phpmanager]-dən (IIS7 üçün GUI plagini) 
istifadə edə bilərsiniz. IIS7 daxili və istifadəyə hazır FastCGI ilə gəlir. Siz sadəcə PHP-ni işləyici olaraq 
konfiqurasiya etməlisiniz. Dəstək və əlavə mənbələr üçün [iis.net-də PHP üçün xüsusi bir sahə][php-iis] var. 


Tərtibat və istehsalat mühitlərinin fərqlənməsi adətən qəribə baqların yaranmasına səbəb ola bilər. 
Əgər Windows-da tərtib edib Linux-a (və ya Windows olmayan istənilən bir sistem) yerləşdirirsinizsə, 
[Virtual Maşın](/#virtualization_title) istifadə etmək haqqında düşünün. 

Chris Tankersley-in [Windows-da PHP ilə tərtibat][windows-tools] zamanı hansı alətlərdən istifadə etdiyi 
haqqında çox faydalı bir məqaləsi var. 

[easyphp]: http://www.easyphp.org/
[phpmanager]: http://phpmanager.codeplex.com/
[openserver]: http://open-server.ru/
[wamp]: http://www.wampserver.com/en/
[php-downloads]: http://windows.php.net/download/
[php-iis]: http://php.iis.net/
[windows-path]: http://www.windows-commandline.com/set-path-command-line/
[windows-tools]: http://ctankersley.com/2016/11/13/developing-on-windows-2016/
[wpi]: https://www.microsoft.com/web/downloads/platform.aspx
[xampp]: http://www.apachefriends.org/en/xampp.html
