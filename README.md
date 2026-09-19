**엔터프라이즈 프라이빗 클라우드와 Private AI를 전략, 플랫폼, 앱과 에이전트 서비스까지 현장에서 바로 참고할 수 있게 정리한 실무 가이드.**
Modern Private Cloud(VCF), Private AI(PAIF / PAIS), Enterprise AI Transformation(AX)

### 가이드 구성

세 가이드는 **전략 → 플랫폼 → 실행** 순서로 구성되어 있습니다. 문서는 모두 94편이며, 가이드 사이에 관련 문서 링크를 두어 필요한 부분만 골라 읽을 수 있습니다. 1번 가이드는 특정 제품이나 실행 환경을 전제하지 않습니다. 문제를 정의하고 검증한 뒤 실행 환경으로 사내 구축을 선택한 경우에 2번과 3번으로 이어집니다.

| 1. 전략 → | 2. 플랫폼 → | 3. 실행 |
|---|---|---|
| **[기업용 AX 방법론](https://github.com/JaeHoYun/enterprise-ax-methodology)**<br>벤더 중립, 9편 | **[VCF Private AI 인프라](https://github.com/JaeHoYun/vcf-private-ai)**<br>PAIF / PAIS, Primer 포함 70편 | **[VCF Private AI 앱과 에이전트 서비스](https://github.com/JaeHoYun/vcf-private-ai-apps)**<br>15편 |
| 출발점 → 문제 정의 → 검증 → 해결 경로와 실행 환경 → 조직과 확장 | 인프라 → 데이터 → 서빙 → RAG, 보안, 사이징, 통합 설계 | 기획과 선정 → 설계 → 구축 → 검증과 출시 → 운영과 종료 |
| 무엇이 문제이고, 누가 어디서 풀 것인가 | 사내에 구축한다면 어떤 인프라로 구현할 것인가 | 그 위에서 어떤 서비스를 만들 것인가 |

1. **[기업용 AX 방법론 가이드](https://github.com/JaeHoYun/enterprise-ax-methodology)** — 전략. AX 착수 전 단계의 큰 그림을 벤더 중립으로 안내합니다. 중심은 문제 정의입니다. 조직의 출발점을 네 유형으로 가리고, 일곱 가지 시선으로 문제를 찾고, 왜 지금까지 못 풀었는가와 AI가 아니어도 풀리는가라는 두 관문 질문을 거쳐 문제를 정의한 뒤 작게 검증합니다. 누가 풀 것인가(내부 개발, 외부 전문가와 FDE, 솔루션 구매, SI 위탁)와 어디서 돌릴 것인가(퍼블릭, 온프렘, 혼합)는 그다음의 선택지로 같은 무게로 다루며, 이 접근이 맞지 않는 조건도 함께 적었습니다. 컨설팅을 대체하지 않고 채워 쓰는 양식을 두지 않는 대신, 끝까지 채운 가상 예시를 본문에 실었습니다. 06장에서 사내 구축을 선택한 경우에 2번 가이드와 연결됩니다.
2. **[VCF Private AI (PAIF) 인프라 가이드](https://github.com/JaeHoYun/vcf-private-ai)** — 플랫폼. VCF 9.1.x PAIF 플랫폼(PAIS 3.0)의 구축과 운영을 인프라, 벡터 DB, 서빙 API, RAG, 보안과 거버넌스, 사이징과 비용, 통합 설계의 일곱 편으로 나누어 다룹니다. AI와 쿠버네티스가 익숙하지 않은 인프라 담당자를 위한 입문(Primer) 편도 있습니다. 이미 AI 자산을 운영 중인 조직을 위한 채워 쓰는 양식(자산 인벤토리, 6R 처분 매트릭스, FinOps 스코어카드, 거버넌스와 데이터주권 갭)은 이 가이드의 ⑤, ⑥, ⑦에 있습니다.
3. **[VCF Private AI 앱과 에이전트 서비스 가이드](https://github.com/JaeHoYun/vcf-private-ai-apps)** — 실행. PAIF 플랫폼 위에서 LLM 앱, RAG 앱, 배치 파이프라인, 에이전트 서비스를 기획, 설계, 구축, 검증, 운영하는 방법을 서비스 수명주기 순서로 다룹니다. 어떤 업무에 적용해야 효과가 있는지와 위험 등급 판정에서 시작해, 사용자 신원 전파, 게이트웨이와 토큰 예산 소비, 문서보안이 걸린 문서의 인입, 사내 시스템 쓰기 설계, PAIS 3.0 Agent Builder와 MCP 구현, 서비스 보안 준비와 출시 심사, 운영과 퇴역까지 앱 팀이 실제로 정해야 하는 것을 다룹니다.

### 상황별 추천 순서

**전략** — 무엇이 문제이고 누가 어디서 풀지 정하는 단계입니다. 들어가는 길은 AX 01장의 상태 유형에 따라 갈립니다.

| 상황 | 먼저 읽을 문서 | 다음 문서 |
|---|---|---|
| AI 전환을 어디서부터 시작할지 정해야 하는 기획 담당자 | [AX 00 오리엔테이션](https://github.com/JaeHoYun/enterprise-ax-methodology/blob/main/docs/00-orientation.md) → 01 출발점 판별 → 02 문제를 보는 시선 → 03 문제 정의 | 04 검증 방식 → 05 해결 경로 선택 → 06 실행 환경 선택 |
| 큰 그림만 빠르게 잡으려는 임원 | [AX 00 오리엔테이션](https://github.com/JaeHoYun/enterprise-ax-methodology/blob/main/docs/00-orientation.md)과 01–08장 첫머리의 요약 | 03 문제 정의의 3.7절 가상 예시 → 04의 4.6절 투자 판단 |
| 문제는 오래전부터 아는데 조직 구조, 권한, 데이터 소유 때문에 손대지 못하는 조직 | [AX 01 출발점 판별](https://github.com/JaeHoYun/enterprise-ax-methodology/blob/main/docs/01-starting-point.md)(1.2.3절) | 03 문제 정의(3.3절 구조적 장애와 누구의 의제로 올릴지) |
| 외부 전문가(FDE), 솔루션 구매, SI 위탁 가운데 누구에게 맡길지 정해야 하는 담당자 | [AX 05 해결 경로 선택](https://github.com/JaeHoYun/enterprise-ax-methodology/blob/main/docs/05-solve-path.md) | 04 검증 방식(4.3절 파일럿 단계의 경로) → 07의 7.1절 현업 오너 |
| 퍼블릭과 온프렘 가운데 어디서 돌릴지, 이미 클라우드에 있는 것을 되돌릴지 정해야 하는 담당자 | [AX 06 실행 환경 선택](https://github.com/JaeHoYun/enterprise-ax-methodology/blob/main/docs/06-execution-environment.md) | Private AI 06 사이징 07의 7.6절 비교 프레임 → 07 통합 설계 08의 8.5절 온프렘 회귀 판정 |
| 이미 AI 도구를 여럿 쓰고 있어 정비가 필요한 조직 | [AX 01 출발점 판별](https://github.com/JaeHoYun/enterprise-ax-methodology/blob/main/docs/01-starting-point.md)(1.4절 이미 AI를 쓰고 있는 조직) | 07 조직, 정착, 통제(7.6절 섀도 AI의 양성화) → Private AI 07 통합 설계의 [워크시트 03 자산 인벤토리](https://github.com/JaeHoYun/vcf-private-ai/blob/main/07-design/worksheet/03-ai-estate-inventory.md)와 04 6R 처분 → 06 사이징 부록 A4 FinOps 스코어카드 |
| AI 기본법과 금융 AI 가이드라인 대응을 준비하는 컴플라이언스, 법무 담당자 | [AX 07 조직, 정착, 통제](https://github.com/JaeHoYun/enterprise-ax-methodology/blob/main/docs/07-organization-and-control.md)(7.5절, 7.8절) → [부록 A2 국내 규제 타임라인](https://github.com/JaeHoYun/enterprise-ax-methodology/blob/main/appendix/A2-kr-regulatory-timeline.md) | Private AI 05 보안 07의 7.4.3절과 [거버넌스와 데이터주권 갭 워크시트](https://github.com/JaeHoYun/vcf-private-ai/blob/main/05-security/worksheet/governance-sovereignty-gap.md) → 앱 가이드 11의 11.6절 고지 → 13의 13.10절 출시 심사 패키지 |

**플랫폼** — Private AI 플랫폼을 세우고 보호하고 산정하는 단계입니다.

| 상황 | 먼저 읽을 문서 | 다음 문서 |
|---|---|---|
| 가상화는 익숙하지만 AI와 쿠버네티스는 처음인 인프라 엔지니어 | [Private AI 입문(Primer)](https://github.com/JaeHoYun/vcf-private-ai/tree/main/00-foundations) | 01 인프라 → 06 사이징 → 07 통합 설계 |
| PAIF 플랫폼 구축과 운영을 맡은 인프라, 플랫폼팀 | [Private AI 01 인프라](https://github.com/JaeHoYun/vcf-private-ai/tree/main/01-infra) | 02 벡터 DB → 05 보안 → 06 사이징 → 07 통합 설계 |
| 보안 때문에 플랫폼 전체를 어떻게 설계하고 어디서부터 시작할지 정해야 하는 보안, 플랫폼 담당자 | [Private AI 05 보안 00 어디서부터 시작하나](https://github.com/JaeHoYun/vcf-private-ai/blob/main/05-security/docs/00-where-to-start.md) | 05 보안 08 에이전트 거버넌스 → 앱 가이드 12 서비스 보안 준비 |
| 운영 중인 플랫폼을 VCF 9.1.1 / PAIS 3.0으로 업그레이드하는 운영자 | [Private AI 01-infra 00 What's New](https://github.com/JaeHoYun/vcf-private-ai/blob/main/01-infra/docs/00-whats-new.md) | 01-infra 10 운영 → 앱 가이드 14 운영 |

**실행** — 그 플랫폼 위에서 서비스 하나를 만들고 책임지는 단계입니다.

| 상황 | 먼저 읽을 문서 | 다음 문서 |
|---|---|---|
| 사내 API로 LLM, RAG 앱을 만드는 개발자 | [Private AI 03 서빙 API](https://github.com/JaeHoYun/vcf-private-ai/tree/main/03-serving-api) | 04 RAG → 앱 가이드 00–03 → 08 |
| 에이전트 도입 여부와 적용 업무를 검토하는 담당자 | [앱 가이드 02 어디에 쓰나](https://github.com/JaeHoYun/vcf-private-ai-apps/blob/main/docs/02-use-cases.md) | AX 03 문제 정의 → 앱 가이드 03 설계 패턴 |
| 앱 팀이 플랫폼 위에서 첫 서비스를 기획부터 출시까지 만든다 | [앱 가이드 00 개관](https://github.com/JaeHoYun/vcf-private-ai-apps/blob/main/docs/00-orientation.md) → 02 어디에 쓰나 | 04–07 설계 → 08–11 구축 → 12–13 검증과 출시 → 14 운영 |

### 다루는 질문

- 과제가 산적한 조직은 어떤 시선으로 문제를 찾고 어떻게 정의하는가 (AX 02, 03)
- 이 문제는 왜 지금까지 못 풀었고, AI가 아니어도 풀리는 것은 아닌가 (AX 03의 3.3절, 3.4절)
- 파일럿을 계속할지 멈출지는 무엇으로 판정하고, 단일 ROI 숫자 없이 투자 판단은 어떻게 받는가 (AX 04)
- 외부 전문가나 FDE에게 맡길 때 무엇을 미리 정해야 끝난 뒤 사내에 주인이 남는가 (AX 05의 5.3절)
- 퍼블릭과 온프렘 가운데 어디서 돌릴지는 무엇으로 판단하고, 이미 클라우드에 있는 것은 되돌려야 하는가 (AX 06, Private AI 07의 8.5절)
- 데이터를 외부로 보내지 않고 LLM, RAG, 에이전트를 운영하려면 어떤 인프라가 필요한가 (Private AI 01, 07)
- GPU는 몇 장이 필요하고 총소유비용은 어떻게 산정하는가 (Private AI 06)
- 같은 모델을 사업부마다 따로 배포하지 않으려면 어떻게 설계하는가 (Private AI 07의 3.4.1절, PAIS 3.0 공유 모델)
- 에이전트는 어떤 업무에 효과가 있고 어떤 업무에서 실패하는가 (앱 가이드 02)
- 에이전트의 가드레일과 운영 책임은 앱과 플랫폼 중 어디에 두는가 (앱 가이드 12, 13, 14, Private AI 05의 08)
- 직원들이 승인 없이 쓰는 AI 도구(섀도 AI)는 어떻게 찾고, 금지 대신 어떻게 다루는가 (AX 07의 7.6절, Private AI 05의 7.2.3절)
- API 게이트웨이는 지금 무엇으로 두고 로드맵에는 어떻게 대응하는가 (Private AI 03의 5.7절, 앱 가이드 05)
- 문서보안(DRM)이 걸린 문서를 검색 소스로 안전하게 연결하려면 어떻게 하는가, 전부 복호화해야 하는가 (앱 가이드 06, Private AI 05의 5.9절)
- 사내 문서가 한국어인데 모델, 임베딩, 파이프라인은 무엇을 기준으로 고르는가 (앱 가이드 10의 10.7절, 06의 6.8절)
- 공개 모델을 사내 서비스에 써도 되는가, 라이선스는 무엇을 확인하나 (앱 가이드 10의 10.8절, Private AI 05의 4.2절)

### 작성 원칙

- **기준선** — VCF 9.1.1 / PAIF 9.1.1 / PAIS 3.0 (2026-09-03 GA). 이전 기준선(VCF 9.1 / PAIS 2.1) 문서는 플랫폼 가이드와 앱 가이드 레포의 태그 `baseline-pais-2.1`에서 볼 수 있습니다(벤더 중립인 AX 가이드에는 기준선 태그가 없습니다).
- **출처 확인** — 수치와 버전은 공식 릴리스 노트로 확인하고 출처 링크를 답니다. 공식 문서로 확인되지 않은 내용은 "확인 필요"로 표시하고, 발표만 된 기능은 GA 전까지 본문에 반영하지 않습니다.
- **판단 기준** — 설정 절차만이 아니라 어떤 경우에 그 방식이 적합하고 어떤 경우에 적합하지 않은지, 장단점이 무엇인지도 정리합니다.
- **익명화** — 특정 기업의 사례는 싣지 않습니다. 사례는 업종과 업무 유형 수준으로 일반화했습니다.
- **안내와 양식의 분리** — AX 가이드는 착수 전 단계의 안내라 채워 쓰는 양식을 두지 않고 끝까지 채운 가상 예시를 싣습니다. 채워 쓰는 양식과 계산 워크북은 플랫폼 가이드와 앱 가이드에 둡니다.
- **맞지 않는 조건도 적기** — 권하는 접근이 맞지 않는 경우와 그때 무엇을 달리해야 하는지를 본문에 함께 적습니다.

오류 제보와 의견은 각 저장소의 Issues로 보내 주시면 됩니다.

---

> 이 깃헙의 공개 가이드는 모두 비공식 문서이며 [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)으로 제공됩니다. 벤더 공식 입장을 대변하지 않습니다.
