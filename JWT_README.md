## JWT Q

### JWT
```
üretilen token Base64 ile kodlanmış 3 ana kısımdan oluşmaktadır. Header(Başlık), Payload(Veri), Signature(İmza) 
```
#### Header(Başlık)
```
{
  "alg": "HS256",   // imzalamada kullanılacak algoritma
  "typ": "JWT"      //token tipi
}

```
#### Payload(Veri)

Bu kısım ‘claim’leri içerir. Bu kısımda tutulan veriler ile token istemci ve sunucu arasında eşsiz olur. Bu tutulan claim bilgileri de bu eşsizliği sağlar. Bu kısımda 3 tip claim bulunmaktadır.
- Registered(Kayıtlı) claims: JWT tarafından önceden reserve edilmiş 3 harf uzunluğunda claimlerdir. Yani bu ayarlanmış belli claim isimlerini diğer claimlerde kullanamazsınız. Bu bilgilerin kullanılması zorunlu değildir ama önerilmektedir. Bu claimlerden bazıları iss (issuer), exp (expiration time), sub (subject), aud(audience) ve diğerleri. Bunlardan en çok kullanılanı expiration time yani son geçerlilik tarihidir. Örneğin token bilginizin 3 saat sonra geçersiz olmasını isterseniz bu bilgiyi exp alanında gönderirsiniz. 3 saat ardından aynı token ile gelen isteklerde token geçersiz olarak değerlendirilir.
- Public (Açık) claims: İsteğe bağlı, açık yayınlanan claimlerdir.
- Private (Gizli) claims: Tarafların kendi aralarında bilgi taşımak için kullandığı gizli claimlerdir.

```
{
  "sub": "1234567890",
  "name": "John Doe",
  "iat": 1516239022
}
```
Bu kısım Base64 ile encode edilir ve oluşturulacak tokenın ikinci parçasını oluşturur.

#### Signature(İmza) 
Bu kısım tokenın son kısmıdır. Bu kısmın oluşturulabilmesi için header, payload ve gizli anahtar(secret) gereklidir. İmza kısmı ile veri bütünlüğü garanti altına alınır. Burada kullandığımız gizli anahtar Header kısmında belirttiğimiz algoritma için kullanılır. Header ve Payload kısımları bu gizli anahtar ile imzalanır
```
HMACSHA256(
  base64UrlEncode(header) + "." +
  base64UrlEncode(payload),
  your-256-bit-secret
)

Bu kısmın oluşturulabilmesi için header, payload ve gizli anahtar(secret) gereklidir.
HMACSHA256(
  base64UrlEncode(header) + "." +
  base64UrlEncode(payload),
  your-256-bit-secret
)
```
