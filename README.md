# RAG

## 🚀 프로젝트 개요 (Overview)

이 프로젝트는 RAG를 활용하여 사용자가 이미지를 그리면 이미지에 대한 캡션을 생성한 후 심리 해석본을 활용한 결과를 바탕으로 답변을 하는 기술입니다.

## ✨ RAG 챗봇의 구조 (Architecture)

<img width="2206" height="674" alt="image" src="https://github.com/user-attachments/assets/8604cab2-f936-412e-a865-cdb98e1d1bde" />


## 🤖 사용된 모델 및 기술 스택 (Models & Tech Stack)

이 프로젝트에서는 이미지 분석 및 캡션 생성을 위해 다음과 같은 최신 인공지능 모델과 기술을 사용했습니다.

### 모델 아키텍처

-   **BAAI/bge-m3**:
        -  BGE‑M3는 BAAI에서 개발한 다목적 임베딩 모델로, dense, multi-vector, sparse 방식의 검색 기능을 하나의 모델에서 통합한다.
        -  다국어 모델을 지원하므로 임베딩 모델을 파인튜닝하기 위한 베이스 모델로 사용하였다.
-   **klue/bert-base**:
        -   KLUE(Benchmark)의 일부로 사전훈련된 한국어 BERT 모델로 크로스 인코더를 파인튜닝 하기 위해 사용하였다.
-   **BAAI/bge-reranker-v2-m3**:
        -   BGE‑Reranker‑v2‑M3는 BAEI BGE 계열의 Cross-encoder 리랭커 모델이다.
        -   경량이면서도 다국어 지원이 강하고, 빠른 추론이 가능하다.
        -   BGE-M3 임베딩 모델을 기반(backbone)으로 사용하여 쿼리-문장 쌍의 관련성 점수를 계산하였기 때문에 파인튜닝한 임베딩 모델의 리랭커 모델로 적합하다고 판단하여 사용하였다.


### 주요 기술 및 라이브러리

-   **Python**: 프로젝트의 주요 개발 언어.
-   **OpenAI API**: GPT-4o 모델과의 연동 및 활용.
-   **Hugging Face Transformers**: BLIP, InstructBLIP, Kosmos-2 등 다양한 VLM 모델의 불러오기 및 사용.
-   **Pillow (PIL)**: 이미지 처리 및 관리를 위한 라이브러리.
-   **google-colab / userdata**: Colab 환경에서 API 키를 안전하게 관리하고 개발을 진행합니다.
