# Lab 23.20
#include <iostream>
using namespace std;

int main() {
  const int MAX_SIZE = 100;
  int grades[MAX_SIZE];
  int numberOfGrades; // the number of grades read.
  int pos;
  int min, max;
  // Read in the values into the array
  pos = 0;
  cout << "Please input a grade from 1 to 100, (or -99 to stop)" << endl; 

  cin >> grades[pos];// the grades that are entered
  while (grades[pos] != -99) // as long as the user doesnt enter -99 the loop will keep going
  {
    pos++;
    cin >> grades[pos];// the grades that are entered until -99
  } 

  numberOfGrades = pos;

  cout << "You entered " << numberOfGrades << " grades:\n";
  
  min = grades[0];
  max = grades [0];
  
  int sum = 0;
  cout << endl;
  for (int i = 0; i < numberOfGrades; i++)
  {
    cout << "Element " << i+1 << " is " << grades[i] << endl;
    sum = sum + grades[i];// total of the grades
  if (grades[i] > max) 
     max = grades[i];
  if (grades[i] < min)
     min = grades[i];
  }
  double average = sum/numberOfGrades;
  cout << "The average of the elements are " << average << endl;
  cout << "The sum of the " << numberOfGrades << " numbers is " << sum << endl;
  cout << "The highest number is " << max<< endl;
  cout << "The lowest number is " << min << endl;
  // this is a partcially filled arrat with a sentinel value is because we do not know how much data will be used and is continuous until the sentinel value is used. which is -99.
}
