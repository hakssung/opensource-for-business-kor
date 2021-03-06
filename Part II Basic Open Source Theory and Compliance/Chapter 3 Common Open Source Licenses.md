
# Chapter 3 Common Open Source Licenses

이해해야할 Licnese들:
- GPL
- LGPL
- Mozilla / Eclipse
- BSD
- MIT
- Apache 2.0

Open source license의 두 category
- permissive
- copyleft

Permissive
- Do whatever you want with the code.  
- Use at your own risk.  
- Acknowledge me.

Copyleft는 위의 내용에 추가로,
- If you distribute binaries, you must make the source code for those binaries available. 
- The source code must be available under the same copyleft terms under which you got the code. 
- You cannot place additional restrictions on the exercise of the license.

Copyleft는 여러 category로 분류
- Ultra-strong (AGPL)
- Strong (GPL)
- Weaker (LGPL)
- Weak (Eclipse, MPL, CDDL)

## Dissecting the Open Source License
Open source license는 conditionaly copyright license이다. 
기술적으로, license는 licensee에 대해 어떤 의무도 포함하지 않고, license를 행사할 조건만 포함한다. 

### Patent License Grants
Open source license는 주로 두종류의 patent provision을 포함. 

#### 1. license

- patent license grant 조항을 갖는 open source license
	- Apache-2.0
	- EPL
	- MPL
	- GPL-3.0

- contributor가 code에 대해 patent를 보유한 경우, 그 contributor는 모든 code rcipient에게 open souce license를 행사할 수 있는 patent license를 부여한다. 

#### 2. defensive termination provision
- express patent license를 포함하는 거의 모든 open source license는 또한 defensive termination provision을 갖고 있다. 
- licensee가 patent를 주장하면, licensee는 open source license하의 right을 잃을 수 있다. 
- open source license에서 licensee는 어떤 patent right도 부여하지 않는 점은 주목할만하다. 
	- open source에는 grantback이나 cross-license가 없다. 
	- 왜냐하면, open source license는 contract이 아니기 때문.
		- acceptance mechanism이 없고
		- licensee에 대한 obligation이 없음
	- condition만 있고, obligation은 없다. 

## Direct Licensing
- Open source license는 direct licensing model이다. 
	- further sublicense를 부여할 권리가 부여되지 않음
	- 대신, code의 재배포를 허용
- author가 code를 open source license로 release할때, 권리 부여는 자동적으로 모든 recipient에게 되는 것임
![enter image description here](https://github.com/hakssung/opensource-for-business-kor/blob/master/img/fig-3.1.png)

- direct licensing model의 몇가지 추론
	- distributor가 open source license를 위반해서 권리를 잃게되어도 downstream recipient는 잃지 않음
	- 기업 인수 합병 시, Buyer company가 Target company 인수 시, Target company가 사용한 open source code를 받게 될 때, Buyer는 이 code에 대한 license를 Target으로부터 받는 것이 아니라 author로부터 direct로 받는 것이다. 
- open source license는 author로부터 모든 recipient에게 가는 것이기때문에 절대 transfer되는 것이 아니다. 
	- 반로, Proprietary license는 하나의 licensee로부터 다른 licensee에게 transfer되야한다. (M&A시 문제가 될 수 있다.)

## Common Open Source Licenses


## GPL

### GPL Versions
- GPL version 2 only
- GPL version 2 or later
	- "or later"는 권리 부여가 아닌 condition만 부여한다고 보는게 맞다. 
	- 즉, GPL-2.0 or later로 code를 release한 author가 이를 GPL-3.0으로 사용하는 recipient에게 patent grant를 해야하는 것은 아니다. 

### Reading GPL Version 2
- GPL의 main term은 세 파트로 나뉨
	1. 수정하지 않은 source code의 배포 
	2. 수정하지 않은 binary의 배포
	3. 수정한 code의 배포

### “Special Exceptions”
- GCC Runtime Library  Exception : Broad exception that removes all requirements of GPL for use of runtime libraries used via any “Eligible Compilation Process.”
- Classpath Exception : Allows linking to proprietary code. Note that this allows any kind of link, but classpath files are likely to be linked dynamically.

## The Lesser General Public License (LGPL)

- FSF는 LGPL이 GPL보다 사용자의 자유를 보장하지 않기 때문에 LGPL의 사용을 권장하지 않는다. 
	- LGPL은 필요할때만 사용해야한다고 믿는다. 
	- GNU Readline과 같이 고유한 기능을 제공하는 것은 GPL로 하면 community 확산에 도움이 됨
	- 다른 경우라면 오히려 역효과가 생겨서 code가 사용되지 않을 수도 있음

- LGPL은 이해하기 어려운 license중 하나이다. 
	- 회사들은 "dynamically linked library" 형태로 LGPL library를 사용하지만, 원문에는 "dynamic linking"에 대해 명확히 언급되지 않았다. 

- LGPL은 본질적으로 GPL + additional permission이다. 
	- LGPL library를 proprietary application과의 integration을 허용
	- LGPL-3.0에서는 GPL의 appendum으로 작성됨 

### Corporate-Style (or “Weak”) Copyleft Licenses

여기서는 copyleft principle을 적용하면서도 licensing attorney들에게 친숙한 형태로 작성된 license들이다. 
- EPL
- MPL
- CDDL

- MPL
	- 2002년 Netscape web browser에 적용
	- 2012년 MPL-2.0으로 개정

- IBM Public License는 MPL-1.0직후 작성
	- 이후 CPL, EPL로 대체됨
	- EPL은 주로 Eclipse 개발 환경에서 사용

- Sun Industry Standards Source License
	- Sun Microsystems가 공개
	- 2005년 CDDL (Common Development and Distribution License)로 대체

- 이러한 License들은 weak copyleft 성격임
	- proprietary product에 결합된 상태로 code library가 release되는 것을 허용
	- source code가 open source license 로 공개된다면 binary는 proprietary term으로의 relicensing 허용
		- 따라서, 어떤 의미에서는 copyleft는 source coded에만 적용
- 이 license들은 모두 patent license와 defensive termination provision을 명시적으로 포함함

## Permissive Licenses

> Redistribution and use in source and binary forms, with or without modification, are permitted provided that the following conditions are met:

- BSD에 대한 변호사들의 고민
	- “source code and binary forms.” : source code와 binary form을 함께 재배포해야하는 것인가? 
	- formal license grant가 없다

- 하지만, 이들은 심각한 우려 사항은 아님
	- BSD는 분명한 permissive license
	- irrevocable (취소할 수 없는) license grant

- open source license는 문맥 내에서 해석해야함
	- 위와 같은 변호사의 걱정은 큰 그림을 보지 않는것임

### Apache

- Apache-1.0 : "advertising requirement" 땜누에 deprecated됨
> “All advertising materials mentioning features or use of this software must display the following acknowledgment: This product includes software developed by the Apache Group for use in the Apache HTTP server project (http://www.apache.org/).”
	- 이 요구사항은 unworkable (실행불가능)하고, GPL과 inconsistent할 수 있음

- 2000년 Apache-1.1 released. 
	- advertising clause 제거
	- BSD나 MIT license와 매우 유사

- 2004년 Apache-2.0 released
	- 표준화되어 작성patent
	- patent provision 추가
	- Google Android project를 포함하여 많은 open source project를 위한 template license가 됨

## Miscellaneous Licenses


### OpenSSL
- OpenSSL : secure socket layer toolkit의 open source implementation
- OpenSSL license : BSD-style permissive license로 보이지만, 혼란을 야기하는 문장도 포함

> The OpenSSL toolkit stays under a dual license, i.e., both the conditions of the OpenSSL License and the original SSLeay license apply to the toolkit.

- 여기서의 "dual license"는 두 license가 동시에 code에 적용된다는 표현을 위해 사용되었는데, 이는 일반적이지 않은 사용이다. 

- GPL과의 compatibility? 

## Content Licenses
- Software package 내에는 non-software material이 다수 포함된다. 
	- bitmapped image (icon 등)
	- music file
	- picture file (GIF, JPEG 등)
	- text file
- 이들을 content라고도 함
- software가 open source 일때, 이러한 material을 위한 동등한 non-software license가 있는 것이 유용함

-  가장 일반적인 content용 license
	- GNU Free Documentation License
	- Creative Commons license

- GNU Free Documentation License
	- FSF가 GPL과 동일한 목적으로 manual, textboot 등을 위해 만듬
	- 이 license의 많은 조항은 documentation에만 적용된다. 
	- 다른 저작물에는 잘 적용되지 않음
	- 일반적으로 사용되지 않음

- Creative Commons license
- 

## Problematic Licenses

몇가지 license는 거의 항상 compliance 문제를 야기하므로 주목할 가치가 있다. 
- ODbL : copyleft 조건이 있는 "open data" license
- CPAL : OSI가 승인한 "badgeware" license
	- badgeware license는 배포사 없는 경우에도 조건이 적용될 수 있으므로 대부분의 회사에 compliance concern을 야기한다. 
	- 이러한 점에서 AGPL과 유사한 매우 강력한 copyleft license로 간주될 수 있다. 
	
> 15. ADDITIONAL TERM: NETWORK USE.
The term “External Deployment” means the use, distribution, or communication of the Original Code or Modifications in any way such that the Original Code or Modifications may be used by anyone other than You, whether those works are distributed or communicated to those persons or made available as an application intended for use over a network. As an express condition for the grants of license hereunder, You must treat any External Deployment by You of the Original Code or Modifications as a distribution under section 3.1 and make Source Code available under Section 3.2.

> https://lwn.net/Articles/243841/
> "Badgeware" refers to a class of software with licenses requiring that some sort of attribution of its origin be displayed in all copies. An example which has seen much discussion over the last year is SugarCRM, whose license required that every screen carry a 106x23 "Powered by SugarCRM" logo and a copyright notice.
