## DATABASE Q

### commit & rollback
```
Commit komutu, veri tabanına yapılan değişikliklerin kalıcı olmasını sağlar ve transaction’u sona erdirir.
Rollback komutu, veri tabanına yapılan değişiklikleri geri almak için kullanılır, 
böylelikle transaction’u sona erdirir orijinal veriye dönülmesini sağlar.
```
### rollback
```
ROLLBACK ile transaction içinde yapılan işlemlerin geri alınması sağlanır.
```
```
BEGIN TRANSACTION
INSERT INTO uyeler (age) VALUES (3);
INSERT INTO uyeler (age) VALUES (4);
ROLLBACK TRANSACTION
```

### transaction
```
Bir Transaction içindeki her işlem adımının gerçekleşmesi gerekir, adımlardan herhangi birinde dahi 
bir hata meydana gelse ilgili transaction içindeki tüm adımlar, 
diğerleri gerçekleşmiş olsa dahi iptal edilir, eski haline döner.
```
```
BEGIN TRANSACTION
INSERT INTO uyeler (age) VALUES (3);
INSERT INTO uyeler (age) VALUES (4);
COMMIT TRANSACTION
```

### sql index
```
SQL indekslemenin amacı işlenen verinin daha az veri okunarak sorgu sonucunun daha kısa zamanda getirilmesini sağlamaktır. 
Indeksleme kullanarak tablonun tamamını okumaktansa oluşturacağımız indeks key i aracılığı ile okumak istediğimiz kayıda 
ulaşabilmemiz daha hızlı bir şekilde mümkün olacaktır. Bu sayede tamamlanması saatler süren sorgunun uygun indeksler 
kullanılarak saniyeler içinde getirilmesini sağlayabiliriz.
```

### SQL — Normalizasyon
```
https://medium.com/@mehmet1icme/sql-normalizasyon-8835d600df71
```

## SQL
Bir döğr. kaç derse giriyor.
```
select t.name	count(td.id) 
from teacher t
join teacher_dersler td 	on t.id=td.teacherid
join dersler d 			on d.id = td.depertmanid
group by td.id having t.id=3
```
Adı a ile b ile yada s ile başlayan kayıtları listeleyelim.
```
SELECT * FROM musteriler WHERE ad LIKE '[abs]%'
``` 
