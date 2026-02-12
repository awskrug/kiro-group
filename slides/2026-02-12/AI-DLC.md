# 개발 방식 춘추 전국 시대?

- 어떤 것이 정확하고 빠르고 **지속적인** 개발 방법일까?
- 기존 개발(관리) 방식의 필요성을 깨닫고 새롭게 적용하는 중?

---
# AI-DLC, 왜 주목했나?

[AI-DLC, 왜 주목했나?](https://aws.amazon.com/ko/blogs/tech/aws-aidlc-woongjinthinkbig-tech-blog/)
> 바이브 코딩이 개발자의 직관과 간단한 프롬프트에 의존한다면, AI-DLC는 체계적이고 구조화된 명세서를 기반으로 AI와 협업합니다. “대충 이런 거 만들어줘”가 아니라, “이런 요구사항이 있고, 이렇게 설계했으니, 이 부분을 구현해줘”라고 요청하는 방식입니다.

[4개월간의 바이브 코딩 결과](https://seungwoo321.github.io/blog/2025/10/10/economic-dashboard-5-ai-dlc-on-aws/):
- 기능은 많아졌지만 구조는 엉망
- 문서는 구버전, 코드는 신버전
- AI도 나도 전체 구조 파악 불가
> 새로운 아키텍처로 문서를 다시 작성해야겠다고 생각했지만, 어디서부터 시작해야 할지 막막했습니다.
---
# [AI-Driven Development Lifecycle](https://prod.d13rzhkk8cj2z0.amplifyapp.com/)

- 시작은 [몹 프로그래밍](https://helloworld.kurly.com/blog/mob-programming/)?
- AI를 통해 단계적으로 구현하는 방법론

---
# [핵심 요소](https://www.linkedin.com/posts/derick-chen_aidlc-specdrivendevelopment-softwareengineer-activity-7394576486097281025-3Gzc/)

## Al-native methodology including tooling, processes and people structure

### Contextual Artefacts
- Tools agnostic, maintain cross session context with artefacts
### Collaborative Processes
- Working with Al-agent as partners, retain human ownership
### Domain-based People Structure
- Multi-disciplined, project specific "Taxi Teams"

---
# INCEPTION(기획/착수)
## Determines WHAT to build and WHY
- Requirements analysis and validation
- User story creation (when applicable)
- Application Design and creating units of work for parallel development
- Risk assessment and complexity evaluation

---
# CONSTRUCTION(구축)
## Determines HOW to build it
- Detailed component design(DDD)
- Code generation and implementation
- Build configuration and testing strategies
- Quality assurance and validation

---
# OPERATIONS
## Deployment and monitoring (future)
Deployment automation and infrastructure
Monitoring and observability setup
Production readiness validation

---
# [Vibe coding vs AI-DLC]((https://seungwoo321.github.io/blog/2025/10/10/economic-dashboard-5-ai-dlc-on-aws/#%ED%95%B5%EC%8B%AC-%EC%B0%A8%EC%9D%B4%EC%A0%90))

|항목|바이브코딩|AI-DLC|
|-|:--:|:--:|
|전체흐름|문서 작성(AI 채팅) → 문서 기반 개발 → 기능 추가 → 문서와 코드 분리|사용자 스토리 → Unit 분리 → 도메인 모델 → 논리적 설계 → 구현 → 테스트|
|접근|전체를 한 번에|Unit 단위로 분리|
|설계|개발하면서 구조 변경|도메인 모델 설계 후 구현|
|진행|문서와 코드 점진적 분리|각 Unit별 문서-코드 동기화|

---
# [SDD vs AI-DLC](https://www.linkedin.com/posts/derick-chen_aidlc-specdrivendevelopment-softwareengineer-activity-7394576486097281025-3Gzc/)

> SDD는 주로 단일 소프트웨어 엔지니어 또는 소규모의 자율적인 팀이 중간 정도의 복잡성을 가진 소프트웨어 프로젝트를 구축
> AI-DLC 역시 문서와 산출물(또는 사양)을 사용

다른 점은?
1. 분산되고 결과 중심적인 사양 관리 방식
2. 복잡성이 높은 프로젝트를 위한 팀 간 협업을 위해 설계
3. 다양한 도메인 전문가가 주도하는 점진적인 맥락적 산출물 구축 방식을 채택
4. 개발자 외에도 다양한 담당자가 참여하는 프로젝트 기반의 인력 구조

---
# 어떻게 적용하지?

Workflow 방식으로 질의의 응답식 진행 가능

[AI-DLC Workflow](https://github.com/awslabs/aidlc-workflows) 
[AI-DLC Workflow for Claude Code](https://mateon01.github.io/aidlc-for-claude/)

---
# 참고

- [AI-Driven Development Lifecycle](https://prod.d13rzhkk8cj2z0.amplifyapp.com/)
- [AI-Driven Development Lifecycle 번역본](https://github.com/Seungwoo321/aidlc-docs/blob/main/ai-dlc-whitepaper-ko.md)
- [AI-DLC 기반 웅진씽크빅 북큐레이터 AI 에이전트 구축](https://aws.amazon.com/ko/blogs/tech/aws-aidlc-woongjinthinkbig-tech-blog/)
- [Agentic AI 기반 플랫폼 – 7주만에 기획부터 배포까지, Part1: AI-DLC 방법론과 유용한 도구들](https://aws.amazon.com/ko/blogs/tech/agentic-ai-foundation-platform-part1/)
- [AI-DLC 워크샵](https://catalog.us-east-1.prod.workshops.aws/workshops/a1753e26-c705-4920-88f8-09ee62b203eb/ko-KR)
