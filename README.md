**엔터프라이즈 프라이빗 클라우드와 Private AI 인프라를 도입하고, 현장에서 바로 참고할 수 있는 실무 가이드 정리.**
Modern Private Cloud(VCF), Private AI(PAIF / PAIS), Enterprise AI Transformation(AX)

### 가이드 구성

세 가이드는 **전략 → 플랫폼 → 워크로드** 순서로 구성되어 있습니다. 문서는 모두 88편이며, 가이드 사이에 관련 문서 링크를 두어 필요한 부분만 골라 읽을 수 있습니다.

| 1. 전략 → | 2. 플랫폼 → | 3. 워크로드 |
|---|---|---|
| **[기업용 AX 방법론](https://github.com/JaeHoYun/enterprise-ax-methodology)**<br>벤더 중립, 11편 | **[VCF Private AI 인프라](https://github.com/JaeHoYun/vcf-private-ai)**<br>PAIF / PAIS, Primer 포함 68편 | **[PAIS 에이전트 서비스](https://github.com/JaeHoYun/vcf-private-ai-agents)**<br>9편 |
| 진단 → 대안 → 운영모델 → 로드맵 → 거버넌스 | 인프라 → 데이터 → 서빙 → RAG, 보안, 사이징, 통합 설계 | 설계 패턴 → Agent Builder → MCP → 평가 → 운영 → 유스케이스 |
| 무엇을 어떤 순서로 바꿀 것인가 | 어떤 인프라로 구현할 것인가 | 그 위에서 어떤 서비스를 만들 것인가 |

1. **[기업용 AX 방법론 가이드](https://github.com/JaeHoYun/enterprise-ax-methodology)** — 전략. DX 방식을 그대로 따르는 AX가 왜 실패하는지 진단하고, 그 대안으로 증거 기반의 점진적 전환 방법과 운영모델, 전사 확장, 로드맵, AI 거버넌스를 벤더 중립으로 정리했습니다. 07장에서 Private AI를 구현 방안으로 다루며 2번 가이드와 연결됩니다.
2. **[VCF Private AI (PAIF) 인프라 가이드](https://github.com/JaeHoYun/vcf-private-ai)** — 플랫폼. VCF 9.1.x PAIF 플랫폼(PAIS 3.0)의 구축과 운영을 인프라, 벡터 DB, 서빙 API, RAG, 보안과 거버넌스, 사이징과 비용, 통합 설계의 일곱 편으로 나누어 다룹니다. AI와 쿠버네티스가 익숙하지 않은 인프라 담당자를 위한 입문(Primer) 편도 있습니다.
3. **[PAIS 에이전트 서비스 가이드](https://github.com/JaeHoYun/vcf-private-ai-agents)** — 워크로드. PAIF 플랫폼에서 PAIS 3.0 Agent Builder와 MCP로 에이전트 서비스를 설계, 구축, 평가, 운영하는 방법과, 어떤 업무에 적용해야 효과가 있는지를 다룹니다.

### 상황별 추천 순서

| 상황 | 먼저 읽을 문서 | 다음 문서 |
|---|---|---|
| AI 전환을 어디서부터 시작할지 정해야 하는 기획, 경영 담당자 | [AX 00 오리엔테이션](https://github.com/JaeHoYun/enterprise-ax-methodology/blob/main/docs/00-orientation.md) → 01 진단 → 03 대안 | 04 유스케이스 → 05 운영모델 → 08 로드맵 |
| 이미 AI 도구를 여럿 쓰고 있어 정비가 필요한 조직 | [AX 09 브라운필드 진단](https://github.com/JaeHoYun/enterprise-ax-methodology/blob/main/docs/09-brownfield-assessment.md) | 10 AI 거버넌스 → 06 전사 확장 |
| 가상화는 익숙하지만 AI와 쿠버네티스는 처음인 인프라 엔지니어 | [Private AI 입문(Primer)](https://github.com/JaeHoYun/vcf-private-ai/tree/main/00-foundations) | 01 인프라 → 06 사이징 → 07 통합 설계 |
| PAIF 플랫폼 구축과 운영을 맡은 인프라, 플랫폼팀 | [Private AI 01 인프라](https://github.com/JaeHoYun/vcf-private-ai/tree/main/01-infra) | 02 벡터 DB → 05 보안 → 06 사이징 → 07 통합 설계 |
| 사내 API로 LLM, RAG 앱을 만드는 개발자 | [Private AI 03 서빙 API](https://github.com/JaeHoYun/vcf-private-ai/tree/main/03-serving-api) | 04 RAG → 에이전트 01~04 |
| 에이전트 도입 여부와 적용 업무를 검토하는 담당자 | [에이전트 08 어디에 쓰나](https://github.com/JaeHoYun/vcf-private-ai-agents/blob/main/docs/08-use-cases.md) | AX 04 유스케이스 → 에이전트 02 설계 패턴 |
| 운영 중인 플랫폼을 VCF 9.1.1 / PAIS 3.0으로 업그레이드하는 운영자 | [Private AI 01-infra 00 What's New](https://github.com/JaeHoYun/vcf-private-ai/blob/main/01-infra/docs/00-whats-new.md) | 01-infra 10 운영 → 에이전트 07 운영 |

### 다루는 질문

- DX 방식의 AX는 왜 실패하며, 대안은 무엇인가 (AX 01, 03)
- 데이터를 외부로 보내지 않고 LLM, RAG, 에이전트를 운영하려면 어떤 인프라가 필요한가 (Private AI 01, 07)
- GPU는 몇 장이 필요하고 총소유비용은 어떻게 산정하는가 (Private AI 06)
- 같은 모델을 사업부마다 따로 배포하지 않으려면 어떻게 설계하는가 (Private AI 07의 3.4.1절, PAIS 3.0 공유 모델)
- 에이전트는 어떤 업무에 효과가 있고 어떤 업무에서 실패하는가 (에이전트 08)
- 에이전트의 가드레일과 운영 책임은 앱과 플랫폼 중 어디에 두는가 (에이전트 06, 07)

### 작성 원칙

- **기준선** — VCF 9.1.1 / PAIF 9.1.1 / PAIS 3.0 (2026-09-03 GA). 이전 기준선(VCF 9.1 / PAIS 2.1) 문서는 각 레포의 태그 `baseline-pais-2.1`에서 볼 수 있습니다.
- **출처 확인** — 수치와 버전은 공식 릴리스 노트로 확인하고 출처 링크를 답니다. 공식 문서로 확인되지 않은 내용은 "확인 필요"로 표시하고, 발표만 된 기능은 GA 전까지 본문에 반영하지 않습니다.
- **판단 기준** — 설정 절차만이 아니라 어떤 경우에 그 방식이 적합하고 어떤 경우에 적합하지 않은지, 장단점이 무엇인지도 정리합니다.
- **익명화** — 특정 기업의 사례는 싣지 않습니다. 사례는 업종과 업무 유형 수준으로 일반화했습니다.

오류 제보와 의견은 각 저장소의 Issues로 보내 주시면 됩니다.

---

> 이 깃헙의 공개 가이드는 모두 비공식 문서이며 [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)으로 제공됩니다. 벤더 공식 입장을 대변하지 않습니다.
