#include <iostream>
using namespace std;

const double CHILD_PRICE = 10.95;
const double ADULT_PRICE = 19.99;
const double SENIOR_PRICE = 18.99;
const double VIP_PRICE = 7.99;

#include <iomanip>
int main() {
    int totalChildren = 0, totalAdults = 0, totalSeniors = 0, totalVIPs = 0;

    for (int day = 1; day <= 3; day++) {
        char category;
        int quantity;

        cout << "Day " << day << " - Enter ticket category (C/A/S/V) or Q to quit: ";
        cin >> category;
        category = toupper(category);

        switch (category) {
            case 'C':
            case 'A':
            case 'S':
            case 'V':
                cout << "Enter the quantity for " << category << ": ";
                cin >> quantity;

                switch (category) {
                    case 'C':
                        totalChildren += quantity;
                        break;
                    case 'A':
                        totalAdults += quantity;
                        break;
                    case 'S':
                        totalSeniors += quantity;
                        break;
                    case 'V':
                        totalVIPs += quantity;
                        break;
                }
                break;
            case 'Q':
                break;
            default:
                cout << "Invalid category. Please enter C, A, S, V, or Q." << endl;
                day--;  // Allow the user to re-enter the correct category
        }

        if (category == 'Q') {
            break;  // Exit the loop when the user quits
        }
    }

    // Calculate and output total ticket sales
    double totalSales = (totalChildren * CHILD_PRICE) + (totalAdults * ADULT_PRICE) +
                       (totalSeniors * SENIOR_PRICE) + (totalVIPs * VIP_PRICE);

    // Output total sales with iomanip
    cout << fixed << setprecision(2);
    cout << "\nTotal Ticket Sales after 3 days:" << endl;
    cout << "Children: " << totalChildren << endl;
    cout << "Adults: " << totalAdults << endl;
    cout << "Seniors: " << totalSeniors << endl;
    cout << "VIPs: " << totalVIPs << endl;
    cout << "Total Sales: $" << totalSales << endl;

    // End of program
    return 0;
}
