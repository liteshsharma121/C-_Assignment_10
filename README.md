
#include <iostream>
using namespace std;

// Class Template
template <class T>
class Calculator {
private:
    T a, b;

public:
    Calculator(T x, T y) {
        a = x;
        b = y;
        cout << "Constructor called." << endl;
    }

    void display() {
        cout << "First value: " << a << endl;
        cout << "Second value: " << b << endl;
        cout << "Sum: " << a + b << endl;
    }
};

// Function Template
template <class T>
T findMax(T a, T b) {
    if (a > b)
        return a;
    else
        return b;
}

int main() {
    cout << "Creating integer object:" << endl;
    Calculator<int> obj1(10, 20);

    cout << "\nInteger object details:" << endl;
    obj1.display();

    cout << "\nCreating float object:" << endl;
    Calculator<float> obj2(5.5f, 2.5f);

    cout << "\nFloat object details:" << endl;
    obj2.display();

    cout << "\nFunction template:" << endl;
    cout << "Maximum of 15 and 25: "
         << findMax(15, 25) << endl;

    cout << "Maximum of 4.5 and 8.2: "
         << findMax(4.5, 8.2) << endl;

    return 0;
}
