#include <stdlib.h>
#include <stdio.h>
#define row 3
#define colume 3
#define _CRT_SECURE_NO_WARNINGS

int main()
{
	int x, y, right = 0, left = 0, counter=1;
	int sum;
	printf("please enter %d x %d numbers.\n", row, colume);
	int mtrx[row][colume];

	for (x = 0; x < row; x++)
	{
		for (y = 0; y < colume; y++)
		{
			scanf_s("%d", &mtrx[x][y]);
		}
	}
	
	for (x = 0; x < row; x++)
	{
		for (y = 0; y < colume; y++)
		{
		
			if (y == x) // החוקיות של האלכסון הראשון
			{
				right = (mtrx[x][y] + right); // אפשר להשתמש ב+= במקום לעשות את אותו הערך פעמיים...
			}


			if (x + y == row - 1) //החוקיות של האלכסון השני
			{
				left = (mtrx[x][y] + left);
			}
			

		}
	}

	printf(" %d and %d are... \n", left, right);
	if (left == right)
		printf("Equal!\n");
	else
		printf("Not Equal!\n");


	system("pause");

}
