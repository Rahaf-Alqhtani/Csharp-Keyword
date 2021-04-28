

#  Break 

### 
<div dir=rtl aliany=right>
هي عبارة توقف عند الانتهاء او اتمام شرط معين والخروج من جملةالتكرار. 
</div><br>

   
      
 
```
    class BreakTest
{
    static void Main()
    {
        for (int i = 1; i <= 100; i++)
        {
            if (i == 5)
            {
                break;
            }
            Console.WriteLine(i);
        }
        Console.WriteLine("Press any key to exit.");
        Console.ReadKey();
    }
}
/*
 Output:
    1
    2
    3
    4
*/
```

    

