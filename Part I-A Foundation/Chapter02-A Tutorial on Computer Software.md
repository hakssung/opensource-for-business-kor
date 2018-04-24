## Chapter 2 A Tutorial on Computer Software
이 chapter는 computer engineer가 아니면서 open source licensing을 이해하는데 유용한 몇가지 개념을 배우려는 사람들을 위한 tutorial이다. 

### What Is the “Source” of Open Source?
- 오늘날 대부분의 computer 사용자는 iOS 또는 Android system의 modile device 또는 Windows 운영체제가 설치된 desktop / laptop computer를 사용한다. 
	- device 또는 computer에서 app 또는 application과 같은 program을 실행할때 program을 구성하는 전자 file을 executable file이라고 한다. 
	- computer내의 다른 file과 마찬가지로 file이지만, 이는 computer에서 실행할 수 있는 format이다. 
	- Windows desktop system에서 이러한 file은 .exe 확장자를 가진다. 
	
- computer는 중앙 processor 또는 graphic processor가 초당 수십억회 수생할 수 있는 매우 작은 step으로 작업을 나누어서 복잡한 작업을 수행한다. 
	- 이러한 작업에는 memory의 한 곳에서 다른 곳으로 1~4 byte를 이동하거나, 간단한 산술 수행 및 실행할 다음 단계의 선택이 포함된다.
	- 각 작업은 매우 간단하지만, 매우 많은 작업을 수행함으로써 computer는 사람이 인식할 수 있는 작업 (예: message를 display)을 수행할 수 있다.
	- computer가 이해할 수 있는 간단한 instruction은 인간이 쉽게 이해하고 구성하기에는 너무 작기 때문에, computer 과학자들은 사람이 보다 쉽게 computer program을 작성하기 위해 언어를 개발했다.
	- 이것이 우리가 programming language라고 부르는 것이다. 
	- programming language의 각 문장은 많은 computer instruction으로 변환된다. 

- 인간은 source code를 작성하여 program을 표현한다. 
	- computer는 source code를 compile 및 interprete라는 process를 통해 실행할 수 있는 것으로 변환한다. 
	- 예를 들어, 대부분의 C 언어 program은 CPU가 직접 실행할 수 있는 binary code로 compile된다. 
	- Java 및 Microsoft의 C#으로 작성된 program은 byte code라는 중간 binary representation으로 변환되며, 이후에는 virtual machine이라는 computer program에 의해 executed binary로 변환된다. 

- C 및 Java와 같은 많은 programming lanague에는 source code와 executable form이 있다. 
	- source code form은 실행 가능하지 않다. 즉, computer가 실행할 수 없다. 
	- executable form은 사람이 읽을 수 없다. 이는 1과 0의 묶음이다. 때로는 object form이라고도 한다. 

- source code는 programmer가 software를 작성한느데 사용하는 언어이다. 
	- source code는 다소 자연스러운 언어처럼 보인다. 
	- 다음은 그 예이다. 

```sh
#include <stdio.h>  
int main(void)  
{  
  int x;  
  x=1;  
  if (x==1) {printf ("I am the One.\n")};  
  return 0;  
}
```

- 이 언어가 nonprogrammer에게는 이상하게 보일 수 있지만, 몇몇 부분은 익숙하다. 
	- computer 언어는 "print"와 같은 동사, "x"와 같은 명사, "int"와 같은 형용사를 갖는다. 
- programmer가 code를 작성하면, file을 text로 저장한다. 
	- 그런 다음, compiler라는 program을 실행하여 source code를 object code로 변환한다. 
	- 한번 code가 object form으로 되면, 다시 source code로 돌아가지 않고서는, 수정할 수 없다. 
	- 이론적으로 code를 "decompiled"할 수 있지만, process가 안정적이지 않으며, decompiled code에는 주석이 포함되지 않는다. 
	- 사실, decompilation은 복잡하다. Java 같은 일부 언어는 decompile이 안정적인 반면, C와 같은 다른 언어는 그렇지 않다. 
	- decompiler는 매년 더욱 정확하고 정교해진다. 

- Computer가 느릴때는 program을 source code에서 executable format으로 변환하는 시간이 측정가능했으며, 사람이 program을 사용하는 것을 느리게 하거나 방해할 수 있었다. 
	- 지난 30년 동안, CPU는 훨씬 빨라졌다.
	- 처리 속도가 빨라짐에 따라 점점 더 많은 작업이 main program에서 library로 옮겨졌다. 
	- 예를 들어, Apple II 시대에, code를 작성하려는 개발자는 image를 screen에 옮겨야 했다. 
	- 오늘날에는 한줄의 source code로 browser에서 image를 animation으로 만드는 방법이 많이 있다. 

- 이러한 발전으로 code는 점점 source form으로 배포되고 있다.
	- 예를 들어, browser가 HTML과 JavaScript를 load하면, browser는 HTML과 JavaScript code를 webpage를 표시하고, 입력을 확인하며, page 내용을 애니메이션화하는 executable code로 변환한다.
	- 일반적인 web page에는 30년된 computer의 사용가능한 전체 memory에 들어갈 수 있는 것 보다 많은 code가 들어가있다. 
	
- internet을 통해 code를 전송하는 시간을 줄이기 위해 programmer는 code를 압축하여 code size를 줄인다. 
	- 이 압축된 code는 기술적으로는 intermediate form이지만, original source code와는 다르게 보인다. 
	- 따라서, browser내에서 실행되는 JavaScript는 종종 모든 공백을 삭제하도록 변경된다. 
	- Programming에서 blank와 tab같은 white space는 일반적으로 기능을 위해서가 아니고, 가독성을 위해서만 사용되므로, 이를 삭제하면 읽기는 어렵지만 기능적으로는 동일한 source code가 생성된다. 따라서 위의 예는 다음과 같이 다시 작성될 수 있다. 
```sh
#include <stdio.h>  
int main(void){int x;x=1;if(x==1){printf("I  
am the One.\n")};return 0;}
```
- 이것은 위의 예제와 동일하지만, 대부분의 공백이 제거되었다. 
	- JavaSCript와 같은 scripting 언어의 경우, 공백을 제거하면 source code의 문자수가 줄어들어 code가 실행되는 사용자 browser로의 code download 속도를 높일 수 있다.
	- mobile device와 같이 작은 pipe를 통해 전달되어야 하는 복잡한 web application을 작성하려는 programmer에게는 속도의 모든 bit가 도움이 된다. 


### Building, Linking, and Packaging
- 실제 대부분의 code는 위의 예제보다 훨씬 복잡하다. 
	- programming의 실제 세계에서 우리의 작은 예제는 거의 쓸모 없다. 
	- 그러나, code은 작은 bit라도 제대로 결합되면 유용할 수 있다. 
	- 예를 들어, 숫자를 더하거나 제곱근을 찾는 code snippet은 필수적일 수 있다.
	- 실제 세계에서의 program은 이 code bit를 반복해서 사용해야 할 수 있고, programmer는 한번만 작성해놓고 쓰기를 원한다. 
	- 이 점이 building과 packaging이 필요한 부분이다. 

- 물론, 오늘날 제곱근을 찾기 위한 routine을 작성하기를 열망하는 programmer는 거의 없다. 왜냐하면 이미 다른 사람들이 그러한 routine을 작성했기 때문이다. 
	- 따라서, 현실세계에서는 programmer들이 기존의 routine을 재사용할 수 있도록 programm을 작성하는 기술이 있다. 
	- 기존의 제곱근 routine은 이미 테스트가 되었으므로 새롭게 작성한 routine보다 더 안정적이다. 
	- 이러한 기존 code routine을 library라고 부른다. 
	- library는 계약서에서 '정의'와 유사하다. 
	- 변호사가 모든 reference point마다 전체 정의를 다시 만들기보다는 정의된 용어를 참조하는 것 처럼, programmer는 잘 정의된, 공통 작업을 수행하기 위해 library routine을 사용한다. 

- programmer가 program을 build할때, 먼저 code를 source code form으로 작성하고, 이를 object code form으로 compile한다. 
	- 그런 다음, linker라는 program을 사용하여 object를 library routine과 link한다. 
	- 이렇게 한다면, library를 위한 source code가 필요 없다. 

- 잘 작성된 library는 대개 programmer에게는 black box이다. 
	- 즉, programmer는 box 안의 내용을 알 필요가 없으며, 들어가는 내용과 나오는 내용만 알면 된다. (
	- 이 information은 interface 정의 또는 API (Application Program Interface)라고도 한다. 

- object들이 모두 엮이고 나면, executable program이라고 한다. 
	- executable program은 실행에 필요한 모든 부분을 가지고 있다. 

- programmer가 library routine에서 bug를 찾았거나, 그가 작성한 code에서 작동하지 않는 use case를 발견했다고 가정하자. 
	- 예를 들어, library가 양력에서 날짜를 선택한다고 가정하지만, programmer는 음력에서 날짜를 선택하려고 한다. 
	- library routine은 programmer의 의도대로 동작하지 않으므로, programmer는 이를 개선하기 위해 source code에 access해야 한다. compile된 code를 변경하는 것은 불가능하다. 
	- programmer가 code를 변경하려면, source code로 돌아가고, 변경하고, source code를 recompile하고, program을 relink해야 한다. 

- 이것이 source code에 대한 access가 중요한 이유이다. 
	- source code 없이 bug를 수정할 수 없다. 
	- source code 없이 변경하거나 개선할 수 없다. 
	- object code로 수행할 수 있는 모든 것은 larger program으로 build하는 것이고, executable로 할 수 있는 모든 것은 실행하는 것이다. 
	
### JavaScript

이 언어는 현재 web 개발에 중요하며 여러 이유로 nonprogrammer들 사이에 많은 혼란을 야기하기 때문에 자체 section을 가질 자격이 있다. 
- JavaScript는 Java가 아니다. 
	- Java는 web 배포에서 널리 사용되는 programming language로 compile이 된다. 
	- 반면, JavaScript는 scripting language로 compiled form이 없고, web browser 내에서 program을 실행한다. 
	- e-commerce seller로부터 구두를 주문한다고 가정해보자. 
		- JavaSCript code는 입력을 검사하고, 필수 입력란을 작성하도록 체크한다. 
		- 어떻게 web page와 interact하게 하는지 지시하는 code는 대개 JavaScript일 것이다. 
- JavaScript와 관련하여 중요한 점은 HTML과 마찬가지로 JavaScript가 source code 형태로 사용자의 browser에 전달되고, 사용자의 computer에서 실행된다는 것이다. 
	- 이 특성은 open source licensing에 큰 차이를 만든다. 

### PERL, Python, PHP, and Other Scripting Languages
PERL, Python 및 PHP와 같이 일반적으로 사용되는 다른 유명한 scripting 언어가 있다. 
- scripting 언어는 high-level 언어이다. 즉, 소량의 code가 많은 일을 할 수 있다. 
	- JavaScript와 마찬가지로 script 언어는 source code form으로 실행된다. 
	- 하지만, 주로 사용자의 browser가 아니라 "back end"에서 실행된다. 
- Scripting 언어는 일반적으로 interpreter, virtual machine 또는 language engine에서 실행된다. 
	- script를 실행하려면, user system에 interpreter가 설치되어 있어야 한다. 
	- inerpreter가 script를 처리하는 방법을 알고 있다. 

### Layers of Computing
- 현대 computer processing은 여러 layer에서 발생한다. 
	- 이런 측면에서 computing은 지난 수십년 동안 엄청나게 변화했다. 
- 예전에는 programmer가 single processor에서 실행되는 single program을 작성했다.
	- 당시에는 모든 개별 기능이 computer processor내 부족한 시간과 공간을 차지했다. 
	- 오늘날 processor는 더 크고 빠르며 동시에 많은 program을 처리할 수 있고, 그래서, computing은 더욱 module화 되었다. 
	- desktop computer와 같은 오늘날의 computer system은 일반적으로 그림 2.1과 같다. 

![enter image description here](https://github.com/hakssung/opensource-for-business-kor/blob/master/img/fig-2.1.png)
Figure 2.1 Computer system architecture

### What Is an Operating System?

### What Is an Application?

### Dynamic Linking and Static Linking

### Monoliths and Loadable Kernel Modules

### Header Files

### Containers


