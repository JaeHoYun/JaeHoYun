## VMware Cloud Foundation · Private AI 실무 가이드

VCF **9.1** 기반 **Private AI** — PAIF(Private AI Foundation with NVIDIA) / PAIS(Private AI Services) — 의 구축·운영 실무 지식을 공개 가이드로 정리합니다. 현장에서 바로 쓰는 레퍼런스를 지향하며, 모든 문서는 Broadcom 공식 릴리스 노트를 기준선으로 작성합니다.

### VCF Private AI 가이드 시리즈

| 편 | 가이드 | 다루는 영역 |
|----|--------|-------------|
| ① | [vcf-private-ai-guide](https://github.com/JaeHoYun/vcf-private-ai-guide) | PAIF/PAIS 구축·개발·운영 전반 (인프라) |
| ② | [vcf-dsm-vectordb-guide](https://github.com/JaeHoYun/vcf-dsm-vectordb-guide) | RAG용 엔터프라이즈 벡터 DB · pgvector (데이터) |
| ③ | [vcf-paif-serving-api-guide](https://github.com/JaeHoYun/vcf-paif-serving-api-guide) | OpenAI 호환 모델 서빙 API (서빙) |
| ④ | [vcf-rag-reference-architecture](https://github.com/JaeHoYun/vcf-rag-reference-architecture) | 엔드투엔드 RAG 레퍼런스 아키텍처 (통합) |
| ⑤ | [vcf-private-ai-security-governance](https://github.com/JaeHoYun/vcf-private-ai-security-governance) | 위협모델·격리·접근통제·공급망·데이터 거버넌스·감사 (보안·거버넌스) |
| ⑥ | [vcf-private-ai-sizing-cost](https://github.com/JaeHoYun/vcf-private-ai-sizing-cost) | 워크로드·GPU·VKS 사이징·용량계획·TCO (사이징·비용) |

**시리즈 허브:** [vcf-private-ai-series](https://github.com/JaeHoYun/vcf-private-ai-series)

### 관련 가이드 — AI 전환(AX) 방법론

위 시리즈가 Private AI를 떠받치는 **인프라·구현**이라면, 그 위에서 "AI 전환을 조직 차원에서 어떻게 추진하는가"라는 **상위 전략·방법론**은 다음 독립 가이드에서 다룹니다.

- [enterprise-ax-methodology](https://github.com/JaeHoYun/enterprise-ax-methodology) — 기업용 AX(AI Transformation) 방법론. DX 답습형 AX의 실패 진단, 증거 기반 증분 전환이라는 대안, 검증된 유스케이스를 Private AI로 갖추는 구현 전략 (위 시리즈를 구현 경로로 참조)

### 다루는 주제

`VCF` · `PAIF` · `PAIS` · `vSAN` · `NSX` · `DLVM` · `vLLM` · `RAG` · `VectorDB` · `pgvector` · `Model Serving` · `MCP` · `Agent Builder` · `Security` · `Governance`

---

> 본 가이드들은 **비공식 문서**입니다. Broadcom·NVIDIA 등 벤더의 공식 입장을 대변하지 않으며, 프로덕션 적용 전 공식 문서 확인을 권장합니다. 모든 문서는 [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)으로 제공됩니다.
