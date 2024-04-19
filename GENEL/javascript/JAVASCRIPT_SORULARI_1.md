## JAVASCRIPT_SORULARI_1
### Virtual DOM nedir
```
Gerçek DOM’a karşılık gelen sanal bir DOM nesnesidir, yani render edilen DOM’un bir kopyasıdır. 
React her state değişikliğinde render edilen gerçek DOM’u bütünüyle tekrar oluşturmak yerine, 
state değişikliğini Virtual DOM’a yansıtmaktadır. Bu sayede gerçek DOM ile ve 
yeni sanal(virtual) DOM arasındaki farklılıkları tespit ederek, 
gerçek DOM’da yapılacak değişikleri hesaplar ve tek seferde 
sadece gerçek DOM’da değişen elemanları yeniden render eder. 
Bu şekilde state her değiştiğinde ana DOM’un tüm elemanlarıyla yeniden oluşturulması 
maliyetinden korunulmuş ve azami performans iyileştirmesi sağlanmaktadır. 
Gerçek DOM render edildiğinde, virtual DOM ile eşittir. 


Virtual DOM (VDOM), bir UI’ın ideal veya “sanal” bir temsilinin bellekte tutulduğu ve 
ReactDOM gibi bir kütüphane tarafından “gerçek” DOM ​​ile senkronize edildiği 
bir programlama konseptidir. Bu sürece uyumlaştırma denir.
```
### null ve undefined anahtar kelimeler arasında fark var mı?
```
JavaScript’te undefined, bir değişkenin bildirildiği ancak henüz bir değer atanmamış olduğu anlamına gelir.

null ise bir atama değeridir, değişkene değersiz bir gösterim olarak atanabilir. typeof null bize nesne döndürür.
```
### Object Oriented JavaScript
```
```
### Prototype, prototype based inheritance
```
```
### Debouncing
```
```
### Throttling
```
```
### Calbacks 
```
```
### Promises 
- Promise istenilen görevi yerine getirdiğinde değeri değişmez (immutable)
- Sadece bir kere başarıya (resolved) ulaşır, veya başarısız (rejected) olur.
- Öngörülemeyen hatalar otomatik olarak Promise’i başarısız (rejected) sonuca götürür. Bu da hataları kontrol etme noktasında faydalıdır.
- Yapısı gereği, gelecekteki bir değerin göstergesi olduğundan daha güvenilirdir.
```
const sozVerdik = new Promise(function(resolve, reject){
  if (herseyYolunda) {
    resolve('İşlem tamam!');
  } else {
    reject('Bir sıkıntı var...');
  }
})

sozVerdik.then(function(cevap){
  console.log(cevap) // 'İşlem tamam!' yazısını basar
}).catch(function(hata){
  console.log(hata) // 'Bir sıkıntı var...' yazısını basar
})
```

```
asenkronIslem()
  .then(sonuc => {
    return baskaAsenkronIslem(sonuc);
  })
  .then(zincirSonuc => {
    return zincirSonuc.json();
  })
  .catch(hata => {
    console.log(hata);
  });
```

### Observables
```
```
### Event Loop 
```
```


