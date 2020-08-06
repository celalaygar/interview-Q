## JWT Q

#### jwt
```
üretilen token Base64 ile kodlanmış 3 ana kısımdan oluşmaktadır. Header(Başlık), Payload(Veri), Signature(İmza) 
```
Header(Başlık)
```
{
  "alg": "HS256",   // imzalamada kullanılacak algoritma
  "typ": "JWT"      //token tipi
}

```
Payload(Veri)
```

```
Signature(İmza) 
```
Bu kısmın oluşturulabilmesi için header, payload ve gizli anahtar(secret) gereklidir.
HMACSHA256(
  base64UrlEncode(header) + "." +
  base64UrlEncode(payload),
  your-256-bit-secret
)

```

#### spring cloud
```

```
####
```

```
####
```

```
