#include <iostream>
#include <vector>
#include <string>

using namespace std;

// Forward declarations for association
class Course;

class Student {
private:
    int student_id;
    string name;
    vector<Course*> courses; // Association: Student enrolls in courses

public:
    Student(int id, string n) : student_id(id), name(n) {}

    void enroll(Course* course);

    void display() const;
};

class Course {
private:
    string code;
    string title;
