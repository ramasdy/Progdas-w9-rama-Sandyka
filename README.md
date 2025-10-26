#include <iostream>
#include <cmath>
#include <iomanip>
using namespace std;

const double PI = 3.14159;

double distance(double x1, double y1, double x2, double y2);
double radius(double x1, double y1, double x2, double y2);
double circumference(double r);
double area(double r);

int main(){
    
    double x1, y1, x2, y2;
    cout << "Enter coordinates of point 1 (x1 y1): ";
    cin >> x1 >> y1;
    cout << "Enter coordinates of point 2 (x2 y2): ";
    cin >> x2 >> y2;

    double dist = distance(x1, y1, x2, y2);
    double r = radius(x1, y1, x2, y2);
    double circ = circumference(r);
    double ar = area(r);

    cout << fixed << setprecision(4);
    cout << "Distance between points: " << dist << endl;
    cout << "Radius: " << r << endl;
    cout << "Circumference: " << circ << endl;
    cout << "Area: " << ar << endl;

    return 0;
}

double distance(double x1, double y1, double x2, double y2) {
    return sqrt(pow(x2 - x1, 2) + pow(y2 - y1, 2));
}

double radius(double x1, double y1, double x2, double y2) {
    return distance(x1, y1, x2, y2) / 2.0;
}
double circumference(double r) {
    return 2 * PI * r;
}
double area(double r) {
    return PI * r * r;
}
