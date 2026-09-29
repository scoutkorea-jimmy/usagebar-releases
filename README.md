# Quotly · 쿼틀리

**AI 사용량과 Mac 상태를 메뉴바에서 한눈에.**

[Quotly V1.001.000 다운로드](https://github.com/scoutkorea-jimmy/usagebar-releases/releases/latest) · [짧은 주소](https://jimmypark.net/quotly) · [후원하기](https://www.paypal.com/ncp/payment/55YEQS4N76GH6)

Apple Silicon Mac · macOS 13 이상 · 한국어 / English

## 주요 기능

- **AI 사용량:** ChatGPT 구독의 Codex 한도와 Claude 한도를 사용률 또는 잔여량으로 표시합니다. 초기화까지 남은 시간, 갱신 시각, 서버에서 제공하는 크레딧·추가 한도를 확인할 수 있습니다.
- **사용량 알림:** 설정한 잔여량 기준을 한도 주기에서 처음 넘을 때 알립니다. 초기화 완료 알림과 방해금지 시간을 지원합니다.
- **공식 서비스 상태:** [Claude Status](https://status.claude.com/)와 [OpenAI Status](https://status.openai.com/)를 1분마다 확인합니다. 새 장애, 진행 상황 변경, 복구를 알려주고 같은 업데이트를 반복해서 알리지 않습니다.
- **기록·분석:** 사용량 추이, 충분한 관측이 있을 때의 소진 예상, 주간 요약을 제공합니다.
- **초기화 소식·쿠폰:** 공개 초기화 소식과 내 계정에서 확인되는 Codex 쿠폰 현황·이력을 보여줍니다. 쿠폰은 조건을 충족하고 사용자가 확인한 경우에만 사용합니다.
- **Mac 모니터링:** 네트워크 업로드·다운로드(Mbps), 선택한 드라이브의 읽기·쓰기(MB/s), 최근 10분 그래프를 확인합니다.
- **메뉴바 맞춤 설정:** 필요한 항목, 글자 크기, 간격, 드라이브를 선택할 수 있습니다.
- **앱 내 업데이트:** 서명된 업데이트 피드와 패키지를 확인하는 Sparkle 자동 업데이트를 지원합니다.

## 서비스 장애 알림 사용법

현황 상단의 **Claude / OpenAI 상태 줄**을 누르면 공식 서비스 상태와 최근 발표를 볼 수 있습니다. **설정 → 알림 → 공식 서비스 상태**에서 서비스별 알림을 켜거나 끌 수 있습니다. 전체 **알림 받기**와 macOS의 Quotly 알림 권한도 켜져 있어야 배너가 표시됩니다.

- 처음 확인할 때 진행 중인 장애는 알리고, 이미 해결된 과거 사건은 알리지 않습니다.
- 같은 업데이트는 앱을 다시 실행해도 반복하지 않습니다. 방해금지 중에 지나간 알림을 나중에 몰아서 보내지 않습니다.
- 앱 실행 중 확인하며, 잠자기·오프라인·일시정지 중에는 조회를 멈춥니다. 조회 실패 시 이전 결과와 확인 지연을 표시하고 재시도 간격을 늘립니다.
- Claude 조회 오류 또는 공식 장애 중에는 메뉴바에 마지막 퍼센트를 표시하지 않고 `C 장애` 또는 `C 조회 오류`로 표시합니다. 복구 후 새 사용량을 받아오면 다시 표시합니다.
- 공식 발표 제목·본문은 원문으로 표시합니다. 서비스 전체 상태이므로 내 계정의 접속 가능 여부나 사용 한도를 보장하지 않습니다.

## 설치와 계정 연결

1. 위 다운로드 링크에서 **Quotly-V1.001.000.zip**을 받습니다.
2. 압축을 풀고 **Quotly.app**을 응용 프로그램 폴더로 옮깁니다.
3. 앱의 **설정 → 계정**에서 본인의 계정을 연결합니다.

Claude는 본인 로그인 세션을 사용합니다. ChatGPT 항목은 **Codex 구독 한도**이며, 일반 ChatGPT 대화의 메시지 잔여 횟수는 지원하지 않습니다. Codex 연결에는 지원되는 로컬 Codex 설치와 로그인 환경이 필요합니다. 공식 상태 조회에는 계정 로그인이 필요하지 않습니다.

이 앱은 현재 로컬 ad-hoc 서명을 사용하며 Apple Developer ID 서명·공증은 적용되지 않았습니다. macOS의 보안 정책에 따라 실행이 제한될 수 있습니다. Intel Mac은 현재 배포 대상이 아닙니다.

이후 업데이트는 앱에서 확인하거나 자동으로 받을 수 있습니다. `.delta`는 기존 버전용 부분 업데이트 파일이므로 직접 설치할 필요가 없습니다. 버전은 **Va.bbb.ccc** 형식입니다. `a`는 제작자가 직접 결정하는 큰 버전, `bbb`는 주요 기능 추가, `ccc`는 버그 수정입니다. 이번 버전은 **V1.001.000**입니다. 업데이트는 중간 버전을 설치할 필요 없이 최신 버전으로 바로 이동합니다.

## English

**Quotly puts AI usage and Mac activity in your menu bar.** Requires Apple Silicon and macOS 13 or later. Korean and English interfaces are available.

- View used or remaining **Codex subscription limits** and Claude usage, reset countdowns, server-reported credits and additional limits.
- Receive first-crossing quota alerts, reset alerts, and official **Claude / OpenAI incident updates** checked every minute.
- Open the status row on Overview for active incidents and recent official updates. Configure each provider under **Settings → Notifications → Official service status**. Enable the app's main notifications switch and macOS notification permission for banners.
- Existing active incidents are announced on first check; historical resolved incidents are not. Identical updates are deduplicated across restarts. Quiet-hour events are not replayed later.
- Polling stops during sleep, offline periods and app pause. Failed checks retain the last result with a stale indication and use retry backoff. Incident text remains in its original language.
- Explore usage history, forecasts when sufficient observations exist, reset news, and eligible Codex reset coupons. Coupon redemption always requires confirmation.
- Monitor network throughput in Mbps, selected-drive I/O in MB/s and recent graphs. Customize visible menu-bar items and sizing.

Download **Quotly-V1.001.000.zip** from [the latest release](https://github.com/scoutkorea-jimmy/usagebar-releases/releases/latest), move Quotly.app to Applications, then connect your own accounts. Regular ChatGPT conversation message counts are not supported. A supported local Codex installation and sign-in are required for Codex usage. Public service-status checks need no account.

The current build is ad-hoc signed, not Apple Developer ID signed or notarized. In-app updates use HTTPS and Ed25519 signatures for the feed and payloads. Updates jump directly to the latest version; intermediate versions are not required. Version format: Va.bbb.ccc (owner-controlled major / feature / fix). Optional `.delta` files are for automatic updates, not manual installation.

## 배포 저장소 / Distribution repository

이 저장소는 앱 배포 파일, 안내 문서와 서명된 업데이트 피드만 제공합니다. **앱 소스 코드, 로그인 정보, 사용자 설정, 서명 개인키는 포함하지 않습니다.** GitHub가 자동으로 표시하는 `Source code` 압축 파일은 이 배포 저장소의 문서·피드 사본이며 앱 소스가 아닙니다.

This repository distributes app binaries, documentation and the signed update feed. It contains no application source code, account sessions, user preferences or signing private keys. GitHub's automatically generated source archives contain only this distribution repository's documents and feed.
