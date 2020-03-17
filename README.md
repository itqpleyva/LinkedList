# LinkedList
Repo to Study LinkedList Collection

public class LinkedListMain {

	public static void main(String[] args) {
		
		LinkedList<String> linked = new LinkedList<String>();
		
		linked.add("First element");
		linked.add("Second element");
		linked.add("Third element");
		linked.add("Fourth element");
		linked.add("Fifth element");

		System.out.println("Printing LinkedList...");
		linked.forEach(System.out::println);
		
		
		System.out.println("Removing element by index in linkedList...");
		
		linked.remove(0);
		linked.forEach(System.out::println);
		
		System.out.println("Removing last element in linkedList...");
		
		linked.removeLast();
		linked.forEach(System.out::println);
		
		
		System.out.println("Removing first element in linkedList...");
		
		linked.removeFirst();
		linked.forEach(System.out::println);
		//Fulling linked
		
		linked.clear();
		linked.add("First element");
		linked.add("Second element");
		linked.add("Third element");
		linked.add("Fourth element");
		linked.add("Fifth element");
		
		System.out.println("Iterating linkedList...");
		System.out.println("---------------------------------------------------");
		System.out.println("using streams...");
		
		LinkedList<String> linked1 = new LinkedList<String>();
		linked.forEach(
				
				(tmp)-> {
					
					linked1.add("--" + tmp + "--");
				}		
		);
		linked1.forEach(System.out::println);
		System.out.println("---------------------------------------------------");
		System.out.println("using for...");
		for (int i = 0; i < linked.size(); i++) {
			System.out.println(linked.get(i));
		}
		System.out.println("---------------------------------------------------");
		System.out.println("using enhanced for...");
		for (int i = 0; i < linked.size(); i++) {
			System.out.println(linked.get(i));
		}
		int i = 0;
		System.out.println("---------------------------------------------------");
		System.out.println("using while...");
		while (i<linked.size()) {
			
			System.out.println(linked.get(i));
			i++;
		}
		System.out.println("---------------------------------------------------");
		System.out.println("using iterator...");
		
		Iterator<String> iterator = linked.iterator();
		Iterator<String> iterator1 = linked.descendingIterator();// to iterate in reverse
		
		while (iterator.hasNext()) {
			System.out.println(iterator.next());			
		}
		System.out.println("---------------------------------------------------");
		System.out.println("Setting element in linkedList...");
		
		linked.set(0, "First element setted");
		System.out.println(linked);
		linked.set(0, "First element");
		
		//adding a collection
		System.out.println("---------------------------------------------------");
		System.out.println("Adding a collection to linkedList...");
		
		ArrayList<String> arrayList = new ArrayList<String>();
		
		arrayList.add("array element1");
		arrayList.add("array element2");
		arrayList.add("array element3");
		arrayList.add("array element4");
		
		linked.addAll(arrayList);
		linked.forEach(System.out::println);
		System.out.println("---------------------------------------------------");
		System.out.println("Adding a collection to linkedList by index...");
		linked.addAll(1,arrayList);
		linked.forEach(System.out::println);
		
		System.out.println("---------------------------------------------------");
		System.out.println("If contains element...");
		System.out.println(linked.contains("First element"));
		System.out.println("---------------------------------------------------");
		System.out.println("index of element...");
		System.out.println(linked.indexOf("First element"));
		System.out.println("---------------------------------------------------");
		System.out.println("Clone linkedList...");
		LinkedList<String> newLinked = (LinkedList<String>) linked.clone();
		System.out.println(newLinked);
		
		System.out.println("---------------------------------------------------");
		System.out.println("get sublist...");
		System.out.println(linked.subList(1, 4));
	}

}
