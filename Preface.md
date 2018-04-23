# Preface 
  - “killer apps” of open source : “LAMP stack”
    - Linux kernel
    - Apache web server
    - MySQL database
    - PHP scripting
 
## Background: UNIX, Linux, and Software Licensing

사실, open source licensing은 software licensing의 original model이다.

  -  proprietary licensing은  새로운것(newcomer)이다.
  -  이  두 model이  어떻게  함께  발전했는지  이해하려면 computing 역사에  대해  이해해야  한다.

## Once Upon a Time, There Was an Operating System Called UNIX

   - “open source”는 license model이면서 software development model이다. license model과 development model의 risk는  매우  다르기  때문에  이  차이는  중요하다.

  - open source의 killer app은 Linux OS이다. Linux가  개발된  이유와  방법을  배우는  것이
    -   현재 “open source”로  알려진 license model이  어떻게  개발되었고,
    -   open source model이 proprietary model과  어떻게  다른지  이해하는  가장  좋은  방법이다.

-   UNIX는 “free software” model이  등장한  이유이다.
    -  computing 초기에는 UNIX가  지배적인 operating system였다.
    -  UNIX는  AT&T Bell lab에서  개발
-   당시 AT&T는  독점  금지법의  결과로  미국  법무부의  법원  명령(consent decree)에  따라 telephone service 분야  이외의  상업  활동에  종사하는  것을  금지당하였다. 이에  따라 AT&T의  가장  뛰어나고  유능한  엔지니어들이 AT&T Bell Lab이라는  비영리  단체를  통해 computer science 개발에  참여했다.
    -   Ken Thompson과 Dennis Ritchie는 Bell Lab의  과학자였으며, computer programming을  공부한  사람은  이  이름을  알고  있다.
    -   그들은 UNIX의 creator이고, UNIX는  최초의  범용 operating system였다.
    -   UNIX를  개발하면서, C언어를  발명하였다.
    -   C는  유연하고  강력한 programming언어이고, “low-level”언어, 즉, software가 hardware와  상호작용하는  박식을 programmer에게 high level로  제어할  수  있게  한다.
    -   C는  오늘날에도  여전히 common하게  사용되고  있다.(C++, object C 등으로  확장하기도  함)

-   그러나, 법원  명령은 AT&T가 UNIX를  상업용  제품으로  사용하는  것을  금지시켰다.
    -   이에  따라 Bell Lab은 UNIX를  수정과  재배포를  헝횽하는  조항  하에 source code form으로  제공했다.
-   이후  법원  명령이  철회되었고, AT&T는 UNIX에 object code form으로만  재배포를  허용하는 licensing 조건의  제한된 license를  부여하기  시작하였다.
    -   이로  인해 UNIX와  호환되지  않는  많은 “forking” version이  만들어졌다.
    -   예를  들어, IBM의 UNIX에  맞게  작성된 program이 Sun의 UNIX에서는  실행되지  않았다.
    -   free software movement는 UNIX의 forking, 즉 proprietary licensing으로의  전환에  대한  직접적인 reaction이었다.
-   당시 “proprietary license”가  오늘날  처럼  보편적이  아니었다는  점을  이해하는  것이  중요하다.
    -   1980년대에는 software를  구매하면  어떤 computer에서도  실행할  수  있다는  사실이  생소했다.
    -   당시 software는  둘중  하나였다. 구매한 computer에  이미 load되있는  것이거나
    -   system 통합업체에서  개발한 custom software이었다.
-   그리고, 항상 source code form으로  제공되었다.
    -   왜냐하면, micro-computer (혹은 IBM PC) 이전에는 binary-only software distribution model을  지원하거나  필요로하는  표준화가  충분하지  않았다.
    -   회사들은  거의  항상  동일한 vendor로부터 hardware와 software를 bundle로  구입했다.
    -   기술  지원을  담당하는  사람들은 source code를  사용해야했으며, 기술  지원은 machine, OS, environment에만  해당되었다.
-   그렇다면, source code와 binary를  분리한  이유는  무엇이었나?
    -   당시에는  합리적이지  않았다.
    -   그러나 computing 세계는  곧  변화하였다.
    -   몇년  후, microcomputer가  표준이었고, binary software가  표준이  되었다.

## Linux: The “Killer App”

-   Open source software (특히 copyleft software licensing)는 Linux가  아니었다면  법적  호기심  정도로  남아있었을  것이다.
    -   많은 system에서 Linux를 operating system core로  사용한다. Android, Chrome 또는 Mac과  같은 layer들도 하단에는 Linux가 있다.
    -   open source licensing을  이해하려면 Linux가  왜  그렇게  인기  있고  중요한지  이해해야  한다.

-   1980년대  후반, UNIX의  인기는  사라졌다.
    -   1980년대  이전에는  대부분의 computer가  정부, 교육기관, 은행  및  대기업과  같은  대형  기관에서  사용되었다.
    -   1세대 microcomputer (Apple II, TRS-80 / 물론, DOS PC)는  몇년만에  모든  것을  바꿔버렸다.
    -   이 machine들은  더  새롭고  저렴한 processor에서  실행되었다.
    -   UNIX는  이런 platform을  위해  쉽게  적응하지  못했다.

-   UNIX는  표준  규격을  갖고  있었다. : UNIX platform과의  호환성을  정의한  일련의 system routine
    -   이  표준은 POSIX라고  한다.
    -   여러  사람들이 POSIX와  호환되지만 AT&T가  제시한 license 제한  없이  자유롭게  사용할  수  있는 operating system를  찾기  시작했다.
    -   그중  한명은 MINIX라는  학술 project를  작성한  네덜란드의 computer science 교수였다.
-   다른  한명은  헬싱키의 Linus Torvalds라는 10대였다.
    -   Torvalds는 1991년에 Linux의  첫번째  버전을  발표하고  세상을  바꾸었다.
-   한편, MIT 인공지능연구소의 computer 과학자인 Richard Stallman은 GNU project를  시작했다.
    -   GNU는 “GNU’s not UNIX”의  재귀적  약어이다.
    -   GNU project는 UNIX의 free 대안이  될 operating system를  만들려고  했다.
-   full 운영  체제는  많은 element가  필요하며, 핵심은 kernel (computer 실행, memory 관리, program 실행, 주변장치  및  기타 hardware와  통신)이다.
    -   full operating system에는  또한 compiler, debugger, text editor, 관리도구  및 user interface와  같은  개발  도구가  필요하다.
    -   Torvalds는  자신의 software를  자유롭게  사용할  수  있도록  동의하였으며, Torvalds가  작성한 original version에서  개선되어서  채택된 Linux kernel은 GNU operating system의 core가  되었다.
    -   이 operating system을  이제는  보통 Linux라고  부른다.
-   Stallman은  이와  더불어  자신이 추구하던  새로운 free operating system의  사유화를  막을 수 있는 licensing paradigm을  만들어갔다.
    -   그는  이 paradigm을 “free software”라고  불렀고, 이는 GNU General Public License (GPL)라는 license를  통해  구체화되었다.
    -   이 license는 source code를  비밀로  유지할  수  없는  조건으로 software를  재배포할  수  있는  자유로운  권리를  부여했다.
    -   이는 copyleft의  근거였다. 저작권법을  사용하여  저작권이  있는 software 저작물의  공유를  강제하는  것이다.
-   Linux kernel은  free software 정신에  입각하여 처음  개발된  이래로  극적으로  성장, 변경  및  개선되었다.
    -   현재는  수천명의 contributor, 이를  관리하는  한  비영리조직, 수백만명의  채택자, 수십억명의  사용자를  보유하고  있다.
    -   그리고, 여전히  자유롭게  변경, 재배포  및  개선할  수  있다.
-   결과적으로, open source licensing model을  업계  전체를  협력하게  하였고, 결과적으로  수백명의 volunteer와  함께 IT분야의  가장  큰  기업들이  관리하는  강력하고  확장성이  뛰어난 system이  되었다.
- 하지만, 더  중요한  것은 Linux를  사용하기  위해  업계는 Linux의 licensing 조항을  사용해야했다.
    -   이에  따라, Stallman이  개척한 copyleft paradigm은  천천히  견인력을  얻었다.
