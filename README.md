E-mail: seunguk.gamja@gmail.com

# Wonderland Of Madness (광기의 원더랜드)
'이상한 나라의 앨리스'를 주제로 뱀서류 게임을 개발한 팀 프로젝트입니다.

---
# 팀 구성
1. 프로그래머: 2명
2. 그래픽 디자이너: 3명

<br>

핵심 역할: 팀장, 기획, 프로그래밍

팀원이 무작위로 구성이 되다보니 저희 팀은 따로 기획자가 없어서 제가 팀장과 함께 맡게 되었습니다.

---
# 게임 개요
- 장르: 2D 탑다운 생존 액션 로그라이크
   
- 개발기간: 2025.03.04~2025.06.16 (약 3개월)
   
- 개발도구: Unity, Aseprite, Photoshop
   
- 설명: '이상한 나라의 앨리스'를 주제로 한 뱀파이어 서바이벌이다. 도트 그래픽을 사용함으로써 이상한 나라의 기괴하고 동화적인 분위기를 표현하였습니다.
   
- 기획의도: 2022년에 출시한 '뱀파이어 서바이벌'은 많은 관심을 받으며 큰 인기를 끌었습니다. 그 이후 일명 '뱀서류'라고 불리게 되는 게임의 장르가 탄생하게 되었고, 시간이 지난 지금까지도 뱀서류 게임은 계속해서 개발이 되며 출시되고 있습니다. 이에 뱀서류 게임을 기획 및 제작을 하며 게임개발의 전반적인 흐름을 경험하고자 기획하게 되었습니다.
   
---
# 기능 구현
몬스터와 아이템, 애니메이션 그리고 이와 관련된 시스템의 기능을 주로 담당하여 구현하였습니다.

+ 몬스터
   - 피격 효과: 무기에 피격 시 데미지, 넉백, 슬로우 여부에 따라 해당 피격 효과를 받는다. (로직 설계는 제가 하였고, 무기 시스템을 담당하는 팀원에게 전달하여 수정 이후 적용하였습니다.)

   - 데미지 텍스트: 데미지를 입었을 시 해당 값을 시각적으로 표현한다.

   - 근접 몬스터: 플레이어의 위치를 추적하며 이동을 한다.
     
   - 원거리 몬스터: 플레이어와의 거리를 비교하며 공격과 이동을 한다.
     
   - 자폭 몬스터: 플레이어의 위치를 추적하며, 일정 범위 내일 경우 자폭을 한다.
     
   - 이벤트 몬스터: 특정 방향으로 돌진하거나 이동을 제한한다.
      - 돌진 이벤트: 십자가 혹은 엑스자 방향으로 이동하는 이벤트 몬스터를 소환한다.
      - 이동제한 이벤트: 플레이어를 중심으로 타원형의 몬스터 그룹을 소환한다.
     
   - 보스 몬스터: 범위 내에서 이동을 하며, 여러 가지의 공격 패턴을 가지고 있다.
      - 네임드 몬스터 소환: 근거리 병사 혹은 원거리 병사를 소환한다.
      - 고정형 길로틴 소환: 맵에 고정형 길로틴을 소환한다.
      - 이동형 길로틴 소환: 플레이어의 위치를 가로질러 공격하는 길로틴을 소환한다.

<br>

+ 아이템
   - 경험치 아이템: 몬스터가 사망 시 바닥에 떨어뜨리는 아이템으로, 해당 아이템을 획득 시 경험치가 증가한다.
     
   - 자석 아이템: 몬스터가 사망 시 일정확률로 떨어뜨리는 아이템으로, 해당 아이템을 획득 시 바닥에 떨어져있는 모든 간, 개체수의 정보를 읽어 해당 몬스터 웨이브를 실행한다.

   - 회복 아이템: 몬스터가 사망 시 일정확률로 떨어뜨리는 아이템으로, 해당 아이템을 획득 시 플레이어의 체력이 회복된다.
     
<br>

+ 시스템

   - 몬스터 웨이브: CSV 파일에서 웨이브 시작시간, 몬스터 타입, 개체수, 생성 간격의 값을 읽어와 몬스터를 활성화한다.
     
   - 몬스터 이벤트: 랜덤한 시간마다 이벤트형 몬스터의 패턴을 실행한다.
 
   - 오브젝트 풀링: 오브젝트를 초기화시킨 후 필요할 때마다 불러와 사용하고, 종료되면 다시 넣어둔다. (팀원이 작성한 오브젝트 풀링을 활용하여 몬스터, 아이템에 적용하였습니다.)
 
   - 카메라 추적: 플레이어를 일정속도로 따라다닌다.
 
   - 카메라 효과: 플레이어 사망 및 보스 사망 시 해당 애니메이션 실행과 해당 위치로 카메라가 줌인된다.

---
# 플레이 영상

https://youtu.be/pitDKVRhuyg
