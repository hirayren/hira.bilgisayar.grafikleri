# hira.bilgisayar.grafikleri
writing my name with webgl primitives
# KODUN GENEL YAPISI HK.
4 harften oluşan HİRA yazısını ekrana farklı renklerde yazmak için basit ancak gereksiz derecede uzun bir yol izledim. Sanırım bunu, bir faktöriyel sorusunu sadeleştirerek çözmek yerine tek tek çarparak sonuca ulaşmaya çalışmak gibi düşünebiliriz. Konudan biraz uzak kaldığım ve ödeve geç başladığım için bu durumu fark ettiğimde başka yoldan gidecek zamanım kalmadı tabi. Peki neden bu çalışmayı faktöriyel sorusuna benzettim, açıklayalım;
Öncelikle harfleri yazmak için her harfi dikdörtgenler halinde çizdim zira bilgisayarda görüntülemenin temeli piksellere bu pikseller bizzat kareler ve kareler de her şeyin başı üçgenlere dayanıyor. Kısaca basit çözüm olacaktı bu. Bunun için sırayla canvas oluşturma, webgl bağlamını alma, vertex ve fragment shaderlarını oluşturma gibi adımları (sevgili chatgpt, ders sunumları ve birtakım tutorial sayfalarının da yardımıyla) uyguladım. Dikdörtgenlerle harfleri olulturmak ise oldukça basit bir yapıya dayanıyor. Zaten harfleri dikdörtgen ve kareler halinde oluşturdum, ardından her birinin köşeleri için tek tek x,y koordinatlarını belirledim ve kodda tanımladım. Aslında her bir dörtgen için 4 köşe olmasına rağmen 6'şar köşe koordinatı göreceksiniz, bu da webgl'in temelde sadece nokta, çizgi ve üçgen çizebilmesinden kaynaklanıyor yani her bir dörtgeni iki üçgenden oluşturan konumları tanımlamak gerekiyor. Ardından yine biraz uzatılmış bir süreç olan renk atamaları için her dörtgeni ayrı ayrı renklendirmek gerekti çünkü başta tek renk olarak yazmaya başlamıştım.
# GELİŞTİRMELER VE EKSİKLER HK.
Halihazırda yukarıda açıkladıklarım ödevde ne hatalar yaptığımı gösteriyor, bu proje faktöriyel sorusunu uzun uzun çarparak çözmeye benziyor çünkü tek tek konum girmek yerine artan birkaç değişken oluşturup bunları döngüye de ekleyebilirdik diye düşünüyorum. Mantık yine aynı basit dörtgenler ancak birçok konumu tek tek girmekle uğraşmamış olacaktım.
Yine de tamamen hüsran değil, daha uzun yazılar, çok daha fazla çokgen içeren bir proje olsaydı tek tek girmek mümkün olmazdı ancak 4 harf için tercih edilmez bir yöntem de değil. Ayrıca noktaları oluştururken GeoGebra kullanıp istediğim tüm noktaları belirlediğimde sadece belirli koordinatları koda eklemek yeterli oldu, modelleme her daim hayat kurtarır. (yorum satırlarında koordinatların yanındaki m-u-s-s-v-m tarzında belirteçler de aslında GeoGebra'da işaretlediğim noktaların adıydı.
Bu hataların dışında ödevde istenenlere nazaran birçok eksik kaldığını da belirtmeliyim, 3 boyutlu bir çizimi geçelim dönüşüm işlemleri dahi bulunmuyor.
Ancak yine de adım ekranda yazıyor!
