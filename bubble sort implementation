public class Main
{
    static void bubble(int n,int[] nums){
        int temp;
        for(int i=0;i<n;i++){
            for(int j=0;j<n-i;j++){
                if(nums[j]>nums[j+1]){
                    temp=nums[j+1];
                    nums[j+1]=nums[j];
                    nums[j]=temp;
                }
            }
        }
    }
	public static void main(String[] args) {
		int[] nums={2,3,12,56,6,34,99,102,32};
		bubble(8,nums);
		for(int a:nums){
		    System.out.print(a+" ");
		}
	}
}
