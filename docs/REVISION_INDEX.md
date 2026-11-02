# 📚 실제 차수와 원고 단계

아래 표는 코드 개발과 원고 수정 당시의 변화입니다. 현재 다운로드는 최신 완성 문서로 연결하며 이전 첨부는 변경 이력에서 구분합니다.

연구 단계·원본 폴더 차수·논문 수정·발표 차수는 서로 다른 구분입니다. 실제 파일과 본문으로 확인한 단계만 정리했습니다. 코드 차수와 원고 수정의 설명·비교 이력은 유지하고, 현재 첨부는 문서 계보별 최신 완성본으로 연결합니다.

| 단계 | 내용 | 파일 종류 | 폴더·자료 | 직전 단계 전체 비교 |
|---|---|---|---|---|
| [1차 · 06.17/06.22/06.29 원고 묶음](revisions/paper-1.md) | 동일 폴더 안에서 06.17·06.22·06.29 수정본과 영문 최종본이 이어집니다. 06.17 PDF에는 학회 양식의 예시 저자소개가 남고, 06.29 영문 초록에는 five benchmark datasets라고 쓰지만 본문 실험 표는 네 데이터셋을 제시합니다. 이는 원고 단계의 불일치로 보존하며 실제 다섯 데이터셋 실험을 추가 주장하지 않습니다. 06.22와06.29 수정본은 HWP만 확인되어 원본 fingerprint와 본문 비교로 구별합니다. | hwp·pdf·png·pptx | [최신 PDF](../%EB%85%BC%EB%AC%B8/%EC%B5%9C%EC%A2%85_%EC%9B%90%EB%AC%B8_%EB%85%BC%EB%AC%B8.pdf) | [전체 차이](revision-diffs/paper-1.diff) · [자료 폴더](../%EC%9B%90%EA%B3%A0%EB%8B%A8%EA%B3%84/1%EC%B0%A8) |
| [2차 원고](revisions/paper-2.md) | 평가 대상을 네 데이터셋으로 바로잡고, Ratings2·Ratings5의 임계값2·5, ML-1M MRR@10 감소 예외, 기본5:5 결합 비율 및 참조문헌을 구체화합니다. 그래프 필터 설명도 Linear에서 High-order로 바뀐 부분이 있습니다. 원고 수정이며 새 실험 실행을 확인한 것은 아닙니다. | hwp·pdf | [최신 PDF](../%EB%85%BC%EB%AC%B8/%EC%B5%9C%EC%A2%85_%EC%9B%90%EB%AC%B8_%EB%85%BC%EB%AC%B8.pdf) | [전체 차이](revision-diffs/paper-2.diff) · [최신 자료](../%EB%85%BC%EB%AC%B8) |
| [3차 · 사물인터넷학회 양식 원고](revisions/paper-3.md) | 당시 2차와 해시가 같은 영문 HWP 사본이 함께 있었고, 별도 12.hwp/PDF는 한글 제목·국영문 초록과 한국사물인터넷학회 양식으로 재구성합니다. 초록은 F1·MRR·NDCG와 Ratings2 23/24·Ratings5 24/24 비교를 명시합니다. | hwp·pdf | [최신 PDF](../%EB%85%BC%EB%AC%B8/%EC%B5%9C%EC%A2%85_%EC%9B%90%EB%AC%B8_%EB%85%BC%EB%AC%B8.pdf) | [전체 차이](revision-diffs/paper-3.diff) · [최신 자료](../%EB%85%BC%EB%AC%B8) |
| [최종 원고](revisions/final.md) | 3차 12.hwp에서 표의 잘린 NDCG@ 표기를 NDCG@10으로 정리한 차이를 확인했습니다. 최종 PDF의 추천 방법·결과표는 원고 보고값이며 재현 코드·원데이터·새 측정은 제공되지 않습니다. | hwp·pdf | [직접 자료](../%EB%85%BC%EB%AC%B8/%EC%B5%9C%EC%A2%85_%EC%9B%90%EB%AC%B8_%EB%85%BC%EB%AC%B8.pdf) | [전체 차이](revision-diffs/final.diff) · [자료 폴더](../%EB%85%BC%EB%AC%B8) |




[🏠 첫 화면](../README.md)

## 📚 현재 첨부 문서

이전 원고·발표의 변경 설명과 코드 차수는 위의 이력에서 확인할 수 있습니다. 다운로드는 문서 계보별 최신 완성본으로 연결합니다.

| 문서 | 자료 폴더 | 상세 | 직전 공개본 전체 비교 |
|---|---|---|---|
| 최종 논문 · 평점 기반 추천 | [폴더](../%EB%85%BC%EB%AC%B8) | [설명](latest/rating-aware-graph-filter.md) | [전체 비교](changes/2026-11-02-%EC%B5%9C%EC%8B%A0%EB%AC%B8%EC%84%9C-%EC%A0%84%EC%B2%B4%EB%B9%84%EA%B5%90.md) |

[📝 최신 문서 구성 변경](changes/2026-11-02-%EC%B5%9C%EC%8B%A0%EB%AC%B8%EC%84%9C.md)
