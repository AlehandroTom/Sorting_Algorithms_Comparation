# Sorting_Algorithms_Comparation

Hi there!

Program Sorting Algorithms Comparation, or SAC is my home project at C++.

By first look, this program is very simple, but it can be easily rebuilt into more powerful tool for sorting big amount of data from file, database or something else. It is not limited in data amount and can take as much as you want to give. In addition, it can compare which algorithm is better suited for your purposes.

Let's take a look on what it can do.

Program in that version takes data from keyboard. To add number in array to be sorted write it down and press enter, after that number will be added to the array. Add next number and the next... As many numbers as you want. To start sorting just press enter without writing any numbers and sorting will begin.

Program sorts data by four algorithms.

1-st - Bubble sorting. Slow, low effective but very simple to code. Nothing special. Compares two numbers and changes their places if required.

2-nd - Improved Bubble sorting. It does the same as classic version but by less iterations. Classic bubble sorting has problem with understanding that the array may be already sorted, this version solved the problem.

3-d - Insertion sorting. finds the smallest number in array and places as first element, then finds bigger than the first and places it after the smallest and so on.

4-th - Merge sorting. Works by principle "Divide and conquer". Divides array into two halves, then this halves into quarters and so on up to the moment when parts are left with one element. Then algorithm merges these parts in right order. Firstly we receive parts with two already sorted elements, then four, eight and so on.

Program counts how much time was spent on each algorithm and by how many iterations it was done.
