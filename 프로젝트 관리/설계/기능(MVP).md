---
cssclasses:
  - table
tags:
  - 설계
---
## 기본 대시보드 기능(MVP)
### UI에 항상 표시되는 정보
<table>
    <thead>
        <tr>
             <th>기능</th>
             <th>설명</th>
        </tr>
    </thead>

	<tbody>
	    <tr>
		    <th scope="row">시간</th>
			<td>UI에 현재 시간 상시 표시</td>
	    </tr>
	    <tr>
		    <th scope="row">날씨</th>
			<td>UI에 현재 닐씨 상시 표시</td>
	    </tr>
	    <tr>
		    <th scope="row">일정</th>
			<td>UI에 오늘의 일정 시간 상시 표시</td>
	    </tr>
	</tbody>
	
</table>


### AI 인터렉션 기능(음성 명령)
<table>
    <thead>
        <tr>
             <th>기능</th>
             <th>설명</th>
        </tr>
    </thead>

	<tbody>
	    <tr>
		    <th scope="row">Wake Word 감지</th>
			<td>"퍼비야" 호출 감지</td>
	    </tr>
	    <tr>
		    <th scope="row">음성 일정 제어</th>
			<td>음성으로 일정 추가/삭제/조회</td>
	    </tr>
	    <tr>
		    <th scope="row">음악 재생</th>
			<td>음성 명령으로 음악 재생</td>
	    </tr>
	    <tr>
		    <th scope="row">타이머</th>
			<td>타이머 설정</td>
	    </tr>
	    <tr>
		    <th scope="row">하루 일과에 대한 회고</th>
			<td>AI가 오늘 진행했던 주요 일정과 사용자와 나누었던 내화 내용을 정리해서 말해줌</td>
	    </tr>
	</tbody>
	
</table>

### 환경 반응형

<table>
    <thead>
        <tr>
             <th>기능</th>
             <th>설명</th>
        </tr>
    </thead>

	<tbody>
	    <tr>
		    <th scope="row">날씨 연동 UI</th>
			<td>날씨에 따라 배경과 캐릭터 UI가 변경</td>
	    </tr>
	    <tr>
		    <th scope="row">시간에 따른 배경 / 캐릭터 UI</th>
			<td>시간에 따라 배경과 캐릭터 UI가 변경</td>
	    </tr>
	</tbody>
	
</table>

### 상태 변화표
<table>
    <thead>
        <tr>
             <th>상태</th>
             <th>설명</th>
             <th>발생 조건</th>
             <th>UI 변화</th>
             <th>애니메이션</th>
        </tr>
    </thead>

	<tbody>
	    <tr>
		    <th scope="row" style="background-color:white; color:#55ABCB">Idle</th>
			<td>기본 대기 상태</td>
			<td>사용자 입력 없음</td>
			<td>캐릭터 중앙에 표시</td>
			<td>눈 깜빡임 / 가벼운 숨쉬기</td>
	    </tr>
	    <tr>
		    <th scope="row" style="background-color:white; color:#00FF8A">Listening</th>
			<td>음성 입력 대기</td>
			<td>Wake Word 감지 후</td>
			<td>캐릭터가 사용자 방향 집중</td>
			<td>귀 기울이는 동작 / 음성 파동 효과</td>
	    </tr>
	    <tr>
		    <th scope="row" style="background-color:white; color:#FDC12C">Thinking</th>
			<td>AI 처리 중</td>
			<td>STT -> AI 분석 중</td>
			<td>캐릭터 생각 표정</td>
			<td>생각 구름 / 로딩링</td>
	    </tr>
	    <tr>
		    <th scope="row" style="background-color:white; color:#9C96CC">Sleeping</th>
			<td>절전 모드</td>
			<td>사용자가 지정한 절전 모드 시간 동안</td>
			<td>화면 dim / 캐릭터 잠</td>
			<td>눈 감기 / Zzz 애니메이션</td>
	    </tr>
	    <tr>
		    <th scope="row" style="background-color:white; color:#29A2FF">Rain/Snow</th>
			<td>특정 날씨 상태</td>
			<td>날씨 API = Rain / Snow</td>
			<td>배경에 날씨에 맞는 애니메이션</td>
			<td>캐릭터 우산, 물방울, 눈 내리는 효과</td>
	    </tr>
	    <tr>
		    <th scope="row" style="background-color:white; color:#A96DE8">Night</th>
			<td>야간 모드 상태</td>
			<td>시간(예 : 22:00 ~ 06:00)</td>
			<td>배경 어두운 모드</td>
			<td>캐릭터 졸린 표정 / 별 애니메이션</td>
	    </tr>
	    <tr>
		    <th scope="row" style="background-color:white; color:#FF424C">Error</th>
			<td>명령 이해 실패</td>
			<td>AI가 명령 이해를 실패하거나 내부적으로 처리 오류가 발생했을 경우 </td>
			<td>캐릭터 당황 표정 / 오류 메시지</td>
			<td>머리 위 물음표 / 고개 갸웃</td>
	    </tr>
	</tbody>
	
</table>

### 모바일 연동
<table>
    <thead>
        <tr>
             <th>기능</th>
             <th>설명</th>
        </tr>
    </thead>

	<tbody>
	    <tr>
		    <th scope="row">모바일 연동</th>
			<td>모바일 앱과 메인서버 연결(첫 시작)</td>
	    </tr>
	    <tr>
		    <th scope="row">배경 설정</th>
			<td>배경 설정</td>
	    </tr>
	    <tr>
		    <th scope="row">절전 시간 설정</th>
			<td>예) 새벽 2시 ~ 새벽 6시</td>
	    </tr>
	</tbody>
	
</table>
