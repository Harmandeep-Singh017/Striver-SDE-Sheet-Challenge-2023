import java.util.* ;
import java.io.*; 
public class Solution {

	static int kthLargest(ArrayList<Integer> arr, int size, int k) {
		// Write your code here.
		PriorityQueue<Integer> pq = new PriorityQueue<>(size, Collections.reverseOrder());
		for (int i : arr)
			pq.offer(i);
		for(int i =0;i<k-1;i++)
			pq.poll();
		return pq.peek();
	}
}
