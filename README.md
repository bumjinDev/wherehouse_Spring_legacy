<img src="https://github.com/user-attachments/assets/f521acdb-4507-4aee-8abd-ac88f80318bb" width="100" height="100"/>| <h1>거주지 추천 서비스 README</h1>|
---| ---|

---

![2](https://github.com/user-attachments/assets/84dc3382-ae6f-4856-a8f0-2a21242319d3)

+ 배포 URL : http://43.202.178.156:8181/wherehouse/


## 프로젝트 소개
---
서울시 1인 MZ 세대의 1인 가구 비율 증가에 따른 거주지 추천 서비스입니다.
+ 거주지 추천은 사용자 선택에 따라 각 구별 안전성 비중, 편의성 비중, 그리고 전세 및 월세 금액 기준으로 주거지 추천 지역구 3곳을 선정하여 제공합니다.
+ 지역구 지도에서는 서울시 내 각 구를 선택하여 해당 구의 전세 또는 월세 정보를 제공하며, 핫플레이스 정보도 함께 제공합니다.
+ 상세 지도 페이지에서는 클릭 이벤트 발생 지점 기준 반경 500m 내의 CCTV 위치를 마커로 표시하고, 가장 가까운 파출소 거리 및 편의 시설 정보를 선택적으로 확인할 수 있습니다.
+ 게시판 기능은 회원들 간 정보 공유를 위해 작성되었습니다.

---

## 팀원 구성

| 정범진 | 이재서 |
| --- | --- |
| <img src="https://github.com/user-attachments/assets/946612ee-7f7f-41ce-8d8c-85b578f18d2d" width="100" height="100" alt="jung"/> | <img src="https://github.com/user-attachments/assets/8b4a2dd0-166a-4e04-93eb-38482a2828fe" width="100" height="100" alt="lee"/> |
| [@bumjinDev](https://github.com/bumjinDev/wherehouse) | [@N0WST4NDUP](https://github.com/N0WST4NDUP) |

---
<br>

## 프로젝트 구조
---
WhereHouse
 ┣ src
 ┃ ┣ main
 ┃ ┃ ┣ java
 ┃ ┃ ┃ ┗ com
 ┃ ┃ ┃ ┃ ┗ wherehouse
 ┃ ┃ ┃ ┃ ┃ ┣ board
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ controller
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ BoardServiceController.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ dao
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ BoardRepository.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ IBoardRepository.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ model
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ BoardVO.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ CommentVO.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┗ service
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ BoardChoiceService.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ BoardDeleteService.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ BoardListService.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ BoardModifyService.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ BoardWriteCommand.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ BoardWriteService.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ IBoardChoiceService.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ IBoardDeleteService.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ IBoardListService.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ IBoardModifyService.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ IBoardWriteCommand.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ IBoardWriteService.java
 ┃ ┃ ┃ ┃ ┃ ┣ information
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ controller
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ InformationController.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ dao
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ AddrRateMapper.xml
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ CctvMapper.xml
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ IAddrRateRepository.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ ICCTVRepository.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ IPoliceOfficeRepository.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ PoliceOfficeMapper.xml
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ model
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ AddrRateVO.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ CctvVO.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ PoliceOfficeVO.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┗ service
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ IInfoService.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ InfoService.java
 ┃ ┃ ┃ ┃ ┃ ┣ mainpage
 ┃ ┃ ┃ ┃ ┃ ┃ ┗ controller
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ PageResponseController.java
 ┃ ┃ ┃ ┃ ┃ ┣ members
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ controller
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ MembersEditController.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ MembersJoinController.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ MembersLoginController.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ dao
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ IMembersRepository.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ MembersRepository.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ model
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ MembersVO.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┗ service
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ IMemberJoinService.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ IMemberLoginService.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ IMemberLogoutService.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ IMembersEditPageService.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ IMembersEditService.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ MemberJoinService.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ MemberLoginService.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ MemberLogoutService.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ MembersEditPageService.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ MembersEditService.java
 ┃ ┃ ┃ ┃ ┃ ┣ recommand
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ controller
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ RecServiceController.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ dao
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ IRecServiceEmpRepository.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ RecServiceEmpRepository.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ model
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ RecServiceVO.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┗ service
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ IRecService.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ RecServiceCharterService.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ RecServiceMonthlyService.java
 ┃ ┃ ┃ ┃ ┃ ┣ HomeController.java
 ┃ ┃ ┃ ┃ ┃ ┗ Test.java
 ┃ ┃ ┣ resources
 ┃ ┃ ┃ ┣ database
 ┃ ┃ ┃ ┃ ┗ jdbc.properties
 ┃ ┃ ┃ ┣ spring
 ┃ ┃ ┃ ┃ ┗ application-config.xml
 ┃ ┃ ┃ ┗ log4j.xml
 ┃ ┃ ┗ webapp
 ┃ ┃ ┃ ┣ META-INF
 ┃ ┃ ┃ ┃ ┣ maven
 ┃ ┃ ┃ ┃ ┃ ┣ com.wherehouse
 ┃ ┃ ┃ ┃ ┃ ┃ ┗ wherehouse
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ pom.properties
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ pom.xml
 ┃ ┃ ┃ ┃ ┃ ┗ e.g
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ com
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ pom.properties
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ pom.xml
 ┃ ┃ ┃ ┃ ┃ ┃ ┗ wherehouse
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ pom.properties
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ pom.xml
 ┃ ┃ ┃ ┃ ┗ MANIFEST.MF
 ┃ ┃ ┃ ┣ resources
 ┃ ┃ ┃ ┃ ┣ css
 ┃ ┃ ┃ ┃ ┃ ┣ bootstrap.css
 ┃ ┃ ┃ ┃ ┃ ┣ comp_modal.css
 ┃ ┃ ┃ ┃ ┃ ┣ contentedit.css
 ┃ ┃ ┃ ┃ ┃ ┣ contentView.css
 ┃ ┃ ┃ ┃ ┃ ┣ description.css
 ┃ ┃ ┃ ┃ ┃ ┣ gu_main_map.css
 ┃ ┃ ┃ ┃ ┃ ┣ gu_map.css
 ┃ ┃ ┃ ┃ ┃ ┣ gu_map_graph.css
 ┃ ┃ ┃ ┃ ┃ ┣ gu_map_info.css
 ┃ ┃ ┃ ┃ ┃ ┣ house_rec.css
 ┃ ┃ ┃ ┃ ┃ ┣ index.css
 ┃ ┃ ┃ ┃ ┃ ┣ information.css
 ┃ ┃ ┃ ┃ ┃ ┣ join.css
 ┃ ┃ ┃ ┃ ┃ ┣ list.css
 ┃ ┃ ┃ ┃ ┃ ┣ listshow.css
 ┃ ┃ ┃ ┃ ┃ ┣ login.css
 ┃ ┃ ┃ ┃ ┃ ┣ main.css
 ┃ ┃ ┃ ┃ ┃ ┣ modify.css
 ┃ ┃ ┃ ┃ ┃ ┣ modifyshow.css
 ┃ ┃ ┃ ┃ ┃ ┣ rec_graph.css
 ┃ ┃ ┃ ┃ ┃ ┣ rec_info.css
 ┃ ┃ ┃ ┃ ┃ ┗ write.css
 ┃ ┃ ┃ ┃ ┣ images
 ┃ ┃ ┃ ┃ ┃ ┣ hotPlace
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 강남구
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img1.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img2.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img3.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ 지역.txt
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 강동구
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img1.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img2.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img3.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ 지역.txt
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 강북구
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img1.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img2.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img3.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ 지역.txt
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 강서구
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img1.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img2.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img3.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ 지역.txt
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 관악구
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img1.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img2.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img3.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ 지역.txt
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 광진구
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img1.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img2.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img3.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ 지역.txt
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 구로구
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img1.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img2.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img3.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ 지역.txt
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 금천구
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img1.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img2.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img3.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ 지역.txt
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 노원구
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img1.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img2.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img3.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ 지역.txt
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 도봉구
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img1.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img2.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img3.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ 지역.txt
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 동대문구
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img1.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img2.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img3.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ 지역.txt
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 동작구
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img1.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img2.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img3.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ 지역.txt
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 마포구
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img1.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img2.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img3.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ 지역.txt
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 서대문구
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img1.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img2.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img3.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ 지역.txt
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 서초구
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img1.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img2.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img3.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ 지역.txt
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 성동구
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img1.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img2.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img3.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ 지역.txt
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 성북구
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img1.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img2.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img3.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ 지역.txt
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 송파구
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img1.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img2.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img3.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ 지역.txt
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 양천구
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img1.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img2.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img3.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ 지역.txt
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 영등포구
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img1.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img2.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img3.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ 지역.txt
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 용산구
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img1.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img2.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img3.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ 지역.txt
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 은평구
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img1.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img2.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img3.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ 지역.txt
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 종로구
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img1.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img2.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img3.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ 지역.txt
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 중구
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img1.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img2.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img3.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ 지역.txt
 ┃ ┃ ┃ ┃ ┃ ┃ ┗ 중랑구
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img1.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img2.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img3.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ 지역.txt
 ┃ ┃ ┃ ┃ ┃ ┣ amenity_icon.png
 ┃ ┃ ┃ ┃ ┃ ┣ board_icon.png
 ┃ ┃ ┃ ┃ ┃ ┣ cctv_icon.png
 ┃ ┃ ┃ ┃ ┃ ┣ city10.jpg
 ┃ ┃ ┃ ┃ ┃ ┣ city11.jpg
 ┃ ┃ ┃ ┃ ┃ ┣ city3.jpg
 ┃ ┃ ┃ ┃ ┃ ┣ city5.jpg
 ┃ ┃ ┃ ┃ ┃ ┣ city6.jpg
 ┃ ┃ ┃ ┃ ┃ ┣ city9.jpg
 ┃ ┃ ┃ ┃ ┃ ┣ closeBtn.svg
 ┃ ┃ ┃ ┃ ┃ ┣ description1.png
 ┃ ┃ ┃ ┃ ┃ ┣ description2.png
 ┃ ┃ ┃ ┃ ┃ ┣ description3.png
 ┃ ┃ ┃ ┃ ┃ ┣ description4.png
 ┃ ┃ ┃ ┃ ┃ ┣ description5.png
 ┃ ┃ ┃ ┃ ┃ ┣ description_sample.png
 ┃ ┃ ┃ ┃ ┃ ┣ detail_icon.png
 ┃ ┃ ┃ ┃ ┃ ┣ detail_icon_preview.png
 ┃ ┃ ┃ ┃ ┃ ┣ gu_icon.png
 ┃ ┃ ┃ ┃ ┃ ┣ gu_icon_preview.png
 ┃ ┃ ┃ ┃ ┃ ┣ home_icon.png
 ┃ ┃ ┃ ┃ ┃ ┣ intro1.png
 ┃ ┃ ┃ ┃ ┃ ┣ intro10.png
 ┃ ┃ ┃ ┃ ┃ ┣ intro11.png
 ┃ ┃ ┃ ┃ ┃ ┣ intro2.png
 ┃ ┃ ┃ ┃ ┃ ┣ intro3.png
 ┃ ┃ ┃ ┃ ┃ ┣ intro4.png
 ┃ ┃ ┃ ┃ ┃ ┣ intro5.png
 ┃ ┃ ┃ ┃ ┃ ┣ intro6.png
 ┃ ┃ ┃ ┃ ┃ ┣ intro7.png
 ┃ ┃ ┃ ┃ ┃ ┣ intro8.png
 ┃ ┃ ┃ ┃ ┃ ┣ intro9.png
 ┃ ┃ ┃ ┃ ┃ ┣ pin_icon.png
 ┃ ┃ ┃ ┃ ┃ ┣ police_office_icon.png
 ┃ ┃ ┃ ┃ ┃ ┣ search_icon.png
 ┃ ┃ ┃ ┃ ┃ ┣ search_icon2.png
 ┃ ┃ ┃ ┃ ┃ ┣ suggest_icon.png
 ┃ ┃ ┃ ┃ ┃ ┗ suggest_icon_preview.png
 ┃ ┃ ┃ ┃ ┣ js
 ┃ ┃ ┃ ┃ ┃ ┣ amenity.js
 ┃ ┃ ┃ ┃ ┃ ┣ boardlist.js
 ┃ ┃ ┃ ┃ ┃ ┣ cctv.js
 ┃ ┃ ┃ ┃ ┃ ┣ circle.js
 ┃ ┃ ┃ ┃ ┃ ┣ contentedit.js
 ┃ ┃ ┃ ┃ ┃ ┣ contentview.js
 ┃ ┃ ┃ ┃ ┃ ┣ description.js
 ┃ ┃ ┃ ┃ ┃ ┣ emoji.js
 ┃ ┃ ┃ ┃ ┃ ┣ getAddress.js
 ┃ ┃ ┃ ┃ ┃ ┣ graph.js
 ┃ ┃ ┃ ┃ ┃ ┣ gu_map.js
 ┃ ┃ ┃ ┃ ┃ ┣ house_rec.js
 ┃ ┃ ┃ ┃ ┃ ┣ index.js
 ┃ ┃ ┃ ┃ ┃ ┣ join.js
 ┃ ┃ ┃ ┃ ┃ ┣ list.js
 ┃ ┃ ┃ ┃ ┃ ┣ main.js
 ┃ ┃ ┃ ┃ ┃ ┣ map.js
 ┃ ┃ ┃ ┃ ┃ ┣ marker.js
 ┃ ┃ ┃ ┃ ┃ ┣ modify.js
 ┃ ┃ ┃ ┃ ┃ ┣ mouseEvent.js
 ┃ ┃ ┃ ┃ ┃ ┣ panel.js
 ┃ ┃ ┃ ┃ ┃ ┣ policeOffice.js
 ┃ ┃ ┃ ┃ ┃ ┣ polygonView.js
 ┃ ┃ ┃ ┃ ┃ ┣ score.js
 ┃ ┃ ┃ ┃ ┃ ┗ writedo.js
 ┃ ┃ ┃ ┃ ┗ json
 ┃ ┃ ┃ ┃ ┃ ┣ arrestRate.json
 ┃ ┃ ┃ ┃ ┃ ┣ density.json
 ┃ ┃ ┃ ┃ ┃ ┣ mapData.json
 ┃ ┃ ┃ ┃ ┃ ┣ policeOffice.geojson
 ┃ ┃ ┃ ┃ ┃ ┗ SeoulCCTV.json
 ┃ ┃ ┃ ┗ WEB-INF
 ┃ ┃ ┃ ┃ ┣ spring
 ┃ ┃ ┃ ┃ ┃ ┗ appServlet
 ┃ ┃ ┃ ┃ ┃ ┃ ┗ servlet-context.xml
 ┃ ┃ ┃ ┃ ┣ views
 ┃ ┃ ┃ ┃ ┃ ┣ board
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ contentedit.jsp
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ contentview.jsp
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ list.jsp
 ┃ ┃ ┃ ┃ ┃ ┃ ┗ writepage.jsp
 ┃ ┃ ┃ ┃ ┃ ┣ information
 ┃ ┃ ┃ ┃ ┃ ┃ ┗ informationPage.jsp
 ┃ ┃ ┃ ┃ ┃ ┣ members
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ join.jsp
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ joinOk.jsp
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ login.jsp
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ loginOk.jsp
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ loginSuccess.jsp
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ logout.jsp
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ modify.jsp
 ┃ ┃ ┃ ┃ ┃ ┃ ┗ modifyOk.jsp
 ┃ ┃ ┃ ┃ ┃ ┣ recommand
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ description.jsp
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ gu_map.jsp
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ house_rec.jsp
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ index.jsp
 ┃ ┃ ┃ ┃ ┃ ┃ ┗ main.jsp
 ┃ ┃ ┃ ┃ ┃ ┗ home.jsp
 ┃ ┃ ┃ ┃ ┗ web.xml
 ┃ ┗ test
 ┃ ┃ ┣ resources
 ┃ ┃ ┃ ┗ log4j.xml
 ┃ ┃ ┗ webapp
 ┃ ┃ ┃ ┣ META-INF
 ┃ ┃ ┃ ┃ ┣ maven
 ┃ ┃ ┃ ┃ ┃ ┗ com.wherehouse
 ┃ ┃ ┃ ┃ ┃ ┃ ┗ wherehouse
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ pom.properties
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ pom.xml
 ┃ ┃ ┃ ┃ ┗ MANIFEST.MF
 ┃ ┃ ┃ ┣ resources
 ┃ ┃ ┃ ┃ ┣ css
 ┃ ┃ ┃ ┃ ┃ ┣ bootstrap.css
 ┃ ┃ ┃ ┃ ┃ ┣ comp_modal.css
 ┃ ┃ ┃ ┃ ┃ ┣ contentedit.css
 ┃ ┃ ┃ ┃ ┃ ┣ contentView.css
 ┃ ┃ ┃ ┃ ┃ ┣ description.css
 ┃ ┃ ┃ ┃ ┃ ┣ gu_main_map.css
 ┃ ┃ ┃ ┃ ┃ ┣ gu_map.css
 ┃ ┃ ┃ ┃ ┃ ┣ gu_map_graph.css
 ┃ ┃ ┃ ┃ ┃ ┣ gu_map_info.css
 ┃ ┃ ┃ ┃ ┃ ┣ house_rec.css
 ┃ ┃ ┃ ┃ ┃ ┣ index.css
 ┃ ┃ ┃ ┃ ┃ ┣ information.css
 ┃ ┃ ┃ ┃ ┃ ┣ join.css
 ┃ ┃ ┃ ┃ ┃ ┣ list.css
 ┃ ┃ ┃ ┃ ┃ ┣ listshow.css
 ┃ ┃ ┃ ┃ ┃ ┣ login.css
 ┃ ┃ ┃ ┃ ┃ ┣ main.css
 ┃ ┃ ┃ ┃ ┃ ┣ modify.css
 ┃ ┃ ┃ ┃ ┃ ┣ modifyshow.css
 ┃ ┃ ┃ ┃ ┃ ┣ rec_graph.css
 ┃ ┃ ┃ ┃ ┃ ┣ rec_info.css
 ┃ ┃ ┃ ┃ ┃ ┗ write.css
 ┃ ┃ ┃ ┃ ┣ images
 ┃ ┃ ┃ ┃ ┃ ┣ hotPlace
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 강남구
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img1.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img2.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img3.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ 지역.txt
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 강동구
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img1.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img2.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img3.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ 지역.txt
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 강북구
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img1.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img2.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img3.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ 지역.txt
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 강서구
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img1.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img2.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img3.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ 지역.txt
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 관악구
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img1.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img2.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img3.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ 지역.txt
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 광진구
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img1.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img2.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img3.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ 지역.txt
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 구로구
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img1.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img2.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img3.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ 지역.txt
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 금천구
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img1.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img2.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img3.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ 지역.txt
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 노원구
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img1.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img2.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img3.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ 지역.txt
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 도봉구
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img1.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img2.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img3.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ 지역.txt
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 동대문구
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img1.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img2.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img3.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ 지역.txt
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 동작구
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img1.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img2.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img3.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ 지역.txt
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 마포구
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img1.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img2.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img3.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ 지역.txt
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 서대문구
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img1.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img2.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img3.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ 지역.txt
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 서초구
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img1.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img2.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img3.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ 지역.txt
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 성동구
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img1.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img2.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img3.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ 지역.txt
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 성북구
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img1.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img2.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img3.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ 지역.txt
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 송파구
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img1.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img2.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img3.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ 지역.txt
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 양천구
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img1.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img2.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img3.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ 지역.txt
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 영등포구
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img1.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img2.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img3.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ 지역.txt
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 용산구
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img1.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img2.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img3.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ 지역.txt
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 은평구
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img1.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img2.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img3.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ 지역.txt
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 종로구
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img1.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img2.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img3.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ 지역.txt
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 중구
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img1.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img2.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img3.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ 지역.txt
 ┃ ┃ ┃ ┃ ┃ ┃ ┗ 중랑구
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img1.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img2.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img3.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ 지역.txt
 ┃ ┃ ┃ ┃ ┃ ┣ amenity_icon.png
 ┃ ┃ ┃ ┃ ┃ ┣ board_icon.png
 ┃ ┃ ┃ ┃ ┃ ┣ cctv_icon.png
 ┃ ┃ ┃ ┃ ┃ ┣ city10.jpg
 ┃ ┃ ┃ ┃ ┃ ┣ city11.jpg
 ┃ ┃ ┃ ┃ ┃ ┣ city3.jpg
 ┃ ┃ ┃ ┃ ┃ ┣ city5.jpg
 ┃ ┃ ┃ ┃ ┃ ┣ city6.jpg
 ┃ ┃ ┃ ┃ ┃ ┣ city9.jpg
 ┃ ┃ ┃ ┃ ┃ ┣ closeBtn.svg
 ┃ ┃ ┃ ┃ ┃ ┣ description1.png
 ┃ ┃ ┃ ┃ ┃ ┣ description2.png
 ┃ ┃ ┃ ┃ ┃ ┣ description3.png
 ┃ ┃ ┃ ┃ ┃ ┣ description4.png
 ┃ ┃ ┃ ┃ ┃ ┣ description5.png
 ┃ ┃ ┃ ┃ ┃ ┣ description_sample.png
 ┃ ┃ ┃ ┃ ┃ ┣ detail_icon.png
 ┃ ┃ ┃ ┃ ┃ ┣ detail_icon_preview.png
 ┃ ┃ ┃ ┃ ┃ ┣ gu_icon.png
 ┃ ┃ ┃ ┃ ┃ ┣ gu_icon_preview.png
 ┃ ┃ ┃ ┃ ┃ ┣ home_icon.png
 ┃ ┃ ┃ ┃ ┃ ┣ intro1.png
 ┃ ┃ ┃ ┃ ┃ ┣ intro10.png
 ┃ ┃ ┃ ┃ ┃ ┣ intro11.png
 ┃ ┃ ┃ ┃ ┃ ┣ intro2.png
 ┃ ┃ ┃ ┃ ┃ ┣ intro3.png
 ┃ ┃ ┃ ┃ ┃ ┣ intro4.png
 ┃ ┃ ┃ ┃ ┃ ┣ intro5.png
 ┃ ┃ ┃ ┃ ┃ ┣ intro6.png
 ┃ ┃ ┃ ┃ ┃ ┣ intro7.png
 ┃ ┃ ┃ ┃ ┃ ┣ intro8.png
 ┃ ┃ ┃ ┃ ┃ ┣ intro9.png
 ┃ ┃ ┃ ┃ ┃ ┣ pin_icon.png
 ┃ ┃ ┃ ┃ ┃ ┣ police_office_icon.png
 ┃ ┃ ┃ ┃ ┃ ┣ search_icon.png
 ┃ ┃ ┃ ┃ ┃ ┣ search_icon2.png
 ┃ ┃ ┃ ┃ ┃ ┣ suggest_icon.png
 ┃ ┃ ┃ ┃ ┃ ┗ suggest_icon_preview.png
 ┃ ┃ ┃ ┃ ┣ js
 ┃ ┃ ┃ ┃ ┃ ┣ amenity.js
 ┃ ┃ ┃ ┃ ┃ ┣ boardlist.js
 ┃ ┃ ┃ ┃ ┃ ┣ cctv.js
 ┃ ┃ ┃ ┃ ┃ ┣ circle.js
 ┃ ┃ ┃ ┃ ┃ ┣ contentedit.js
 ┃ ┃ ┃ ┃ ┃ ┣ contentview.js
 ┃ ┃ ┃ ┃ ┃ ┣ description.js
 ┃ ┃ ┃ ┃ ┃ ┣ emoji.js
 ┃ ┃ ┃ ┃ ┃ ┣ getAddress.js
 ┃ ┃ ┃ ┃ ┃ ┣ graph.js
 ┃ ┃ ┃ ┃ ┃ ┣ gu_map.js
 ┃ ┃ ┃ ┃ ┃ ┣ house_rec.js
 ┃ ┃ ┃ ┃ ┃ ┣ index.js
 ┃ ┃ ┃ ┃ ┃ ┣ join.js
 ┃ ┃ ┃ ┃ ┃ ┣ list.js
 ┃ ┃ ┃ ┃ ┃ ┣ main.js
 ┃ ┃ ┃ ┃ ┃ ┣ map.js
 ┃ ┃ ┃ ┃ ┃ ┣ marker.js
 ┃ ┃ ┃ ┃ ┃ ┣ modify.js
 ┃ ┃ ┃ ┃ ┃ ┣ mouseEvent.js
 ┃ ┃ ┃ ┃ ┃ ┣ panel.js
 ┃ ┃ ┃ ┃ ┃ ┣ policeOffice.js
 ┃ ┃ ┃ ┃ ┃ ┣ polygonView.js
 ┃ ┃ ┃ ┃ ┃ ┣ score.js
 ┃ ┃ ┃ ┃ ┃ ┗ writedo.js
 ┃ ┃ ┃ ┃ ┗ json
 ┃ ┃ ┃ ┃ ┃ ┣ arrestRate.json
 ┃ ┃ ┃ ┃ ┃ ┣ density.json
 ┃ ┃ ┃ ┃ ┃ ┣ mapData.json
 ┃ ┃ ┃ ┃ ┃ ┣ policeOffice.geojson
 ┃ ┃ ┃ ┃ ┃ ┗ SeoulCCTV.json
 ┃ ┃ ┃ ┗ WEB-INF
 ┃ ┃ ┃ ┃ ┣ spring
 ┃ ┃ ┃ ┃ ┃ ┗ appServlet
 ┃ ┃ ┃ ┃ ┃ ┃ ┗ servlet-context.xml
 ┃ ┃ ┃ ┃ ┣ views
 ┃ ┃ ┃ ┃ ┃ ┣ board
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ contentedit.jsp
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ contentview.jsp
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ list.jsp
 ┃ ┃ ┃ ┃ ┃ ┃ ┗ writepage.jsp
 ┃ ┃ ┃ ┃ ┃ ┣ information
 ┃ ┃ ┃ ┃ ┃ ┃ ┗ informationPage.jsp
 ┃ ┃ ┃ ┃ ┃ ┣ members
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ join.jsp
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ joinOk.jsp
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ login.jsp
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ loginOk.jsp
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ loginSuccess.jsp
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ logout.jsp
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ modify.jsp
 ┃ ┃ ┃ ┃ ┃ ┃ ┗ modifyOk.jsp
 ┃ ┃ ┃ ┃ ┃ ┣ recommand
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ description.jsp
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ gu_map.jsp
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ house_rec.jsp
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ index.jsp
 ┃ ┃ ┃ ┃ ┃ ┃ ┗ main.jsp
 ┃ ┃ ┃ ┃ ┃ ┗ home.jsp
 ┃ ┃ ┃ ┃ ┗ web.xml
 ┣ target
 ┃ ┣ classes
 ┃ ┃ ┣ com
 ┃ ┃ ┃ ┗ wherehouse
 ┃ ┃ ┃ ┃ ┗ information
 ┃ ┃ ┃ ┃ ┃ ┗ dao
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ AddrRateMapper.xml
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ CctvMapper.xml
 ┃ ┃ ┃ ┃ ┃ ┃ ┗ PoliceOfficeMapper.xml
 ┃ ┃ ┣ database
 ┃ ┃ ┃ ┗ jdbc.properties
 ┃ ┃ ┣ spring
 ┃ ┃ ┃ ┗ application-config.xml
 ┃ ┃ ┗ log4j.xml
 ┃ ┣ m2e-wtp
 ┃ ┃ ┗ web-resources
 ┃ ┃ ┃ ┗ META-INF
 ┃ ┃ ┃ ┃ ┣ maven
 ┃ ┃ ┃ ┃ ┃ ┗ e.g
 ┃ ┃ ┃ ┃ ┃ ┃ ┗ wherehouse
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ pom.properties
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ pom.xml
 ┃ ┃ ┃ ┃ ┗ MANIFEST.MF
 ┃ ┣ maven-archiver
 ┃ ┃ ┗ pom.properties
 ┃ ┣ test-classes
 ┃ ┃ ┗ log4j.xml
 ┃ ┗ wherehouse-1.0.0-BUILD-SNAPSHOT
 ┃ ┃ ┣ META-INF
 ┃ ┃ ┃ ┣ maven
 ┃ ┃ ┃ ┃ ┣ com.wherehouse
 ┃ ┃ ┃ ┃ ┃ ┗ wherehouse
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ pom.properties
 ┃ ┃ ┃ ┃ ┃ ┃ ┗ pom.xml
 ┃ ┃ ┃ ┃ ┗ e.g
 ┃ ┃ ┃ ┃ ┃ ┣ com
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ pom.properties
 ┃ ┃ ┃ ┃ ┃ ┃ ┗ pom.xml
 ┃ ┃ ┃ ┃ ┃ ┗ wherehouse
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ pom.properties
 ┃ ┃ ┃ ┃ ┃ ┃ ┗ pom.xml
 ┃ ┃ ┃ ┗ MANIFEST.MF
 ┃ ┃ ┣ resources
 ┃ ┃ ┃ ┣ css
 ┃ ┃ ┃ ┃ ┣ bootstrap.css
 ┃ ┃ ┃ ┃ ┣ comp_modal.css
 ┃ ┃ ┃ ┃ ┣ contentedit.css
 ┃ ┃ ┃ ┃ ┣ contentView.css
 ┃ ┃ ┃ ┃ ┣ description.css
 ┃ ┃ ┃ ┃ ┣ gu_main_map.css
 ┃ ┃ ┃ ┃ ┣ gu_map.css
 ┃ ┃ ┃ ┃ ┣ gu_map_graph.css
 ┃ ┃ ┃ ┃ ┣ gu_map_info.css
 ┃ ┃ ┃ ┃ ┣ house_rec.css
 ┃ ┃ ┃ ┃ ┣ index.css
 ┃ ┃ ┃ ┃ ┣ information.css
 ┃ ┃ ┃ ┃ ┣ join.css
 ┃ ┃ ┃ ┃ ┣ list.css
 ┃ ┃ ┃ ┃ ┣ listshow.css
 ┃ ┃ ┃ ┃ ┣ login.css
 ┃ ┃ ┃ ┃ ┣ main.css
 ┃ ┃ ┃ ┃ ┣ modify.css
 ┃ ┃ ┃ ┃ ┣ modifyshow.css
 ┃ ┃ ┃ ┃ ┣ rec_graph.css
 ┃ ┃ ┃ ┃ ┣ rec_info.css
 ┃ ┃ ┃ ┃ ┗ write.css
 ┃ ┃ ┃ ┣ images
 ┃ ┃ ┃ ┃ ┣ hotPlace
 ┃ ┃ ┃ ┃ ┃ ┣ 강남구
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ img1.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ img2.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ img3.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┗ 지역.txt
 ┃ ┃ ┃ ┃ ┃ ┣ 강동구
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ img1.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ img2.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ img3.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┗ 지역.txt
 ┃ ┃ ┃ ┃ ┃ ┣ 강북구
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ img1.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ img2.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ img3.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┗ 지역.txt
 ┃ ┃ ┃ ┃ ┃ ┣ 강서구
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ img1.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ img2.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ img3.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┗ 지역.txt
 ┃ ┃ ┃ ┃ ┃ ┣ 관악구
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ img1.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ img2.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ img3.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┗ 지역.txt
 ┃ ┃ ┃ ┃ ┃ ┣ 광진구
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ img1.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ img2.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ img3.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┗ 지역.txt
 ┃ ┃ ┃ ┃ ┃ ┣ 구로구
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ img1.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ img2.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ img3.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┗ 지역.txt
 ┃ ┃ ┃ ┃ ┃ ┣ 금천구
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ img1.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ img2.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ img3.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┗ 지역.txt
 ┃ ┃ ┃ ┃ ┃ ┣ 노원구
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ img1.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ img2.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ img3.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┗ 지역.txt
 ┃ ┃ ┃ ┃ ┃ ┣ 도봉구
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ img1.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ img2.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ img3.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┗ 지역.txt
 ┃ ┃ ┃ ┃ ┃ ┣ 동대문구
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ img1.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ img2.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ img3.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┗ 지역.txt
 ┃ ┃ ┃ ┃ ┃ ┣ 동작구
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ img1.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ img2.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ img3.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┗ 지역.txt
 ┃ ┃ ┃ ┃ ┃ ┣ 마포구
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ img1.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ img2.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ img3.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┗ 지역.txt
 ┃ ┃ ┃ ┃ ┃ ┣ 서대문구
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ img1.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ img2.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ img3.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┗ 지역.txt
 ┃ ┃ ┃ ┃ ┃ ┣ 서초구
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ img1.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ img2.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ img3.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┗ 지역.txt
 ┃ ┃ ┃ ┃ ┃ ┣ 성동구
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ img1.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ img2.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ img3.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┗ 지역.txt
 ┃ ┃ ┃ ┃ ┃ ┣ 성북구
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ img1.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ img2.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ img3.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┗ 지역.txt
 ┃ ┃ ┃ ┃ ┃ ┣ 송파구
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ img1.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ img2.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ img3.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┗ 지역.txt
 ┃ ┃ ┃ ┃ ┃ ┣ 양천구
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ img1.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ img2.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ img3.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┗ 지역.txt
 ┃ ┃ ┃ ┃ ┃ ┣ 영등포구
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ img1.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ img2.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ img3.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┗ 지역.txt
 ┃ ┃ ┃ ┃ ┃ ┣ 용산구
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ img1.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ img2.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ img3.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┗ 지역.txt
 ┃ ┃ ┃ ┃ ┃ ┣ 은평구
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ img1.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ img2.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ img3.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┗ 지역.txt
 ┃ ┃ ┃ ┃ ┃ ┣ 종로구
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ img1.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ img2.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ img3.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┗ 지역.txt
 ┃ ┃ ┃ ┃ ┃ ┣ 중구
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ img1.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ img2.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ img3.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┗ 지역.txt
 ┃ ┃ ┃ ┃ ┃ ┗ 중랑구
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ img1.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ img2.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ img3.jpg
 ┃ ┃ ┃ ┃ ┃ ┃ ┗ 지역.txt
 ┃ ┃ ┃ ┃ ┣ amenity_icon.png
 ┃ ┃ ┃ ┃ ┣ board_icon.png
 ┃ ┃ ┃ ┃ ┣ cctv_icon.png
 ┃ ┃ ┃ ┃ ┣ city10.jpg
 ┃ ┃ ┃ ┃ ┣ city11.jpg
 ┃ ┃ ┃ ┃ ┣ city3.jpg
 ┃ ┃ ┃ ┃ ┣ city5.jpg
 ┃ ┃ ┃ ┃ ┣ city6.jpg
 ┃ ┃ ┃ ┃ ┣ city9.jpg
 ┃ ┃ ┃ ┃ ┣ closeBtn.svg
 ┃ ┃ ┃ ┃ ┣ description1.png
 ┃ ┃ ┃ ┃ ┣ description2.png
 ┃ ┃ ┃ ┃ ┣ description3.png
 ┃ ┃ ┃ ┃ ┣ description4.png
 ┃ ┃ ┃ ┃ ┣ description5.png
 ┃ ┃ ┃ ┃ ┣ description_sample.png
 ┃ ┃ ┃ ┃ ┣ detail_icon.png
 ┃ ┃ ┃ ┃ ┣ detail_icon_preview.png
 ┃ ┃ ┃ ┃ ┣ gu_icon.png
 ┃ ┃ ┃ ┃ ┣ gu_icon_preview.png
 ┃ ┃ ┃ ┃ ┣ home_icon.png
 ┃ ┃ ┃ ┃ ┣ intro1.png
 ┃ ┃ ┃ ┃ ┣ intro10.png
 ┃ ┃ ┃ ┃ ┣ intro11.png
 ┃ ┃ ┃ ┃ ┣ intro2.png
 ┃ ┃ ┃ ┃ ┣ intro3.png
 ┃ ┃ ┃ ┃ ┣ intro4.png
 ┃ ┃ ┃ ┃ ┣ intro5.png
 ┃ ┃ ┃ ┃ ┣ intro6.png
 ┃ ┃ ┃ ┃ ┣ intro7.png
 ┃ ┃ ┃ ┃ ┣ intro8.png
 ┃ ┃ ┃ ┃ ┣ intro9.png
 ┃ ┃ ┃ ┃ ┣ pin_icon.png
 ┃ ┃ ┃ ┃ ┣ police_office_icon.png
 ┃ ┃ ┃ ┃ ┣ search_icon.png
 ┃ ┃ ┃ ┃ ┣ search_icon2.png
 ┃ ┃ ┃ ┃ ┣ suggest_icon.png
 ┃ ┃ ┃ ┃ ┗ suggest_icon_preview.png
 ┃ ┃ ┃ ┣ js
 ┃ ┃ ┃ ┃ ┣ amenity.js
 ┃ ┃ ┃ ┃ ┣ boardlist.js
 ┃ ┃ ┃ ┃ ┣ cctv.js
 ┃ ┃ ┃ ┃ ┣ circle.js
 ┃ ┃ ┃ ┃ ┣ contentedit.js
 ┃ ┃ ┃ ┃ ┣ contentview.js
 ┃ ┃ ┃ ┃ ┣ description.js
 ┃ ┃ ┃ ┃ ┣ emoji.js
 ┃ ┃ ┃ ┃ ┣ getAddress.js
 ┃ ┃ ┃ ┃ ┣ graph.js
 ┃ ┃ ┃ ┃ ┣ gu_map.js
 ┃ ┃ ┃ ┃ ┣ house_rec.js
 ┃ ┃ ┃ ┃ ┣ index.js
 ┃ ┃ ┃ ┃ ┣ join.js
 ┃ ┃ ┃ ┃ ┣ list.js
 ┃ ┃ ┃ ┃ ┣ main.js
 ┃ ┃ ┃ ┃ ┣ map.js
 ┃ ┃ ┃ ┃ ┣ marker.js
 ┃ ┃ ┃ ┃ ┣ modify.js
 ┃ ┃ ┃ ┃ ┣ mouseEvent.js
 ┃ ┃ ┃ ┃ ┣ panel.js
 ┃ ┃ ┃ ┃ ┣ policeOffice.js
 ┃ ┃ ┃ ┃ ┣ polygonView.js
 ┃ ┃ ┃ ┃ ┣ score.js
 ┃ ┃ ┃ ┃ ┗ writedo.js
 ┃ ┃ ┃ ┗ json
 ┃ ┃ ┃ ┃ ┣ arrestRate.json
 ┃ ┃ ┃ ┃ ┣ density.json
 ┃ ┃ ┃ ┃ ┣ mapData.json
 ┃ ┃ ┃ ┃ ┣ policeOffice.geojson
 ┃ ┃ ┃ ┃ ┗ SeoulCCTV.json
 ┃ ┃ ┗ WEB-INF
 ┃ ┃ ┃ ┣ classes
 ┃ ┃ ┃ ┃ ┣ database
 ┃ ┃ ┃ ┃ ┃ ┗ jdbc.properties
 ┃ ┃ ┃ ┃ ┣ spring
 ┃ ┃ ┃ ┃ ┃ ┗ application-config.xml
 ┃ ┃ ┃ ┃ ┗ log4j.xml
 ┃ ┃ ┃ ┣ spring
 ┃ ┃ ┃ ┃ ┗ appServlet
 ┃ ┃ ┃ ┃ ┃ ┗ servlet-context.xml
 ┃ ┃ ┃ ┣ views
 ┃ ┃ ┃ ┃ ┣ board
 ┃ ┃ ┃ ┃ ┃ ┣ contentedit.jsp
 ┃ ┃ ┃ ┃ ┃ ┣ contentview.jsp
 ┃ ┃ ┃ ┃ ┃ ┣ list.jsp
 ┃ ┃ ┃ ┃ ┃ ┗ writepage.jsp
 ┃ ┃ ┃ ┃ ┣ information
 ┃ ┃ ┃ ┃ ┃ ┗ informationPage.jsp
 ┃ ┃ ┃ ┃ ┣ members
 ┃ ┃ ┃ ┃ ┃ ┣ join.jsp
 ┃ ┃ ┃ ┃ ┃ ┣ joinOk.jsp
 ┃ ┃ ┃ ┃ ┃ ┣ login.jsp
 ┃ ┃ ┃ ┃ ┃ ┣ loginOk.jsp
 ┃ ┃ ┃ ┃ ┃ ┣ loginSuccess.jsp
 ┃ ┃ ┃ ┃ ┃ ┣ logout.jsp
 ┃ ┃ ┃ ┃ ┃ ┣ modify.jsp
 ┃ ┃ ┃ ┃ ┃ ┗ modifyOk.jsp
 ┃ ┃ ┃ ┃ ┣ recommand
 ┃ ┃ ┃ ┃ ┃ ┣ description.jsp
 ┃ ┃ ┃ ┃ ┃ ┣ gu_map.jsp
 ┃ ┃ ┃ ┃ ┃ ┣ house_rec.jsp
 ┃ ┃ ┃ ┃ ┃ ┣ index.jsp
 ┃ ┃ ┃ ┃ ┃ ┗ main.jsp
 ┃ ┃ ┃ ┃ ┗ home.jsp
 ┃ ┃ ┃ ┗ web.xml
 ┣ .classpath
 ┣ .project
 ┗ pom.xml
