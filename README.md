# Hearts of Korea 하츠 오브 코리아 Anime

Hearts of Iron IV의 **하츠 오브 코리아**에 애니메이션풍 초상과 삽화, 한국군 음성을 더하는 서브모드입니다. 본체의 중점, 이벤트, 결정과 게임 규칙 위에 시청각 자산을 적용합니다.

## 포함 자산

초기 저장소 `81b5b22` 기준으로 DDS 188개와 WAV 20개를 포함합니다.

| 자산 | 저장소 경로 |
| --- | --- |
| 한국·일본 인물 초상 | `gfx/leaders/KOR/`, `gfx/leaders/JAP/` |
| 이벤트·뉴스 그림 | `gfx/event_pictures/` |
| 중점·국민정신·결정 아이콘 | `gfx/interface/goals/`, `gfx/interface/ideas/`, `gfx/interface/decisions/` |
| 한국군 유닛 음성 | `sound/kor/` |

## 설치와 호환성

1. 플레이할 하츠 오브 코리아 본체를 준비합니다. 이 저장소에서 대조한 본체는 `하츠 오브 코리아 Hearts of Korea[1.19 호환](씹덕 모드 제작자 개정)`이며 `Korean Language`를 의존성으로 선언합니다.
2. 로컬 개발본을 쓸 때는 Paradox Launcher에 이 저장소 폴더를 가리키는 모드 항목을 등록합니다. 본체와 **Hearts of Korea 하츠 오브 코리아 anime**를 같은 플레이세트에 넣고, 자산 교체를 확인할 때 본체 뒤에 서브모드를 배치합니다.
3. 적용 여부는 사용 중인 게임 버전과 본체 조합에서 초상·아이콘·음성을 직접 확인합니다. 로컬 소스 대조와 별개로 런처 로드 순서 및 실제 표시·재생 검증이 남아 있습니다.

현재 [서브모드 descriptor](descriptor.mod)는 HOI4 `1.12.*`를 선언하고, 본체 descriptor는 `1.19.*`를 선언합니다. 서브모드에는 기존 Hearts of Korea 이름, `Gookppong Generals`, 1.19 계승판, Road to 56 호환판 이름이 의존성으로 함께 기록되어 있습니다. 각 조합의 호환성은 미검증입니다.

서브모드의 `replace_path` 여섯 경로 중 중점·국민정신·결정·이벤트 그림 폴더에는 현재 본체에만 있는 파일이 있습니다. 해당 경로의 표시 누락 여부도 호환성 확인 항목입니다.

## 출처와 크레딧

- **하츠 오브 코리아 원작과 기여자** — 원작 Workshop `2898629778`. 현재 서브모드가 대조하는 본체는 계승판 `3793992662`입니다.
- **Hearts of Korea 하츠 오브 코리아 Anime** — 이 저장소의 [descriptor](descriptor.mod)에 기록된 Workshop ID는 `2905927886`입니다.
- **Anime History** — Workshop `1862018480`. 시각 스타일과 모드 구조를 살펴본 참고 프로젝트입니다. 현재 서브모드의 개별 그림·음성에 대한 원출처와 재배포 조건은 별도 확인이 필요합니다.

개발 작업 위치와 검증 범위는 [AGENTS.md](AGENTS.md)를 참고하세요.
