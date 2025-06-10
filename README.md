# ⛰️ 나만의 하이킹 메이트, 마이킹(Myking) - 등산 정보 제공 및 등산 메이트 매칭 플랫폼
<div align="center">
   최근 몇 년 간 등산은 소위 MZ 세대의 트렌디한 취미로 자리잡았다.<br />하지만 등산 입문자에게는 편한 코스 혹은 빨리 올라갈 수 있는 코스 등을 알아보는 일이 쉽지만은 않다.<br />마이킹(Myking)은 흩어져 있는 <strong>등산 정보를 보기 쉽게 제공</strong>한다.<br />또한, 등산이라는 취미를 공유할 수 있는 공간을 제공함으로써 <strong>신뢰도 있는 등산 메이트를 만날 수 있도록 하기 위해 마이킹(Myking)을 구현하게 되었다.</strong><br />
</div>

## 🛠️ 기술 스택
- **프레임워크**: ![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=Next.js&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=TypeScript&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=React&logoColor=black)
![Styled-Components](https://img.shields.io/badge/Styled--Components-DB7093?style=flat-square&logo=styled-components&logoColor=white)
- **개발 언어**: ![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=JavaScript&logoColor=black)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=HTML5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=CSS3&logoColor=white)
- **데이터베이스**: ![Supabase](https://img.shields.io/badge/Supabase-3ECF8E?style=flat-square&logo=Supabase&logoColor=white)

## ✨ 기능
### 1️⃣ 등산 코스를 손쉽게 검색하거나 조회할 수 있어요!
찾기 어려운 여러 등산 코스 정보를 검색 한 번으로 쉽게 찾아볼 수 있습니다.

✅ 외부 API를 사용해 등산로 정보 조회
✅ 검색된 코스를 상세 페이지에서 확인 가능

### 2️⃣ 파티를 모집하고, 다른 사용자와 함께 등산을 계획해요!
등산 파티를 만들고 다른 사용자의 참여를 받을 수 있습니다.

✅ 파티 생성, 수정, 삭제 기능
✅ 모집 상태(모집 중 / 모집 마감 등) 관리

 ### 3️⃣ 내가 참여 중이거나 생성한 파티를 한 눈에 볼 수 있어요!
 참여하거나 직접 생성한 파티를 쉽게 확인하고 관리할 수 있습니다.

 ✅ 참여/생성한 파티 목록 조회
 ✅ 참여 취소 기능 제공(마감 후 취소는 불가능)

 ### 4️⃣ 내 프로필도 자유롭게 관리할 수 있어요!
 소셜 로그인(카카오)를 통해 간편하게 가입하고, 자유롭게 관리할 수 있습니다.

 ✅ 닉네임, 프로필 사진 등의 프로필 정보 수정
 ✅ 사용자 정보 조회 기능

## 📺 프로젝트 시연
[전체 프로젝트 시연](https://www.canva.com/design/DAGkb-XsG-o/NozjwFtMg8WaX_Qwu6aaQA/view?utm_content=DAGkb-XsG-o&utm_campaign=designshare&utm_medium=link2&utm_source=uniquelinks&utlId=he86a4dea2d#19)

### 1️⃣ 회원가입 및 로그인
![마이킹-회원가입및로그인](https://github.com/user-attachments/assets/06795215-80f2-44a7-8ba0-d9bcb7062c5b)

### 2️⃣ 게시/참여한 파티 조회
![image](https://github.com/user-attachments/assets/89c2fea6-c000-4033-84e2-0870b9c6654b)

### 3️⃣ 게시/참여한 파티 삭제
![image](https://github.com/user-attachments/assets/ab31efe1-d829-4bf2-b4c9-9de95aec1589)

### 4️⃣ 사용자 정보 수정
![마이킹-사용자정보수정](https://github.com/user-attachments/assets/17a53eca-8f90-43c4-8369-e8c2a08df211)

## 📁 폴더 구조
```plaintext
myking
├─ app/                    # Next.js 라우트 기반 폴더 (페이지 및 레이아웃 정의)
├─ application/            # 유스케이스 및 상태 관리 계층
├─ components/             # 공통 UI 컴포넌트 모음
├─ context/                # 글로벌 컨텍스트 API (예: AuthProvider)
├─ domain/                 # 엔티티와 인터페이스 정의 (비즈니스 로직 계층)
├─ infrastructure/         # 외부 서비스 및 저장소 구현체
├─ public/                 # 정적 리소스 (이미지, 아이콘 등)
├─ utils/                  # 공통 유틸 함수 (토큰 관리, Supabase 클라이언트 등)
└─ @types/                 # 전역 타입 선언 (예: next-auth 타입 확장)
```

### 폴더 설명
| 폴더명 | 설명 |
| -- | -- |
| app/ | 라우팅을 담당하는 폴더로, Next.js 의 App Router 구조에 따라 페이지, 레이아웃, API 핸들러들을 구성합니다. |
| application/ | 유스케이스 중심의 비즈니스 로직 처리 계층입니다. DTO, 상태관리(Zustand), 각종 UseCase가 포함되어 있습니다. |
| components/ | 프로젝트에서 공통으로 사용하는 UI 컴포넌트를 분리하여 재사용성을 높입니다. |
| context/ | 전역 상태 관리를 위한 React Context API를 관리합니다. (ex. 인증 상태) |
| domain/ | 핵심 도메인 모델 및 Repository 인터페이스 정의가 포함되어 있습니다. |
| infrastructure/ | Supabase 등 외부 의존성 구현체가 정의된 계층입니다. Repository 인터페이스의 실제 구현체가 위치합니다. |
| public/ | 앱에서 사용되는 이미지, 아이콘 등의 정적 파일이 포함됩니다. |
| utils/ | 공통적으로 사용되는 유틸리티 함수들이 위치합니다. Supabase 초기화, 토큰 처리 등도 포함됩니다. |
| @types/ | 타입 확장 및 전역 타입 설정을 위한 폴더입니다. 예: next-auth 타입 정의 확장 등 |

## 🧑‍🧒‍🧒 프로젝트 구성원
| [권영우(T)](https://github.com/kwonup) | [고가연](https://github.com/gayeongogo) | [김민경](https://github/m01310g) | [김종윤](https://github.com/whddbsl) |
| -- | -- | -- | -- |
|   <img src="https://github.com/user-attachments/assets/07fd2755-20ff-45fe-88a3-a7a60a7f4054" width="200px" /> |   <img src="https://github.com/user-attachments/assets/1abfbcc5-1e00-43dd-9a8d-9082768484f8" width="200px" /> |   <img src="https://github.com/user-attachments/assets/709647ca-bea5-46a8-bd05-e05852c7c24a" width="200px" /> |   <img src="https://github.com/user-attachments/assets/9007b5c8-40b8-46ce-be10-da53b6f89126" width="200px" /> |
