#include <iostream>
#include <vector>
using namespace std;
template<class T>
class Maxheap 
{
private:
	// vector to store heap elements
	vector<int> heap;
public:
	// function to check if heap is empty or not/*Complexcity==o(1)*/
	bool empty()
	{
		return size() == 0;
	}
    // return size of the heap/*Complexcity==o(1)*/
	int size()
	{
		return heap.size();
	}
	// return parent of heap[i]/*Complexcity==o(1)*/
    // don't call this function if i is already a root node
	int PARENT(int i)
	{
		return (i - 1) / 2;
	}
	// return left child of heap[i]/*Complexcity==o(1)*/
	int LEFT(int i)
	{
		return (2 * i + 1);
	}
	// return right child of heap[i]/*Complexcity==o(1)*/
	int RIGHT(int i)
	{
		return (2 * i + 2);
	}
    // insert key into the heap/*Complexcity==o(1)*/
	void push(T key)
	{
		// insert the new element to the end of the vector
		heap.push_back(key);

		// get element index and call heapify-up procedure
		int index = size() - 1;
		heapify_up(index);
	}
	// function to remove element with highest priority (present at root)/*Complexcity==o(1)*/
	T pop()
	{
		if (empty())
			throw exception("Empty Array");
		int temp = heap[0];
		heap.erase(heap.begin());
		//size();
		return temp;
	}
    // function to return element with highest priority (present at root)/*Complexcity==o(1)*/
 	T getMax()
	{
		return heap[0];
	}
    // Recursive Heapify-up algorithm/*Complexcity==o(1)*/
	void heapify_up(int i)
	{
		// check if node at index i and its parent violates 
		// the heap property
		if (i && heap[PARENT(i)] < heap[i])
		{
			// swap the two if heap property is violated
			swap(heap[i], heap[PARENT(i)]);

			// call Heapify-up on the parent
			heapify_up(PARENT(i));
		}
	}
    // prints the heap/*Complexcity==o(n)*/
	void printHeap() 
	{
		for (int i = 0; i < size(); i++)
		{
			cout <<heap [i]<<endl;
		}
		cout << endl;
	}
};
