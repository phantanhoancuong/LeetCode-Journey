Author: Cuong Phan
### LeetCode Journal

| No. | Name    | Difficulty | Solution              |Notes|Time Complexity|Space Complexity|
| --- | ------- | ---------- | --------------------- |----|---|-|
| 1  | [Two Sum](https://leetcode.com/problems/two-sum/) | Easy       | [C#](./algorithms/cs/1_HashMap.cs) | C#: Use a hashmap to look up values at constant time.|C#: $O(n)$|C#: $O(n)$|
| 2  | [Add Two Numbers](https://leetcode.com/problems/add-two-numbers/) | Medium       | [C#](./algorithms/cs/2_LinkedLists.cs) | C#: Remember to check if the last addition requires a carry node|C#: $O(max(m, n))$|C#: $O(max(m, n))$|
| 3  | [Longest Substring Without Repeating Characters](https://leetcode.com/problems/longest-substring-without-repeating-characters/) | Medium       | [C#](./algorithms/cs/3_SlidingWindow.cs) | C#: Use a hashmap to to store the last visited index of a character.|C#: $O(n)$|C#: $O(min(m, n))$|
| 4  | [Median of Two Sorted Arrays](https://leetcode.com/problems/median-of-two-sorted-arrays/) | Hard      | [C#_Iterative](./algorithms/cs/4_Iterative.cs) | C# Iterative: Use two pointers to traverse the arrays until you encounter the medians.|C# Iterative: $O(m + n)$|C# Iterative: $O(1)$|
| 5  | [Longest Palindromic Substring](https://leetcode.com/problems/longest-palindromic-substring/) | Medium     | [C#](./algorithms/cs/5_CenterExpansion.cs) | C#: Use two pointers 'left' and 'right' of the substring with the ith element as its center and keep expanding by the sides as long as the string is palindromic. Remember to check the both odd and even lengths.|C#: $O(n^{2})$|C#: $O(1)$|
| 6  | [Zigzag Conversion](https://leetcode.com/problems/zigzag-conversion/) | Medium    | [C#](./algorithms/cs/6_Iterative.cs) | C#: Create an array of StringBuilder corresponding to the rows, iteratively append the characters into the StringBuilder array.|C#: $O(n)$|C#: $O(n)$|
| 7  | [Reverse Integer](https://leetcode.com/problems/reverse-integer/) | Medium    | [C#](./algorithms/cs/7_Iterative.cs) | C#: Check if underflows or overflows before adding the tail end digit to the result int iteratively using modulus.|C#: $O(log(n))$|C#: $O(1)$|
| 8  | [String to Integer (atoi)](https://leetcode.com/problems/string-to-integer-atoi/) | Medium    | [C#](./algorithms/cs/8_Iterative.cs) | C#: Skip leading whitespaces, check for sign, subtract ASCII '0' to get value, check if underflows or overflows. |C#: $O(n)$|C#: $O(1)$|
| 9  | [Palindrome Number](https://leetcode.com/problems/palindrome-number/) | Medium    | [C#](./algorithms/cs/9_MidReverse.cs) | C#: False if negative or divisible by 10 (excluding 0), reverse till middle, check if reversed = original (odd-length number) or reversed / 10 = original (even-length number). |C#: $O(log(n))$|C#: $O(1)$|
| 11  | [Container With Most Water](https://leetcode.com/problems/container-with-most-water/) | Medium    | [C#](./algorithms/cs/11_TwoPointers.cs)<br><br>[C++](./algorithms/cpp/11_TwoPointers.cpp) | C#: Use two pointers at the start and end of array, contract the container by the lower wall's side.<br><br>C++: Use two pointers at the start and end of array, contract the container by the lower wall's side. |C#: $O(n)$<br><br>C++: $O(n)$|C#: $O(1)$<br><br>C++: $O(1)$|
| 13  | [Roman to Integer](https://leetcode.com/problems/roman-to-integer/) | Easy    | [C++](./algorithms/cpp/13_Iterative.cpp) | C++: If the next numeral is larger then subtract the current one, else add it. |C++: $O(n)$|C++: $O(1)$|
| 15  | [3Sum](https://leetcode.com/problems/3sum/) | Medium    | [C++](./algorithms/cpp/15_TwoPointers.cpp) | C++: Sort the array, iterate through the array as "fixed value" then use two pointers on the subarray on the right to find the triplets. |C++: $O(n^2)$|C++: $O(1)$|
| 16  | [3Sum Closest](https://leetcode.com/problems/3sum-closest/) | Medium    | [C++](./algorithms/cpp/16_TwoPointers.cpp) | C++: Sort the array, iterate through the array as "fixed value" then use two pointers on the subarray on the right to find the triplet. |C++: $O(n^2)$|C++: $O(1)$|
| 17  | [Letter Combinations of a Phone Number](https://leetcode.com/problems/letter-combinations-of-a-phone-number/) | Medium    | [C++](./algorithms/cpp/17_Recursive.cpp) | C++: Use a recursive backtrack method. Base case if when the currentString is the same length as digits |C++: $O(3^N*4^M)$, N is the number of digits in the input string that map to 3 letters and M is the number of digits that map to 4 letters.|C++: $O(3^N*4^M)$|
| 55  | [Jump Game](https://leetcode.com/problems/jump-game/) | Medium    | [C++](./algorithms/cpp/55_Greedy.cpp) | C++: Use greedy algorithm, iterate through the vector, if current index is larger than max reach then return false else update max reach. |C++: $O(n)$|C++: $O(1)$|
| 75  | [Sort Colors](https://leetcode.com/problems/sort-colors/) | Medium    | [C++](./algorithms/cpp/75_ThreePointers.cpp) | C++: Use the Dutch National Flag (3-way partition algorithm). |C++: $O(n)$|C++: $O(1)$|
| 118  | [Pascal's Triangle](https://leetcode.com/problems/pascals-triangle/) | Easy    | [C++](./algorithms/cpp/118_Combinatorial.cpp) | C++: Initialize each row with values of 1, adjust the middle values with combinatorial formula. |C++: $O(n^2)$|C++: $O(n^2)$|
| 119  | [Pascal's Triangle II](https://leetcode.com/problems/pascals-triangle-ii/) | Easy    | [C++_TwoRows](./algorithms/cpp/119_TwoRows.cpp)<br><br>[C++_OneRow](./algorithms/cpp/119_OneRow.cpp) | C++_TwoRows: Make base rows - vector<int> prevRow(1, 1) and use two vectors to store the current row and the previous row for calculation. <br><br>C++_OneRow: Use a single row with size rowIndex + 1, calculate the middle values backwards (row[j] += row[j - 1]).|C++_TwoRows: $O(n^2)$<br><br>C++_OneRow: $O(n^2)|C++_TwoRows: $O(n)$<br><br>C++_OneRow: $O(n)$|
| 121  | [Best Time to Buy and Sell Stock](https://leetcode.com/problems/best-time-to-buy-and-sell-stock/) | Easy    | [C++](./algorithms/cpp/121_Iterative.cpp) | C++: Update minBuy and maxProfit separately. |C++: $O(n)$|C++: $O(1)$|
| 122  | [Best Time to Buy and Sell Stock II](https://leetcode.com/problems/best-time-to-buy-and-sell-stock-ii/) | Medium    | [C++](./algorithms/cpp/122_Iterative.cpp) | C++: If price is lower, update minBuy if not sell constantly. |C++: $O(n)$|C++: $O(1)$|
| 125  | [Valid Palindrome](https://leetcode.com/problems/valid-palindrome/) | Easy    | [C++](./algorithms/cpp/125_TwoPointers.cpp) | C++: Two pointers. |C++: $O(n)$|C++: $O(1)$|
| 202  | [Happy Number](https://leetcode.com/problems/happy-number/) | Easy    | [C++_UnorderedSet](./algorithms/cpp/202_UnorderedSet.cpp) | C++_UnorderedSet: Use unordered set to keep track of what sum has been seen to detect cycle.|C++_UnorderedSet: $O(log(n))$ |C++_TwoRows: $O(log(n))$|
| 345  | [Reverse Vowels of a String](https://leetcode.com/problems/reverse-vowels-of-a-string/) | Easy    | [C++](./algorithms/cpp/345_TwoPointers.cpp) | C++: Two pointers approach. |C++: $O(n)$|C++: $O(1)$|
| 383  | [Ramsom Note](https://leetcode.com/problems/ransom-note/) | Easy    | [C++](./algorithms/cpp/383_UnorderedMap.cpp) | C++: Build a map from the magazine then iterate and decrement map value by character's appearance in the ransom note. |C++: $O(m + n)$|C++: $O(m)$|
| 392  | [Is Subsequence](https://leetcode.com/problems/is-subsequence/) | Easy    | [C++](./algorithms/cpp/392_Iterative.cpp) | C++: Iterative approach. |C++: $O(n)$|C++: $O(1)$|
| 605  | [Can Place Flowers](https://leetcode.com/problems/can-place-flowers/) | Easy    | [C++](./algorithms/cpp/605_Iterative.cpp) | C++: Iterative approach, can also skip the next 1 or 2 elements if the current or the next element is occupied. |C++: $O(n)$|C++: $O(1)$|
| 1431  | [Kids With the Greatest Number of Candies](https://leetcode.com/problems/kids-with-the-greatest-number-of-candies/) | Easy    | [C++](./algorithms/cpp/1431_Iterative.cpp) | C++: Find max then build boolean vector. |C++: $O(n)$|C++: $O(1)$|
| 1768  | [Merge Strings Alternately](https://leetcode.com/problems/merge-strings-alternately/) | Easy    | [C++](./algorithms/cpp/1768_OnePointer.cpp) | C++: Use only one pointer to keep track of the indices. |C++: $O(n)$|C++: $O(1)$|
| 2037  | [Minimum Number of Moves to Seat Everyone](https://leetcode.com/problems/mininum-number-of-moves-to-seat-everyone/) | Easy    | [C++](./algorithms/cpp/2037_Sorting.cpp) | C++: Sort the arrays, then calculate the difference between the paired elements. |C++: $O(nlog(n))$|C++: $O(log(n))$|