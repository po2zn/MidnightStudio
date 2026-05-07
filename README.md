# MidnightStudio
TeamODD 제 2회 단기 프로젝트

📌 Overview
- MidnightStudio는 플레이어가 주어진 정보를 바탕으로 사건의 순서를 맞추는 게임입니다.

📌 My Role
- 메인 Dialogue, CSV기반 데이터들을 딕셔너리를 사용하여 출력
- 사진 기반의 캐릭터 애니메이션 구현 - 사진의 key값을 이용하여 스프라이트를 재설정
- 대화 스킵 기능 구현
- 정답 순서와 플레이타임에 따른 점수 시스템 구현

📌 Tech Stack
- UI_Production
- Sprtie
- TextMeshPro

📌 Key Implementation
- DialogueParser를 주로 작성 <br />
- UI_Production을 주로 사용하여 Sprtie 기반 애니메이션을 작업함
```
 private Sprite LoadActSprite(string speaker, string act)
    {
        string basePath = "";
        if (speaker.Contains("ink"))
        {
            basePath = "Ink_Character/";
        }
        else if (speaker.Contains("client"))
        {
            basePath = "Client_Character/";
        }
        else
        {
            Debug.LogWarning("알 수 없는 화자입니다.");
            return null;
        }

        string fullPath = basePath + act;

        Sprite sprite = Resources.Load<Sprite>(fullPath);

        if (sprite == null)
        {
            Debug.LogError($"[로드 실패] Sprite 경로: Resources/{fullPath}.png 또는 .jpg 가 존재하지 않음.");
        }

        return sprite;
    }
```
```

```
  
📌 Trouble Shooting
- 게임 프로그래밍을 처음 하는 거라 팀원이 협업 작업을 어려워 함.
- Unity 관련 지식이 전무했다. => ChatGpt와 Unity Document를 사용하여 부분 해결

📌 What I Learned
- 게임 개발이 무엇인지 정확히 깨달음.
- 코딩 관련 CleanCode 기법이나 협업 관련 작성 방식에 대해서 알아감.
- 
