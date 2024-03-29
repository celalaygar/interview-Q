## REACT GENEL SORULAR 1

### Virtual DOM nedir ?
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
```
```
Virtual DOM (VDOM), bir UI’ın ideal veya “sanal” bir temsilinin bellekte tutulduğu ve 
ReactDOM gibi bir kütüphane tarafından “gerçek” DOM ​​ile senkronize edildiği 
bir programlama konseptidir. Bu sürece uyumlaştırma denir.
```
### SPA nedir ?
```
Single Page Application (SPA), birçok bilginin aynı kaldığı ve bir seferde yalnızca 
birkaç parçanın güncellenmesi gereken tek bir sayfadır.

Single Page Application, sunucudan yeni sayfaların tamamını yüklemek yerine geçerli 
sayfayı dinamik olarak yeniden yazarak kullanıcıyla etkileşime giren bir web uygulaması veya web sitesidir.
```
Alıntı yapılan sayfa
```
https://www.argenova.com.tr/single-page-application-spa-nedir
```
### Base component nedir ?
```

```
### UseRef, UseMemo ve UseCallBack nedir ?
useRef
```
useRef bir component içerisinde component'in tekrar render olmasını tetiklemeden “mutable” değişken tutmamızı sağlayan yapıdır.
```
useMemo
```
useMemo, gereksiz render işleminin önüne geçmek sebebi ile değişmeyen state'lere sahip sayfaların render işlemini engeller. 
React ile hazırladığımız projede oluşturduğumuz state'leri farklı componentlere aktarmamız gerekebilir. 
Bu durumda state değişmese bile o componentlerin de render edilme sorunu ile karşılaşırız.
```
UseCallBack
```
useCallback parametre olarak bir fonksiyon ve dependency array alıyor ve dependency array içerisindeki değerler 
değişmediği sürece parametre olarak aldığı fonksiyonu return ediyor.
```

### React Element ve Component arasındaki fark nedir ?
Alıntıdır : https://kodsozluk.com/bakigul/react-element-ve-component-arasindaki-fark-nedir
```
Bir element, DOM düğümleri veya diğer bileşenler açısından ekranda ne görünmesini istediğinizi açıklayan düz bir nesnedir. 
Elementler, sahnelerinde başka Elementler içerebilir. Bir React elementi oluşturmak ucuzdur. 
Bir element oluşturulduktan sonra asla mutasyona uğramaz.

const element = React.createElement('div', { id: 'login-btn' }, 'Login');
```
Yukarıdaki React.createElement() işlevi aşağıdaki nesneyi döndürür:
```
{
  type: 'div',
  props: {
    children: 'Login',
    id: 'login-btn'
  }
}
```
Ve son olarak, ReactDOM.render() kullanarak DOM'a dönüştürülür:
```
Oysa bir component birkaç farklı şekilde bildirilebilir. render() yöntemiyle bir sınıf olabilir. 
Alternatif olarak, basit durumlarda bir fonksiyon olarak tanımlanabilir. Her iki durumda da girdi olarak props alır ve 
çıktı olarak bir JSX ağacı döndürür:

const Button = ({ onLogin }) => (
  <div id={'login-btn'} onClick={onLogin}>
    Login
  </div>
);
```
Ardından JSX, bir React.createElement() işlev ağacına aktarılır:
```
const Button = ({ onLogin }) =>
  React.createElement('div', { id: 'login-btn', onClick: onLogin }, 'Login');
```

### JS ile JSX arasındaki fark nedir ? 
```
.js dosyaları genel JavaScript kodlarını içerirken, . jsx dosyaları React veya benzeri UI kütüphaneleriyle kullanılan,
JavaScript'e HTML benzeri bir sözdizimi ekleyen dosyalardır.

JSX, JavaScript için XML benzeri bir sözdizimi uzantısıdır. Başka bir deyişle, HTML'yi JavaScript ile birleştirir! 
Bu çok büyük bir avantaj çünkü DOM'umuzun nasıl görüneceğini görselleştirmek daha kolay.
```
```
// JavaScript example
let element = React.createElement('h1', {}, 'This is JavaScript')
ReactDOM.render(element, document.getElementById('root'));

// JSX equivalent
let element = <h1>This is JSX</h1>
ReactDOM.render(element, document.getElementById('root'))
```

