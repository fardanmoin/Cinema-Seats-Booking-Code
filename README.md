# Cinema-Seats-Booking-Code

// Online C++ compiler to run C++ program online
#include <iostream>
using namespace std; 

int main() {
    int r = 3;
    int c = 4;
    
    char seats[3][4] = {
        {'R','F','R','R'},
        {'R','F','F','F'},
        {'F','R','F','F'}
    };

    cout<<"Please see the updated bookings below: "<<endl;
    for (int i=0; i<r; i++) {
        for (int j=0; j<c; j++) {
            cout<<"("<<i+1<<" "<<j+1<< " " << seats[i][j]<<") ";
        }
        cout<<endl<<endl;
    }

    int row, col;
    cout<<"Enter row number to reserve: ";
    cin>>row;
    cout<<"Enter column number to reserve: ";
    cin>>col;

    row = row - 1; 
    col = col - 1; 

    if (seats[row][col] == 'R') {
        cout<<"This seat is already reserved."<< endl;
    } else {
        seats[row][col] = 'R';
        cout<<"Seat reserved successfully."<< endl;
    }
    cout<<"Updated bookings: "<<endl;
    for (int i=0; i<r; i++) {
        for (int j=0; j<c; j++) {
            cout<<"("<<i+1<<" "<<j+1<< " " << seats[i][j]<< ") ";
        }
        cout<<endl<<endl;
    }

    return 0;
}
