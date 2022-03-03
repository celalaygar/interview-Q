## REACT Q
### React Element ve Component arasındaki fark nedir?
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
JSX , geliştiricilerin mantığı kontrol etmek için JS ile karıştırılamayan HTML ve XML'ye benzeyen 
sözdizimini kullanarak görünümler yazmasına izin veren bir JavaScript uzantısıdır.

```
```
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





