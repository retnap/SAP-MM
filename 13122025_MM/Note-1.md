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

## MM01 -> Malzeme Yaratma Ekranı 

<img width="837" height="617" alt="13_mm01_1" src="https://github.com/user-attachments/assets/1c47eae0-e7e9-4c2e-aade-7e7873ee84f1" />

+ Temel Veriler 1 ve Temel Veriler 2 seçildi.

+ Satınalma seçildi.

+ Depolama 1 ve Depolama 2 seçildi.

+ Muhasebe 1 ve Muhasebe 2 seçildi.

+ **Not:** Bu seçimleri kaydedip sonrasında kullanmak için sağ altta bulunan "Ön Ayarlar" butonuna bas. 

**ROH:** SAP'nin standart malzeme türü. Bir hammaddeyi temsil eder. Dışarıdan satın alınabilir. Stokları takip edilebilir. Değeri takip edilebilir. 

Hammadde işlenerek mamule ya da yarı mamule dönüşür. 

**HALB:** Sistemdeki yarı mamulü temsil eder. Dışarıdan satın alınabilir ve değeri vardır. 

**FERT:** Sistemdeki mamulü temsil eder. İsteğe bağlı satın alınabilir. Değeri ve stoğu vardır. 

**NLAG:** Sarf, depolanmayan malzemeleri temsil eder. 

**SERV:** Hizmet ürününü temsil eder. 

<img width="826" height="401" alt="15_mm01_3" src="https://github.com/user-attachments/assets/81b944f8-e8fd-44d4-a24c-e5857a02432e" />



<img width="734" height="783" alt="16_mm01_4" src="https://github.com/user-attachments/assets/c2d4de4b-6464-454f-8f76-9c239021b769" />

+ Temel Veriler 1, görselde doldurulduğu gibidir. 

+ Temel Veriler 2'de aslında **konfigüre edilebilirlik** durumu kontrol edilir. Örnek olarak, bir araba alırken siyah rengi yerine bin lira farkla kırmızı rengini almak denebilir.

  + Temel Veriler 2'de bir değişiklik yapılmadı.
 
<img width="715" height="610" alt="17_mm01_5" src="https://github.com/user-attachments/assets/8ec34da2-8daf-487d-8c83-b21b318a0911" />
 
+ Yukarıdaki görselde Temel Veriler 1 ve 2 ekranlarından sonra **Satın Alma** ekranına geldik.
  + Temel ölçü birimi olarak daha önceden "KG" seçilmişti.
  + SAS Ölçü Birimi olarak (Satın Alma Ölçü Birimi) "PAK" -paket- seçildi.
  + Paket seçildikten sonra çıkan ekranda 1 pakette kaç kg olacağını girmemiz için ekran çıkıyor.
  + Satın Alma Grubu "200" olarak seçildi.
  + Parti Yönetimi kutucuğu işaretlendi.

+ Depolama 1 ekranında depo türü, raf ömrü, kalan süresi girildi.
  + Depolama 2'de bir değişiklik yapılmadı.


<img width="713" height="684" alt="18_mm_6" src="https://github.com/user-attachments/assets/54cc320d-d5c8-4270-a84a-025ff5e7079c" />

+ Muhasebe 1 ekranına geçildi.
  + Değerleme sınıfı olarak 7900 seçildi. Bu da demek oluyor ki 7900 'ın altına bağlı olan ana hesaplar benim için çalışacak.
  + **Değerleme Sınıfı (Valuation Class):** Bu malzemeyle ilgili parasal hareketler hangi muhasebe hesaplarında izlenecek ?
    + Uzun tanım olarak; malzemenin muhasebe kayıtları hangi G/L (ana hesaplara) gideceğini belirleyen alan.
    + SAP, hangi ana hesabı kullanacağını **Otomatik Hesap Ataması (Automatic Account Determination)** üzerinden **Değerleme Sınıfına** bakarak ilerler.     
  + Muhasebe 2 'de herhangi bir değişiklik yapılmadı.
 
+ Enter tuşuna bastıktan sonra önceki verilerin kaydedilmesi hakkında bir uyarı geldi. Evet diyip MM01 ekranına geri dönüyoruz. Bu şekilde bir malzeme oluşturmuş olduk.

+ **NOT:** Oluşturduğumuz malzemeye atanan kod "4451".    
--- 

## MM02 -> Malzeme Değiştirme Ekranı 

<img width="764" height="620" alt="19_mm02_1" src="https://github.com/user-attachments/assets/1392ec70-8c0d-4a04-8b2f-311b0dd7b0d0" />

<img width="716" height="622" alt="20_mm02_2" src="https://github.com/user-attachments/assets/532d29de-057a-47dd-9b00-d25c78fe6e68" />

## MM03 -> Malzeme Görüntüleme Ekranı 

<img width="722" height="620" alt="21_mm03_1" src="https://github.com/user-attachments/assets/8830c513-ac25-4339-899d-8ee403c86b1e" />


---

## BP -> Muhatap Düzenleme 

+ İş ortağı anlamına gelir. Ona ya mal satılıyordur ya da ondan mal alınıyordur.

<img width="862" height="833" alt="22_bp_1" src="https://github.com/user-attachments/assets/5b8affa6-d72f-4372-8309-1683db1d17cc" />

+ BP işlem kodunu girip Muhata Düzenleme ekranı geldikten sonra, üstte bulunan **"Organizasyon"** butonuna basıyoruz.
  + **Gruplama** olarak T001 Yurt İçi Muhatap seçildi.
  + Adres ekranı otomatik olarak karşımıza çıktı.
  + Muhatabın **"Hitap Biçimi"** olarak 0003 Şirket seçildi.
  + **"Ad"** kısmına muhatabın adı yazıldı.
  + **"Arama Terimleri"** kısmına, arama çubuğuna yazılacak terimi giriyoruz.
  + Alt kısımda bulunan adres kısımlarını dolduruyoruz. Detaylı doldurmak istersek bloğun sağ tarafta bulunan "+" simgesine basıyoruz.
  + Tüm bilgileri girdikten sonra Kontrol Et (F8) butonuna basıyoruz.
  + Hatasız ise Kaydet butonuna basıyoruz. Bu işlemden sonra sistem otomatik olarak muhatap kodu atıyor.

---

<img width="890" height="600" alt="25_bp_4" src="https://github.com/user-attachments/assets/78dda943-1397-4ca3-99f9-4f6d9d0928f3" />

+ Bu işlemden sonra "Muhatap Rolü" değerini **FLVN00 Satıcı - FI** seçiyoruz.
  + Değer seçildikten sonra sağ üstte **şirket kodu** butonu çıkıyor. Yani "hangi şirket kodu için bunu satıcı yapacaksın" diyor.
  + Şirket kodu olarak TR03 seçildi.
  + **Mutabakat Hesabı** olarak "3202021000 Satıcılar Hesabı Yurt İçi" seçildi. Yani para hangi ana hesaba ödenecek durumu seçilir.
  + Satıcı:Ödeme İşlemleri ekranına geliyoruz. **Ödeme Koşulu** olarak 0003 seçildi.
  + Kaydet butonuna tıkladığımızda artık **satıcı kodu** otomatik olarak sistem tarafından atanır.

---

<img width="1033" height="604" alt="26_bp_5" src="https://github.com/user-attachments/assets/8ac97524-6186-40b4-8cde-1395d0a5775d" />

+ Bu işlemden sonra da "Muhatap Rolü" değerini **FLVN01 Satıcı - MM** seçiyoruz.
  + Değer seçildikten sonra sağ üstte **Satınalma** butonu çıkıyor.
  + **SA Organizasyonu** olarak "1710" seçildi.
  + **SAS Para Birimi** olarak "TRY" seçildi.
  + Varsa ödeme koşulları ve aşağıda bulunan koşullar eklenebilir.
  + Tüm işlemlerden sonra "Kaydet" butonuna basıyoruz. 

---

<img width="976" height="393" alt="27_bp_6" src="https://github.com/user-attachments/assets/e51694fa-8b46-4da3-b311-be4cc2f36c2e" />

+ Oluşturulan muhatabı görüntülemek ve detayına inmek için tekrardan BP işlem kodunu kullanıyoruz.

+ "Ad"a göre arama yapabiliriz. Muhatap gözükürse çift tıklayarak detayına ulaşabiliriz.

---

<img width="891" height="577" alt="28_bp_7" src="https://github.com/user-attachments/assets/95337266-99b0-4077-98e2-c04e27f02dc4" />

+ **SE16N** transaction kodu ile **BUT000** Muhatap Genel Veriler tablosuna geliyoruz.

+ Oluşturulan Muhatap kodunu ilgili alana girdikten sonra sol üstte bulunan yürütme butonuna (F8) basıyoruz.

<img width="1101" height="350" alt="29_bp_8" src="https://github.com/user-attachments/assets/b48f1901-a904-42c3-a94c-9d4584102c7b" />

+ Böylece oluşturulan muhatabın detaylı bilgilerine ulaşabiliriz.

---

<img width="872" height="422" alt="30_bp_9" src="https://github.com/user-attachments/assets/b5d222ef-fd62-43d6-a1a6-f94cbe9b11d1" />

+ Önceki BUT000 ekranından Muhatap GUID'sini kopyalıyoruz.

+ Yine SE16N işlem kodundan **CVI_VEND_LINK** tablosuna geliyoruz.

+ Kopyaladığımız Muhatap GUID'sini ilgili alana yapıştırıyoruz ve sol üstte bulunan yürütme butonuna (F8) basıyoruz.

<img width="679" height="328" alt="31_bp_10" src="https://github.com/user-attachments/assets/e833dce1-db41-4534-910f-9dbbb47e0dc6" />

+ Yapılan işlemler sonucunda Muhatabın **satıcı numarasını** buluyoruz.

--- 






