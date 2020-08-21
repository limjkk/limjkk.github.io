---
title: "Tic Tac Toe"
date: 2020-04-07-18:00
categories:
- Cpp

tags:
- 객체지향 프로그래밍
---


Tic Tac Toe
객체지향 프로그래밍

```
#include <iostream>
#include <cstdlib>
#include <ctime>

using namespace std;
char User_Sep(int i) // 유저 구분
{
	switch (i)
	{
	case -1: // 플레이어 0
		return 'X';
	case 0:
		return ' ';
	case 1: // 플레이어 1
		return 'O';
	}
}

void Print_Board(int Board[9]) // 출력
{
	int i;
	cout << User_Sep(Board[0]) << " | " << User_Sep(Board[1]) << " | " << User_Sep(Board[2]) << endl;
	cout << User_Sep(Board[3]) << " | " << User_Sep(Board[4]) << " | " << User_Sep(Board[5]) << endl;
	cout << User_Sep(Board[6]) << " | " << User_Sep(Board[7]) << " | " << User_Sep(Board[8]) << endl;
}// Board 배열에 있는 데이터를 가져와서 User_Sep함수로 전달 후, 출력
int Check_Win(int Board[9]) // 승리 체크
{// 이기는 경우의 수를 2차원 배열로 나타냄.
	int WinBoard[8][3] = {
	{0,1,2},
	{3,4,5},
	{6,7,8},
	{0,3,6},
	{1,4,7},
	{2,5,8},
	{2,4,6},
	{0,4,8}
	}, i;
	for (i = 0; i < 8; ++i)
	{// 만약 각데이터가 2차원배열과 동일하면
		if (Board[WinBoard[i][0]] != 0 && Board[WinBoard[i][0]] == Board[WinBoard[i][1]] && Board[WinBoard[i][0]] == Board[WinBoard[i][2]])
			return Board[WinBoard[i][2]]; // 승리한 플레이어의 값을 리턴
	}// -1 : 플레이어 0 , 0 : 비어있음 , 1 : 플레이어 1
	return 0;
}
void User_Play(int Board[9])
{// 플레이어 0 : -1 | 플레이어 1 : 1
	int input, i;
	for (i = 0; i < 9; i++)
	{
		if (Check_Win(Board) != 0)
			return;
		cout << i % 2 << " 번 플레이어 차례입니다." << endl;
		Print_Board(Board);
		cin >> input;
		if (i % 2 == 0)
			Board[input] = -1; // 짝수번째 - 0번 플레이어
		else
			Board[input] = 1; // 홀수번째 - 1번 플레이어
	}
}
void Random(int Board[9])
{
	int random;
	while (1)
	{// 시드를 초기화
		srand((unsigned int)time(NULL));
		random = rand() % 8; // 0부터 8까지 난수 발생
		if (Board[random] == 0)// Board의 난수번째 인덱스에 데이터가 0이라면
		{
			Board[random] = 1; // 난수번째 인덱스에 1을 입력
			return;
		}
		else // 만약 난수번째 인덱스에 데이터가 있다면,
			continue; // 반복문을 재실행
	}
}
void AI_Play(int Board[9])
{// 인공지능과 플레이.
	int i, input;
	for (i = 0; i < 9; i++)
	{
		if (Check_Win(Board) != 0) // 게임 보드의 데이터 검사
			return; // 만약 Check_Win 의 데이터가 1또는 -1이라면 게임종료
		cout << i % 2 << " 번 플레이어 차례입니다." << endl;
		Print_Board(Board); // Print_Board 함수를 이용하여 데이터 출력
		if (i % 2 == 0) // 플레이어 0
		{
			cin >> input;// 플레이어 0 의 좌표를 입력받음
			Board[input] = -1; // 플레이어 0이 입력한 좌표에 -1 입력
		}
		else if (i % 2 == 1) // 플레이어 1(AI)
			Random(Board); // 랜덤함수를 통해 난수를 발생, 보드에 데이터를 저장
	}
}
int main()
{
	int Board[9] = { 0 }, input, win0 = 0,win1 =0 ,game = 0;
	double win_rate0 = 0, win_rate1 = 0;// 이길 확률
	while (1)
	{
		if (game > 0)
		{
			for (int i = 0; i < 9; i++)
				Board[i] = 0;
			win_rate0 = (win0 / game) * 100;
			win_rate1 = (win1 / game) * 100;
			cout << "0번 플레이어의 승률" << win_rate0 << " %"<< endl;
			cout << "1번 플레이어의 승률" << win_rate1 << " %"<< endl;
		}
		cout << "Tic Tac Toe" << endl << "1. 1대1 플레이 | 2. 인공지능과 플레이 | 3. 종료 " << endl;
		cin >> input;
		if (input == 1)
			User_Play(Board); // 사용자의 입력데이터가 1이면 1대1 플레이
		else if (input == 2)
			AI_Play(Board); // 사용자의 입력데이터가 2라면, 인공지능과 플레이
		else
			break; // break;를 통해 게임 종료
		Print_Board(Board); // 게임이 끝나면, 보드 출력
		switch (Check_Win(Board)) // 게임을 통해 Return 된 값
		{
		case -1: // 플레이어 0
		{
			game++;
			win0++;
			cout << "0번 플레이어가 승리 하였습니다."<<endl;
			break;
		}
		case 0: // 비긴경우
		{
			game++;
			cout << "비겼습니다." << endl;
			break;
		}
		case  1: // 플레이어 1이 이긴 경우
		{
			game++;
			win1;
			cout << "1번 플레이어가 승리 하였습니다."<<endl;
			break;
		}
		}
	}
}
```
