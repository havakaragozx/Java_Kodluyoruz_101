# Java_Kodluyoruz_101

Bu repo [Kodluyoruz](https://www.kodluyoruz.org/) Java 101 eğitimi için hazırlamış olduğum repo. İçerisinde Java pratiklerin,ödevlerinin soru ve cevaplarını içeren bir adet README dosyası barındırıyor.

|  PRATİKLER  |  ÖDEVLER |
|-----------|---------|
| [PRATİK 1](https://github.com/havakaragozx/Java_Kodluyoruz_101/blob/main/README.md#pratik-1---not-ortalamas%C4%B1) - Not Ortalaması| [ÖDEV 1](https://github.com/havakaragozx/Java_Kodluyoruz_101/blob/main/README.md#%C3%B6dev-1---v%C3%BCcut-kitle-indeksi-hesaplama) - Vücut Kitle Indeksi Hesaplama|
| [PRATİK 2](https://github.com/havakaragozx/Java_Kodluyoruz_101/blob/main/README.md#pratik-2---kdv-tutar%C4%B1) - Kdv Tutarı | [ÖDEV 2](https://github.com/havakaragozx/Java_Kodluyoruz_101/blob/main/README.md#%C3%B6dev-2--manav-kasa-program%C4%B1) - Manav Kasa Programı |
| [PRATİK 3](https://github.com/havakaragozx/Java_Kodluyoruz_101/blob/main/README.md#pratik-3---alan-hesaplama) - Alan Hesaplama |
|[PRATİK 4](https://github.com/havakaragozx/Java_Kodluyoruz_101/blob/main/README.md#pratik-4---taksimetre-hesaplama) - Taksimetre Hesaplama |
|[PRATİK 5](https://github.com/havakaragozx/Java_Kodluyoruz_101/blob/main/README.md#prati%CC%87k-5---alan-hesaplama) - Alan Hesaplama |
|[PRATİK 6](https://github.com/havakaragozx/Java_Kodluyoruz_101/blob/main/README.md#pratik-6---hesap-makinesi) - Hesap Makinesi|
|[PRATİK 7]() - Kullanıcı Girişi|
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
