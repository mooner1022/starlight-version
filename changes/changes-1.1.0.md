### 주요 변경 사항
+ **카카오톡 26.7.0 이상** 대응
  + 카카오톡 26.7.0부터 알림에서 채팅방 이름이 빠져, 방 이름 대신 보낸 사람의 이름이 전달되고 그룹 채팅방도 1:1 채팅으로 처리되던 문제 수정
  + 메세지 변환/분석 스펙 `kakao_26_7` 추가, 규칙 자동 설정이 카카오톡 버전에 맞는 스펙을 선택
  + StarLight가 켜져 있는 동안 카카오톡이 업데이트되어도 다음 메세지부터 맞는 스펙으로 전환
+ **StarLight AI 문서** 개편
  + 스크립트 API, 타입, 이벤트 문서를 코드에서 만들어, AI가 실제 동작과 같은 문서를 참고
  + 플러그인이 함께 제공하는 문서와 가이드도 참고
  + 개발자 모드에 AI가 참고하는 문서를 그대로 볼 수 있는 'StarLight AI 문서' 화면 추가
+ **StarLight AI 작업** 안정성 개선
  + 작업 도중 앱이 종료되거나 멈춘 대화에서 이후 요청이 계속 실패하던 문제 수정
  + AI가 시작한 컴파일에 제한 시간 추가 (기본 60초, 프로젝트 설정의 'AI 컴파일 제한 시간 (초)')
  + 한 프로젝트는 누가 시작하든 한 번에 하나씩만 컴파일

### 버그 수정 / 개선 사항
+ NeonJS 프로젝트에서 `Api.UIThread`를 쓰면 앱이 응답하지 않던(ANR) 문제 수정
+ 여러 칸 떨어진 탭을 눌렀을 때 선택된 탭과 다른 화면이 표시될 수 있던 문제 수정
+ 메세지 변환/분석 스펙이 앱이나 안드로이드 버전과 맞지 않을 때 메세지를 받을 때마다 앱이 종료되던 문제 수정
+ 문제 해결 도우미가 규칙 자동 설정이 켜져 있어도 쓰이지 않는 저장된 규칙을 검사하던 문제 수정
+ `Device.acquireWakeLock`/`releaseWakeLock`: 해제되었거나 시간이 지난 wake lock 때문에 앱을 다시 시작할 때까지 이후 호출이 실패하던 문제 수정
+ `Notification`: `build()`를 호출할 때만 알림을 게시하고, 제목이나 내용이 빠졌으면 알려 줌
+ `Bridge.getScopeOf`를 컴파일되지 않은 프로젝트에 쓰거나 `Env`에 값을 대입할 때 알아보기 쉬운 오류 표시
+ 플러그인의 `isEnabled()`가 실제 상태를 반환, 플러그인이 켜지는 중에 추가한 리스너도 동작하고 플러그인을 내리면 리스너도 꺼짐
+ StarLight의 `onMessage`도 받는 프로젝트에서 시작 코드의 API2 리스너가 Rhino에서 두 번 호출되던 문제 수정 (`onApi2Message` 등으로 이름을 구분)

### 호환성 / 주의 사항
+ 카카오톡 26.7.0 이상의 방 이름은 Android 11 이상에서만 읽을 수 있습니다. Android 10 이하에서는 방 이름 대신 보낸 사람의 이름이 전달됩니다.
+ 규칙 자동 설정을 끄고 `android_r` 스펙을 직접 지정해 두었다면, 카카오톡 26.7.0 이상에서는 `kakao_26_7`로 바꿔야 방 이름을 읽습니다.

### 개발자 변경 사항
+ PluginCore 1.1.0
+ `MessageParserSpec.parse`에 알림의 `RankingMap`을 함께 받는 형태 추가 (기존 형태를 구현한 스펙은 그대로 동작)
+ `ProjectInfoBuilder.allowedEventIds`, `ProjectEvent.scriptArguments`·`listenerName`·`alternateFunctionName`·`generateCode(CodeGenerator, String)`, 받을 이벤트를 함께 받는 `Language.formatDefaultCode` 추가
+ PluginCore가 각 API가 추가된 버전을 기록 (`starlight/plugincore-api.json`), StarLight Gradle 플러그인이 이를 읽어 플러그인의 `api_version`을 계산
+ 새 버전에서만 실행되는 플러그인 코드를 표시하는 `@RequiresPluginCore` 추가
+ 플러그인 패키지에 StarLight AI가 참고할 문서(`starlight/agent/<플러그인 ID>.api.json`)와 가이드(`assets/agent/guides`) 포함 가능
