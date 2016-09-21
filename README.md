# Sort
#排序

// 冒泡
void Bubble(int *arr, int length)
{
    for(int i=0; i<length; i++)
    {
	for(int j=length-1; j>=i; j--)
	{
	    if(arr[j+1] > arr[j])
	    {
		swap(arr[j+1, j]);
 	    }
	}
    }
}

// 快排
 void Qsort(int *arr, int low, int high)
 {
 	int left = low;
 	int right = high;
 	int pivotpos = arr[left];
 	while(left < right)
 	{
 		while(left<right && arr[right] > pivotpos)
 		{
 			right--;
 		}
 		arr[left] = arr[right];
 		while(left<right && arr[left] < pivotpos)
 		{
 			left++;
 		}
 		arr[right] = arr[left];
        arr[left] = pivotpos;
        Qsort(arr, low, left-1);
        Qsort(arr, left+1, high);
 	}
 }
 void QuickSort(int *arr, int n)
 {
 	Qsort(arr, 0, n);
 }
