﻿# 🎮 Game Server Study

**C++을 활용한 게임 서버 개발 학습 프로젝트**

이 저장소는 C++을 사용한 게임 서버 개발 학습을 위한 교육용 프로젝트입니다. 멀티쓰레드 프로그래밍, 동기화 메커니즘(Lock), 그리고 네트워크 프로그래밍의 핵심 개념들을 실제 게임 서버 환경에서 학습하고 구현하는 것을 목표로 합니다.

---

## 📋 프로젝트 개요

본 프로젝트는 현대적인 게임 서버 개발에 필요한 핵심 기술들을 체계적으로 학습할 수 있도록 설계되었습니다. 이론적 지식과 실무 경험을 동시에 제공하여, 실제 운영 환경에서 사용할 수 있는 견고하고 확장 가능한 게임 서버 구축 능력을 배양합니다.

### 🎯 학습 목표

- **C++ 기반 게임 서버 아키텍처 이해**: 현대적인 게임 서버의 구조와 설계 패턴 학습
- **멀티쓰레드 환경에서의 동기화 기법 습득**: Lock, Mutex, 세마포어 등을 활용한 스레드 안전성 보장
- **네트워크 프로그래밍 기초 및 실전 응용**: TCP/UDP 소켓 통신과 비동기 I/O 처리 마스터
- **클라이언트-서버 통신 구조 설계**: 효율적인 프로토콜 설계와 세션 관리 기법 학습
- **게임 서버 최적화 및 성능 튜닝**: 실제 운영 환경에서 필요한 최적화 기법 습득

---

## 🏗️ 프로젝트 구조

```
Game_Server_Study/
├── 📁 DummyClient/                  # 테스트용 클라이언트 구현체
├── 📁 Libraries/Debug/              # 디버그 모드 라이브러리 및 의존성
├── 📁 ServerCore/                   # 게임 서버 핵심 로직 구현
├── 📁 Server_Cpp/                   # 메인 서버 애플리케이션
├── 📄 Server_Cpp.sln                # Visual Studio 솔루션 파일
└── 📄 Server_Cpp.slnLaunch.user     # 개발자별 실행 설정
```

| 디렉토리/파일 | 설명 |
|--------------|------|
| **DummyClient/** | 서버와의 통신을 테스트하기 위한 더미 클라이언트 애플리케이션. 다양한 시나리오 시뮬레이션 가능 |
| **Libraries/Debug/** | 디버그 모드에서 사용되는 라이브러리 파일들과 의존성 관리 |
| **ServerCore/** | 네트워크 처리, 멀티쓰레딩, 동기화 등 게임 서버의 핵심 기능 구현 |
| **Server_Cpp/** | ServerCore를 활용한 실제 게임 서버 로직과 비즈니스 규칙 구현 |

---

## 🛠️ 기술 스택

### 💻 프로그래밍 언어
- **C++ (89.4%)**: 메인 서버 로직 및 핵심 기능 구현
- **C (10.6%)**: 저수준 시스템 프로그래밍 및 성능 최적화

### 🔧 핵심 기술
- **멀티쓰레딩**: 동시성 처리 및 성능 최적화를 위한 스레드 관리
- **동기화 메커니즘**: Lock, Mutex, 세마포어 등을 활용한 스레드 안전성 보장
- **네트워크 프로그래밍**: TCP/UDP 소켓 통신, 비동기 I/O 처리
- **메모리 관리**: 효율적인 메모리 할당 및 해제 전략 구현

---

## 🚀 시작하기

### ⚙️ 필요 조건

- **Visual Studio 2019 이상** (C++17 표준 지원)
- **Windows 10/11** (Windows API 의존성)
- **최소 4GB RAM** (멀티쓰레드 환경 테스트를 위해)

### 📦 빌드 및 실행

```bash
# 1. 저장소 클론
git clone https://github.com/LimJunHui-dot/Game_Server_Study.git

# 2. Visual Studio에서 프로젝트 열기
# Server_Cpp.sln 파일을 Visual Studio로 열기

# 3. 솔루션 빌드
# Ctrl + Shift + B 또는 메뉴에서 빌드 실행

# 4. 서버 실행
# Server_Cpp 프로젝트를 시작 프로젝트로 설정
# F5 키로 디버그 모드 실행 또는 Ctrl + F5로 일반 실행

# 5. 클라이언트 테스트
# DummyClient 프로젝트 실행으로 서버 연결 테스트
```

---

## 📖 주요 학습 내용

### 🎮 ServerCore 모듈

ServerCore는 게임 서버의 핵심 기능을 담당하는 모듈로, 다음과 같은 주요 기능들을 포함합니다:

- **네트워크 추상화**: 소켓 통신을 추상화한 고수준 네트워크 레이어
- **스레드 풀**: 작업 분산 및 성능 최적화를 위한 효율적인 스레드 관리
- **동기화 유틸리티**: Lock-free 자료구조 및 다양한 동기화 프리미티브
- **메모리 풀**: 빈번한 할당/해제를 최적화하는 메모리 풀링 시스템

### 🧵 멀티쓰레딩 학습 요소

멀티쓰레드 환경에서의 동시성 제어와 성능 최적화를 위한 핵심 기법들을 학습합니다:

- **Producer-Consumer 패턴**: 생산자-소비자 모델을 통한 작업 분산 및 동기화
- **Reader-Writer Lock**: 읽기/쓰기 작업의 효율적인 동기화 메커니즘
- **Lock-free 프로그래밍**: 무잠금 자료구조를 활용한 고성능 구현 기법
- **데드락 방지**: 교착상태 예방 및 성능 최적화를 위한 전략

### 🌐 네트워크 프로그래밍 학습 요소

효율적인 네트워크 통신과 클라이언트 관리를 위한 핵심 기술들을 다룹니다:

- **비동기 소켓 통신**: 논블로킹 I/O를 활용한 효율적인 네트워크 처리
- **패킷 직렬화/역직렬화**: 데이터 전송을 위한 효율적인 변환 기법
- **연결 관리 및 세션 처리**: 클라이언트 연결 상태 관리와 세션 유지
- **네트워크 오류 처리**: 통신 장애 상황에서의 복구 및 재시도 로직

---

## 🔧 개발 환경 설정

### 🎨 Visual Studio 권장 설정

프로젝트 최적화를 위해 다음 설정을 권장합니다:

- **C++ 표준**: C++17 이상
- **플랫폼**: x64 (64비트 환경)
- **런타임 라이브러리**: Multi-threaded (/MT)
- **최적화**: 디버그 모드에서는 비활성화, 릴리스 모드에서는 전체 최적화

### 🐛 디버깅 팁

효율적인 디버깅을 위한 실용적인 팁들입니다:

- **멀티쓰레드 디버깅**: Visual Studio의 스레드 창을 활용하여 각 스레드의 상태를 모니터링
- **네트워크 통신 디버깅**: 상세한 로그 시스템을 구축하여 패킷 흐름을 추적
- **메모리 누수 검사**: CRT 디버그 힙을 활용하여 메모리 관리 문제를 조기에 발견

---

## 📚 학습 가이드

### 📈 단계별 학습 순서

체계적인 학습을 위한 단계별 가이드입니다:

1. **기초 개념 이해**: C++ 기본 문법 및 객체지향 프로그래밍 원리 숙지
2. **멀티쓰레딩 기초**: `std::thread`, `mutex`, `condition_variable` 등 기본 동시성 도구 학습
3. **네트워크 프로그래밍**: 소켓 API 및 비동기 통신 메커니즘 이해
4. **서버 아키텍처**: 클라이언트-서버 모델 설계 및 확장성 고려사항 학습
5. **성능 최적화**: 프로파일링 도구를 활용한 성능 분석 및 튜닝 기법 습득

### 🎯 실습 프로젝트

단계별로 다음과 같은 실습을 통해 점진적으로 복잡한 서버를 구현할 수 있습니다:

1. **에코 서버 구현**: 기본적인 네트워크 통신과 메시지 에코 기능
2. **채팅 서버 구현**: 멀티 클라이언트 처리와 브로드캐스팅 기능
3. **게임 로비 서버 구현**: 세션 관리와 룸 시스템 구현
4. **실시간 게임 서버 구현**: 게임 상태 동기화와 실시간 업데이트 처리

