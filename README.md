# 🤖 Agent Bible - AI Agent 실습 환경

패스트캠퍼스 **Agent 초격차** 강의를 위한 실습 환경입니다.

## 📋 목차

- [사전 요구사항](#사전-요구사항)
- [설치 방법](#설치-방법)
- [실습 노트북](#실습-노트북)
- [프로젝트 구조](#프로젝트-구조)
- [문제 해결](#문제-해결)

---

## 🔧 사전 요구사항

- **Python 3.10 이상**
- **OpenAI API 키** ([OpenAI Platform](https://platform.openai.com/)에서 발급)
- (선택) LangSmith API 키 - 추적 및 모니터링용

---

## 🚀 설치 방법

### 1. 저장소 클론

```bash
git clone https://github.com/HarryKane11/FC_Agent_bible.git
cd FC_Agent_bible
```

### 2. 패키지 설치 (두 가지 방법 중 선택)

#### 방법 A: ⚡ uv 사용 (권장 - 10배 이상 빠름!)

[uv](https://github.com/astral-sh/uv)는 Rust로 작성된 초고속 Python 패키지 매니저입니다.

**1) uv 설치:**
```bash
# Windows (PowerShell)
powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"

# Mac/Linux
curl -LsSf https://astral.sh/uv/install.sh | sh
```

**2) 가상환경 생성 + 패키지 설치 (한 줄로 끝!):**
```bash
uv sync
```

**3) 가상환경 활성화:**
```bash
# Windows
.venv\Scripts\activate

# Mac/Linux
source .venv/bin/activate
```

---

#### 방법 B: 기존 pip 사용

**1) 가상환경 생성 및 활성화:**

**Windows:**
```bash
python -m venv venv
venv\Scripts\activate
```

**Mac/Linux:**
```bash
python -m venv venv
source venv/bin/activate
```

**2) 패키지 설치:**
```bash
pip install -r requirements.txt
```

### 4. 환경 변수 설정

```bash
# .env.example을 .env로 복사
cp .env.example .env  # Mac/Linux
copy .env.example .env  # Windows
```

`.env` 파일을 열고 API 키를 입력하세요:

```env
OPENAI_API_KEY=sk-your-actual-api-key-here
```

### 5. Jupyter Notebook 실행

```bash
jupyter notebook
```

---

## 📚 실습 노트북

### Part 1. AI 에이전트 기초 다지기
| 위치 | 노트북 | 설명 |
|------|--------|------|
| CH03 | `CH03.02.01.Langchain으로 구현하는 Basic RAG.ipynb` | LangChain을 활용한 RAG 구현 실습 |
| CH03 | `CH03.02.02.Langgraph로 구현하는 Basic RAG.ipynb` | LangGraph를 활용한 RAG 워크플로우 실습 |

> 📌 Part 2, Part 3 실습 자료는 강의 진행에 따라 순차적으로 업데이트됩니다.

---

## 📁 프로젝트 구조

```
FC_Agent_bible/
├── Part 1. AI 에이전트 기초 다지기/
│   └── CH03.LLM 어플리케이션의 기본, RAG/
│       ├── docs/
│       │   └── DeepSeek_OCR_paper.pdf
│       ├── CH03.02.01.Langchain으로 구현하는 Basic RAG.ipynb
│       └── CH03.02.02.Langgraph로 구현하는 Basic RAG.ipynb
├── Part 2. AI 에이전트 초간단 구현해보기/
│   ├── CH02.노코드 기반의 프레임워크, n8n/
│   ├── CH03.에이전트 PoC 최적의 프레임워크, OpenAI Agent SDK/
│   └── CH04.프로덕션 수준의 프레임워크, Langgraph/
├── Part 3. 멀티 에이전트 구조 정복하기/
│   ├── CH02.Langgraph 기본 워크플로우 구현/
│   └── CH03.Langgraph 통한 실제 AI 에이전트 서비스 따라하기/
├── requirements.txt                # 패키지 의존성
├── .env.example                    # 환경 변수 템플릿
├── .gitignore                      # Git 제외 파일
└── README.md                       # 프로젝트 설명
```

---

## ❗ 문제 해결

### 1. `ModuleNotFoundError` 발생 시

가상환경이 활성화되어 있는지 확인하세요:
```bash
# Windows
venv\Scripts\activate

# Mac/Linux
source venv/bin/activate
```

### 2. OpenAI API 오류 발생 시

- `.env` 파일에 올바른 API 키가 입력되어 있는지 확인
- API 키에 충분한 크레딧이 있는지 확인

### 3. ChromaDB 관련 오류 발생 시

```bash
pip install --upgrade chromadb
```

---

## 📞 문의

강의 관련 문의는 패스트캠퍼스를 통해 연락해주세요.

---

**Happy Coding! 🎉**

