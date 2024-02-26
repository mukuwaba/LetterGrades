//LetterGrades.java
//LetterGrades class uses the switch statement to count letter grades
import java.util.Scanner;
public class LetterGrade {
    public static void main(String[] args) {
        int total = 0; //sum of grades
        int gradeCounter = 0;// number of grades entered
        int aCount = 0;//count of a grades
        int bCount =0;//count of B grades
        int cCount =0;//count of C grades
        int dCount =0;//count of D grades
        int eCount =0;//count of E grades
        int fCount =0;//count of F grades

        Scanner input = new Scanner(System.in);

        System.out.printf("%s%n%s%n  %s%n    %s%n",
                "Enter the integer grades in the range 0-100.",
                "Type the end-of-file indicator to terminate input:",
                "On UNIX/Linux/macOS type <Ctrl> d then press Enter",
                "On Windows type <Ctrl> z then press Enter");

        //loop until user eneters the end-of-file indicator
        while (input.hasNext()){
            int grade = input.nextInt();//read grade
            total += grade;//add grade to total
            ++gradeCounter;//increment number of grade

            //increment appropriate letter-grade counter
            switch (grade/10) {
                case 9://grade was between 90
                case 10: //and 100, inclusive
                    ++aCount;
                    break;
                case 8://grade was between 80 and 89
                    ++bCount;
                    break;
                case 7://grade was between 70 and 79
                    ++cCount;
                    break;//exits switch
                case 6://grade was between 60 and 69
                    ++dCount;
                    break; //exits switch
                default://grade was less than 60
                    ++fCount;
                    break; //optinal; exits switch anyway
                        
            }
        }
            
        //display grade report
        System.out.printf("%nGrade report: %n);
                
                //if user enetered at least one grade...
                if (gradeCounter != 0){
                    //calculate average of all grades enetered
                    double average = (double) total / gradeCounter;
                    //output summary of results
        System.out.printf("Total of the %d grades enetered is %d%n",
                gradeCounter, total);
        System.out.printf("Class average is %.2f%n", average);
        System.out.printf("%n%s%n%"
        )
        }
                
                
                



    }//main
}//LetterGrade
