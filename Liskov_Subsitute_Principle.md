**Liskov Substitution Principle**

**NE,NEDEN**

Liskov Substitution Principle, 1987 yılında ‘Barbara Liskov’ tarafından bir konferansta tanıtıldı.

İlkenin anlamı, kodlarımızda herhangi bir değişiklik yapmaya gerek duymadan alt sınıfları, türedikleri(üst) sınıfların yerine kullanabilmektir. Başka bir söyleyişle, bir alt sınıfın üst sınıftan kalıtım alırken, kullanmayacağı özellikleri almaması gerekmektedir. Sadece ihtiyacı olduğu özellikleri alması gerekmektedir. Dolayısıyla sadece özelliklerinin bulunduğu sınıfı ‘inheritance’ etmelidir. Böylece karışıklıklar ve hata fırlatma önlenecek, uygulama bozulmadan bir üst sınıfın nesneleri alt sınıf nesneleriyle değişebilecektir.

**NASIL**

Mesela arabaya bir klima düğmesi koydunuz ancak ona bir görev atamadınız. Yani sadece görüntü olarak klima var ancak içeriyi soğutmuyor veya hava üflemiyor. İşte bu durum Liskov’a aykırı bir durumdur. Yani Liskov’a göre bir düğme varsa, o düğmenin işlevi de olmaldıır. 

Liskov ilkesinin daha da önemli olduğunu anlatmak için yukarıdakinden farklı, şöyle bir örnek de verilebilir;
Bir ordunun uçakları olduğunu düşünelim ve bu uçakların hem keşif yapabildiğini hem de hedefi vurabildiğini varsayalım. Daha sonra bu orduya sadece keşif yapabilen bir uçağın katıldığını kabul edelim. İşte burada eğer sadece tek bir arayüz belirlemişsek bu arayüz tüm özellikleri tüm uçaklara zorla uygulatacaktır ancak sonradan gelen uçağımızda bulunmayan bir özellik de vardır. Dolayısıyla burada Liskov’a uyumluluk için, keşif yapma ve hedefi vurma gibi iki ayrı arayüz oluşturulması gerekmektedir. Önceki uçaklar iki arayüze ‘inheritance’ edilmeli, sonradan eklenen tek özellikli uçak ise sadece bir arayüze ‘inheritance’ edilmelidir. Böylece kullanamayacağı bir işlevi barındırmamış olacaktır.
