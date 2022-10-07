### Task 8 kyu

[Task link](https://www.codewars.com/kata/5ae62fcf252e66d44d00008e/)

Given three integers a ,b ,c, return the largest number obtained after inserting the following operators and brackets: +, *, ()
In other words , try every combination of a,b,c with [*+()] , and return the Maximum Obtained

### My solution

```Java

public class Kata
{
    public static int expressionsMatter(int a, int b, int c)
    {
        int e = Math.max(a*b*c, a+b+c);
        int f = Math.max(a*(b+c), (a+b)*c);
        int g = Math.max(a*b+c,a+b*c);

        int h = Math.max(e,f);
        int k = Math.max(h,g);

        int j = Math.max(h,k);

        return j;

    }

```

### Favourite solution from code-wars

```Java

public class Kata
{
    public static int expressionsMatter(int a, int b, int c)
    {

        int[] myArray = {a+b+c, a*b*c, a+b*c, a*b+c, (a+b)*c, a*(b+c)};
        int max = 0;
        for(int i = 0; i<myArray.length; i++ ){
            if(myArray[i] > max ){
                max = myArray[i];
            }
        }
        return max;
    }
}

```

Using array at this task so unpredictable, I like this idea!

# Have a nice day!