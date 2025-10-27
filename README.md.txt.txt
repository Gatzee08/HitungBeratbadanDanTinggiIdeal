## Program Menghitung Berat Badan Ideal (BMI)

Program ini dibuat menggunakan bahasa pemrograman **Java** untuk menghitung **Body Mass Index (BMI)** dan menentukan kategori berat badan seseorang berdasarkan tinggi dan berat badan.

---

## 🧮 Fungsi Program
- Menginput berat badan (kg)
- Menginput tinggi badan (cm)
- Menghitung BMI menggunakan rumus:
- Menampilkan kategori berat badan:
  - Kurang (Underweight)
  - Ideal (Normal)
  - Berlebih (Overweight)
  - Obesitas

- Memberikan informasi berapa kg yang perlu ditambah atau diturunkan untuk mencapai kategori ideal

---

## 📌 Kategori BMI yang Digunakan
| BMI | Kategori |
|-----|----------|
| < 18.5 | Berat badan kurang |
| 18.5 - 24.9 | Berat badan ideal |
| 25 - 29.9 | Berat badan berlebih |
| ≥ 30 | Obesitas |

---

## ✅ Contoh Output
import java.util.Scanner;

public class HitungBeratBadanIdeal {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

        System.out.println("=== Program Menghitung Berat Badan Ideal ===");
        System.out.print("Masukkan berat badan Anda (kg): ");
        double berat = input.nextDouble();

        System.out.print("Masukkan tinggi badan Anda (cm): ");
        double tinggi = input.nextDouble();

        // Mengubah tinggi ke meter
        double tinggiMeter = tinggi / 100;

        // Rumus BMI
        double bmi = berat / (tinggiMeter * tinggiMeter);

        System.out.println("\n=== Hasil Perhitungan ===");
        System.out.printf("BMI Anda: %.2f\n", bmi);

        // Menentukan kategori BMI
        if (bmi < 18.5) {
            double idealMin = 18.5 * tinggiMeter * tinggiMeter;
            double perluNaik = idealMin - berat;
            System.out.printf("Berat badan Anda kurang. Anda perlu menambah sekitar %.1f kg.\n", perluNaik);
        } else if (bmi >= 18.5 && bmi <= 24.9) {
            System.out.println("Selamat! Berat badan Anda ideal.");
        } else if (bmi >= 25 && bmi <= 29.9) {
            double idealMax = 24.9 * tinggiMeter * tinggiMeter;
            double perluTurun = berat - idealMax;
            System.out.printf("Berat badan Anda berlebih. Anda perlu menurunkan sekitar %.1f kg.\n", perluTurun);
        } else {
            double idealMax = 24.9 * tinggiMeter * tinggiMeter;
            double perluTurun = berat - idealMax;
            System.out.printf("Anda termasuk obesitas! Anda perlu menurunkan sekitar %.1f kg.\n", perluTurun);
        }

        input.close();
    }
}

---

## 💡 Catatan
- Hasil BMI hanya estimasi, tidak mempertimbangkan massa otot atau faktor kesehatan lain
- Cocok digunakan untuk pembelajaran dasar Java (Scanner, kondisi if-else, input-output)

---

## 👤 Pembuat
Nama: *[Muhammad Gatot Prasetia]*  
Kelas / Mata Kuliah: *[H / Pemrograman Lanjut]*

---

Terima kasih telah menggunakan program ini! 💪✨
