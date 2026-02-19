Count Distinct Numbers on Board
🧩 Problem

You are given a positive integer n, that is initially placed on a board.

Every day, for 
10
9
10
9
 days, you perform the following procedure:

For each number x present on the board, find all numbers 1 <= i <= n such that:

x % i == 1


Then, place those numbers on the board.

Note:

Once a number is placed on the board, it will remain on it until the end.

% stands for the modulo operation. For example, 14 % 3 = 2.

🔹 Task

Return the number of distinct integers present on the board after 
10
9
10
9
 days.

💡 Solution
🧠 Idea

After many days, the board stabilizes.

Mathematical observation shows the result depends on powers of 2.

We compute efficiently using modular exponentiation.

✅ Python Implementation
class Solution:
    def monkeyMove(self, n: int) -> int:
        mod = 10**9 + 7
        return (pow(2, n, mod) - 2) % mod

⏱️ Complexity

Time Complexity: O(log n)

Space Complexity: O(1)

🚀 Example

Input

n = 3


Output

6
