**엔터프라이즈 프라이빗 클라우드와 Private AI 인프라를 도입하고, 현장에서 바로 참고할 수 있는 실무 가이드 정리.**
Modern Private Cloud(VCF), Private AI(PAIF / PAIS), Enterprise AI Transformation(AX)

### 세 가이드가 이루는 지도

엔터프라이즈 AI를 **전략 → 플랫폼 → 워크로드** 순서로 한 번에 검토할 수 있도록 세 가이드를 한 흐름으로 묶었습니다. 문서 88편이 상호 참조로 이어져 있어 어느 한 편에서 시작해도 나머지로 이어집니다.

```
 전략                            플랫폼                                  워크로드
┌──────────────────────────────┐   ┌──────────────────────────────────────┐   ┌──────────────────────────────────────┐
│ 1. 기업용 AX 방법론          │   │ 2. VCF Private AI 인프라             │   │ 3. PAIS 에이전트 서비스              │
│ (벤더 중립, 11편)            │   │ (PAIF / PAIS, Primer 포함 68편)       │   │ (9편)                                │
│                              │ → │                                      │ → │                                      │
│ 진단 → 대안 → 운영모델       │   │ 인프라 → 데이터 → 서빙 → RAG,        │   │ 설계 패턴 → Agent Builder            │
│ → 로드맵 → 거버넌스          │   │ 보안, 사이징, 통합 설계              │   │ → MCP → 평가 → 운영 → 유스케이스     │
└──────────────────────────────┘   └──────────────────────────────────────┘   └──────────────────────────────────────┘
 무엇을, 왜, 어떤 순서로 바꾸나  그 결정을 어떤 토대 위에 세우나         그 토대 위에 무엇을 올려 성과를 내나
```

1. **[기업용 AX 방법론 가이드](https://github.com/JaeHoYun/enterprise-ax-methodology)** — 전략. DX를 답습한 AX가 왜 실패하는지 진단하고, 증거 기반의 점진적 전환과 운영모델, 전사 확장, 로드맵, AI 거버넌스까지 벤더 중립으로 정리했습니다. 07장 'Private AI로 AX 갖추기'에서 2번 가이드로 연결됩니다.
2. **[VCF Private AI (PAIF) 인프라 가이드](https://github.com/JaeHoYun/vcf-private-ai)** — 플랫폼. VCF 9.1.x PAIF 플랫폼(PAIS 3.0)을 인프라, 벡터 DB, 서빙 API, RAG, 보안과 거버넌스, 사이징과 비용, 통합 설계의 일곱 편으로 구축하고 운영합니다. AI와 쿠버네티스가 낯선 인프라 담당을 위한 입문(Primer) 트랙을 따로 두었습니다.
3. **[PAIS 에이전트 서비스 가이드](https://github.com/JaeHoYun/vcf-private-ai-agents)** — 워크로드. 그 플랫폼 위에서 PAIS 3.0 Agent Builder와 MCP로 에이전트 서비스를 설계, 구축, 평가, 운영하고, 어디에 써야 성과가 나는지를 판단합니다.

### 어디서 시작할지

| 지금 상황 | 여기서 시작 | 이어서 |
|---|---|---|
| AI 전환을 어디서부터 시작할지 정해야 하는 기획, 경영 담당 | [AX 00 오리엔테이션](https://github.com/JaeHoYun/enterprise-ax-methodology/blob/main/docs/00-orientation.md) → 01 진단 → 03 대안 | 04 유스케이스 → 05 운영모델 → 08 로드맵 |
| 이미 AI 도구를 여럿 쓰고 있어 정비가 필요한 조직 | [AX 09 브라운필드 진단](https://github.com/JaeHoYun/enterprise-ax-methodology/blob/main/docs/09-brownfield-assessment.md) | 10 AI 거버넌스 → 06 전사 확장 |
| 가상화는 능숙하지만 AI와 쿠버네티스가 낯선 인프라 엔지니어 | [Private AI 입문(Primer)](https://github.com/JaeHoYun/vcf-private-ai/tree/main/00-foundations) | 01 인프라 → 06 사이징 → 07 통합 설계 |
| PAIF 플랫폼 구축과 운영을 맡은 인프라, 플랫폼팀 | [Private AI 01 인프라](https://github.com/JaeHoYun/vcf-private-ai/tree/main/01-infra) | 02 벡터 DB → 05 보안 → 06 사이징 → 07 통합 설계 |
| 사내 API로 LLM, RAG 앱을 만드는 개발자 | [Private AI 03 서빙 API](https://github.com/JaeHoYun/vcf-private-ai/tree/main/03-serving-api) | 04 RAG → 에이전트 01~04 |
| 에이전트를 도입할지, 어디에 쓸지 판단해야 하는 담당 | [에이전트 08 어디에 쓰나](https://github.com/JaeHoYun/vcf-private-ai-agents/blob/main/docs/08-use-cases.md) | AX 04 유스케이스 → 에이전트 02 설계 패턴 |
| 운영 중인 플랫폼을 VCF 9.1.1 / PAIS 3.0으로 올리는 운영자 | [Private AI 01-infra 00 What's New](https://github.com/JaeHoYun/vcf-private-ai/blob/main/01-infra/docs/00-whats-new.md) | 01-infra 10 운영 → 에이전트 07 운영 |

### 이런 질문에 답합니다

- DX처럼 하면 AX는 왜 실패하고, 대신 무엇을 어떤 순서로 해야 하는가 (AX 01, 03)
- 데이터를 사외로 내보내지 않고 LLM, RAG, 에이전트를 돌리려면 어떤 토대가 필요한가 (Private AI 01, 07)
- GPU는 몇 장이 필요하고 총소유비용은 어떻게 잡는가 (Private AI 06)
- 사내 표준 모델을 사업부마다 복제하지 않으려면 어떻게 설계하는가 (Private AI 07의 3.4.1절, PAIS 3.0 공유 모델)
- 에이전트는 어디에 쓰면 성과가 나고 어디서 실패하는가 (에이전트 08)
- 에이전트의 가드레일과 운영 책임은 앱과 플랫폼 중 어느 쪽이 지는가 (에이전트 06, 07)

### 작성 원칙

- **기준선** — VCF 9.1.1 / PAIF 9.1.1 / PAIS 3.0 (2026-09-03 GA). 이전 기준선(VCF 9.1 / PAIS 2.1) 문서는 두 레포의 태그 `baseline-pais-2.1`에 그대로 남겨 두었습니다.
- **근거 우선** — 수치와 버전은 공식 릴리스 노트와 대조하고 근거 링크를 남깁니다. 공식 문서로 단정할 수 없는 것은 "확인 필요"로 표기하고, 발표 단계의 기능은 GA로 확인되기 전까지 본문 논지에 넣지 않습니다.
- **판단 기준까지** — 구성 절차만이 아니라 언제 그 선택을 하고 언제 하지 않는지, 무엇을 얻고 무엇을 치르는지를 함께 적습니다.
- **익명화** — 특정 기업의 사례를 싣지 않습니다. 사례는 업종과 일의 형태로 일반화한 유형입니다.

피드백과 오류 제보는 각 저장소의 Issues로 받습니다.

---

> 이 깃헙의 공개 가이드는 모두 비공식 문서이며 [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)으로 제공됩니다. 벤더 공식 입장을 대변하지 않습니다.
