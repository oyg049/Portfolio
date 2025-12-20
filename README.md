# 개발자 포트폴리오

## 소개

본 포트폴리오는 C#, C++, .NET (Core / Framework), WPF 등 다양한 기술 스택을 활용하여 개발된 프로젝트들을 소개합니다. 키오스크 브라우저, POS 시스템과 같은 상용 애플리케이션부터 산업용 제어 시스템(철도, RFID), e-러닝 플랫폼, 하드웨어 유틸리티, 음악 연주 프로그램에 이르기까지 폭넓은 분야의 경험을 포함하고 있습니다.

이 프로젝트들은 복잡한 비즈니스 로직, 하드웨어 연동, 실시간 데이터 통신, 데이터베이스 설계 및 클라이언트-서버 아키텍처에 대한 깊은 이해를 보여줍니다.

---

## 보유 기술

*   **언어:** C#, C++, SQL
*   **프레임워크 & 플랫폼:** .NET (8, 6, 4.x), .NET Framework, WPF, Entity Framework
*   **아키텍처:** MVVM, 서비스 지향 아키텍처 (SOA)
*   **데이터베이스:** SQLite, MS-SQL, MySQL
*   **프로토콜 & 통신:** REST API, MQTT, Modbus, TRDP, WebSocket, SOAP, Serial, TCP/IP
*   **하드웨어 연동:** RFID 리더기, 신용카드 단말기, 영수증 프린터
*   **기타:** Inno Setup, Git, 리포팅

---

## 프로젝트 상세

### 1. PEAK9 Rail
*   **설명:** 철도 시스템 또는 관련 장비 개발을 도와줄 시뮬레이션 데스크톱 애플리케이션입니다. .NET 8과 WPF 기반의 최신 MVVM 아키텍처로 설계되었으며, 산업 현장에서 사용되는 다양한 표준 프로토콜을 통해 하드웨어 및 IoT 시스템과 통신합니다.
*   **주요 기능:**
    *   Modbus, 직렬 포트를 통한 산업용 하드웨어 통신
    *   MQTT 프로토콜을 이용한 IoT 시스템 연동
    *   네트워크 패킷 캡처(`SharpPcap`)를 통한 고급 진단 기능
    *   다국어 지원 및 백그라운드 서비스 호스팅
    *   로컬 DB(SQLite)를 사용한 데이터 관리
*   **사용 기술:** C#, .NET 8, WPF, MVVM (CommunityToolkit.Mvvm), SQLite (EF Core), MQTT, Modbus, SharpPcap, Serial Port

### 2. STEP VT (Smart Training & E-learning Platform - Virtual Training)
*   **설명:** 이러닝 가상 교육을 위한 종합 데스크톱 클라이언트입니다. 수강생이 강의를 듣고, 진도율을 추적하며, 교육 콘텐츠와 상호작용할 수 있는 포털 형태의 WPF 애플리케이션입니다.
*   **주요 기능:**
    *   REST API를 통한 클라이언트-서버 아키텍처
    *   과정 카탈로그, 수강 신청, 학습 진도 관리
    *   포인트 및 랭킹 시스템을 통한 게이미피케이션 요소 도입
    *   실시간 알림(MQTT, UWP Notifications) 및 로컬 캐싱(SQLite)
    *   런처 등 다른 프로세스와의 통신을 위한 Named Pipe 활용
*   **사용 기술:** C#, .NET Framework 4.8, WPF, MVVM, SQLite (EF Core), REST API, MQTT, Named Pipes

### 3(1). Flywall
*   **설명:** 전관판 영상/현황 디스플레이 기능을 하는 유칠리티입니다. 백그라운드 스케줄러, 실시간 차트, 시스템 트레이 아이콘 등 고급 기능을 포함하며, 별도의 라이선스 키 생성기를 통해 관리되는 상용 애플리케이션의 특징을 가집니다.
*   **주요 기능:**
    *   `LiveCharts`를 이용한 데이터 시각화 대시보드
    *   `Quartz.NET`을 이용한 백그라운드 작업 스케줄링
    *   WebDAV를 통한 원격 파일 관리 및 동기화
    *   SQLite 데이터베이스를 사용한 로컬 데이터 저장
*   **사용 기술:** C#, .NET 6, WPF, SQLite (EF Core), LiveCharts, Quartz.NET, WebDAVClient

### 3(2). Mac Certification Key Generator
*   **설명:** `Flywall`과 같은 다른 소프트웨어에 사용될 라이선스 키를 생성하는 간단한 유틸리티입니다. 이름에서 유추할 수 있듯이, 네트워크 카드의 MAC 주소와 같은 하드웨어 식별자를 사용하여 특정 장비에 종속되는 키를 생성하는 것으로 보입니다.
*   **주요 기능:**
    *   하드웨어 정보(MAC 주소 등) 기반 라이선스 키 생성
    *   WPF 기반의 간단하고 직관적인 UI
*   **사용 기술:** C#, .NET 8, WPF

### 4. LiveCoach
*   **설명:** 아이스하키 분석을 위한 고도의 스포츠 분석 애플리케이션입니다. 비디오 재생, 데이터 시각화, 3D 렌더링을 결합하여 코치가 경기 영상을 분석하고 선수의 움직임 및 통계를 추적할 수 있도록 설계되었습니다.
*   **주요 기능:**
    *   VLC 플레이어 연동을 통한 경기 영상 재생 및 제어
    *   `HelixToolkit`을 이용한 선수 움직임의 3D 시각화
    *   `LiveCharts`를 활용한 통계 데이터 대시보드
    *   MySQL 및 SQLite 데이터베이스 연동
    *   WebSocket을 통한 실시간 데이터 통신
*   **사용 기술:** C#, .NET Framework 4.6.1, WPF, MVVM, VLC, HelixToolkit, LiveCharts, MySQL, SQLite, WebSocket

### 5. SAPOON (ksp-pos)
*   **설명:** 사푼사푼 카페 종합 POS(Point-of-Sale) 시스템입니다. 주문, 결제, 재고, 매장 관리 등 매장 운영에 필요한 모든 기능을 갖춘 WPF 기반의 상용 애플리케이션입니다.
*   **주요 기능:**
    *   주문 및 결제 처리 (신용카드, 현금, 상품권)
    *   KICC 정보통신 등 국내 결제 게이트웨이 연동
    *   영수증 프린터, 바코드 리더 등 주변 하드웨어 제어
    *   고객 관리, 프로모션, 쿠폰 및 기프트카드 기능
    *   SQLite 기반의 로컬 데이터베이스 및 외부 서버 통신(SOAP, WebSocket)
*   **사용 기술:** C#, .NET Framework 4.8, WPF, MVVM, SQLite (EF6), SOAP, WebSocket, 하드웨어 연동(DLL)

### 6. AlcoBrowser
*   **설명:** 산업용 키오스크를 위해 개발된 맞춤형 데스크톱 브라우저입니다. Microsoft Edge의 WebView2 컨트롤을 사용하여 웹 콘텐츠를 렌더링하며, 원격 제어 및 실시간 통신을 위한 MQTT 기능이 포함되어 있습니다.
*   **주요 기능:**
    *   WPF와 Edge WebView2 컨트롤의 통합
    *   MQTT 프로토콜을 통한 실시간 양방향 통신
    *   설정 페이지를 통한 브라우저 기능 맞춤화
    *   Inno Setup을 통한 배포 패키지 제작
*   **사용 기술:** C#, .NET Framework 4.8, WPF, MVVM, WebView2, M2Mqtt (MQTT), Inno Setup

