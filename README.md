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
| 한국군 보병 3D 외형 | `gfx/models/units/`, `gfx/entities/` |

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

### 다즐링 한국 보병 모델

2026-11-13에 한국 보병 외형을 [TRY RE HQ ANIME MOD 1.0](https://steamcommunity.com/sharedfiles/filedetails/?id=1171917559)의 다즐링으로 교체했습니다. 캐릭터는 《걸즈 앤 판처》의 다즐링이며, HOI4 모델 포팅은 [Milek의 3d Anime infantry model](https://steamcommunity.com/sharedfiles/filedetails/?id=2393210146)에서 왔습니다. 이 서브모드의 재배포 허가는 미확인입니다.

Workshop 설치본 `gfx/models/units`의 `ENG_infantry.mesh`와 메시가 참조하는 색상·노멀·광택 DDS 31개를 [다즐링 자산 폴더](gfx/models/units/darjeeling/)에 원본 바이트 그대로 복사했습니다. [모델 정의](gfx/entities/kor_infantry_trinity.gfx)에서 한국 보병의 소총·기관단총 메시가 이 파일을 사용합니다. 적용 대상은 `KOR_infantry_entity`, `KOR_infantry_2_entity`, `KOR_infantry_3_entity`입니다. 포병에 동반되는 보병도 첫 번째 엔티티를 사용합니다.

본체 보병과 뼈 33개의 이름·순서·부모 관계 및 장비 부착 뼈가 일치합니다. Blender에서 기존 소총·기관단총 이동과 공격 클립을 확인했습니다. 게임 내 표시와 총기 부착 위치는 미검증입니다.

### 이전 각청 시안

2026-11-13에 [Anime Units-Chinese](https://steamcommunity.com/sharedfiles/filedetails/?id=2604675336)의 각청 모델을 시안으로 사용했습니다. 원본은 HoYoverse, HOI4 모델 포팅은 Milek238, Workshop 모드 제작자는 Bitter Tenderness입니다. OpenAI ImageGen으로 의상과 머리 텍스처를 다시 그렸고 메시에서 앞머리와 눈 주변을 조정했습니다. Blender에서 대기 자세와 소총 이동·사격을 확인했습니다. 다즐링으로 전환하면서 시안을 외부 작업 백업에 보관했습니다.

### 본체 메시 기반 트리니티 시안

2026-11-13에 본체 `065b555`의 `KOR_infantry.mesh`를 바탕으로 남색 주름치마와 양갈래 장발을 Blender에서 모델링했습니다. [Anime Units-Chinese](https://steamcommunity.com/sharedfiles/filedetails/?id=2604675336)의 각청을 외형 참고로 사용했습니다. `KOR_infantry_diffuse.dds`는 본체의 색상 텍스처를 OpenAI ImageGen으로 다시 그리고, 기존 256×256 비압축 BGRA32 형식과 알파를 보존해 변환했습니다.

`KOR_infantry_trinity.mesh`는 본체의 뼈대와 충돌 형상을 사용했습니다. 이 시안의 메시와 텍스처는 다즐링 적용 후 저장소 밖 작업 백업으로 옮겼습니다. 기병·자전거·차량 탑승 모델은 본체의 기존 메시를 사용합니다.

Blender에서 내보낸 메시를 다시 열고 원본 뼈 33개와 기존 대기·이동·돌격·소총 사격·앉아 쏘기·기관단총 사격 애니메이션의 대표 프레임을 확인했습니다. 실제 게임 표시는 미검증입니다.

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

### 대선·쇼와 데모크라시·비전 1950·대한제국 사건 삽화

2026-11-12에 OpenAI ImageGen으로 투표 삽화 두 장을 다시 그렸고, 기존 서브모드의 해안·야경·광장 구도를 바탕으로 세 장을 편집했습니다. 기존 삽화의 개별 원출처는 미확인입니다.

| 사건 | 그림과 연결 | 장면 |
| --- | --- | --- |
| 1946년 제9대 대통령 선거 (`kor_events.71`) | [report_event_K004.dds](gfx/event_pictures/report_event_K004.dds) · `GFX_report_event_K004` | 여운형(모자를 벗은 노도카), 이강(드레스 하루카), 윤보선(사오리)의 후보 안내지 |
| 쇼와 데모크라시 (`newsj.3`) | [newsj_event_003.dds](gfx/event_pictures/newsj_event_003.dds) · `GFX_newsj_event_003` | 카호·미모리·나구사·카에데의 투표판 |
| 비전 1950 해군 완성 (`newsk.12`) | [newsk_event_008.dds](gfx/event_pictures/newsk_event_008.dds) · `GFX_newsk_event_008` | 기존 해안도로 앞의 함대와 갑판 위 오디세이아 학생들 |
| 명동성당 즉위식 (`newsk.17`) | [newsk_event_015.dds](gfx/event_pictures/newsk_event_015.dds) · `GFX_newsk_event_015` | 기존 야경을 바탕으로 그린 마코토와 만마전 일행의 행렬 |
| 은장도의 밤 (`newsk.26`) | [newsk_event_017.dds](gfx/event_pictures/newsk_event_017.dds) · `GFX_newsk_event_017` | 기존 광장을 밤으로 바꾸고 게헨나와 트리니티 모브들의 충돌을 그림. 후속 편집에서 양측 모브의 눈을 앞머리와 그림자로 가림 |

대선 삽화는 서브모드의 노도카·하루카·사오리 초상에 맞췄습니다. 쇼와 삽화는 [카호](https://x.com/Blue_ArchiveJP/status/1643886488676077568), [미모리](https://x.com/Blue_ArchiveJP/status/1490521019236626435), [나구사](https://x.com/Blue_ArchiveJP/status/1924314158402830736), [카에데](https://x.com/Blue_ArchiveJP/status/1517337541346619394)의 공식 소개를 참고했습니다. 비전 1950은 서브모드에서 그린 미나토 초상, 명동성당은 이은 초상과 기존 경복궁 즉위식 삽화의 만마전 일행을 참고했습니다.

대선은 210×176 투명 외곽을 유지한 비압축 BGRA32 DDS, 나머지는 397×153 비압축 BGRA32 DDS입니다. 본체 스프라이트의 경로, DDS 규격과 표시 크기 미리보기를 확인했습니다. 게임 내 표시는 미검증입니다.

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

2026-11-12에 본체와 서브모드의 기존 문장을 참고해 세 장을 OpenAI ImageGen으로 다시 그렸습니다. 화해 아이콘은 왼쪽부터 린·나기사·노도카를 배치했습니다. 린의 복장과 얼굴은 [공식 소개](https://x.com/Blue_ArchiveJP/status/1356074850909999105)를 참고했고, 나기사와 노도카는 위에 기록한 공식 소개 그림을 참고했습니다. 계연수 중점 두 장의 첫 제작에는 [유우카 공식 소개](https://x.com/Blue_ArchiveJP/status/1353175798992179200)와 [교체 전 계연수 초상](https://github.com/jaewoopark351/Hearts-of-Korea-anime/blob/237728a5b45ee3e2942aa027019b60e4d8b9362d/gfx/leaders/KOR/Portrait_KOR_Yeonsu_Gye.dds)을 참고했습니다. 기존 수녀 차림 그림의 개별 제작 출처는 미확인입니다.

| 중점 | 아이콘 | 장면 |
| --- | --- | --- |
| 공화주의자들과의 화해 (`KOR_nomination_prime_minister`) | [focus_kor_nomination_prime_minister.dds](gfx/interface/goals/focus_kor_nomination_prime_minister.dds) | 파란 원형 문장 속 안창호(린), 김구(나기사), 여운형(노도카) |
| 제국섭정 계연수 (`KOR_imperial_regent_gyeyeonsu`) | [focus_kor_imperial_regent_gyeyeonsu.dds](gfx/interface/goals/focus_kor_imperial_regent_gyeyeonsu.dds) | 열린 월계관 속 시스터후드 복장의 사쿠라코 |
| 계연수 축출 (`KOR_oppose_gyeyeonsu`) | [focus_kor_oppose_gyeyeonsu.dds](gfx/interface/goals/focus_kor_oppose_gyeyeonsu.dds) | 보라색 문장과 교차한 칼 장식 위로 보이는 사쿠라코 |

유우카가 들어갔던 축출 아이콘은 당시 후속 편집에서 베일 바깥으로 나온 옆머리를 정리했습니다. 두 계연수 중점의 인물은 이후 OpenAI ImageGen으로 다시 그려, 아래 계연수 대형 초상과 같은 시스터후드 복장의 사쿠라코로 교체했습니다.

세 장 모두 100×88 비압축 32비트 DDS이며, 본체의 기존 경로를 사용합니다. 기본 그림과 광택 마스크의 연결 및 실제 크기의 DDS 미리보기를 확인했습니다. 게임 내 표시는 미검증입니다.

### 왕의 귀환 중점과 인물 초상

2026-11-12에 《블루 아카이브》의 캐릭터 디자인을 참고해 OpenAI ImageGen으로 다시 그렸습니다. 왕의 귀환은 기존 중점의 왕관과 월계 장식을 참고했습니다. 기존 자산의 개별 제작 출처는 미확인입니다.

| 대상 | 캐릭터 | 교체 파일 | 캐릭터 참고 자료 |
| --- | --- | --- | --- |
| 왕의 귀환 (`KOR_return_of_the_king`) | 하누마 마코토 | [중점](gfx/interface/goals/focus_kor_return_of_the_king.dds) | [공식 소개](https://x.com/Blue_ArchiveJP/status/1749280823805870118) |
| 이강 (`KOR_Gang_Lee`) | 이구사 하루카(드레스) | [대형](gfx/leaders/KOR/Portrait_KOR_Gang_Lee.dds) | [공식 소개](https://x.com/Blue_ArchiveJP/status/2058397620327129204) |
| 유일한 (`KOR_Ilhan_Yu`) | 우시오 노아 | [소형](gfx/interface/ideas/idea_KOR_Ilhan_Yu.dds) | [공식 소개](https://x.com/Blue_ArchiveJP/status/1573507606278459392) |
| 손원일 (`KOR_Wonil_Son`) | 미소노 미카(수영복) | [대형](gfx/leaders/KOR/Portrait_KOR_Wonil_Son.dds) · [소형](gfx/interface/ideas/idea_KOR_wonil_son.dds) | [공식 소개](https://x.com/Blue_ArchiveJP/status/1949318904779878694) |
| 이규갑 (`KOR_Gyugap_Lee`) | 오디세이아 미나토 | [대형](gfx/leaders/KOR/Portrait_KOR_Gyugap_Lee.dds) · [소형](gfx/interface/ideas/idea_KOR_Gyugap_Lee.dds) | [게임 스프라이트](https://www.reddit.com/r/BlueArchive/comments/1vytq4a/jp_spoiler_all_new_character_sprites_in_the/) |
| 권기옥 (`KOR_Giok_Gwon`) | 와일드헌트 에리 | [대형](gfx/leaders/KOR/Portrait_KOR_Giok_Gwon.dds) · [소형](gfx/interface/ideas/idea_KOR_Giok_Gwon.dds) | [공식 소개](https://x.com/Blue_ArchiveJP/status/1957291422039916600) |
| 안창남 (`KOR_Changnam_Ahn`) | 와일드헌트 미요 | [소형](gfx/interface/ideas/idea_KOR_changnam_ahn.dds) | [공식 소개](https://x.com/Blue_ArchiveJP/status/1969597863455048085) |
| 김정렬 (`KOR_Jeongryeol_Kim`) | 케이 | [소형](gfx/interface/ideas/idea_KOR_Jeongryeol_Kim.dds) | [공식 소개](https://x.com/Blue_ArchiveJP/status/2015621284898775451) |
| 최성학 (`KOR_Seonghak_Choi`) | 나나미 | [대형](gfx/leaders/KOR/Portrait_KOR_Seonghak_Choi.dds) · [소형](gfx/interface/ideas/idea_KOR_Seonghak_Choi.dds) | [게임 스크린샷](https://pomzero.hatenablog.com/entry/2026/09/01/205518) |
| 최용덕 (`KOR_Yongdeuck_Choi`) | 와일드헌트 미리아(기숙사 감독) | [소형](gfx/interface/ideas/idea_KOR_Yongdeok_Choi.dds) | [게임 스크린샷](https://pomzero.hatenablog.com/entry/2025/08/23/200211) |

본체 `cdc022e`에 연결된 기존 경로를 사용합니다. 중점은 100×88, 대형 초상은 156×210, 소형 초상은 65×67 비압축 32비트 DDS입니다. 소형은 기존 종이와 그림자, 투명 여백을 보존하고 인물 영역을 교체했습니다. 본체의 연결, DDS 헤더와 알파, 실제 크기의 미리보기를 확인했습니다. 게임 내 표시는 미검증입니다.

### 이은 초상

2026-11-12에 [하누마 마코토 공식 소개](https://x.com/Blue_ArchiveJP/status/1749280823805870118)와 서브모드의 기존 초상을 참고해 OpenAI ImageGen으로 다시 그렸습니다. 후속 요청에 따라 황제와 장군의 대형 초상은 첨부된 금장 모자와 예복 차림의 마코토 그림으로 통일했습니다. 이전 초상의 개별 제작 출처는 미확인입니다.

| 화면 | 스프라이트 | 파일 |
| --- | --- | --- |
| 황제 대형과 시민 영향력 창 | `GFX_Portrait_KOR_Eun_Lee` | [Portrait_KOR_Eun_Lee.dds](gfx/leaders/KOR/Portrait_KOR_Eun_Lee.dds) |
| 장군 대형 | `GFX_Portrait_KOR_Eun_Lee_general` | [Portrait_KOR_Eun_Lee_general.dds](gfx/leaders/KOR/Portrait_KOR_Eun_Lee_general.dds) |
| 장군 소형 | `GFX_Portrait_KOR_Eun_Lee_general_small` | [idea_KOR_Eun_Lee_general.dds](gfx/interface/ideas/idea_KOR_Eun_Lee_general.dds) |

본체 `cdc022e`의 이은(`KOR_Eun_Lee`) 연결과 같은 경로를 사용합니다. 대형 두 장은 156×210, 소형은 65×67 비압축 32비트 DDS입니다. 장군 소형은 모자를 벗은 마코토 그림을 사용하며 원본의 종이, 그림자, 알파를 보존했습니다. 두 대형 DDS의 파일 해시와 실제 크기의 미리보기를 대조했습니다. 게임 내 표시는 미검증입니다.

### 계연수·염동진·박승직 초상

2026-11-12에 세 초상을 OpenAI ImageGen으로 다시 그렸습니다. 사쿠라코는 시스터후드 기본 복장, 토키는 SMILE BASE CAFE의 공식 협업 「Autumn Code」 가을 사복을 참고했습니다. 히로미는 와일드헌트 사감대 복장의 게임 스크린샷을 참고했습니다. 이전 초상의 개별 제작 출처는 미확인입니다.

| 인물 | 캐릭터 | 교체 파일 | 디자인 참고 |
| --- | --- | --- | --- |
| 계연수 (`KOR_Yeonsu_Gye`) | 우타즈미 사쿠라코 | [대형](gfx/leaders/KOR/Portrait_KOR_Yeonsu_Gye.dds) | [공식 소개](https://x.com/Blue_ArchiveJP/status/1622792666521157637) |
| 염동진 (`KOR_Dongjin_Yeom`) | 아스마 토키(사복) | [소형](gfx/interface/ideas/idea_KOR_Dongjin_Yeom.dds) | [공식 협업](https://smilebase.co.jp/10210/) |
| 박승직 (`KOR_Seungjik_Park`) | 와일드헌트 히로미 | [소형](gfx/interface/ideas/idea_KOR_Seungjik_Park.dds) | [게임 스크린샷](https://pomzero.hatenablog.com/entry/2025/08/23/200211) |

본체 `cdc022e`에 연결된 기존 경로를 사용합니다. 계연수 대형은 156×210, 염동진과 박승직 소형은 65×67 비압축 32비트 DDS입니다. 계연수 대형은 시민 영향력 창에서 공유하며, 염동진과 박승직 소형은 정치고문 화면에서 사용합니다. 소형의 종이, 그림자, 투명 영역을 보존했습니다. 스프라이트 연결, DDS 형식과 실제 크기의 미리보기를 확인했습니다. 게임 내 표시는 미검증입니다.

### 한국 신규 모집 과학자와 김두봉 초상

2026-11-12에 《블루 아카이브》의 캐릭터 자료를 참고해 OpenAI ImageGen으로 아홉 장을 그렸습니다. 과학자 초상은 본체 작업 트리 `cdc022e`에서 추가된 한국 전용 남녀 슬롯과 스프라이트에 같은 상대 경로로 연결합니다. 남성 슬롯에도 요청된 블루 아카이브 캐릭터 그림을 사용하므로 모집 인물의 이름과 성별은 본체 목록의 구분을 따릅니다.

| 대상 | 캐릭터 | 교체 파일 | 디자인 참고 |
| --- | --- | --- | --- |
| female_01 | 아즈마 미라이 | [대형](gfx/leaders/scientists/HOK_KOR/portrait_HOK_KOR_scientist_female_01.dds) | [게임 스프라이트](https://bluearchive.wikiru.jp/?%E3%83%9F%E3%83%A9%E3%82%A4) |
| female_02 | 시라이시 우타하 | [대형](gfx/leaders/scientists/HOK_KOR/portrait_HOK_KOR_scientist_female_02.dds) | [공식 소개](https://x.com/Blue_ArchiveJP/status/1352450997054914560) |
| female_03 | 네코즈카 히비키 | [대형](gfx/leaders/scientists/HOK_KOR/portrait_HOK_KOR_scientist_female_03.dds) | [공식 소개](https://x.com/Blue_ArchiveJP/status/1352813334752497671) |
| female_04 | 토요미 코토리(안경 벗음) | [대형](gfx/leaders/scientists/HOK_KOR/portrait_HOK_KOR_scientist_female_04.dds) | [공식 소개](https://x.com/Blue_ArchiveJP/status/1352088620920832001) · [안경을 벗은 얼굴](https://x.com/Blue_ArchiveJP/status/1698531591793090648) |
| male_01 | 쿠로사키 코유키 | [대형](gfx/leaders/scientists/HOK_KOR/portrait_HOK_KOR_scientist_male_01.dds) | [공식 소개](https://x.com/Blue_ArchiveJP/status/1632214513197137920) |
| male_02 | 코세키 우이 | [대형](gfx/leaders/scientists/HOK_KOR/portrait_HOK_KOR_scientist_male_02.dds) | [공식 소개](https://x.com/Blue_ArchiveJP/status/1495231862805262341) |
| male_03 | 엔도 시미코 | [대형](gfx/leaders/scientists/HOK_KOR/portrait_HOK_KOR_scientist_male_03.dds) | [공식 소개](https://x.com/Blue_ArchiveJP/status/1347377530701967361) |
| male_04 | 아라마키 야쿠모 | [대형](gfx/leaders/scientists/HOK_KOR/portrait_HOK_KOR_scientist_male_04.dds) | [공식 소개](https://x.com/Blue_ArchiveJP/status/1989891753294664178) |
| 김두봉 (`KOR_Dubong_Kim`) | 미요시 타카네 | [소형](gfx/interface/ideas/idea_KOR_Dubong_Kim.dds) | [공식 소개](https://x.com/Blue_ArchiveJP/status/1989543975699845158) |

후속 편집에서는 기존 투명 초상화 뒤에 OpenAI ImageGen으로 그린 학교별 배경을 합성했습니다. 미라이는 밀레니엄 유사과학부 연구실, 우타하·히비키·코토리는 밀레니엄 엔지니어부 작업실, 코유키는 밀레니엄 세미나실을 사용합니다. 우이·시미코는 트리니티 고서관, 야쿠모는 레드윈터 출판부 편집실을 사용합니다.

과학자 8장은 156×210, 김두봉은 65×67 비압축 BGRA32 DDS입니다. 과학자 초상은 기존 인물의 위치와 불투명 영역의 색을 유지하고 반투명 윤곽을 배경에 합성했습니다. 김두봉 소형의 종이와 그림자, 알파는 기존 서브모드 자산에서 보존했습니다. 같은 상대 경로의 본체 연결과 최종 DDS 형식을 확인했습니다. 과학자 초상은 원본 크기와 명단의 약 0.4배 표시 크기로 확인했습니다. 애니 초상의 게임 내 표시는 미검증입니다.

### 한국 신규 모집 첩보원과 윤봉길 초상

2026-11-12에 《블루 아카이브》 공식 캐릭터 자료를 참고해 OpenAI ImageGen으로 아홉 장을 그렸습니다. 신규 모집 첩보원 여덟 명은 본체 작업본의 검은 중절모·코트·정장과 불투명 회색 배경을 참고해 드라마 《도깨비》의 저승사자 복장을 입혔습니다. 윤봉길의 메구 초상에도 저승사자 복장과 검은 중절모를 적용했습니다. 고글을 빼고, 고개를 숙인 무표정에 메구 기준 오른쪽 눈을 앞머리로 가렸습니다. 포니테일은 모자 챙 아래 목덜미 쪽으로 내렸습니다. [《도깨비》 공식 인물 소개](https://tvn.cjenm.com/ko/dokebi/character/)

| 대상 | 캐릭터 | 교체 파일 | 디자인 참고 |
| --- | --- | --- | --- |
| female_01 | 니키 안나 | [portrait_HOK_KOR_operative_female_01.dds](gfx/leaders/operatives/HOK_KOR/portrait_HOK_KOR_operative_female_01.dds) | [공식 소개](https://x.com/Blue_ArchiveJP/status/2101507177118892342) |
| female_02 | 이치노세 아스나 | [portrait_HOK_KOR_operative_female_02.dds](gfx/leaders/operatives/HOK_KOR/portrait_HOK_KOR_operative_female_02.dds) | [공식 소개](https://x.com/Blue_ArchiveJP/status/1881914740307558717) |
| female_03 | 쿠다 이즈나 | [portrait_HOK_KOR_operative_female_03.dds](gfx/leaders/operatives/HOK_KOR/portrait_HOK_KOR_operative_female_03.dds) | [공식 소개](https://x.com/Blue_ArchiveJP/status/1362990372146700292) |
| female_04 | 나카츠카사 키리노 | [portrait_HOK_KOR_operative_female_04.dds](gfx/leaders/operatives/HOK_KOR/portrait_HOK_KOR_operative_female_04.dds) | [공식 소개](https://x.com/Blue_ArchiveJP/status/1805118746912260126) |
| male_01 | 카스미자와 미유 | [portrait_HOK_KOR_operative_male_01.dds](gfx/leaders/operatives/HOK_KOR/portrait_HOK_KOR_operative_male_01.dds) | [공식 소개](https://x.com/Blue_ArchiveJP/status/1510814671909298176) |
| male_02 | 무로카사 아카네(안경 벗음) | [portrait_HOK_KOR_operative_male_02.dds](gfx/leaders/operatives/HOK_KOR/portrait_HOK_KOR_operative_male_02.dds) | [공식 소개](https://x.com/Blue_ArchiveJP/status/2038089449905729923) |
| male_03 | 시라스 아즈사 | [portrait_HOK_KOR_operative_male_03.dds](gfx/leaders/operatives/HOK_KOR/portrait_HOK_KOR_operative_male_03.dds) | [공식 소개](https://x.com/Blue_ArchiveJP/status/1395953346301763588) |
| male_04 | 사유리 | [portrait_HOK_KOR_operative_male_04.dds](gfx/leaders/operatives/HOK_KOR/portrait_HOK_KOR_operative_male_04.dds) | [오디세이아 공식 소개 영상](https://www.youtube.com/watch?v=hTpD_SHfCGY) |
| 윤봉길 (`KOR_bonggil_yoon`) | 시모쿠라 메구 | [portrait_KOR_operative_Bonggil_Yoon.dds](gfx/leaders/KOR/portrait_KOR_operative_Bonggil_Yoon.dds) | [공식 소개](https://x.com/Blue_ArchiveJP/status/1619168626946510848) |

신규 모집 초상은 본체 `f1282d7` 기반 작업 트리의 한국 전용 남녀 슬롯과 스프라이트를 같은 상대 경로로 사용합니다. 모집 이름과 성별은 본체 슬롯을 따릅니다. 윤봉길은 고정 첩보원용 `GFX_portrait_bonggil_yoon`에 연결됩니다. 아홉 장 모두 156×210 불투명 BGRA32 DDS입니다. 파일 연결과 규격, 원본 및 모집 목록 크기 미리보기를 확인했습니다. 게임 내 표시는 미검증입니다.

### 한국 신규 육군 장군·사단장 초상 8번

2026-11-13에 한국 육군의 무작위 초상 8번을 시이나 츠무기로 교체했습니다. OpenAI ImageGen으로 와일드헌트 교복, 머리띠, 헤일로를 참고해 대형을 그렸습니다. [《블루 아카이브》 공식 소개 이미지](https://blue-utils.me/static/img/intro/JP/ja/tsumugi.jpg) · [공식 모집 공지](https://bluearchive.jp/news/newsJump/696)

본체 `065b555`의 `GFX_Portrait_Korea_Generic_land_8`과 `GFX_Portrait_Korea_Generic_land_8_small`이 참조하는 기존 파일을 교체했습니다. 대형은 기존 156×210 BGRA32 DDS와 알파를 유지했습니다. 소형은 같은 그림을 기존 사진 영역에 넣고 종이·그림자·투명 외곽을 보존해 본체와 같은 65×67 BGRA32 DDS로 저장했습니다. 두 파일의 연결, DDS 규격과 실제 크기의 미리보기를 확인했습니다. 게임 내 표시는 미검증입니다. [대형](gfx/leaders/KOR/Portrait_KOR_Generic_land_8.dds) · [소형](gfx/interface/ideas/idea_KOR_generic_land_8.dds)

### 한국 육군·해군 무작위 초상

2026-11-13에 아래 네 초상을 OpenAI ImageGen으로 새로 그렸습니다. 무츠키·나츠·미모리는 공식 복장을 참고했고, 주리는 처음에 짙은 보라색 드레스로 그렸고, 후속 요청에서 사용자가 첨부한 그림을 참고해 흰 새틴 드레스와 검은 목 리본, 별자리 헤일로, 야간 연회장 배경을 살린 상반신 초상으로 다시 그렸습니다. 이후 사용자가 첨부한 확대 구도를 참고해 얼굴과 뿔이 화면을 더 채우도록 대형을 다시 그렸으며, 소형에서도 눈이 보이도록 인물 위치를 조정했습니다. 첨부 그림의 개별 제작 출처는 미확인입니다. 이전 초상과 소형 종이의 개별 제작 출처는 미확인입니다.

| 슬롯 | 캐릭터 | 교체 파일 | 디자인 참고 |
| --- | --- | --- | --- |
| 육군 2 | 아사기 무츠키(드레스) | [대형](gfx/leaders/KOR/Portrait_KOR_Generic_land_2.dds) · [소형](gfx/interface/ideas/idea_KOR_generic_land_2.dds) | [공식 소개](https://x.com/Blue_ArchiveJP/status/2058382817441235322) |
| 육군 3 | 우시마키 주리(드레스) | [대형](gfx/leaders/KOR/Portrait_KOR_Generic_land_3.dds) · [소형](gfx/interface/ideas/idea_KOR_generic_land_3.dds) | [기본 복장 공식 소개 이미지](https://blue-utils.me/static/img/intro/GL/en/juri.jpg) · 사용자 첨부 흰 드레스 그림 |
| 육군 9 | 유토리 나츠(밴드) | [대형](gfx/leaders/KOR/Portrait_KOR_Generic_land_9.dds) · [소형](gfx/interface/ideas/idea_KOR_generic_land_9.dds) | [공식 소개](https://x.com/Blue_ArchiveJP/status/1929010072388251739) |
| 해군 3 | 미즈하 미모리(수영복) | [대형](gfx/leaders/KOR/Portrait_KOR_Generic_navy_3.dds) · [소형](gfx/interface/ideas/idea_KOR_generic_navy_3.dds) | [공식 소개 이미지](https://blue-utils.me/static/img/intro/JP/ja/mimori_swimsuit.jpg) |

본체 `065b555`의 무작위 초상 목록과 스프라이트가 참조하는 기존 파일을 교체했습니다. 육군 2번의 대형·소형은 고정 장군 최용건(`KOR_Yonggeon_Choe`)도 공유합니다. 대형은 기존 156×210 BGRA32와 알파를 유지했고, 소형은 종이·그림자·투명 외곽을 보존해 본체와 같은 65×67 BGRA32로 저장했습니다. 스프라이트 연결, DDS 규격과 실제 크기의 미리보기를 확인했습니다. 게임 내 표시는 미검증입니다.

### 조선임시인민위원회 초상

2026-11-13에 기존 단체 초상의 인물을 OpenAI ImageGen으로 다시 그렸습니다. 노도카·토모에·체리노가 앞줄에 서고, 미노리·시구레·메루·모미지가 뒤에 섭니다. 마리나는 제외했습니다. 두 그림에 같은 인물을 배치하고 각 원본의 깃발 디자인과 배경을 살렸습니다. 기존 단체 그림의 개별 제작 출처는 미확인입니다. [노도카](https://blue-utils.me/static/img/intro/JP/ja/nodoka.jpg) · [토모에](https://blue-utils.me/static/img/intro/JP/ja/tomoe.jpg) · [체리노](https://blue-utils.me/static/img/intro/JP/ja/cherino.jpg) · [미노리](https://blue-utils.me/static/img/intro/JP/ja/minori.jpg) · [시구레](https://blue-utils.me/static/img/intro/JP/ja/shigure.jpg) · [메루](https://blue-utils.me/static/img/intro/JP/ja/meru.jpg) · [모미지](https://blue-utils.me/static/img/intro/JP/ja/momiji.jpg)

본체 `065b555`에서 일반 초상은 `GFX_Portrait_KOR_provisional_peoples_committee`를 통해 지도자 화면과 시민 영향력 창에 표시됩니다. `_anarchist`의 호출처와 두 초상의 소형 파일 연결은 확인되지 않았습니다. 두 대형 DDS의 기존 156×210 BGRA32 규격과 알파를 보존했고, 실제 크기에서 인물과 깃발을 확인했습니다. 게임 내 표시는 미검증입니다. [일반 초상](gfx/leaders/KOR/Portrait_KOR_provisional_peoples_committee.dds) · [무정부주의 초상](gfx/leaders/KOR/Portrait_KOR_provisional_peoples_committee_anarchist.dds)

개발 작업 위치와 검증 범위는 [AGENTS.md](AGENTS.md)를 참고하세요.
