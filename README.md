# 유수연 포트폴리오
성장을 추구하는 인재 유수연입니다.

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

## 1. [실전 프로젝트](https://github.com/2023-SMHRD-IS-CLOUD-1/Letmein-front)
### [백엔드](https://github.com/2023-SMHRD-IS-CLOUD-1/Letmein.git)

> Letmein (팀 프로젝트) 
>개발 기간: 2024.2.1 ~ 2024.2.27 
> 
> Front-end + Back-end
> 
> 프로젝트 기여도 50%
> 
> 팀원 3명 (PM, 모델링, Front-end+Back-end)
> 
### 1. 프로젝트 설명
> 
> - YOLO기반 체형확인 및 패션 스타일러 입니다
> - 커뮤니티에 코디 사진을 업로드 할 수 있습니다!
> - 체형 사진을 업로드해 체형 기반 아바타를 생성해 코디를 해볼 수 있습니다!
> - 사진대신 사이즈를 입력한 아바타 생성도 가능합니다!
>
### 2. 구현내용
>  - aws s3 이미지 업로드 기능
>  - spring boot security를 활용한 비밀번호 암호화 구현
>  - 메인페이지 제작
>  - 커뮤티니 페이지 제작 & 모든 기능 구현
>  - 체형 분석 페이지 제작 & 모든 기능 구현
>  - 고객 센터 페이지 제작 & 모든 기능 구현
>  - 마이페이지 제작 & 기능 구현
>  - 관리자 페이지 제작 & 모든 기능 구현
>  - EC2 활용한 Spring Boot, react 배포
> 
<div align="center">
	<P>기술스택</P>
	<img src="https://img.shields.io/badge/react-61DAFB?style=for-the-badge&logo=react&logoColor=white">
	<img src="https://img.shields.io/badge/springboot-6DB33F?style=for-the-badge&logo=springboot&logoColor=white" />
	<img src="https://img.shields.io/badge/oracle-F80000?style=for-the-badge&logo=oracle&logoColor=white" />
	<img src="https://img.shields.io/badge/apachetomcat-F8DC75?style=for-the-badge&logo=apachetomcat&logoColor=black"/>
	<img src="https://img.shields.io/badge/flask-000000?style=for-the-badge&logo=flask&logoColor=white"/>
	<img src="https://img.shields.io/badge/amazons3-569A31?style=for-the-badge&logo=amazons3&logoColor=white"/>
</div>
 <br/>
 <br/>

### 3. 핵심 화면

<details>
    <summary>화면구성 보기</summary>
<!-- summary 아래 한칸 공백 두고 내용 삽입 -->
   
   #### 7-1 메인 페이지
   ![제목 없는 동영상 - Clipchamp로 제작](https://github.com/yusuyeon1111/portfolio/assets/142488306/e94a754c-fa5c-4b7a-b925-be1531f704f0)

   #### 7-2 회원가입 & 로그인 페이지
   ![제목 없는 동영상 - Clipchamp로 제작](https://github.com/yusuyeon1111/portfolio/assets/142488306/f06b7c39-26ac-47eb-af1f-bc2d8ed32edc)
   
   #### 7-3 커뮤니티 페이지
 ![-Clipchamp3-ezgif com-video-to-gif-converter](https://github.com/yusuyeon1111/portfolio/assets/142488306/b5dfbf08-3f8d-4344-bc32-18f00510663f)
 
   #### 7-4 마이페이지 & 고객센터 페이지
![-Clipchamp5-ezgif com-video-to-gif-converter](https://github.com/yusuyeon1111/portfolio/assets/142488306/3d90494b-3cd9-4401-8763-cca21fa97364)

#### 7-5 이미지 업로드 & 체형 분석 결과 페이지
![제목 없는 동영상 - Clipchamp로 제작 (1)](https://github.com/yusuyeon1111/portfolio/assets/142488306/f3d0c30a-822e-4ffa-9381-7b83d1868d7b)

#### 7-6 사이즈 등록 페이지
![제목 없는 동영상 - Clipchamp로 제작 (1)](https://github.com/yusuyeon1111/portfolio/assets/142488306/f2eb06b4-19fb-4061-9660-477c28c7c9d0)

#### 7-7 아바타 페이지
![제목 없는 동영상 - Clipchamp로 제작 (3)](https://github.com/yusuyeon1111/portfolio/assets/142488306/7ac9ad8e-718b-4b45-930a-8e6966b6eed4)

#### 7-8 관리자 페이지
 ![image](https://github.com/yusuyeon1111/portfolio/assets/142488306/919ebf59-9f54-4013-976c-cf189de56682)
 
</details>

### 4. 담당 기능
<details>
	<summary>기능 펼치기</summary>
	<details>
		<summary> 4-1. 로그인 / 회원가입 기능 </summary>

```
// 회원가입
@PostMapping("/join")
	public void join(@RequestBody MemberDTO dto) {
		dto.incode(dto.getUser_pw());
		memberService.MemberJoin(dto);
	}
// 로그인 	
	@PostMapping("/login")
	public MemberDTO login(@RequestBody MemberDTO dto) {
		MemberDTO login = memberService.MemberLogin(dto);
		if(login != null && passwordEncoder.matches(dto.getUser_pw(), login.getUser_pw())) {
			return login;
		}
		return null;
	}
```
- 회원가입 시 Spring Security를 사용해 비밀번호 암호화 구현
  
- 로그인 시 db에 저장된 암호화된 비밀번호와 사용자가 입력한 비밀번호와 비교하여 일치할 시 로그인 성공하게 구현

- 이메일 인증 기능
  
 ![제목을-입력해주세요_-001 (6)](https://github.com/yusuyeon1111/portfolio/assets/142488306/c88f3dfc-2ed0-4c48-a3ac-4acbbe8579dd)

  - emailjs 라이브러리를 사용해 회원가입시 리액트에서 인증메일을 전송함.
  - 인증번호가 일치해야만 회원가입 가능

```
  const handleGenerateMessage = () => {
    const newMessage = generateMessage();
    setMsg(newMessage);
    sendEmail(user_email, user_name, newMessage)
      .then((res) => {
        setIsEmailSent(true);
        console.log(msg)
      })
      .catch((error) => {
        console.error('이메일 전송 실패', error);
      });
  };
```

</details>
<details>
	<summary> [4-2 커뮤니티 기능](https://github.com/2023-SMHRD-IS-CLOUD-1/Letmein/blob/e8a4241aaa4c41dcea771e42f66afafe000098de/Letmein/src/main/java/com/smhrd/controller/PostController.java#L35) </summary>

- 1. 무한스크롤로 모바일 환경에 최적화된 페이징 구현
- 2. 커뮤니티 글 등록
     - 이미지 업로드 시 S3에 저장  후 spring boot에 전송해 db에 등록함

```
          // aws 이미지 업로드
    AWS.config.update({
      accessKeyId: process.env.REACT_APP_CLIENT_ID,
      secretAccessKey: process.env.REACT_APP_SECRET,
      region: 'us-east-2'
    });
    const s3 = new AWS.S3();

    const uploadParams = {
      Bucket: 'letmein0229',
      Key: `folder/${user_id}${date}/${imgRef.current.files[0].name}`,
      Body: img
    };

    s3.upload(uploadParams, (err, data) => {
      if (err) {
        console.error(err);
      } else {
        console.log(data);
        // spring boot -> db에 저장 
        axios.post("letmein/post", {
          post_title: title,
          post_content: content,
          post_acc: acc,
          post_top: top,
          post_pants: pants,
          post_shoe: shoe,
          user_id: user_id,
          post_imgsrc: `https://d1nypumamskciu.cloudfront.net/folder/${user_id}${date}/${imgRef.current.files[0].name}`
        }).then((res) => {
          console.log(res);
          nav("/community")
        }).catch((error) => {
          console.error(error);
        });
      }
    });
  };
```
- 3. 글 상세보기 기능 구현
     - 좋아요 기능
     - 본인 글 일시 수정, 삭제 기능 구현

</details>

<details>
	<summary> 4-3. 체형분석 & 아바타 페이지 </summary>
	
#### 1. 체형분석 이미지 업로드 기능
	
 - 이미지 업로드 시 s3에 이미지를 업로드
- 업로드 성공시 해당 이미지 url을 flask에 전송해 분석된 성별과 체형 정보를 받아와 저장하도록 구현함.
   
```
// 이미지 업로드 후 분석 실행 
      AWS.config.update({
        accessKeyId: process.env.REACT_APP_CLIENT_ID,
        secretAccessKey: process.env.REACT_APP_SECRET,
        region: 'us-east-2'
      });
      const s3 = new AWS.S3();
  
      const uploadParams = {
        Bucket: 'letmein0229',
        Key: "img.jpg",
        Body: img
      };
  
      s3.upload(uploadParams, (err, data) => {
        if (err) {
          console.error(err);
        } else {
          //파이썬 요청
          axios.post("/upload")
          .then((res) => {
	// 성별
            setGender(res.data.gender)
	// 체형
            setType(res.data.body)
          setSuc(true)
      }).catch((err)=>{
        console.error('분석에러',err)
      })
      }
      });
```

#### 2. 아바타 페이지
- useContext와 useState를 사용해 저장해둔 체형과 성별정보를 기반으로 db에 저장되어 있는 아바타 정보를 확인하여 체형에 해당하는 아바타를 출력
- 체형에 해당하는 코디 이미지를 db에서 가져옴
- 코디 클릭시 아바타 번호와 코디 이미지 번호를 flask에 전달해 가상피팅된 아바타 이미지를 가져옴.

```
// 가상피팅 완료된 아바타 이미지 가져오기!
 axios.post("/try2",{
	// 의상번호
      cloth : codiImgSrc,
	// 아바타 번호
      image : name
      }).then((res)=>{
	// 이미지 결과 저장
        setResultAvatar(res.data)  
    }).catch((err)=>{
      console.error("코디에러",err)
    }
```

</details>



### 5. 트러블 슈팅

<details>
<summary>트러블 슈팅</summary>
	
#### 1. 이메일 API 사용
<br/>
이메일 인증을 위해 이메일 API인 email.js를 사용했습니다.
<br/>

![image](https://github.com/yusuyeon1111/portfolio/assets/142488306/deb5ca66-6f01-4579-b827-d50302f7055c)

<br/>

[코드 보러 가기](https://github.com/2023-SMHRD-IS-CLOUD-1/Letmein-front/blob/05e84843bfaef66c4b6417432049e14dc2a611a1/src/components/Join.jsx#L23)

<br/>


#### 2. 무한 스크롤 기능 구현
모바일 환경에 최적화를 위해 게시판 형식의 기본 페이징이 아닌, 무한 스크롤 방식을 사용함.
기존의 페이징은 offset과 limit을 사용해서 페이징할 범위를 정하지만, 이 방식은 초반에는 효율이 나쁘지 않지만 뒤로 갈수록 효율이 급격히 떨어진다는 단점이 있어 사용하지 않고, JPA의 pageable 기능을 사용해 구현했습니다.
<br/>
 spring Boot 
 <br/>
 @post controller
 <br/>
 
 ![image](https://github.com/yusuyeon1111/portfolio/assets/142488306/65c1da60-66a0-452a-9d12-e09afb0673b0)
 
 <br/>
 
 ![image](https://github.com/yusuyeon1111/portfolio/assets/142488306/e83e393c-8f3c-45c5-ba89-ef1f814407f9)
 
<br/>

React 

<br/>
useInview를 활용하여 페이지 끝에 도달할 시 페이지 넘버를 증가시켜 로드 했습니다.

<br/>

![image](https://github.com/yusuyeon1111/portfolio/assets/142488306/f97031a6-9097-4960-a890-b45568d24586)

<br/>

페이지넘버를 get방식으로 요청해 이미지를 로드 하였습니다.

<br/>

![image](https://github.com/yusuyeon1111/portfolio/assets/142488306/acf1d653-b0b1-471f-ae06-410840c1216f)

<br/>

[코드보러가기](https://github.com/2023-SMHRD-IS-CLOUD-1/Letmein-front/blob/05e84843bfaef66c4b6417432049e14dc2a611a1/src/components/CommunityMasonry.jsx#L76)

<br/>
 [느낀점]
 <br/>
 JPA를 처음 사용하다 보니 어려움을 겪었으나 수많은 시행착오와 구글링을 통해 구현할 수 있었으며, JPA에 대한 이해도를 올릴 수 있었습니다.
</details>

---

## 2. [핵심 프로젝트](https://github.com/2023-SMHRD-IS-CLOUD-1/1stProject.git)
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
  </details>
