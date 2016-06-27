# 1. Programming Language / Compiler

- 자바에서 public, protected, private 키워드가 있는데 아무것도 안 쓸 경우 default로 적용되는 범위는?
- Static typing과 dynamic typing의 차이점은? C++/JAVA은 어떤 typing을 사용하는가?
- C++에서 서로 다른 타입의 오브젝트를 가리키는 포인터를 사용할 수 있나?
- 전역 변수 사용의 장단점은?
- 프로그램 실행 전 컴파일 시에 타입과 같은 프로그램의 정적 성질을 검사하는 프로 그래밍 언어와 그렇지 않은 프로그래밍 언어를 비교하시오.
-  파라미터 패싱 방식에는 eager evaluation 방식과 lazy evaluation 방식이 있다. 두 방식
 의 차이점을 비교 설명하세요. call-by-value와 call-by-name 파라미터 패싱 방식은 각
 각 어느 방식에 속하는지 구분하세요.
- 언어를 분류하는 데 있어서는 해당 언어를 생성하는 Production 룰의 형태에 가해지 는 제약 사항을 가지고 분류하는 것이 일반적이다. Context Sensitive Language, Context Free Language, Regular Language를 생성하는 데 사용되는 Production 룰의 형태에 대해서 그 차이점을 비교 설명하세요.
- Let L be a regular language. Prove that R(L), strings in L reversed, is also a regular language.
- LR 파싱이란? Parsing Table의 역할은? 핸들이란? 핸들의 가장 중요한 특징은?
- 파싱에서 bottom-up 방식과 top-down 방식의 차이점은?
- Recursive-descent 방식에서 백트래킹이 일어나지 않게 하려면 어떻게 해야 하는가?
- A grammar G generating language L is defined by:
- Consider the following grammar, with start symbol E:
```
E -> E*E | E/E
| E+E
| E–E
| (E)
| a|b|c|d|e|f.....x|y|z
```
The following strings are legal derivations from this grammar:
```
I. a * b + c
II. (a – b) * c
III. a / (b – c)
```
Which of the above are rightmost sentential forms?  