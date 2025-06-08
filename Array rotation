import java.util.*;
public class Main
{
    static int[] rotate(int[] arr, int d){
        int[] temp=new int[arr.length];
        int k=0;
        for(int i=d;i<arr.length;i++){
            temp[k++]=arr[i];
        }
        for(int i=0;i<d;i++){
            temp[k++]=arr[i];
        }
        return temp;
    }
	public static void main(String[] args) {
		Scanner sc=new Scanner(System.in);
		System.out.println("enter the size of array:");
		int n=sc.nextInt();
		int[] arr=new int[n];
		for(int i=0;i<arr.length;i++){
		    System.out.print("enter the elements of array:");
		    int num=sc.nextInt();
		    arr[i]=num;
		}
		System.out.print("enter the rotate degree:");
		int d=sc.nextInt();
		int[] rot=rotate(arr,d);
		for(int i:rot){
		    System.out.print(i);
		}
		
	}
}
