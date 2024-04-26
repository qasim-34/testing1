# testing1
import java.util.Scanner;

public class IsoscelesTriangle {
    private double sideLength;
    public IsoscelesTriangle(double sideLength) {
        this.sideLength = sideLength;
    }

    public double findBase() {
        return Math.sqrt(sideLength * sideLength - (0.5 * sideLength) * (0.5 * sideLength));
    }

    public double findHeight() {
        return Math.sqrt(sideLength * sideLength - (findBase() * 0.5) * (findBase() * 0.5));
    }

    public double findArea() {
        return 0.5 * findBase() * findHeight();
    }

    public double findPerimeter() {
        return 2 * sideLength + findBase();
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter the length of the equal sides of the isosceles triangle: ");
        double sideLength = scanner.nextDouble();
        IsoscelesTriangle triangle = new IsoscelesTriangle(sideLength);
        
        System.out.println("Base of the triangle: " + triangle.findBase());
        System.out.println("Height of the triangle: " + triangle.findHeight());
        System.out.println("Area of the triangle: " + triangle.findArea());
        System.out.println("Perimeter of the triangle: " + triangle.findPerimeter());
    }
}
