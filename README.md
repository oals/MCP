# 💻 MCP (Model Context Protocol)

**MCP**는 LLM(대형 언어 모델)이 외부 애플리케이션과 연동할 수 있도록 해주는 프로토콜입니다.

<br>

**클로드 모델**은 기본적으로 학습된 내용을 바탕으로 텍스트 응답만 생성할 수 있지만, **MCP를 활용하면 외부 애플리케이션과의 연동이 가능해집니다.** <br>
이를 통해 사용자의 명령으로 **노션에 글을 작성하거나, 구글 캘린더의 일정을 수정**하는 등의 실제 작업을 자동으로 수행할 수 있습니다.





## 📱 목차

> 🏠 **[노션 에이전트 다운로드](#)**  <br><br>
> 🏠 **[노션 API 키 발급](#)**  <br><br>
> 🏠 **[MCP 연결](#)**  <br><br>
> 🏠 **[결과](#)**  <br><br>

---


# 💻 클로드로 notion에 글 작성하기


# 노션 API 키 생성 

https://developers.notion.com/  <br>

이동

<img width="1423" height="107" alt="notionapi키얻기" src="https://github.com/user-attachments/assets/b9bac8b8-fd63-4656-82eb-7d9f94398416" />

오른쪽 상단 view my integrations 클릭 


<img width="1254" height="185" alt="노션디벨로퍼 api통합" src="https://github.com/user-attachments/assets/011d7d3b-d7a3-4bab-8c78-3690934ebe64" />

새 api 통합 

<img width="1288" height="563" alt="새 api 통합" src="https://github.com/user-attachments/assets/89dbf292-c471-4ae1-bfc5-3d9142f5b6ab" />

저장

<img width="1277" height="267" alt="notion페이지권한" src="https://github.com/user-attachments/assets/3170d175-cbf1-4347-a668-dc862e4de4fe" />

Access tab 클릭

<img width="1263" height="416" alt="노션페이지권한1" src="https://github.com/user-attachments/assets/df2ef813-44b4-45be-af76-197973f5907b" />

페이지 선택

<img width="590" height="573" alt="사용권한전달" src="https://github.com/user-attachments/assets/877d1101-c6e6-45cf-9f85-e328d15915ce" />

페이지 사용 권한 업데이트

<img width="1287" height="426" alt="사용권한페이지확인" src="https://github.com/user-attachments/assets/62cf472e-1008-4a2a-9637-471485c4187a" />

페이지 사용 권한 업데이트 확인

<img width="1304" height="278" alt="키 확인" src="https://github.com/user-attachments/assets/166b9db8-e0eb-42e2-95c5-8decc80a73a3" />

키 확인 및 복사 

---

# 클로드 MCP 설정

<img width="481" height="137" alt="simithery" src="https://github.com/user-attachments/assets/770f3bf0-d13f-45bc-b932-656fb95fa8c6" />


**https://smithery.ai/** 접속

<img width="878" height="250" alt="notion검색" src="https://github.com/user-attachments/assets/68430f90-b0a2-4c2b-a325-f87c8bec925a" />

**notion** 검색

<img width="436" height="196" alt="notion다운로드" src="https://github.com/user-attachments/assets/282d3811-25ec-4a81-a8cc-557948ec2b56" />

클릭

<img width="502" height="491" alt="mcpnotion연결" src="https://github.com/user-attachments/assets/ed9b5b32-e979-49d1-8880-e9ecc9c6b878" />

노션 api 키 입력

<img width="506" height="576" alt="mcpjson받기" src="https://github.com/user-attachments/assets/de67371f-a204-4930-9ffc-007edb78eb33" />

JSON 파일 복사

<img width="288" height="193" alt="클로드설정이동" src="https://github.com/user-attachments/assets/1bd07c8a-6bb9-4547-b62e-14e954fab29f" />

클로드 > 설정

<img width="998" height="803" alt="구성편집" src="https://github.com/user-attachments/assets/871c04b3-8b90-46bf-9b9a-12ddf196c0b0" />

설정 > 개발자 > 구성편집

<img width="1129" height="615" alt="구성편집2" src="https://github.com/user-attachments/assets/0c22319d-8495-443d-95a2-f7b0bd93dfa7" />

claude_desktop_config 파일 열기 

<img width="690" height="416" alt="구성편집3" src="https://github.com/user-attachments/assets/5986ab77-3529-49b7-9058-5bbee3867104" />

JSON 붙여넣기

<img width="302" height="181" alt="구성편집4 종료" src="https://github.com/user-attachments/assets/a19a388b-eb42-4313-ba56-57fd529698e2" />

클로드 재시작

<img width="996" height="794" alt="노션 커넥터 연결 " src="https://github.com/user-attachments/assets/4ce12baf-7260-4792-86ca-5f8e9e4a608b" />
<img width="1000" height="801" alt="노션 개발자 연결" src="https://github.com/user-attachments/assets/16ed98c3-ef8a-460d-94ed-627845011287" />


클로드 > 설정 > 노션MCP 확인 

<img width="624" height="135" alt="노션페이지아이디" src="https://github.com/user-attachments/assets/0103ba8e-230b-4a0f-810e-98425df9e155" />


작성할 노션 페이지 아이디 복사

<img width="717" height="279" alt="명령어입력" src="https://github.com/user-attachments/assets/687c438b-263d-499a-9048-b0382362b0e6" />

노션 페이지 아이디를 포함해서 명령 

<img width="986" height="791" alt="클로드답변" src="https://github.com/user-attachments/assets/300ac174-6403-4913-a44e-937d55f7a5e8" />
<img width="749" height="832" alt="노션잓어완료" src="https://github.com/user-attachments/assets/9d4ce389-155c-4072-b9e6-3b89b641b77d" />


작성된 결과물 확인 



