Pinler
======

Bu mikro site [Raspberry Pi Türkiye Topluluğu](http://raspi.gen.tr) için hazırlanmıştır. Online haline [bu adresten](http://pinler.raspi.gen.tr) erişebilirsiniz.

Bu repo [Gadgetoid/Pinout](https://github.com/Gadgetoid/Pinout)'un Türkçe çevirisi olmakla birlikte sizler aracılığı ile gelen isteklerle daha da şekillenmeyi, örnekleri zenginleşmeyi amaçlıyorum.

Kurulum
======
Bu dosyaların düzgün kurulduktan sonra (virtual)host'unuzda gelen her isteği `pinout.html`'e kırmalısınız. Bunun için Apache kullanıyorsanız ve `mod_rewrite` açıksa şunun gibi bir `.htaccess` dosyası oluşturabilirsiniz:

```
RewriteEngine On
RewriteCond %{REQUEST_URI}  !(\.png|\.css|\.js)$
RewriteRule (.*)  pinout.html [QSA,L]
```

Nginx'de de şuna benzer bir özel ayar iş görecektir:


```
location ~ (\.png|\.css|\.js)$ {
}
rewrite ^(.*)$ /pinout.html;
```

Destek
======
Bu sayfa altından bu projeye destek olabilirsiniz. Bu repoyu forklayıp, kendinizce geliştirip push request ile geliştirmenizi bana sunabilir, issues kısmında konuları tartışabilirsiniz. Raspberry Pi hakkındaki diğer tüm sorular için [Raspberry Pi Türkiye Forumları](http://forum.raspi.gen.tr)'na başvurun.

Lisans
======
Bu mikrosite Creative Commons 3.0 Attribution lisansı ile lisanslanmıştır.

https://creativecommons.org/licenses/by/3.0/

*Orijinal kaynağa alıntı yaptığınız sürece* ticari veya ticari olmayan işlerinizde kullanabilir, projelerinize bu repodaki kodları dahil edebilirsiniz.

Kaynak kodunda bulunan Google Code Prettify kütüphanesi de Apache 2.0 lisansına sahiptir.

http://www.apache.org/licenses/LICENSE-2.0
