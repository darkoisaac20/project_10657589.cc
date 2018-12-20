#include <iostream>
#include <conio.h>
#include <stdio.h>
using namespace std;

struct student
    {
        int id;
        char _class[20];
        int age;
	    int marks;
        long double tel;
        char grade[4];
        int course_code;
        char course_title[25];
        char name[25];
        char address[50];
    };





int main()
{
   char dow;
     int add=0;
     int add2=0;
     // variables initialized to increment records

       cout << "Press 1 Edit/Delete/Add Student" << endl;
       cout << "Press 2 Edit/Delete/Add Staff" << endl;


       cout << endl;
       cout << "\t Select Option:";

       int sw2;
       cin >> sw2;

       switch(sw2)
    {
        case  1 :

         cout << "You Can Edit/Add/Delete Student Records.. \n";

    do
   {
       student stud[20];

       cout << "Press 1 to Add New Record" << endl;
       cout << "Press 2 to Delete Record" << endl;
       cout << "Press 3 to Edit Record" << endl;
       cout << "Press 4 to Print Academic Record" << endl;

       cout << endl;
       cout << "\t Select Option:";

       int idcheck = 0;

    int sw;
    cin >> sw;

    switch(sw)
    {
        case  1 :


        cout << "\n Enter the info of the student " << add+1 << "  :" << endl;

        cout << "\t Enter the ID No. (E.g. 1,2.....): ";
    int id2;
    int id1;



    cin >> id1;

    for(int j=0; j<=add; j++){

        id2=id1;
    if(id2 == stud[j].id)
    {
        idcheck = 1;
         }
    }
    // Code to check duplicate record entered using ID
    if(idcheck!= 1){
        stud[add].id=id1;

    cout <<"\t Enter the Name = ";
    cin >> stud[add].name;

    cout << "\t Enter the Address = ";
    cin >> stud[add].address;

    cout << "\t Enter the Telephone no = ";
    cin >> stud[add].tel;

    cout << "\t Enter the Class = ";
    cin >> stud[add]._class;

    cout << "\t Enter the Course_code = ";
    cin >> stud[add].course_code;

    cout << "\t Enter the Course_title = ";
    cin >> stud[add].course_title;

    cout << "\t Enter the Marks = ";
    cin >> stud[add].marks;

    cout << "\t Enter the Grade = ";
    cin >> stud[add].grade;

    cout << "\t Enter the Age = ";
    cin >> stud[add].age;
    add=add+1;
    }
    else
    {
        cout << "This Record Already Exists \n";
    }


            break;
        // code to delete record
        case 2:
            cout << "\n Enter the ID No. of the Student to Delete: " << endl;

            cin >> id1;

            for(int j=0; j<=add; j++)
            {

                id2=id1;
            if(id2==stud[j].id)
            {
                stud[j].id = 'd';
                cout << "\t Record Successfully Deleted";
                  }
            }
                    break;
        case 3:
            cout << "\n Enter the ID No. of the Student to Edit: " << endl;


            cin >>id1;

        for(int j=0; j<=add; j++)
        {


            id2=id1;
        if(id2==stud[j].id)
        {
        cout << "\t ID No.  ";
        cout << stud[j].id;
        cout << "\t Name = ";
        cout << stud[j].name;
        cout << "\t Address = ";
        cout << stud[j].address;
        cout << "\t Telephone no ";
        cout << stud[j].tel;
        cout << "\t Class = ";
        cout << stud[j]._class;

        cout << "\t Course Code = ";
        cout << stud[j].course_code;

        cout << "\t Course Title = ";
        cout << stud[j].course_title;
        cout << "\t Marks = ";
        cout << stud[j].marks;
        cout << "\t Grade = ";
        cout << stud[j].grade;


    cout << "\n\t Re-Enter Info ";
            cout << "\n\t Enter the Name = ";
            cin >> stud[j].name;

            cout << "\n\t Enter the Address = ";
            cin >> stud[j].address;

            cout << "\n\t Enter the Telephone no = ";
            cin >> stud[j].tel;

            cout << "\n\t Enter the Class = ";
            cin >> stud[j]._class;

            cout << "\n\t Enter the Course Code = ";
            cin >> stud[j].course_code;

            cout << "\n\t Enter the Course Title = ";
            cin >> stud[j].course_title;

            cout << "\n\t Enter the Marks = ";
            cin >> stud[j].marks;

            cout << "\n\t Enter the Grade = ";
            cin >> stud[j].grade;

            cout << "\n\t Enter the Age = ";
            cin >> stud[j].age;
               }

    }
    break;


        case 4:
            cout << "\n________________________________________________________________________________________________________" << endl;
            for(int i=0; i<1; i++)
            {
                cout << "ID No. ||";
                cout << " Name ||";
                cout << " Address ||";
                cout << "Tele no ||";
                cout << " Class ||";
                cout << " Course Code || ";
                cout << " Course Title || ";
                cout << " Marks || ";
                cout << " Grade ||\n";
                cout << "________________________________________________________________________________________________________";

            for(int k=0;k<add;k++)
            {
                if(stud[k].id!='d')
                {
                    cout << "\n";
                      cout << " ";
                    cout << stud[k].id;
                    cout << "   || ";
                    cout << stud[k].name;
                    cout << " || ";
                    cout << stud[k].address;
                    cout << "   ||  ";
                    cout << stud[k].tel;
                    cout << "  ||  ";
                    cout << stud[k]._class;
                    cout << " ||  ";
                    cout << stud[k].course_code;
                    cout << "       ||  ";
                    cout << stud[k].course_title;
                    cout << "            ||   ";
                    cout << stud[k].marks;
                    cout << "      ||   ";
                    cout << stud[k].grade;
                    cout << "   ||";
                }

            }
            }

            cout << "\n...............................................................................................................\n";
            cout << "\n________________________________________________________________________________________________________________\n";

                break;


        default:
            cout << "\t You've selected a wrong Option";
            break;
    }
          cout << "\n \n \t Do You want to Continue Again? [Y/N]";
          cin>> dow;
            }

            while(dow=='Y' || 'y');


      break;

        case 2:
            cout << "You Can Edit/Add/Delete Staff Records: " << endl;

            //Add/Delete/Edit Staff records
             do
   {
       student stud[20];

       cout << "Press 1 to Add New Record" << endl;
       cout << "Press 2 to Delete Record" << endl;
       cout << "Press 3 to Edit Record" << endl;
       cout << "Press 4 to Display Record" << endl;

       cout << endl;
       cout << "\t Select Option:";

       int idcheck = 0;

    int sw;
    cin >> sw;

    switch(sw)
    {
        case  1 :


        cout << "\n Enter the info of the Staff " << add2+1 << "  :" << endl;

        cout << "\t Enter the ID No. (E.g. 1,2...) :";
    int id2;
    int id1;

    cin >> id1;

    for(int j=0; j<=add2; j++){

        id2=id1;
    if(id2 == stud[j].id)
    {
        idcheck = 1;
         }
    }
    if(idcheck!= 1){
        stud[add2].id=id1;

    cout <<"\t Enter the Name = ";
    cin >> stud[add2].name;

    cout << "\t Enter the Address = ";
    cin >> stud[add2].address;

    cout << "\t Enter the Telephone no = ";
    cin >> stud[add2].tel;

    cout << "\t Enter the Age = ";
    cin >> stud[add2].age;
    add2=add2+1;
    }
    else
    {
        cout << "This Record Already Exists \n";
    }


            break;

        case 2:
            cout << "\n Enter the ID No. of the Staff to Delete: " << endl;

            cin >> id1;

            for(int j=0; j<=add2; j++)
            {

                id2=id1;
            if(id2==stud[j].id)
            {
                stud[j].id = 'd';
                cout << "\t Record Successfully Deleted";
                  }
            }
                    break;
        case 3:
            cout << "\n Enter the ID No. of the Staff to Edit: " << endl;


            cin >>id1;

        for(int j=0; j<=add; j++)
        {


            id2=id1;
        if(id2==stud[j].id)
        {
        cout << "\t ID No.  ";
        cout << stud[j].id;
        cout << "\t Staff Name = ";
        cout << stud[j].name;
        cout << "\t Address = ";
        cout << stud[j].address;
        cout << "\t Telephone no ";
        cout << stud[j].tel;
        cout << "\t Age ";
        cout << stud[j].age;


    cout << "\n\t Re-Enter Info ";
            cout << "\n\t Enter the Staff ID No. = ";
            cin >> stud[j].id;
            cout << "\n\t Enter the Staff Name = ";
            cin >> stud[j].name;

            cout << "\n\t Enter the Address = ";
            cin >> stud[j].address;

            cout << "\n\t Enter the Telephone no = ";
            cin >> stud[j].tel;

            cout << "\n\t Enter the Age = ";
            cin >> stud[j].age;
               }
        }

                break;

            case 4:
            cout << "\n_____________________________________________"<< endl;
            for(int i=0; i<1; i++)
            {
                cout << "ID No. ||";
                cout << " Name ||";
                cout << " Address ||";
                cout << "Tele no ||";
                cout << " Age ||\n";
                cout << "_____________________________________________";

            for(int k=0;k<add;k++)
            {
                if(stud[k].id!='d')
                {
                    cout << "\n";
                      cout << " ";
                    cout << stud[k].id;
                    cout << "   || ";
                    cout << stud[k].name;
                    cout << " || ";
                    cout << stud[k].address;
                    cout << "   ||  ";
                    cout << stud[k].tel;
                    cout << "  ||  ";

                    cout << stud[k].age;
                    cout << "   ||";
                }

            }
            }

            cout << "\n.............................................\n";
            cout << "\n_____________________________________________\n";

                break;


        default:
            cout << "\t You've selected a wrong Option";
            break;
    }
          cout << "\n \n \t Do You want to Continue Again? [Y/N]";
          cin>> dow;
            }

            while(dow=='Y' || 'y'); // Y is displayed so when user even types y, the programme does not end

            break;




    return 0;





    }


}
