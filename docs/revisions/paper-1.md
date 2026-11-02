<div align="center">

# ⭐ 1차 · 평점 기반 추천 원고의 수정 흐름

**06.17·06.22·06.29의 수정본과 영문 원고가 이어진 초기 편집 단계입니다.**

**기술 분류:** 추천 시스템 › 그래프 신호 처리 › 평점 기반 이중 그래프 필터

[목적](#purpose) · [기능](#features) · [입출력](#flow) · [구성](#files) · [준비](#setup) · [사용법](#usage) · [결과](#results) · [제약](#limits) · [변경](#changes)

</div>

<a name="purpose"></a>

## 🎯 이 단계에서 하는 일

연구의 공통 질문은 평점을 단순 상호작용으로 축약하지 않고 활용했을 때 추천 점수가 어떻게 달라지는가입니다. 원고 단계의 수정과 새 성능 실험 실행은 구분해 설명합니다.

<a name="features"></a>

## 🧩 주요 기능과 처리 방식

| 구성 | 실제 역할 |
| --- | --- |
| 초기 주장 비교 | 영문 초록의 five benchmark datasets와 본문의 네 데이터셋 표 등 당시 불일치를 구분합니다. |
| 편집의 변화 | 한글·영문 표현과 그래프 필터 설명이 단계마다 달라지는 흐름을 비교합니다. |
| 평점 그래프 | 임계값 2·5 이상인 평가 정보를 이용해 Ratings2·Ratings5를 구성합니다. |
| 이중 경로 | 기존 전체 상호작용 경로와 평점 정보를 이용한 경로를 결합합니다. |
| 평가 지표 | F1·MRR·NDCG를 K5·10과 데이터셋별로 나누어 읽습니다. |
| 기본 결합 | 기본 5:5 비율과 Ratings5의 데이터셋별 예외를 표와 함께 확인합니다. |

<a name="flow"></a>

## 🔄 입력 → 처리 → 출력

| 입력 | 처리 | 출력·읽을 결과 |
| --- | --- | --- |
| 사용자·아이템 상호작용과 평점 | 전체 상호작용·평점 임계값 그래프 구성 | 두 그래프 경로 |
| 각 그래프 | HiGSP 기반 필터링과 예측값 산출 | 경로별 추천 점수 |
| 두 예측값 | 가중 결합과 상위 K 추천 평가 | F1·MRR·NDCG 비교 |

<a name="files"></a>

## 📁 파일과 핵심 처리

| 파일 | 이용 방법 |
| --- | --- |
| [논문/최종_원문_논문.pdf](../../%EB%85%BC%EB%AC%B8/%EC%B5%9C%EC%A2%85_%EC%9B%90%EB%AC%B8_%EB%85%BC%EB%AC%B8.pdf) | 전체 원문·도표 읽기 |
| [논문/최종_원문_논문.hwp](../../%EB%85%BC%EB%AC%B8/%EC%B5%9C%EC%A2%85_%EC%9B%90%EB%AC%B8_%EB%85%BC%EB%AC%B8.hwp) | 같은 판의 편집 원본 |

<a name="setup"></a>

## ⚙️ 환경과 설정

| 항목 | 조건·기본값 |
| --- | --- |
| 데이터셋 | ML-100K·ML-Latest-Small·ML-1M·CiaoDVD |
| 평점 임계값 | 2 또는 5 |
| 평가 | F1·MRR·NDCG, K5·10 |
| 기본 가중치 | HiGSP:제안 경로 5:5·일부 Ratings5 예외 |

<a name="usage"></a>

## 📖 읽고 활용하는 순서

1. 초록에서 전체 상호작용·평점 그래프의 두 경로를 파악합니다.
2. 방법의 그래프 필터와 가중 결합식을 읽고 표의 하이퍼파라미터를 확인합니다.
3. 네 데이터셋의 K5·10 결과를 지표별로 비교합니다.
4. 개선한 조합과 ML-1M MRR@10의 예외를 함께 읽고 결합 비율의 영향을 확인합니다.

<a name="results"></a>

## 📊 결과를 읽는 방법

최종 원고는 Ratings2의 24개 조합 중 23개, Ratings5의 24개 조합 전체에서 HiGSP 대비 개선을 보고합니다. 데이터셋·지표·평점 임계값별 원고 보고 결과로 읽습니다.

기본 결합 비율·평점 임계값·데이터셋·지표에 따라 효과가 다릅니다. 전체 사용자에게 추천 품질이 동일하게 좋아진다거나 운영 서비스의 결과로 확대하지 않습니다.

<a name="limits"></a>

## 🛠️ 알려진 제약과 확인 지점

| 상황 | 확인할 내용 |
| --- | --- |
| 자료 범위 | 원고와 도표이며 추천 서비스·실험 코드·원본 사용자 로그는 별도 자료입니다. |
| 개선의 예외 | Ratings2의 ML-1M MRR@10은 감소합니다. 모든 지표가 개선됐다고 일반화하지 않습니다. |
| 서지 | 권·호·날짜 자리표시자와 공식 게재 확인은 구분합니다. |

<a name="changes"></a>

## 🔀 이전 단계와의 변화

초기 원고 묶음의 날짜별 문장·표현을 구분합니다. 현재 첨부는 최종 전체 원고로 연결하고 이전 문구는 단계 비교에서 읽습니다.

[🔎 직전 단계 전체 비교·구성](../revision-diffs/paper-1.diff) · [📋 전체 파일 크기·해시](../revision-manifests/paper-1.json)

<details>
<summary>📎 이 단계의 파일 기록과 전체 해시</summary>

아래 표는 해당 단계가 기록될 당시의 파일 정보입니다. 현재 첨부는 [프로젝트 자료 안내](../PAPERS.md)에서 확인할 수 있습니다.

| 파일 | 종류 | 바이트 | SHA-256 |
|---|---|---:|---|
| `원고단계/1차/06.17_원고.pdf` | .pdf | 990860 | `2cbeeb844d29e0b2ff9678e53af9e125ddac87f5cdc44262e984203891afa99f` |
| `원고단계/1차/06.29_영문_원고.pdf` | .pdf | 390409 | `5ffd68fd8e8cffa632d2f9ec30cdb96481f26507ae54110076fc3bd1f1645b71` |
| [최신 편집 원문](../../%EB%85%BC%EB%AC%B8/%EC%B5%9C%EC%A2%85_%EC%9B%90%EB%AC%B8_%EB%85%BC%EB%AC%B8.hwp) | .hwp | 1359360 | `76d62566214e255710bfcd65a195238fc8d06fafa56be8245c0ef391ba724752` |
| [최신 편집 원문](../../%EB%85%BC%EB%AC%B8/%EC%B5%9C%EC%A2%85_%EC%9B%90%EB%AC%B8_%EB%85%BC%EB%AC%B8.hwp) | .hwp | 858112 | `884e8c7373aa44f1cdf2bb7327bfd4132414e6f18a33f589dc1f9735a7c60656` |
| [원고단계/1차/mainDocument-1[26M-07-082]-Original_1.hwp](../../%EC%9B%90%EA%B3%A0%EB%8B%A8%EA%B3%84/1%EC%B0%A8/mainDocument-1%5B26M-07-082%5D-Original_1.hwp.md) | .hwp | 262144 | `c0c6ed9a59d60c7687e4a91d028e05f53f9e19738ad34ddb3ce168f387f0d982` |
| [최신 편집 원문](../../%EB%85%BC%EB%AC%B8/%EC%B5%9C%EC%A2%85_%EC%9B%90%EB%AC%B8_%EB%85%BC%EB%AC%B8.hwp) | .hwp | 286208 | `a7a1c23e62df80ee179f456186ff2ccf0b412f79c90dd7b68566ed572c34545d` |
| [최신 편집 원문](../../%EB%85%BC%EB%AC%B8/%EC%B5%9C%EC%A2%85_%EC%9B%90%EB%AC%B8_%EB%85%BC%EB%AC%B8.hwp) | .hwp | 282624 | `dc3b2ed80ba74003b4cfa57ed5e23be51e1d77a522579b5278b579d1d914e481` |
| [최신 편집 원문](../../%EB%85%BC%EB%AC%B8/%EC%B5%9C%EC%A2%85_%EC%9B%90%EB%AC%B8_%EB%85%BC%EB%AC%B8.hwp) | .hwp | 125440 | `78222e462610a4f63ad57ce96eab1ca7f386ad30334bcca2276b604c8f14cfdb` |
| `원고단계/관련문서/1차/희찬이 형 논문 그림/논문 그림.pptx` | .pptx | 406977 | `9836bb2573d21d417a08edcedffeccc617b49d40e083b3295da9144a781111e7` |
| [원고단계/1차/그림/논문 그림.pptx](../../%EC%9B%90%EA%B3%A0%EB%8B%A8%EA%B3%84/1%EC%B0%A8/%EA%B7%B8%EB%A6%BC/%E1%84%82%E1%85%A9%E1%86%AB%E1%84%86%E1%85%AE%E1%86%AB%20%E1%84%80%E1%85%B3%E1%84%85%E1%85%B5%E1%86%B7.pptx) | .pptx | 406977 | `9836bb2573d21d417a08edcedffeccc617b49d40e083b3295da9144a781111e7` |
| [원고단계/1차/그림/그림1.png](../../%EC%9B%90%EA%B3%A0%EB%8B%A8%EA%B3%84/1%EC%B0%A8/%EA%B7%B8%EB%A6%BC/%EA%B7%B8%EB%A6%BC1.png) | .png | 21190 | `97d5f42dcb92f7f411a0d0f4e75872e7e12c7cab4143ba8e4676054f4b61d87b` |
| [원고단계/1차/그림/그림10.png](../../%EC%9B%90%EA%B3%A0%EB%8B%A8%EA%B3%84/1%EC%B0%A8/%EA%B7%B8%EB%A6%BC/%EA%B7%B8%EB%A6%BC10.png) | .png | 110487 | `4a518bc608a8351006efa09285f7958d0b1cf186cd82bfcf756c807ce3c93ccf` |
| [원고단계/1차/그림/그림2.png](../../%EC%9B%90%EA%B3%A0%EB%8B%A8%EA%B3%84/1%EC%B0%A8/%EA%B7%B8%EB%A6%BC/%EA%B7%B8%EB%A6%BC2.png) | .png | 226711 | `102a5875e58a27da7dcefe30d6046471b2734321b437cc8e5fdd12067bcadd00` |
| [원고단계/1차/그림/그림3.png](../../%EC%9B%90%EA%B3%A0%EB%8B%A8%EA%B3%84/1%EC%B0%A8/%EA%B7%B8%EB%A6%BC/%EA%B7%B8%EB%A6%BC3.png) | .png | 107576 | `6692573be67dd04dd92ffef7a8e996d99e1e04d3317cf9b86d40a8c66eaff1b5` |
| [원고단계/1차/그림/그림4.png](../../%EC%9B%90%EA%B3%A0%EB%8B%A8%EA%B3%84/1%EC%B0%A8/%EA%B7%B8%EB%A6%BC/%EA%B7%B8%EB%A6%BC4.png) | .png | 37464 | `2759ef8c71dc5aaa26a4ee5d2829f6f4ff36cd94a7b8320829c14a8b544be05d` |
| [원고단계/1차/그림/그림5.png](../../%EC%9B%90%EA%B3%A0%EB%8B%A8%EA%B3%84/1%EC%B0%A8/%EA%B7%B8%EB%A6%BC/%EA%B7%B8%EB%A6%BC5.png) | .png | 18109 | `31fc8d8ab585cedfd7d7f6ddc3b624040cc9701a3ed3915a57e1dc0b633a1d7d` |
| [원고단계/1차/그림/그림6.png](../../%EC%9B%90%EA%B3%A0%EB%8B%A8%EA%B3%84/1%EC%B0%A8/%EA%B7%B8%EB%A6%BC/%EA%B7%B8%EB%A6%BC6.png) | .png | 59047 | `17398d61ac5be83e00b3ade53a4e9e90ee6fd3e3b13d251d222f6e57b2b59955` |
| [원고단계/1차/그림/그림7.png](../../%EC%9B%90%EA%B3%A0%EB%8B%A8%EA%B3%84/1%EC%B0%A8/%EA%B7%B8%EB%A6%BC/%EA%B7%B8%EB%A6%BC7.png) | .png | 95822 | `55a6fde9d752c09c3693e066559db00beff6867e382bb154b22b67f972d1be48` |
| [원고단계/1차/그림/그림8.png](../../%EC%9B%90%EA%B3%A0%EB%8B%A8%EA%B3%84/1%EC%B0%A8/%EA%B7%B8%EB%A6%BC/%EA%B7%B8%EB%A6%BC8.png) | .png | 112486 | `0a7b6f63201f8da42861f28d1c40c44689e10eb9d2511e65c9c8dc0222e8b649` |
| [원고단계/1차/그림/그림9.png](../../%EC%9B%90%EA%B3%A0%EB%8B%A8%EA%B3%84/1%EC%B0%A8/%EA%B7%B8%EB%A6%BC/%EA%B7%B8%EB%A6%BC9.png) | .png | 143451 | `65c4b6c50432d9bd3d94542a8d2e4e27d538795caf31e3c508afc449dc3951bd` |

</details>

---

[🏠 프로젝트](../../README.md) · [🗂️ 전체 차수](../REVISION_INDEX.md) · [📁 자료 폴더](../../%EC%9B%90%EA%B3%A0%EB%8B%A8%EA%B3%84/1%EC%B0%A8) · [➡️ 2차 원고](paper-2.md)
