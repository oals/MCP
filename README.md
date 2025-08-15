# 🌐 MCP (Model Context Protocol)

**MCP**는 Anthropic에서 개발한 **LLM이 외부 애플리케이션과 연동**할 수 있도록 해주는 프로토콜 <br>
다양한 데이터 소스 및 도구에 양방향 연결을 구축할 수 있는 **표준화된 방식**을 제공

**클로드 모델**은 기본적으로 학습된 내용을 바탕으로 텍스트 응답만 생성할 수 있지만, <br>
**MCP를 활용하면 외부 애플리케이션과의 연동이 가능해집니다.** <br>
<br>
이를 통해 **노션에 글을 작성하거나, 구글 캘린더의 일정을 수정**하는 등의 실제 작업을 수행할 수 있습니다.

---

<img width="1024" height="576" alt="test" src="https://github.com/user-attachments/assets/64cdfc51-c5a0-430f-8921-003662a0c82c" />

<br>

## 🔧 MCP 아키텍처


- **🧠 MCP Host**  
  MCP를 통해서 외부 작업을 요청하는 **LLM 주체**

  
- **🌐 MCP Server**  
  MCP 표준으로 **정의 되어있는 도구**


- **📡 MCP Client**  
  사용자의 요청을 받아 **MCP Server**에 전달하는 역할을 합니다.  

---

## 📚 목차

> 🔑 **[노션 API 키 생성](#노션-api-키-생성)**   <br><br>
> 🤖 **[클로드 MCP 연결](#클로드-mcp-연결)**   <br><br>
> 📄 **[결과](#결과)** 

---


# 💻 클로드로 Notion에 글 작성하기


# 노션 API 키 생성 

- [Notion 개발자 페이지](https://developers.notion.com/)

<br>

<img width="1423" height="107" alt="notionapi키얻기" src="https://github.com/user-attachments/assets/43e23f76-e6d7-47f2-8990-d3ebc5ad94ef" />

- 오른쪽 상단의 **View my integrations** 버튼 클릭  

<br>

<img width="1254" height="185" alt="노션디벨로퍼 api통합" src="https://github.com/user-attachments/assets/2ffd0f7b-f55d-4e6e-9582-6726fceb935c" />

- **새 API 통합** 생성
<br>

<img width="1288" height="563" alt="새 api 통합" src="https://github.com/user-attachments/assets/f8d36a2f-0346-4d1f-9a4d-b5fe84a2e907" />

- 통합 이름을 설정하고 **필요한 권한**을 선택한 후 저장
<br>

<img width="1277" height="267" alt="notion페이지권한" src="https://github.com/user-attachments/assets/6b5afe90-6fc2-421e-838f-215311e7aedc" />

- **사용 권한 탭**으로 이동하여 페이지 접근 권한 설정
<br>

<img width="1263" height="416" alt="노션페이지권한1" src="https://github.com/user-attachments/assets/d080abcb-f699-4cce-b78e-0b01dbea30c0" />

<br>

<img width="590" height="573" alt="사용권한전달" src="https://github.com/user-attachments/assets/eebe49b8-b720-4585-902a-ddfd536b382c" />

- **LLM**에서 접근하려는 노션 페이지 추가
<br>

<img width="1304" height="278" alt="키 확인" src="https://github.com/user-attachments/assets/efcf3c57-41e5-4c92-a58b-cb1a564b126a" />

- **구성 탭**으로 이동하여 API키 복사
<br>

---

# 클로드 MCP 연결


<img width="481" height="137" alt="simithery" src="https://github.com/user-attachments/assets/a38ea9ab-76d3-4a90-81ac-b8d48236a2e6" />

- [Smithery](https://smithery.ai/)

**Smithery**는 여러 가지 **MCP 서버들을 모아놓은 플랫폼**
<br>

<img width="878" height="250" alt="notion검색" src="https://github.com/user-attachments/assets/3ea53776-cabc-4b23-ad31-cd0e2ae1fa4c" />

- 검색창에 **Notion** 검색
<br>

<img width="436" height="196" alt="notion다운로드" src="https://github.com/user-attachments/assets/0596b777-1a01-42f0-b5cd-c3a9d62c4f69" />

- 가장 많이 사용된 **Notion MCP Server** 선택
<br>

<img width="502" height="491" alt="mcpnotion연결" src="https://github.com/user-attachments/assets/f9bd92c5-025a-4f6d-87d0-ba555c39ae47" />

- [Notion 개발자 페이지](https://developers.notion.com/)에서 복사한 **Notion Api** 키 입력
<br>

<img width="506" height="576" alt="mcpjson받기" src="https://github.com/user-attachments/assets/08971474-f200-4d68-abf5-2b9aeb8dcabf" />

- 생성된 **JSON 데이터** 복사
<br>

<img width="288" height="193" alt="클로드설정이동" src="https://github.com/user-attachments/assets/4576577a-22e2-42a1-ac5a-bca90cce2f2f" />

- 클로드를 열어 **설정**으로 이동
<br>

<img width="998" height="803" alt="구성편집" src="https://github.com/user-attachments/assets/bc4083e9-6cc8-4ff2-ba39-9a0ddb26e9bf" />

- **개발자**탭으로 이동하여 구성편집 클릭
<br>

<img width="1129" height="615" alt="구성편집2" src="https://github.com/user-attachments/assets/b9705ea2-5d1d-4c29-a188-7842074a51d0" />

- 폴더가 열리면 **claude_desktop_config** 파일 열기
<br>

<img width="690" height="416" alt="구성편집3" src="https://github.com/user-attachments/assets/73300f93-c920-4e6b-96fb-6f1c697d33de" />

- [Smithery](https://smithery.ai/)에서 복사한 JSON 데이터 입력
<br>

<img width="302" height="181" alt="구성편집4 종료" src="https://github.com/user-attachments/assets/cbd45752-cb3f-4a79-965f-7f0f4cbf2fc3" />

- **종료**버튼을 눌러 클로드 재시작
<br>

<img width="996" height="794" alt="노션 커넥터 연결 " src="https://github.com/user-attachments/assets/473bae21-8032-468c-8619-0e6a308e1bfc" />
<img width="1000" height="801" alt="노션 개발자 연결" src="https://github.com/user-attachments/assets/89aa6770-b20d-4166-a77c-af4ccd627107" />
  
- **설정**으로 이동하여 연결이 제대로 됐는지 확인
<br>

<img width="624" height="135" alt="노션페이지아이디" src="https://github.com/user-attachments/assets/cf5f23f5-6e3f-4da3-9708-9caf47bf4caf" />

- 클로드를 통해 작성할 **노션 페이지 아이디** 복사
<br>

<img width="717" height="279" alt="명령어입력" src="https://github.com/user-attachments/assets/b6372e5d-7b37-47cd-8085-3b1957fd0f4c" />

- **노션 페이지 아이디**를 포함하여 클로드에게 명령
<br>

<img width="986" height="791" alt="클로드답변" src="https://github.com/user-attachments/assets/126fda45-0c5c-4656-a0d3-68c7ca2752a1" />

<br>
<br>

# 결과

<img width="749" height="832" alt="노션잓어완료" src="https://github.com/user-attachments/assets/0ac8413c-55d3-409f-a90a-f9318f4207cf" />

<br>



