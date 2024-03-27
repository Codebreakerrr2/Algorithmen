# Algorithmen
/******************************************************************************

                            Online Java Compiler.
                Code, Compile, Run and Debug java program online.
Write your code in this editor and press "Run" button to execute it.

*******************************************************************************/

public class Main
{
	public static void main(String[] args) {
	    int[] array={0,1,2,3,4,5,6,7,8,9,10};
	   System.out.print(binarysearch(10,11,array));
		
	}
	private static boolean binarysearch(int x,int y, int firstIndex, int[] array){
	    
	    
	    /// länge prüfen ob man es überhaupt teilen kann.
	    if(y-firstIndex==1){
	        if(array[firstIndex]==x) return true;
	        return false;
	    }
	    
	   //\\Ende
	   
	   ///länge auf gerade und ungerade prüfen, bestimmt wie die teilarrays dann behandelt werden sollen
	   
	   /// falls die länge eine gerade Zahl ist
	   if(y%2==0){
	       int arrayMitte= (firstIndex+y)/2;
	       
	       /// prüfen ob die mitte der Array unser gesuchte Zahl ist.
	       if(array[arrayMitte]==x) return true;
	      
	       /// prüfen ob die die Zahl kleiner als die mitte der Array ist.
	       if(x<array[arrayMitte]){
	           
	           int TeilArrayLaenge=arrayMitte;
	           int newFirstIndex = arrayMitte-(arrayMitte/2);
	           return binarysearch(x,TeilArrayLaenge,newFirstIndex,array);
	           
	       }
	       /// prüfen ob die Zahl großer als die mitte der Array ist.
	       else{
	            int TeilArrayLaenge=arrayMitte+((arrayMitte/2)+1);
	            int newFirstIndex = arrayMitte+1;
	           return binarysearch(x,TeilArrayLaenge,newFirstIndex,array);
	           
	       }
	       
	       
	   }
	   
	   /// falls die länge eine ungerade Zahl ist
	   else{
	         int arrayMitte= (firstIndex+y)/2;
	       
	       /// prüfen ob die mitte der Array unser gesuchte Zahl ist.
	       if(array[arrayMitte]==x) return true;
	      
	       /// prüfen ob die die Zahl kleiner als die mitte der Array ist.
	       if(x<array[arrayMitte]){
	           
	           int TeilArrayLaenge=arrayMitte;
	           int newFirstIndex = arrayMitte-(arrayMitte/2);
	           return binarysearch(x,TeilArrayLaenge,newFirstIndex,array);
	           
	       }
	       /// prüfen ob die Zahl großer als die mitte der Array ist.
	       else{
	            int TeilArrayLaenge=arrayMitte+((arrayMitte/2));
	            int newFirstIndex = arrayMitte+1;
	           return binarysearch(x,TeilArrayLaenge,newFirstIndex,array);
	           
	       
	       
	       
	       
	   }
	   
	    
	}}
	public static boolean binarysearch(int x,int y, int[] array){
	  return  binarysearch(x,y,0,array);
}
    
}
	    
	
    

