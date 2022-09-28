//1. Append:

internal class Program
{
	public static void Main(string[] args)
	{
		int[] arr = { 1, 2 };

		Console.WriteLine("enter a number you wish to append: ");
		int num = int.Parse(Console.ReadLine());

		void Add(int[] arr, int num)
		{
			int[] newArr = new int[arr.Length + 1];

			for (int i = 0; i < arr.Length; i++)
			{
				newArr[i] = arr[i];
			}
			newArr[arr.Length] = num;
			foreach (var item in newArr)
			{
				Console.Write($"{item} ");
			}
		}


		Add(arr, num);




		Console.WriteLine("*************************");
		//2. GetIndexes:

		int[] arr1 = { 1, 4, 1, 5, 9, 2 };
		int[] arr2 = { 1, 7, 4, 8, 3, 6, 2 };

		Console.WriteLine("enter a number: ");
		int num1 = int.Parse(Console.ReadLine());
		int[] empty = { };

		void Find(int[] arr, int num)
		{
			for (int i = 0; i < arr.Length; i++)
			{
				if (num == arr[i]) Add(empty, i);
			}
		}

		Find(arr1, num1);



		Console.WriteLine("*************************");

		//3.GetItemsAbove

		Console.WriteLine("enter a number: ");
		int num2 = int.Parse(Console.ReadLine());
		int[] empty1 = { };
		int[] arr3 = { 1, 4, 1, 5, 9, 2 };

		void FindAbove(int[] arr, int num)
		{
			for (int i = 0; i < arr.Length; i++)
			{
				if (num < arr[i]) Add(empty1, arr[i]);
			}
		}


		FindAbove(arr3, num2);

		Console.WriteLine("*************************");


		//4.GetItemsExcept

		Console.WriteLine("enter a number you dont want: ");
		int num3 = int.Parse(Console.ReadLine());
		int[] empty2 = { };
		void FindExcept(int[] arr, int num)
		{
			for (int i = 0; i < arr.Length; i++)
			{
				if (num3 != arr[i]) Add(empty2, arr[i]);
			}
		}

		FindExcept(arr3, num3);
        Console.WriteLine("*************************");



        //5.


        //6.GetSorted
        int[] items1 = { 3,2,1 };

		void Sorted(int[] arr)
		{
		    int helped;
		    for (int i = 0; i < arr.Length; i++)
		    {
		        for (int w = i + 1; w < arr.Length; w++)
		        {
		            if (arr[i] > arr[w])
		            {
		                helped = arr[i];
		                arr[i] = arr[w];
		                arr[w] = helped;
		            }
		        }
		    }
		    foreach (var i in arr)
		    {
		        Console.Write(i);
		        Console.Write(" ");
		    }
		}
        Console.WriteLine("*************************");

        Sorted(items1);


        //7.AreItemsSame

        int[] isSame = { 1, 4, 1 };
	int[] isSame1 = { 1, 1, 1 };


	void IsTheSame(int[] arr)
		{
			int number = arr[0];
			bool correct = true;
			for (int i = 0; i < arr.Length; i++)
			{
				if (arr[i] != number) correct = false;
			}
			Console.WriteLine(correct);
		}
        Console.WriteLine("*************************");

        IsTheSame(isSame);

        IsTheSame(isSame1);
    }
}
