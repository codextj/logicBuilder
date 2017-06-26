```
package javaapplication4;
import java.util.Scanner;
```

 * @author jarvisTJ*
 
```java
   public class JavaApplication4 {    
   
        public static void main(String[] args) {
        Scanner scan = new Scanner(System.in);
        int width= scan.nextInt();
        int printPyRows = width;
```

        
       // >find n req terms
       // >for input 2 req no. of terms to make pyramid is 3 ie 2+1
       // >for input 4 req no. of terms to make pyramid is 10 ie 4+3+2+1
        
 ```java    
        int numOfTerms=0;
        while(width>0)
        {       
        numOfTerms = numOfTerms + width;
        width -=1;}
 
 ```
      
        //at each loop width decreases by 1 ie as we go up the pyramid
        //System.out.println(numOfTerms);// for width==4 numOfTerms==10
        //now we have to generate numOfTerms
        
 ```java
        int k=2;
        int i=-1;
        String terms;
        String []strPyramid = new String [numOfTerms];
        
        while(numOfTerms>0)
        {
            numOfTerms-=1;
            terms=""+(k*(2*k-1));
        
            //apply padding if needed
            if(terms.length()<5){
            int diff = 5-terms.length();
            while(diff>0){
              String padding ="0";
              terms = padding+terms;
              diff-=1;
            }
            }
 ```
           saving terms in an array
   ```java
          i++;
          strPyramid[i]=terms;
   ```        
             to generate next term in series
             
         ```java    
               k+=2;}
         ```    
             generate Pyramid
            ```java 
                   int nums=0;
                   for(int xi=0;xi<printPyRows;xi++) 
                   {
                        for(int yj=0;yj<printPyRows-xi;yj++)
                        {
                           System.out.print("   "); 
                        }
                  
                        for(int zk=0;zk<=xi;zk++) 
                        {
                           System.out.print(strPyramid[nums]+" ");
                           nums++;
                        }
                    System.out.println();  
                      }       
                    }    
                   }
            ```
