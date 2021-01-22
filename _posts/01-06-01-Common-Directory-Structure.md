---
title:   Ümumi Kataloq Strukturu
isChild: true
anchor:  common_directory_structure
---

## Ümumi Kataloq strukturu {#common_directory_structure_title}

Veb üçün proqramlar yazmağa başlayanlar arasında ümumi bir sual "fayllarımı hara qoyum?"-dur. 
Uzun illər ərzində bu sual dəyişilməz olaraq "`DocumentRoot` haradadır?" idi. 
Bu cavab tam olmasa belə, başlamaq üçün əla bir yerdir. 

Təhlükəsizlik səbəbinbən konfiqurasiya faylları saytın ziyarətçilərinə əlçatan olmamalıdır; 
bu səbəbdən, ümumi skriptlər ictimai (public) kataloqda, özəl (private) konfiqurasiyalar 
və məlumatlar isə bu kataloqdan kənarda saxlanılır. 

Bir nəfərin işlədiyi komanda, CMS və ya freymvorkun hər birində standart kataloq strukturundan istifadə olunur. 
Lakin layihəyə tək başlayan biri üçün hansı kataloq strukturundan istifadə etməli olduğunu bilmək çətin ola bilər. 

[Paul M. Jones] PHP aləmində on minlərlə github layihəsinin ümumi təcrübələri üzərində fantastik tədqiqatlar aparmışdır. 
O, bu tədqiqata əsasən standart fayl və kataloq strukturu - [Standard PHP Package Skeleton] hazırlamışdır. 
Bu kataloq strukturunda `DocumentRoot` `public/`-ə işarə etməli, modul testləri `tests/`, [composer] tərəfindən 
quraşdırılmış kənar kitabxanalar isə `vendor/` qovluğunda olmalıdır. 
Digər fayllar və kataloqlar üçün [Standard PHP Package Skeleton]-nə 
riayət etmək layihə iştirakçıları üçün ən yaxşı seçim olacaq. 

[Paul M. Jones]: http://paul-m-jones.com/
[Standard PHP Package Skeleton]: https://github.com/php-pds/skeleton
[Composer]: /#composer_and_packagist
