# Experiment-19
## AIM
To do sorting in c++.

## Problem Statement
1.) Write a c++ to do selection sorting.

2.) Write a c++ to do insertion sorting.

3.) Write a c++ to do bubble sorting.

## THEORY
A sorting algorithm arranges elements in an array or list into a specified sequence according to a comparison rule. This rule guides the algorithm in deciding if one element should precede another. Different algorithms employ unique methods to achieve the sorted order, each suited to specific situations and data types.

Selection Sort: This is a comparison-based sorting algorithm that organizes elements by iteratively selecting the smallest (or largest) element from the unsorted portion of an array and swapping it into its correct position. The array is divided into sorted and unsorted sections, with the sorted section expanding one element at a time as each smallest element from the remaining list is added in sequence.

Insertion Sort: Insertion Sort gradually constructs a sorted sequence by picking one element at a time from the unsorted section and inserting it in the correct place within the sorted portion. This process is similar to arranging playing cards in your hand, where each new card finds its correct position relative to the already sorted cards.

Bubble Sort: In Bubble Sort, elements are sorted by repeatedly comparing and swapping adjacent pairs if they are in the wrong order. With each full pass, the algorithm moves the largest unsorted element to its correct position at the end of the array. While simple and easy to implement, Bubble Sort is inefficient for large datasets due to its high time complexity.
## CODE-
1-
```javascript
//Mohit Rawat
//23070123086
#include <iostream>
using namespace std;

void swap(int *a, int *b){
    int temp;
    temp = *a;
    *a=*b;
    *b=temp;

}
void s_sort(int *a, int elements){
    int n=0;
    int *b;

    while (n!= elements){
        b = a+1; 
        for(int i = 0; i<(elements-1)-n; i++){
            if(*a > *b) {
                swap(a,b);
            }
            b++;
        }
        n++;
        a++;
    }
}
int main(){
    int no_el;
    cout << "How many elements in your array ? "<<endl;
    cin>>no_el;
    int arr[no_el];
    cout<<"Enter "<<no_el<<" Elements: "<<endl;
    for(int i=0; i<no_el;i++){
        cin>>arr[i];
    }
    cout<<"Sorted Array: ";
    s_sort(&arr[0],no_el);

    for(int i=0; i<no_el;i++){
        cout<<arr[i]<< " ";

    }
    return 0;


}
```
2-
```javacsript
//Mohit Rawat
//23070123086
#include <iostream>
using namespace std;

void insertionsort(int arr[], int n){
    for (int i = 1; i<n ; i++){
        int key = arr [i];
        int j =i-1;

        while (j>= 0 &&  arr[j]>key){
            arr[j+1] = arr[j];
            j--;
        }
        arr[j+1]= key;
    }
}
int main(){
    int arr[]= {64, 25, 12,22,11};
    int n = sizeof(arr) / sizeof(arr[0]);
    cout<< "Original array: ";
    for (int i =0; i<n;i++){
        cout<<arr[i]<<" ";
    }
    insertionsort(arr,n);
    cout<< "\n Sorted array: ";
    for (int i = 0; i< n ; i++){
        cout << arr[i]<<" ";
    }
    return 0;
    }
```
3-
```javacsript
//Mohit Rawat
//23070123086
#include<iostream>
using namespace std;

void swap(int* a,int* b){
int temp;
 temp=*a;
*a=*b;
 *b=temp;
}
int main(){
 int elements;
  cout<<"How many elements in the array? :";
  cin>>elements;
   int array[elements];
 cout<<"Enter elements:";
for(int i=0;i<elements;i++){
 cin>>array[i];
 }
for(int i=0;i<elements;i++){
 cout<<array[i]<<" ";
  }
 int n=0;
while(n!=elements){
 for(int i=0;i<elements-n;i++){
if(array[i]>array[i+1]){
swap(&array[i],&array[i+1]);
 }
}
 n++;
 }
 cout<<"\nSorted array is:"<<endl;
for(int i=0;i<elements;i++){
 cout<<array[i]<<" ";
 }

 return 0;
}
```

## OUTPUTS-
1- <img width="377" alt="image" src="https://github.com/user-attachments/assets/068c66d8-3883-4cf3-82d3-8084a3769157">

2- <img width="334" alt="image" src="https://github.com/user-attachments/assets/319abfd5-b418-45bf-8ce3-f65b8503f159">

3- <img width="371" alt="image" src="https://github.com/user-attachments/assets/8eaf9d46-faa7-4711-a95a-8598fe795045">

## CONCLUSION-
We learnt about selection, insertion and bubble sort.




