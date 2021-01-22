---
title: Mac-da Quraşdırma
isChild: true
anchor:  mac_setup
---

## Mac-da Quraşdırma {#mac_setup_title}

macOS PHP ilə hazır gəlir. Lakin normal halda ən son stabil versiyadan bir qədər geri olur. 
Ən son PHP versiyasını macOS-a yükləməyin bir neçə yolu var. 

### PHP-ni Homebrew ilə quraşdırmaq

[Homebrew], macOS üçün PHP və müxtəlif genişləndirmələri asanlıqla quraşdırmağınıza kömək edən bir paket meneceridir. 
Homebrew-nun əsas repozitoriyası PHP 5.6, 7.0, 7.1, 7.2, 7.3, 7.4 və PHP 8.0 üçün "düsturlar" təqdim edir. 
Ən son versiyanı bu əmrlə quraşdırın: 

```
brew install php@8.0
```

Homebrew PHP versiyaları arasında `PATH` dəyişəninizi redaktə etməklə keçid edə bilərsiniz. 
Alternativ olaraq PHP versiyalarını avtomatik dəyişmək üçün 
[brew-php-switcher][brew-php-switcher]-dən istifadə edə bilərsiniz. 

### PHP-ni MacPorts ilə quraşdırmaq

The [MacPorts] Project - OS X əməliyyat sistemində əmr sətri, X11 və ya Aqua əsaslı 
açıq mənbəli proqramların kompilyasiyası, quraşdırılması və təkmilləşdirilməsi üçün 
istifadəsi asan bir sistem hazırlamaq üçün açıq mənbə ictimaiyyətinin bir təşəbbüsüdür. 

MacPorts əvvəldən kompilyasiya edilmiş ikili faylları dəstəkləyir. 
Beləliklə, mənbə tarball fayllarından bütün asılılıqları yenidən kompilyasiya etməyə ehiyac qalmır. 
Əgər sisteminizdə heç bir paket quraşdırılmayıbsa, bu sizin həyatınızı xilas edəcək. 

Bu baxımdan siz `php54`, `php55`, `php56`, `php70`, `php71`, `php72`, `php73`, `php74` və ya `php80`-i `port install` 
əmrindən istifadə edərək quraşdıra bilərsiniz. Məsələn: 

    sudo port install php74
    sudo port install php80

Aktiv PHP-yə keçmək üçün isə `select` əmrini işə sala bilərsiniz: 

    sudo port select --set php php80

### PHP-ni phpbrew ilə quraşdırmaq

[phpbrew] bir neçə PHP versiyasını quraşdırmaq və idarə etmək üçün bir alətdir. İki fərqli tətbiq/layihə üçün fərqli
PHP versiyaları lazımdırsa və virtual maşınlardan istifadə etmirsinizsə, bu, həqiqətən də faydalı ola bilər. 

### PHP-ni Liip ikili quraşdırıcısı ilə quraşdırın

Digər bir populyar seçim, 5.3-dən 7.3-dək versiyalar üçün bir sətirdə quraşdırma üsulları təqdim edən [php-osx.liip.ch]-dır.
O, PHP-ni Apple tərəfindən quraşdırılmış PHP ikili fayllarının üzərinə deyil, ayrı bir yerə quraşdırır (/usr/local/php5). 

### Mənbədən kompilyasiya edin

Qurduğunuz PHP versiyasını idarə etməyə imkan verən başqa bir seçim - [özünüz kompilyasiya edin][mac-compile].
Bu halda [Xcode][xcode-gcc-substitution] -un və ya Apple-ın Mac Developer Center-dən yüklənə bilən 
əvəzedici ["Command Line Tools for XCode"]-un quraşdırıldığından əmin olun. 

### Universal Quraşdırıcılar

Yuxarıda sadalanan həllər əsasən PHP-nin özünü idarə edir və [Apache][apache], [Nginx][nginx] və ya 
SQL server kimi şeyləri təmin etmir. 
[MAMP][mamp-downloads] və [XAMPP][xampp] kimi universal həllər bu və digər proqram təminatlarını 
sizin üçün quraşdıracaq və bir-biri ilə əlaqələndirəcək. 
Lakin quraşdırma asanlığı rahatlığın itirilməsi hesabına başa gəlir. 

[Homebrew]: https://brew.sh/
[Homebrew PHP]: https://github.com/Homebrew/homebrew-php#installation
[MacPorts]: https://www.macports.org/install.php
[phpbrew]: https://github.com/phpbrew/phpbrew
[php-osx.liip.ch]: https://php-osx.liip.ch/
[mac-compile]: https://secure.php.net/install.macosx.compile
[xcode-gcc-substitution]: https://github.com/kennethreitz/osx-gcc-installer
["Command Line Tools for XCode"]: https://developer.apple.com/downloads
[apache]: https://httpd.apache.org/
[nginx]: https://www.nginx.com/
[mamp-downloads]: https://www.mamp.info/en/downloads/
[xampp]: https://www.apachefriends.org/index.html
[brew-php-switcher]: https://github.com/philcook/brew-php-switcher
