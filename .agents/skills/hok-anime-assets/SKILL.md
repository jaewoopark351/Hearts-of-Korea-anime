---
name: hok-anime-assets
description: Hearts of Korea Anime의 초상화, 뉴스·사건 삽화, UI 아이콘, 한국군 음성을 교체하거나 표시·재생 오류를 추적할 때 사용한다. 초상화와 뉴스·사건 삽화는 블루 아카이브 그림을 주로 사용하며, 본체 호출처에서 DDS·WAV까지 추적해 덮어쓰기 범위와 출처를 확인한다.
---

# Hearts of Korea Anime 자산 교체

작업 위치와 권한은 [AGENTS.md](../../../AGENTS.md)를 따른다. 검토나 문서 요청에서는 매핑과 근거를 기록하는 단계까지 진행한다. 파일 변경과 실행은 각각 허용된 범위에서 수행한다.

## 사용처에서 실제 파일까지 추적

1. 본체에서 대상의 ID와 표시·재생 상황을 찾는다. 호출부 → 스프라이트 또는 음성 ID → 정의 → 실제 파일 순으로 추적한다. 같은 상대 경로의 본체·서브모드 파일을 대조하고 해당 파일을 공유하는 호출처를 함께 찾는다.
2. 초상화와 뉴스·사건 삽화에는 블루 아카이브 그림을 우선 사용한다. 본체에서 해당 인물이 맡는 역할이나 사건 장면에 맞춰 그림을 고른다. 공식 일러스트, 게임 내 이미지, 팬아트 등 출처를 구분하고 원본 링크와 제작자를 기록한다.
3. 호출처에서 요구하는 크기, 형식, 알파·프레임 또는 WAV 채널·샘플레이트·비트 깊이를 확인한다. 이름이 비슷한 파일은 대소문자까지 대조한다. 같은 인물의 대형 초상과 소형 아이콘, 중점의 기본 아이콘과 광택 마스크, 결정 행과 범주 헤더는 각각의 경로와 표시 규격을 확인한다.
4. 실제 호출처에 맞는 교체 경로를 정한다. 현재 참조를 유지해 같은 상대 경로로 교체할 수 있으면 그 범위를 우선 검토한다. 참조 공유 때문에 한 화면만 바꿔야 할 경우에는 새 자산 경로가 필요한지 판단하고 요청 범위의 호출처만 조정한다.

### 본체에서 확인된 예

| 대상 | 추적 경로 |
| --- | --- |
| 인물 초상 | `common/characters/KOR.txt`의 `KOR_Beomseok_Lee` → `interface/characters_HoK.gfx`의 대형·소형 스프라이트 → `gfx/leaders/KOR/Portrait_KOR_Beomseok_Lee.dds`와 `gfx/interface/ideas/idea_KOR_beomseok_lee.dds` |
| 이벤트 그림과 초상 | `events/korea.txt`의 `GFX_report_event_kor_intro` → `interface/eventpictures_HoK.gfx` → `gfx/event_pictures/report_event_kor_intro.dds`. 같은 이벤트 파일에서 `Portrait_KOR_Teul_Eo_Kim.dds`를 경로로 직접 참조하는 사례도 있다. |
| 한국군 음성 | `sound/voice_korea.asset`의 효과 → `sound` ID → `sound/kor/*.wav`. 예를 들어 `kor_Idle_006` ID의 파일은 `kor_Idle_003.wav`다. 서브모드에 들어 있는 `kor_Idle_006.wav`와 `kor_Neutral_005.wav`는 확인한 본체 매핑에서 직접 참조되지 않는다. |

일반 장군·제독 초상은 본체 `portraits/00_portraits_KOR.txt`와 `interface/random_portraits_HoK.gfx`도 확인한다. 일본 인물이나 다른 본체 모듈의 그림을 교체할 때도 해당 캐릭터·이벤트의 실제 연결을 같은 방식으로 추적한다.

## 덮어쓰기 범위와 증거

- `descriptor.mod`의 `replace_path` 아래에서 본체에만 있는 파일을 찾고, 대체 파일이 없는 경로의 화면·음성 영향도 확인 대상으로 잡는다. 서브모드 `81b5b22`와 본체 `e2009b6`의 2026-11-11 작업 트리를 대조했을 때 중점 파일 8개가 같은 경로에 있었고, 본체에만 있는 경로가 301개 더 있었다. 본체의 `gfx/interface/goals/HOK_KOR/link_power_grids.dds`가 그 예다. 정적 차이는 누락 가능성을 보여 준다. 실제 적용 결과는 플레이세트에서 확인한다.
- Anime History의 DDS·WAV 구조, `sound/vo.asset` 매핑, 메뉴 GUI는 접근 방식이 필요할 때 참고한다. 참고본의 descriptor에는 `replace_path`와 의존성 선언이 없다. 대상이 HOK 인물·음성이면 실제 파일명과 호출처의 기준은 HOK 본체다. 참고본의 설치 경로와 자산의 배포 근거를 별개로 확인한다.
- 결과에는 대상 ID·화면 또는 음성 효과, 본체 호출부, 기존과 신규 파일 경로, 공유 호출처, 출처·가공 내용, 검증 상태를 남긴다. 실행이 허용되면 본체 기준과 본체+서브모드 조합을 같은 조건에서 비교하고, 대상 표시·재생과 인접 자산 누락 여부를 확인한다. 실제 선택된 모드 복사본, 로드 순서, 실행 결과 및 로그를 소스 대조 결과와 구분한다.
