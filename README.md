package Beyblade;

import java.util.Scanner;

public class Test {

    public static void main (String [] args) {


        System.out.println("Beyblade PRogramına Hoşgeldiniz");
        System.out.println("Çıkış için Q ya basın.");

        Scanner scanner = new Scanner(System.in);

        while (true){

            System.out.println("Hangi Beyblade ? ");
            String islem = scanner.nextLine();
            if (islem.equals("q")) {

                System.out.println("Programdan çıkılıyor.");
                break;
            }
            else {

                BeybladeFabrikasi fabrika = new BeybladeFabrikasi();

                Beyblade beyblade = fabrika.beybladeUret(islem);

                if (beyblade == null) {

                    System.out.println("Lütfen Geçerli bir Beyblade ismi girin.!");

                }
                else {
                    beyblade.bilgileriGoster();
                    beyblade.saldiri();
                    beyblade.kutsalCanavarOrtayaCikar();


                }
            }

        }


    }

}
