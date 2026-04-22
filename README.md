# shared-bench-schema

`공통 결과 스키마`를 조직 공통 자산으로 분리한 인프라 저장소입니다. 실험, 벤치마크, 앱 저장소가 동일한 결과 구조와 리포팅 규칙을 사용하도록 기준 스키마와 템플릿을 제공합니다.

## 저장소 역할
- 원시 결과 JSON의 구조를 표준화해 저장소 간 비교 가능성을 유지합니다.
- `RESULTS.md`와 예제 결과 파일의 최소 형식을 제공해 문서 품질 편차를 줄입니다.
- 각 프로젝트가 독자 포맷을 만들지 않도록 공통 스키마의 단일 source of truth 역할을 합니다.

## 우선순위
- P0

## 포함 내용
- `schemas/ai-webgpu-lab-result.schema.json`
- `templates/example-result.json`
- `templates/RESULTS-template.md`
- `docs/RESULT-RULES.md`

## 사용 방식
- 실험, 벤치마크, 앱 저장소는 이 저장소의 스키마와 템플릿을 기준으로 결과 파일을 복제합니다.
- `reports/raw/` 아래 JSON 산출물은 이 스키마와 일치해야 합니다.
- 결과 보고 규칙이 변경되면 개별 저장소 README/RESULTS 규칙도 함께 갱신해야 합니다.

## 완료 기준
- 새 결과 필드가 필요할 때 스키마, 예제, 결과 규칙 문서가 함께 업데이트됩니다.
- 공통 템플릿 변경이 실험/벤치/App 저장소의 실제 운영 흐름과 충돌하지 않습니다.
- 임의 포맷이 아니라 재현 가능한 결과 산출 구조를 유지합니다.

## 관련 저장소
- `docs-lab-roadmap` - 계획 문서와 리포팅 정책 기준
- `shared-github-actions` - CI에서 스키마 검증을 붙일 공통 액션 대상
- `tpl-webgpu-vanilla`, `tpl-webgpu-react` - 새 프로젝트가 가져갈 기본 출발점

## 라이선스
MIT
