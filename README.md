package arbolito;

public class Arbolito {

    public static void main(String[] args) throws InterruptedException {
        int ran, color = 0, n = 10;
        while (true) {
            for (int i = 0; i < n + (n / 2); i++) {
                for (int j = n + (n / 2); j > i; j--) {
                    System.out.print(" ");
                }
                for (int k = 1; k <= 2 * i - 1; k++) {
                    ran = (int) (Math.random() * 101) + 1;
                    if (ran % 10 == 0) {
                        System.out.print("\033[34m*");
                    } else {
                        System.out.print("\033[32m*");
                    }

                }
                System.out.println("");
            }
            for (int i = 1; i < n - (n / 2); i++) {
                for (int j = n + (n / 2); j > 1; j--) {
                    System.out.print(" ");

                }
                System.out.println("\033[31m**");
            }
            Thread.sleep(1000);
            System.out.print("\033[H033[2J");
            System.out.flush();
            
            

        }
    }

}
