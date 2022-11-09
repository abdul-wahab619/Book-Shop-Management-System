# Book-Shop-Management-Sysytem
// Final Term Project
            // Basic concept of Project is Inheritance
            // Project Title: Book Shop Management System
            // language : C++
            // Development Technology: Object Oriented Programming
//  Header File:
#include<iostream>   //for input/output
#include<conio.h>   //for console input/output
#include<string>
using namespace std; //standard libarary
                    
int i=0;
//parent class declared;
class book_var
{     
  public:     // All data members are publicaly specifier
	int book_id,price,pages,bill_check;
	string book_name,aurthor,publisher;
	book_var()//constructor for intializing
	{
		book_id=0;
		book_name="";
		aurthor="";
		publisher="";
		price=0;
		pages=0;
	}
}b[20];
class book_fun:public book_var    // Child class declared     and      type of inheritance is public
{
	public:      // All data members are publicaly specifier
	void menu();    // menu function
	void add();     // Add new book function
	void search();  //Search book function
	void update();  //Update book function
	void del();	    //Delete book function
	void show();    //Show all book function
};

void book_fun::menu()
{
	p:
		system("cls");
		int choice;
		cout<<"\n\nWELCOME TO THE BOOK SHOP";
		cout<<"\n\n 1. Add new book";
		cout<<"\n\n 2. Search a book";
		cout<<"\n\n 3. Update book";
		cout<<"\n\n 4. Delete book";
		cout<<"\n\n 5. Show books";
		cout<<"\n\n 6. Exit";
		cout<<"\n\n Enter your choice : ";
		cin>>choice;
		switch(choice)  // Switch statment for handling cases
		{
			case 1:
				add();
				break;
			case 2:
				search();
				break;
			case 3:
				update();
				break;
			case 4:
				del();
				break;
			case 5:
				show();
				break;
			case 6:
				exit(0);
				break;
			default:
				cout<<"\n\n Invalid choice entered, try again. ";		
		}
		getch();
		goto p; //it is lable which work like loop
		
}
void book_fun::add()  // Access the Add function in child class
{
	p:  // this is lable for reapting of code
		system("cls");  //For clearing previous screen
		cout<<"\n\n\t\tBook Management System";
        cout<<"\n\n Book ID :";
        cin>>b [i].book_id;
        for(int a=0 ; a<i; a++)
        {
	        if(b[i]. book_id== b[a].book_id)
	        {
		        cout<<"\n\n Book ID Already Exist ....";
		        getch();
		        goto p;
	       }
        }
        cout<<"\n\n Book Name :";
        cin>>b[i].book_name;
        cout<<"\n\n Author Name: ";
        cin>>b[i].aurthor;
        cout<<"\n\n Publisher Name: ";
        cin>>b[i].publisher;
        cout<<"\n\n Pages: ";
        cin>>b[i].pages;
        cout<<"\n\n Price: ";
        cin>>b[i].price;
        cout<<"\n\n\n\t\t New Book Add Successfully...";
        i++;
}
void book_fun::search() //Access Search function in child class
{
	system("cls");    // for making our project clear and presentable
	int id, found=0, choice;
		string bookname , authorname;
		cout<<"\n\n\t\tBook Management System";
	    if(i == 0)  // if else condition
		{
			cout<<"\n\n Data Base is Empty...";
		}

        else
		{
		    cout<<"\n\n 1. According Book ID";
			cout<<"\n\n 2. According Book Name";
			cout<<"\n\n 3. According Author Name";
			cout<<"\n\n\n  Enter Your Choice: ";
			cin>>choice;

   if(choice == 1)
   {
   	    cout<<"\n\n Book ID :";
   	    cin>>id;
   	    for(int a=0;a<i;a++)
   	        {
   	  	        if(id == b[a].book_id)
   	  	    {
   	  		    system("cls");
   	  		    cout<<"\n\n\t\t Book Management System";
   	  		    cout<<"\n\n Book ID : " <<b[a].book_id;
   	  		    cout<<"\n\n Book Name: " <<b[a].book_name;
   	  		    cout<<"\n\n Author Name: " <<b[a].aurthor;
   	  		    cout<<"\n\n Publisher Name: " <<b[a].publisher;
   	  		    cout<<"\n\n Pages: " <<b[a].pages;
   	  		    cout<<"\n\n Price: " <<b[a].price;
   	  		    cout<<"\n\n\n===============================";
   	  		    found++;
   	  		
		    }
	        }
		        if(found == 0)
		    {
		 	    cout<<"\n\n Book ID Not Found...";
		    }
   }
   else if(choice == 2)
   {
   	    cout<<"\n\n Book Name :";
   	    cin>>bookname;
   	    system("cls");
        cout<<"\n\n\t\tBook Management System";
        for(int a=0; a<i; a++)
		{
		if (bookname == b[a].book_name) 
		{
            cout<<"\n\n Book ID : "<<b[a].book_id;
			cout<<"\n\n Book Name: "<<b[a].book_name;
			cout<<"\n\n Author Name: "<<b[a].aurthor;
			cout<<"\n\n Publisher Name: "<<b[a].publisher;
			cout<<"\n\n Pages: "<<b[a].pages;
			cout<<"\n\n Price : "<<b[a].price;
            cout<<"\n\n\n===================";
		    found++;
	    }
		if (found  == 0)
		{
	        cout<<"\n\n Book Name Not Found...";
		}
        }
    }
    else if(choice == 3)
    {
		cout<<"\n\n Author Name: ";
		cin>>authorname;
		system("cls");
		cout<<"\n\n\t\tBook Management System"; 
		for(int a=0; a<i; a++)
		{
		if(authorname == b[a].aurthor)
		{
            cout<<"\n\n Book ID : "<<b[a].book_id;
			cout<<"\n\n Book Name: "<<b[a].book_name; 
			cout<<"\n\n Author Name : "<<b[a].aurthor;
			cout<<"\n\n Publisher Name: "<<b[a].publisher;
			cout<<"\n\n Pages : "<<b[a].pages;
			cout<<"\n\n Price : "<<b[a].price;
			cout<<"\n\n\n======:";
			found++;
		}
		}
	
		if (found == 0)
		{
		    cout<<"\n\n Author Name Not Found...";
		}
	}
	}
}

void book_fun::update()  //Access update function in child class
{
    
	int id, found=0;
	cout<<"\n\n\t\tBook Management System";
    if(i == 0)
	{
        cout<<"\n\n Data Base is Empty...";
    }
	else
	{
	    cout<<"\n\n Book ID For Update : ";
		cin>>id;
		for(int a=0; a<i; a++)
		{
	        if(id == b[a].book_id)
	    {
		system("cls");
		cout<<"\n\n\t\tBook Management System";
		cout<<"\n\n Book ID : ";
		cin>> b[a].book_id;
		cout<<"\n\n Book Name : ";
		cin>>b[a].book_name;
		cout<<"\n\n Author Name : ";
		cin>> b[a].aurthor;
	    cout<<"\n\n Publisher Name : ";
		cin>> b[a].publisher;
		cout<<"\n\n Pages : ";
		cin>> b[a].pages;
		cout<<"\n\n Price : ";
		cin>> b[a].price;
		cout<<"\n\n\n\tUpdate Book successfully....";
		found++;
	}
 }
		if(found ==0)	
		{
			cout<<"\n\n Book ID Not found...";
		}
   }
}
void book_fun::del()  //Access delete function in child class
	{
		system("cls");
		int id, found =0;
		cout<<"\n\n\t\tBook Management System"; 
		if(i==0)
		{
			cout<<"\n\n Data Base is Empty...";
		}
		else
		{
			cout<<"\n\n Book Id for Delete : ";
			cin>>id;
			for(int a=0; a<i; a++)
			{
				if(id == b[a].book_id )
				{
					for(int k=0; k<i; k++)
					{
						b[k].book_id = b[k+1].book_id;
						b[k].book_name = b[k+1].book_name;
						b[k].aurthor = b[k+1].aurthor;
						b[k].publisher = b[k+1].publisher;
						b[k].pages = b[k+1].pages;
						b[k].price = b[k+1].price;
							
					}
					cout<<"\n\n\n\t\tDelete Book successfully....";
					i--;
					found++;
					
				}
			}
			if (found == 0)
			{
				cout<<"\n\n Book ID not Found...";
			}
		}
	}
	
		void book_fun::show() //Access show function in child class
	{
		system("cls");
		cout<<"\n\n\t\tBook Management System"; 
		if( i == 0)
		{
			cout<<"\n\n Data Base is Empty...";
		}
		else
		{
		
			for (int a=0; a<i; a++)
			{
				cout<<"\n\n Book ID : "<<b[a].book_id;
				cout<<"\n\n Book name : "<<b[a].book_name;
				cout<<"\n\n Author Name: "<<b[a].aurthor;
				cout<<"\n\n Publisher Name : "<<b[a].publisher;
				cout<<"\n\n Pages : "<<b[a].pages;
				cout<<"\n\n Price : "<<b[a].price;
				cout<<"\n\n====================================";
			
			}
		}
	}

// This is the main body of program;
int main()
{
	book_fun obj;  //Here we made a object of child class
	obj.menu();   // Here we call the object of child class
	return (0);   
}
