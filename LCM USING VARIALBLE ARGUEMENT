class Demo1{
    int gcd(int num1, int num2){
        while(num2>0){
            int temp=num2;
		    num2=num1%num2;
		    num1=temp;
        }
        return num1;
    }
    void lcm(int... num){
        int l=num[0];
        for(int i=1;i<num.length;i++){
            l=l*num[i]/gcd(l,num[i]);
        }
        System.out.println(l);
    }
}
public class Main
{
	public static void main(String[] args) {
		Demo1 dem=new Demo1();
		dem.lcm(15,10);
		dem.lcm(4,6,24,40);
		dem.lcm(8,24,15,30,36);
	}
}
