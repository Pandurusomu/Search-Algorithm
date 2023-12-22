# Linear Search and Binary search
## Aim:
To write a program to perform linear search and binary search using python programming.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
## Linear Search:
1.	Start from the leftmost element of array[] and compare k with each element of array[] one by one.
2.	If k matches with an element in array[] , return the index.
3.	If k doesn’t match with any of elements in array[], return -1 or element not found.
## Binary Search:
1.	Set two pointers low and high at the lowest and the highest positions respectively.
2.	Find the middle element mid of the array ie. arr[(low + high)/2]
3.	If x == mid, then return mid.Else, compare the element to be searched with m.
4.	If x > mid, compare x with the middle element of the elements on the right side of mid. This is done by setting low to low = mid + 1.
5.	Else, compare x with the middle element of the elements on the left side of mid. This is done by setting high to high = mid - 1.
6.	Repeat steps 2 to 5 until low meets high
## Program:
i)	#Use a linear search method to match the item in a list.
```
''' 
Program for linear search method to match the item in a list
Developed by: Panduru somu
RegisterNumber: 23005083
'''
def linearsearch(array,n,k):
    for i in range(0,n):
        if(array[i] == k ):
            return i
    return 0 
array = eval(input())
k = eval(input())
n = len(array)
array.sort()
result= linearsearch(array,n,k)
if(result == 0):
    print(array)
    print("Element not found")
else :
    print(array)
    print("Element found at index: ",result)
```
ii)	# Find the element in a list using Binary Search(Iterative Method).
```
''' 
Program to find the element in a list using Binary Search(Iterative Method)..
Developed by: Panduru somu
RegisterNumber: 23005083
'''
list_1 = eval(input())
list_1.sort()
n = int(input())
lower=0
upper = len(list_1)-1
result = -1
print(list_1)
while(upper>=lower):
    mid=(lower+upper)//2
    if(list_1[mid]==n):
        result = mid
        break
    else:
        if(list_1[mid]>n):
            upper = mid-1
        elif(list_1[mid]<n):
            lower = mid+1
if(result==-1):
    print("Element not found")
else:
    print(f"Element found at index:  {result}")

```
iii)	# Find the element in a list using Binary Search (recursive Method).
```
''' 
Program to find the element in a list using Binary Search (recursive Method).
Developed by: Panduru somu
RegisterNumber: 23005083 
'''
def binarysearch(arr , k , low , high):
    if high>= low:
        mid = (low+high)//2
        if arr[mid] == k:
            return print(f"Element found at index:  {mid}")
        elif arr[mid] > k:
            return  binarysearch(arr , k , low , mid-1)
        elif arr[mid]<k:
            return binarysearch(arr , k , mid+1 , high)
    else:
        print("Element not found")
list_1 = eval(input())
list_1.sort()
n = int(input())
lower=0
upper = len(list_1)-1
print(list_1)
binarysearch(list_1,n,lower,upper);
```
## Sample Input and Output
![Screenshot 2023-12-22 093625](https://github.com/Pandurusomu/Search-Algorithm/assets/148988619/afe21591-c666-4db4-8145-ac35e01ac9e6)
![Screenshot 2023-12-22 093651](https://github.com/Pandurusomu/Search-Algorithm/assets/148988619/1d039eee-8317-41b4-8e55-87c76eee27e2)
![Screenshot 2023-12-22 093718](https://github.com/Pandurusomu/Search-Algorithm/assets/148988619/2921605c-2f43-48b7-9285-c232868fa01e)






## Result
Thus the linear search and binary search algorithm is implemented using python programming.
