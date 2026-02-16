# OpenClaw 설치 및 기본 설정 가이드 (WSL2/Ubuntu)

**예상 읽기 시간:** 1-2분  
**대상:** Linux/WSL2를 처음 사용하는 분

---

## 단계 1: WSL2 설치

Windows PowerShell을 **관리자 권한**으로 실행 후:

```powershell
wsl --install
```

WSL2 설치가 자동으로 진행되며, Ubuntu 배포판이 기본으로 설치됩니다.

---

## 단계 2: Ubuntu 실행 및 업데이트

WSL을 실행하면 Ubuntu 터미널이 열립니다. 처음 실행 시:

```bash
sudo apt update && sudo apt upgrade -y
```

---

## 단계 3: Node.js 및 npm 확인

```bash
node --version
npm --version
```

OpenClaw는 Node.js 18 이상이 필요합니다. (현재 버전: v22.22.0)

---

## 단계 4: OpenClaw 전역 설치

```bash
npm install -g openclaw
```

---

## 단계 5: OpenClaw 초기 설정

```bash
openclaw init
```

마법사가 시작됩니다:
1. 기본 설정 저장 위치 선택 (기본값 그대로 Enter)
2. Gateway 바인딩 주소: `127.0.0.1` (기본)
3. 기본 모델 선택: StepFun `step-3.5-flash:free` (무료 티어)

"Configuration saved successfully!" 메시지가 나오면 완료!

---

## 단계 6: Gateway 시작

```bash
openclaw gateway start
```

성공 시: "Gateway started on 127.0.0.1:18789"

---

✅ **Part 1 완료!** 이제 OpenClaw가 로컬에서 실행 중입니다.

**다음 단계:** [Part 2: OpenRouter 가입 및 API 키 설정](./part2-openrouter-setup.md)
