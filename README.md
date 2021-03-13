# averagerainfallcalculator
This program allows the user the calculate the average rainfall for a set number of months

#include <iostream>
using namespace std;

// this function allows the user to display how many inches of rainfall there was for the month
double rainfallForMonth(double& x)
{
    cout << "How many inches of rainfall are in this month? ";
    cin >> x;
    return x;
}

// this function calculates the average amount of rainfall over a specified number of months
double averageRainfall(double total, int numMonths)
{
    return total/numMonths;
}

int main()
{
    double inches = 0.0; // variable inches will allow the user to input inches of rainfall
    double totalRainfall = 0.0; // stores the total rainfall after each iteration
    int iteration = 0; // iteration denotes the number of months and  will be used to calculate the average rainfall
    char repetition; // allows the user to continue the program for additional months
    do // do while loop allows user to display how many inches of rainfall there were for the month and calculate the average rainfall
    {
        cout << rainfallForMonth(inches) << endl;
        totalRainfall+=inches;
        iteration++;
        cout << "Would you like to calculate rainfall for more months? (Type 'Y' or 'y'): ";
        cin >> repetition;
    } while(repetition == 'y' || repetition == 'Y');
    cout << "The average rainfall for this time period is " << averageRainfall(totalRainfall, iteration) << " inches" << endl;
    return 0;
}
