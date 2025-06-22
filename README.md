# 🛠️ PCB Defect Classification using OpenCV (Rule-based, 6 Classes)

본 프로젝트는 PCB(Printed Circuit Board) 기판 이미지에서 발생하는 **6가지 유형의 불량을 전통적인 이미지 처리 기법을 활용해 자동 분류**하는 시스템입니다.  
딥러닝 없이도 실제 검사 환경에서 적용 가능한 수준의 분류 정확도를 달성하는 것을 목표로 하였으며, **SIFT 기반 이미지 정합과 형상/밝기 기반 분석**, 그리고 **조건 기반(rule-based) 분류 방식**을 통해 각 이미지의 불량 유형을 식별합니다.

📌 **최종 결과: 과제 내 전체 참가자 중 2등 성적 달성**  


---
<img width="674" alt="Image" src="https://github.com/user-attachments/assets/4a63504d-4820-4474-9f39-4d82227d6018" />
## 🧪 핵심 기능 요약

- 기준 이미지와 검사 이미지 간 **SIFT 특징점 기반 정합**
- 정합 실패 시 **대비 향상(CLAHE, 히스토그램 균등화, 감마 보정)** 후 재시도
- 기준 이미지와 정렬된 검사 이미지 간 **차이 영역 검출 및 마스크 처리**
- 단일 결함에 대해:
  - **밝기 비교**
  - **형상 기반 특징 추출** (이심률, 면적 비율, 사각형 유사도, 중심 거리 등)
  - **컨투어 정보** 활용
- **불량 분류 기준에 따른 조건문(Rule-based Decision Tree)** 방식으로 6가지 유형 판단:
  - `missing_hole`
  - `mouse_bite`
  - `open_circuit`
  - `short`
  - `spur`
  - `spurious_copper`

---

