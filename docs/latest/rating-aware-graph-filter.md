<div align="center">

# 📄 Performance Improvement of Recommendation Systems using User Evaluation Information

사용자 평점 정보를 기존 상호작용 그래프와 결합해 추천 순위의 성능을 비교한 10쪽 최종 전체 원고입니다.

</div>

[📖 목적·구성·사용법·결과의 상세 안내](../revisions/final.md) · [🏠 프로젝트](../../README.md) · [🗂️ 전체 차수](../REVISION_INDEX.md)

## 🧭 이 자료를 읽는 순서

1. 초록에서 전체 상호작용·평점 그래프의 두 경로를 파악합니다.
2. 방법의 그래프 필터와 가중 결합식을 읽고 표의 하이퍼파라미터를 확인합니다.
3. 네 데이터셋의 K5·10 결과를 지표별로 비교합니다.
4. 개선한 조합과 ML-1M MRR@10의 예외를 함께 읽고 결합 비율의 영향을 확인합니다.

## 🔎 연결된 내용

| 구성 | 읽을 내용 |
| --- | --- |
| 최종 전체 본문 | 사진을 포함한 최종 PDF와 같은 판의 HWP를 제공합니다. |
| 보고 결과 | 네 데이터셋×두 K×세지표 24조합에서 Ratings2는 23개, Ratings5는 24개 개선을 보고합니다. |
| 평점 그래프 | 임계값 2·5 이상인 평가 정보를 이용해 Ratings2·Ratings5를 구성합니다. |
| 이중 경로 | 기존 전체 상호작용 경로와 평점 정보를 이용한 경로를 결합합니다. |
| 평가 지표 | F1·MRR·NDCG를 K5·10과 데이터셋별로 나누어 읽습니다. |
| 기본 결합 | 기본 5:5 비율과 Ratings5의 데이터셋별 예외를 표와 함께 확인합니다. |


## 📊 해석 범위

최종 원고는 Ratings2의 24개 조합 중 23개, Ratings5의 24개 조합 전체에서 HiGSP 대비 개선을 보고합니다. 데이터셋·지표·평점 임계값별 원고 보고 결과로 읽습니다.

<details>
<summary>📎 파일·크기·SHA-256과 자료 연결</summary>

| 원문 파일 | 바이트 | SHA-256 |
|---|---:|---|
| [최종_원문_논문.pdf](../../%EB%85%BC%EB%AC%B8/%EC%B5%9C%EC%A2%85_%EC%9B%90%EB%AC%B8_%EB%85%BC%EB%AC%B8.pdf) | 518941 | `73a18db184a7d63ccab5f8d57d31d3e10079cda68e93d0353fbf6095a41226dd` |
| [최종_원문_논문.hwp](../../%EB%85%BC%EB%AC%B8/%EC%B5%9C%EC%A2%85_%EC%9B%90%EB%AC%B8_%EB%85%BC%EB%AC%B8.hwp) | 739328 | `0382a4f19d559927066fd3899b6184bb5dda86b62d55a6be0eb230dbef11d499` |

</details>

[➡️ 전체 설명으로 이동](../revisions/final.md)
