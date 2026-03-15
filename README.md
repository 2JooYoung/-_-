## Jupyter Notebook 개인정보 일괄 제거 스크립트

- **remove_personal_info.py**  
  `.ipynb` 파일 첫 셀에 포함된 학과/학번/이름을 자동으로 탐지해 일괄 삭제하는 스크립트

---

## About
수업에서 제출한 Jupyter Notebook 약 30개에 개인정보가 반복 포함되어 있어,
수동 수정 대신 Python 스크립트로 자동화했습니다.

- `.ipynb`가 JSON 구조임을 파악해 파싱 방식으로 접근
- `glob`으로 폴더 내 파일 재귀 탐색 후 일괄 처리
- 정규표현식으로 학과/학번/이름 패턴만 정확히 감지해 제거
- 트러블슈팅 경험 포함 (경로 오류 디버깅)
```bash
python remove_personal_info.py
```

---

## Tech Stack
- Python 3
- json / glob / re (표준 라이브러리)
