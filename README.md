# Java_Kodluyoruz_101

Bu repo [Kodluyoruz](https://www.kodluyoruz.org/) Java 101 eğitimi için hazırlamış olduğum repo. İçerisinde Java pratiklerin,ödevlerinin soru ve cevaplarını içeren bir adet README dosyası barındırıyor.

|  PRATİKLER  |  ÖDEVLER |
|-----------|---------|
| [PRATİK 1]() - Not Ortalaması| [ÖDEV 1]() |

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
