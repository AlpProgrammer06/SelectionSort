```
package com.company;

public class Main {

    public static void main(String[] args) {
        int counter = 0;
        int[] dizi = new int[5];

        for (int i = 0; i < dizi.length; i++) {
            dizi[i] = (int) (Math.random() * 21);
        }
            for (int i = 0; i < dizi.length; i++) {
                System.out.print( dizi[i]+ ",");

            }
        System.out.println();


    //    1   5   3   7   9
        for (int i = 0; i < dizi.length; i++) {
            int enkucuk=dizi[i];
            int enkuckyer=i;
            for (int j = i+1; j < dizi.length; j++) {
                if(dizi[j]<enkucuk){
                    enkucuk=dizi[j];    // dizi[j]=3   enküçük =3
                    enkuckyer=j;       //  enküçükyer=2
                }
                counter++;
            }

            int temp=dizi[i];
            dizi[i]=dizi[enkuckyer];
            dizi[enkuckyer]=temp;
        }
        for (int i = 0; i < dizi.length; i++) {
            System.out.print(dizi[i]+ ",");

        }



    }
}


```