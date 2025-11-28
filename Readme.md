# Katkı Kuralları

1. main branch’e direkt push yasaktır..
2. Herkes kendi branch’ini açar:
   git checkout -b isim-ozellik
3. Kod bittikten sonra Pull Request açılır
4. En az 1 onay olmadan merge yapılmaz
5. Merge sonrası herkes git pull ile güncel main’i çeker

GitHub Ortak Çalışma Rehberi (Branch + Pull Request Yöntemi)
Aşağıdaki adımlar, bir. sayfanın farklı bölümlerini grup olarak tasarlayıp ortak GitHub reposuna yüklemek için kullanılacaktır.

1. Reponun Bilgisayara İndirilmesi (Clone)
   Terminal açılır ve proje klasörünün bulunacağı dizine gidilir:
   cd klasor-yolu
   Ortak repo indirilir:
   git clone REPO_ADRESI
   Oluşan klasöre girilir:
   cd proje-adi
2. Her Öğrenci Kendi Branch’ini Oluşturur
   Herkes kendine ait bir çalışma alanı (branch) açar:
   git checkout -b benim-branchim
   Bu branch’te herkes kendi bölümünü tasarlar.
3. Kendi Dosyalarını Proje Klasörüne Aktarma
   Her öğrenci kendi bilgisayarındaki tasarım dosyalarını (örneğin index.html, style.css) projenin içine sürükleyip bırakır veya kopyalar.
4. Git'in Değişiklikleri Görmesi
   git status
   Yeni eklenen veya değişen dosyalar burada listelenir.
5. Dosyaların Git’e Eklenmesi
   git add .
   Nokta, mevcut klasördeki tüm değişiklikleri ekler.
6. Commit Yapılması
   git commit -m "Tasarım dosyalarımı ekledim"
   Açıklama mesajı yaptığınız işi belirtmelidir.
7. Branch’in GitHub’a Gönderilmesi (Push)
   git push --set-upstream origin Hasan_K -- ilk push için
   git push --daha sonra yapılacak pushlar için yeterli
   Bu komut çalışınca GitHub’da otomatik olarak yeni branch oluşur.
8. Pull Request (PR) Açılması
   GitHub’da:
9. Pull Requests → New Pull Request
10. “base: main” “compare: benim-branchim”
11. Açıklama yazılır.
12. Create Pull Request butonuna basılır.
    Ekip arkadaşları inceleyip onaylar.
13. PR Onaylandıktan Sonra Merge Edilir
    Kod ana (main) branch’e eklenmiş olur.

14. Tüm Ekip En Güncel Kodu Çeker
    PR onaylandıktan sonra
    git checkout main
    git pull origin main

    bu kodlar ile main local bilgisayarınızın main branchi güncel tutulur

    daha sonra kendi branchinize

    git checkout Kendi_branchiniz
    git pull origin main

    yapılarak kendi branchiniz de güncel ile eşitlenmiş olur

15. Her push işleminden sonra pull request oluşturulması zorunludur
16. Her pull işleminden önce pull request kontrol edilmelidir aksi halde conflictler oluşmaktadır.
17. Github da şuan dosya karmaşası olmaması için herkes yaptığı her değişikliği yorum satırları halinde bir blok içine almalıdır.
18. Sınıf adlarına öncelik vererek css düzenlemeleri tekrar yapılmalıdır.Kodlar birleşeceği için element isimlerine stil verilmememelidir
19. Stil verilen elementler için stil belirtecinin başına bir sınıf veya ait olduğu sectionın belirteci konulmalıdır (örn: .hero p, footor p)
20. Vector ve jpg formatlı dosyalar tek el olarak ekip lideri tarafından tekrar indirilip özel olarak klasörlenecektir bu işlemden sonra html düzenlemeleri ekip üyeleri tarafından yapılmalıdır
21. Oluşan düzeni bozacak veya fazladan dosya ekleyecek herhangi bir push işleminden kaçınılmalı böyle bir durum olduğunda ekip üyelerinden yardım istenmesi zorunludur.
