using System;

class Program
{
    static void Main()
    {
        Console.WriteLine("برنامه محاسبه عمر به ماه، روز و ساعت");
        Console.WriteLine("----------------------------------");
        
        // دریافت سال تولد
        Console.Write("سال تولد خود را وارد کنید: ");
        int birthYear = int.Parse(Console.ReadLine());
        
        // دریافت ماه تولد
        Console.Write("ماه تولد خود را وارد کنید (1-12): ");
        int birthMonth = int.Parse(Console.ReadLine());
        
        // دریافت روز تولد
        Console.Write("روز تولد خود را وارد کنید: ");
        int birthDay = int.Parse(Console.ReadLine());
        
        // تاریخ فعلی
        DateTime currentDate = DateTime.Now;
        
        // تاریخ تولد کاربر
        DateTime birthDate = new DateTime(birthYear, birthMonth, birthDay);
        
        // محاسبه تفاوت تاریخ‌ها
        TimeSpan age = currentDate - birthDate;
        
        // محاسبه ماه‌ها (تقریبی)
        int months = (int)(age.TotalDays / 30.44);
        int days = (int)age.TotalDays;
        long hours = (long)age.TotalHours;
        
        // نمایش نتایج
        Console.WriteLine("\nنتایج محاسبه:");
        Console.WriteLine($"سن شما به ماه: {months} ماه");
        Console.WriteLine($"سن شما به روز: {days} روز");
        Console.WriteLine($"سن شما به ساعت: {hours} ساعت");
        
        Console.WriteLine("\nبرای خروج از برنامه، یک کلید را فشار دهید...");
        Console.ReadKey();
    }
}
