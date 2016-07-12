# 3. OS

1. Kernel을 필요에 의해 어느정도 수정했다고 하자. 
이 kernel이 제대로 작동하는지를 알기 위해서 어떤 test를 해야겠나?
1. Sequential program과 multithread program에서 error detection에 대한
 차이점에는 어떤 것이 있나?
1. 어떤 C program으로 작성되어 수행중인 process가 있다고 가정하자. 
C언어에서는 직 접적으로 주소를 변수에게 지정해 줄 수 있다. 
만약 주소 1, 2, 3, 4에 변수를 잡아서 어떤 일을 수행하는 process라고 하자.
이 process를 한 시스템에 동시에 두번 수행 시켰다. 
그랬을 때 한 프로세스가 1,2,3,4 주소에 있는 변수를 바꿨을 때
다른 프로 세스의 변수들에도 영향을 끼치는가?
1. Thread와 process의 차이는 무엇인가?
1. IPC가 무엇인가?
1. Logical address와 physical address의 차이는 무엇인가?
1. Logical address를 physical address로 바꾸어주는 hw가 무엇인가?
1. Interrupt란 무엇인가? 
interrupt를 두 종류로 나눈다면 어떻게 되는가? 
(software interrupt/hardware interrupt) 
두 interrupt의 차이는 무엇인가?
두 interrupt의 handler 를 서로 구분해서 구현해야 하는 것이 좋은가, 아니어도 상관 없는가?
1. C로 숫자로 직접 입력된 주소를 참조하는 프로그램을 짜서 컴파일한 후, 
두 개를 실 행시켰다고 하자. 그러면 이 두 프로세스는 물리적으로 같은 곳을 참조하나? 
만약 아니라면, 어떻게 서로 다른 물리적 공간을 참조할 수 있나?
1. 프로세스는 가상 메모리 주소로 어떻게 실제 메모리 주소를 찾아가죠?
1. Paging이 무엇인가? paging을 할 때 어떻게 실제 메모리 주소에 데이터를 전송하는 가? 
page table에는 어떤 항목이 저장되는가? page table은 어디에 저장되는가? 
page table이 메모리에 저장되면, paging을 할 떄 메모리를 두 번 참조해야 되는데, 
좀 더 빠르게 하는 방법은 없는가? TLB에는 어떤 항목이 저장되는가?
1. Thread와 Process의 차이는? Thread끼리 context switching 하는 과정에 대해
설명하 시오. 같은 프로세스 내부의 thread들끼리 전환되는 것과 다른 프로세스간의 thread 까리
전환되는 것이 어떻게 다른가?
1. Virtual Address와 Virtual memory에 대해 설명하시오.
1. 시스템 콜과 인터럽트의 차이는? 인터럽트가 걸리면 어떤 일이 일어나고, 
인터럽트 처리 후에 어떻게 이전 상태로 돌아가나?
1. Non-preemptive scheduling이란? Critical section이란?
1. OS의 캐시 메모리의 사이즈를 구하기 위한 프로그램을 어떻게 구현하면 되는가?
1. 세마포어의 개념은? 주요 연산 2가지는? 어떻게 구현해야 하는가?
1. Virtual memory에서 page replacement policy에는 어떤 것이 있는가? LRU의 단점은?
1. 운영 체제에서 memory management 기법중 하나로 paging이 많이 사용되고 있습니다. 
Paging 기법의 장단점들로는 무엇이 있으며, hierarchical paging 
혹은 inverted page table은 어떤 환경에서 유리할까요?
1. 요즘 많은 사람들이 각각 자신만의 스마트폰을 사용하고 있습니다. 
이처럼 각 개인 스마트폰을 위하여 process system을 design하려고 합니다. 
스마트폰에서 각 application이 하나의 process로 독립해서 실행하는 것이 나을까요? 
아니면, 하나의 thread로 만들어져서 실행하는 것이 나을까요? 
어느 쪽이 나을지 결정하고, 그 이유 를 설명하세요.
1. 캐쉬 메모리와 메인 메모리의 주소 지정 방식의 차이점이 무엇인가?