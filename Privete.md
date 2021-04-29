# Privete


 <div dir=rtl aliany=right>
 يتم اضافة هذا المعدل لتحديد طريقة الوصول اليه .وباستخدام هذا التعريف  نستطيع الوصول إلى هذا المتغير أو الدالة من خلال نفس الكلاس فقط، وليس من أي مكان آخر.
 </div><br> 
 
```
    class Employee2
{
    private string name = "FirstName, LastName";
    private double salary = 100.0;

    public string GetName()
    {
        return name;
    }

    public double Salary
    {
        get { return salary; }
    }
}

class PrivateTest
{
    static void Main()
    {
        var e = new Employee2();

        // The data members are inaccessible (private), so
        // they can't be accessed like this:
        //    string n = e.name;
        //    double s = e.salary;

        // 'name' is indirectly accessed via method:
        string n = e.GetName();

        // 'salary' is indirectly accessed via property
        double s = e.Salary;
    }
}
```