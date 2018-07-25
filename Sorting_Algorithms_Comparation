#include <iostream>
#include <vector>
#include <ctime>
#include "cstring"
#include <string>
using namespace std;

vector <string> v;
vector <int> MyVector;
int iter2 = 0;

int counter;

void VectorFunct() { // function for filling in vector from keyboard

	cout << "Write down integer number and press enter to add it to an array. Write as many elements as you want." << endl << "To start sorting just press enter without filling in line" << endl;
	unsigned int vector_size = MyVector.size(); // Defining vector size
	string buffer = ""; // declaration for temporary buffer to contatin string of numbers
	do { // start cycle to fill in string buffer
		getline(cin, buffer);
		if (buffer.size() > 0) {
			int num1 = stoi(buffer, 0, 0); // transition string to int
			MyVector.push_back(num1); // recording to vector
		}
	} while (buffer != ""); // allows finish filling in vector by pressing enter
	cout << "Here is your unsorted array:" << endl;
	// start cycle to output vector
	for (int i = 0; i < MyVector.size(); ++i) {
		cout << MyVector[i] << " ";

	}
	cout << endl << endl;
}

void BubblesortFunct() { // function for bubble sorting algorithm
	vector <int> TempVec(MyVector);

	int tempbubble1; // temporary local
	int iter = 0; // local for counting cycle iterations
	cout << "Bubbles Sorting Algorithm" << endl << endl;
	for (int i = 0; i < TempVec.size(); i++) { // external cycle for sorting
		for (int j = 0; j < TempVec.size() - 1; j++) { // internal cycle for sorting
			if (TempVec[j] > TempVec[j + 1]) {
				tempbubble1 = TempVec[j]; // record smaller value to temp local
				TempVec[j] = TempVec[j + 1]; // change smaller value to bigger
				TempVec[j + 1] = tempbubble1; // change bigger value to smaller
			}
			iter++;
		}
	}
	cout << "Here is your sorted array:" << endl; // output sorted vector
	for (int i = 0; i < TempVec.size(); i++) {
		cout << TempVec[i] << " ";
	}
	cout << endl << endl << "Iterations - " << iter << endl;
}

void InprBubblesortFunct() { // function for inmproved bubble sorting algorithm
	vector <int> TempVec(MyVector);
	cout << "Improved Bubbles Sorting Algorithm" << endl << endl;
	int tempbubble1; // temporary local
	int iter = 0; // local for counting cycle iterations
	for (int i = 0; i < TempVec.size(); i++) { // external cycle for sorting
		int fbreak = 0;
		for (int j = 0; j < TempVec.size() - 1; j++) { // internal cycle for sorting
			if (TempVec[j] > TempVec[j + 1]) {
				tempbubble1 = TempVec[j]; // record smaller value to temp local
				TempVec[j] = TempVec[j + 1]; // change smaller value to bigger
				TempVec[j + 1] = tempbubble1; // change bigger value to smaller

				fbreak++;
			}
			iter++;
		}
		if (fbreak == 0) {
			i = TempVec.size(); // breacking external cycle when all components already sorted 
		}
	}
	cout << "Here is your sorted array:" << endl; // output sorted vector
	for (int i = 0; i < TempVec.size(); i++) {
		cout << TempVec[i] << " ";
	}
	cout << endl << endl << "Iterations - " << iter << endl;
}

void InsertionSort2() {
	vector <int> TempVec(MyVector);
	cout << "Insertion Sorting Algorithm" << endl << endl;
	int VectorIndex, TempInsert, min;
	int iter = 0; // local for counting cycle iterations

	for (int i = 0; i < TempVec.size(); i++) { // external cycle
		min = TempVec[i]; // setting min value equal to the first array element
		VectorIndex = i; // recording index of the min value
		for (int j = 0; j < TempVec.size() - 1; j++) { // internal cycle
			if (min < TempVec[j]) {
				min = TempVec[j]; // need to quit internal cycle
				// changing min value and bigger value places
				VectorIndex = j;
				TempInsert = TempVec[VectorIndex];
				TempVec[VectorIndex] = TempVec[i];
				TempVec[i] = TempInsert;
			}
			// changing min value and bigger value places

		}

		iter++;
	}

	cout << "Here is your sorted array:" << endl; // output sorted vector
	for (int i = 0; i < TempVec.size(); i++) {
		cout << TempVec[i] << " ";
	}
	cout << endl << endl << "Iterations - " << iter << endl;
}

void merge(int arr[], int left, int middle, int right) // merges two sub arrays
{
	int i, j, k;
	int n1 = middle - left + 1;
	int n2 = right - middle;
	// temporary arrays
	int *L = new int[n1];
	int *R = new int[n2];

	// Copy data to temp arrays L[] and R[] 
	for (i = 0; i < n1; i++)
		L[i] = arr[left + i];
	for (j = 0; j < n2; j++)
		R[j] = arr[middle + 1 + j];

	// Merge the temp arrays back into arr[l..r]
	i = 0; // Initial index of first subarray
	j = 0; // Initial index of second subarray
	k = left; // Initial index of merged subarray
	while (i < n1 && j < n2)
	{
		if (L[i] <= R[j])
		{
			arr[k] = L[i];
			i++;
		}
		else
		{
			arr[k] = R[j];
			j++;
		}
		k++;
	}

	//Copy the remaining elements of L[], if there are any
	while (i < n1)
	{
		arr[k] = L[i];
		i++;
		k++;
	}

	//Copy the remaining elements of R[], if there are any
	while (j < n2)
	{
		arr[k] = R[j];
		j++;
		k++;
	}
}

void mergeSort(int arr[], int left, int right) //left is for left index and right is for right index of the sub - array of arr to be sorted
{

	if (left < right)
	{
		int middle = (left + right) / 2; // devides array into two parts

		// Sort first and second halves
		mergeSort(arr, left, middle);
		mergeSort(arr, middle + 1, right);

		merge(arr, left, middle, right);
		iter2++;
	}
}

int main() {

	VectorFunct(); // start function to fill in vector form keyboard

	unsigned int start_time = clock();

	// start Bubble Sorting

	cout << "******************************************************" << endl;
	BubblesortFunct();

	unsigned int end_time = clock();
	unsigned int search_time = end_time - start_time;
	cout << "Start time sorting = " << start_time << "ms" << endl;
	cout << "End time sorting = " << end_time << "ms" << endl;
	cout << "Runtime = " << search_time << "ms" << endl << endl;

	// start improved Bubble Sorting

	cout << "******************************************************" << endl;
	start_time = clock();
	InprBubblesortFunct();
	end_time = clock();
	search_time = end_time - start_time;
	cout << "Start time sorting = " << start_time << "ms" << endl;
	cout << "End time sorting = " << end_time << "ms" << endl;
	cout << "Runtime = " << search_time << "ms" << endl << endl;

	// start Insertion sorting

	cout << "******************************************************" << endl;
	start_time = clock();
	InsertionSort2();
	end_time = clock();
	search_time = end_time - start_time;
	cout << "Start time sorting = " << start_time << "ms" << endl;
	cout << "End time sorting = " << end_time << "ms" << endl;
	cout << "Runtime = " << search_time << "ms" << endl << endl;

	// start merge sorting

	cout << "******************************************************" << endl;
	cout << "Merge Sorting Algorithm" << endl << endl;

	start_time = clock();
	int *MyArr = new int[MyVector.size()];
	for (int i = 0; i < MyVector.size(); i++) {
		MyArr[i] = MyVector[i];
	}
	
	mergeSort(MyArr, 0, MyVector.size() - 1);

	cout << "Here is your sorted array:" << endl;
	for (int i = 0; i < MyVector.size(); i++)
	{
		cout << MyArr[i] << " ";
	}
	end_time = clock();
	search_time = end_time - start_time;
	cout << endl << endl << "Iterations - " << iter2 << endl;
	cout << "Start time sorting = " << start_time << "ms" << endl;
	cout << "End time sorting = " << end_time << "ms" << endl;
	cout << "Runtime = " << search_time << "ms" << endl << endl;
	cout << "******************************************************" << endl;
	system("Pause");

	return 0;
}
