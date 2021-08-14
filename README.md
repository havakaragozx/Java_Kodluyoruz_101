# Java_Kodluyoruz_101

Bu repo [Kodluyoruz](https://www.kodluyoruz.org/) Java 101 eğitimi için hazırlamış olduğum repo. İçerisinde Java pratiklerin,ödevlerinin soru ve cevaplarını içeren bir adet README dosyası barındırıyor.

|  PRATİKLER  |  ÖDEVLER |
|-----------|---------|
| [PRATİK 1](https://github.com/havakaragozx/Java_Kodluyoruz_101/blob/main/README.md#pratik-1---not-ortalamas%C4%B1) - Not Ortalaması| [ÖDEV 1]() |
| [PRATİK 2](https://github.com/havakaragozx/Java_Kodluyoruz_101/blob/main/README.md#pratik-2---kdv-tutar%C4%B1) - Kdv Tutarı | [ÖDEV 2]() |
| [PRATİK 3](https://github.com/havakaragozx/Java_Kodluyoruz_101/blob/main/README.md#pratik-3---alan-hesaplama) - Alan Hesaplama |
|[PRATİK 4](https://github.com/havakaragozx/Java_Kodluyoruz_101/blob/main/README.md#pratik-4---taksimetre-hesaplama) - Taksimetre Hesaplama |
|[PRATİK 5](https://github.com/havakaragozx/Java_Kodluyoruz_101/blob/main/README.md#prati%CC%87k-5---alan-hesaplama) - Alan Hesaplama |
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
### PRATİK 5 - Alan Hesaplama
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

### ÖDEV 1 - VUCUT KİTLE İNDEKSİ HESAPLAMA
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
