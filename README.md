📚 C# Notebook Uygulaması (OOP Projesi)
Proje Tanımı
Bu proje, C# dili ve Windows Forms kullanılarak geliştirilmiş, temel not alma işlemlerini (oluşturma, okuma, güncelleme, silme) gerçekleştiren basit bir masaüstü uygulamasıdır. Projenin ana amacı, Nesne Tabanlı Programlama (OOP) prensiplerini pratik olarak uygulamaktır.

Kullanılan Teknolojiler
Dil: C#

Platform: .NET Framework / .NET (Windows Forms Uygulaması)

Geliştirme Ortamı: Visual Studio

💡 Nesne Tabanlı Programlama (OOP) Prensipleri
Uygulamanın yapısı, iyi bir OOP tasarımı için iki temel sınıf üzerine kurulmuştur: Not ve NotYoneticisi.

1. Kapsülleme (Encapsulation)
Notun özellikleri (Baslik, Icerik, OlusturmaTarihi) Not.cs sınıfında tanımlanmıştır. Veri bütünlüğünü korumak amacıyla bu özelliklere erişim, public get; set; veya kontrollü (private set) yöntemlerle sağlanarak kapsülleme ilkesi uygulanmıştır.

2. Sorumlulukların Ayrılması
Proje, iş mantığı ile sunum katmanını net bir şekilde ayırır:

Not.cs: Tek bir notun verisini (Model) tutar.

NotYoneticisi.cs: Tüm notları bir koleksiyonda (List<Not>) tutar ve Ekleme, Silme, Güncelleme gibi tüm iş mantığı operasyonlarından sorumludur.

Formlar (Form1, NotListeleForm): Yalnızca kullanıcı arayüzünü ve veri gösterimini (Sunum Katmanı) yönetir.

3. Çok Biçimlilik (Polymorphism)
Not.cs sınıfında, notların liste ekranında daha anlamlı görünmesi için temel Object sınıfından gelen ToString() metodu ezilerek (Override) Çok Biçimlilik prensibi kullanılmıştır.

Temel İşlevler
Uygulama, temel CRUD (Create, Read, Update, Delete) operasyonlarını destekler:

Oluşturma (Create): "Dosya > Yeni Not" ile başlatılır ve "Dosya > Kaydet" ile yeni not NotYoneticisi'ne eklenir.

Okuma/Listeleme (Read): "Dosya > Aç" menüsü ile tüm notların listesi ayrı bir formda görüntülenir.

Güncelleme (Update): Açık olan notun içeriği değiştirilip "Dosya > Kaydet" ile güncellenir.

Silme (Delete): Not listesi formu üzerinden seçilen not, NotYoneticisi'nin metodu çağrılarak koleksiyondan silinir.
