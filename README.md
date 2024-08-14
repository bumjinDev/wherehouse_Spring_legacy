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
WhereHouse<br>
┣ src<br>
┃ ┣ main<br>
┃ ┃ ┣ java<br>
┃ ┃ ┃ ┗ com<br>
┃ ┃ ┃ ┃ ┗ wherehouse<br>
┃ ┃ ┃ ┃ ┃ ┣ board<br>
┃ ┃ ┃ ┃ ┃ ┃ ┣ controller<br>
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ BoardServiceController.java<br>
┃ ┃ ┃ ┃ ┃ ┃ ┣ dao<br>
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ BoardRepository.java<br>
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ IBoardRepository.java<br>
┃ ┃ ┃ ┃ ┃ ┃ ┣ model<br>
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ BoardVO.java<br>
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ CommentVO.java<br>
┃ ┃ ┃ ┃ ┃ ┃ ┗ service<br>
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ BoardChoiceService.java<br>
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ BoardDeleteService.java<br>
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣    .<br>
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣    .<br>
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣    .<br>
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ IBoardWriteService.java<br>
┃ ┃ ┃ ┃ ┃ ┣ information<br>
┃ ┃ ┃ ┃ ┃ ┃ ┣ controller<br>
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ InformationController.java<br>
┃ ┃ ┃ ┃ ┃ ┃ ┣ dao<br>
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ AddrRateMapper.xml<br>
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ CctvMapper.xml<br>
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ IAddrRateRepository.java<br>
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ ICCTVRepository.java<br>
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ IPoliceOfficeRepository.java<br>
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ PoliceOfficeMapper.xml<br>
┃ ┃ ┃ ┃ ┃ ┃ ┣ model<br>
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ AddrRateVO.java<br>
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ CctvVO.java<br>
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ PoliceOfficeVO.java<br>
┃ ┃ ┃ ┃ ┃ ┃ ┗ service<br>
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ IInfoService.java<br>
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ InfoService.java<br>
┃ ┃ ┃ ┃ ┃ ┣ mainpage<br>
┃ ┃ ┃ ┃ ┃ ┃ ┗ controller<br>
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ PageResponseController.java<br>
┃ ┃ ┃ ┃ ┃ ┣ members<br>
┃ ┃ ┃ ┃ ┃ ┃ ┣ controller<br>
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ MembersEditController.java<br>
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ MembersJoinController.java<br>
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ MembersLoginController.java<br>
┃ ┃ ┃ ┃ ┃ ┃ ┣ dao<br>
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ IMembersRepository.java<br>
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ MembersRepository.java<br>
┃ ┃ ┃ ┃ ┃ ┃ ┣ model<br>
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ MembersVO.java<br>
┃ ┃ ┃ ┃ ┃ ┃ ┗ service<br>
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ IMemberJoinService.java<br>
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ IMemberLoginService.java<br>
┃ ┃ ┃ ┃ ┃ ┃ ┣ IMemberLogoutService.java<br>
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ IMembersEditPageService.java<br>
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ IMembersEditService.java<br>
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ MemberJoinService.java<br>
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ MemberLoginService.java<br>
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ MemberLogoutService.java<br>
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ MembersEditPageService.java<br>
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ MembersEditService.java<br>
┃ ┃ ┃ ┃ ┃ ┣ recommand<br>
┃ ┃ ┃ ┃ ┃ ┃ ┣ controller<br>
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ RecServiceController.java<br>
┃ ┃ ┃ ┃ ┃ ┃ ┣ dao<br>
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ IRecServiceEmpRepository.java<br>
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ RecServiceEmpRepository.java<br>
┃ ┃ ┃ ┃ ┃ ┃ ┣ model<br>
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ RecServiceVO.java<br>
┃ ┃ ┃ ┃ ┃ ┃ ┗ service<br>
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ IRecService.java<br>
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ RecServiceCharterService.java<br>
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ RecServiceMonthlyService.java<br>
┃ ┃ ┃ ┃ ┃ ┣ HomeController.java<br>
┃ ┃ ┃ ┃ ┃ ┗ Test.java<br>
┃ ┃ ┣ resources<br>
┃ ┃ ┃ ┣ database<br>
┃ ┃ ┃ ┃ ┗ jdbc.properties<br>
┃ ┃ ┃ ┣ spring<br>
┃ ┃ ┃ ┃ ┗ application-config.xml<br>
┃ ┃ ┃ ┗ log4j.xml<br>
┃ ┃ ┗ webapp<br>
┃ ┃ ┃ ┣ META-INF<br>
┃ ┃ ┃ ┃ ┣ maven<br>
┃ ┃ ┃ ┃ ┣ com.wherehouse<br>
┃ ┃ ┃ ┃ ┃ ┃ ┗ wherehouse<br>
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ pom.properties<br>
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ pom.xml<br>
┃ ┃ ┃ ┃ ┃ ┗ e.g<br>
┃ ┃ ┃ ┃ ┃ ┃ ┣ com<br>
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ pom.properties<br>
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ pom.xml<br>
┃ ┃ ┃ ┃ ┃ ┃ ┗ wherehouse<br>
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ pom.properties<br>
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ pom.xml<br>
┃ ┃ ┃ ┃ ┗ MANIFEST.MF<br>
┃ ┃ ┃ ┣ resources<br>
┃ ┃ ┃ ┃ ┣ css<br>
┃ ┃ ┃ ┃ ┃ ┣ bootstrap.css<br>
┃ ┃ ┃ ┃ ┃ ┣ comp_modal.css<br>
┃ ┃ ┃ ┃ ┃ ┣    .<br>
┃ ┃ ┃ ┃ ┣    .<br>
┃ ┃ ┃ ┃ ┃ ┣    .<br>
┃ ┃ ┃ ┃ ┃ ┗ write.css<br>
┃ ┃ ┃ ┃ ┣ images<br>
┃ ┃ ┃ ┃ ┃ ┣ hotPlace<br>
┃ ┃ ┃ ┃ ┃ ┃ ┣ 강남구<br>
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img1.jpg<br>
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img2.jpg<br>
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img3.jpg<br>
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ 지역.txt<br>
┃ ┃ ┃ ┃ ┃ ┃ ┃   .<br>
┃ ┃ ┃ ┃ ┃ ┃ ┃   .<br>
┃ ┃ ┃ ┃ ┃ ┃ ┃   .<br>
┃ ┃ ┃ ┃ ┃ ┃ ┗ 중랑구<br>
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ img1.jpg<br>
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img2.jpg<br>
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img3.jpg<br>
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ 지역.txt<br><br>
┃ ┃ ┃ ┃ ┃ ┣ amenity_icon.png<br>
┃ ┃ ┃ ┃ ┃ ┣ board_icon.png<br>
┃ ┃ ┃ ┃ ┃ ┣    .<br>
┃ ┃ ┃ ┃ ┃ ┣    .<br>
┃ ┃ ┃ ┃ ┃ ┣    .<br>
┃ ┃ ┃ ┃ ┃ ┗ suggest_icon_preview.png<br>
┃ ┃ ┃ ┣ js<br>
┃ ┃ ┃ ┃ ┃ ┣ amenity.js<br>
┃ ┃ ┃ ┃ ┃ ┣ boardlist.js<br>
┃ ┃ ┃ ┃ ┃ ┣ cctv.js<br>
┃ ┃ ┃ ┃ ┃ ┣    .<br>
┃ ┃ ┃ ┃ ┃ ┣    .<br>
┃ ┃ ┃ ┃ ┃ ┣    .<br>
┃ ┃ ┃ ┃ ┃ ┗ writedo.js<br>
┃ ┃ ┃ ┃ ┗ json<br>
┃ ┃ ┃ ┃ ┃ ┣ arrestRate.json<br>
┃ ┃ ┃ ┃ ┃ ┣ density.json<br>
┃ ┃ ┃ ┃ ┃ ┣ mapData.json<br>
┃ ┃ ┃ ┃ ┃ ┣ policeOffice.geojson<br>
┃ ┃ ┃ ┃ ┃ ┗ SeoulCCTV.json<br>
┃ ┃ ┗ WEB-INF<br>
┃ ┃ ┃ ┃ ┣ spring<br>
┃ ┃ ┃ ┃ ┃ ┗ appServlet<br>
┃ ┃ ┃ ┃ ┃ ┃ ┗ servlet-context.xml<br>
┃ ┃ ┃ ┃ ┣ views<br>
┃ ┃ ┃ ┃ ┃ ┣ board<br>
┃ ┃ ┃ ┃ ┃ ┃ ┣ contentedit.jsp<br>
┃ ┃ ┃ ┃ ┃ ┃ ┣ contentview.jsp<br>
┃ ┃ ┃ ┃ ┃ ┃ ┣ list.jsp<br>
┃ ┃ ┃ ┃ ┃ ┃ ┗ writepage.jsp<br>
┃ ┃ ┃ ┃ ┃ ┣   .<br>
┃ ┃ ┃ ┃ ┃ ┣   .<br>
┃ ┃ ┃ ┃ ┃ ┣   .<br>
┃ ┃ ┃ ┃ ┗ web.xml<br>
┃ ┗ test<br>
┃ ┃ ┣ resources<br>
┃ ┃ ┗ log4j.xml<br>
┃ ┃ ┗ webapp<br>
┃ ┃ ┃ ┣ META-INF<br>
┃ ┃ ┃ ┃ ┣ maven<br>
┃ ┃ ┃ ┃ ┃ ┗ com.wherehouse<br>
┃ ┃ ┃ ┃ ┃ ┃ ┗ wherehouse<br>
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ pom.properties<br>
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ pom.xml<br>
┃ ┃ ┃ ┃ ┗ MANIFEST.MF<br>
┃ ┃ ┣ resources<br>
┃ ┃ ┃ ┃ ┣ css<br>
┃ ┃ ┃ ┃ ┃ ┣ bootstrap.css<br>
┃ ┃ ┃ ┃ ┃ ┣ comp_modal.css<br>
┃ ┃ ┃ ┃ ┃ ┣    .<br>
┃ ┃ ┃ ┃ ┃ ┣    .<br>
┃ ┃ ┃ ┃ ┃ ┣    .<br>
┃ ┃ ┃ ┃ ┃ ┗ write.css<br>
┃ ┃ ┃ ┃ ┣ images<br>
┃ ┃ ┃ ┃ ┃ ┣ hotPlace<br>
┃ ┃ ┃ ┃ ┃ ┃ ┣ 강남구<br>
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img1.jpg<br>
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img2.jpg<br>
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img3.jpg<br>
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ 지역.txt<br>
┃ ┃ ┃ ┃ ┃ ┃    .<br>
┃ ┃ ┃ ┃ ┃ ┃ ┃    .<br>
┃ ┃ ┃ ┃ ┃ ┃ ┃    .<br>
┃ ┃ ┃ ┃ ┃ ┃ ┗ 중랑구<br>
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img1.jpg<br>
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img2.jpg<br>
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ img3.jpg<br>
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ 지역.txt<br>
┃ ┃ ┃ ┃ ┃ ┣ amenity_icon.png<br>
┃ ┃ ┃ ┃ ┣ board_icon.png<br>
┃ ┃ ┃ ┃ ┃ ┣    .<br>
┃ ┃ ┃ ┃ ┃ ┣    .<br>
┃ ┃ ┃ ┃ ┃ ┣    .<br>
┃ ┃ ┃ ┃ ┃ ┗ suggest_icon_preview.png<br>
┃ ┃ ┃ ┃ ┣ js<br>
┃ ┃ ┃ ┃ ┃ ┣ amenity.js<br>
┃ ┃ ┃ ┃ ┃ ┣ boardlist.js<br>
┃ ┃ ┃ ┃ ┃ ┣    .<br>
┃ ┃ ┃ ┃ ┃ ┣    .<br>
┃ ┃ ┃ ┃ ┃ ┣    .<br>
┃ ┃ ┃ ┃ ┃ ┣ score.js<br>
┃ ┃ ┃ ┃ ┃ ┗ writedo.js<br>
┃ ┃ ┃ ┃ ┗ json<br>
┃ ┃ ┃ ┃ ┣ arrestRate.json<br>
┃ ┃ ┃ ┃ ┃ ┣ density.json<br>
┃ ┃ ┃ ┃ ┃ ┣ mapData.json<br>
┃ ┃ ┃ ┃ ┃ ┣ policeOffice.geojson<br>
┃ ┃ ┃ ┃ ┃ ┗ SeoulCCTV.json<br>
┃ ┃ ┃ ┗ WEB-INF<br>
┃ ┃ ┃ ┃ ┣ spring<br>
┃ ┃ ┃ ┃ ┃ ┗ appServlet<br>
┃ ┃ ┃ ┃ ┃ ┃ ┗ servlet-context.xml<br>
┃ ┃ ┃ ┣ views<br>
┃ ┃ ┃ ┃ ┃ ┣ board<br>
┃ ┃ ┃ ┃ ┃ ┃ ┣ contentedit.jsp<br>
┃ ┃ ┃ ┃ ┃ ┃ ┣ contentview.jsp<br>
┃ ┃ ┃ ┃ ┃ ┃ ┣ list.jsp<br>
┃ ┃ ┃ ┃ ┃ ┃ ┗ writepage.jsp<br>
┃ ┃ ┃ ┃ ┣    . <br>
┃ ┃ ┃ ┃ ┣    . <br>
┃ ┃ ┃ ┣    . <br>
┃ ┃ ┃ ┃ ┃ ┣ recommand<br>
┃ ┃ ┃ ┃ ┃ ┃ ┣ description.jsp<br>
┃ ┃ ┃ ┃ ┃ ┃ ┣ gu_map.jsp<br>
┃ ┃ ┃ ┃ ┃ ┃ ┣ house_rec.jsp<br>
┃ ┃ ┃ ┃ ┃ ┃ ┣ index.jsp<br>
┃ ┃ ┃ ┃ ┃ ┃ ┗ main.jsp<br>
┃ ┃ ┃ ┃ ┃ ┗ home.jsp<br>
┃ ┃ ┃ ┃ ┗ web.xml<br>
┣ target<br>
┃ ┣ classes<br>
┃ ┃ ┣ com<br>
┃ ┃ ┃ ┗ wherehouse<br>
┃ ┃ ┃ ┃ ┗ information<br>
┃ ┃ ┃ ┃ ┗ dao<br>
┃ ┃ ┃ ┃ ┃ ┃ ┣ AddrRateMapper.xml<br>
┃ ┃ ┃ ┃ ┃ ┃ ┣ CctvMapper.xml<br>
┃ ┃ ┃ ┃ ┃ ┃ ┗ PoliceOfficeMapper.xml<br>
┃ ┃ ┣ database<br>
┃ ┃ ┃ ┗ jdbc.properties<br>
┃ ┃ ┣ spring<br>
┃ ┃ ┃ ┗ application-config.xml<br>
┃ ┃ ┗ log4j.xml<br>
┃ ┣ m2e-wtp<br>
┃ ┗ web-resources<br>
┃ ┃ ┃ ┗ META-INF<br>
┃ ┃ ┃ ┃ ┣ maven<br>
┃ ┃ ┃ ┃ ┃ ┗ e.g<br>
┃ ┃ ┃ ┃ ┃ ┃ ┗ wherehouse<br>
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ pom.properties<br>
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ pom.xml<br>
┃ ┃ ┃ ┃ ┗ MANIFEST.MF<br>
┃ ┣ maven-archiver<br>
┃ ┃ ┗ pom.properties<br>
┃ ┣ test-classes<br>
┃ ┃ ┗ log4j.xml<br>
┗ wherehouse-1.0.0-BUILD-SNAPSHOT<br>
┃ ┃ ┣ META-INF
┃ ┃ ┃ ┣ maven<br>
┃ ┃ ┃ ┃ ┣ com.wherehouse<br>
┃ ┃ ┃ ┃ ┃ ┗ wherehouse<br>
┃ ┃ ┃ ┃ ┃ ┃ ┣ pom.properties<br>
┃ ┃ ┃ ┃ ┃ ┃ ┗ pom.xml<br>
┃ ┃ ┃ ┃ ┗ e.g<br>
┃ ┃ ┃ ┃ ┃ ┣ com<br>
┃ ┃ ┃ ┃ ┃ ┃ ┣ pom.properties<br>
┃ ┃ ┃ ┃ ┃ ┃ ┗ pom.xml<br>
┃ ┃ ┃ ┃ ┃ ┗ wherehouse<br>
┃ ┃ ┃ ┃ ┃ ┣ pom.properties<br>
┃ ┃ ┃ ┃ ┃ ┃ ┗ pom.xml<br>
┃ ┃ ┃ ┗ MANIFEST.MF<br>
┃ ┃ ┣ resources<br>
┃ ┃ ┃ ┣ css<br>
┃ ┃ ┃ ┃ ┣ bootstrap.css<br>
┃ ┃ ┃ ┃ ┣ comp_modal.css<br>
┃ ┃ ┃ ┃ ┣    .<br>
┃ ┃ ┃ ┃ ┣    .<br>
┃ ┃ ┃ ┣    .<br>
┃ ┃ ┃ ┃ ┣ rec_info.css<br>
┃ ┃ ┃ ┃ ┗ write.css<br>
┃ ┃ ┃ ┣ images<br>
┃ ┃ ┃ ┣ hotPlace<br>
┃ ┃ ┃ ┃ ┃ ┣ 강남구<br>
┃ ┃ ┃ ┃ ┃ ┃ ┣ img1.jpg<br>
┃ ┃ ┃ ┃ ┃ ┃ ┣ img2.jpg<br>
┃ ┃ ┃ ┃ ┃ ┃ ┣ img3.jpg<br>
┃ ┃ ┃ ┃ ┃ ┃ ┗ 지역.txt<br>
┃ ┃ ┃ ┃ ┣ 강동구<br>
┃ ┃ ┃ ┃ ┃ ┣    .<br>
┃ ┃ ┃ ┃ ┃ ┣    .<br>
┃ ┃ ┃ ┃ ┃ ┣    .<br>
┃ ┃ ┃ ┃ ┃ ┗ 중랑구<br>
┃ ┃ ┃ ┃ ┃ ┃ ┣ img1.jpg<br>
┃ ┃ ┃ ┃ ┃ ┣ img2.jpg<br>
┃ ┃ ┃ ┃ ┃ ┃ ┣ img3.jpg<br>
┃ ┃ ┃ ┃ ┃ ┃ ┗ 지역.txt<br>
┃ ┃ ┃ ┃ ┣ amenity_icon.png<br>
┃ ┃ ┃ ┃ ┣ board_icon.png<br>
┃ ┃ ┃ ┃ ┣     .<br>
┃ ┃ ┃ ┃ ┣     .<br>
┃ ┃ ┃ ┣     .<br>
┃ ┃ ┃ ┃ ┗ suggest_icon_preview.png<br>
┃ ┃ ┃ ┣ js<br>
┃ ┃ ┃ ┃ ┣ amenity.js<br>
┃ ┃ ┃ ┃ ┣ boardlist.js<br>
┃ ┃ ┃ ┃ ┣     .<br>
┃ ┃ ┃ ┃ ┣     . <br>
┃ ┃ ┃ ┣     .<br>
┃ ┃ ┃ ┃ ┣ score.js<br>
┃ ┃ ┃ ┃ ┗ writedo.js<br>
┃ ┃ ┃ ┗ json<br>
┃ ┃ ┃ ┃ ┣ arrestRate.json<br>
┃ ┃ ┃ ┃ ┣ density.json<br>
┃ ┃ ┃ ┣ mapData.json<br>
┃ ┃ ┃ ┃ ┣ policeOffice.geojson<br>
┃ ┃ ┃ ┃ ┗ SeoulCCTV.json<br>
┃ ┃ ┗ WEB-INF<br>
┃ ┃ ┃ ┣ classes<br>
┃ ┃ ┃ ┃ ┣ database<br>
┃ ┃ ┃ ┃ ┃ ┗ jdbc.properties<br>
┃ ┃ ┃ ┃ ┣ spring<br>
┃ ┃ ┃ ┃ ┗ application-config.xml<br>
┃ ┃ ┃ ┃ ┗ log4j.xml<br>
┃ ┃ ┃ ┣ spring<br>
┃ ┃ ┃ ┃ ┗ appServlet<br>
┃ ┃ ┃ ┃ ┃ ┗ servlet-context.xml<br>
┃ ┃ ┃ ┣ views<br>
┃ ┃ ┃ ┃ ┣ board<br>
┃ ┃ ┃ ┃ ┣ contentedit.jsp<br>
┃ ┃ ┃ ┃ ┃ ┣ contentview.jsp<br>
┃ ┃ ┃ ┃ ┃ ┣ list.jsp<br>
┃ ┃ ┃ ┃ ┃ ┗ writepage.jsp<br>
┃ ┃ ┃ ┃ ┃ ┗    .<br>
┃ ┃ ┃ ┃ ┃ ┗    .<br>
┃ ┃ ┃ ┃ ┃ ┗    .<br>
┃ ┃ ┃ ┃ ┣ recommand<br>
┃ ┃ ┃ ┃ ┣ description.jsp<br>
┃ ┃ ┃ ┃ ┃ ┣ gu_map.jsp<br>
┃ ┃ ┃ ┃ ┃ ┣ house_rec.jsp<br>
┃ ┃ ┃ ┃ ┃ ┣ index.jsp<br>
┃ ┃ ┃ ┃ ┃ ┗ main.jsp<br>
┃ ┃ ┃ ┃ ┗ home.jsp<br>
┃ ┃ ┃ ┗ web.xml<br>
┣ .classpath<br>
┣ .project<br>
┗ pom.xml<br>
