## VMware Cloud Foundation · Private AI 실무 가이드

VCF **9.1** 기반 **Private AI** — PAIF(Private AI Foundation with NVIDIA) / PAIS(Private AI Services) — 의 구축·운영 실무 지식을 공개 가이드로 정리합니다. 현장에서 바로 쓰는 레퍼런스를 지향하며, 모든 문서는 Broadcom 공식 릴리스 노트를 기준선으로 작성합니다.

### 📚 VCF Private AI 가이드 시리즈

| 편 | 가이드 | 다루는 영역 |
|----|--------|-------------|
| ① | [vcf-private-ai-guide](https://github.com/JaeHoYun/vcf-private-ai-guide) | PAIF/PAIS 구축·개발·운영 전반 (인프라) |
| ② | [vcf-dsm-vectordb-guide](https://github.com/JaeHoYun/vcf-dsm-vectordb-guide) | RAG용 엔터프라이즈 벡터 DB · pgvector (데이터) |
| ③ | [vcf-paif-serving-api-guide](https://github.com/JaeHoYun/vcf-paif-serving-api-guide) | OpenAI 호환 모델 서빙 API (서빙) |
| ④ | [vcf-rag-reference-architecture](https://github.com/JaeHoYun/vcf-rag-reference-architecture) | 엔드투엔드 RAG 레퍼런스 아키텍처 (통합) |

👉 **시리즈 허브:** [vcf-private-ai-series](https://github.com/JaeHoYun/vcf-private-ai-series)

### 🧭 다루는 주제

`VCF` · `PAIF` · `PAIS` · `vSAN` · `NSX` · `DLVM` · `vLLM` · `RAG` · `VectorDB` · `pgvector` · `Model Serving` · `MCP` · `Agent Builder`

---

> ⚠️ 본 가이드들은 **비공식 문서**입니다. Broadcom·NVIDIA 등 벤더의 공식 입장을 대변하지 않으며, 프로덕션 적용 전 공식 문서 확인을 권장합니다. 모든 문서는 [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)으로 제공됩니다.
