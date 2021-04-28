
#  Protected

<div dir=rtl aliany=right> 
  يتم اضافة هذا المعدل لتحديد طريقة الوصول و باستخدام هذا التعريف
 نستطيع الوصول إلى هذا المتغير أو الدالة من نفس الكلاس او من كلاس أخرى مشتقة منها.</div>
 <br>
 
```
    class A
{
    protected int x = 123;
}

class B : A
{
    static void Main()
    {
        var a = new A();
        var b = new B();

        // Error CS1540, because x can only be accessed by
        // classes derived from A.
        // a.x = 10;

        // OK, because this class derives from A.
        b.x = 10;
    }
}
```