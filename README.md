# 유수연 포트폴리오


</br>

## :pushpin: Intro
- Front-end 개발자를 희망합니다

</br>

## :pushpin: Contact
- 이메일: yusuyeon443@gmail.com
- 깃헙: https://github.com/yusuyeon1111

</br>

## :pushpin: Projects

---

### 1. [실전 프로젝트](https://github.com/2023-SMHRD-IS-CLOUD-1/Letmein-front)
#### [백엔드](https://github.com/2023-SMHRD-IS-CLOUD-1/Letmein.git)

> Letmein (팀 프로젝트) 
>개발 기간: 2024.2.1 ~ 2024.2.27 (개발중)  
> Front-end + Back-end
> 
> 프로젝트 설명
> 
> - YOLO기반 체형확인 및 패션 스타일러 입니다
> - 커뮤니티에 코디 사진을 업로드 할 수 있습니다!
> - 체형 사진을 업로드해 체형 기반 아바타를 생성해 코디를 해볼 수 있습니다!
> - 사진대신 사이즈를 입력한 아바타 생성도 가능합니다! 
<div align="center">
	<P>기술스택</P>
	<img src="https://img.shields.io/badge/react-61DAFB?style=for-the-badge&logo=react&logoColor=white">
	<img src="https://img.shields.io/badge/springboot-6DB33F?style=for-the-badge&logo=springboot&logoColor=white" />
	<img src="https://img.shields.io/badge/oracle-F80000?style=for-the-badge&logo=oracle&logoColor=white" />
	<img src="https://img.shields.io/badge/apachetomcat-F8DC75?style=for-the-badge&logo=apachetomcat&logoColor=black"/>
	<img src="https://img.shields.io/badge/flask-000000?style=for-the-badge&logo=flask&logoColor=white"/>
	<img src="https://img.shields.io/badge/amazons3-569A31?style=for-the-badge&logo=amazons3&logoColor=white"/>
</div>
>  
>[프로젝트 상세 설명]

### 2. [핵심 프로젝트](https://github.com/2023-SMHRD-IS-CLOUD-1/1stProject.git)
>HEF  (팀 프로젝트)  
>개발 기간: 2023.11.22 ~ 2023.12.8
>
> Front-end + Back-end
>
>프로젝트 설명
> - 게시판 기반 심부름 매칭 서비스 입니다!<br/>
> - OCR로 신분증 인증이 가능합니다!<br/>
> - 커뮤니티로 소통할 수 있습니다!<br/>
<div align="center">
	<P>기술스택 </P>
	<img src="https://img.shields.io/badge/Java-007396?style=for-the-badge&logo=Java&logoColor=white" />
	<img src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=HTML5&logoColor=white" />
	<img src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=CSS3&logoColor=white" />
	<img src="https://img.shields.io/badge/oracle-F80000?style=for-the-badge&logo=oracle&logoColor=white"/>
	<img src="https://img.shields.io/badge/javascript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=white"/>
</div>


<details>
<summary><b>핵심 기능 설명 펼치기</b></summary>
 <div markdown="1>
	 
 #### 1. 전체 흐름
![image](https://github.com/yusuyeon1111/sample/assets/142488306/fb8c738f-39f2-4bde-8ffb-b62c8f893d55)
1. 의뢰인이 심부름 의뢰글을 작성합니다
2. 의뢰글을 수행인이 심부름 페이지에서 검색해서 조회할 수 있습니다.
3. 수행인이 의뢰글에 수행 신청을 하게되면
4. 의뢰인의 수행인 신청 목록 확인 서비스에서 수행인의 프로필을 확인할 수 있습니다
5. 의뢰인은 수행인의 신청 목록을 확인해 신청을 수락할 수 있고 거절할 수 있습니다.
6. 신청을 수락하게 되면 심부름은 매칭되고 매칭 여부가 데이터베이스 상에서 변화됩니다.

#### 2. 심부름 페이지

![image](https://github.com/yusuyeon1111/sample/assets/142488306/e5cb9e68-77ad-4374-ba8d-b40cda984f70)

<br/>
 1. 카테고리 : 카테고리 필터링 시스템을 구현해 카테고리에 따라 확인 가능
   
[🔍](https://github.com/2023-SMHRD-IS-CLOUD-1/1stProject/blob/c01013df001193fbb4c00e65eb206ceccf58d18b/FirstProject_Whip/src/main/java/com/smhrd/controller/Err_readService.java#L18)
<br/>
 2. 검색창 : 검색 기능을 통해 사용자가 원하는 심부름 신청글을 제목과 작성자를 기준으로 검색 가능<br/>
   
[🔍](https://github.com/2023-SMHRD-IS-CLOUD-1/1stProject/blob/c01013df001193fbb4c00e65eb206ceccf58d18b/FirstProject_Whip/src/main/java/com/smhrd/controller/Err_searchService.java#L18)
   <br/>

3. 심부름 요청 글 작성 페이지로 이동


4. 심부름 글의 상세 내용을 확인할 수 있는 기능, 다른 사용자가 열람 가능.

[🔍글 상세보기](https://github.com/2023-SMHRD-IS-CLOUD-1/1stProject/blob/c01013df001193fbb4c00e65eb206ceccf58d18b/FirstProject_Whip/src/main/java/com/smhrd/controller/Err_detailService.java#L18)<br/>
[🔍글 수정](https://github.com/2023-SMHRD-IS-CLOUD-1/1stProject/blob/c01013df001193fbb4c00e65eb206ceccf58d18b/FirstProject_Whip/src/main/java/com/smhrd/controller/ErrmodifyService.java#L15)
<br/>
[🔍글 삭제](https://github.com/2023-SMHRD-IS-CLOUD-1/1stProject/blob/c01013df001193fbb4c00e65eb206ceccf58d18b/FirstProject_Whip/src/main/java/com/smhrd/controller/ErrdeleteService.java#L15)
<br/>
 5. 신청 버튼 클릭시 신청되며 신청인의 수행인 신청 목록 확인 서비스에서 확인 가능
   
[🔍](https://github.com/2023-SMHRD-IS-CLOUD-1/1stProject/blob/c01013df001193fbb4c00e65eb206ceccf58d18b/FirstProject_Whip/src/main/java/com/smhrd/controller/Err_matchService.java#L20)
<br/>
#### 3. 고객센터 페이지

![image](https://github.com/yusuyeon1111/sample/assets/142488306/3e7a3b69-9e93-411c-904e-1df81ba40895)

1)  검색창 : 검색 기능을 통해 사용자가 원하는 문의글을 제목과 작성자를 기준으로 검색 가능
    <br/>
[🔍](https://github.com/2023-SMHRD-IS-CLOUD-1/1stProject/blob/c01013df001193fbb4c00e65eb206ceccf58d18b/FirstProject_Whip/src/main/java/com/smhrd/controller/Man_searchService.java#L21)
<br/>   

2) 문의글 작성 페이지로 이동

[🔍](https://github.com/2023-SMHRD-IS-CLOUD-1/1stProject/blob/c01013df001193fbb4c00e65eb206ceccf58d18b/FirstProject_Whip/src/main/java/com/smhrd/controller/ManagePostService.java#L15)
 
3) 문의글 상세 내용을 확인할 수 있는 기능

[🔍](https://github.com/2023-SMHRD-IS-CLOUD-1/1stProject/blob/c01013df001193fbb4c00e65eb206ceccf58d18b/FirstProject_Whip/src/main/java/com/smhrd/controller/Manage_detailService.java#L21)
   <br/>
   
4) 관리자 답변여부 확인 가능<br/>

5) 관리자 계정을 생성해, 관리자 계정으로 로그인 시, 고객센터 문의글에 답변할 수 있는 기능

[🔍](https://github.com/2023-SMHRD-IS-CLOUD-1/1stProject/blob/c01013df001193fbb4c00e65eb206ceccf58d18b/FirstProject_Whip/src/main/java/com/smhrd/controller/Manage_answerService.java#L16)    
---

