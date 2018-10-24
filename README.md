# volumeCode
volume code 
/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */
package chunk2methods;

import java.util.Scanner;
import java.lang.Math;
/**
 *
 * @author jeremy.carpenter
 */
public class GeometricShapes {
    public static void main(String[] args) {
       //guts 
        //double returnedVolume = calcVolumeOfCube(50.0);
        //System.out.println("Volume of a cube: " + returnedVolume);
        System.out.println("Please enter the side "
                + "length of the cube to calculate its volume: ");
         Scanner myScanner = new Scanner(System.in);
         Double userInput = myScanner.nextDouble();
        System.out.println("The volume of a cube with a side length of " 
                + userInput +" is " + calcVolumeOfCube(userInput));
        calcVolumeOfCylinder();
        calcVolumeOfOctagon();
    }//end main
    
    public static double calcVolumeOfCube(double sideLength){
        //guts
        double cubeVolume = Math.pow(sideLength, 3);
        return cubeVolume;
    }//end VolumeOfCube
    
    public static double calcVolumeOfCylinder(){
        final double PI = 3.1416;
        System.out.println("Enter the radius value for the cylinder.");
         Scanner myScanner = new Scanner(System.in);
         double userInput = myScanner.nextDouble();
         double radius = userInput;
         System.out.println("Enter the height for the cylinder.");
         double height = myScanner.nextDouble();
         double cylVol = PI * (radius * radius) * height;
         
         System.out.println("The volume of a cylinder with radius: " + radius + 
                 " and height of " + height + " is " + cylVol);
        return 1;
    }
    
    public static double calcVolumeOfOctagon(){
        final double sqrt2 = Math.sqrt(2);
        
        System.out.println("Enter the length for one side of your 3-Dimensional "
                + "Octagon: ");
        Scanner myScanner = new Scanner(System.in);
        double userInput = myScanner. nextDouble();
        double sideLength = userInput; 
        System.out.println("Enter the height of the Octagon :");
        double height = myScanner.nextDouble();
        double octVol= 2 * (1 + sqrt2) * (sideLength * sideLength) * height ;
        System.out.println("The volume of an Octagon with a side length of: " 
                + sideLength + " and a height of " + height + " is " + octVol);
        
        
        
        return 1;
    } 
    
}
