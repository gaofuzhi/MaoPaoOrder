# MaoPaoOrder

package test;
/*
 * 冒泡排序：
 * 相邻两个数进行比较，升序放大的再后面，降序放小的在后面
 * 与所有的数进行一次比较，叫一轮(外循环)
 * 轮数为：Y==X-1;(X为总数)
 * 每轮比较的次数为：Z==X-第几轮-1(内循环)
 */
public class MaoPao {
	public static void main(String[] args) {
		double mid=0;
		double[] arr = new double[]{5,3,8,9,5,5,6,5,55,2,1};
		for(int i=0;i<arr.length;i++){
			for(int j=0;j<arr.length-i-1;j++){
				//if it is '<' ,降序;反之,升序
				if(arr[j]<arr[j+1]){
					mid = arr[j+1];
					arr[j+1] = arr[j];
					arr[j] = mid;
				}
			}
		}
		for(int k=0;k<arr.length;k++){
			System.out.println(arr[k]+"\t");
		}	
	}
}
