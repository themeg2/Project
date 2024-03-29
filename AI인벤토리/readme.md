# AI 인벤토리 프로젝트 구조
```
|---> 1단계: 보안 및 얼굴 인식 (OpenCV)
|      |
|      |---> 카메라를 이용한 얼굴 인식
|             |
|             |---> 등록된 담당자 확인
|                    |
|                    |---> 출입 허가: 등록된 담당자에게 출입 허용
|                    |      |
|                    |      |---> 출입 로그: 담당자 데이터베이스에 기록
|                    |
|                    |---> 출입 금지: 등록되지 않은 자에게 출입 거부
|
|---> 2단계: 음성을 통한 재고 조회 (Whisper Mic)
|      |
|      |---> 통합
|            |
|            |---> 마이크 입력 받기
|                   |
|                   |---> OpenAI Whisper 기반 음성 인식
|                          |
|                          |---> 음성 입력을 텍스트로 변환
|
|---> 3단계: 데이터베이스를 이용한 재고 관리
|      |
|      |---> 재고 데이터 조회
|             |
|             |---> 재고 유무 확인
|                    |
|                    |---> 재고 있음: 위치 정보 음성 및 텍스트 출력, 맵 표시
|                    |      |
|                    |      |---> 재고 입출고 로그: 데이터베이스에 기록
|                    |
|                    |---> 재고 없음: 재고 부족 안내
|
|---> 4단계: 로그 관리
       |
       |---> 입출입 로그 기록
       |      |
       |      |---> 얼굴 인식을 통한 출입자 로깅
       |
       |---> 재고 입출고 로그 기록
              |
              |---> 재고 변동 사항 로깅
```
