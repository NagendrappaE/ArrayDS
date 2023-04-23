# ArrayDS
jenny leacture
https://www.youtube.com/watch?v=AT14lCXuMKI&list=PLdo5W4Nhv31bbKJzrsKfMpo_grxuLl8LU


Q1.Insertion on elements in middle of list is fast in below
 A)ArrayList
 B)Linked List
 C)Vector
 D)ArrayList and Linked list Both.
 
Q2.Pls choose the correct/s statement on Vector.

A)Vector allows  to opertate  more than on thread.
B)Vector is threadsafe and hence slow.
C)Increased memory usage in vector to maintain dynamic size on adding more element .
D)All the above statements

Q3.chose the correct  output of the below program 
 
 /**
 * 
 */
package io.paycorp.programs;

import java.util.Arrays;

public class ArrayCopy {

	/**
	 * @param args
	 */
	public static void main(String[] args) {

		int old[] = { 1, 2, 3 };

		int newar[] = new int[4];
		int index = 2;

		for (int a = 0; a < old.length + 1; a++) {

			if (index == a && index <= newar.length) {
				newar[index] = 5;
				index++;
				newar[index] = old[a];
				a++;

			} else {
				newar[a] = old[a];
			}
		}

		System.out.println(Arrays.toString(newar));

	}

}


A)[1, 2, 5, 0]
B)[1, 2, 3, 0]
C)[1, 2, 5, 3]
D)Array Index Outof Bond exception


Q4)Choose the correct output of the below program.
package io.paycorp.programs;

public class ArrayImpl {

	Object[] arr = null;

	int index = 0;

	public ArrayImpl(int size) {
		arr = new Object[size];
	}

	public boolean add(Object ob) {

		if (arr.length != index) {
			arr[index] = ob;
			index++;
			return true;
		}

		return false;
	}

	public boolean add(int n, Object ob) {

		if (n <= arr.length) {
			arr[n] = ob;

			return true;
		}

		return false;

	}

}

//Main method.

		ArrayImpl arrImp = new ArrayImpl(5);
		arrImp.add(1);
		arrImp.add("one");
		arrImp.add("two");
		arrImp.add("Three");
		arrImp.add("four");
		arrImp.add(true);

		arrImp.add(2,"three");


A)Class cast Exception
B)ArrayIndex Out bond Exception
C)[1, one, three, Three, four]
D)[1, one, two, Three, four]

Q5)Which of the Map implemented class/(s) is fast in read /acces elements from  respective map.

A)HashMap
B)ConcurrentHashMap
C)Linked Hash map
D)Tree Map

Q6)Choose the correct output of below program.
package io.paycorp.programs;


public class Student {

	public Student() {
		z=40;

	}

	int z = 10;

	public void test(int z) {
		z = 20;
		System.out.println(" the values " + z);
	}

	public static void main(String[] args) {
		Student s = new Student();

		s.test(30);
	}

}


A)the values 10
B)the values 20
C)the values 30
D)the values 40
