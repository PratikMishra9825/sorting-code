#include <iostream>
#include <vector>
using namespace std;

void Sort0s1s2s(vector<int> &arr) {
    int low = 0, mid = 0, high = arr.size() - 1;

    while (mid <= high) {
        if (arr[mid] == 0) {
            swap(arr[low], arr[mid]);
            low++;
            mid++;
        }
        else if (arr[mid] == 1) {
            mid++;
        }
        else { // arr[mid] == 2
            swap(arr[mid], arr[high]);
            high--;
        }
    }
}
int main() {
    vector<int> arr = {2, 0, 2, 1, 1, 0};
    Sort0s1s2s(arr);
    for (int num : arr) {
        cout << num << " ";
    }
    cout << endl;
    return 0;
}

