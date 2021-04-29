

# Countinu 

### 
<div dir=rtl aliany=right>
هي عبارة تخطي او استمرار عند اتمام شرط معين في جملةالتكرار. 
</div><br>

   
      
 
```
    class ContinueTest
{
    static void Main()
    {
        for (int i = 1; i <= 10; i++)
        {
            if (i < 9)
            {
                continue;
            }
            Console.WriteLine(i);
        }

        // Keep the console open in debug mode.
        Console.WriteLine("Press any key to exit.");
        Console.ReadKey();
    }
}
/*
Output:
9
10
*/
```

    

