int dayNumber = 6;

switch (dayNumber) 
{
    case 5 or 6 or 7: 
        Console.WriteLine("Выходной"); 
        break;
    default: 
        Console.WriteLine("Будний"); 
        break;
}


// Шаг 2. Диапазоны через and
int score = 78;

switch (score) 
{
    case >= 0 and <= 39:
        Console.WriteLine("Неудовлетворительно");
        break;
    case >= 40 and <= 59:
        Console.WriteLine("Удовлетворительно");
        break;
    case >= 60 and <= 79:
        Console.WriteLine("Хорошо");
        break;
    case >= 80 and <= 100:
        Console.WriteLine("Отлично");
        break;
    default:
        Console.WriteLine("Некорректный балл");
        break;
}

// Задание с температурой (switch expression)
int temperature = 20;

string result = temperature switch {
    < 0 => "Мороз",
    >= 0 and <= 14 => "Прохладно",
    >= 15 and <= 24 => "Комфортно",
    >= 25 and <= 34 => "Жарко",
    >= 35 => "Очень жарко"
};

Console.WriteLine(result);

// Задание с ролями (switch expression)
string role = "user";

string result = role switch {
    "admin" => "Полный доступ",
    "teacher" => "Доступ преподавателя",
    _ => "Ограниченный доступ"
};

Console.WriteLine(result);


// Задание с ключевым словом when
int age = 20;
bool hasTicket = true;

switch (age) {
    case >= 18 when hasTicket:
        Console.WriteLine("Вход разрешён");
        break;
    case >= 18:
        Console.WriteLine("Нет билета");
        break;
    default:
        Console.WriteLine("Возраст не подходит");
        break;
}

int month = 12;

string season = month switch {
    12 or 1 or 2 => "Зима",
    3 or 4 or 5 => "Весна",
    6 or 7 or 8 => "Лето",
    9 or 10 or 11 => "Осень",
    _ => "Неверный месяц"
};

Console.WriteLine(season);

int age = 25;

string ageCategory = age switch {
    < 0 => "Ошибка",
    >= 0 and <= 6 => "Ребёнок",
    >= 7 and <= 17 => "Подросток",
    >= 18 and <= 64 => "Взрослый",
    >= 65 => "Пенсионер"
};

Console.WriteLine(ageCategory);

string userRole = "admin";

string accessLevel = userRole switch {
    "admin" => "Полный доступ",
    "teacher" => "Доступ преподавателя",
    "user" => "Ограниченный доступ",
    _ => "Неизвестная роль"
};

Console.WriteLine(accessLevel);

int hour = 14;

string tariff = hour switch {
    >= 0 and <= 5 => "Ночной тариф",
    >= 6 and <= 9 => "Утренний тариф",
    >= 10 and <= 17 => "Дневной тариф",
    >= 18 and <= 23 => "Вечерний тариф",
    _ => "Некорректный час"
};

Console.WriteLine(tariff);

int number = 42;

string numberCategory = number switch {
    < 0 => "Отрицательное",
    1 or 2 or 3 => "Маленькое число",
    >= 0 and <= 9 => "Однозначное",
    >= 10 and <= 99 => "Двузначное",
    >= 100 => "Трёхзначное или больше"
};

Console.WriteLine(numberCategory);









int totalExercises = 8;

for (int number = totalExercises; number >= 1; number--) 
{
    Console.WriteLine($"Упражнение {number}");
}

Console.WriteLine("Домашнее задание готово");

------
for (int room = 5; room <= 50; room += 5) 
{
    Console.WriteLine($"Кабинет {room}");
}

------

int totalWeeks = 3;

for (int week = 1; week <= totalWeeks; week++) 
{
    for (int day = 1; day <= 5; day++) 
    {
        Console.WriteLine($"Неделя {week}, день {day}");
    }
    Console.WriteLine("^_^");
}
------

int skippedTickets = 0;

for (int ticket = 1; ticket <= 30; ticket++) 
{
    if (ticket == 4 || ticket == 12 || ticket == 19) 
    {
        skippedTickets++;
        continue;
    }

    Console.WriteLine($"Первый доступный билет: {ticket}");
    Console.WriteLine($"Пропущено билетов: {skippedTickets}");
    break;
}

------

int n = 15;

for (int i = 1; i <= n; i += 2)
{
    Console.WriteLine(i);
}


for (int i = 100; i >= 0; i -= 10)
{
    Console.WriteLine(i);
}

for (int i = 1; i <= 9; i++)
{
    for (int j = 1; j <= 9; j++)
    {
        Console.WriteLine($"{i} * {j} = {i * j}");
    }
    Console.WriteLine(); // Разделитель между блоками чисел
}

for (int i = 1; i <= 50; i++)
{
    if (i % 7 == 0)
    {
        Console.WriteLine($"Первое число, кратное 7: {i}");
        break;
    }

    if (i % 3 == 0)
    {
        continue;
    }

    Console.WriteLine(i);
}

------

int n = 22;
int sum = 0;

for (int i = 1; i <= n; i++)
{
    if (i % 5 == 0)
    {
        continue;
    }
    sum += i;
}

Console.WriteLine($"Сумма чисел от 1 до {n} без кратных 5 равна: {sum}");


------

Console.Write("Введите общее количество недель тренировок N: ");
int n = int.Parse(Console.ReadLine());

int trainingDaysCount = 0;
bool enough = false;

for (int week = 1; week <= n && !enough; week++)
{
    for (int day = 1; day <= 7; day++)
    {
        if (day == 7)
        {
            continue;
        }

        trainingDaysCount++;

        if (trainingDaysCount == 20)
        {
            enough = true;
            Console.WriteLine($"Набрано 20 тренировочных дней! Остановка на неделе {week}, день {day}.");
            break;
        }
    }
}



10.

string subject = "Программирование";

foreach (char letter in subject) 
{
    Console.WriteLine(letter);
}

Console.WriteLine($"Общее количество букв: {subject.Length}");

------

int[] grades = { 4, 5, 3, 5, 4 };
int sum = 0;

foreach (int grade in grades) 
{
    Console.WriteLine(grade);
    sum += grade;
}

double average = (double)sum / grades.Length;
Console.WriteLine($"Средний балл: {average}");

------

string[] students = { "Аня", "Ярослав", "Вика" };
int studentCount = 0;

foreach (string student in students) 
{
    Console.WriteLine(student);
    studentCount++;
}

Console.WriteLine($"Всего учеников: {studentCount}");

------
int[] points = { 10, 20, 15 };

for (int i = 0; i < points.Length; i++)
{
    points[i] = points[i] + 5;
}

for (int i = 0; i < points.Length; i++)
{
    Console.WriteLine(points[i]);
}


------

int[] numbers = { 10, 23, 5, 42, 17 };
int sum = 0;

foreach (int num in numbers)
{
    Console.WriteLine(num);
    sum += num;
}

Console.WriteLine($"Сумма: {sum}");


string[] days = { "Понедельник", "Вторник", "Среда", "Четверг", "Пятница", "Суббота", "Воскресенье" };

foreach (string day in days)
{
    Console.WriteLine($"{day}!");
}


string word = "программирование";
int vowelsCount = 0;

foreach (char letter in word)
{
    if (letter is 'а' or 'е' or 'ё' or 'и' or 'о' or 'у' or 'ы' or 'э' or 'ю' or 'я')
    {
        vowelsCount++;
    }
}

Console.WriteLine($"Количество гласных букв: {vowelsCount}");


int[] grades = { 4, 3, 5, 2, 5, 4 };
int maxGrade = int.MinValue;

foreach (int grade in grades)
{
    if (grade > maxGrade)
    {
        maxGrade = grade;
    }
}

Console.WriteLine($"Наибольшая оценка: {maxGrade}");

------

int[] numbers = { 4, 8, 15, 16, 23, 42 };

for (int i = 0; i < numbers.Length; i++)
{
    numbers[i] = numbers[i] + 1;
}

foreach (int num in numbers)
{
    Console.WriteLine(num);
}


------
string[] names = { "Аня", "Борис", "Вика", "Дима" };
int[] grades = { 5, 4, 5, 3 };

int sum = 0;
int maxGrade = int.MinValue;
string bestStudent = "";

for (int i = 0; i < names.Length; i++)
{
    Console.WriteLine($"{names[i]} — {grades[i]}");
    
    sum += grades[i];

    if (grades[i] > maxGrade)
    {
        maxGrade = grades[i];
        bestStudent = names[i];
    }
}

double average = (double)sum / grades.Length;

Console.WriteLine($"Средний балл по классу: {average}");
Console.WriteLine($"Ученик с максимальной оценкой: {bestStudent}");


------

11.

PrintHeader();
PrintHeader();
Console.WriteLine("Основная часть программы");
PrintFooter();

void PrintHeader() {
    Console.WriteLine("^__^");
    Console.WriteLine("Лабораторная работа №13");
    Console.WriteLine("Дата формирования отчёта");
    Console.WriteLine("0_0");
}

void PrintFooter() {
    Console.WriteLine(">_<");
    Console.WriteLine("      Конец программы");
    Console.WriteLine("X_X");
}

------
void PrintStudentCard(string name, int age, string groupNumber) {
    Console.WriteLine($"Студент: {name}, возраст: {age}, группа: {groupNumber}");
}

PrintStudentCard("Егор", 18, "ИСП-21");
PrintStudentCard("Валерия", 17, "ИСП-22");
------
double CalculateScholarship(double baseAmount, double bonusPercent) {
    return baseAmount + baseAmount * bonusPercent / 100;
}

bool IsEligibleForBonus(double averageGrade) {
    return averageGrade >= 4.5;
}

double currentAverageGrade = 4.7;
double baseScholarship = 2000;
double finalResult;

if (IsEligibleForBonus(currentAverageGrade)) {
    finalResult = CalculateScholarship(baseScholarship, 15);
} else {
    finalResult = CalculateScholarship(baseScholarship, 0);
}

Console.WriteLine(finalResult);
------
double CalculateAverageGrade(int[] grades) {
    int sum = 0;
    foreach (int grade in grades) {
        sum += grade;
    }
    return (double)sum / grades.Length;
}

int CountFives(int[] grades) {
    int count = 0;
    foreach (int grade in grades) {
        if (grade == 5) {
            count++;
        }
    }
    return count;
}

int[] gradesArray = { 4, 5, 3, 5, 4 };
double average = CalculateAverageGrade(gradesArray);
int fives = CountFives(gradesArray);

Console.WriteLine($"Средний балл: {average}");
Console.WriteLine($"Количество пятёрок: {fives}");
------
void PrintDivider() {
    Console.WriteLine("--------------------------------");
}

Console.WriteLine("Текст до первого разделителя");
PrintDivider();
Console.WriteLine("Текст между разделителями");
PrintDivider();
Console.WriteLine("Текст в самом конце");
------
void PrintPerson(string name, int age) {
    Console.WriteLine($"Имя: {name}, Возраст: {age} лет");
}

PrintPerson("Иван", 20);
PrintPerson("Анна", 19);
PrintPerson("Сергей", 25);
------
bool IsEven(int number) {
    return number % 2 == 0;
}

int testNumber = 14;

if (IsEven(testNumber)) {
    Console.WriteLine($"Число {testNumber} является чётным");
} else {
    Console.WriteLine($"Число {testNumber} является нечётным");
}

------
int FindMax(int[] numbers) {
    int max = numbers[0];
    foreach (int num in numbers) {
        if (num > max) {
            max = num;
        }
    }
    return max;
}

int[] array = { 4, 12, 8, 23, 5 };
int maxResult = FindMax(array);
Console.WriteLine($"Максимальное число в массиве: {maxResult}");
------
bool ContainsValue(int[] numbers, int target) {
    foreach (int num in numbers) {
        if (num == target) {
            return true;
        }
    }
    return false;
}

int[] myNumbers = { 5, 10, 15, 20, 25 };
int searchTarget = 15;

if (ContainsValue(myNumbers, searchTarget)) {
    Console.WriteLine($"Значение {searchTarget} найдено в массиве");
} else {
    Console.WriteLine($"Значение {searchTarget} не найдено в массиве");
}
------
13.

int[] recordBooks = { 1042, 1058, 1071, 1093, 1105 };
int target = 9999;
bool found = false;

foreach (int number in recordBooks) {
    if (number == target) {
        found = true;
        break;
    }
}

Console.WriteLine(found ? "Студент найден" : "Студент не найден");
------
int variant = 1;
bool isPrime = true;

if (variant <= 1) {
    Console.WriteLine("Единица и отрицательные числа не являются ни простыми, ни составными");
} else {
    for (int divisor = 2; divisor < variant; divisor++) {
        if (variant % divisor == 0) {
            isPrime = false;
            break;
        }
    }
    Console.WriteLine(isPrime ? "Номер варианта простой" : "Номер варианта составной");
}
------
int[] pointsPerLab = { 8, -1, 10, 9, -1, 7 };
int sum = 0;
int passedLabsCount = 0;

foreach (int points in pointsPerLab) {
    if (points < 0) {
        continue;
    }
    sum += points;
    passedLabsCount++;
}

Console.WriteLine($"Сумма баллов за сданные работы: {sum}");
Console.WriteLine($"Количество сданных работ: {passedLabsCount}");
------
int[] groupIds = { 101, 104, 107, 104, 110 };
bool hasDuplicates = false;

for (int i = 0; i < groupIds.Length; i++) {
    for (int j = i + 1; j < groupIds.Length; j++) {
        if (groupIds[i] == groupIds[j]) {
            hasDuplicates = true;
            Console.WriteLine($"Найдена пара дубликатов: {groupIds[i]} и {groupIds[j]}");
            break;
        }
    }
    if (hasDuplicates) {
        break;
    }
}

Console.WriteLine(hasDuplicates ? "Есть повторяющиеся номера" : "Все номера уникальны");
------
int[] numbers = { 10, 20, 30, 40, 50 };
int target = 30;
int index = -1;
bool found = false;

for (int i = 0; i < numbers.Length; i++)
{
    if (numbers[i] == target)
    {
        index = i;
        found = true;
        break;
    }
}

if (found)
{
    Console.WriteLine($"Индекс числа: {index}");
}
else
{
    Console.WriteLine("Числа нет в массиве");
}
------
int number = 29;
bool isPrime = true;

if (number <= 1)
{
    isPrime = false;
}
else
{
    for (int i = 2; i < number; i++)
    {
        if (number % i == 0)
        {
            isPrime = false;
            break;
        }
    }
}

Console.WriteLine(isPrime ? "Число простое" : "Число не простое");
------
int[] numbers = { 4, 7, 2, 9, 8, 5 };
int sum = 0;

foreach (int num in numbers)
{
    if (num % 2 != 0)
    {
        continue;
    }
    sum += num;
}

Console.WriteLine($"Сумма чётных чисел: {sum}");
------
int[] numbers = { 5, 12, 8, 12, 3 };
bool hasDuplicates = false;

for (int i = 0; i < numbers.Length; i++)
{
    for (int j = i + 1; j < numbers.Length; j++)
    {
        if (numbers[i] == numbers[j])
        {
            hasDuplicates = true;
            break;
        }
    }
    if (hasDuplicates)
    {
        break;
    }
}

Console.WriteLine(hasDuplicates ? "Есть повторяющиеся элементы" : "Все элементы уникальны");
------
string word = "довод";
bool isPalindrome = true;

for (int i = 0; i < word.Length / 2; i++)
{
    if (word[i] != word[word.Length - 1 - i])
    {
        isPalindrome = false;
        break;
    }
}

Console.WriteLine(isPalindrome ? "Слово является палиндромом" : "Слово не является палиндромом");
------
int[] numbers = { 2, 7, 11, 15, 3 };
int target = 10;
bool found = false;

for (int i = 0; i < numbers.Length; i++)
{
    for (int j = i + 1; j < numbers.Length; j++)
    {
        if (numbers[i] + numbers[j] == target)
        {
            Console.WriteLine($"Пара найдена: индексы {i} и {j}");
            found = true;
            break;
        }
    }
    if (found)
    {
        break;
    }
}

if (!found)
{
    Console.WriteLine("Пара не найдена");
}
------

