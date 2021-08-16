# Java_Kodluyoruz_101

Bu repo [Kodluyoruz](https://www.kodluyoruz.org/) Java 101 eğitimi için hazırlamış olduğum repo. İçerisinde Java pratiklerin,ödevlerinin soru ve cevaplarını içeren bir adet README dosyası barındırıyor.

|  PRATİKLER  |  ÖDEVLER |
|-----------|---------|
| [PRATİK 1](https://github.com/havakaragozx/Java_Kodluyoruz_101/blob/main/README.md#pratik-1---not-ortalamas%C4%B1) - Not Ortalaması| [ÖDEV 1](https://github.com/havakaragozx/Java_Kodluyoruz_101/blob/main/README.md#%C3%B6dev-1---v%C3%BCcut-kitle-indeksi-hesaplama) - Vücut Kitle Indeksi Hesaplama|
| [PRATİK 2](https://github.com/havakaragozx/Java_Kodluyoruz_101/blob/main/README.md#pratik-2---kdv-tutar%C4%B1) - Kdv Tutarı | [ÖDEV 2](https://github.com/havakaragozx/Java_Kodluyoruz_101/blob/main/README.md#%C3%B6dev-2--manav-kasa-program%C4%B1) - Manav Kasa Programı |
| [PRATİK 3](https://github.com/havakaragozx/Java_Kodluyoruz_101/blob/main/README.md#pratik-3---alan-hesaplama) - Alan Hesaplama | [ÖDEV 3](https://github.com/havakaragozx/Java_Kodluyoruz_101/blob/main/README.md#%C3%B6dev-3---u%C3%A7ak-bileti-fiyat%C4%B1-hesaplayan-program) - Uçak Bileti Fiyatı Hesaplayan Program |
|[PRATİK 4](https://github.com/havakaragozx/Java_Kodluyoruz_101/blob/main/README.md#pratik-4---taksimetre-hesaplama) - Taksimetre Hesaplama | [ÖDEV 4]() - Çin Zodyağı Hesaplama |
|[PRATİK 5](https://github.com/havakaragozx/Java_Kodluyoruz_101/blob/main/README.md#prati%CC%87k-5---alan-hesaplama) - Alan Hesaplama |
|[PRATİK 6](https://github.com/havakaragozx/Java_Kodluyoruz_101/blob/main/README.md#pratik-6---hesap-makinesi) - Hesap Makinesi|
|[PRATİK 7](https://github.com/havakaragozx/Java_Kodluyoruz_101/blob/main/README.md#pratik-7---kullan%C4%B1c%C4%B1-giri%C5%9Fi) - Kullanıcı Girişi|
|[PRATİK 8](https://github.com/havakaragozx/Java_Kodluyoruz_101/blob/main/README.md#pratik-8---s%C4%B1n%C4%B1f%C4%B1-ge%C3%A7me-durumu) -  Sınıfı Geçme Durumu|
|[PRATİK 9](https://github.com/havakaragozx/Java_Kodluyoruz_101/blob/main/README.md#pratik-9---hava-s%C4%B1cakl%C4%B1g%C4%B1na-g%C3%B6re-etkinlik) - Hava Sıcaklıgına Göre Etkinlik|
|[PRATİK 10](https://github.com/havakaragozx/Java_Kodluyoruz_101/blob/main/README.md#pratik-10---k%C3%BC%C3%A7%C3%BCkten-b%C3%BCy%C3%BC%C4%9Fe-s%C4%B1ralama) - Küçükten Büyüğe Sıralama|
|[PRATİK 11](https://github.com/havakaragozx/Java_Kodluyoruz_101/blob/main/README.md#pratik-11---bur%C3%A7-bulan-program) - Burç Bulan Program|
-------------------------------------------
### Pratik 1 - Not Ortalaması
Java ile Matematik, Fizik, Kimya, Türkçe, Tarih, Müzik derslerinin sınav puanlarını kullanıcıdan alan ve ortalamalarını hesaplayıp ekrana bastırılan programı yazın.

```
package Pratik1;
import java.util.Scanner;
public class NotOrtalamasi {
    public static void main(String[] args) {
    int mat,fizik,kimya,turkce,tarih,muzik;
    Scanner input=new Scanner(System.in);
        System.out.print("Matematik notunuzu giriniz = ");
        mat = input.nextInt();

        System.out.print("Fizik notunuzu giriniz = ");
        fizik = input.nextInt();

        System.out.print("Kimya notunuzu giriniz = ");
        kimya = input.nextInt();

        System.out.print("Türkçe notunuzu giriniz = ");
        turkce = input.nextInt();

        System.out.print("Tarih notunuzu giriniz = ");
        tarih = input.nextInt();

        System.out.print("Müzik notunuzu giriniz = ");
        muzik = input.nextInt();

         int toplam=mat+fizik+kimya+muzik+turkce+tarih;
         double ortalama= toplam/6;
         System.out.println("Ortalama :"+ortalama);

         boolean kosul1=ortalama>=60;
        System.out.print("Durum="+(kosul1==true ? "Geçti" : "Kaldı"));
    }
}
```
### Pratik 2 - Kdv Tutarı
Java ile kullanıcıdan alınan para değerinin KDV'li fiyatını ve KDV tutarını hesaplayıp ekrana bastıran programı yazın.

```
package Pratik1;
import java.util.Scanner;
public class KdvHesaplama {
    public static void main(String[] args) {
        double tutar,kdvOran=0,kdvTutar,kdvliTutar;
        Scanner input=new Scanner(System.in);
        System.out.print("Ücret Tutarını Giriniz:");
        tutar=input.nextDouble();
        if (tutar>0 && tutar<1000){
            kdvOran=0.18;

        }
        else if(tutar>1000){
            kdvOran=0.08;
        }
        else{
            System.out.println("Geçerli Tutar Giriniz.");
        }
        kdvTutar=tutar*kdvOran;
        kdvliTutar=tutar+kdvTutar;
        System.out.println("Kdv'siz Tutar : "+tutar);
        System.out.println("Kdv Oranı: "+kdvOran);
        System.out.println("Kdv Tutarı: "+kdvTutar);
        System.out.println("Kdv'li Tutar: "+kdvliTutar);

    }
}
```
### Pratik 3 - Alan Hesaplama
Üç kenar uzunluğunu kullanıcıdan aldığınız üçgenin alanını hesaplayan programı yazınız.
```
package Pratik1;
import java.util.Scanner;
public class Hipotenus {
    public static void main(String[] args) {
        double a,b,c;
        double alan,u;

        Scanner input=new Scanner(System.in);
        System.out.print("1.Kenarı giriniz:");
        a=input.nextInt();
        System.out.print("2.Kenarı giriniz:");
        b=input.nextInt();

        System.out.print("3.Kenarı giriniz:");
        c=input.nextInt();

        u=(a+b+c)/2;
        alan=Math.sqrt(u*(u-a)*(u-b)*(u-c));
        System.out.println("Üçgenin Alanı : "+alan);



        System.out.println();
    }

}
```
### Pratik 4 - Taksimetre Hesaplama
Java ile gidilen mesafeye (KM) göre taksimetre tutarını ekrana yazdıran programı yazın.
-Taksimetre KM başına 2.20 TL tutmaktadır.
-Minimum ödenecek tutar 20 TL'dir. 20 TL altında ki ücretlerde yine 20 TL alınacaktır.
-Taksimetre açılış ücreti 10 TL'dir.
```
package Pratik1;
import java.util.Scanner;
public class Taksimetre {
    public static void main(String[] args) {
        int km;
        double perKm=2.20,total=10;

        Scanner input=new Scanner(System.in);
        System.out.print("Mesafeyi km cinsinden giriniz: ");
        km=input.nextInt();
        total+=(km*perKm);
        total=(total<20) ? 20 : total;
        System.out.println("Toplam Tutar: "+total);

    }
}

```
### Pratik 5 - Alan Hesaplama
Yarıçapı r, merkez açısısının ölçüsü 𝛼 olan daire diliminin alanı bulan programı yazınız.
-𝜋 sayısını = 3.14 alınız.
-Formül : (𝜋 * (r*r) * 𝛼) / 360

```
import java.util.Scanner;
public class DaireAlanCevre {
    public static void main(String[] args) {
        int r;
        double pi=3.14;

        Scanner input=new Scanner(System.in);
        System.out.print("Dairenin Yarıçapını girin:");
        r=input.nextInt();
        double alan=pi*r*r;
        System.out.println("Dairenin Alanı : "+alan);
        double merkezAcı,daireDilimAlan;
        System.out.println("Dairenin merkez açısını giriniz: ");
        merkezAcı=input.nextDouble();
        daireDilimAlan=(pi*(r*r)*merkezAcı)/360;
        System.out.println("Dairenin diliminin Alanı : "+daireDilimAlan);
    }
}
```

### ÖDEV 1 - Vücut Kitle Indeksi Hesaplama
Java ile kullanıcıdan boy ve kilo değerlerini alıp bir değişkene atayın. Aşağıda ki formüle göre kullanıcının "Vücut Kitle İndeks" değerini hesaplayıp ekrana yazdırın.
```
import java.util.Scanner;
public class VucutKitleIndeksi {
    public static void main(String[] args) {
        double boy,kilo,kitleIndeks;
        Scanner input=new Scanner(System.in);
        System.out.println("Boyunuzu giriniz: ");
        boy=input.nextDouble();
        System.out.println("Kilonuzu giriniz: ");
        kilo=input.nextDouble();

        kitleIndeks=kilo/(boy*boy);
        System.out.println("Vücut Kitle Indeksiniz: "+kitleIndeks);
    }
}
```
### ÖDEV 2 -Manav Kasa Programı
Java ile kullanıcıların manavdan almış oldukları ürünlerin kilogram değerlerine göre toplam tutarını ekrana yazdıran programı yazın. 
Meyveler ve KG Fiyatları: 
Armut : 2,14 TL,
Elma : 3,67 TL,
Domates : 1,11 TL,
Muz: 0,95 TL,
Patlıcan : 5,00 TL
```
import java.util.Scanner;
public class ManavKasa {
    public static void main(String[] args) {
        double armutKg=2.14, elmaKg=3.67, domatesKg=1.11, muzKg=0.95, patlicanKg=5;
        double armut, elma, domates, muz, patlican, toplamTutar;
        Scanner input = new Scanner(System.in);
        System.out.print("Armut Kaç Kilo ? :");
        armut = input.nextFloat();

        System.out.print("Elma Kaç Kilo ? :");
        elma = input.nextFloat();

        System.out.print("Domates Kaç Kilo ? :");
        domates = input.nextFloat();

        System.out.print("Muz Kaç Kilo ? :");
        muz = input.nextFloat();

        System.out.print("Patlıcan Kaç Kilo ? :");
        patlican = input.nextFloat();
        toplamTutar=(armut*armutKg)+(elma*elmaKg)+(domates*domatesKg)+(muz*muzKg)+(patlican*patlicanKg);
        System.out.print("Toplam Tutar :" + toplamTutar + " TL");
    }
}
```
### Pratik 6 - Hesap Makinesi 
Java switch case ile basit hesap makinesi yapımı.
```
import java.util.Scanner;
public class HesapMakinesi {
     public static void main(String[] args) {
          int n1,n2,select;

          Scanner input=new Scanner(System.in);
          System.out.print("İlk sayıyı girin: ");
          n1=input.nextInt();
          System.out.print("İkinci sayıyı girin:");
          n2=input.nextInt();
          System.out.println(n1 + n2);

          System.out.println("1-Toplama\n2-Çıkarma\n3-Çarpma\n4-Bölme");
          System.out.print("Seçiminiz:");
          select=input.nextInt();
    
          switch (select){
               case 1 :
                    System.out.println("Toplam:"+(n1+n2));
                    break;
               case 2:
                    System.out.println("Çıkarma: "+(n1-n2));
                    break;
               case 3:
                    System.out.println("Çarpma: "+(n1*n2));
                    break;
               case 4:
                    if(n2!=0){
                         System.out.println("Bölme: "+(n1/n2));
                    }
                    else{
                         System.out.println("Bir sayı 0 a bölünemez.");
                    }
                    break;
               default:
                    System.out.println("Yanlış seçim yaptınız.");
                    break;
          }
     }

}


```

### Pratik 7 - Kullanıcı Girişi
Java koşullu ifadeler ile kullanıcı adı ve şifreyi kontrol eden program yapımı.

```
import java.util.Scanner;

public class KullaniciGirisi {
    public static void main(String[] args) {

        String userName, passWord;
        char sifreCevap;

        Scanner input = new Scanner(System.in);
        System.out.print("Lütfen kullanıcı adınızı giriniz: ");
        userName = input.nextLine();

        System.out.print("Lütfen şifrenizi giriniz: ");
        passWord = input.nextLine();

        if (userName.equals("patika")) {
            if (passWord.equals("dev")) {
                System.out.println("Sisteme başarılı bir şekilde giriş yaptınız.");
            } else {
                System.out.println("Hatalı şifre girişi !!!");
                System.out.print("Şifrenizi sıfırlamak ister misiniz? E/H : ");
                sifreCevap = input.next().charAt(0);

                if (sifreCevap == 'E') {

                    System.out.print("Lütfen yeni şifrenizi giriniz: ");
                    String newPassword = input.next();

                    if (newPassword.equals(passWord) || newPassword.equals("dev")) {
                        System.out.print("Şifre oluşturulamadı");
                    } else {
                        System.out.print("Şifre oluşturuldu.");
                    }
                } else if (sifreCevap == 'H') {
                    System.out.print("Şifre oluşturma işlemi iptal edildi..");

                } else {
                    System.out.print("Lütfen geçerli bir parametre giriniz. E (Evet) veya H (Hayır) !!!");
                }
            }
        } else {
            System.out.println("Hatalı kullanıcı adı girişi !!!");
        }
    }
}

```
### Pratik 8 - Sınıfı Geçme Durumu
Java koşullu ifadeler ile kullanıcının not durumuna göre sınıfı geçme durumunu hesaplayan program yapımı.Eğer girilen ders notları 0 veya 100 arasında değil ise ortalamaya katılmasın
```
import java.util.Scanner;
public class NotOrtalamasi {
    public static void main(String[] args) {
    int mat,fizik,kimya,turkce,muzik,dersSayisi=5;
    Scanner input=new Scanner(System.in);
        System.out.print("Matematik notunuzu giriniz = ");
        mat = input.nextInt();

        System.out.print("Fizik notunuzu giriniz = ");
        fizik = input.nextInt();

        System.out.print("Kimya notunuzu giriniz = ");
        kimya = input.nextInt();

        System.out.print("Türkçe notunuzu giriniz = ");
        turkce = input.nextInt();


        System.out.print("Müzik notunuzu giriniz = ");
        muzik = input.nextInt();
        if (mat < 0 || mat > 100) {
            mat = 0;
            dersSayisi--;
        }

        if (fizik < 0 || fizik > 100) {
            fizik = 0;
            dersSayisi--;
        }

        if (turkce < 0 || turkce > 100) {
            turkce = 0;
            dersSayisi--;
        }

        if (kimya < 0 || kimya > 100) {
            kimya = 0;
            dersSayisi--;
        }

        if (muzik < 0 || muzik > 100) {
            muzik = 0;
            dersSayisi--;
        }
         int toplam=mat+fizik+kimya+muzik+turkce;
         double ortalama= toplam/dersSayisi;



        if (ortalama<55 && ortalama>=0){
            System.out.println("Kaldınız.");

        }
        else if(ortalama >= 55 && ortalama <= 100){
            System.out.println("Geçtiniz");

        }
        else{
            System.out.println("Geçerli not giriniz.");
        }
        System.out.println("Ortalama :"+ortalama);
    }
}
```
### Pratik 9 - Hava Sıcaklıgına Göre Etkinlik
```
import java.util.Scanner;
public class HavaSicakligi {
    public static void main(String[] args) {
        int heat;

        Scanner input=new Scanner(System.in);
        System.out.print("Sıcaklık Giriniz: ");
        heat=input.nextInt();
        if (heat<5){
            System.out.println("Kayak yapabilirsiniz.");
        }
        else if(heat>=5 && heat<=25){
           if(heat<=15){
               System.out.println("Sinemaya gidebilirsiniz.");
           }
           if(heat>=10){
               System.out.println("Pikniğe gidebilirsiniz.");
           }

        }
        else {
            System.out.println("Yüzmeye gidebilirsiniz");
        }
    }
}
```
### Pratik 10 - Küçükten Büyüğe Sıralama

```
import java.util.Scanner;
public class KucuktenBuyuge {
    public static void main(String[] args) {
        int a,b,c;
        Scanner input=new Scanner(System.in);
        System.out.print("1.Sayı: ");
        a=input.nextInt();
        System.out.print("2.Sayı: ");
        b=input.nextInt();
        System.out.print("3.Sayı: ");
        c=input.nextInt();
        if ((a<b) && (a<c)){
            if (b<c){
                System.out.println("a<b<c");
            }
            else{
                System.out.println("a<c<b");
            }
        }
        else if((b<a) && (b<c)){
            if(a<c){
                System.out.println("b<a<c");
            }
            else{
                System.out.println("b<c<a");
            }
        }
        else{
            if(a<b){
                System.out.println("c<a<b");
            }
            else{
                System.out.println("c<b<a");
            }
        }

    }
}
```
### Pratik 11 - Burç Bulan Program
```
package Pratik11;

import java.util.Scanner;

public class BurcBulanProgram {
    public static void main(String[] args) {

        // Değişkenler oluşturuldu kullanıcıdan gün ve ay bilgisi istendi.
        int ay, gun;
        Scanner input = new Scanner(System.in);

        System.out.print("Kaçıncı ayda doğdunuz ? : ");
        ay = input.nextInt();

        System.out.print("Ayın kaçında doğdunuz ? : ");
        gun = input.nextInt();


        // SWTICH-CASE İLE ÇÖZÜM
        System.out.print("!!! SWITCH-CASE İLE ÇÖZÜM !!!\n");

        switch (ay){
            case 1:
                if(gun>=22){
                    System.out.println("Kova Burcu");
                } else {
                    System.out.println("Oğlak Burcu");
                }
                break;

            case 2:
                if(gun>=20){
                    System.out.println("Balık Burcu");
                } else {
                    System.out.println("Kova Burcu");
                }
                break;

            case 3:
                if(gun>=21){
                    System.out.println("Koç Burcu");
                } else {
                    System.out.println("Balık Burcu");
                }
                break;

            case 4:
                if(gun>=21){
                    System.out.println("Boğa Burcu");
                } else {
                    System.out.println("Koç Burcu");
                }
                break;

            case 5:
                if(gun>=22){
                    System.out.println("İkizler Burcu");
                } else {
                    System.out.println("Boğa Burcu");
                }
                break;

            case 6:
                if(gun>=23){
                    System.out.println("Yengeç Burcu");
                } else {
                    System.out.println("İkizler Burcu");
                }
                break;

            case 7:
                if(gun>=23){
                    System.out.println("Aslan Burcu");
                } else {
                    System.out.println("Yengeç Burcu");
                }
                break;

            case 8:
                if(gun>=23){
                    System.out.println("Başak Burcu");
                } else {
                    System.out.println("Aslan Burcu");
                }
                break;

            case 9:
                if(gun>=23){
                    System.out.println("Terazi Burcu");
                } else {
                    System.out.println("Başak Burcu");
                }
                break;

            case 10:
                if(gun>=23){
                    System.out.println("Akrep Burcu");
                } else {
                    System.out.println("Terazi Burcu");
                }
                break;

            case 11:
                if(gun>=22){
                    System.out.println("Yay Burcu");
                } else {
                    System.out.println("Akrep Burcu");
                }
                break;

            case 12:
                if(gun>=22){
                    System.out.println("Oğlak Burcu");
                } else {
                    System.out.println("Yay Burcu");
                }
                break;

            default:
                System.out.println("Lütfen ay için 1-12 arasında bir sayı giriniz. Gün için takvimden yardım alın. :)");
        }


        // IF ile ÇÖZÜM
        System.out.print("\n!!! IF İLE ÇÖZÜM !!!\n");

        System.out.print("Kaçıncı ayda doğdunuz ? : ");
        ay = input.nextInt();

        System.out.print("Ayın kaçında doğdunuz ? : ");
        gun = input.nextInt();

        if (ay == 1 && gun >= 22) {
            System.out.println("Kova Burcu");
        } else if (ay == 1){
            System.out.println("Oğlak Burcu");
        }

        if (ay == 2 && gun >= 20) {
            System.out.println("Balık Burcu");
        } else if (ay == 2){
            System.out.println("Kova Burcu");
        }

        if (ay == 3 && gun >= 21) {
            System.out.println("Koç Burcu");
        } else if (ay == 3){
            System.out.println("Balık Burcu");
        }

        if (ay == 4 && gun >= 21) {
            System.out.println("Boğa Burcu");
        } else if (ay == 4){
            System.out.println("Koç Burcu");
        }

        if (ay == 5 && gun >= 22) {
            System.out.println("ikizler Burcu");
        } else if (ay == 5){
            System.out.println("Boğa Burcu");
        }

        if (ay == 6 && gun >= 23) {
            System.out.println("Yengeç Burcu");
        } else if (ay == 6){
            System.out.println("ikizler Burcu");
        }

        if (ay == 7 && gun >= 23) {
            System.out.println("Aslan Burcu");
        } else if (ay == 7){
            System.out.println("yengeç Burcu");
        }

        if (ay == 8 && gun >= 23) {
            System.out.println("Başak Burcu");
        } else if (ay == 8){
            System.out.println("Aslan Burcu");
        }

        if (ay == 9 && gun >= 23) {
            System.out.println("Terazi Burcu");
        } else if (ay == 9){
            System.out.println("Başak Burcu");
        }

        if (ay == 10 && gun >= 20) {
            System.out.println("Akrep Burcu");
        } else if (ay == 10){
            System.out.println("Terazi Burcu");
        }

        if (ay == 11 && gun >= 20) {
            System.out.println("Yay Burcu");
        } else if (ay == 11){
            System.out.println("Akrep Burcu");
        }

        if (ay == 12 && gun >= 20) {
            System.out.println("Oğlak Burcu");
        } else if (ay == 12){
            System.out.println("Yay Burcu");
        }
    }
}

```
### ÖDEV 3 - Uçak Bileti Fiyatı Hesaplayan Program
Java ile mesafeye ve şartlara göre uçak bileti fiyatı hesaplayan programı yapın. Kullanıcıdan Mesafe (KM), yaşı ve yolculuk tipi (Tek Yön, Gidiş-Dönüş) bilgilerini alın. Mesafe başına ücret 0,10 TL / km olarak alın. İlk olarak uçuşun toplam fiyatını hesaplayın ve sonrasında ki koşullara göre müşteriye aşağıdaki indirimleri uygulayın ;

📌 Kullanıcıdan alınan değerler geçerli (mesafe ve yaş değerleri pozitif sayı, yolculuk tipi ise 1 veya 2) olmalıdır. Aksi takdirde kullanıcıya "Hatalı Veri Girdiniz !" şeklinde bir uyarı verilmelidir.

📌 Kişi 12 yaşından küçükse bilet fiyatı üzerinden %50 indirim uygulanır.

📌 Kişi 12-24 yaşları arasında ise bilet fiyatı üzerinden %10 indirim uygulanır.

📌 Kişi 65 yaşından büyük ise bilet fiyatı üzerinden %30 indirim uygulanır.

📌 Kişi "Yolculuk Tipini" gidiş dönüş seçmiş ise bilet fiyatı üzerinden %20 indirim uygulanır.
🔍 İpucu

```
Normal Tutar = Mesafe * 0.10 = 1500 * 0.10 = 150 TL
Yaş İndirimi = Normal Tutar * Yaş İndirim Oranı = 150 * 0.10= 15 TL
İndirimli Tutar = Normal Tutar – Yaş İndirimi = 150 – 15 = 135 TL
Gidiş Dönüş Bilet İndirimi = İndirimli Tutar * 0.20 = 135 * 0.20 = 27 TL
Toplam Tutar = (135-27)* 2 = 216 TL

```
```
import java.util.Scanner;
import java.text.DecimalFormat;

public class UcakBiletiFiyati {
    public static void main(String[] args) {

        double mesafe, yas, mUcret=0.10, nTutar, yIndirimi=0, iTutar, gdbIndirimi, tTutar;
        int yolTip;

       
        Scanner input = new Scanner(System.in);
        DecimalFormat df = new DecimalFormat("#.##");

        System.out.print("Mesafeyi km türünden giriniz : ");
        mesafe = input.nextInt();

        System.out.print("Yaşınızı giriniz : ");
        yas = input.nextInt();

        System.out.print("Yolculuk tipini giriniz (1 => Tek Yön , 2 => Gidiş Dönüş ): ");
        yolTip = input.nextInt();

        nTutar=mesafe*mUcret;

        if (yas < 12) {
            yIndirimi=nTutar*0.50;
        } else if (yas >=12 && yas <= 24){
            yIndirimi=nTutar*0.10;
        } else if (yas >= 65){
            yIndirimi=nTutar*0.30;
        }

        iTutar=nTutar-yIndirimi;

        switch (yolTip) {
            case 1:
                gdbIndirimi=iTutar*0;
                tTutar=iTutar-gdbIndirimi;
                System.out.print("\nToplam Tutar = " + df.format(tTutar) +" TL");
                break;

            case 2:
                gdbIndirimi=iTutar*0.20;
                tTutar=iTutar-gdbIndirimi;
                tTutar=tTutar*2;
                System.out.print("\nToplam Tutar = " + df.format(tTutar) +" TL");
                break;

            default:
                System.out.println("\nHatalı Veri Girdiniz !");
                break;
        }
    }
}


```
### ÖDEV 4 - Çin Zodyağı Hesaplama
Çin Zodyağı Hesaplayan Program

Java ile kullanıcıdan doğum tarihini alıp Çin Zodyağı değerini hesaplayan program yazınız.

🔍 Çin Zodyağı nedir?
4000 bin yıldır kullanılan bir astroloji çeşididir Çin astrolojisi ve insanları 12 değişik burç ve sembollerle tanımlar. Çin Zodyağı bu 12 burcun eşit aralıklarla(10 derece genişliğinde) sıralandığı bir hayvan halkasıdır ve yıldızlarla pek bir ilgisi yoktur.

📌 Çin Zodyağı nasıl hesaplanır? Çin zodyağı hesaplanırken kişinin doğum yılının 12 ile bölümünde kalana göre bulunur.

Doğum Tarihi %12 = 0 ➜ Maymun,
Doğum Tarihi %12 = 1 ➜ Horoz,
Doğum Tarihi %12 = 2 ➜ Köpek,
Doğum Tarihi %12 = 3 ➜ Domuz,
Doğum Tarihi %12 = 4 ➜ Fare,
Doğum Tarihi %12 = 5 ➜ Öküz,
Doğum Tarihi %12 = 6 ➜ Kaplan,
Doğum Tarihi %12 = 7 ➜ Tavşan,
Doğum Tarihi %12 = 8 ➜ Ejderha,
Doğum Tarihi %12 = 9 ➜ Yılan,
Doğum Tarihi %12 = 10 ➜ At,
Doğum Tarihi %12 = 11 ➜ Koyun.

```
import java.util.Scanner;

public class CinZodyagi {
    public static void main(String[] args) {
        int dYil, kalan;
        Scanner input = new Scanner(System.in);

        System.out.print("Doğum Yılınızı Giriniz : ");
        dYil = input.nextInt();

        kalan = dYil%12;

        if (kalan==0){
            System.out.print("Çin Zodyağı Burcunuz : Maymun");
        } else if (kalan==1){
            System.out.print("Çin Zodyağı Burcunuz : Horoz");
        }else if (kalan==2){
            System.out.print("Çin Zodyağı Burcunuz : Köpek");
        }else if (kalan==3){
            System.out.print("Çin Zodyağı Burcunuz : Domuz");
        }else if (kalan==4){
            System.out.print("Çin Zodyağı Burcunuz : Fare");
        }else if (kalan==5){
            System.out.print("Çin Zodyağı Burcunuz : Öküz");
        }else if (kalan==6){
            System.out.print("Çin Zodyağı Burcunuz : Kaplan");
        }else if (kalan==7){
            System.out.print("Çin Zodyağı Burcunuz : Tavşan");
        }else if (kalan==8){
            System.out.print("Çin Zodyağı Burcunuz : Ejderha");
        }else if (kalan==9){
            System.out.print("Çin Zodyağı Burcunuz : Yılan");
        }else if (kalan==10){
            System.out.print("Çin Zodyağı Burcunuz : At");
        }else if (kalan==11){
            System.out.print("Çin Zodyağı Burcunuz : Koyun");
        }
    }
}


```
