**练习11：（2）创建一个类，包含一个Integer，其值通过使用java.util.Random被初始化为0到100之间的某个值。使用这个Integer域来实现Comparable。用这个类的对象
来填充PriorityQueue，然后使用poll()抽取这些值以展示该队列将按照我们预期的顺序产生这些值。**
```java
package containers;
import java.util.*;

class Item implements Comparable<Item> {
	private static Random rand = new Random(47);
	private Integer num = rand.nextInt(100);
	@Override
	public int compareTo(Item arg) {
		return arg.num > num ? 1 : (arg.num == num ? 0 : -1);
	}
	public String toString() { return String.valueOf(num); }
}

public class Ex11_PriorityQueueTest {
    static void fill(Queue<Item> queue, int quantity) {
    	for(int i = 0; i < quantity; i++)
    		queue.add(new Item());
    }
	public static void main(String[] args) {
		// TODO Auto-generated method stub
        Queue<Item> queue = new PriorityQueue<Item>();
        fill(queue, 10);
        while(!queue.isEmpty())
        	System.out.print(queue.poll() + " ");
	}

}/*Output:
93 68 61 61 58 55 29 22 7 0 
*/
```