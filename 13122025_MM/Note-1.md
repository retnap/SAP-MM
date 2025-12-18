# SAP MM Modülüne Genel Bakış 

<img width="1023" height="448" alt="Ekran Resmi 2025-12-18 14 12 28" src="https://github.com/user-attachments/assets/42147d11-bf0c-472f-87d3-2b7164134615" />

+ MM Modülü fatura kesmez, fatura girişi yapar.

  + Faturayı satış yapan firma, satış yaptığı için keser. Alım yapıldığı için MM modülü, fatura girişi yapar.

---

# SAP MM Organizasyonel Yapı 

<img width="1025" height="577" alt="Ekran Resmi 2025-12-18 14 16 24" src="https://github.com/user-attachments/assets/0993da44-30f2-4bfa-82f9-7d2748968d9b" />

+ **Şirket kodu** yasal bir gerekliliktir.

  + Muhasebe belgeleri, şirket kodu bazında çalışır. 

  + Sistemde şirket kodunu muhasebe departmanı yaratır. 

+ Sistemde istenilen kadar **üretim yeri** yaratılabilir ama **en az bir** şirket koduna atanmak zorundadır.

  + Üretim yeri bazında **maliyet muhasebesi (CO)** belgeleri çalışır.
 
+ **Depo yeri**, sistemde istenildiği kadar yaratılabilir.

  + Depo yeri, üretim yerine bağlı olmak zorundadır.

+ **Satın alma organizasyonu**, bir satın alma kanalı gibi düşünülebilir.

  + Bir satın alma kanalı, genellikle **raporlama** amacı ile kullanılır.
 
  + Yukarıdaki görselde de görüldüğü üzere, satın alma organizasyonu herhangi bir yere atanmamıştır. Çünkü satın alma organizasyonunu atamanın 3 yolu vardır: 

    + 1. Grup İçi Satın Alma
      2. Şirket Kodu Bazlı Satın Alma
      3. Üretim Yeri Bazlı Satın Alma
     
    + **Grup İçi Satın Alma** -> Şirketin bir tane satın alma departmanı var ve içerisinde 100 kişi çalışıyor. Tüm üretim yerlerine satın alma işlemi sadece bu departmandan yönetiliyor. 

    + **Şirket Kodu Bazlı Satın Alma** -> Satın alma organizasyonu şirket koduna bağlanır. Sonrasında sistem hangi üretim yerlerinin seçileceğini sorar.
   
    + **Üretim Yeri Bazlı Satın Alma** -> Satın alma organizasyonu direkt üretim yerine bağlanır.
   
  + **Satın Alma Grubu:** Satın alma süreçlerinde bir departmanı veya bir kişiyi temsil eder. Üç gruba ayrılabilir:
    
    + **Direkt Satın Almalar:** Üretimi doğrudan etkliyene satın almalar  
    + **Endirekt Satın Almalar:** Hizmet, sarf malzemesi satın almalar
    + **Bakım Satın Almalar:** B01 

 ---
 
# Ana Veri

<img width="689" height="493" alt="Ekran Resmi 2025-12-18 14 41 31" src="https://github.com/user-attachments/assets/2868ad07-9d10-46b8-b693-3b1f89abead6" />

+ **Malzeme Ana Verisi:** Faaliyette olan malzemenin sisteme kaydı için gerekli olan verisidir.

+ **Satıcı Ana Verisi:** Malzemenin satın alındığı, tedarik edildiği yer anlamına gelir.

+ **Bilgi Kaydı Ana Verisi:** Malzeme ve satıcının birleşimi ile oluşur. Bu malzeme şu satıcıdan, bu üretim yerinden, şu satın alma organizasyonundan gibi işlemler tutulur. Şirket ve satıcı arasındaki yazılı olmayan anlaşmaları da tutar.

  + Kısaca şikretin malzemesi ve satıcı arasındaki tedarik bilgilerini tutar. 

+ **Satıcı Listesi:** Bu malzeme bu üretim yerinde şu satıcılardan alınabilir demek.

  + MRP'de malzeme ihtiyaç planlama aşamasında kullanılabilir.
 
+ **Kotalama:** Bir ürünün yüzde kaç oranında ve kimden tedarik edinilebileceğini gösteren ekran.


## Malzeme Ana Verisi 

<img width="1019" height="576" alt="Ekran Resmi 2025-12-18 14 52 45" src="https://github.com/user-attachments/assets/8820181e-cdf9-45cc-931d-505f9d9d19e9" />

+ Görselde bulunan silindirlerin SAP'deki karşılığı **görünümdür**.
  + Temel Veriler Görünümü
  + Satın Alma Görünümü
  + Depolama Görünümü
  + Muhasebe Görünümü

---

## Satıcı Ana Verisi 
  
<img width="698" height="463" alt="Ekran Resmi 2025-12-18 15 04 09" src="https://github.com/user-attachments/assets/9fff57b7-8daa-48ce-995f-7e896c362b8d" />

---

## Satın Alma Bilgi Kaydı 

<img width="774" height="487" alt="Ekran Resmi 2025-12-18 15 05 34" src="https://github.com/user-attachments/assets/2fb7cf42-e32a-4c40-923e-dcd611700a03" />

+ Malzeme ve satıcının birleşimiyle ortaya çıkıyor. 

+ Satın alma organizasyonu ve üretim yeri bazında oluyor.

  + **Konsinye:** Bir satıcının ürünlerini sattığı başka bir satıcıya, bir dağıtıcıya ya da bir komisyoncuya, ürünlerin tamamen satıldıktan sonra ödemenin yapıldığı bir satış yöntemini ifade eder.

    + Örn: Bir satıcıdan 100 tane malzeme alındı ve depoya konuldu. Alınan malzemelerin parası, her ay kullanılan kadar ödenir. Bu ay 20 malzeme kullanıldıysa 20 malzemelik para satıcıya ödenir.
   
  + **Fason:** Bir firmanın kendi üretim tesislerinde üretmek yerine, üretim aşamasının bir kısmını veya tamamını başka bir firmaya yaptırmasıdır.
 
    + Örn: Sandalye üretim yapan firma, kendi bünyesinde boyahane bulundurmadığı için sandalyeleri boyatmak üzere bir boyahaneye gönderir. Bu fason üretimdir.
   
  + **Yoldaki:** Gaz, sıvı, elektrik gibi takibi zor olan durumlarda kullanılır. Borunun içinden geçen malzemeler gibi düşünülebilir.    

---

## Satıcı Listesi 

<img width="728" height="421" alt="Ekran Resmi 2025-12-18 15 16 39" src="https://github.com/user-attachments/assets/a7d149de-cb2a-4c6e-b38e-dc1e116fadce" />

+ Bu malzeme bu üretim yerinde Satıcı A'dan alınsın, Satıcı B'den alınsın, Satıcı C'den alınmasın. 

---

## Kotalama 

<img width="701" height="362" alt="Ekran Resmi 2025-12-18 15 18 14" src="https://github.com/user-attachments/assets/c63f3736-f4d8-4c46-9ecf-0ac5d30847c1" />

+ Süreç başlangıç ve bitiş tarihi boyunca, **üretim yeri bazında** olur. 

---

# Standart Satın Alma Süreci 

<img width="824" height="482" alt="Ekran Resmi 2025-12-18 15 20 02" src="https://github.com/user-attachments/assets/c165ce33-ce25-438c-926f-2cc671ffed3c" />

+ Sözleşme **miktar bazlı** ya da **değer bazlı** olabilir.

## Standart Satın Alma Süreci Adımları 

<img width="711" height="429" alt="Ekran Resmi 2025-12-18 15 30 46" src="https://github.com/user-attachments/assets/77260aed-f8a9-4fc8-9dd1-1402b27ae4c9" />

+ **Satın Alma Talebi:** Oluşturulmak zorunlu değildir.
  + Manuel ya da MRP sistemi ile oluşturulur.
  + Malzeme veya Hizmet Kalemi girilir.

+ **Satın Alma Onayı:** Satın alma onayı **kalem** seviyesinde ya da **başlık** seviyesinde olabilir.
  + **Kalem Seviyesinde Onay:** 100 kalemden 80 tanesi onaylanacak, 20 tanesi reddedilecek.
  + **Başlık Seviyesinde Onay:** 100 kalemin de onaylandığı durum.

---

 <img width="705" height="387" alt="11_Satin_Alma_2" src="https://github.com/user-attachments/assets/bf39c826-26b0-439a-a19b-b008f710fa6b" />

---

<img width="714" height="323" alt="12_Satin_Alma_3" src="https://github.com/user-attachments/assets/b88db0cb-7dcc-4d63-9c6c-1d2c10df1fad" />

---

MM01 -> Malzeme Yaratma Ekranı 

MM02 -> Malzeme Değiştirme Ekranı 

MM03 -> Malzeme Görüntüleme Ekranı 







