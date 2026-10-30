# 📚 실제 차수와 원고 단계

연구 단계·원본 폴더 차수·논문 수정·발표 차수는 서로 다른 구분입니다. 실제 파일과 본문으로 확인한 단계만 정리했습니다. 이전 공개 파일과 이름은 보존하며, 현재 원문과 과거 정제 사본을 구별합니다.

| 단계 | 내용 | 파일 종류 | 폴더·자료 | 직전 단계 전체 비교 |
|---|---|---|---|---|
| [1차 · 06.17/06.22/06.29 원고 묶음](revisions/paper-1.md) | 동일 폴더 안에서 06.17·06.22·06.29 수정본과 영문 최종본이 이어집니다. 06.17 PDF에는 학회 양식의 예시 저자소개가 남고, 06.29 영문 초록에는 five benchmark datasets라고 쓰지만 본문 실험 표는 네 데이터셋을 제시합니다. 이는 원고 단계의 불일치로 보존하며 실제 다섯 데이터셋 실험을 추가 주장하지 않습니다. 06.22와06.29 수정본은 HWP만 확인되어 원본 fingerprint와 본문 비교로 구별합니다. | hwp·pdf·png·pptx | [직접 자료](../%EC%9B%90%EA%B3%A0%EB%8B%A8%EA%B3%84/1%EC%B0%A8/06.17_%EC%9B%90%EA%B3%A0.pdf) | [전체 차이](revision-diffs/paper-1.diff) |
| [2차 원고](revisions/paper-2.md) | 평가 대상을 네 데이터셋으로 바로잡고, Ratings2·Ratings5의 임계값2·5, ML-1M MRR@10 감소 예외, 기본5:5 결합 비율 및 참조문헌을 구체화합니다. 그래프 필터 설명도 Linear에서 High-order로 바뀐 부분이 있습니다. 원고 수정이며 새 실험 실행을 확인한 것은 아닙니다. | hwp·pdf | [직접 자료](../%EC%9B%90%EA%B3%A0%EB%8B%A8%EA%B3%84/2%EC%B0%A8/%EC%9B%90%EA%B3%A0.pdf) | [전체 차이](revision-diffs/paper-2.diff) |
| [3차 · 사물인터넷학회 양식 원고](revisions/paper-3.md) | 2차와 해시가 같은 영문 HWP 사본이 함께 남고, 별도 12.hwp/PDF는 한글 제목·국영문 초록과 한국사물인터넷학회 양식으로 재구성합니다. 초록은 F1·MRR·NDCG와 Ratings2 23/24·Ratings5 24/24 비교를 명시합니다. | hwp·pdf | [직접 자료](../%EC%9B%90%EA%B3%A0%EB%8B%A8%EA%B3%84/3%EC%B0%A8/%EC%9B%90%EB%AC%B8_%EC%9B%90%EA%B3%A0.pdf) | [전체 차이](revision-diffs/paper-3.diff) |
| [최종 원고](revisions/final.md) | 3차 12.hwp에서 표의 잘린 NDCG@ 표기를 NDCG@10으로 정리한 차이를 확인했습니다. 최종 PDF의 추천 방법·결과표는 원고 보고값이며 재현 코드·원데이터·새 측정은 제공되지 않습니다. | hwp·pdf | [직접 자료](../%EB%85%BC%EB%AC%B8/%EC%B5%9C%EC%A2%85_%EB%85%BC%EB%AC%B8.pdf) | [전체 차이](revision-diffs/final.diff) |
