// задайте массив заполненный случайными положительными трехзначными числами. напишите программу, которая покажет количество четных и нечетчных чисел в массив
// [345, 897,568,234] ->

Console.Write(«Введите количество элементов массива: «);
int a = Convert.ToInt32(Console.ReadLine());
int[] randomArray = new int[a];

void mas(int a)
{
for (int i = 0; i < a; i++)
{
randomArray[i] = new Random().Next(99,999);
Console.Write(randomArray[i] + » «);
}

}

int kol(int[] randomArray)
{
int kol = 0;
for (int i = 0; i < randomArray.Length; i++)
{
if (randomArray[i] % 2 == 0)
kol = kol + 1;
}
return kol;
}
 
// Задайте одномерный массив, заполненный случайными числами.Найдите сумму элементов , стоящих на нечетных индексах.
// [3, 7,23,12] ->
// [-4, -6 ,89, 6] -> 0


Console.Write(«Введите количество элементов массива: «);
int a = Convert.ToInt32(Console.ReadLine());
int[] randomArray = new int[a];

void mas(int a)
{
for (int i = 0; i < a; i++)
{
randomArray[i] = new Random().Next(1,9);
Console.Write(randomArray[i] + » «);
}

}

int kol(int[] randomArray)
{
int sum = 0;
int i = 0;
while (i < randomArray.Length)
{
sum = sum + randomArray[i];
i = i + 2;
}
return sum;
}

mas(a);
Console.Write($»\nCумма элементов, стоящих на нечётных позициях: {kol(randomArray)}»);
mas(a);
Console.Write($»\nКоличество чётных чисел в массиве: {kol(randomArray)}»);
