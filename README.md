
# Port Tarama ve Banner Alma Scripti

Bu Python scripti, belirli bir IP adresinde (örneğin `192.168.1.251`) 1 ile 100 arasındaki portları tarar ve açık olan portların banner bilgilerini elde etmeye çalışır.


- **Python 3.x**
- **socket** kütüphanesi



Bu script, belirtilen IP adresindeki portları sırayla tarar ve her bir portun açık olup olmadığını kontrol eder. Eğer bir port açıksa, bu porttan alınabilecek bir banner (tanıtıcı metin) varsa bunu alır ve ekrana yazdırır.

### Adımlar:
1. **Socket Oluşturma:** Her bir port için bir TCP bağlantısı oluşturmak üzere `socket` modülü kullanılır.
2. **Timeout Ayarı:** Bağlantının hızlı bir şekilde kontrol edilmesi için 1 saniyelik bir timeout süresi belirlenir.
3. **Bağlantı Kurma:** Her port için bağlantı kurulmaya çalışılır. Bağlantı başarılı olursa portun açık olduğu kabul edilir.
4. **Banner Alma:** Açık olan portlar için, eğer port 80 (HTTP) ise, basit bir HTTP GET isteği gönderilir ve dönen cevap alınır. Diğer portlar için ise "farklı bir yöntem kullanılmalı" uyarısı verilir.
5. **Hata Yönetimi:** Bağlantı kurulamazsa portun kapalı olduğu varsayılır ve ilgili hata mesajı ekrana yazdırılır.
6. **Bağlantı Kapama:** Her işlemden sonra socket bağlantısı kapatılır.



## Kullanım

1. Python yüklü bir bilgisayarda bu scripti çalıştırabilirsiniz.
2. `ip` değişkenini taramak istediğiniz hedef IP adresiyle değiştirin.
3. Port aralığını genişletmek veya daraltmak için `range(1,100)` kısmını değiştirin.
4. Scripti çalıştırdığınızda açık portlar ve varsa banner bilgileri ekrana yazdırılacaktır.


