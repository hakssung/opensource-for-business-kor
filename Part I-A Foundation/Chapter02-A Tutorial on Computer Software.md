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

### JavaScript

### PERL, Python, PHP, and Other Scripting Languages

### Layers of Computing

### What Is an Operating System?

### What Is an Application?

### Dynamic Linking and Static Linking

### Monoliths and Loadable Kernel Modules

### Header Files

### Containers


