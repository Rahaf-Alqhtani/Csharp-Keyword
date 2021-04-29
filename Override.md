
#  Override

###    Override :
<div dir=rtl aliany=right>
هي تعريف الداله التي ورثها الكلاس الفرعي  من الكلاس الاساسي . هذه الداله تكون مشابهه للداله الاساسية  حيث الشكل والهيكل  فقط اي ان لها نفس الاسم والنوع والمعاملات ولكن باستخدام هذا التعريف  يكمن كتابة محتوى مختلف لدالة.
وهذا هو السبب خلف استخدام هذا التعريف .
</div><br>

   
      
 

     
         class TestOverride
      {
      public class Employee
      {
      public string name;
      
        public Employee(string name, decimal basepay)
        {
            this.name = name;
            this.basepay = basepay;
        }

        public virtual decimal CalculatePay()
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

        public override decimal CalculatePay()  //overrid هكذا تم اعادة  كتابة محتوى الداله .
        {
            return basepay + salesbonus;
        }
    }

    

