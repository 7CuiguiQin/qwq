# qwq
自我介绍.ixx
#include<stdio.h>
#include<time.h>
#include<stdlib.h>
int main()
{
	int magic, guess, counter = 0, ret;
	char reply;
	srand(time(NULL));
	magic = rand() % 100 + 1;
	do {
		printf("Please guess a magic number:");
		scanf_s("%d", &guess);
		counter++;
		if (guess > magic) {
			printf("Wrong! Bigger than right!\n");
		}
		else if (guess < magic) {
			printf("Wrong! Smaller than right!\n");
		}
		else
			printf("Right!");
	} while (guess != magic && counter < 20);
	printf("counter=%d\n", counter);
	switch (counter)
	{
	case 0:
		printf("level:天选之人！");
		break;
	case 1:
	case 2:
	case 3:
		printf("level:运气真好！");
		break;
	case 4:
	case 5:
	case 6:
		printf("level:正常水平！");
		break;
	case 7:
	case 8:
	case 9:
		printf("level:有脑子？");
		break;
	default:
		printf("level:rz不配玩这游戏！");
		break;
	}
	return 0;
}
