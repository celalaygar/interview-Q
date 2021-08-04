## JAVASCRIPT Q
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


