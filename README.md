# ORIENTED OBJECT PROGRAMMING


### Superclass dari BangunDatar
        //Membuat Superclass BangunDatar
        public class BangunDatar {

            public void luas(){
                System.out.println("Luas dari Bangun Datar");
            }

            public void keliling(){
                System.out.println("Keliling dari Bangun Datar");
            }
        }


### Subclass Lingkarn
        //Subclass Lingkaran
        public class Lingkaran extends BangunDatar {

            //Memasukan Atribut Private
            private int r;

            //Menambahkan Setter & Getter
            public void setR(int r) {
                this.r = r;
            }
            public int getR() {
                return r;
            }

            //Method dengan nilai pengembalian float
            public float luas(int r) {
                return (float) (3.14 * r * r);
            }

            public float keliling(int r){
                return (float) (2 * 3.14 * r);
            }
        }


### Subclass Segitiga
        //Subclass Segitiga
        public class Segitiga extends BangunDatar{

            //Membuat atribut private
            private int alas;
            private int tinggi;
            private int sisi;


            //Memasukan Setter & Getter
            public void setAlas(int alas) {
                this.alas = alas;
            }

            public int getAlas() {
                return alas;
            }

            public void setTinggi(int tinggi) {
                this.tinggi = tinggi;
            }
            public int getTinggi() {
                return tinggi;
            }

            public void setSisi(int sisi) {
                this.sisi = sisi;
            }

            public int getSisi() {
                return sisi;
            }

            //Method dengan nilai pengembalian float
            public float luas(int alas, int tinggi){
                return (float) (0.5 * alas * tinggi);
            }

            public float keliling(int sisi){
                return (float) (3 * sisi);
            }

        }


### Subclass Persegi
        //Subclass Persegi
        public class Persegi extends BangunDatar {

            //Membuat attribut private
            private int sisi;

            //Memasukkan Setter & Getter
            public void setSisi(int sisi) {
                this.sisi = sisi;
            }
            public int getSisi() {
                return sisi;
            }

            //Method dengan nilai pengembalian float
            public float luas(int sisi){
                return (float) (sisi * sisi);
            }

            public float keliling(int sisi){
                return (float) (4 * sisi);
            }
        }


### Class Main
        //Membuat Class Main
        public class Main {
            public static void main(String[] args){

                //Memasukan objek ke subclass
                Lingkaran lingkaran1 = new Lingkaran();
                Segitiga segitiga1 = new Segitiga();
                Persegi persegi1 = new Persegi();

                //Memasukan nilai ke objek dan menampilkannya
                System.out.println("\nLuas Lingkaran: " + lingkaran1.luas(10));
                System.out.println("Keliling Lingkaran: " + lingkaran1.keliling(10));
                System.out.println("\nLuas Segitiga: " + segitiga1.luas(10,15));
                System.out.println("Keliling Segitiga: " + segitiga1.keliling(10));
                System.out.println("\nLuas Persegi: " + persegi1.luas(8));
                System.out.println("Keliling persegi: " + persegi1.keliling(8));

            }
        }


![Screenshot (14)](https://user-images.githubusercontent.com/115928747/201391216-d1c3d531-0be2-412a-874e-0bb97691ff24.png)

