# 본인의 Azure 구독에 배포하기

이 폴더에는 LAB511 지식 베이스 인프라를 본인의 Azure 구독에 배포하기 위한 리소스가 포함되어 있습니다.

## 📋 사전 요구 사항

- 리소스를 생성할 수 있는 충분한 권한이 있는 **Azure 구독**
- **Azure CLI** 설치 및 구성 ([설치 가이드](https://learn.microsoft.com/cli/azure/install-azure-cli))
- **Python 3.10+** 설치
- **Git** (이 리포지토리를 복제하기 위해)
- **VS Code** 또는 Jupyter 확장이 설치된 **GitHub Codespaces** (권장)

### 필요한 Azure 권한

다음 권한이 필요합니다:
- 리소스 그룹 생성
- Bicep 템플릿 배포
- 다음 리소스 생성 및 관리:
  - Azure Storage 계정
  - Azure AI Search 서비스
  - Azure OpenAI 서비스
  - Azure AI Services (Cognitive Services)
- Azure RBAC 역할 할당

## 🚀 빠른 시작

### 1. 리포지토리 복제

```bash
git clone https://github.com/microsoft/ignite25-LAB511-build-agentic-knowledge-bases-next-level-rag-with-azure-ai-search.git
cd ignite25-LAB511-build-agentic-knowledge-bases-next-level-rag-with-azure-ai-search
```

### 2. Azure에 로그인

```bash
az login
```

### 3. 인프라 배포

⏱️ **예상 시간: 10-15분**

두 옵션 모두 먼저 Azure에 로그인해야 합니다:

```shell
az login
```

#### 옵션 A: 배포 스크립트 사용

  **Windows (PowerShell):**
  ```powershell
  cd infra/deploy-yourself
  .\deploy.ps1 -ResourceGroupName "LAB511-ResourceGroup" -Location "westcentralus"
  ```

  **Linux/macOS (Bash):**
  ```bash
  cd infra/deploy-yourself
  ./deploy.sh -g "LAB511-ResourceGroup" -l "westcentralus"
  ```

#### 옵션 B: 수동 배포

```bash
# 리소스 그룹 생성
az group create --name **LAB511-ResourceGroup** --location westcentralus

# 사용자 개체 ID 가져오기
USER_OBJECT_ID=$(az ad signed-in-user show --query id -o tsv)

# Bicep 템플릿 배포
az deployment group create \
  --resource-group LAB511-ResourceGroup \
  --template-file ../LAB511.bicep \
  --parameters labUserObjectId=$USER_OBJECT_ID \
  --parameters resourcePrefix=lab511
```

### 4. 환경 설정

⏱️ **예상 시간: 5-10분**

인프라가 배포된 후 설정 스크립트를 실행하세요:

**Windows (PowerShell):**
```powershell
.\setup-environment.ps1 -ResourceGroupName "LAB511-ResourceGroup"
```

**Linux/macOS (Bash):**
```bash
./setup-environment.sh -g "LAB511-ResourceGroup"
```

이 스크립트는 Azure에서 연결 문자열과 엔드포인트를 가져오고, 리포지토리 루트에 `.env` 파일을 생성하며, Python 가상 환경을 설정하고, 필요한 종속성을 설치한 다음, 검색 인덱스를 생성하고 샘플 데이터를 업로드합니다.

### 5. 랩 시작

⏱️ **예상 시간: 모든 노트북 완료에 60-90분**

VS Code에서 [notebooks](../../notebooks) 폴더를 열고 **`part1-basic-knowledge-base.ipynb`부터 시작하세요**.

## 🧹 정리

모든 리소스를 삭제하고 지속적인 요금을 방지하려면:

```bash
az group delete --name LAB511-ResourceGroup --yes --no-wait
```

## 📚 추가 리소스

- [Azure AI Search 문서](https://learn.microsoft.com/azure/search/)
- [Azure OpenAI Service 문서](https://learn.microsoft.com/azure/ai-services/openai/)
- [Azure Bicep 문서](https://learn.microsoft.com/azure/azure-resource-manager/bicep/)
- [Azure AI Foundry 커뮤니티 Discord](https://aka.ms/AIFoundryDiscord-Ignite25)
