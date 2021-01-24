---
title: Proqramlaşdırma Paradiqmaları
isChild: true
anchor:  programming_paradigms
---

## Proqramlaşdırma Paradiqmaları {#programming_paradigms_title}

PHP müxtəlif proqramlaşdırma texnikalarını dəstəkləyən çevik, dinamik bir dildir. O, illər ərzində PHP 5.0-da (2004) 
davamlı bir obyekt yönümlü model, PHP 5.3-də (2009) anonim funksiyalar və adlar məkanı (namespaces) və PHP 5.4-də (2012) 
treytlər əlavə etməklə dramatik bir şəkildə inkişaf etmişdir. 

### Obyekt yönümlü Proqramlaşdırma

PHP klasları, mücərrəd klasları, interfeysləri, varisliyi, konstruktorları, klonlamanı, istisnaları və digərlərini 
dəstəkləyən tam bir obyekt yönümlü proqramlaşdırma imkanlarına malikdir. 

* [Obyekt yönümlü PHP haqqında oxu][oop]
* [Treytlər haqqında oxu][traits]

### Funksional Proqramlaşdırma

PHP birinci dərəcəli funksiyaları dəstəkləyir. Bu o deməkdir ki, funksiya hər hansı bir dəyişənə təyin edilə bilər. 
Həm istifadəçi tərəfindən təyin edilmiş, həm də daxili funksiyalar dəyişənlə istinad oluna və dinamik olaraq çağrıla bilərlər. 
Funksiyalar digər funksiyalara parametr kimi ötürülə bilərlər (buna _Yüksək səviyyəli funksiyalar 
(Higher-order Functions)_ deyilir). Həmçinin funksiyalar digər funksiyaları qaytara bilərlər. 

Bir funksiyanın öz özünü çağırması imkanı olan rekursiya dil tərəfindən dəstəklənir. Lakin PHP kodlarının əksəriyyəti 
iterasiyaya fokuslanmışdır. 

PHP 5.3-dən (2009) bəri yeni anonim funksiyalar (qapanma dəstəyi ilə) mövcuddur. 

PHP 5.4-də anonim funksiyalarla bir-birini əvəz edəcək şəkildə istifadə oluna bilməsi üçün qapanmaları obyektlərin əhatə 
dairəsinə bağlamaq imkanı əlavə edilmiş, həmçinin, çağrıla bilən obyektlərin dəstəyi yaxşılaşdırılmışdır. 

* [PHP-də Funksional Proqramlaşdırma](/pages/Functional-Programming.html)-da oxumağa davam et
* [Anonim Funksiyalar haqqında oxu][anonymous-functions]
* [Qapanma Klası (Closure Class) haqqında oxu][closure-class]
* [Daha çox detallar Closures RFC-də][closures-rfc]
* [Çağrıla bilənlər (Callables) haqqında oxu][callables]
* [`call_user_func_array()` vasitəsilə funksiyaları dinamik olaraq çağırmaq haqqında oxu][call-user-func-array]

### Meta Proqramlaşdırma

PHP Reflection API və Magic Methods (Sehrli Metodlar) kimi mexanizmlər vasitəsilə müxtəlif meta-proqramlaşdırma formalarını dəstəkləyir. 

Proqramçıların klasın davranışlarına birbaşa daxil olmalarına imkan yaradan `__get()`, `__set()`, `__clone()`, 
`__toString()`, `__invoke()` və s. kimi Sehrli Metodlar mövcuddur. Ruby proqramçıları tez-tez PHP-də `method_missing`-in 
çatışmadığını deyirlər. Lakin bu `__call()` və `__callStatic()` metodları kimi mövcuddur. 

* [Sehrli Metodlar haqqında oxu][magic-methods]
* [Reflection (Refleksiya) haqqında oxu][reflection]
* [Overloading (Həddindən artıq yüklənmə) haqqında oxu][overloading]


[oop]: https://secure.php.net/language.oop5
[traits]: https://secure.php.net/language.oop5.traits
[anonymous-functions]: https://secure.php.net/functions.anonymous
[closure-class]: https://secure.php.net/class.closure
[closures-rfc]: https://wiki.php.net/rfc/closures
[callables]: https://secure.php.net/language.types.callable
[call-user-func-array]: https://secure.php.net/function.call-user-func-array
[magic-methods]: https://secure.php.net/language.oop5.magic
[reflection]: https://secure.php.net/intro.reflection
[overloading]: https://secure.php.net/language.oop5.overloading

