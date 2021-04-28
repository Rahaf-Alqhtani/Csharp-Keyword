# Vitual
###  Virtual:


<div dir=rtl aliany=right>
 يتم استخدام هذا التعريف عند انشاء داله في الكلاس الاساسي حيث انها وسم لتعريف الدوال المراد اعادة تعرفها بمحتوى مختلف في الكلاس المشتق . هذا التعريف لداله يجعل منها تابعًا ظاهريًّا يسمح للتوابع الأخرى بتجاوزه أي إعادة تعريف التابع بالشكل الذي يناسب .
</div><br>

    enter  class TestOverride
      {
      public class Employee
      {
      public string name;
      
        public Employee(string name, decimal basepay)
        {
            this.name = name;
            this.basepay = basepay;
        }

        public virtual decimal CalculatePay() //Virtual هنا تم استخدام 
        {
            return basepay;
        }
    }
    
    public class SalesEmployee : Employee
    {
           private decimal salesbonus;

     public SalesEmployee(string name, decimal basepay, decimal salesbonus) 
     : base(name, basepay) 
    {
          this.salesbonus = salesbonus; 
    } 

        public override decimal CalculatePay()  //هنا تم اعادة استخدام الدالة بشكل مختلف .
        {
            return basepay + salesbonus;
        }
    }

