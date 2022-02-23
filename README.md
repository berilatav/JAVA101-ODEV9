Kullanıcı Giriş Sistemi

Eğer şifre yanlış ise kullanıcıya şifresini sıfırlayıp sıfırlamayacağını sorun, eğer kullanıcı sıfırlamak isterse yeni girdiği şifrenin hatalı girdiği ve unuttuğu şifre ile aynı olmaması gerektiğini kontrol edip , şifreler aynı ise ekrana "Şifre oluşturulamadı, lütfen başka şifre giriniz." sorun yoksa "Şifre oluşturuldu" yazan programı yazınız.

import java.util.Scanner;

public class Odev9 {

    public static void main(String[] args) {

        String userName, password;
        int select;

        Scanner input = new Scanner(System.in);
        System.out.println("Kullanıcı adınızı giriniz: ");
        userName = input.nextLine();

        System.out.println("Şifrenizi giriniz: ");
        password = input.nextLine();

        if (userName.equals("berilatav") && password.equals("mavi")) {
            System.out.println("Giriş yaptınız.");
        }
        else {
            System.out.println("Bilgileriniz yanlış girdiniz. Yeni bir şifre oluşturmak ister misiniz ?");
            System.out.println("Şifrenizi sıfırlamak için 1'e basınız.");
            System.out.println("Yeni bir şifre oluşturmak istemiyorsanız 2'ye basınız.");
            System.out.print("Seçiminiz : ");

            select = input.nextInt();

            switch (select) {
                case 1:
                    System.out.println("Lütfen yeni bir şifre oluşturunuz.");
                    System.out.print("Şifreniz : ");

                    Scanner input2 = new Scanner(System.in);
                    password = input2.nextLine();

                    if (password.equals("mavi")) {
                        System.out.println("Yeni şifreniz eskisiyle aynı olamaz ! ");
                    } else {
                        System.out.println("Yeni şifreniz oluşturuldu. ");
                    }
                    break;
                case 2:
                    System.out.println("Tekrar deneyiniz !");
                    break;
            }


        }

    }

}

