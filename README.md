# Quotly · 쿼틀리

**AI 사용량과 Mac 상태를 메뉴바에서 한눈에.**

[Quotly V1.008.004 다운로드](https://github.com/scoutkorea-jimmy/usagebar-releases/releases/latest) · [짧은 주소](https://jimmypark.net/quotly) · [후원하기](https://www.paypal.com/ncp/payment/55YEQS4N76GH6)

Apple Silicon Mac · macOS 13 이상 · 한국어 / English

상단 **톱니바퀴 설정 버튼**에서 메뉴바 표시 항목·갱신·알림·계정을 관리합니다. 하단 탐색은 **현황·모니터링** 두 화면으로 구성됩니다.

## 주요 기능

- **AI 사용량:** ChatGPT 구독의 Codex 한도와 Claude 한도를 사용률 또는 잔여량으로 표시합니다. 초기화까지 남은 시간, 갱신 시각, 서버에서 제공하는 크레딧·추가 한도를 확인할 수 있습니다.
- **이용 플랜:** 현황·상세·계정에서 서버가 제공하는 플랜명을 표시합니다. Claude는 확인된 다음 결제일을 표시하고, 날짜가 없으면 월간·연간 결제 주기만 표시합니다. 결제 정보를 받지 못하면 생략하며, 현재 ChatGPT 연동에는 결제 정보가 없습니다.
- **사용량 알림:** 설정한 잔여량 기준을 한도 주기에서 처음 넘을 때 알립니다. 초기화 완료 알림과 방해금지 시간을 지원합니다.
- **공식 서비스 상태:** [Claude Status](https://status.claude.com/)와 [OpenAI Status](https://status.openai.com/)를 1분마다 확인합니다. 새 장애, 진행 상황 변경, 복구를 알려주고 같은 업데이트를 반복해서 알리지 않습니다.
- **기록·분석:** 연속 기록은 계단형 선 그래프로, 단독 관측과 최신 값은 점으로 표시합니다. 조회 공백·초기화·재실행 구간은 연결하지 않습니다. 충분한 관측이 있을 때 소진 예상과 주간 요약을 제공합니다.
- **초기화 소식·쿠폰:** 공개 초기화 소식과 내 계정에서 확인되는 Codex 쿠폰 현황·이력을 보여줍니다. 쿠폰은 사용자가 직접 승인한 경우에만 요청합니다. 95% 미만에서도 사용할 수 있으며, 남은 한도와 쿠폰 소모에 관한 추가 확인이 필요합니다.
- **Mac 모니터링:** 네트워크 업로드·다운로드(Mbps), 선택한 드라이브의 읽기·쓰기(MB/s), 최근 10분 그래프를 확인합니다.
- **디스크 용량:** 메뉴바에서 선택한 드라이브의 사용 용량 또는 잔여 용량 / 전체 용량과 해당 비율을 표시합니다. 볼륨 기준으로 1분마다 갱신하며, 설정 → 메뉴바에서 용량 숫자·전체 용량(분모)·퍼센트를 각각 선택합니다. 메뉴바에는 사용량/잔여량 배지가 붙습니다. 자주 쓰는 숫자+비율/숫자만/비율만 선택을 먼저 보여주고, 숫자·분모·퍼센트 개별 옵션과 독립 기준은 ‘세부 표시 조정’에 접어 둡니다.
- **메뉴바 맞춤 설정:** 필요한 항목, 글자 크기, 간격, 드라이브를 선택할 수 있습니다.
- **앱 내 업데이트:** 서명된 업데이트 피드와 패키지를 확인하는 Sparkle 자동 업데이트를 지원합니다.

## 서비스 장애 알림 사용법

현황 상단의 **Claude / OpenAI 상태 줄**을 누르면 공식 서비스 상태와 최근 발표를 볼 수 있습니다. **설정 → 알림 → 공식 서비스 상태**에서 서비스별 알림을 켜거나 끌 수 있습니다. 전체 **알림 받기**와 macOS의 Quotly 알림 권한도 켜져 있어야 배너가 표시됩니다.

- 처음 확인할 때 진행 중인 장애는 알리고, 이미 해결된 과거 사건은 알리지 않습니다.
- 같은 업데이트는 앱을 다시 실행해도 반복하지 않습니다. 방해금지 중에 지나간 알림을 나중에 몰아서 보내지 않습니다.
- 앱 실행 중 확인하며, 잠자기·오프라인·일시정지 중에는 조회를 멈춥니다. 조회 실패 시 이전 결과와 확인 지연을 표시하고 재시도 간격을 늘립니다.
- Claude 조회 오류 또는 공식 장애 중에는 메뉴바에 마지막 퍼센트를 표시하지 않고 `C 장애` 또는 `C 조회 오류`로 표시합니다. 복구 후 새 사용량을 받아오면 다시 표시합니다.
- 공식 발표 제목·본문은 원문으로 표시합니다. 서비스 전체 상태이므로 내 계정의 접속 가능 여부나 사용 한도를 보장하지 않습니다.

## 웹 사용량과 비교할 때

같은 계정·한도·표시 기준으로 양쪽을 새로고침해서 비교하세요. 예를 들어 웹의 **잔여 5%**는 앱의 **사용 95%**와 같습니다. 세션 한도와 주간 한도는 서로 다른 값이며, 메뉴바는 선택한 한도를 표시합니다. 서비스 웹페이지와 앱의 갱신 시각 차이로 잠시 다른 수치가 보일 수 있습니다.

## 설치와 계정 연결

1. 위 다운로드 링크에서 **Quotly-V1.008.004.zip**을 받습니다.
2. 압축을 풀고 **Quotly.app**을 응용 프로그램 폴더로 옮깁니다.
3. 앱의 **설정 → 연결 → 관리**에서 본인의 계정을 연결합니다.

**Claude:** CLI나 Claude 앱을 설치할 필요가 없습니다. Quotly의 **Claude 로그인** 창에서 본인 계정으로 로그인한 뒤 앱에서 새로고침하세요.

**ChatGPT · Codex:** 최신 ChatGPT 데스크톱 앱에 포함된 Codex와 OpenAI 서명이 확인되는 기존 Codex 실행 파일을 자동으로 찾습니다. 서명이 없거나 변조된 CLI·실행 파일은 실행하지 않습니다. 연결 화면에 찾은 도구가 표시됩니다. 로그인 완료 후에는 사용량과 연결됨 상태를 표시하고 연결 관리는 접어둡니다. 로그아웃은 연결 관리를 펼쳐 실행할 수 있습니다. 브라우저·터미널 로그인 결과가 반영되지 않으면 ‘로그인 결과 다시 확인’을 누르세요. 실행 파일이 없으면 **ChatGPT 데스크톱 설치하기 → 응용 프로그램 폴더로 이동 → 설치 확인 → ChatGPT 로그인** 순서로 연결하세요. Codex가 포함된 앱이 있으면 CLI를 따로 설치할 필요가 없습니다. 이전 대화 전용 ChatGPT 앱이나 웹 로그인만으로는 연결되지 않습니다.

ChatGPT 항목은 **Codex 구독 한도**이며, 일반 ChatGPT 대화의 메시지 잔여 횟수는 지원하지 않습니다. Codex 연결에는 지원되는 로컬 Codex 설치와 로그인 환경이 필요합니다. 공식 상태 조회에는 계정 로그인이 필요하지 않습니다.

이 앱은 현재 로컬 ad-hoc 서명을 사용하며 Apple Developer ID 서명·공증은 적용되지 않았습니다. macOS의 보안 정책에 따라 실행이 제한될 수 있습니다. Intel Mac은 현재 배포 대상이 아닙니다.

이후 업데이트는 앱에서 확인하거나 자동으로 받을 수 있습니다. `.delta`는 기존 버전용 부분 업데이트 파일이므로 직접 설치할 필요가 없습니다. 버전은 **Va.bbb.ccc** 형식입니다. `a`는 제작자가 직접 결정하는 큰 버전, `bbb`는 주요 기능 추가, `ccc`는 버그 수정입니다. 이번 버전은 **V1.008.004**입니다. 업데이트는 중간 버전을 설치할 필요 없이 최신 버전으로 바로 이동합니다.

## 로그인 보안

- Claude 로그인 창은 Claude·Google·Apple의 지정된 HTTPS 로그인 주소만 허용합니다. 실제 접속 중인 호스트를 창 제목에 표시하며, 알 수 없는 기업 SSO 주소는 현재 지원하지 않습니다.
- ChatGPT Codex는 OpenAI 서명이 확인되는 실행 파일만 사용합니다. Quotly에서 실행하는 사용량 조회는 공식 ChatGPT 주소로 고정하며, 사용자의 Codex 설정 파일은 변경하지 않습니다.
- 사용 기록·상태 기록은 사용자 전용 접근 권한으로 저장합니다. 진단 보고에는 비밀번호·인증 토큰·이메일·대화·원본 오류 응답을 넣지 않습니다.
- Quotly가 비밀번호를 직접 수집하거나 저장하지는 않지만, Claude 로그인 세션은 이 Mac의 WebKit 저장소에 유지되고 Codex 인증은 공식 Codex가 관리합니다. 감염된 Mac 또는 같은 사용자 권한의 악성 프로그램에 대한 완전한 보호를 보장하지 않습니다.
- 현재 Apple Developer ID 서명·공증은 없습니다. 업데이트 피드·배포 패키지의 Ed25519 서명 검증은 유지합니다.

## 글꼴

앱 화면과 메뉴바는 엘리스 디지털 배움체 Regular·Bold를 사용합니다. 원본 폰트와 [제작사 라이선스](https://cdn-front-door.elice.io/font/static/downloads/EliceDigitalBaeum_License.pdf)를 앱에 포함하며, 별도 폰트 설치는 필요하지 않습니다. macOS 시스템 대화상자와 서비스 로그인 웹페이지는 해당 환경의 글꼴을 유지합니다.

## 개발 후원 · 불편 접수

설정의 앱 관리 화면 상단에서 [PayPal로 개발 후원](https://www.paypal.com/ncp/payment/55YEQS4N76GH6)을 할 수 있습니다. 후원은 선택이며 모든 기능을 그대로 사용할 수 있습니다.

오류나 개선 의견은 **scoutkorea@kakao.com**으로 보내주세요. 앱의 **불편 접수 메일 쓰기** 버튼은 메일 작성 창만 열며 자동 전송하거나 진단 정보를 첨부하지 않습니다.

## English

**Quotly puts AI usage and Mac activity in your menu bar.** Requires Apple Silicon and macOS 13 or later. Korean and English interfaces are available.

- View recognized server-reported plan names in Overview, details and account settings. Claude shows an explicit next payment date, falling back to a confirmed monthly/annual cycle. Missing billing details are omitted; the current ChatGPT integration supplies none.
- View used or remaining **Codex subscription limits** and Claude usage, reset countdowns, server-reported credits and additional limits.
- Receive first-crossing quota alerts, reset alerts, and official **Claude / OpenAI incident updates** checked every minute.
- Open the status row on Overview for active incidents and recent official updates. Configure each provider under **Settings → Notifications → Official service status**. Enable the app's main notifications switch and macOS notification permission for banners.
- Existing active incidents are announced on first check; historical resolved incidents are not. Identical updates are deduplicated across restarts. Quiet-hour events are not replayed later.
- Polling stops during sleep, offline periods and app pause. Failed checks retain the last result with a stale indication and use retry backoff. Incident text remains in its original language.
- Explore usage history as continuous stepped lines, with dots only for isolated observations and the latest value. Observation gaps remain disconnected. View forecasts when sufficient observations exist, reset news, and eligible Codex reset coupons. Coupon redemption always requires confirmation.
- Monitor network throughput in Mbps, selected-drive I/O in MB/s and recent graphs. Customize visible menu-bar items and sizing.

When comparing with the service website, refresh both views and match the account, quota window and used/remaining mode. For example, 5% remaining equals 95% used. Refresh timing can temporarily differ.

Download **Quotly-V1.008.004.zip** from [the latest release](https://github.com/scoutkorea-jimmy/usagebar-releases/releases/latest), move Quotly.app to Applications, then connect your own accounts. Regular ChatGPT conversation message counts are not supported. For Codex usage, Quotly accepts Codex bundled with the current ChatGPT desktop app or an existing native helper with a valid OpenAI signature. Unsigned wrappers and modified helpers are not executed. The connection screen shows the detected helper. If none is found, install the current ChatGPT desktop app in Applications, select Check installation, then sign in. A separate CLI is not required when the app bundles Codex; older chat-only apps and web sign-in alone are insufficient. Claude needs neither a CLI nor a separate app: sign in through Quotly’s Claude window. Public service-status checks need no account.

The current build is ad-hoc signed, not Apple Developer ID signed or notarized. In-app updates use HTTPS and Ed25519 signatures for the feed and payloads. Updates jump directly to the latest version; intermediate versions are not required. Version format: Va.bbb.ccc (owner-controlled major / feature / fix). Optional `.delta` files are for automatic updates, not manual installation.

Claude sign-in windows accept only designated HTTPS Claude, Google and Apple hosts and show the current host in the native title. Unknown enterprise SSO providers are currently blocked. Codex helpers require a valid OpenAI signature; usage requests pin the official ChatGPT base URL without changing your Codex config. History and status files use owner-only permissions. Quotly does not collect passwords directly; Claude sessions persist in this Mac's WebKit store and Codex manages its own credentials. This does not guarantee protection against malware running as your OS user or a compromised Mac.

Feedback: **scoutkorea@kakao.com**. App management settings include a prominent PayPal support button and an email-composer button. Support is optional; feedback is never sent automatically.

App-owned UI and menu-bar text use bundled Elice Digital Baeum Regular/Bold. Original font files and license are included; system dialogs and service login pages keep their native typography.

## 배포 저장소 / Distribution repository

이 저장소는 앱 배포 파일, 안내 문서와 서명된 업데이트 피드만 제공합니다. **앱 소스 코드, 로그인 정보, 사용자 설정, 서명 개인키는 포함하지 않습니다.** GitHub가 자동으로 표시하는 `Source code` 압축 파일은 이 배포 저장소의 문서·피드 사본이며 앱 소스가 아닙니다.

This repository distributes app binaries, documentation and the signed update feed. It contains no application source code, account sessions, user preferences or signing private keys. GitHub's automatically generated source archives contain only this distribution repository's documents and feed.

### 오류 보고 / Report an issue
설정 → 앱 또는 하단 더 보기 → 오류 보고에서 진단 내용을 미리 보고 메일 작성·복사할 수 있습니다. 자동 전송하지 않습니다. 계정·토큰·대화·경로·원본 오류 응답은 제외됩니다.

Open Settings → App or More → Report an issue to preview and copy diagnostics or compose an email. Reports are never sent automatically.

### 작은 모니터링 창 / Mini monitor
하단 더 보기 → 작은 모니터링 창 또는 설정 → 작은 창에서 열 수 있습니다. 메뉴바와 같은 데이터를 사용하고 표시 항목은 별도로 선택하며 핀 버튼으로 항상 위 표시를 전환합니다. 위치·크기를 기억하고 창을 닫아도 기존 모니터링은 계속됩니다.

Open Mini monitor from More or Settings → Mini window. It shares menu-bar data without extra polling; pin it above regular windows and reopen it at its saved position and size.

작은 창은 AI 사용량 원형 차트와 네트워크·디스크의 최근 10분 추이 그래프를 표시합니다. 기존 측정 기록을 재사용하며 측정이 끊긴 구간을 연결하지 않습니다.

The mini window shows AI usage rings and the last ten minutes of network/disk charts, reusing existing measurements and preserving gaps.

설정 → 작은 창에서 ChatGPT Codex와 Claude의 차트 한도를 각각 선택합니다. 서버가 제공하지 않는 세션·주간 한도는 표시하지 않습니다.

### 앱 색상 / Appearance
설정 → 앱 → 앱 색상에서 시스템·라이트·다크 화면 모드와 강조색을 선택할 수 있습니다. 작은 모니터링 창도 같은 색상을 사용합니다.
Choose system, light or dark appearance and an accent color in Settings → App. The mini monitor shares the same appearance.

작은 창은 설정 → 작은 창에서 표시 항목과 원형 차트의 한도를 고릅니다. 강조색은 10가지 견본 또는 사용자 지정 색상을 지원합니다.
Mini window contents and ring quotas have their own settings. Ten accent swatches and a custom color picker are available.

Disk capacity: show used or free space / total volume capacity and the matching percentage for the menu bar drive. Configure numbers, total capacity, percentage and separate used/free modes in Settings → Menu bar. Refreshes every minute in the background.
