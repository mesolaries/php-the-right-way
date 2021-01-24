---
title: Adlar Məkanı
isChild: true
anchor:  namespaces
---

## Adlar Məkanı {#namespaces_title}

Yuxarıda qeyd edildiyi kimi, PHP ictimaiyyəti saysız-hesabsız kod yazan çoxlu proqramçılardan ibarətdir. 
Bu o deməkdir ki, bir kitabxanın PHP kodu başqa bir kitabxananın kodu ilə eyni klas adına malik ola bilər. 
Hər iki kitabxana eyni adlar məkanında istifadə edildikdə, onlar toqquşur və problem yaradır. 

_Adlar məkanı (namespaces)_ bu problemi həll edir. PHP dokumentasiyasında qeyd edildiyi kimi, adlar məkanı əməliyyat 
sistemində _adlar məkanı_ faylları olan qovluqlarla müqayisə edilə bilərlər; iki eyni adlı fayl müxtəlif qovluqlarda 
yerləşdirilə bilərlər. Eyni şəkildə, eyni adlı iki PHP klası müxtəlif PHP adlar məkanında mövcud ola bilərlər. 
Bu qədər sadə. 

Kodunuzu adlar məkanında yerləşdirməyiniz digər kitabxanalarla toqquşma qorxusu olmadan başqa proqramçılar tərəfindən 
istifadə edilə bilməsi üçün vacibdir. 

Adlar məkanından istifadə etməyin məsləhətli bir yolu [PSR-4][psr4]-də qeyd olunub. O, qoş-və-oyna (plug-and-play) 
kodunun mümkün olması üçün standart fayl, klas və adlar məkanı konvensiyasını təqdim etməyi hədəfləyir. 

2014-cü ilin oktyabrında PHP-FIG əvvəlki avtomatik yükləmə (autoloading) standartını ləğv etdi: [PSR-0][psr0]. 
Həm PSR-0, həm də PSR-4 hələ də istifadəyə tam yaralıdır. Sonuncusu PHP 5.3 tələb edir, yalnız bir çox PHP 5.2 layihələri 
PSR-0-ı tətbiq edir. 

Yeni bir tətbiqetmə və ya paket üçün avtomatik yükləmə standartından istifadə edəcəksinizsə PSR-4-ə nəzər yetirin. 

* [Adlar məkanı haqqında oxu][namespaces]
* [PSR-0 haqqında oxu][psr0]
* [PSR-4 haqqında oxu][psr4]


[namespaces]: https://secure.php.net/language.namespaces
[psr0]: https://www.php-fig.org/psr/psr-0/
[psr4]: https://www.php-fig.org/psr/psr-4/
