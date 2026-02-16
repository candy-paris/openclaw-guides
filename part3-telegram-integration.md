# Telegram 연동 가이드

**예상 읽기 시간:** 1-2분  
**대상:** BotFather 사용이 처음인 분

---

## 단계 1: BotFather 시작

Telegram 앱에서 `@BotFather` 검색 → 채팅 시작

---

## 단계 2: 새 봇 생성

BotFather에게 `/newbot` 전송

봇 이름 입력 (예: `My OpenClaw Bot`)

유저네임 입력 (예: `MyOpenClawBot` 또는 `my_openclaw_bot_bot`)

"Done! Congratulations on your new bot..." 메시지가 표시됩니다.

---

## 단계 3: API 토큰 받기

BotFather이 다음과 같이 응답합니다:

```
Use this token to access the HTTP API:
1234567890:ABCdefGHIjklMNOpqrsTUVwxyz-1234567890
```

**반드시 이 토큰을 안전한 곳에 복사해 두세요!**

---

## 단계 4: OpenClaw에 Telegram 설정

터미널에서:

```bash
openclaw config set telegram.botToken=YOUR_BOT_TOKEN_HERE
openclaw config set telegram.chatIds=YOUR_CHAT_ID
```

**chatIds**는 본인의 Telegram 채팅 ID입니다.

---

## 단계 5: 본인의 Chat ID 찾기

**방법 A (추천):**
1. 방금 만든 봇에게 `/start` 메시지 보내기
2. 잠시 후 BotFather에게 `/getupdates` 전송
3. 응답에서 `"chat":{"id":123456789,...}` 숫자를 찾기

**방법 B:**
@userinfobot 봇에게 메시지 보내기 → ID 확인

---

## 단계 6: Gateway 재시작

```bash
openclaw gateway restart
```

---

## 단계 7: 테스트

Telegram에서 봇에게 아무 메시지나 보내보세요. OpenClaw가 응답하면 성공입니다!

---

✅ **Part 3 완료!** Telegram 연동이 끝났습니다. 이제 메시지로 OpenClaw를 제어할 수 있어요.

**첫 번째 단계:** [Part 1: OpenClaw 설치 및 기본 설정](./part1-openclaw-install.md)

**이전 단계:** [Part 2: OpenRouter 가입 및 API 키 설정](./part2-openrouter-setup.md)
