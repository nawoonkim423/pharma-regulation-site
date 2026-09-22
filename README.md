# 제약 규제 업데이트

FDA·식약처·EMA·MHRA·PIC/S 등 규제기관의 공식 게시물(Warning Letter, Form 483 관찰사항,
실사 결과, 회수·처분, 가이드라인)을 매일 자동으로 모아 검색 가능한 형태로 정리하는
개인 프로젝트입니다.

**사이트**: https://nawoonkim423.github.io/pharma-regulation-site/

## 왜 만들었나

처음에 GMP와 규제를 공부하면서, 이론만 보기보다 실제 사례를 직접 찾아보고 싶었습니다.
그래서 식약처·FDA·EMA 같은 사이트를 하나하나 들어가서 확인했는데, 매번 반복하려니
번거롭고 꾸준히 챙겨보기가 쉽지 않았습니다.

그래서 수집과 정리를 자동화해서 매일 규제 동향을 확인하는 걸 지속 가능하게 만들었습니다.
비슷한 사례를 한데 모아 보고, 통계로 어떤 부분을 자주 지적받는지 파악할 수 있으면
좋겠다는 생각도 있었습니다.

## 어떻게 쓰나

- 회사명·키워드·CFR 조항으로 검색해서 관련 실사·처분·가이드라인 바로 찾기
- 기관별·유형별 통계로 어떤 지적사항이 자주 나오는지 흐름 보기
- 최근 30일 중요도 높은 자료만 모은 우선 검토 목록
- 매일 자동 수집되어 별도로 관리하지 않아도 최신 상태 유지

## 수집 범위

식약처 처분·회수·법령·공지, FDA 경고서·Form 483 관찰사항·OAI·회수·공고, EMA·MHRA·PIC/S와
TGA·PMDA·NMPA·ANVISA의 공개 자료를 보관합니다. FDA는 openFDA(의약품 회수)와 Data
Dashboard API(Warning Letter·483 관찰사항·실사 분류·수입거부)를 공식 API로 사용합니다.

우선순위 주제: GMP, Data Integrity, CSV, Annex 1/11, 무균공정, 밸리데이션, 일탈·CAPA

전 기관의 모든 규제 발생 건수를 뜻하지 않으며, 수집 범위와 한계는 사이트의
[출처·수집 범위](https://nawoonkim423.github.io/pharma-regulation-site/sources/) 페이지에
그대로 공개해 두었습니다.

## 구조

이 저장소에는 빌드 결과물만 들어옵니다. 수집·분석 코드는 비공개 저장소
[`pharma-regulation`](https://github.com/nawoonkim423/pharma-regulation)에 있고, 매일
GitHub Actions가 데이터를 수집해 Claude로 요약한 뒤 이 저장소로 정적 사이트를 배포합니다.
(GitHub Free 플랜은 비공개 저장소에 Pages를 쓸 수 없어 배포용 저장소만 분리했습니다.)
