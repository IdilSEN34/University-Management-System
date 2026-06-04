# 🎓 Üniversite Veri Yapıları Otomasyon Sistemi

Marmara Üniversitesi Bilgisayar Mühendisliği Bölümü için geliştirilmiş, arka planında standart Java kütüphaneleri (`java.util.*`) yerine **tamamen sıfırdan tasarlanmış veri yapıları** kullanan modern bir üniversite yönetim otomasyonudur. 

Sistem; akademik kadro yönetimi, öğrenci işleri, interaktif ders önkoşul hesaplamaları ve UI/UX odaklı dinamik gösterge panellerini (dashboard) tek bir MVC mimarisinde birleştirir.

![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=java&logoColor=white)
![JavaFX](https://img.shields.io/badge/JavaFX-FF0000?style=for-the-badge&logo=javafx&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-07405E?style=for-the-badge&logo=sqlite&logoColor=white)
![Architecture](https://img.shields.io/badge/Architecture-MVC-success?style=for-the-badge)

## 🚀 Öne Çıkan Özellikler ve Algoritmik Altyapı

Bu projenin mühendislik odak noktası, bellek yönetiminin ve gösterici (pointer) mantığının derinlemesine işlendiği özel veri yapılarıdır:

* **Hızlı Veri Erişimi $O(\log N)$:** Öğrenci, öğretmen ve ders kayıtları bellekte özel **Binary Search Tree (BST)** yapısında tutularak yüksek performanslı arama ve manipülasyon sağlanır.
* **Ders Önkoşul Yönetimi (Kahn's Algorithm):** Dersler arası önkoşul bağlantıları yönlü graf (**Directed Graph**) ile modellenmiş ve öğrencilerin alabileceği ders sıralamaları **Topolojik Sıralama** ile $O(V + E)$ karmaşıklığında hesaplanmıştır.
* **Dinamik Başarı Sıralaması $O(\log N)$:** Üniversitenin en yüksek ortalamaya (GPA) sahip öğrencileri **Max Heap** yapısı kullanılarak anlık olarak listelenir.
* **Durum Kontrolü ve İşlem Geçmişi:** Sistemdeki CRUD işlemlerinin güvenle geri (Undo) ve ileri (Redo) alınması, **Custom Stack** (LIFO) ve duyuru/burs kuyrukları **Custom Queue** (FIFO) ile yönetilmektedir.
* **Sıralama Algoritmaları:** Grid ve listeleme operasyonlarında özelleştirilmiş **Merge Sort** ve **Quick Sort** algoritmaları kullanılmıştır.

## 🎨 Arayüz (UI/UX) ve Deneyim

* **Modern MVC Tasarımı:** Separation of Concerns prensibiyle ayrıştırılmış, duyarlı (responsive) JavaFX arayüzü.
* **Dinamik Çizelgeler:** Öğrenci not ortalaması değişimlerini gösteren interaktif `LineChart` grafikleri.
* **Görsel Geri Bildirimler:** İşlem durumlarına göre renk kodlu (success, danger, warning) statü rozetleri (badges).
* **Asenkron İşlemler:** Veritabanı okuma/yazma işlemlerinin UI thread'ini dondurmaması için `Task<T>` yapısıyla kurgulanmış arka plan thread yönetimi.

## 💻 Ekran Görüntüleri

| Yönetici Paneli (Dashboard) | Veri Yönetimi ve Önkoşullar |
| :---: | :---: |
| ![Dashboard](docs/images/dashboard.png) <br> *Dinamik Timeline, LineChart ve MaxHeap ile Top Öğrenci Listesi* | ![Queue](docs/images/queue.png) <br> *BST tabanlı hızlı arama ve durum etiketleri* |

*(Not: Ekran görüntülerini repo'ya ekledikten sonra yukarıdaki dosya yollarını güncelleyiniz.)*

## 🛠️ Kurulum ve Çalıştırma

Projeyi yerel ortamınızda test etmek için:

1. Repoyu bilgisayarınıza klonlayın:
   ```bash
   git clone [https://github.com/IdilSEN34/University-Management-System.git](https://github.com/IdilSEN34/University-Management-System.git)
