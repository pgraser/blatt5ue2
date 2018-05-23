# blatt5ue2
```
public class Program
    {
        public static void Main(string[] args)
        {
            int[] arr = CalcCumSum(new int[] {5, 23, 7, 1, -14, 15, -8}, 4);

            foreach(var number in arr)
            {
                Console.Write(number + " ");
            }
            Console.ReadKey();
        }

        public static int[] CalcCumSum(int[] workArray, int i)
        {
            if (i == 0)
            {
                return workArray;
            }
            else
            {
                int[] newArray = (int[])workArray.Clone();

                for(int j = 0; j<i; j++)
                {
                    newArray[i] += workArray[j];
                }

                return CalcCumSum(newArray, i - 1);
            }
        }
    }
    ```
