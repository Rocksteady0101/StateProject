import java.util.Scanner;
import java.util.Arrays;

public class Main {
  public static void main(String[] args) {
  String[][] capitals = {
      {"Alabama", "Montgomery"},
      {"Alaska", "Juneau"},
      {"Arizona", "Phoenix"},
      {"Arkansas", "Little Rock"},
      {"California", "Sacramento"},
      {"Colorado", "Denver"},
      {"Connecticut", "Hartford"},
      {"Delaware", "Dover"},
      {"Florida", "Tallahassee"},
      {"Georgia", "Atlanta"},
      {"Hawaii", "Honolulu"},
      {"Idaho", "Boise"},
      {"Illinois", "Springfield"},
      {"Indiana", "Indianapolis"},
      {"Iowa", "Des Moines"},
      {"Kansas", "Topeka"},
      {"Kentucky", "Frankfort"},
      {"Louisiana", "Baton Rouge"},
      {"Maine", "Augusta"},
      {"Maryland", "Annapolis"},
      {"Massachusetts", "Boston"},
      {"Michigan", "Lansing"},
      {"Minnesota", "Saint Paul"},
      {"Mississippi", "Jackson"},
      {"Missouri", "Jefferson City"},
      {"Montana", "Helena"},
      {"Nebraska", "Lincoln"},
      {"Nevada", "Carson City"},
      {"New Hampshire", "Concord"},
      {"New Jersey", "Trenton"},
      {"New Mexico", "Santa Fe"},
      {"New York", "Albany"},
      {"North Carolina", "Raleigh"},
      {"North Dakota", "Bismarck"},
      {"Ohio", "Columbus"},
      {"Oklahoma", "Oklahoma City"},
      {"Oregon", "Salem"},
      {"Pennsylvania", "Harrisburg"},
      {"Rhode Island", "Providence"},
      {"South Carolina", "Columbia"},
      {"South Dakota", "Pierre"},
      {"Tennessee", "Nashville"},
      {"Texas", "Austin"},
      {"Utah", "Salt Lake City"},
      {"Vermont", "Montpelier"},
      {"Virginia", "Richmond"},
      {"Washington", "Olympia"},
      {"West Virginia", "Charleston"},
      {"Wisconsin", "Madison"},
      {"Wyoming", "Cheyenne"}
  };

    int n = capitals.length;
    int counter = 0;

    for (int i = 0; i < n-1; i++) {
                for (int j = 0; j < n - i - 1;  j++){

      if(capitals[j][1].compareTo(capitals[j+1][1]) > 0){
                        String[] temp = capitals[j];
                        capitals[j] = capitals[j + 1];
                        capitals[j + 1] = temp;
                    }
                }
             }

for (int i = 0; i < capitals.length; i++){
  System.out.print(" "+capitals[i][0]+" "+capitals[i][1]);
  };
  
           
  int k = 0;

  Scanner scanner = new Scanner(System.in);

    while (k < n) {
        System.out.print("What is the capital of " + capitals[k][0]);
        String city = scanner.next();

        if (city.equalsIgnoreCase(capitals[k][1])) {
            counter++;
        }
        k++;
    }
System.out.print(counter+" / 50 right");
}
}
