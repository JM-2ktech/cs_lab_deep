---
title: 용어집
nav_order: 12
---

# 용어집

이 과정에서 쓰는 용어를 등장하는 일차 순서로 정리했습니다. 각 항목에는 고정 id가 있어 다른 페이지에서 `../glossary.html#id`로 연결할 수 있습니다.

## D1. 실행 환경

### 하네스 (실행 환경) `#harness`
{: #harness }
모델을 감싸고 실제로 일을 하게 하는 환경. 작업 대상, 빌트인 스킬, 코드 실행 공간, 개인 설정으로 이루어진다. 같은 모델이라도 하네스가 다르면 처리 방식과 결과가 달라진다.

### 오케스트레이터 `#orchestrator`
{: #orchestrator }
사용자 입력을 보고 어떤 지식·도구·스킬을 쓸지 정하는 판단 계층. 문장을 만드는 LLM과 역할이 다르다.

### LLM (거대 언어 모델) `#llm`
{: #llm }
실제 텍스트를 만드는 모델. 오케스트레이터의 판단에 따라 호출된다.

### 빌트인 스킬 `#built-in-skill`
{: #built-in-skill }
앱마다 기본으로 들어 있는 작업 능력. Word·Excel·PowerPoint의 Copilot 창에서 **+** → **플러그 인 선택**으로 목록을 본다. 앱마다 항목이 다르다.

### 플러그 인 `#plugin`
{: #plugin }
Copilot에 붙여 쓰는 스킬·에이전트·확장 기능의 묶음. 화면에서는 「플러그 인」 메뉴로 관리한다.

### 개인 설정 (사용자 지정·메모리) `#personalization`
{: #personalization }
내 모든 대화에 걸리는 지침과 기억. 항상 필요한 원칙만 넣는다. 필요할 때만 쓰는 방식은 스킬로 만든다.

### 코드 실행 공간 (Sandbox) `#sandbox`
{: #sandbox }
Copilot이 파일을 열어 코드로 계산하는 격리된 공간. 대화마다 따로 있고, 시간이 지나면 정리한 결과가 남지 않는다. 인터넷과 사내 시스템에는 연결되지 않는다. Excel·PowerPoint·Chat에는 있고 Word에는 없다.

## D2. 확장과 자산화

### 코드베이스 `#codebase`
{: #codebase }
검증한 처리 방법을 다시 쓸 수 있게 남겨 둔 코드와 규칙의 묶음. 이 과정에서는 스킬 안에 넣어 둔다.

### fastexcel `#fastexcel`
{: #fastexcel }
엑셀 파일을 빠르게 읽는 도구. 실습 스킬이 코드 실행 공간에 설치해 쓴다.

### Polars `#polars`
{: #polars }
읽은 표를 정리하고 집계하는 도구.

### SQLite `#sqlite`
{: #sqlite }
표를 파일 하나에 담아 두고 질문마다 계산식(SQL)으로 조회하는 데이터베이스. 코드 실행 공간에 기본으로 들어 있다.

### 스킬 (기술) `#skill`
{: #skill }
`SKILL.md`에 업무 지침·처리 규칙·템플릿·스크립트를 묶은 작업 방식. 입력란에 `@스킬이름`으로 멘션해 필요할 때 부른다. 화면 이름은 「기술」이다.

### 재현성 `#reproducibility`
{: #reproducibility }
같은 입력과 같은 요청으로 다시 실행했을 때 같은 결과가 나오는 성질. 규칙과 형식을 스킬로 정해 두면 높아진다.

### Agent Builder `#agent-builder`
{: #agent-builder }
Microsoft 365 Copilot에 들어 있는 에이전트 제작 도구. 이름·설명·지침을 채워 만든다. 지식 범위를 특정 파일·사이트로 좁힐 수 있다.

### 지침 (Instructions) `#instructions`
{: #instructions }
에이전트의 역할·답변 원칙·경계 규칙을 정의하는 텍스트.

### 지식 (Knowledge) `#knowledge`
{: #knowledge }
에이전트가 근거로 삼는 문서·사이트. 기준을 담는 자료이며 실시간 개인 데이터가 아니다.

### 그라운딩 `#grounding`
{: #grounding }
답을 만들기 전에 질문과 가까운 자료를 찾아 붙이는 단계. 목적은 정답을 보증하는 것이 아니라 관련 자료를 빠르게 찾는 것이다. 찾은 자료가 맞는지는 따로 검증한다.

### Indexing (인덱싱) `#indexing`
{: #indexing }
업로드한 문서를 검색할 수 있게 처리하는 과정. 끝날 때까지 시간이 걸린다. 업로드 직후에는 파일 이름으로 불러도 찾지 못할 수 있다.

### RAG (검색 증강 생성) `#rag`
{: #rag }
질의 → 검색 → 그라운딩 → 생성 순서로, 찾은 자료를 근거로 답을 만드는 방식.

### Work IQ `#work-iq`
{: #work-iq }
Microsoft 365 Copilot이 메일·일정·문서·채팅 같은 업무 맥락을 찾아 답에 쓰는 기반.

### Copilot Studio `#copilot-studio`
{: #copilot-studio }
지식·지침·도구·토픽·흐름을 붙여 에이전트를 만들고 확장하는 도구.

## D3. 위임과 통제

### SharePoint List `#sharepoint-list`
{: #sharepoint-list }
SharePoint에 만드는 표 형식 데이터. 열마다 형식(텍스트·선택·사람·날짜·조회 등)을 정해 두고 행 단위로 쌓는다.

### 커넥터 (표준 커넥터) `#connector`
{: #connector }
SharePoint·Excel·Outlook 같은 서비스에 미리 만들어진 방식으로 연결하는 도구.

### 에이전트 흐름 (Agent flow) `#agent-flow`
{: #agent-flow }
에이전트가 도구로 호출하는 흐름. 「에이전트가 흐름을 호출할 때」 트리거로 시작한다.

### 클라우드 흐름 (Power Automate) `#cloud-flow`
{: #cloud-flow }
파일 생성·List 행 추가 같은 이벤트를 트리거로 시작하는 Power Automate 흐름.

### 승인 흐름 `#approval-flow`
{: #approval-flow }
사람이 승인하거나 반려해야 다음 단계로 가는 흐름. 사람의 판단을 업무 절차에 넣는 방법이다.

### HITL (Human-in-the-loop) `#hitl`
{: #hitl }
자동화 과정에 사람의 승인·확인이 들어가는 지점.

### 자율 실행 `#autonomous`
{: #autonomous }
사람이 부르지 않아도 트리거가 에이전트를 실행하는 방식. 라이선스와 관계없이 크레딧이 청구된다. 이 과정에서는 소개만 한다.

### Copilot Credit `#copilot-credit`
{: #copilot-credit }
Copilot Studio 사용량을 환산한 과금 단위. 기준은 기초교육 Part 04를 따른다.

### Tokenizer / 토큰 `#tokenizer`
{: #tokenizer }
텍스트를 잘게 쪼갠 단위. 길이 제한과 사용량 계산의 기준이 된다.

## 부록에서 쓰는 용어

### 생성형 오케스트레이션 `#generative-orchestration`
{: #generative-orchestration }
사용자 입력을 보고 에이전트가 지식·도구·토픽을 골라 조합해 답하는 방식.

### 토픽 (Topic) `#topic`
{: #topic }
정해진 트리거 문구에 반응하는 대화 단위. 생성형 오케스트레이션과 대비된다.

### 트리거 문구 `#trigger-phrase`
{: #trigger-phrase }
토픽을 실행시키는 정해진 입력 문구(또는 비슷한 표현).

### Question 노드 `#question-node`
{: #question-node }
토픽 안에서 사용자에게 질문하고 응답을 변수로 받는 단위.

### 변수 (Variable) `#variable`
{: #variable }
토픽 안에서 사용자 응답이나 도구 결과에 이름을 붙여 담아 두는 값. 다음 노드에서 다시 쓸 수 있다.

### Adaptive Card `#adaptive-card`
{: #adaptive-card }
응답을 구조화된 카드 형태로 보여 주는 메시지 형식.

### 연결된 에이전트 `#connected-agent`
{: #connected-agent }
다른 에이전트를 도구처럼 등록해 호출하는 방식. 부모 에이전트는 자식의 설명(Description) 한 문단만 읽고 호출 여부를 정한다.

### MCP (Model Context Protocol) `#mcp`
{: #mcp }
외부 서버가 제공하는 도구·리소스를 표준 방식으로 에이전트에 연결하는 프로토콜.

### 커스텀 커넥터 `#custom-connector`
{: #custom-connector }
API 스펙을 직접 정의해 만드는 커넥터. 표준 커넥터나 MCP보다 만들기 어렵다.
