# Arrays-EasyQuestions

question 1.
//check array sorted or not 

-->
package RecursionArrayQ;

public class CheckSortArr {
    public static void main(String[]args){
int []arr={1,2,3,4,10,6,7,9};
        System.out.println(sorted(arr,0));

    }
    static Boolean sorted(int[] num,int index){
        if(index==num.length-1){
            return true;
        }
return num[index]<num[index+1] && sorted(num,index+1);

    }
}



---------------------
question-2
//Linear search in array
----->
package RecursionArrayQ;

public class LinearSearch {
    public static void main(String[]args){
        int []arr={1,2,3,4,10,6,7,9};
        int target=10;
                System.out.println(linearSearchArr(arr,target,0));
                int ans =linearSearchA(arr,target,0);
                System.out.println(ans);
        
            }
            static Boolean linearSearchArr(int[]arr,int target,int index){
                if(index==arr.length){
                    return false;
                }
                return (arr[index]==target) || linearSearchArr(arr,target,index+1);
            }

            static int linearSearchA(int[]arr,int target,int index){
                if(index==arr.length){
                    return -1;
                }
                if(arr[index]==target)
                {
                    return index;
                }
                return linearSearchA(arr,target,index+1);
            }}
            
            
       ----------------------------
  question 3-
  
  Binary Search in array 
  
  --->>
  
public class BinarySearch {
    public static void main(String[]args)
    {
        int []arr={1,2,5,8,14,19,32,55};
        int target=19;
        int index=binary(arr,target,0,arr.length-1);
        System.out.println(index);
    }
    static int binary(int[]arr,int target,int s,int e)
    {
        
        if(s>e){
            return -1;
        }
        int m=s+(e-s)/2;
        if(arr[m]==target){
            return m;
        }
        if(arr[m]>target){
            return binary(arr,target,s,m-1);

        }
        
    return binary(arr,target,m+1,e); }}


