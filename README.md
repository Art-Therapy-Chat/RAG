# RAG

## 🚀 프로젝트 개요 (Overview)

이 프로젝트는 RAG를 활용하여 사용자의 텍스트 혹은 이미지를 입력하면 입력한 질문으로 연관된 문서를 검색하고, 그 검색 결과를 바탕으로 답변을 하는 기술입니다.

## ✨ RAG 챗봇의 구조 (Architecture)

<img width="2206" height="674" alt="image" src="https://github.com/user-attachments/assets/8604cab2-f936-412e-a865-cdb98e1d1bde" />


## 🤖 사용된 모델 및 기술 스택 (Models & Tech Stack)

이 프로젝트에서는 이미지 분석 및 캡션 생성을 위해 다음과 같은 최신 인공지능 모델과 기술을 사용했습니다.

### 모델 아키텍처

-   **YOLOv8**: 이미지 내 객체를 탐지하고 바운딩 박스와 클래스 확률을 제공하여, 이를 다른 캡션 모델의 입력으로 활용합니다. 예를 들어 '나무전체', '수관', '꽃', '열매', '기둥' 등을 정확하게 식별합니다. [【1】](about:blank)
-   **GPT-4o (OpenAI)**: YOLO 탐지 정보를 포함한 프롬프트를 사용하여 이미지를 자세하고 간결하게 설명하는 데 활용됩니다. 이를 통해 보다 문맥적이고 정확한 캡션을 생성합니다. [【1】](about:blank)[【3】](about:blank)
-   **Kosmos-2**: 이미지 캡션 생성에 사용된 또 다른 Vision-Language 모델입니다. 생성된 캡션의 추가적인 정리 과정을 통해 품질을 높입니다. [【2】](about:blank)[【5】](about:blank)
-   **BLIP (Bootstrapping Language-Image Pre-training)**: 이미지 캡션의 기본 성능을 제공하는 모델 중 하나로, 다른 모델들과의 비교를 위해 사용됩니다. [【4】](about:blank)
-   **InstructBLIP**: BLIP의 지시 추론 능력을 강화한 모델로, 상세한 캡션을 생성하며 비교 대상 모델로 활용됩니다. [【4】](about:blank)
-   **CLIP Interrogator**: 이미지의 시각적 특징을 기반으로 다양한 키워드와 스타일을 조합하여 프롬프트를 생성하거나 캡션을 제공하는 데 사용됩니다. [【4】](about:blank)

### 주요 기술 및 라이브러리

-   **Python**: 프로젝트의 주요 개발 언어.
-   **OpenAI API**: GPT-4o 모델과의 연동 및 활용.
-   **Hugging Face Transformers**: BLIP, InstructBLIP, Kosmos-2 등 다양한 VLM 모델의 불러오기 및 사용.
-   **Pillow (PIL)**: 이미지 처리 및 관리를 위한 라이브러리.
-   **google-colab / userdata**: Colab 환경에서 API 키를 안전하게 관리하고 개발을 진행합니다.
