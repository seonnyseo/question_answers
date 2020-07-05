
June 29, 2020 
- Missed Questions

Q1. How Python Garbage Collector works ?

Answer

1. Reference Counting

Python의 모든 객체는 참조 될 때마다 Reference Counter가 증가하고, 참조가 없어질 때 감소한다. 객체의 Reference Counter가 0이 되면 메모리에서 해제된다.

2. Circular References

Circular Reference
(Ex. 자기 자신을 참조하는 객체. 
	 l = []
	 l.append(l)
)

Reference Counter가 0이 될 수 없는 조건이므로 Reference Counting으로는 Garbage Collection을 마칠 수 없다. 이를 해결하기 위한 방법으로 Circular Reference를 감지하는 별도의 알고리즘을 사용한다. (Circular Reference는 Container Object만 확인하면 된다.)

https://winterj.me/python-gc/
https://stackify.com/python-garbage-collection/

3. List & Genarator

Generator에 대해 설명할 때 꼭 필요한 두가지
- yield와 return의 차이
- Generator는 yield를 통해 값을 return한 이후에도 memory 상에 남아 Generator에 다시 접근하였을 때 해당 위치부터 다시 진행 할 수 있도록 한다.

4. List & Tuple

List: Mutable
Tuple: Immutable



- Python과 C 차이
- RDBMS / NoSQL 차이 (언제 NoSQL이 잇점이 있나요?)
- Local Miminum / Global Minimum
- SVM / CNN을 왜 NLP에 적용했나요?