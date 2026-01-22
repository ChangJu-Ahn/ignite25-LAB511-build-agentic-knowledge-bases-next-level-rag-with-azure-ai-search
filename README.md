<p align="center">
<img src="img/Banner-ignite-25.png" alt="decorative banner" width="1200"/>
</p>

# [Microsoft Ignite 2025](https://ignite.microsoft.com)

## 🔥LAB511: Build Agentic Knowledge Bases: Next-Level RAG with Azure AI Search

[![Microsoft Foundry Discord](https://dcbadge.limes.pink/api/server/nTYy5BXMWG)](https://aka.ms/MicrosoftFoundry-Ignite25)
[![Microsoft Foundry Developer Forum](https://img.shields.io/badge/GitHub-Microsoft_Foundry_Developer_Forum-blue?style=for-the-badge&logo=github&color=adff2f&logoColor=fff)](https://aka.ms/MicrosoftFoundryForum-Ignite25)

### 세션 설명

이 실습 랩에서는 Azure AI Search의 차세대 검색 기술인 에이전틱 RAG를 사용하여 지식 베이스를 구축합니다. 여러 인덱스와 스토리지 시스템에서 스마트 소스 선택을 통해 에이전틱 검색 엔진을 데이터에 연결합니다. 자연어 가이드를 사용하여 계획을 향상시키고 사용 사례에 맞는 인용 또는 추출 답변을 포함한 근거 있는 응답을 생성하는 방법을 배웁니다. 실습이 끝나면 엔터프라이즈 데이터에 대해 응답하는 완전한 기능의 에이전틱 지식 베이스를 갖추게 됩니다.

### 🧠 학습 목표

이 세션이 끝나면 학습자는 다음을 수행할 수 있습니다:

- 에이전틱 RAG를 사용하여 엔터프라이즈 데이터를 검색하고, 추론하고, 응답하는 지식 베이스를 설계하고 구축합니다.
- 스마트 소스 선택을 구현하여 여러 인덱스와 데이터 소스를 지능적으로 연결하고 쿼리합니다.
- 자연어 가이드를 사용하여 쿼리 계획을 향상시키고 비즈니스 요구에 맞는 근거 있는, 인용이 풍부한 또는 추출 응답을 생성합니다.

### 💻 사용 기술

- **[Azure AI Search](https://learn.microsoft.com/azure/search/)** - 벡터 검색, 시맨틱 랭킹 및 에이전틱 검색 지식 베이스
- **[Azure Foundry Service](https://learn.microsoft.com/azure/ai-services/openai/)** - 답변 합성을 위한 GPT-4.1 및 벡터 임베딩을 위한 text-embedding-3-large
- **[Azure Storage](https://learn.microsoft.com/azure/storage/)** - 문서 저장 및 처리를 위한 Blob 스토리지
- **[Python](https://www.python.org/)** - Jupyter 노트북을 사용하는 주요 프로그래밍 언어
- **[Azure SDK for Python](https://learn.microsoft.com/python/api/overview/azure/)** - `azure-search-documents`, `azure-identity`, `azure-storage-blob`
- **[Visual Studio Code](https://code.visualstudio.com/)** - Jupyter 노트북을 지원하는 개발 환경

## 🚀 시작하기

### 1️⃣ 개발 환경 선택

이 랩을 실행하기 위한 개발 환경을 선택하세요:

<table>
<tr>
<td width="50%">

#### 🐳 Dev Container (권장)
**사전 구성된 환경으로 즉시 시작**

**GitHub Codespaces (클라우드)**
- 이 리포지토리에서 **Code** → **Codespaces** → **Create codespace** 클릭
- 브라우저에서 VS Code가 열리고 모든 도구가 설치됨

**VS Code Dev Container (로컬)**
- [Docker Desktop](https://www.docker.com/products/docker-desktop) 설치
- [Dev Containers 확장](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers) 설치
- 이 리포지토리를 VS Code에서 열고 `F1` → **Reopen in Container**

✅ 포함 내용: Python 3.12, Azure CLI, Jupyter, 모든 종속성

</td>
<td width="50%">

#### 💻 로컬 환경
**기존 개발 환경 사용**

**필수 요구사항:**
- Python 3.10 이상
- Azure CLI
- Visual Studio Code
- Jupyter 확장

수동으로 환경을 설정하고 종속성을 설치합니다.

</td>
</tr>
</table>

### 2️⃣ Azure 리소스 배포

본인의 Azure 구독에 필요한 클라우드 리소스를 배포하세요:
- Azure AI Search (지식 베이스 및 인덱스)
- Azure OpenAI (GPT-4.1, text-embedding-3-large)
- Azure Storage (문서 저장)
- Azure AI Services (문서 처리)

**⏱️ 소요 시간: 약 20-25분**

👉 **[상세 배포 가이드 보기](./infra/deploy-yourself/README.md)**

### 3️⃣ 노트북 실행

환경 설정과 Azure 배포가 완료되면 `notebooks/` 폴더의 Jupyter 노트북을 순서대로 실행하세요.

**⏱️ 소요 시간: 약 60-90분**

### 📚 리소스 및 다음 단계

| 리소스          | 링크                             | 설명        |
|:-------------------|:----------------------------------|:-------------------|
| Ignite 2025 Next Steps | [https://aka.ms/Ignite25-Next-Steps](https://aka.ms/Ignite25-Next-Steps?ocid=ignite25_nextsteps_cnl) | Ignite 2025 세션의 모든 리포지토리 링크 |
| Microsoft Foundry Community Discord | [![Microsoft Foundry Discord](https://dcbadge.limes.pink/api/server/nTYy5BXMWG)](https://aka.ms/MicrosoftFoundry-Ignite25)| Microsoft Foundry 커뮤니티와 연결하세요! |
| Learn at Ignite | [https://aka.ms/LearnAtIgnite](https://aka.ms/LearnAtIgnite?ocid=ignite25_nextsteps_github_cnl) | Microsoft Learn에서 학습을 계속하세요 |

## 콘텐츠 소유자

<table>
<tr>
    <td align="center"><a href="http://github.com/aycabas">
        <img src="https://github.com/aycabas.png" width="100px;" alt="Ayca Bas"
"/><br />
        <sub><b> Ayca Bas
</b></sub></a><br />
            <a href="https://github.com/aycabas" title="talk">📢</a> 
    </td>
    <td align="center"><a href="http://github.com/mattgotteiner">
        <img src="https://github.com/mattgotteiner.png" width="100px;" alt="Matt Gotteniner
"/><br />
        <sub><b>Matt Gotteiner
</b></sub></a><br />
            <a href="https://github.com/mattgotteiner" title="talk">📢</a> 
    </td>
    <td align="center"><a href="http://github.com/pamelafox">
        <img src="https://github.com/pamelafox.png" width="100px;" alt="Pamela Fox"
"/><br />
        <sub><b> Pamela Fox
</b></sub></a><br />
            <a href="https://github.com/pamelafox" title="talk">📢</a> 
    </td>
</tr></table>


## 기여하기

이 프로젝트는 기여와 제안을 환영합니다. 대부분의 기여는 귀하가 귀하의 기여를 사용할 권리를 부여할 권리가 있고 실제로 부여한다고 선언하는
기여자 라이선스 계약(CLA)에 동의해야 합니다. 자세한 내용은 [기여자 라이선스 계약](https://cla.opensource.microsoft.com)을 방문하세요.

풀 리퀘스트를 제출하면 CLA 봇이 자동으로 CLA를 제공해야 하는지 여부를 결정하고
PR을 적절하게 장식합니다(예: 상태 확인, 댓글). 봇이 제공하는 지침을 따르기만 하면 됩니다.
CLA를 사용하는 모든 리포지토리에서 한 번만 수행하면 됩니다.

이 프로젝트는 [Microsoft 오픈 소스 행동 강령](https://opensource.microsoft.com/codeofconduct/)을 채택했습니다.
자세한 내용은 [행동 강령 FAQ](https://opensource.microsoft.com/codeofconduct/faq/)를 참조하거나
추가 질문이나 의견이 있으면 [opencode@microsoft.com](mailto:opencode@microsoft.com)으로 문의하세요.

## 상표

이 프로젝트에는 프로젝트, 제품 또는 서비스에 대한 상표 또는 로고가 포함될 수 있습니다. Microsoft
상표 또는 로고의 승인된 사용은 [Microsoft 상표 및 브랜드 지침](https://www.microsoft.com/legal/intellectualproperty/trademarks/usage/general)을
따라야 합니다. 이 프로젝트의 수정된 버전에서 Microsoft 상표 또는 로고를 사용하면 혼란을 일으키거나 Microsoft의 후원을 암시해서는 안 됩니다.
제3자 상표 또는 로고의 사용은 해당 제3자의 정책에 따릅니다.
