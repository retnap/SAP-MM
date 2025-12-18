# SAP MM Modülüne Genel Bakış 

<img width="1023" height="448" alt="Ekran Resmi 2025-12-18 14 12 28" src="https://github.com/user-attachments/assets/42147d11-bf0c-472f-87d3-2b7164134615" />

+ MM Modülü fatura kesmez, fatura girişi yapar.

  + Faturayı satış yapan firma, satış yaptığı için keser. Alım yapıldığı için MM modülü, fatura girişi yapar.
 
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
    
    + Direkt Satın Almalar
    + En Direkt Satın Almalar
    + Bakım Satın Almalar
 
  + 
