Q1 solution:
//java
```java
public static int fortis1(int[] A){
	Hashtable<Integer,Integer> dic = new Hashtable<Integer,Integer>();
	int value;
	int acc = 0;
	int temp;
	for(int data : A){
		if(dic.containsKey(data)){
			value = dic.get(data);
			dic.put(data, ++value);
		}
		else{
			dic.put(data,1);
		}
	}
	for(int dicValue : dic.values() ){
		temp = (dicValue*(--dicValue))/2;
		acc += temp;
	}
	return acc;

}