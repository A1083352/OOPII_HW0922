# OOPII_HW0922_1
import java.util.*;
public class OOPII_HW0922_1 {
    public static void main(String[] args) {
        System.out.println("電腦從1～100的整數中,亂數取出10個不重複的號碼....");
        //TreeSet可以對集合中的元素進行指定順序的排序的功能，且不會重複
        TreeSet A = new TreeSet<>();
        TreeSet B = new TreeSet<>();
        //定義產生變數的名稱num
        int num=0;
        //亂數回傳十個不重複號碼，Math.random回傳隨機小數，所以須*100
        for(int k=1;k<=10;k++){
            num=(int)(Math.random()*100)+1;
            A.add(num);

            //設定亂數範圍
            if(num>30&&num<70){
                B.add(num);
            }
            System.out.println("第"+ k +"個號碼:"+num);
        }
        System.out.println("物件內元素個數為："+A.size());
        System.out.println("物件內元素的內容："+A);
        System.out.println("第一個元素內容為："+A.first());
        System.out.println("最後一個元素內容："+A.last());
        System.out.println("內容介於30～70者："+B);
    }

}
