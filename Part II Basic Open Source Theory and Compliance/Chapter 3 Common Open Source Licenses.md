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

### Reading GPL Version 2

### “Special Exceptions”

## The Lesser General Public License (LGPL)

### Corporate-Style (or “Weak”) Copyleft Licenses

## Permissive Licenses

### Apache

## Miscellaneous Licenses


### OpenSSL

## Content Licenses

## Problematic Licenses






