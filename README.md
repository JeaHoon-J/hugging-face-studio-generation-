# 인물 보존형 AI 가상 배경 스튜디오 (Hugging Face)


## 🛠️ Model Stack (AI 모델 구성)


| 단계 | 모델명 | 역할 | 설명 |
| :-- | :--- | :--- | :--- |
| **1. 누끼** | `briaai/RMBG-1.4` | **Background Removal** | 이미지 세분화(Segmentation) 기술을 통해 전경(물체/사람)과 배경을 정교하게 분리합니다. |
| **2. 가이드** | `ControlNet (Canny/Depth)` | **Edge Extraction** | 원본 이미지의 윤곽선이나 구조를 추출하여, 새로운 이미지가 생성될 때 형태가 뒤틀리지 않게 가이드를 제공합니다. |
| **3. 번역** | `Helsinki-NLP/opus-mt-ko-en` | **Prompt Translator** | 한국어 자연어 입력을 Stable Diffusion이 이해할 수 있는 영어 프롬프트로 변환합니다. |
| **4. 생성** | `Stable Diffusion` | **Image Generation** | 번역된 텍스트와 ControlNet의 가이드를 결합하여 고해상도의 새로운 배경 이미지를 생성 및 합성합니다. |

## 🚀 Key Features (주요 기능)

- **Native Language Support**: 영어 번거로움 없이 한국어로 직접 명령(예: "배경을 우주 공간으로")이 가능합니다.
- **State-of-the-Art Segmentation**: `RMBG-1.4`를 사용하여 머리카락 한 올까지 섬세한 배경 제거가 가능합니다.
- **Structural Integrity**: ControlNet을 적용하여 단순 배경 합성을 넘어, 원본 피사체와 자연스럽게 어우러지는 결과물을 만듭니다.

<img width="1108" height="690" alt="가상 배경 생성 결과" src="https://github.com/user-attachments/assets/4831b2d2-772b-41e6-80da-42661823a581" />
