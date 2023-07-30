import java.util.*;

public class Solution {
	public static void f(int node, HashMap<Integer,ArrayList<Integer>> map,ArrayList<Integer> storeDfs,boolean[] visited){
		storeDfs.add(node);
		visited[node] = true;
		for(Integer it:map.get(node)){
			if(!visited[it]){
				f(it,map,storeDfs,visited);
			}
		}
		
	}
    public static ArrayList<ArrayList<Integer>> depthFirstSearch(int v, int e, ArrayList<ArrayList<Integer>> edges) {
        // Write your code here.
		HashMap<Integer,ArrayList<Integer>> map = new HashMap<>();
		for(int i=0;i<v;i++){
			map.put(i,new ArrayList<>());
		}
		
		for(int i=0;i<edges.size();i++){
			map.get(edges.get(i).get(0)).add(edges.get(i).get(1));
			map.get(edges.get(i).get(1)).add(edges.get(i).get(0));
		}
		//System.out.println(map);
		boolean[] visited = new boolean[v];
		for(int i=0;i<v;i++) visited[i] = false;
		
		ArrayList<ArrayList<Integer>> ans = new ArrayList<>();
		int count=0;
	
		
		for(int i=0;i<v;i++){
			
			
			if(!visited[i]){
				ArrayList<Integer> storeDfs = new ArrayList<>();
				count++;
				f(i,map,storeDfs,visited);
				if(storeDfs.size()==0) continue;
				ans.add(storeDfs);
			}
			
		}
		
		return ans;
    }
}
