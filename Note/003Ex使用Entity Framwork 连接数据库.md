# 使用Entity Framwork 连接数据库

1. 使用NuGet添加Entity Framework类库

2. 项目中添加ADO.NET Entity Data Model

3. 设置Data Model

   a. Generate from database

   b. Add new connection, select Microsoft SQL Sever

   c. Fill in sever name, local

   d. Select Adventure Work Database

   e. Select table

```c#
namespace PropertySample
{
    class Program
    {
        static void Main(string[] args)
        {
            AdventureWorks2014Entities proxy = new AdventureWorks2014Entities();
            foreach (Product p in proxy.Products)
            {
                Console.WriteLine(p.Name);
            }
            Console.WriteLine("===============");
            Console.WriteLine(proxy.Products.Count());
        }
    }
}
```



**Code Snippet**

1. foreach + Tab * 2

1. cw + Tab * 2 == Cosole.WriteLine();