# Experiment-7
#include <stdio.h>
float totalBill(float *price, int n) {
if (n == 0)
return 0;
return price[n - 1] + totalBill(price, n - 1);
}
int main() {
float items[10];
int i;
printf("Enter prices of 10 items in the shop:\n");
for (i = 0; i < 10; i++) {
printf("Enter price of item %d: ", i + 1);
scanf("%f", &items[i]);
}
float bill = totalBill(items, 10);
printf("\n===========================\n");
printf(" SHOP BILL\n");
printf("===========================\n");
printf("Total Bill for 10 Items = ₹%.2f\n", bill);
printf("===========================\n");
return 0;
}

