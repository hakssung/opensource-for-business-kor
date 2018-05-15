# Chapter 4. License Compatibility

due diligence의 필요성과 license compatibility 문제는 open source licensing을 훨씬 능가한다. 
이 장에서 다룰 내용 중 상당 부분은 software licensing에 관한 것이고, 최종적으로는 due diligence에서 가장 큰 문제를 야기하는 것은 open source license가 아닌 proprietary license라는 결론에 도달 할 것이다. 

## The Awkward Dinner Party

다른 사람과 공존하는 것을 거부하는 식성이 다른 모든 사람을 한 식탁에서 식사 대접하는 것은 어려울 것이다. 

Software license도 자기만 옳고, 다른 모든 사람이 틀렸다고 확신하는 사람과 마찬가지로, 자신의 rule들을 갖고 있다. 이러한 모든 rule이 충돌할때라면 coexistence는 불가능할 수 있다. 

## What Is Due Diligence?
- Due Diligence
	- 이 process는 여러 이름을 갖는다. 
		- audit
		- due diligence
		- housekeeping
		- compliance
		- hygiene
	- 여하튼, 회사가 software에 적용된 open source license를 준수하였는지를 확인하는 process이다. 

- diligence project는 여러 이유로 발생할 수 있다.
	- 합병, 인수, 매각, financing 거래와 같은 기업 거래에서 거의 발생한다. 
	- 고객 요구, regulatory audit, 
	- 또는 license 준수를 위해 발생할 수도 있다. 

- diligence process는 perfection에 관한 것이 아니다. risk management에 관한 것이다. 
	- 최악의 문제를 먼저 해결하고 다음으로 이동한다. 
	- 이를 시간, energy, risk에 대한 두려움이 없어질때까지 다음 단계로 이동한다. 
	- 이는 문제를 분류하고 합리적인 결정을 내리는 과정이다. 

- 전반적인 관점에서 볼때, diligence는 inbound right이 outbound right보다 크거나 같은지 확인하는 process이다. 
	- inbound : 회사에 부여된 license
	- outbound : 회사에서 행사하거나 다른이에게 부여한 권리
	- 회사에 부여된 것보다 더 많은 권리를 부여하거나 사용하면 이는 다른이의 권리를 침해하는 것

![fig-4.1](https://github.com/hakssung/opensource-for-business-kor/blob/master/img/fig-4.1.png)

- Figure 4.1은 software code base로 들어가는 right 정리에 대한 두가지 일반적인 경우를 보여준다. 
	1. target software를 생성하는 party에서 작성한 software
		- 저작자로서, party는 copyright을 행사할 권리가 있다. 
	2. 다른 사람이 작성한 software
		- copyright을 행사하기 위해서는 license가 요구된다. 
		- broad inboud license로 제공이 되었다. 
- 이러한 각 inbound 사례는 outbound right을 clear하기에 충분한다. 
- outbound right이 inbound right과 동등하거나 작다면 licensing은 동작한다. 

### Potential Diligence Issues

- Right 정리 문제는 주로 두가지이다. 
	- license restriction : proprietary license에서만 발생
	- license condition : 주로 open source licensing에서 발생

![fig-4.2](https://github.com/hakssung/opensource-for-business-kor/blob/master/img/fig-4.2.png)

Figure 4.2는 proprietary licensing에서 전형적인 diligence 문제를 보여준다. 
- proprietary software를 위한 inbound license의 범위가 outbound 부여보다 좁다. 
	- 부여하는 right 중 일부는 들어오지 않은 것. 
- 물론, 이런 문제는 open source component에 대해서는 발생하지 않는다.
	- open source definition이 license grant에 restriction을 요구하지 않기 때문. 
	- 그러나, open source license도 Figure 4.3과 같이 diligence problem을 야기할 수 있는 condition을 가할 수 있다. 

![fig-4.3](https://github.com/hakssung/opensource-for-business-kor/blob/master/img/fig-4.3.png)

- Figure 4.3에서, software code base는 inbound license가 GPL이 적용된 component를 포함한다. 
	- GPL은 copyleft license
		- software를 재배포 시, copyleft license condition을 따라야함
- 그러나, 여기서 실수가 있었다. 
	- 이 조건이 recipient에게 흘러나가지 않았다. 
	- 이것은 전형적인 open source diligence 문제이다. 
- 또 다른 문제는 inbound license인 GPL이 outbound license인 Apache와 compatible하지 않다는 것이다. 

- open source에서 condition의 충돌은 많은 diligence 문제를 발생시킨다. 
- 위와 같은 형태로 target code를 만든 회사는 문제를 해결하기 위해 outbound license를 GPL로 변경해야 한다. 
- license가 올바르게 동작하는 software를 만들려면, outbound license와 compatible한 inbound license만 사용해야 한다. 
	- 즉, outbound license와 비교하여, 더 적과 consistent condition의 inbound license만 사용해야 한다. 

![fig-4.4](https://github.com/hakssung/opensource-for-business-kor/blob/master/img/fig-4.4.png)

- Figure 4.4에서는 GPL-3.0과 compatible한 많은 license가 이 project에 적용되었다. 
	- basic rule은 outbound license는 가장 많은 condition을 갖춘 license여야 한다는 것이다. 
	- "The basic rule is that the outbound license must be the one with the most conditions."

- 그러나, AGPL (더 많은 condition을 가짐), EPL, CDDL (모두 다른 copyleft condition을 가짐)과 같은 license가 적용된 component들은 이 software에 포함될 수 없다. 
	- 이러한 copyleft license들은 모두 awkward dinner party에 초대된 guest들과 같다. 
		- 그들의 diet는 상호 배타적이다. (mutually exclusive)
	- 그 이유는 모두 software에 additional licensing restriction 두는 것을 허용하지 않기 때문이다. 
	- 또한, 각각이 slightly different term을 포함하고 있기 때문에, 각각 다른 additional restriction을 구성한다. 
- 예: GPL-2.0 section 6
> Each time you redistribute the Program (or any work based on the Program), the recipient automatically receives a license from the original licensor to copy, distribute or modify the Pro- gram subject to these terms and conditions. You may not im- pose any further restrictions on the recipients’ exercise of the rights granted herein.

- 일부 copyleft licenses는 compatible하다. 
	- 예를들어, LGPL code는 GPL의 해당 version으로 재배포될 수 있다. 
	- 왜냐하면, LGPL은 단지 GPL + additional permission (non-GPL software와의 integration을 허용)인 형태이기 때문이다. 

- 위의 논의는 vertical compatibility와 관련이 있다. 
	- inbound license를 고려할때, 이 software는 다른 outbound license가 적용된 전체 code base로 재배포될 수 있을까? 

- 그러나, open source license는 sublicensing regime이 아님을 명심하라. 
- inbound license는 변경되지 않는다. 
	- 이는 모든 recipient에게 direct로 전달된다. 
- 그러나, open source에서 모든 copyright에 대한 right가 부여되므로, license간에는 아무런 불일치가 있을 수 없다.
	- 유일한 차이는 license를 행사하는데 부여된 condition이다. 
	- 따라서, inbound license와 outbound license의 condition이 상호 배타적이지 않는한 compatibility 문제는 없다. 

### “Horizontal” Compatibility Issues

- 그러나 수평적 호환성 (horizontal compatibility)이라고 생각되는 미묘한 문제가 있을 수 있으며, 이는 GPL과 LGPL에서만 일어난다. (GPL과 LGPL만 code가 통합될 수 있는 방법에 제한을 두는 license이기 때문.)
- GPL과 LGPL의 shorthand rules:
	- 하나의 program내 어떤 code가 GPL인 경우, GPL로 모두 제공되어야 한다. 
	- LGPL code는 dynamically linked library로만 다른 code와 하나의 program으로 통합될 수 있다. 

![fig-4.5](https://github.com/hakssung/opensource-for-business-kor/blob/master/img/fig-4.5.png)

Figure 4-5는 horizontal incompatibility로 발생할 수 있는 문제를 보여준다. 
- copyleft license하의 code는 다른 term으로 재배포될 수 없다. 
	- 따라서, 어떤 license로 작동할 수 없다. 
- 이는 어떤 하나의 음식도 모두를 만족시키지 못하는 저녁 식탁과 같다. 
	- GPL은 다른 사람과 같은 식사를 먹지 않을 뿐만 아니라 같은 테이블에 다른 음식이 존재하는것을 허락하지 않는다. 

![fig-4.6](https://github.com/hakssung/opensource-for-business-kor/blob/master/img/fig-4.6.png)

- 대조적으로, weak copyleft license하에 제공된 software는 같은 program내에 공존할 수 있다. 
	- 물론 permissive license도 다른 code에 대해 restriction을 두지 않는다. 
- 따라서, Figure-4.6의 상황은 동작한다.
	- 모든 license들이 copyleft이지만, weak copyleft이다. 
	- recipient에게 동시에 licensing term을 전달하는 licensing이 가능할 수 있다. 
	- 각 component는 자체 license가 적용된다. 
	- code base 전체로는 하나의 license를 갖는 것이 아니다. 
	- 이것은 마치 방문자들이 같은 table에 앉았지만, 음식을 share하지 않고,  각자 자신의 음식을 먹는 저녁 table과 같다. 

### How to Avoid License Bugs

- 개발자는 자신의 software를 자신이 원하는 term으로 license할 수 있다. 
- 그러나 licensing을 특이하게 하면 다른 개발자들은 그 software를 다른 project에서는 재사용할 수 없는 상황이 만들어질 수도 있다. 
	- 예를들어, proprietary나 다른 copyleft component와 동일한 program내에서 포함이 되어야만하는 library를 GPL로 선택하는 것

- 때때로, 이런 option을 선택하는 것은 사용자에게 proprietary license를 사도록 강제하는 방법이다. (dual licensing model)
	- 이 경우, 개발자는 고의로 license bug 및 해결 경로를 만들어낸다. 
	- 그러나, 그러한 선택이 분명한 생각없이 이뤄진다면, licensing이 역효과를 일으키고, 단지 문제만 만들어낼 수 있다. 

## Apache 2 and GPL 2
- 위에서 Apache-2.0과 GPL-2.0은 imcompatible하다는 점에 주목했다. 
	- permissive license는 일반적으로 다른 open source license와 compatible하다. 
	- 그러나, Apache-2.0이 release된 후, FSF는 Apache-2.0이 GPL-2.0과 incompatible하다는 입장을 취했다. 

- Apache Foundation posted:
	- FSF의 GPL에 대한 입장을 ASF가 이해한 바는 다음과 같다. : 
		1. explicit patent license의 granting은 모든 implicit patent license를 무효화시킴
		2. explicit patent license를 무효화하는 것은 자신의 patent의 침해를 주장한 사람이 GPL의 implicit right을 통해 취득할 수 있는 patent right을 잃게 함. patent right의 상실은 사용권(right to use) 상실을 의미함. 
			- GPL-2.0 7조에서는 GPL work내 patent 침해를 주장하는 patent owner가 계속해서 work을 GPL로 배포할 수 있게 허용함 (judgement or injunction이 있을때까지) (즉, Apache-2.0에서 patent 침해를 주장하는 patent owner는 더이상 work을 배포할 권리가 없는 것은 GPL보다 restriction을 더 가하는 것임)
			- GPL-2.0 6조에서는 "You man not impose any further restrictions on the recipients' execise of the rights granted herein"이라고 했는데, "rights granted herein"은 copyright임 (GPL-2.0은 명시적으로 copyright만 허여). patent에는 해당하지 않음. 따라서, patent claim으로 다른사람이 redistribute할 권리에 restriction을 가한다하더라도 이는 6조의 "rights granted herein" (copyright)에 해당하지 않기 때문에 (판결이 내려지기 건까지) patent claim을 제기한 사람이 계속해서 work을 distribute할 수 있음. (-> Apache-2.0의 특허보복조항으로 patent claim을 제기한 사람은 work을 distribute할 수 없음. 즉, GPL보다 restriction을 더 가하는 것임)


## License Proliferation

