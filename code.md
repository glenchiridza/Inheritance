/*
 * File:   main.cpp
 * Author: R156442A
 *
 * Created on September 28, 2016, 11:31 AM
 */

#include <cstdlib>
#include <iostream>
using namespace std;

class Students {
    string regNum;
    string name;
    int age;
public:
    Students(){}
    Students(string reg,string thisName, int thisAge){
    regNum = reg;
    name = thisName;
    age = thisAge;
    }
    void setStudent(string reg,string thisName, int thisAge){

    regNum = reg;
    name = thisName;
    age = thisAge;
    }
    void Display(){
cout<<regNum<<name<<age<<"\n";
}

};

class SotStudent: public Students {
    string intake;
    string period;
    public:
        SotStudent(){}
        SotStudent(string thisIntake,string thisPeriod){
            intake = thisIntake;
            period = thisPeriod;
        }
        void setIntake(string thisIntake,string thisPeriod){
            intake=thisIntake;
            period=thisPeriod;

        }
        void SotDisplay(){
           cout<<"intake Level:"<<intake<<"\n"<<"Period of study"<<period<<"\n";
        }
};

class LawStudent: public Students {
    string semester;
public:
    void setSemester(string Semester){
        semester=Semester;
    }
};

class Diploma: public SotStudent {
    string courseName;
public:
    Diploma(){}
    Diploma(string course){
    courseName=course;
    }
    void setCourseName(string course){
        courseName=course;
    }
    void CourseDisplay(){
    cout<<"Course name : "<<courseName;
    }
};

class Certificate: public SotStudent {
    string courseName;
public:
    void setCourseName(string course){
    courseName = course;
    }
      void CourseDisplay(){
    cout<<"Course name : "<<courseName;
    }
};

class Software: public Diploma {
    string enroll;
public:
    Software(){}
    Software(string enrolling){
    enroll = enrolling;
    }
    void Enroling(string enrolling){
        enroll=enrolling;
      }
    void EnrollDisplay(){
      cout<<"you have been enrolled in "<<enroll<<"class";
    }

};

class Hardware: public Diploma {
    string enroll;
public:
    Hardware(){}
    Hardware(string enrolling){
    enroll = enrolling;
    }
    void Enroling(string enrolling){
        enroll=enrolling;
      }
    void EnrollDisplay(){
      cout<<"you have been enrolled in "<<enroll<<"class";
    }

};

class Networking: public Diploma {
        string enroll;
public:
    Networking(){}
    Networking(string enrolling){
    enroll = enrolling;
    }
    void Enroling(string enrolling){
        enroll=enrolling;
      }
    void EnrollDisplay(){
      cout<<"you have been enrolled in "<<enroll<<"class";
    }

};

int main(int argc, char** argv) {

    SotStudent student;
    LawStudent Law;
    Diploma diploma;
    Certificate certificate;
    Software software;
    Hardware hardware;
    Networking networking;
    int a;
    cout<<"enter faculty   [1]:SotStudent  [2]:Law    ";
    cin>>a;
    if(a==1){

        cout<<"Uz Sot"<<endl;
          cout<<" enter  [1]Diploma      [2] Certificate"<<endl;
           int b;
    cin>>b;
           if(b==1){
                int c;
cout<<"enter where to enroll"<<endl;
cout<<"[1]Software   [2]Hardware   [3]Networking"<<endl;
cin>>c;
if(c==1){
        student.setStudent("R156442A"," Glen ",19);
           diploma.setIntake("Diploma in IT  "," 10 months");
           software.setCourseName("Software");
           diploma.SotDisplay();
           student.Display();
           software.CourseDisplay();
    }
    if(c==2){
        student.setStudent("R156442A"," Glen ",19);
           diploma.setIntake("Diploma in IT  "," 10 months");
            hardware.setCourseName("Hardware");
              diploma.SotDisplay();
            student.Display();
              hardware.CourseDisplay();
    }
       if(c==3){

            student.setStudent("R156442A"," Glen ",19);
           diploma.setIntake("Diploma in IT"  ," 10 months");
            networking.setCourseName("Networking");
           diploma.SotDisplay();
           student.Display();
           networking.CourseDisplay();
       }


           }
           else{
                certificate.setIntake("Certificate in IT  ","7 months");
                    certificate.SotDisplay();
            cout<<"NOTE:  Certificate intake not yet in Progress";

           }
    }
   else{
    Law.setStudent("r111111"," Jigs ",23);
    Law.Display();
}
cout<<endl;
    return 0;
}

