# 1. Programming Language / Compiler

- 자바에서 public, protected, private 키워드가 있는데 아무것도 안 쓸 경우 default로 적용되는 범위는?
    - default로 잡은 경우, 같은 package 내의 클래스들이 접근할 수 있다.
- Static typing과 dynamic typing의 차이점은? C++/JAVA은 어떤 typing을 사용하는가?
    - static typing과 dynamic typing은 변수의 타입이 결정되는 시점을 기준으로 나뉘어진다. 
    변수의 타입이 컴파일 시점에서 결정되는 경우 static typing이라고 한다. 변수의 타입이 런타임
    시간에 결정된다면 dynamic typing이라고 한다.
    - C++/Java에서는 static typing을 사용한다.
- C++에서 서로 다른 타입의 오브젝트를 가리키는 포인터를 사용할 수 있나?
    - 사용할 수 있다. 다만, 그 포인터의 타입이 가르키는 오브젝트의 타입에 대해서 superclass
    관계를 가진 클래스여야 한다.  
- 전역 변수 사용의 장단점은?
    - 전역 변수의 장점은 program statements의 모든 scope에서 접근 가능한 변수를 만들 수
    있다는 점이다. 하지만, 전역 변수는 모든 scope에서 수정 가능하기 때문에, 전역 변수의 값이
    프로그램의 의도대로 변화하는지를 파악하는 것이 매우 어렵다. OOP 패러다임의 관점에서는,
    encapsulation을 위반하는 것이기 떄문에 문제가 된다. 다른 변수와 함수들과의 연관성이
    많아지게 되면서 coupling이 심해진다. (coupling이 심해질 수록 가독성과 유지 보수 관점
    에서 손해를 보는 것이다.) 다중 스레드 프로그램에서는 thread-safe를 만족하기 위한 별도의
    노력이 요구된다.
- 프로그램 실행 전 컴파일 시에 타입과 같은 프로그램의 정적 성질을 검사하는 프로 그래밍 언어와 그렇지 않은 프로그래밍 언어를 비교하시오.
    - [스택 오버플로우 참고!](http://stackoverflow.com/questions/125367/dynamic-type-languages-versus-static-type-languages)
    - static typing: C, C++, Java
        - 정적 타입을 지원하는 언어는, 타입과 관련된 개발 오류를 더 적은 비용으로 알아낼 수 있다.
        컴파일러 최적화를 더욱 효율적으로 할 수 있다. 런타임 속도를 더 높일 수 있다. 하지만, 모든
        변수를 선언하고 사용할 때, 그 타입에 대해서 충분히 숙지한 후 사용해야 한다. 따라서, 좀 더
        추상적이면서 고수준 단계에서의 프로그래밍을 하기가 쉽지 않다.
    - dynamic typing: Python
        - 동적 타입을 지원하는 언어는, 변수를 선언하고 사용할 때, 변수의 타입에 전혀 신경 쓰지
        않아도 되기 때문에 좀 더 추상적이면서 고수준 단게에서 프로그래밍을 하는 것이 가능하다.
        하지만, 타입과 관련된 오류를 미리 알아낼 수 없고, 그에 대한 exception 처리 비용이 
        정적 타입 언어에 비해서 많이 크다. 또한, 런타임에 타입을 체크하기 때문에 런타임 속도가
        상대적으로 떨어진다는 단점도 있다.
-  파라미터 패싱 방식에는 eager evaluation 방식과 lazy evaluation 방식이 있다. 두 방식
 의 차이점을 비교 설명하세요. call-by-value와 call-by-name 파라미터 패싱 방식은 각
 각 어느 방식에 속하는지 구분하세요.
    - eagar evaluation을 사용하면, 수식의 값은 변수에 접근할 때 바로 계산이 된다. 계산되지
    않은 수식을 표현하는 중간 자료 구조를 생성하고 관리할 필요가 없다. 따라서, 메모리와 속도에서
    이득을 얻는다. lazy evaluation은 수식을 계산한 값이 필요할 때까지 계산을 늦추는 기법이다.
    이 기법에서는 필요없는 계산을 하지 않으므로 프로그램 전체의 실행을 더 빠르게 할 수 있다.
    - call-by-value은 eager evaluation에 속한다. call-by-name은 lazy evaluation에 속한다.
    call-by-name에서는 한 argument가 사용되지 않으면 evaluate되지 않고, 여러 번 사용되면
    여러 번 evaluate된다. 반면, call-by-value를 하면 일단 argument가 evaluate되고,
    그 뒤로 그 argument를 사용하더라도 evaluate를 다시 하지는 않는다.   
- 언어를 분류하는 데 있어서는 해당 언어를 생성하는 Production 룰의 형태에 가해지는 제약 사항을
 가지고 분류하는 것이 일반적이다. Context Sensitive Language, Context Free Language,
 Regular Language를 생성하는 데 사용되는 Production 룰의 형태에 대해서 그 차이점을 비교 설명하세요.
    - Context Sensitive Language: aAb -> acb (c=/=ε)
    - Context Free Language: A->β1|β2 (nonterminal -> terminal)
    - Regular Language: B->a|aC|ε(right regular) or B->a|Ca|ε(left regular)
- Let L be a regular language. Prove that R(L), strings in L reversed, is also a regular language.
    - R(L)을 받아들이는 finite automata가 있음을 보이면 된다.
        - L을 받아들이는 finite automata에 대해서 모든 링크의 방향을 역방향으로 바꾼다. 
        - 새로운 상태 q~s~ 를 추가한다.
        - 모든 final state에서 ε으로 그 상태 q~s~로 갈 수 있는 링크들을 만든다.
        - 모든 final state들을 normal state로 바꾼다.
        - initial state를 final state로 바꾼다.
        - 상태 q~s~를 initial state로 둔다. 
- LR 파싱이란? Parsing Table의 역할은? 핸들이란? 핸들의 가장 중요한 특징은?
    - LR파싱은 bottom-up방식으로 파싱하는 중 하나이며, right derivation을 기준으로 
    input string을 추적해나가는 것이다. parsing table은 각 state에서 각 input을
    만났을 때, 어떤 state로 가는지 명세해놓은 표이다. 
    - 핸들: string in the right sentential form + production
    - 파스 과정에서 다음으로 올 핸들을 결정하는 것이 LR파싱을 하는 주요 업무이다.
- 파싱에서 bottom-up 방식과 top-down 방식의 차이점은?
    - bottom-up은 detail을 먼저 살피는 것이고, top-down은 큰 그림을 먼저 보는 것이다.
    bottom-up 방식에서는 인풋 스트링의 가장 왼쪽부터 하나하나 살피면서, reduce를
    하는 과정을 거친다. 하지만, top-down 방식은 제일 처음 전체 스트링을 초기 상태로 잡고,
    terminal부분과 non-terminal부분으로 쪼개어 나가는 방식으로 파싱을 한다. 
- Recursive-descent 방식에서 백트래킹이 일어나지 않게 하려면 어떻게 해야 하는가?
    - 잘 모르겠네요 ㅠㅠ. left recursion removal?
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
    - III. E -> E / E -> E / (E) -> E / (E-E) -> E / (E - c)
    -> E / (b - c) -> a / (b - c)
- A relation on the integer 0 through 4 is defined by:
```
R = {(x,y) | x+y ≤ 2x }
```
Which of the properties listed below applies to this relation? Why?  
I. Transitivity  
II. Symmetry  
III. Reflexivity  
    - Answer: I, III
    - I: if a1 + a2 <= 2a1, then, a2 <= a1
    if a2 + a3 <= 2a2, then, a3 <= a2.
    Thus, a3 <= a1 <=> a1 + a3 <= 2a1
    - II: a + b <= 2a, then a >= b, but, not necessarily b + a <= 2b
    - III: a + a <= 2a (trivial)
- Grammar G is defined by: 
```
G = ({x,y,z}, {S,W,X,Y,Z}, P, S)
```
Where the members of P are: 
```
S -> WZ
W -> X | Y
X -> x | xX (원래랑 다르게 바꿈. 그래야 말이 맞을듯)
Y -> y | yY
Z -> z | zZ (원래랑 다르게 바꿈. 그래야 말이 맞을듯)
```
Which of the following regular expressions corresponds to this grammar?  
(A) xx* | yy* | zz*  
(B) (xx* | yy*).zz* *(v)*  
(C) xx*.(yy* | zz*)  
(D) (xx | yy)*.zz*  
(E) x*.yy*.xx*  
- A computer system stores floating-point numbers with a 16-bit mantissa and an 8-bit exponent, each in two’s complement. The smallest and largest positive values which can be stored are    
(A) 1 x 10^-128 and 2^15 x 10^128  
(B) 1 x 10^-256 and 2^15 x 10^255  
(C) 1 x 10^-128 and 2^15 x 10^127  
(D) 1 x 10^-128 and (2^15-1)x 10^127 *(v)*  
(E) 1 x 10^-256 and (2^15-1)x 10^255  
- A grammar G generating language L is defined by:
```
G = ( {x,y}, {S,X,Y}, P, S)
where the elements of P are:
S -> xY 
S -> yX 
X -> xZ 
X -> x 
Y -> y 
Z -> z
```
Is the language L generated by G most accurately said to be:  
A. Chomsky type 0  
B. Chomsky type 1 (context sensitive)  
C. Chomsky type 2 (context free)  
D. Chomsky type 3 (regular)  *(v)*
E. None of the above  
- Consider the following program fragment:
```
read(a, b)
c := 3.0 * a + b ;
if c = 0 then a :=1 else a := 1.0/c +1.0/b ;
```
This program fragment will fault if given certain values for “a” and “b.”
Which is the weakest of the supplied conditions (least restrictive or
smallest) which, if applied to the data, will prevent failure?  
A. b>0  
B. a>0 and b>0  
C. a ≠ -b/3  *(v)*
D. b≠0  
E. 3.0*a≠0andb≠0  
- Grammar G is defined by: 
```
G = ({x,y,z}, {S,W,X,Y,Z}, P, S)
Where the members of P are: 
S -> WZ
W -> X | Y
X -> x | xY
Y -> y | yY
Z -> z | zZ
```
A. Show some examples that are generated by this grammar.  
B. Write the regular expression corresponds to this grammar?
    - A. {xz, yz, xyz, yyz, ...}    
    - B. (x|ε)y*zz*
- A relation over the set s = {x,y,z} is defined by: 
```
{(x,x), (x,y), (y,x), (x,z), (y,z), (y,y), (z,z)}
```
What properties hold for this realtion?  
I. Symmetry x c.e. (x,z) -> (z,x) doesn't exist  
II. Reflexivity o  
III. Antisymmetry x c.e. (x,y), (y,x)  
IV. Irreflexivity x c.e. (x,x), (y,y), (z,z)
V. Transitivity o