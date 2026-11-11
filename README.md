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

2026-11-11에 교체한 뉴스 삽화는 《블루 아카이브》 캐릭터와 본체의 사건 설명을 바탕으로 OpenAI ImageGen에서 생성했습니다. 그림은 가로 구도에 맞춰 잘라낸 뒤 397×153 DDS로 변환했습니다.

| 뉴스 | 그림과 연결 | 장면 |
| --- | --- | --- |
| 도쿄 함락 (`newsk.5`) | [newsk_event_010.dds](gfx/event_pictures/newsk_event_010.dds) · `GFX_newsk_event_010` | 고쿄 돌다리 앞에서 가면을 벗고 태극기를 든 와카모 |
| 신징 함락 (`newsk.18`) | [newsk_event_011.dds](gfx/event_pictures/newsk_event_011.dds) · `GFX_newsk_event_011` | 중국풍 건물 위로 보이는 기존 삽화의 헬리콥터와 흰 로봇 |
| 난징 함락 (`newsk.23`) | [newsk_event_002.dds](gfx/event_pictures/newsk_event_002.dds) · `GFX_newsk_event_002` | 새벽의 중산문 앞 히나와 아코 |
| 베이핑 함락 (`newsk.22`) | [newsk_event_018.dds](gfx/event_pictures/newsk_event_018.dds) · `GFX_newsk_event_018` | 천안문 앞 유우카와 노아, 여성 의장대 |

난징 삽화의 아코는 2026-11-11에 [《블루 아카이브 The Animation》 공식 아코 설정화](https://sh-anime.shochiku.co.jp/bluearchive-anime/character/amau-ako/)의 얼굴, 머리 장식과 헤일로를 참고해 ImageGen으로 다시 그렸습니다. 설정화는 제작 참고 자료로 사용했습니다.

도쿄는 [와카모 공식 소개](https://x.com/Blue_ArchiveJP/status/1484752717839237121)와 [일본 궁내청 고쿄 안내](https://sankan.kunaicho.go.jp/english/guide/koukyo.html)를 참고했습니다. 후속 편집에서는 [NEONMAX의 와카모 피규어 사진](https://www.neonmax.net/wakamo)과 [행정안전부 태극기 도안](https://www.mois.go.kr/frt/sub/a06/b08/nationalIcon_2_2/screen.do)을 참고해 얼굴과 깃발을 그렸습니다.

신징은 사용자가 첨부한 기존 서브모드 삽화를 바탕으로, ImageGen에서 중국풍 건물을 그려 배경 건물 영역에 적용했습니다. 기존 그림의 개별 원출처는 미확인입니다.

삽화는 기존 경로를 사용합니다. 도쿄와 신징은 본체와 같은 비압축 32비트 DDS입니다. 네 삽화의 이벤트 연결과 DDS 형식을 확인했습니다. 게임 버전 `1.19.4.2.2da5`에서 신징의 표시를 확인했으며, 도쿄·베이핑·난징의 게임 내 표시는 미검증입니다.

### 지도자 중점 아이콘

2026-11-12에 기존 방패의 형태와 색을 참고해 중점 아이콘 네 장을 OpenAI ImageGen으로 다시 그렸습니다. 캐릭터의 머리, 복장, 장식은 《블루 아카이브》 일본 공식 소개 그림을 참고했습니다. 이전 아이콘의 개별 제작 출처는 미확인입니다.

| 중점 | 캐릭터 참고 자료 | 아이콘 |
| --- | --- | --- |
| 여운형 주석 (`KOR_yeo_woon_hyung_as_the_leader`) | [노도카 공식 소개](https://x.com/Blue_ArchiveJP/status/1386530752360173571) | [focus_kor_korea_yeo_woon_hyung_as_the_leader.dds](gfx/interface/goals/focus_kor_korea_yeo_woon_hyung_as_the_leader.dds) |
| 박헌영 주석 (`KOR_park_heon_young_as_the_leader`) | [토모에 공식 소개](https://x.com/Blue_ArchiveJP/status/1463704456760299520) | [focus_kor_korea_park_heon_young_as_the_leader.dds](gfx/interface/goals/focus_kor_korea_park_heon_young_as_the_leader.dds) |
| 김구 대통령 (`KOR_president_kim_gu`) | [나기사 공식 소개](https://x.com/Blue_ArchiveJP/status/1627503590750433283) | [focus_kor_president_kim_gu.dds](gfx/interface/goals/focus_kor_president_kim_gu.dds) |
| 이승만 재선 (`KOR_syngman_rhee_reelected`) | [미카 공식 소개](https://x.com/Blue_ArchiveJP/status/1398851690242088960) | [focus_kor_syngman_rhee_reelected.dds](gfx/interface/goals/focus_kor_syngman_rhee_reelected.dds) |

후속 편집에서 노도카와 토모에의 모자를 벗기고 가려졌던 머리 부분을 다시 그렸습니다.
토모에는 사용자가 첨부한 그림을 참고해 머리와 어깨의 비율, 고개 각도와 웃는 표정을 다시 그렸습니다. 첨부 그림의 개별 제작 출처는 미확인입니다.

본체와 같은 100×88 비압축 32비트 DDS로 변환해 테두리의 반투명 픽셀을 보존했습니다. 각 중점의 기본 그림과 광택 마스크가 같은 DDS를 참조하는 것을 확인했고, 최종 파일을 원본 크기로 열어 확인했습니다. 게임 내 표시는 미검증입니다.

### 대한제국 분기 중점 아이콘

2026-11-12에 본체와 서브모드의 기존 문장을 참고해 세 장을 OpenAI ImageGen으로 다시 그렸습니다. 화해 아이콘은 왼쪽부터 린·나기사·노도카를 배치했습니다. 린의 복장과 얼굴은 [공식 소개](https://x.com/Blue_ArchiveJP/status/1356074850909999105)를 참고했고, 나기사와 노도카는 위에 기록한 공식 소개 그림을 참고했습니다. 계연수 두 장은 [유우카 공식 소개](https://x.com/Blue_ArchiveJP/status/1353175798992179200)와 [서브모드의 기존 계연수 초상](gfx/leaders/KOR/Portrait_KOR_Yeonsu_Gye.dds)을 참고했습니다. 기존 수녀 차림 그림의 개별 제작 출처는 미확인입니다.

| 중점 | 아이콘 | 장면 |
| --- | --- | --- |
| 공화주의자들과의 화해 (`KOR_nomination_prime_minister`) | [focus_kor_nomination_prime_minister.dds](gfx/interface/goals/focus_kor_nomination_prime_minister.dds) | 파란 원형 문장 속 안창호(린), 김구(나기사), 여운형(노도카) |
| 제국섭정 계연수 (`KOR_imperial_regent_gyeyeonsu`) | [focus_kor_imperial_regent_gyeyeonsu.dds](gfx/interface/goals/focus_kor_imperial_regent_gyeyeonsu.dds) | 월계관 속 수녀 차림 유우카 |
| 계연수 축출 (`KOR_oppose_gyeyeonsu`) | [focus_kor_oppose_gyeyeonsu.dds](gfx/interface/goals/focus_kor_oppose_gyeyeonsu.dds) | 보라색 문장과 교차한 칼 장식 위로 보이는 수녀 차림 유우카 |

축출 아이콘은 후속 편집에서 베일 바깥으로 나온 옆머리를 정리했습니다.

세 장 모두 100×88 비압축 32비트 DDS이며, 본체의 기존 경로를 사용합니다. 기본 그림과 광택 마스크의 연결 및 실제 크기의 DDS 미리보기를 확인했습니다. 게임 내 표시는 미검증입니다.

개발 작업 위치와 검증 범위는 [AGENTS.md](AGENTS.md)를 참고하세요.
