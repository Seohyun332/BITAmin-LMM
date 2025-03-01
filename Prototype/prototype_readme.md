### Prototype

- RDM_Kandinsky_Prototype.ipynb
    - Colab 환경에서 DB 검색 과정을 통한 reference image vector를 이미지 생성에 반영할 수 있도록 제작.
    - Kandinsky 모델을 활용하여 검색을 통해 조건을 부여할 시 생성 성능을 확인하고자 함.

- pipeline_kandinsky_prior_up.py
    - KandinskyPriorPipeline을 수정하여 CLIP 모델을 활용해 임베딩 된 벡터도 조건 전처리에 넣을 수 있도록 수정