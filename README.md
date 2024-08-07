# Daum 우편번호 서비스

[Daum 우편번호 서비스](http://postcode.map.daum.net/guide)는 웹사이트에서 도로명 주소와 우편번호(기초구역번호)를 검색할 수 있는 **Javascript API**입니다.  
Sample 코드와 상세 Reference는 [http://postcode.map.daum.net/guide](http://postcode.map.daum.net/guide) 에서 확인할 수 있습니다.  

문의 사항은 먼저 아래 FAQ를 확인해주시고, [Issue로 등록해주시면 됩니다.](https://github.com/daumPostcode/QnA/issues)

---

## >> [업데이트 소식 바로가기(Click!!)](https://github.com/daumPostcode/QnA/blob/master/PATCHNOTE.md)

업데이트 소식을 더 보기 편하시도록 페이지를 이동하였습니다. 업데이트와 관련된 사항은 위 링크된 페이지를 확인해 주세요.
추가적인 업데이트의 자세한 내용은 **[가이드 페이지](http://postcode.map.daum.net/guide)** 를 참고해 주세요.

---



## 자주 묻는 질문(FAQ)

### 1. 주소가 없습니다 / 검색되지 않습니다.

다음 우편번호 서비스 API는 **도로명 주소가 발급된 주소만 검색이 가능**합니다 (자세한건 아래 추가사항 참고)

그렇기 때문에 주소가 검색이 안된다면 우선 [행정안전부 도로명주소 검색시스템](http://juso.go.kr)에서 검색이 되는지 확인해 주세요. 만약 행정안전부 도로명주소 검색시스템에서 검색이 되지 않는다면 직접 등록 요청을 하셔야 합니다. 
 
1. 행정안전부 도로명 주소 검색시스템 접속  
2. 상단 메뉴 중 "고객지원" -> "도움센터(Q&A)" 클릭  
3. 게시판에 해당 주소에 대해서 등록 요청 글을 남기시면 됩니다.(로그인 필요)  

위 단계를 통해 해당 주소가 행정안전부 도로명 주소 검색시스템에 등록이 되면, Daum 우편번호 서비스 시스템에는 등록된 날로부터 1일 후에 업데이트 됩니다.  
만약 행정안전부 도로명 주소 검색시스템에서는 검색이 되는데 Daum 우편번호 서비스에서 검색이 되지 않는다면, 검색 방식의 차이로 인한 오류일 수 있으니 [Issue로 등록해주시기 바랍니다](https://github.com/daumPostcode/QnA/issues).

**추가사항**

국가보안시설(주요 기관, 발전소 등)로 지정된 곳의 주소의 경우, 검색결과에서 "지도" 버튼이 자동 삭제가 됩니다.(행안부 도로명검색 시스템과 동일)
이부분 참고해 주시기 바랍니다.


### 2. 주소에 있는 건물명이 실제 명칭과 다릅니다. 
1번 질문과 같은 방식으로 확인하시면 됩니다. 주소 데이터는 저희가 수정할 수는 없습니다.

### 3. 6자리 구우편번호가 필요합니다 
2015년 8월 1일 부로 6자리 구우편번호는 우정사업본부에서 더이상 생성/관리되지 않으므로 5자리 새우편번호(기초구역번호)를 이용하셔야 합니다.  (참고. [우정국 새우편번호 시행 공지](http://www.epost.go.kr/main.retrieveNoticeContent.comm?news_seq_no=900))  현재 일부 제공되고 있는 6자리 구우편번호는 시간이 지남에 따라 삭제될 예정입니다.


### 4. REST API로도 제공하고 있나요?
제공 계획은 없습니다.

### 5. 정말 아무에게나 무료인가요? 회사에서 상업적인 용도로 써도 무료인가요?
레알 100% 무료입니다.

### 6. 하루 사용량 제한이 있나요?
레알 100% 무제한 입니다.

### 7. 하단 로고를 안보이게 할 수 없나요?
로고는 정책상 반드시 노출하는 것을 원칙으로 하고 있습니다. 하단의 'Powered by kakao' 을 통한 저작자 표기 정책은 Daum 우편번호서비스를 지속적으로 무료 운영할 수 있는 근거로 활용되고 있으며, 로고를 숨길 경우에는 사용상의 제약을 받을 수 있습니다.

### 8. UI를 변경하는 기능이나 옵션은 없나요?
현재 [우편번호 서비스 화면의 색상을 변경할 수 있는 테마기능](http://postcode.map.daum.net/guide#themeWizard)과 '영문보기','지도' 버튼을 가릴 수 있는 옵션을 제공하고 있습니다.
단, 이외 UI컴포넌트 추가 및 레이아웃 변경과 같은 기능은 제공하고 있지 않습니다.

### 9. 모바일앱에서도 사용할 수 있나요?
웹뷰를 이용하여 하이브리드앱 제작 방식으로 사용할 수 있습니다. 단, html,js,css들을 정적으로 넣고 실행하는 경우에는 데이터 전달이 되지 않기 때문에, 페이지를 호출하는 방식으로 사용하셔야 합니다.

### 10. iOS/Android에서 webview를 이용하여 사용할 수 있나요?
9번과 같이 정적 html,js,css가 아닌 http(s)프로토콜을 사용한 페이지를 호출하는 페이지에서는 사용가능합니다.  
단, 기본 webview의 경우 우편번호서비스의 open메소드를 이용한 팝업방식 보다는 embed메소드를 이용한 레이어 방식을 사용하시길 권해드립니다.  
이유는 기본적인 webview에서 open메소드 사용시, 팝업이 뜨기보다 기존페이지에서 우편번호서비스 페이지로 이동이 되어 버리기 때문에, 데이터 전달이 되지 않습니다. 반드시 open메소드를 사용하시고자 하실때에는 각 플랫폼의 webview에서 window.open에 대응할 수 있도록 webview를 개선하여 사용하시기 바랍니다.

### 11. typescript나 node 모듈로 이용할 수 있나요?
아뇨. 현재 대응하고 있지 않습니다.

### 12. 팝업창에서 검색 후 결과를 클릭해도 반응이 없습니다.
혹시 웹서버 환경에서 확인하고 계신가요? 정적페이지로 브라우저에서 파일을 오픈하여 사용할 경우에는 host정보를 알 수 없어 데이터 전달이 되지 않습니다.

### 13. 팝업창이 비어 있는 채로 뜹니다.
혹시 document.domain을 사용하고 계신가요? Daum 우편번호 서비스를 사용하시는 페이지에서는 document.domain값을 임의로 세팅하는 경우에 일부 IE 브라우저에서 제대로 동작하지 않습니다.

### 14. 검색 후 결과 클릭한 후 팝업이 닫히지 않습니다(값이 입력되거나 또는 입력되지 않는 상황).
FAQ 13번의 이슈가 아니라면, javascript 실행시 오류가 난 경우입니다. oncomplete 함수에서 사용하는 변수가 정확한지, input tag의 id값을 잘못 사용하고 있는지 확인해 보시길 바랍니다. 브라우저의 개발자 도구 활용을 권장합니다. (팝업형의 경우 개발자 도구는 팝업창에 focus를 두고 개발자 도구를 띄우셔야 합니다.)
> 예를 들면, document.getElementById() 함수 이용시,   
> IE9이하에서는 input tag의 name값으로도 노드를 가져올 수 있지만, 그 외 브라우저에서는 null을 리턴합니다.   
> 그렇기 때문에 반드시 id 속성을 사용하시기 바라며,   
> 그렇지 못할 경우에 다른 셀렉터 함수(document.querySelector, jQuery selector 등)를 사용하시기 바랍니다.

### 15. javascript API 코드를 복사해서 사용해도 되나요?
javascript API 코드를 복사하여 자체 서버에 업로드 하여 사용하실 경우에는 추후에 기능적인 업그레이드로 인한 지원을 받으실 수 없기 때문에 오류가 발생하거나 사용상의 제약을 받을 수 있습니다.

### 16. 사용자가 지번/도로명 중 어떤 것을 선택하더라도 무조건 도로명 주소만 이용하고 싶은데.. 어떻게 해야되나요?
사용자가 선택한 값(userSelectedType)과 상관 없이 로직상 autoRoadAddress변수를 체크하고, 값이 없으면 roadAddress변수를 이용하시면 됩니다.  
도로명 주소의 데이터가 셋팅되는 방법에 대해서 추가 설명 드리자면  
**(autoMapping을 true로 설정한 경우 - 기본값)**  

* 사용자가 지번-도로명 1:N 관계에서 메인 지번주소를 선택할 경우, 도로명 주소는 autoRoadAddress에 들어가게 됩니다. 또한 연관된 도로명 주소를 선택하게 되면 roadAddress에 들어가게 됩니다.
* 사용자가 지번-도로명 1:1 관계에서 메인 지번주소나 연관된 도로명주소를 선택하면, 도로명 주소는 roadAddress에 들어가게 됩니다.
* 사용자가 도로명-지번 1:N, 1:1 관계에서 메인 도로명주소를 선택하거나 연관된 지번주소를 선택할 경우, 도로명 주소는 address, roadAddress에 들어가게 됩니다.

### 17. 사용자가 지번/도로명 중 어떤 것을 선택하더라도 무조건 지번 주소만 이용하고 싶은데.. 어떻게 해야되나요?
사용자가 선택한 값(userSelectedType)과 상관 없이 로직상 autoJibunAddress변수를 체크하고, 값이 없으면 JibunAddress변수를 이용하시면 됩니다.
지번 주소의 데이터가 셋팅되는 방법에 대해서 추가 설명 드리자면
**(autoMapping을 true로 설정한 경우 - 기본값)**

* 사용자가 도로명-지번 1:N 관계에서 메인 도로명 주소를 선택할 경우, 지번 주소는 autoJibunAddress에 들어가게 됩니다. 또한 연관된 지번 주소를 선택하게 되면 jibunAddress에 들어가게 됩니다.
* 사용자가 도로명-지번 1:1 관계에서 메인 도로명 주소나 연관된 지번주소를 선택하면, 지번 주소는 jibunAddress에 들어가게 됩니다.
* 사용자가 지번-도로명 1:N, 1:1 관계에서 메인 지번주소를 선택하거나 연관된 도로명주소를 선택할 경우, 지번 주소는 address, jibunAddress에 들어가게 됩니다.

### 18. '세종특별자치시', '제주특별자치도'의 축약형이 내려오지 않습니다.
우편번호 서비스는 기본적으로 축약형 형태로 주소정보를 제공(shorthand=true)하고 있으나, 각 지자체의 요청에 따라 해당 기능의 기본 값이 변경될 수 있습니다.
이러한 주소는 shorthand옵션에 영향을 받지 않고 항상 전체 이름으로 내려가게 됩니다.

현재 이와 같은 처리가 된 주소는 아래와 같습니다. 
- 세종특별자치시
- 제주특별자치도
- 강원특별자치도
- 전북특별자치도 (24년 1월 18일 이후)
 
그렇기 때문에, 축약형을 원하는 이용자 분들께서는 oncomplete 콜백 함수내에서 데이터를 받을 시, sido 변수가 위 주소인지를 확인하시어 적절한 값으면 변경하여 사용하시기 바랍니다.
