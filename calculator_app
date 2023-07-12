#include <iostream>
#include <ctype.h>

void decimalToBinHex (int num){
    if (num == 0) {
        printf("Binary representation: 0\n");
        return;
    }

    int binary[32];  // Assuming a 32-bit integer
    int i = 0;
    int hnum = num;

    while (num > 0) {
        binary[i] = num % 2;
        num /= 2;
        i++;
    }
    printf("Binary: ");
    for (int j = i-1; j >= 0; j--) {
      printf("%d", binary[j]);
    }
    printf("\n");
    printf("Hexadecimal: %x\n", hnum);
}

int main() {
    int num1, num2, num3;
    char oper, programmer;
    

    printf ("What would you like to do?\n");
    printf ("Type 'C' for convert number; 'M' for basic math\n");
    scanf ("%c", &programmer);
    programmer = tolower(programmer);
    
    switch (programmer){
        case 'c':
            printf ("Enter the integer value you want to convert:");
            scanf ("%d", &num3);
            decimalToBinHex(num3);
            break;
        case 'm':
            printf ("Enter first number: ");
            scanf ("%d", &num1);
            printf ("Enter an operator (+, -, *, /): ");
            scanf ("%c", &oper);
            printf ("Enter second number: ");
            scanf ("%d", &num2);
    
            switch (oper){
                case '+':
                  printf ("%d + %d = %d\n", num1, num2, num1 + num2);
                  break;
                case '-':
                  printf ("%d - %d = %d\n", num1, num2, num1 - num2);
                  break;
                case '*':
                  printf ("%d * %d = %d\n", num1, num2, num1 * num2);
                  break;
                case '/':
                  if (num2 != 0)
                    printf ("%d / %d = %.2f\n", num1, num2, (float) num1 / num2);
                  else
            	    printf ("Error: Division by zero\n");
                  break;
                default:
                  printf ("Error: Invalid operator\n");
                  break;
            }
        default:
            printf ("Error: Invalid option.\n");
            break;
    }
    
  return 0;
}
