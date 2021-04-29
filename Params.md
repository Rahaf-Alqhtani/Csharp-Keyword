# Params
<div dir=rtl alainy=right>هذا التعريف يحدد معامل الداله التي لديها عددمن معاملات المتغيرات . حيث انه يجب ان يكون نوع مصفوفة المعاملات احادية الابعاد.<br>لايمكن اعادة تعريف معاملات بعد هذا التعريف  وقت تعريف دالة ونكتفي فقط بتعريف واحد لجميع المعاملات .</div><br>
<div dir=rtl alainy=right> عند استدعاء دالة مع هذا التعريف  يجب مراعاة التالي:<br>
1.  كتابة فاصلة بين عناصر المصفوفة<br>
2. تحديد نوع  مصفوفة المعاملات .<br>
3. في حال عدم وجود معاملات لهذة المصفوفة فان طول التعريف يساوي 0.</div><br>

```
public class MyClass
{
    public static void UseParams(params int[] list)
    {
        for (int i = 0; i < list.Length; i++)
        {
            Console.Write(list[i] + " ");
        }
        Console.WriteLine();
    }

    public static void UseParams2(params object[] list)
    {
        for (int i = 0; i < list.Length; i++)
        {
            Console.Write(list[i] + " ");
        }
        Console.WriteLine();
    }

    static void Main()
    {
        
        UseParams(1, 2, 3, 4);
        UseParams2(1, 'a', "test");

       UseParams2();
        int[] myIntArray = { 5, 6, 7, 8, 9 };
        UseParams(myIntArray);

        object[] myObjArray = { 2, 'b', "test", "again" };
        UseParams2(myObjArray);
       
        UseParams2(myIntArray);
    }
}
/*
Output:
    1 2 3 4
    1 a test

    5 6 7 8 9
    2 b test again
    System.Int32[]
*/
```