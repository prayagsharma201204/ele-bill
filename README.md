import java.util.Scanner;
public class Assignment1
{
    public static void main(String args[]){
        double unit , billcal =0 , mtrcharge = 0 , netbill =0 ;
        boolean st =false;
        double s1 , s2 , s3 , s4 ;
        s1 = s2 = s3 = s4 = 0 ;
        Scanner x = new Scanner(System.in);
        System.out.println("-----Electricity Bill-----\n\n");
        System.out.print("Enter Your Name ---");
        String name = x.nextLine(); 
        System.out.print("Enter Units -- ");
        unit = Double.valueOf(x.next());
        if(unit>=0 && unit <=50){
            billcal = unit * 3.50;
            s1 = unit;
            mtrcharge = 0;
            st = true;
        } else  if(unit>=51 && unit <=150){
            billcal = (50 * 3.50) + (unit-50) * 4;
            s1 = 50 ;
            s2 = (unit-50);
            mtrcharge = 100;
            st = true;
        } else  if(unit>=151 && unit <=250){
            billcal = (50 * 3.50) + (100 * 4) + (unit-150) * 5.20;
            s1 = 50 ;
            s2 = 100;
            s3 = (unit-150);
            mtrcharge = 150;
            st = true;
        } else  if(unit>=251){
            billcal = (50 * 3.50) + (100 * 4) + (100 * 5.20) + (unit-250) * 6.50;
            s1 = 50 ;
            s2 = 100;
            s3 = 100;
            s4 = (unit-250);
            mtrcharge = 250;
            st = true;
        } else {
            System.out.println("/n/nYou Entered Invalid Units/n/n");
        } 
        if( st = true){
            netbill = billcal + mtrcharge;
            System.out.println("\n\nElectricity Bill Details \n\n");
            System.out.println("Name of Owner ---" + name);       
            System.out.println("Total Units --- " + unit + "\n");
            System.out.println("0-50 @3.50 X " + s1 + " = " + (s1 * 3.50) );
            System.out.println("51-150 @4.00 X " + s2 + " = " + (s2 * 4.00) );
            System.out.println("151-250 @5.20 X " + s3 + " = " + (s3 * 5.20));
            System.out.println("250 >  @6.50 X " + s4 + " = " + (s4 * 6.50) );
            System.out.println("Gross Unit Bill --- " + billcal + "\n");
            System.out.println("Meter Charge --- " + mtrcharge + "\n");
            System.out.println("-".repeat(50));
            System.out.println("Net Bill --- " + netbill + "\n");
            System.out.println("Thanks For Visit\n");
        }
    }
}
