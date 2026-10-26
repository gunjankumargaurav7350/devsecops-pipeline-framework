# ??? Enterprise DevSecOps Hardened CI/CD Pipeline Framework

[![CI/CD Status](https://img.shields.io/badge/Pipeline-Passing-0078D4?style=for-the-badge&logo=githubactions&logoColor=white)](https://github.com/gunjankumargaurav7350/devsecops-pipeline-framework)
[![Shift-Left](https://img.shields.io/badge/Security-Shift--Left_Gates-8A2BE2?style=for-the-badge&logo=shieldsdotio&logoColor=white)](https://github.com/gunjankumargaurav7350)
[![Azure DevOps](https://img.shields.io/badge/Azure_DevOps-Multi--Stage_YAML-00A2FF?style=for-the-badge&logo=azuredevops&logoColor=white)](https://dev.azure.com)
[![Author](https://img.shields.io/badge/Lead-Gunjan_Kumar_Gaurav-0A0E27?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/gunjan-gaurav)

Production-hardened, multi-stage **DevSecOps Shift-Left Delivery Framework** for both **GitHub Actions** and **Azure DevOps Pipelines**, embedding static code analysis, secret scanning, vulnerability assessments, policy-as-code guardrails, and FinOps cost gates into every pull request.

---

## ? Multi-Stage Pipeline Lifecycle

```
[ Phase 1: Lint & Validate ]  -->  [ Phase 2: Secret Scanning ]  -->  [ Phase 3: SAST & IaC Security ]
• terraform fmt check              • TruffleHog deep scan              • Checkov compliance benchmark
• TFLint azurerm ruleset           • GitLeaks pre-commit               • Trivy vulnerability checks
                                                                                   |
       +---------------------------------------------------------------------------+
       |
       v
[ Phase 4: FinOps Cost Gate ]  -->  [ Phase 5: Speculative Plan ]  -->  [ Phase 6: Production Gated Apply ]
• Infracost PR delta comment        • Speculative plan artifact         • Manual Change Board Approval
• Budget threshold validation       • Nightly drift detection           • Zero-downtime execution
```

---

## ?? Security Toolchain Matrix

| Scanning Category | Tool | Function in Pipeline |
| :--- | :--- | :--- |
| **Secret Detection** | `TruffleHog` / `GitLeaks` | Prevents hardcoded API keys, passwords, and tokens from reaching git history. |
| **Static IaC Security**| `Checkov` | Benchmarks Terraform HCL against CIS Microsoft Azure Benchmarks and NIST 800-53. |
| **Vulnerability Analysis**| `Trivy` | Identifies CVEs in container base images and misconfigurations in Kubernetes manifests. |
| **Syntax & Best Practices**| `TFLint` | Validates Azure-specific naming conventions and resource properties prior to plan. |
| **Cloud FinOps Guardrail**| `Infracost` | Automatically calculates monthly dollar cost difference on pull requests. |

---

## ?? Getting Started

1. **GitHub Actions:** The workflow `.github/workflows/devsecops-pipeline.yml` executes automatically on pull requests and commits to `main`.
2. **Azure DevOps:** Import `azure-pipelines.yml` into your Azure DevOps pipeline library and bind with an Azure Service Connection via OIDC workload identity.

---

## ?? Author & Inquiries

**Gunjan Kumar Gaurav**  
*Senior Cloud & DevSecOps Consultant | Azure Solutions Architect Expert (AZ-305)*  
LinkedIn: [linkedin.com/in/gunjan-gaurav](https://www.linkedin.com/in/gunjan-gaurav) | Email: `gunjankumargaurav7@gmail.com`
