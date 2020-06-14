---
title: "Linked List 01"
type: post
permalink: /study/java/Linked_List
category: 
    - STUDY
        - etc
tag:
    - java
    - Data Structure
use_math: true
toc: ture
siderbar_main: true
---
본 글은 [엔지니어대한민국](https://www.youtube.com/user/damazzang)를 참고하여 작성하였습니다.

# Linked List
`Linked List`를 이해하기 위해선 일단 `Array`를 알아야한다.  

**Array**  
- 변수가 선언 되고 나서 크기 변경 불가
- 메모리 상에서 물리적으로 연결 돼 있음
- 저장 된 순서에 따라 값을 추출 할 수 있음

**Linked List**  
- 변수가 선언 되고 나서 크기 변경 가능
- 메모리 상에서 물리적으로 연결 돼 있지 않음
- 하나의 `list`가 값과 다음 `list`의 주소를 저장하고 있음

## Linked List 단/양 방향

**단방향**  
- 다음 `list`의 주소값 보유

**양방향**  
- 이전의 `list`의 주소값과 다음 `list`의 주소값 보유
- `list` 삽입 시 : 이전 `list`의 주소값과 다음 `list`의 주소값 보유
- `list` 삭제 시 : 다음 `list`의 주소값을 이전 `list`의 주소값에 할당, 이전 `list`의 주소값을 다음 `list`의 할당

### 구현 in Java (단방향)
```java
class Node {
	int data;
	Node next = null;

	Node(int d) {
		this.data = d;
	}

	void append(int d) {
		Node end = new Node(d);
		Node n = this;
		while (n.next != null) {
			n = n.next;
		}
		n.next = end;
	}

	void delete(int d) {
		Node n = this;
		while (n.next != null) {
			if (n.next.data == d) {
				n.next = n.next.next;
			} else {
				n = n.next;
			}
		}
	}

	void retrieve() {
		Node n = this;
		while (n.next != null) {
			System.out.print(n.data + " -> ");
			n = n.next;
		}
		System.out.println(n.data);
	}
}
```

```java
public class SinglyLinkedList {
	public static void main(String[] args) {
		Node head = new Node(1);
		head.append(2);
		head.append(3);
		head.append(4);
		head.retrieve();
	}
}
```

```java
public class SinglyLinkedList {
	public static void main(String[] args) {
		Node head = new Node(1);
		head.append(2);
		head.append(3);
		head.append(4);
		head.retrieve();
        head.delete(2);
        head.retrieve();
	}
}
```
