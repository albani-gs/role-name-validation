# role-name-validation
Validando uma string com um loop do-while em C#.

```
Console.WriteLine("Enter your role name (Administrator, Manager, User):");
bool validEntry = false;
string? readResult;
string roleName = "";

do
{
    readResult = Console.ReadLine();
    
    if (readResult != null)
    {
        roleName = readResult.Trim();
    }
    if (roleName.ToLower() == "administrator" || roleName.ToLower() == "manager" || roleName.ToLower() == "user")
    {
        validEntry = true;
    } else
    {
        Console.WriteLine($"The role name that you entered, \"{roleName}\" is not valid. Enter your role name (Administrator, Manager, or User)");
    }
    
} while(validEntry == false);

Console.WriteLine($"Your input value ({roleName}) has been accepted.");
```
