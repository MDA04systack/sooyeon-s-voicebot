# 박수연의 음성 비서 프로그램 (Voicebot)

이 프로젝트는 OpenAI의 API와 Streamlit을 활용하여 개발된 인공지능 음성 비서 웹 애플리케이션입니다.

## 1. 프로젝트의 주요 기능과 목적, 접속 링크

- **목적**: 사용자의 음성 질문을 텍스트로 변환(STT)하여 ChatGPT 모델에 전달하고, 그에 대한 답변을 다시 음성으로 변환(TTS)하여 들려주는 대화형 인공지능 비서 서비스를 제공합니다.
- **주요 기능**:
  - **음성 인식 (STT)**: OpenAI의 `Whisper` 모델을 활용한 높은 정확도의 음성-텍스트 변환.
  - **인공지능 대화**: OpenAI의 `GPT-3.5-turbo` 및 `GPT-4` 모델을 활용한 맞춤형 답변 제공.
  - **음성 합성 (TTS)**: 구글의 `gTTS` 라이브러리를 사용해 자연스러운 한국어 음성 출력 제공.
  - **대화 기록 시각화**: 사용자와 봇 간의 대화 내용을 메신저 UI 형태로 시각적으로 제공.
- **접속 링크 (서비스 주소)**: [https://sooyeon-s-voicebot.streamlit.app/](https://sooyeon-s-voicebot.streamlit.app/)

## 2. 설치 방법

로컬 환경에서 직접 실행해보고 싶으신 경우 아래의 방법을 따라주세요.

```bash
# 1. 저장소 클론
git clone https://github.com/MDA04systack/sooyeon-s-voicebot.git
cd sooyeon-s-voicebot

# 2. 필수 패키지 설치
pip install streamlit audiorecorder openai gTTS

# 3. 앱 실행
streamlit run voicebot.py
```
*(참고: OpenAI API 키가 별도로 필요합니다. 앱 실행 후 사이드바에 API 키를 입력하여 사용하세요.)*

## 3. 문제 해결 방법

- **마이크 작동이 안 될 때**: 브라우저 설정에서 해당 사이트에 대한 `마이크(Microphone) 접근 권한`이 허용되어 있는지 확인해 주세요.
- **답변이 생성되지 않을 때**: 사이드바에 입력하신 OpenAI API 키가 유효한지, 토큰 한도를 초과하지 않았는지 확인하시기 바랍니다.
- **모듈을 찾을 수 없다는 에러(ModuleNotFoundError)**: `설치 방법`을 참고하여 `streamlit`, `audiorecorder`, `openai`, `gTTS` 패키지가 정상적으로 설치되었는지 확인해 주세요.

## 4. 지원 창구

프로젝트 이용 중 궁금한 점이 있거나 버그를 발견하신 경우 다음 창구를 통해 문의해 주세요.
- **GitHub Issues**: [https://github.com/MDA04systack/sooyeon-s-voicebot/issues](https://github.com/MDA04systack/sooyeon-s-voicebot/issues)

## 5. 라이선스 정보

이 프로젝트는 [MIT 라이선스](LICENSE) 하에 배포됩니다. 자유롭게 활용 및 수정이 가능합니다.

## 6. 변경 로그

- **v1.0.0 (최초 릴리즈)**
  - Streamlit 기반 전체 UI 구축
  - OpenAI Whisper AI 연동 기능 (STT) 추가
  - GPT 채팅 모델(3.5-turbo, 4) 연동 추가
  - Google Translate TTS 연동 기능 (TTS) 추가
