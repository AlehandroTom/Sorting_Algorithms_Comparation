# Sorting_Algorithms_Comparation

Program Sorting Algorithms Comparation is my home project using C++.

This program has a demonstration purposes and shows the difference in PCU time and iterations requred to process defferent sorting algorithms.

Program takes data from keyboard. To add number in an array write it down and press enter. You can add as many numbers as you want. To start sorting just press enter without writing any numbers.

Program sorts data by four algorithms.

1-st - Bubble sorting. Slow, low effective but very simple to code. Nothing special. Compares two numbers and changes their places if required.

2-nd - Improved Bubble sorting. It does the same as classic version but by less iterations. Classic bubble sorting has problem with understanding that the array may be already sorted, this version solved the problem.

3-d - Insertion sorting. finds the smallest number in array and places as first element, then finds bigger than the first and places it after the smallest and so on.

4-th - Merge sorting. Works by principle "Divide and conquer". Divides array into two halves, then this halves into quarters and so on up to the moment when parts are left with one element. Then algorithm merges these parts in right order. Firstly we receive parts with two already sorted elements, then four, eight and so on.

Program counts how much time was spent on each algorithm and by how many iterations it was done.
