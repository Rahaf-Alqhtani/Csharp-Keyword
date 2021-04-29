# Public 
 <div dir=rtl aliany=right> 
  يتم اضافة هذا المعدل لتحديد طريقة الوصول و باستخدام هذا التعريف  
 نستطيع الوصول إلى هذا المتغير أو الدالة  او الكلاس من اي مكان في المشروع، او حتى من خلال مشروع آخر. 
</div><br>

```

class PointTest
{
    public int x;
    public int y;
}

class Program
{
    static void Main()
    {
        var p = new PointTest();
        //  public وصول مباشر الى المتغير  .
        p.x = 10;
        p.y = 15;
        Console.WriteLine($"x = {p.x}, y = {p.y}");
    }
}
// Output: x = 10, y = 15

```
