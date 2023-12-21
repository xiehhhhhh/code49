# code49
package zfcpx;
import java.util.Arrays;
import java.util.Scanner;
   
public class zfcpx {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.println("请输入一个包含数值的字符串：");
        String input = scanner.nextLine();
        String[] strArray = input.split(" ");
        Integer[] intArray = new Integer[strArray.length];

        // 转换字符串数组为整型数组
        for (int i = 0; i < strArray.length; i++) {
            intArray[i] = Integer.parseInt(strArray[i]);
        }

        // 对整型数组进行排序
        Arrays.sort(intArray);

        // 使用StringBuffer将排序后的整型数组转换回字符串
        StringBuffer output = new StringBuffer();
        for (int i = 0; i < intArray.length; i++) {
            output.append(intArray[i]);
            if (i < intArray.length - 1) {
                output.append(" ");
            }
        }

        System.out.println("排序后的字符串为：" + output.toString());
    }
}
