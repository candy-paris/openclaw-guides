# OpenRouter 가입 및 API 키 설정 (무료 모델)

**예상 읽기 시간:** 1-2분  
**대상:** API 키 발급이 낯선 분

---

## 단계 1: OpenRouter 웹사이트 접속

브라우저에서 https://openrouter.ai 접속

---

## 단계 2: 회원가입

- 우측 상단 "Sign Up" 클릭
- GitHub/GitLab/Google 연동 또는 이메일 가입
- 이메일 인증 완료

---

## 단계 3: API 키 생성

1. 마이페이지 → "Keys" 메뉴
2. "Create Key" 버튼 클릭
3. 키 이름 입력 (예: "OpenClaw")
4. 생성된 키 복사 (즉시 저장! 한 번만 표시)

키 형식: `sk-or-v1-xxxxxxxxxxxx`

---

## 단계 4: OpenClaw에 OpenRouter 키 설정

터미널에서:

```bash
openclaw config set openrouter.key=YOUR_API_KEY_HERE
```

`YOUR_API_KEY_HERE` 대신 복사한 키 붙여넣기.

---

## 단계 5: 무료 모델 선택

```bash
openclaw config set openrouter.defaultModel=openrouter/stepfun/step-3.5-flash:free
```

---

## 단계 6: 설정 적용 및 재시작

```bash
openclaw gateway restart
```

재시작 후 상황 확인:

```bash
openclaw status
```

모델 연결 상태가 "connected"로 표시되면 성공!

---

✅ **Part 2 완료!** 이제 무료 StepFun 모델을 사용할 수 있습니다.

**다음 단계:** [Part 3: Telegram 연동 가이드](./part3-telegram-integration.md)

**이전 단계:** [Part 1: OpenClaw 설치 및 기본 설정](./part1-openclaw-install.md)
