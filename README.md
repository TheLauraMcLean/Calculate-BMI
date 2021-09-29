public class CalculateBMI {

    public static <DecimalFormat> void main(String[] args) {

        Scanner scan = new Scanner(in);

        out.print("Enter weight in kilograms: ");
        double weight = scan.nextDouble();

        out.print("Enter height in metres: ");
        double height = scan.nextDouble();

        double bmi = weight / (height * height);
        
        java.text.DecimalFormat tmt = new java.text.DecimalFormat("0.#");

        if (bmi < 18.5) {
            System.out.print("Your BMI is " + tmt.format(bmi) + ".0"+", which means you are in the Underweight range.");
        } else if (bmi >= 18.5 && bmi < 25.0) {
            System.out.print("Your BMI is " + tmt.format(bmi) +  ", which means you are in the Normal range.");
        } else if (bmi >= 25.0 && bmi < 30.0) {
            System.out.print("Your BMI is " + tmt.format(bmi) + ".0" + ", which means you are in the Overweight range.");
        } else if (bmi >= 30.0) {
            System.out.print("Your BMI is " + tmt.format(bmi) + ", which means you are in the Obese range.");

        }
    }
}
