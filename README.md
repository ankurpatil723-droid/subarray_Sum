#include <bits/stdc++.h>
using namespace std;

int main()
{
    int n;

    cout << "Enter size of array: ";
    cin >> n;

    int arr[10];

    cout << "Enter elements of array: ";
    for (int i = 0; i < n; i++)
    {
        cin >> arr[i];
    }

    int key;
    cout << "Enter key: ";
    cin >> key;

    int count = 0;

    // Check pairs
    for (int i = 0; i < n; i++)
    {
        for (int j = i + 1; j < n; j++)
        {
            int sum = arr[i] + arr[j];

            if (sum == key)
            {
                count++;
            }
        }
    }

    cout << "Total pairs with sum " << key << " = " << count;

    return 0;
}
