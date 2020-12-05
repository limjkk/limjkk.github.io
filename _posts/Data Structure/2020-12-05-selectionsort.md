---
title: "[C++/Python] 선택정렬"
date: 2020-12-05-19:00
categories:
- Data Structure

tags:
- Data Structure
---

# 선택 정렬
![이미지](/images/datastructure/selection sort/1.gif)
출처 : https://i2.wp.com/algorithms.tutorialhorizon.com/files/2019/01/Selection-Sort-Gif.gif?ssl=1


---
# 파이썬 코드
```
Array = [5,3,4,1,2] # 정렬되지 않은 Array

for i in range(0,len(Array)):
    for j in range(i,len(Array)):
        if Array[i] > Array[j]:
            Array[i],Array[j] = Array[j],Array[i]
print(Array)



print(Array) # 출력
```
# C++ 코드
```
#include <iostream>

using namespace std;

int main()
{
	int array[] = { 5,3,4,1,2 };
	int swap = 0;
	for (int i = 0; i < 5; ++i)
	{
		for (int j = i; j <5; ++j)
		{
			if (array[i] > array[j])
			{
				swap = array[i];
				array[i] = array[j];
				array[j] = swap;
			}
		}
	}
	for (int i = 0; i < 5; i++)
	{
		cout << array[i];
	}
}
```
