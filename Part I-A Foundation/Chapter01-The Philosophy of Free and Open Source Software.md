
# Part I: A Foundation

## Chapter 1 The Philosophy of Free and Open Source Software

-   대부분의  사람들은 Linux kernel과 Apache web server와  같은 software를 “open source” software라고  한다.
    -   하지만, open source 운동의  선구자들은 open source라는  용어를  사용하지  않으며, 그들이  시작한  것은 “free software” 운동이었다.
    -   이러한  용어의  차이는  이  운동에  참여한  사람들의  철학에서  중요한  차이점을  나타낸다.

-   free software 운동의  창시자인 Richard Stallman은  그의  철학을  기술적이고  경제적인 freedom을  장려하는  것으로  설명한다.

-   그는 “software 저작권  체계를  감안할때, software 개발은  그 software의  사용을  통제하는 owner의  존재와  연계가  있다. 이  연계가  존재하는한, 우리는 proprietary software를  선택하거나  선택하지  않아야  하는  상황에  직면하는  경우가  종종  있다. 그러나  이러한  연계는  내재적이거나  필연적인  것이  아니다. 이것은  특정  사회적 / 법적  정책  결정(소유주를  결정하는  것)의  결과이고, 이는  우리가  의문을  제기하는  것이다. “라고  말했다.

-   Copyleft는  저작권법(Stallman이  도덕적으로  반대하는)의  힘을  이용해  다른  사람들이  저작권으로  인한  이익을  포기하도록  하는 system이다.
    -   free software license는  저작권이  있는  저작물의  공유  및  수정  허락을  요구하는  조건으로  모든  사람에게  광범위한  저작권  사용  허가를  부여한다.
    -   이는 free software뿐만아니라 permissive term하에  허가된 software를  포함하는  광범위한 open source 개념과는  상당히  다르다.

- open source 운동 초기에, free software 철학의 반기업적인 구호는 open source의 도입을 방해하였고, 이에 몇몇 평화주의자들이 free software 지지자와 기업의 이익을 조화시키기 위해 모였다. 
	- 이로 인해 OSI (Open Source Initiative)가 탄생하였다. 

- open source에 처음 접근하는 대부분의 사람들은 copyleft가 사람들에게 software의 무료 기부를 요구한다고 생각한다. 
	- 이는 free software 운동의 구호는 반기업적이고 반자본주의 경향이 있다는 점을 감안하면 이해할만하다.  
	-  그러나, 이 선입견이 정확한 것은 아니다. 
	- 현실에서는 (Linux와 Android Platform을 사용하는) 주요 소비자 전자제품 제조업체는 말할것도 없고, Red Hat, MontaVista Software와 같은 성공적인 회사들이 존재한다. 

- 사실, "free software"에서 free라는 단어는 무료가 아니라 자유를 말한다. 
	- free software는 금전적인 목적으로 software 사본을 판매하는 것을 금지하지 않는다. 
	- 이러한 noncommercial 제한은 open source licensing과 대조적이다. 
	- 그럼에도 불구하고, free software에만 licensing 사업을 기반으로 하는 것은 비현실적이다. 
- 사업적인 관점에서 볼때, free software는 모두가 사용하는 infrastructure software에 훌륭한 model이며, specialized application에는 좋지 않다. 
	- 가장 인기있는 open source software가 전자상거래를 위한 LAMP stack이라는 것은 우연이 아니다.
		- 이를 이용하는 사람들은 Web을 통해 물건을 팔아 돈을 버는 것이지, Web에 접근하는 것으로 돈을 버는 것이 아니다. 
- 지적 재산의 주장이 없는 free infrastructure의 존재는 번영을 촉진시키는 반면, 지적 재산이 완전히 없는 것은 번영을 실질적으로 방해한다. 
	- 공적 및 사적 재화의 올바른 균형을 찾는 것이 혁신을 일으킨다. 
	- 기술 사업이 지난 20년간 free software를 도입해왔기때문에 이런 일이 일어났다. 

- Richard Stallman은 GNU project와 free software 운동의 창시자이다. 
	- Stallman은 GPL의 작가이다. 
	- Stallman은 programmer들은 보상이나 이익에 의해서가 아니라, 그들의 평판을 높이고, community에 선행을 하는 것에 의해 동기 부여를 받아야 한다고 믿고 있다. 

- 만약 한 사람이 Stallman의 free software 이론과 반대되는 것을 구현한다면, 그것은 아마도 Linus Tovalds일 것이다. 
	- Linus Torvalds는 1996년 헬싱키 대학의 학생이었을때 original Linux kernel을 작성했고, 이후로 Linux kernel 기술 혁신에 참여했다. 
	- 현재 Torvalds는 Linux Foundation (www.kernel.org)에 의해 공개되고 있는 kernel의 방향에 대한 가이드를 제공하고 있다. 
	- Torvalds는 free software 이데올로기의 지지자가 아니며 자유롭게 이용할 수 있는 software에 대한 지지자이다. 
	- 그는 때때로 Stallman 캠프의 사람들과 사이가 틀어졌다. 그는 정치적 지지자라기 보다는 기술자이다. 

- 사실, Stallman과 Torvalds는 공생하는 사이이다. 
	- licensing model은 이 model을 구동하기 위한 좋은 software가 없이는 성공할 수 없다. 
	- software도 이를 가능하게하는 licensing model이 없이는 성공할 수 없다. 

### The Open Source Development Model
- 사람들이 open source에 관하 이야기할 때, 두가지 다른 의미가 있다.
	- licensing model과 development model이다. 
	- 이 책의 대부분은 open source software license를 포함하는 licensing model에 대해 설명한다. 

- open source development model은 실제로 open souce software의 가치를 창출하는 것이다. 
	- license 는 그렇지 않다. 단지, model을 가능하게 하는 수단일 뿐이다. 

- 이 model을 이해하는 가장 좋은 방법은 Eric Raymond가 open source development에 대해 독창적으로 작성한 글인 "성당과 시장 (The Cathedral and the Bazzar"의 비유를 통하는 것이다. 
	- proprietary software를 개발하는 것은 중세 성당을 짓는 것과 같다. 
		- 강력한 조직 (교회)이 project를 고안하고, 기금을 모으고, mater builder를 임명한다. master builder는 project를 수행할 기능공과 builder를 고용한다. 
		- project의 진행은 sponser의 자금과 master builder가 project를 감독할 수 있는 능력에 의해 제한된다. 
	- open source development는 시장과 같다. 
		- 누구든지 상품을 판매할 수 있다. 시장은 무엇이 사고 팔리는가를 결정한다. 
		- 개발은 협업적이고, 자원은 부족하지 않으며, 어떤 개인이나 조직도 project 전체를 통제하지 못한다. 
		- 시장이 요구하면 project의 방향이 바뀌거나 project가 여러 project로 나뉠 수 있다. 

- 많은 사람들은 free software 운동의 구호가 전체주의로 들리기 시작했을때 에 혼란을 겪는다. : 모든 software는 GPL하에 있어야 하고, forking은 일어나지 말아야 한다 등. 
	- 이는 개발의 본질은 시장의 생각에 따라 바뀔수 있다는 자유 시장에 대한 Raymond의 비전과는 상당히 다르다. 
- 이 두가지 비전을 조화시키는 것이 어렵게 보인다면, 가장 자유로운 시장에서도 표준화하려는 자연스러운 경향이 있음을 명심해라. 
	- 이는 단지 (licensing term이나 software code가 무엇인지와는 상관없이 ) 많은 forking은 유용하다는 것을 의미한다. 
	- 시장에서의 free actor조차도 자발적으로 그들의 practice를 표준화할 것이다. 그렇지 않으면 비호환성을 조정하는 것에 너무 많은 노력이 낭비될 것이다. 
	- 그러므로, open source는 freedom이 가장 중요한 세계이지만, 어떤 practice는 도태될 것이다 (fat에 의해서가 아니라 합의에 의해서). 

### The Free Software Defnition and the Open Source Defnition
- free software 순정주의자 (Stallman과 같은)와 기술적 실용주의자 (Torvalds와 같은) 사이의 철학적 차이점을 고려할때, free software와 open source software가 경쟁적인 방식으로 그들의 지지자에 의해 정의되는 것은 놀랄 일이 아니다. 

#### The Free Software Defnition: The Four Essential Freedoms
  0. 원하는 목적에 따라 program을 실행할 수 있는 freedom
  1.  program 동작 방식을 연구하고 원하는대로 computing을 수행할 수 있도록 변경할 수 있는 freedom
  2. 복사본을 재배포하여 이웃을 도울 수 있는 freedom
  3. 수정본을 다른 사람에게 배포할 수 있는 freedom. 이렇게 함으로써, 전체 community에게 수정 사항에 대한 혜택을 줄 수 있다. 

#### The Open Source Defnition, promulgated by OSI, covers both copyleft and  permissive software licenses:
  1. free 재배포
  2. source code [반드시 포함되어야한다.]
  3. 파생 저작물 [반드시 허용되어야 한다.]
  4. 저자의 souce code의 무결성
  5. 개인이나 단체에 대한 차별 금지
  6. 노력 분야에 대한 차별 금지
  7. license 배포
  8. license가 하나의 제품에 한정되어서는 안된다.
  9. license가 다른 software를 제한해서는 안된다. 
  10. license는  기술 중립적이어야 한다. 
- OSI는 website에 명시적으로 GPL이 이 정의를 준수한다고 명시하고 있다. 
	- GPL은 GPL이 적용되는 저작물에 추가된 software를 통제하려고 하기 때문에 이 정의 항목이 GPL에 맞지 않는다는 비판이 예상된다. 
	- 이 두 정의가 분명히 다르지만, 이 구별에 대한 실질적인 결과는 거의 없다. 
	- OSI는 더이상 이 정의에 맞는 모든 license를 승인하지는 않으며, FSF는 free software 정의에 적합한 것으로 간주되는 license만을 release한다. 
	- OSI는  한때 기업과 free software를 조화시키기 위한 핵심적인 노력을 했다. 오늘날에는 거의 관련성이 없다. 
- OSI는 free software를 둘러싼 논쟁이 free software의 채택을 몰아내겠다고 위협했을때 시작되었다. 
	- OSI의 목적은 "open source community에서 다양한 지지자들 사이에 다리를 놓는 것"이다.
- OSI는 software license를 open source license로 인증하는 조직이다. 
	- OSI는 또한 Open Source 상표에 대한 관리를 한다. (비록, 이 용어는 거의 일반적이고 상표로써 상표권으로 집행 할 수 없는 것이지만)
	- 모든 승인된 open source license는 OSI website에 게시된다.
	- 80개 정도가 있고, 매년 몇몇 새로운 license가 승인된다. 
	- 1990년대, OSI는 open source definition에 부합하는 거의 모든 license agreement를 승인했다.
	- 그러나, 오늘날 OSI는 "license 확산"과 "무의미한 license"를 막기 위해 거의 새로운 license를 승인하지 않는다. : major license의 variation (단지 한 두 project에서 사용) 

### It’s Not a Virus
- open source licensing에 대한 토론에서 바이러스(viral)라는 단어를 제거하는 것은 오래 전에 이루어졌어야 한다. 
	- 왜냐하면, 이 단어는 open source licencing 원칙에 대해 이해하는 것을 왜곡하고 제한하기 때문이다. 
	- 이에 대하여 책임이 있는 것은 대부분 변호사들이다. 
		- 변호사들이 copyleft license에 대해 설명할때, 종종 바이러스(viral)라는 단어를 사용한다. 
		- 불행하게도 그 단어는 부정확하다. 

- 올바른 용어에 대한 다양한 선택이 있다. 
	- free software
	- copyleft
	- 상호주의 (reciprocal)
	- 유전 (hereditary)

- 최선의 선택은 copyleft이다. 
	- copyleft license는, software binary 배포의 조건으로, 배포자가 동일한 license term에 따라 corresponding source code의 공개를 요구하는 license이다. 
	- copyleft license는 software의 저작권에 달라붙는다. ; 얼마나 많은 downstream 배포가 일어날지라도 license term은 동일하게 유지된다. 

- Copyleft license는 GPL, LGPL, MPL, EPL 등을 포함한다.
	- 그러나, 이 개념을 설명하기 위해 바이러스(viral)라는 단어를 사용하는 것은 오해의 소지가 있고, 불필요한 두려움을 유발한다. 
	- copyleft license에 관한 가중 큰 오해는 바로 이 단어의 사용때문이다. : 바이러스 (viral)

- 하나의 executable program내에서 GPL code와 다른 code를 결합하는 것을 흔히 "derivative work"을 생성한다고 한다. 
	- 이는 GPL이 특정 program내에 GPL code가 있는 경우, 해당 program내 전체 code를 GPL로 공개해야한다고 말하기 때문이다. 그렇지 않으면 GPL 위반이다.
	- 기업들은 GPL과 proprietary code가 하나의 program으로 결합하면 GPL licensing term이 proprietary code를 "감염"시킬 것이고, proprietary code는 GPL에 따라 자동으로 relicense될 것이라고 우려하고 있다. 
	- 그러나 이것은 copyleft가 동작하는 방식이 아니다. 

- 사실, 회사가 GPL을 위반하는 방식으로 GPL과 proprietary code를 결합하는 경우, 그 결과는 GPL을 위반하는 것이다. 그 이상도 이하도 아니다. 
	- 법적으로 GPL code의 author는 GPL 위반에 대해 remedy를 가질 수 있다. 
	- 그리고, 그 결과 license가 종료되었다면, author는 GPL software의 unlicesed use에 대한 remedy를 가질 수 있다. 
	- 이 둘 모두, 본질적으로, 저작권 침해 claim이다. 
	- 저작권 침해 claim에 대한 법적 remedy는 damage (돈)와 injuction (GPL code 사용 중지)이다. 
	- 실제로, proprietary code를 감염시키고, licensing term을 변경하는 GPL의 법적 mechanism은 없다. 
- 반대로, GPL을 위반하게 proprietary와 GPL code를 하나의 single program으로 결합하는 것은 license incompatability이다. (즉, 두 term이 충돌하고 동시에 만족될 수 없는 상황)

### The Philosophy of “Open”
- 지난 수십년 동안 open source software의 성공을 기반으로 openness의 광범위한 개념이 개발되었다. 
	- "open"이라는 개념이 기술 산업에서 business practice를 어떻게 바꿔놓았는지 이해하는 것이 중요하다. 

- open을 한가지로 정의할 수는 없으며, 많은 것들이 open이라고 주장한다. 
	- 그러나, 전반적으로 open paradigm은 외부의 참여를 추구한다. 
	- open model은 또한 투명성이 특징이며, 장점에 기반한 참여에 중점을 둔다. 

- 10년전인 2007년에 출시된 Apple iOS platform의 혁신적인 특성을 고려해보자. 
	- 이 platform은 "open"이라고 불렸지만, open source software는 아니다.
	- 누구나 무료 개발 tool을 이용하여 이 platform에서 개발할 수 있다는 의미에서 "open"이다. 
	- open source 지지자들은 이것이 진정한 open technology 환경이 아니라는 것을 지적할 것이다. 
	- 개발자는 developer agreement에 서명해야 하고, App Store를 통해서만 판매하고, 많은 platform 규칙을 따라야만했다. 
	- 그러나, 당시, Apple의 움직임은 극적이고, 혁명적이고, 거의 사람들이 예상하지 못한 방식의 "open"이었다. 

- 2008년, Android platform이 소개되었다.
	- 이 platform은 openness의 개념을 확장시켰다.
	- open soruce software 기반이었고, 많은 제조사에게 제공되었으며, 여러 app store가 경쟁할 수 있게 하였다. 

- 한편, Linux computer OS는 꽤 오랫동안 성장해왔다. 
	- 수년 동안, Linux는 server 시장과 embedded system을 능가하는 시장 진입을 하지 못했다. desktop에서 특히 눈에 띄지 않았다. 
	- 진정한 open platform에 가장 가까왔지만, 이러한 very openness는 business model로서는 매력적이지 않은 토대였다는 것을 의미했다. 

- Red Hat은 1999년에 공개되었다. 
	- 그 후, Linux 배포판 시장은 쇠퇴하였다.
	- service와 support를 주기반으로 하는 business model에 내재된 어려움은 시장에 많은 참여자들이 설 자리가 많지 않다는 것을 의미한다. 
	- 하지만, Red Hat은 계속해서 번창하는 사업이며, e-commerce 경제는 그 사업에 거의 전적으로 의존한다.

- 2010년, open infrastructure initiative를 지원하기 위해 한데 묶는 것이 산업계에 매우 인기가 있었다. 
	- IAAS (Infrastructure As A Service)를 제공하는 open source project인 OpenStack은 2010년에 시작되어 엄청난 인기를 얻었다.
	- OpenStack은 Dell, EMC, Oracle, HP, AT&T, Red Hat, IBM, Canonical, Yahoo, Rackspace, Intel, Cisco와 같은 거대 기술 기업들이 지원한다. 
	- 이러한 기술 기업들이 open source project에 그렇게 빨리, 기꺼이 협력한다는 생각은 10년 전만해도 상상도 할 수 없었다. 

- open과 closed간의 이데올로기 전쟁이 있었던한, open이 이긴것이다. 
	- 그러나, 그 이데올로기가 사실이라면, "open"이라는 idea는 항상 변화하고 확장한다.
	- 의심할 여지 없이, business의 미래를 형성하는데 도움이 되는 놀라움을 계속 제공할 것이다. 
