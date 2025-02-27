# 🖼️ RDM을 통한 생성 이미지 성능 향상  

## **🌟 프로젝트 개요**  

### ✅ 프로젝트 목표  
- **Retrieval-Augmented Diffusion Model (RDM)**을 활용하여 생성 이미지의 **디테일과 품질 향상**  
- **서브 쿼리 분할**을 통한 생성 이미지의 정교화  
- **DB 검색 성능 개선**을 통한 RAG 기반 이미지 생성 연구  
- **광고 이미지 생성** 및 **광고 의도 반영**을 위한 프로토타입 개발  

---

## **👥 Team Members**  

| 기수  | 팀원 |
|------|------|
| **14기** | 김민열, 김홍재, 우동협 |
| **15기** | 이지영, 황서현 |

---

## **📅 진행 기간**  
**2025.01.11 ~ 2025.02.22**  

---

## **🔍 연구 내용 및 방법**  

### 🚀 **RAG 기반 RDM 기법 연구**  
> **Retrieval-Augmented Generation (RAG)** 개념을 **Latent Diffusion Model (LDM)**과 결합하여 검색 및 생성 과정 개선  

1. **서브 쿼리 기반 검색 성능 향상**  
   - 단일 입력 텍스트를 세부 **서브 쿼리로 분할**하여 Retrieve 성능 개선  
   - 유사도 검증을 통한 검색 이미지 필터링  

2. **모델 생성 성능 향상을 위한 DB 구성**  
   - 검색된 이미지를 조건부로 삽입하여 모델 성능 개선  
   - FAISS 기반 이미지 벡터 DB 구축  

3. **광고 이미지 생성 최적화**  
   - 광고주의 의도를 텍스트로 반영한 프로토타입 제작  
   - 촬영한 이미지에 대한 다양한 바리에이션 적용  
   - 높은 품질과 요구(쿼리) 충족도가 필요한 이미지 생성  

---

## **🛠️ 알고리즘 개요**  

![RDM Algorithm](https://user-images.githubusercontent.com/your-image-link.png)  

---

## **🤖 RDM (Retrieval-Augmented Diffusion Model)**  

RDM은 **RAG (Retrieval-Augmented Generation) 개념을 활용하여 Latent Diffusion Model (LDM)에서 이미지 품질을 향상**시키는 기법입니다.  
기존의 텍스트-이미지 생성 방식에 검색 기능을 추가하여 보다 정교한 데이터 활용이 가능하도록 개선하였습니다.  

### 🔨 **수정 사항**  
✅ Hugging Face의 **KandinskyPriorPipeline**을 수정하여 **DB에서 검색한 데이터를 입력으로 받을 수 있도록 구조 변경**  
✅ 기존의 **텍스트 & 이미지 입력 구조**를 수정하여 **검색 기능 추가 시 성능 개선 여부 확인**  
✅ 검색된 데이터를 생성 과정에 반영할 수 있도록 **조건부 삽입 기능 추가**  

---

## **📊 데이터 수집 (FAISS 기반 이미지 벡터 DB 구축)**  

| 데이터 종류 | 개수 | 출처 |
|-----------|----|----|
| 동물 이미지 | 500장 | Unsplash |
| 배경 이미지 | 300장 | Unsplash |
| 동물과 사람이 함께 나온 이미지 | 500장 | Unsplash |

➡️ **FAISS를 활용하여 벡터 DB 구축 후 이미지 검색 최적화**  

---

## **📌 Repository Structure**  
```bash
📂 RDM-Image-Generation
│── 📂 data/               # 이미지 데이터셋
│── 📂 models/             # 수정된 KandinskyPriorPipeline 코드
│── 📂 retrieval/          # FAISS 기반 검색 코드
│── 📂 experiments/        # 실험 및 결과 분석
│── 📂 results/            # 생성된 이미지 및 성능 비교
│── README.md             # 프로젝트 개요 및 진행 내용
