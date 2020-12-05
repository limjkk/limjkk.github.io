---
title: "[C++/Python] 버블정렬"
date: 2020-12-05-19:00
categories:
- Data Structure

tags:
- Data Structure
---

# 버블 정렬
![이미지](/images/datastructure/bubble sort/1.gif)
출처 : https://upload.wikimedia.org/wikipedia/commons/0/06/Bubble-sort.gif


---
# 파이썬 코드
```
Array = [5,3,6,1,8,7,2,4] # 정렬되지 않은 Array

for i in range(0,len(Array)): # 0부터 Array 길이까지 반복
    for j in range(0,(len(Array)-1)-i): # 0부터 ((Array 길이-1) - i)번 반복
        if (Array[j] > Array[j+1]):
            Array[j],Array[j+1] = Array[j+1],Array[j] # Swap


print(Array) # 출력
```
# C++ 코드
```
#include <iostream>

using namespace std;

int main()
{
	int array[] = { 5,3,6,1,8,7,2,4 };
	int swap = 0;
	for (int i = 0; i < 10; ++i)
	{
		for (int j = 0; j < 9 - i; ++j)
		{
			if (array[j] > array[j + 1])
			{
				swap = array[j];
				array[j] = array[j + 1];
				array[j + 1] = swap;
			}
		}
	}
	for (int i = 0; i < 10; i++)
	{
		cout << array[i];
	}
}
```
