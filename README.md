# Marksheet-generator-In-C++
A simple C++ console-based project that generates a student marksheet. The program takes marks of 5 subjects as input, calculates total marks, percentage, and grade, and then saves the result in a text file (marksheet.txt) for record keeping. It helps beginners understand the use of basic input/output, conditionals, and file handling in C++.

#include <iostream>
#include <fstream>   // for file handling
using namespace std;

int main() {
    string name;
    int roll;
    float m1, m2, m3, m4, m5, total, percent;
    char grade;

    cout << "===== Student Marksheet Generator =====\n";
    cout << "Enter Student Name: ";
    getline(cin, name);
    cout << "Enter Roll Number: ";
    cin >> roll;

    cout << "\nEnter marks of 5 subjects (out of 100):\n";
    cout << "Subject 1: "; cin >> m1;
    cout << "Subject 2: "; cin >> m2;
    cout << "Subject 3: "; cin >> m3;
    cout << "Subject 4: "; cin >> m4;
    cout << "Subject 5: "; cin >> m5;

    total = m1 + m2 + m3 + m4 + m5;
    percent = total / 5;

    // Grade calculation
    if (percent >= 90)
        grade = 'A';
    else if (percent >= 75)
        grade = 'B';
    else if (percent >= 60)
        grade = 'C';
    else if (percent >= 40)
        grade = 'D';
    else
        grade = 'F';

    // Display result
    cout << "\n===== RESULT =====\n";
    cout << "Name: " << name << endl;
    cout << "Roll No: " << roll << endl;
    cout << "Total Marks: " << total << "/500" << endl;
    cout << "Percentage: " << percent << "%" << endl;
    cout << "Grade: " << grade << endl;

    // Save to file
    ofstream file("marksheet.txt", ios::app);
    file << "Name: " << name << "\n";
    file << "Roll No: " << roll << "\n";
    file << "Total Marks: " << total << "/500\n";
    file << "Percentage: " << percent << "%\n";
    file << "Grade: " << grade << "\n";
    file << "------------------------------\n";
    file.close();

    cout << "\nMarksheet saved to 'marksheet.txt'\n";
    return 0;
}

#🌟 Features of Marksheet Generator Project

1. User Input Based – Takes student name, roll number, and marks for 5 subjects.


2. Automatic Calculations – Calculates total marks and percentage automatically.


3. Grade Assignment – Assigns grades (A, B, C, D, F) based on percentage.


4. File Handling – Saves each student’s result in a text file (marksheet.txt) for future record.


5. Easy to Use – Simple console-based interface; works on any compiler (Turbo C++, Dev C++, Code::Blocks, etc.).


6. Error-Free & Beginner Friendly – Uses only basic C++ concepts (loops, conditionals, file handling).


7. Readable Output – Displays marksheet neatly in a formatted way.
