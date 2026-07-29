# 🛒 Shopping List App

바닐라 JavaScript로 만든 간단한 쇼핑 리스트 웹앱입니다. 별도의 빌드 과정 없이 `index.html` 파일 하나로 동작하며, 데이터는 Supabase 데이터베이스에 저장됩니다.

## 기능

- 항목 추가 / 삭제
- 체크박스로 구매 완료 표시 (취소선 처리)
- 전체 개수 · 완료 개수 카운터
- Supabase 데이터베이스에 자동 저장 (어느 기기·브라우저에서 접속해도 동일한 목록 유지)

## 사용 방법

`index.html` 파일을 브라우저에서 열면 바로 사용할 수 있습니다. Supabase 프로젝트의 `shopping_items` 테이블과 연동되어 있으며, 접속 URL과 publishable 키는 `index.html` 상단에 설정되어 있습니다.

## 데이터베이스 구조

`shopping_items` 테이블:

| 컬럼 | 타입 | 설명 |
| --- | --- | --- |
| `id` | `bigint` (identity) | 기본 키 |
| `text` | `text` | 항목 이름 |
| `checked` | `boolean` | 구매 완료 여부 |
| `created_at` | `timestamptz` | 생성 시각 |

## 기술 스택

- HTML / CSS / Vanilla JavaScript
- [Supabase](https://supabase.com/) (PostgreSQL, `@supabase/supabase-js`)
