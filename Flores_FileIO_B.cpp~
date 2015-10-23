//Name: Sandra Flores
//Date: Oct. 23, 2015
//Description: Programming Practice File IO- B

#include<fstream>
#include<iostream>
#include<iomanip>
#include<cstdlib>

using namespace std;

int main()
{
    ifstream fin;
    ofstream fout;
    char file_name[12];
    double s1, s2, s3, s4, s5, s6, average;
    string firstName, lastName, highName;
    double highaverage = 0;
    
    fin.open("scores.txt");//open the file we are receiving the infot from
    fout.open("result.txt");//made the file for the result
    
    if(fin.fail())//error message
    {
        cout << "Error in the input file." << endl;
        exit(1);
    }
    
    if(fout.fail())
    {
        cout << "Error in the output file." << endl;
        exit(1);
    }
    
    while(fin >> firstName >> lastName >> s1 >> s2 >> s3 >> s4 >> s5 >> average)
    {
        fout.setf(ios::fixed);
        fout.setf(ios::showpoint);
        fout.precision(1);//fixed numbers to one decimal place 
        fout.setf(ios::left);//fixes numbers to the left
        average = (s1 + s2 + s3 + s4 + s5)/5;
        
        fout << setw(10) << firstName << setw(10) << lastName << setw(10) << s1 << setw(10) << s2 << setw(10) << s3 << setw(10) << s4 << setw(10) << s5;
        
        fout.precision(2);//the average is fixed to two decimal places
        fout << setw(10) << average << endl;
         
         
         if(highaverage < average)//check for the highest average
         {
            highName = firstName + " " + lastName;
            highaverage = average;
            
         }
    }
    
    fout << "\nThe highest average is: " + highName << endl;
    
    fin.close();//close files
    fout.close();
    
    return 0;
}
