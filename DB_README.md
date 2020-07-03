## DATABASE Q
- binary search
```
```
- commit
```
```
- rollback
```
ROLLBACK ile transaction içinde yapılan işlemlerin geri alınması sağlanır.

BEGIN TRANSACTION
INSERT INTO uyeler (age) VALUES (3);
INSERT INTO uyeler (age) VALUES (4);
ROLLBACK TRANSACTION
```
- transaction
```
Bir Transaction içindeki her işlem adımının gerçekleşmesi gerekir, adımlardan herhangi birinde dahi 
bir hata meydana gelse ilgili transaction içindeki tüm adımlar, 
diğerleri gerçekleşmiş olsa dahi iptal edilir, eski haline döner.

BEGIN TRANSACTION
INSERT INTO uyeler (age) VALUES (3);
INSERT INTO uyeler (age) VALUES (4);
COMMIT TRANSACTION
```
- sql index
```
SQL indekslemenin amacı işlenen verinin daha az veri okunarak sorgu sonucunun daha kısa zamanda getirilmesini sağlamaktır. 
Indeksleme kullanarak tablonun tamamını okumaktansa oluşturacağımız indeks key i aracılığı ile okumak istediğimiz kayıda 
ulaşabilmemiz daha hızlı bir şekilde mümkün olacaktır. Bu sayede tamamlanması saatler süren sorgunun uygun indeksler 
kullanılarak saniyeler içinde getirilmesini sağlayabiliriz.

```
- Observer (Gözlemci) Pattern
```
```
