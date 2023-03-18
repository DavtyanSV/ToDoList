# ToDoList

using System;
using System.Collections.Generic;
using System.Linq;


namespace ToDoList
{
    class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("Вы открыли программу список задач");
            List<string> taskList = new List<string>();
            string option = "";
            string tire = "--------------------------------------------------------------";

            while (option != "q")
            {
                Console.WriteLine("Что вы хотите сделать?");
                Console.WriteLine("Нажмите 1 чтобы добавить задачу в список");
                Console.WriteLine("Нажмите 2 чтобы удалить задачу из списка");
                Console.WriteLine("Нажмите 3 чтобы посмотреть все задачи");
                Console.WriteLine("Нажмите q чтобы выйти из программы");

                option = Console.ReadLine();

                if (option == "1")
                {
                    Console.WriteLine(tire);
                    Console.WriteLine("Пожалуйста, внесите вашу задачу");
                    string task = Console.ReadLine();
                    taskList.Add(task);
                    Console.WriteLine("Задача добавлена");
                    Console.WriteLine(tire);
                }
                else if (option == "2")
                {
                    Console.WriteLine(tire);
                    Console.WriteLine("Выберите какую номер задачи которую хотите удалить:");
                    for (int i = 0; i < taskList.Count; i++)
                    {
                        Console.WriteLine($"{i} - {taskList[i]}");

                    }
                    int number_for_delete = Convert.ToInt32(Console.ReadLine());
                    taskList.RemoveAt(number_for_delete);
                    Console.WriteLine(tire);
                }
                else if (option == "3")
                {
                    Console.WriteLine(tire);
                    Console.WriteLine("Ваши задачи");
                    for (int i = 0; i < taskList.Count; i++)
                    {
                        Console.WriteLine(taskList[i]);
                    }
                  

                    Console.WriteLine(tire);

                }
                else if (option == "q")
                {
                    Console.WriteLine(tire);
                    Console.WriteLine("Выполняется выход из программы");
                    Console.WriteLine(tire);
                }
                else
                {
                    Console.WriteLine(tire);
                    Console.WriteLine("Введено некорректная команда. Пожалуйста, попробуйте еще раз!");
                    Console.WriteLine(tire);
                }





            }


        }
    }

}

