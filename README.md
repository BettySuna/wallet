# 암호화폐 지갑

H채널구독자를 위한 개인 월렛 보안에 관한 초보자 안내서

![img](https://github.com/BettySuna/wallet/blob/master/img/01.%EB%B2%A0%EC%8A%A4%ED%8A%B8%EC%9B%94%EB%A0%9B.jpg?raw=true)

> 이 안내서는 올바른 코인 지갑 사용과 보안을 위해 작성되었습니다.
> 최대한 전문용어를 배제하고 초보 투자자분들께서도 이해하기 쉽도록 작성하려 했습니다만…
> 공식 문서에 기초해서 작성한다고 했지만 혹 잘못된 내용이 있는 경우 정정 요청 주시기 바랍니다.

※ 게재 허락을 득하지 못한 이미지를 일부 포함하고 있기에 자료는 해밀리 회원만 보시고 공유는 지양 부탁드립니다.

## 지갑의 개념

![img](https://github.com/BettySuna/wallet/blob/master/img/02.%EC%9B%94%EB%A0%9B%EB%A9%94%EC%9D%B8.jpg?raw=true)

- 암호화폐 지갑의 구성
  - **씨드키**(Seed Value): 모든 키의 근본이 되는 값, 지갑 복구 시 사용 (아래 추가 설명)
  - **개인키**(Private Key): 비밀번호와 같은 개념, 코인을 출금하기 위한 서명키
  - **공개키**(Public Key): 계좌번호와 같은 개념, 개인키와 대조하여 블록체인상 소유 검증
  - **코인주소**(Address): 코인별 받는 입금 주소, 전송을 받기 위한 공개 주소 (코인별 상이)

---

![img](https://github.com/BettySuna/wallet/blob/master/img/03.%ED%94%84%EB%9D%BC%EC%9D%B4%EB%B9%97%ED%82%A4%EC%99%80%ED%8D%BC%EB%B8%94%EB%A6%BF%ED%82%A4.jpg?raw=true)

| 지갑의 생성순서                                              |
| ------------------------------------------------------------ |
| 씨드키(Seed Value) <-> 프라이빗키(Private Key) -> 공개키(Public Key) -> 코인주소(Address) |



![img](https://github.com/BettySuna/wallet/blob/master/img/05.%EB%B8%94%EB%9F%AD%EC%B2%B4%EC%9D%B8%EC%A7%80%EA%B0%91%EA%B5%AC%EC%A1%B0%EB%8F%84.jpg?raw=true)

>암호화폐는 물리적이거나 파일 형태로 존재하지 않으며 블록체인상에 존재합니다.
>간혹 콜드 월렛(USB 형태의)에 파일 형태로 저장되는 것으로 오해하시는 분들도 있습니다.
>지갑은 블록체인 네트워크상의 암호 자산에 접속하여 소유권을 인정받고 전송하는 기능을 합니다.
>따라서 지갑이 삭제(S/W, APP) 또는 분실, 파손(USB, 스마트폰) 되었다고 해서 코인이 함께 사라지는 것이 아니며 씨드키가 보존되어 있다면 지갑을 언제든지 복구할 수 있는 것입니다.



그 만큼 씨드키(Seed)와 개인키(Private Key)가 매우 중요! 별이 다섯 개 ! `★★★★★`



> 월렛은 기본적으로 계정이나 코인 주소를 저장하여 보관하는 수단이며 코인이 보존되어 있는 블록체인 네트워크에 연결해야만 지갑과 개인키를 이용하여 송금이나 거래를 할 수 있기 때문에 결국은 온라인과 연결이 되어야 작동을 합니다. 따라서 콜드 월렛 속에 코인이 들어 있다는 오해는 이제 그~만~



만약 개인키를 잃어버린다면 해당 코인이 있는 블록체인 네트워크에 접근할 수 없으므로 소유권을 주장할 수 없는 것입니다.~~ 
때문에 개인키가 없이는 당신의 코인을 어딘가로 전송(판매) 할 수 없게 되는 것이지요.
결국 당신 것이지만 당신 것이 아닌 게 되는 것입니다. `★★★★★`



| 여기서 잠깐!                                                 |
| ------------------------------------------------------------ |
| 블록체인이 혁신기술이라 불리는 가장 큰 이유는 해킹이 불가능하며 그 누구도 블록체인 네트워크 상의 원장(거래 기록)을 마음대로 조작하거나 고칠 수 없기 때문입니다. <br/>조작이나 위 변조가 가능했다면 코인 자산을 마음대로 늘리거나 무한대로 만들어 팔겠죠? <br/>그게 가능하다면 블록체인 자체가 해커에게 뚫린 상황이나 다름이 없기 때문에 코인 시장이 폭망하겠죠. |



## 지갑의 형태

![img](https://github.com/BettySuna/wallet/blob/master/img/06.%ED%95%AB%EC%9B%94%EB%A0%9B%EA%B3%BC%EC%BD%9C%EB%93%9C%EC%9B%94%EB%A0%9B.jpg?raw=true)



#### **거래소** - 거래소의 월렛에서 사용자들에게 할당 되어진 코인주소

| 장점                                | 단점                                           | 대상               |
| ----------------------------------- | ---------------------------------------------- | :----------------- |
| 코인 거래 시 편리함                 | 거래소는 해커들의 주 표적이다.                 | 단기 트레이더      |
| 월렛이나 개인키를 만들 필요 없다.   | 에어드롭을 받을 수 없다.(거래소 별도 처리)     | 소액 투자자        |
| 별도 보안키를 관리하지 않아도 된다. | 거래소 보안 시스템에 의존.                     | 거래소 보안 신뢰자 |
| 로그인(접근)이 비교적 쉽고 빠르다.  | 거래 기록은 블록체인 원장에 기록 안됨.         |                    |
|                                     | 입, 출금이 막히거나 지연될 수 있다.            |                    |
|                                     | 법적으로 유실 자산에 대한 보호를 받을 수 없다. |                    |

> 업비트, 빗썸, 코인원 등...

---



#### **핫월렛** - 인터넷에 연결되어 있는 온라인 지갑

| 장점                               | 단점                                   | 대상                      |
| ---------------------------------- | -------------------------------------- | ------------------------- |
| 거래소의 해킹사고에서 비교적 안전  | 거래를 위해 거래소 입 출금 시 번거로움 | 자금 규모가 크지 않은 분  |
| 개인 소유 지갑                     | 철저한 개인키 관리 필요                | 컴퓨터 보안에 능숙한 분   |
| 콜드월렛에 비해 비교적 접근이 편리 | 월렛 제공 업체의 신뢰 필요             | 온라인월렛 보안을 믿는 분 |

> 웹사이트기반 월렛, PC설치 월렛(소프트웨어), 모바일(APP)월렛 등

---



#### **콜드월렛** - 인터넷과 단절되어 있으며 보안성이 뛰어난 오프라인 하드웨어 월렛

| 장점                            | 단점                                  | 대상                    |
| ------------------------------- | ------------------------------------- | ----------------------- |
| 개인소유 월렛을 사용할 수 있다. | 월렛 구매 비용이 발생(5만~50만원)     | 자금 규모가 큰 투자자   |
| 거래소의 해킹사고에서 안전함.   | 철저한 시앗키(복구문구) 관리 필요     | 장기 투자자             |
| 마음의 평화가 찾아 온다.        | 복구키를 오프라인에 기록 관리         | 심리적 불안감이 심한 분 |
|                                 | 도난이나 화재 수해 등의 유실 위험     |                         |
|                                 | 사용시 PC나 모바일에 연결이 다소 불편 |                         |

> 나노 렛저 S(X), Trezor, 디센트,KASSE, 쿨월렛, keepkey, fuze 등

---



#### **종이(인쇄)월렛** - 인터넷과 단절 되어 있으며 종이에 개인키를 적어서 보관하는 종이 월렛

| 장점                        | 단점                                                         | 대상                   |
| --------------------------- | ------------------------------------------------------------ | ---------------------- |
| 개인월렛을 사용할 수 있다.  | 사용이 필요한 경우 메모를 보며     직접 타이핑해야 하는 번거로움. | 장기투자자             |
| 온라인 해킹사고에서 안전함. | 철저한 종이의 관리 필요.                                     | 심리적 불안감이 심한자 |
|                             | 도난이나 화재 수해 등의 유실 위험                            | 보관 금고 소유자       |
|                             | 복사가 쉽다.                                                 | 거래소 불신자          |

> [https://www.bitaddress.org](https://www.bitaddress.org/) 등

---

```
※ 본인의 스타일에 맞는 월렛을 선택하시면 됩니다.
```



## 거래소 월렛?



여러분들의 코인은 안녕하십니까?

> 결론부터 말씀드리면 필자는 암호화폐를 거래소에 보관하는 것을 추천하지 않습니다. 
> 물론 소액(단타) 투자자와 개인지갑 사용에 자신 없는 자 그리고 거래소를 맹신하는 자께서는 어쩔 수 없다고 봅니다.



거래소가 해킹 당하면?

> 거래소 코인 주소는 개인 투자자의 소유가 아니며 거래소의 월렛입니다.
> 아직 법적 보호장치가 없고 해킹 시 거래소의 도의적 보상(?) 이외에는 방법이 없는 것이 사실입니다.
> 실제로 거래소 직원으로 위장 취업해 탈취하거나, 해킹으로 꾸며낸 거래소의 자작극, 심지어 거래소 대표가 갑자기 심장마비로 사망하여 콜드 월렛에 접근할 수 없는 경우 등 우리가 어떻게 할 수 없는 유실 유형도 다양하죠...



```
※ 장기 투자자이며 거래소를 믿을 수 없고 키 관리를 잘 할 수 있다면 개인 월렛
※ 소액이며 단기투자자 이것저것 귀찮고 거래소 믿어 보겠다면 거래소 월렛
```

![img](https://github.com/BettySuna/wallet/blob/master/img/07.%EB%A7%88%EC%9A%B4%ED%8A%B8%EA%B3%A1%EC%8A%A4.jpg?raw=true)

> 2013년 마운트곡스 거래소 해킹 사건에서 10만 고객의 비트코인 75만 개가 탈취됨



| 조심!                                                        |
| ------------------------------------------------------------ |
| ※ 거래소 지갑은 개인소유의 지갑이 아니며 거래를 위해 거래소 소유의 지갑에 위탁해 두는 개념입니다.<br/>해커들은 거대한 자금을 운용하는 거래소를 가장 큰 목표로 삼고 호시탐탐 노리고 있습니다. <br/>물론 해킹 이슈가 100% 해커의 범죄가 아닌 듯한 정황도 많이 느끼고 있죠….헥헥..ㅠㅜ |



## 콜드 월렛 형태와 장단점

|                                          | 장점                                                         | 단점                                                         |
| ---------------------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| 하드웨어 월렛<br />(렛저나노, 토레져 등) | 안전한 보안<br />복사할 수 없다<br />타거나 썩지 않는다<br />복구할 수 있다 | 입출금이 자유롭지 못하다<br />파손의 위험이 있다<br />방수가 되지 않는다<br />유료이다 |
| 종이 월렛<br />(인쇄된 월렛)             | 무료이다<br />카드 형태로 선물할 수 있다<br />휴대하기 쉽다  | 프린터를 믿어야 한다<br />도난의 위험이 있다<br />썩거나 불에 탈 수 있다<br />복사하기 쉽다<br />방수가 안된다 |
| PC 월렛<br />(월렛 제공업체의 PC버전)    | 사용하기 쉽다<br />쉽게 다운 받을 수 있다<br />비교적 안전한 보안 | 복구할 수 없다<br />해킹당할 수 있다<br />불타거나 훼손 될 수 있다 |
| USB드라이브<br />월렛이 설치된 USB메모리 | 사용하기 쉽다<br />쉽게 구할 수 있다.                        | 도난이나 파손의 위험이 있다<br />자석등에 의해 손상될 수 있다<br />복구가 어렵다 |



## 해킹 방법은?

![img](https://github.com/BettySuna/wallet/blob/master/img/08.%ED%95%B4%EC%BB%A4%EC%9D%B4%EB%AF%B8%EC%A7%80.jpg?raw=true)

> 피싱사이트, 디도스, 멀웨어, 바이러스, 악성코드, 키로거, DNS스푸핑, IP스푸핑, APT, 누킹, 부르트포스, 사전공격, 파밍, 제로데이, e메일해킹, 클라우드해킹, 보이스피싱, 키보드후킹, 클립보드가로채기, 공유기, 블루투스 좀비 등...



| 상상초월!                                                    |
| ------------------------------------------------------------ |
| 이 밖에도 상상을 초월하는 방법과 다양한 경로로 해킹되고 있습니다.<br/>과연 해커 집단에게 주 타깃은 개인일까요? 거래소일까요?<br/>필자는 개인적으로는 거래소가 고객의 자산을 자의든 타의든 100% 지켜주지 못할 것이라고 확신합니다.<br/>얼마 전 추적 60분 팀에서 부산저축은행 비리 사태에 대해서 다뤘더군요.(생략) |



---



## 해킹 방지는?

![img](https://github.com/BettySuna/wallet/blob/master/img/09.%ED%8C%A8%EC%8A%A4%EC%9B%8C%EB%93%9C%EC%9D%B4%EB%AF%B8%EC%A7%80.jpg?raw=true)

> 해킹을 근본적으로 방지할 수 있는 방법은? (아래에 계속)

| 중요!                                                        |
| ------------------------------------------------------------ |
| 개인키(Seed or Private Key)를 절대로 컴퓨터나 스마트폰(Internet)에 보관하지 않아야 합니다. |

![img](https://github.com/BettySuna/wallet/blob/master/img/%EC%BD%94%EC%9D%B8%EC%A3%BC%EC%86%8C%EB%A9%94%EB%AA%A8%EC%9E%A5X.jpg?raw=true)

---



## 해킹 사례는?

▷ 아래는 연도별 거래소 해킹 사례

| 2012년                                                       | 2016년                                                       |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| 9월 비트플로어(bitfloor) $250,000<br />12월 비트마켓(bitmarket) $260,000 | 8월 비트파이넥스 $72,000,000                                 |
| **2013년**                                                   | **2017년**                                                   |
| 5월 버큐렉스(Vircurex) $50,000,000 <br />11월 인풋(inputs) $1,200,000 <br />11월 빕스(bips) $1,000,000<br />11월 피코스탁스 $6,000,000 | 4월 야피존 $5,300,000 <br />4월 유빗(youbit) 17% 자산 <br />12월 나이스해시 $60,000,000 |
| **2014년**                                                   | **2018년**                                                   |
| 2월 마운트곡스(MT.GOX) $460,000,000 <br />3월 폴로닉스(POLONIEX) $50,000 <br />7월 크립트시(Cryptsy) $9,500,000 <br />7월 민트팔(mintpal) $2,000,000 <br />10월 비트페이(bitpay) $1,800,000<br />10월 민트팔(mintpal) $1,500,000 | 1월 코인체크 $534,800,000 <br />2월 비트그레일 $195,000,000 <br />4월 코인시큐어 $3,300,000 <br />6월 코인레일 $40,000,000 <br />6월 빗썸 $31,500,000 <br />9월 자이프 $60,000,000 |
| **2015년**                                                   | **2019년**                                                   |
| 1월 796익스체인지 $230,000 <br />1월 비트스탬프 $5,100,000<br />2월 비터 $1,750,000 | 5월 빗썸 $8,500,000<br />5월 바이낸스 $40,000,000            |

| 그리고!                                                      |
| ------------------------------------------------------------ |
| ※ 과연 거래소 해킹이 정말 해커에 의해서만 탈취되었을까요? (나머지는 여러분들의 상상에...)<br/>	현재까지 한국에서 거래소 해킹으로 피해를 입은 투자자의 보호를 위해 마련된 법적 장치는 없습니다.. |



## 그럼 어떻게?



![img](https://github.com/BettySuna/wallet/blob/master/img/%EB%A0%9B%EC%A0%B8%EB%82%98%EB%85%B8%EB%B3%B5%EA%B5%AC%ED%82%A4%EC%9D%B4%EB%AF%B8%EC%A7%80.jpg?raw=true)



> 거래가 필요한 경우에만 필요분 만 거래소에 전송하고 그 외엔 최대한 개인 월렛(콜드 월렛)에 보관해야 합니다.
> 그러나 개인 월렛에 보관한다고 해서 해킹의 위험에서 완전히 벗어날 수 있는 것은 아닙니다.
> 때문에 개인 월렛의 보안에 관해서 우리는 더욱 논의해야 하며 노력해야 합니다.(아래에 계속)
> 가장 중요한 사실은 자신의 개인키를 탈취당하면 한 번의 실수로 모든 자산을 잃어버릴 수 있습니다.
> 현재는 거래소를 이용하지 않고도 거래를 할 수 있는 방법(교환 거래)도 있습니다.



## 멘/탈/붕/괴

여기 계십니다. (레전드님)
실제로 7500개의 비트코인(현재가치 약 740억)이 들어있는 지갑의 개인키(Private Key)를 하드디스크에 보관해 두다가 쓰레기 매립장에 버려 쓰레기 더미를 파헤치다 결국 찾지 못해  멘붕에 빠진 한 남성이 있습니다.

![img](https://github.com/BettySuna/wallet/blob/master/img/10.%ED%9D%91%EC%9A%B0%EC%98%A4%EB%B9%A0.jpg?raw=true)

> 잃어버린 비트코인을 찾지 못하는 불운의 사나이



| 그러므로                                                     |
| ------------------------------------------------------------ |
| ※ 당신이 쓰레기 매립장에서 하드디스크를 찾을 수 없다면 당신의 비트코인은 블록체인 네트워크 속에서 주인을 만나지 못한 체 영원히 표류해야 합니다. <br />덕분에 비트코인의 희소가치도 한 단계 높아졌습니다. |



## 지갑 형태별 제공업체

![img](https://github.com/BettySuna/wallet/blob/master/img/11.%EB%B9%84%EC%BD%94%EC%A7%80%EA%B0%91.jpg?raw=true)

> 지갑을 비교 선택하실 분들은 아래 링크에 접속해서 꼼꼼히 비교해 보시고 선택하세요.
> (나열 순서와 선호도 무관)

| 웹(Web)또는 PC월렛                                           | 콜드월렛(하드웨어)                                           | 모바일(APP)월렛                                            |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ---------------------------------------------------------- |
| [https://wallet.btc.com](https://wallet.btc.com)             | [https://www.ledger.com](https://www.ledger.com)             | [https://www.coinus.io](https://www.coinus.io)             |
| [https://www.myetherwallet.com](https://www.myetherwallet.com) | [https://trezor.io](https://trezor.io)                       | [https://enjinwallet.io](https://enjinwallet.io)           |
| [https://coolwallet.io](https://coolwallet.io)               | [https://dcentwallet.com](https://dcentwallet.com)           | [https://www.huobiwallet.com](https://www.huobiwallet.com) |
| [https://keys.casa](https://keys.casa)                       | [https://fuzeway.com](https://fuzeway.com)                   | [https://trustwallet.com](https://trustwallet.com)         |
| [https://token.im](https://token.im)                         | [http://coolwallet.co.kr](http://coolwallet.co.kr)           | [https://coinmanager.io](https://coinmanager.io)           |
| [https://metamask.io](https://metamask.io)                   | [https://keepkey.myshopify.com](https://keepkey.myshopify.com) | [https://edge.app](https://edge.app)                       |
| [https://bitberry.app](https://bitberry.app)                 | [https://coolwallet.io](https://coolwallet.io)               | [https://www.coinomi.com](https://www.coinomi.com)         |
| [https://electrum.org](https://electrum.org)                 | [http://hd-kasse.com](http://hd-kasse.com)                   | [https://brd.com](https://brd.com)                         |
| [https://jaxx.io](https://jaxx.io)                           | [https://www.temexe.com](https://www.temexe.com)             | [http://wallet.io](http://wallet.io)                       |

> 이 밖에도 많은 종류의 월렛들이 존재하고 계속 생겨나고 있기에 우리는 해킹 사례 등의 사용자 경험을 지속적으로 공유하여야 하며 보안 기능이 좋은 월렛을 찾아서 알려야 한다고 생각합니다.

![img](https://github.com/BettySuna/wallet/blob/master/img/12.%EC%97%94%EC%A7%84%EC%9B%94%EB%A0%9B.jpg?raw=true)

> 필자는 기존 거래소 사용자들이나 웹(PC) 월렛 사용자들이 모바일 월렛으로 이동할 것으로 예상됩니다.
> 모바일 연동형 콜드 월렛과 월렛별 보안의 안전성 등을 사용자 경험과 리뷰를 통해 지속적으로 검증해 볼 필요가 있다고 생각합니다.

| 추천!                                                        |
| ------------------------------------------------------------ |
| 아래는 필자가 괜찮다고 생각하는 니모닉(복구 단어) 백업 기능 모바일 월렛들 (필자는 아래 업체들과 무관.)<br/>모바일 월렛은 신중히 선택해야 합니다. 씨드키는 백업하지만 개인키는 APP에서 보관하기 때문입니다. |

- 엔진 월렛 Enjin - 싱가폴
  - 보안이 강함, 다양한 코인과 토큰 지원, 바이낸스DEX 외 5곳의 교환거래소 이용 가능 단, 리플 아직 미지원

- 후오비 월렛 Huobi - 싱가폴(중국)
  - 리플 포함 다양한 월렛 지원 보안 기술이 뛰어난 고스트 월렛사와 기술 협의 중

- 코인베이스 월렛 Coinbase - 미국
  - 리플, TrueUSD 등 다양한 알트코인 지원, 코인베이스 거래소와 지갑 간 이동 편리(거래가 빈번한 분들의 대안?

- 코이노미 월렛 Coinomi - 미국
  - 코인 종류 다양, 교환거래 지원, 두터운 기존 사용자, 평가 좋음, 바이낸스 DEX와 협력 등(해킹 이슈 있었으나 미확정)



| 여기서 잠깐!                                                 |
| ------------------------------------------------------------ |
| 여기서 잠깐! 우리가 흔히 말하는 비트코인 해킹 위험이라 함은? <br/>해커가 블록체인 네트워크 상에 존재하는 암호화 코인을 공격해서 탈취해가는 의미가 아니며 <br/>해당 코인의 소유권이나 다름없는 개인키를 탈취해가는 것입니다. <br/>해커는 개인키 탈취에 성공하면 블록체인 네트워크 상의 훔친 코인을 해커의 지갑이나 거래소로 이동시키겠죠. |



## 개인키의 종류와 형태



- 개인키 (Private Key)
![img](https://github.com/BettySuna/wallet/blob/master/img/13.%EA%B0%9C%EC%9D%B8%ED%82%A4%EC%98%88.JPG?raw=true)
  
  > 일반적인 개인키이며 복잡하여 받아 적기 힘들고 타이핑 시 오타의 확률이 높으며 그 때문에 PC에(메모장, 이메일, 클라우드 등) 저장할 경우 해커의 표적이 될 수 있으며 타이핑의 부정확도로 인해 복사 후 붙여넣기를 하게 되고 그 경우 키보드 후킹 기법이나 클립보드 가로채기 등으로 해킹 위험에 노출된다. (실제로 개인키를 텔레그램에 실수로 붙여넣기 해서 탈취당한 사례)



------



- 키스토어 파일 (Keystore)

  ![img](https://github.com/BettySuna/wallet/blob/master/img/14.%ED%82%A4%EC%8A%A4%ED%86%A0%EC%96%B4%EC%9D%B4%EB%AF%B8%EC%A7%80.jpg?raw=true)

  >개인키를 암호화하여 작성된 텍스트 파일, 파일 형태이기 때문에 PC나 USB 메모리 등 파일 저장 스토리지 등에 보관, 
  >사용하기 위해서는 온라인에 노출되어야 하며 그 경우 해커의 표적이 될 수 있다.



------



- 니모닉 단어 (Mnemonic Phrases)

  ![img](https://github.com/BettySuna/wallet/blob/master/img/15.%EB%8B%88%EB%AA%A8%EB%8B%89%EC%98%88.jpg?raw=true)
  
  >지갑 복원이 가능한 씨드키를 복잡한(Entropy+SHA256+Checksum) 알고리즘을 거쳐 12개 또는 24개의 단어로 변환하여 비교적 알아보기 쉬운 단어의 조합으로 만든 키(Seed). 오타율이 적고 인터넷이 연결되지 않은 곳에 적어두거나 기록하여 보관하기 용이하다. 해커의 표적에서 안심할 수 있지만 기록물의 화재, 파손, 도난 등의 유실 가능성이 있다.
>(나노S 등 다양한 하드웨어 월렛과 모바일 월렛 시스템에서 대부분 니모닉 사용)
  >우리는 씨드키로 활용되는 니모닉 단어에 대해서 아래에 이야기를 계속하겠습니다.





```
우리는 지갑 보안에 가장 많이 활용되고 있는 니모닉에 대하여 아래에 조금 더 알아보겠습니다.
```



## 니모닉 이란?

![img](https://github.com/BettySuna/wallet/blob/master/img/16.%EB%8B%88%EB%AA%A8%EB%8B%89%EC%9D%B4%EB%AF%B8%EC%A7%80.png?raw=true)



| 니모닉 어원                                                  |
| ------------------------------------------------------------ |
| Mnemonic의 어원은 기억의 여신 ‘Mnemosyne’ 이다.<br/>그리스어로 ‘기억', ‘생각하다'라는 뜻을 가지고 있고,<br/>Mnemonic은 오늘날 ‘기억술' 이나 ‘기억 증진법'을 의미한다. |

| 지갑에서의 의미                                              |
| ------------------------------------------------------------ |
| 코인 지갑 보안 개념의 니모닉(Mnemonic) 이란?<br/>암호화폐 지갑에서 사용하는 니모닉 단어는  복잡한 컴퓨터 암호코드보다 쉽게 인지하고 오타나 실수를 줄이기 위해 암기가 가능한 12~24개의 단어를 생성하여, 그것을 기반으로 지갑 복구용 씨앗키로 활용 된다. |

> 니모닉은 암호화폐 지갑 기술이 발전됨에 따라 지갑을 쉽고 안전하게 사용하기 위해 업계 표준이 되고 있으며 대부분의 지갑에 채택되어 지갑들이 상호 운용될 수 있도록 만들고 있습니다. 
> 사용자는 이러한 지갑들 중 하나에 생성된 니모닉을 다른 지갑으로 가져와 모든 키와 주소를 복구할 수 있습니다.



![img](https://github.com/BettySuna/wallet/blob/master/img/17.%EB%8B%88%EB%AA%A8%EB%8B%89%EC%9E%91%EC%84%B1%EB%90%9C%EC%A2%85%EC%9D%B4.jpg?raw=true)

---



## 니모닉 복제 가능성?

![img](https://github.com/BettySuna/wallet/blob/master/img/04.%EB%8B%88%EB%AA%A8%EB%8B%89%EC%83%9D%EC%84%B1%EA%B3%BC%EC%A0%95.jpeg?raw=true)

필자는 암호학자가 아니라서 복잡한 수학적 계산 방식을 나열하진 않겠습니다.(위 그림은 보지 마세요 ㅎㅎ)
수학자들에 따르면 씨드키 무작위 대입을 통해 똑같은 개인키를 생성하려면

> 340,282,366,920,938,463,463,374,607,431,768,211,456개의 경우의 수

이것을 해커가 분석하여 생성하려면 일반 PC로 약

> 847,904,136,496,835,804,725,427년의 시간

그리고 또 하나 풀어야 하죠? 니모닉 생성 시 옵션으로 함께 만든 Pin-code 비밀번호

> 혹자는 이렇게 표현합니다. 우주에서 바늘 찾기…

무작위 대입을 통해 지갑을 탈취당할 가능성은 없다고? 봐도? 되겠죵?ㅎㅎ

> 따라서 니모닉 단어 유출만 안되도록 신경 쓴다면 안전합니다.
> 그렇다면 니모닉 단어가 유출되지 않도록 어떻게 신경 써야 할까요? (아래에 계속)



## 니모닉 백업 방법

![img](https://github.com/BettySuna/wallet/blob/master/img/19.%EB%A6%AC%EC%BB%A4%EB%B2%84%EB%A6%AC%EC%8B%9C%EB%93%9C.jpg?raw=true)

>지갑 생성 시 보안을 니모닉(Mnemonic Recovery Phrase)으로 선택 (월렛별 방법 상이)
>지갑에서 랜덤으로 생성된 니모닉 단어를(12-24개) 컴퓨터에 저장하지 않고 종이에 정확하게 순서대로 메모

![img](https://github.com/BettySuna/wallet/blob/master/img/20.%EB%8B%88%EB%AA%A8%EB%8B%89%EC%84%B8%ED%8C%85.png?raw=true)![img](https://github.com/BettySuna/wallet/blob/master/img/21.%EB%8B%88%EB%AA%A8%EB%8B%89%EC%A0%81%ED%9E%8C%EC%A2%85%EC%9D%B4.jpg?raw=true)

※ 이때 단어의 스펠링과 순서가 바뀌지 않게 주의해야 하며 물에 번지는 펜을 쓰지 말아야 한다.



## 니모닉 보관 방법

![img](https://github.com/BettySuna/wallet/blob/master/img/22.%EB%8B%88%EB%AA%A8%EB%8B%89%EB%B3%B4%EA%B4%80%ED%83%80%EC%9D%B4%ED%8B%80.jpg?raw=true)



| 펜과 종이를 가지고 당신의 니모닉 문구를 기록하십시오.        |
| ------------------------------------------------------------ |
| 오랫동안 종이와 펜은 데이터를 기록하는데 유용하게 사용된 도구 |

| 복구 문구를 두 장 이상 작성하고 각각 다른 위치의 금고에 보관하십시오. |
| ------------------------------------------------------------ |
| 천재 지변 화재, 홍수 등이 발생한 경우를 대비<br />![img](https://github.com/BettySuna/wallet/blob/master/img/23.%EC%B0%A2%EC%96%B4%EC%A7%84%EC%A2%85%EC%9D%B4.jpg?raw=true) |

| 복구 문구를 절대 스크린샷이나 사진을 찍어 저장하지 마십시오. |
| ------------------------------------------------------------ |
| 누군가 컴퓨터/모바일을 훔쳐보거나 해킹하여 복사할 수 있기 때문 |

| 복구 문구의 디지털 파일 (메모장 등)을 만들지 마십시오. |
| ------------------------------------------------------ |
| 그것을 이메일이나 클라우드 서비스에 저장하지 마십시오. |

| 복구 문구 생성 시 비밀번호 옵션(Pin code)을 선택 하십시오. |
| ---------------------------------------------------------- |
| 복구 시드 보안을 한 단계 더 높일 수 있습니다.              |

| 기억력이 좋은 분들은 복구 문구를 모두 외우십시오. |
| ------------------------------------------------- |
| 이 경우 사망 시 상속 불가! (기록 후 기억)         |

| 당신의 자금에 대해 걱정이 크다면 천재지변에 대비할 수 있도록 키를 기록해야 합니다 . |
| ------------------------------------------------------------ |
| 이 방법은 복구 문구를 강철판에 새겨 넣어 금고에 보관합니다.  |

| 종이에 적은 니모닉 단어를 화재나 물 등 보존력이 강한 스틸 제품으로 교체 |
| ------------------------------------------------------------ |
| 아래에 샘플 제품 이미지 참고                                 |

> 당신의 사망할 경우를 대비해 가장 신뢰할 수 있는 가족 구성원에게 키 복구 방법을 알려줍니다.
> 상속인이 상속받은 자금을 새로운 지갑에서 복구하는 방법을 모를 수 있기 때문입니다.
> 그러나 이 방법이 조심스러운 이유는 만약 당신이 엄청난 양의 자산을 보유하고 있는 경우 당신의 돈을 얻기 위해 당신에게 해를 끼칠 수도 있습니다. (꼭! 신뢰하는 가족 구성원에게!)

------

![img](https://github.com/BettySuna/wallet/blob/master/img/24.%EB%8B%88%EB%AA%A8%EB%8B%89%EC%9B%94%EB%A0%9B%EB%AC%B6%EC%9D%8C.jpg?raw=true)



## 마치며…

![img](https://github.com/BettySuna/wallet/blob/master/img/coinwoman.jpg?raw=true)

살림하는 아줌마로써 틈나는 대로 공부하며 수집한 정보를 토대로 작성되었으며 저만의 생각도 일부 투영 되었을 수 있으나 보안에 관해 서로 토론하고 공유함으로써 회원들의 지갑이 더 안전해지길 바라는 마음입니다.



다음 편 또 공부할 시간이 주어진다면 좀 더 고급 내용인 HD 지갑 과 하이브리드 월렛, 멀티 SIG 지갑, 교환거래 등을 좀 더 깊이 공부해 보고 싶습니다.



부족한 기록 읽어 주셔서 감사합니다.^^
H채널에서 열공중이신 어머님, 아버님 포함 구독자 모두 성공투자하시길 기원드립니다.





감사합니다.



*Betty Sun*
