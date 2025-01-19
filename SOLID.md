# SOLID

Amaç;

- Kodlarınızı daha esnek ve geliştirilebilir kılar.
- Kodun yeniden kullanılabilirliğini arttırır.
- Kodların anlaşılır olmasını sağlar ve okunurluğunu sağlar.
- Kodların gereksiz tekrarını engeller.
- Kodlama zamanını kısaltır, performansı arttırır.

---

S → Single Responsibility - Tek Sorumluluk İlleki

- Bir sınıf bir method sadece tek bir göreve odaklanmalı ve tek iş yapmalıdır.
Örnek: IPostRepository, UserProfileController  - save(), findById()....

---

O → Open/Closed - Açıklık Kapalılık İlkesi

- Bir sınıf değişime kapalı , gelişiime açık olmalıdır.
- Bir sınıfıı kodlarken nihai halini kodlamalsınız. Yani o sınıf için yazılabilecek gerekli nihai kodları yazmalsınız. Böyle sınıf değişime kapalı olur. Ancak sınıf yeni geliştirmelere açık olabilir. bunu da sınıftan SubClass türeterek sağlarsınız.

---

L → Liskov Substutition - Liskov Prensibi

- Gereksiz method tanımlamaları ve kullanımlarından uzak durmalısınız. Eğer sınıflar arasında ortak method tanımları var ise mutlaka bir ParentClass içinde tanımlanarak miras alınmalıdır. Ek özellikler ve method tanımları mutlaka interface aracılığı ile tanımlanmalı ve kullanılmalıdır.

---

I → Interface Segretation - Genel Arayüz Tanımlama İlkesi

- Uygulamarı kullanırken genellikle Interface ' lerden yararlanırızz. Ancak genel tanımlı interface oluşturmak uygulamayı geliştirirken gayet verimli ve gelişime açık olmasını sağlıyıor.
→ Repository
       ->JPARepository (İlişkisel DB ler için işlemler gerçekleştirir)
             → ListCrudRepository
                   → CrudRepository
->JDBCRepository (Java DB Connection İşemleri)
→MongoRepository (Mongo DB için)

---

D → Dependency Inversion

- Sınıflar bir birilerine belli bir noktadan sonra bağımlılık atfetmeye başlarlar ve bu kaçınılmazdır. Ancak uygulamarımızda bu bağımlılıkların mümlün olduğun zayıflatılmasına çalışmalıyız.

