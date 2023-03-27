#include<iostream>
#include<string>
#include<algorithm>
#include<vector>
using namespace std;
class Sort{
	string name[3];
    vector<string> dates;
	public:
		Sort(){
			storename();
			storeDates();
			sortname();
			sortDates();
			printNames();
			printDates();
		}
		void sortname(){
			int Fletter;
			int Sletter;
			string temp;
			for(int i=0;i<2;i++)
    {
        if(name[i][0] > name[i+1][0])
        {
            temp=name[i+1];
            name[i+1]=name[i];
            name[i]=temp;
        }
    }
		}
		void printNames(){
			for(int i=0;i<3;i++)
			{
				cout<<"name of persn "<<i+1<<" "<<name[i]<<endl;
			
			}
		}
		void storename(){
			cout<<"enetr names "<<endl;
			for(int i=0;i<3;i++)
			{
			 cout<<"enetr name of person "<<i+1<<endl;
			 getline(cin>>ws,name[i]);
			}
		}
	 void sortDates(){
        sort(dates.begin(), dates.end() , greater<string>());
    }

	void printDates(){
        for(int i=0; i<dates.size(); i++){
            cout << dates[i] << endl;
        }
    }
    void storeDates(){
        cout << "Enter dates (in any format):" << endl;
        for(int i=0; i<3; i++){
            string date;
            getline(cin>>ws, date);
            dates.push_back(date);
        }
    }
};
int main()
{
	Sort object;
}
