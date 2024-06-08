# Replace-Array
Replace the array such that arr[i] element gets replaced with arr[arr[i]]
//Make the array as arr[i] gets replaced by arr[arr[i]]
#include<iostream>
using namespace std;

int main(){
	int n;
	cout<<"Enter the size: ";
	cin>>n;
	int arr[n];
	for(int i=0;i<n;i++){
		cin>>arr[i];
	}
	int j=0;
	for(int i=0;i<n;i++){
		int temp=arr[i];
		arr[i]=arr[arr[j]];
		arr[arr[j]]=temp;
		j++;
	}
	for(int i=0;i<n;i++){
		cout<<arr[i]<<" ";
	}
}
