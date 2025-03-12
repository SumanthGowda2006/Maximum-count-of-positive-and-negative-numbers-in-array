# Maximum-count-of-positive-and-negative-numbers-in-array

#include <stdio.h>

int maximumCount(int nums[], int size) {
    int pos = 0, neg = 0;
    for (int i = 0; i < size; i++) {
        if (nums[i] > 0) {
            pos++;  
        } else if (nums[i] < 0) {
            neg++;  
        }
    }
    return (pos > neg) ? pos : neg;
}

int main() {
    int nums[] = {1, -2, 3, -4, 0, 5, -6};  // Example array
    int size = sizeof(nums) / sizeof(nums[0]);

    int result = maximumCount(nums, size);
    printf("Maximum count of positives or negatives: %d\n", result);

    return 0;
}
