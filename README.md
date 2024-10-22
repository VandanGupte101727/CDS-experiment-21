# CDS-experiment-21
c plus plus and data structures experiment 21

AIM:- to learn and implement searching algorithms(binary and linear)<br>

Software used:- VS code<br>

Theory:-<br>
Linear search:-Linear search is a simple algorithm that sequentially checks each element of a list until it finds the target value or reaches the end. It's used when the list is unsorted or small. The search starts from the first element and proceeds to the last, comparing each one with the target. If a match is found, its index is returned; otherwise, the search ends with no match.Time complexity O(n) as there are n no. of elements <br>
Binary search:-Binary search is an efficient algorithm used to find a target element in a sorted array. It repeatedly divides the search interval in half. The search begins by comparing the middle element with the target. If the target matches, the search ends. If the target is smaller, the search continues in the left half; otherwise, it proceeds in the right half. This process is repeated until the target is found or the interval is empty.<br>
1).Start by comparing the target element with the middle element of the array.<br>
2).If the target element matches the middle element, return the index.<br>
3).If the target element is smaller, repeat the search on the left half of the array.<br>
4).If the target element is larger, repeat the search on the right half of the array.<br>
5).Continue this process until the target element is found or the sub-array is reduced to size zero.<br>

CODE:-<br>

    #include <iostream>
    using namespace std;

    int linearSearch(int arr[], int n, int key) {
    for (int i = 0; i < n; i++) {
        if (arr[i] == key)
            return i;
    }
    return -1;
    }
  
    int main() {
    int arr[] = {10,17,27,72,4};
    int n = sizeof(arr) / sizeof(arr[0]);
    int key = 27;
    int result = linearSearch(arr, n, key);
    
    if (result != -1)
        cout << "Element found at index: " << result;
    else
        cout << "Element not found.";

    return 0;
    }

