# 📄 Soh-Singh Token Growth Model White Paper

**Authors:** Julian Soh & Priyanshi Singh  
**Affiliation:** Microsoft Corporation – US State, Local, Education (SLED) Independent Software Vendors  
**Date:** December 4, 2025  

---

## 📘 Overview

This repository contains the white paper **"A Dynamic Model for AI Adoption and Compute Projection"** and supporting assets.  
The paper introduces a **non-linear logistic growth framework** to model AI adoption dynamics and correlate them with **token usage** and **compute requirements**.  

The goal is to provide a **data-driven, reproducible methodology** for:
- Forecasting AI adoption trajectories  
- Estimating token consumption (including caching efficiencies in GPT-4.1 and GPT-5)  
- Mapping adoption to compute provisioning via **Azure OpenAI Provisioned Throughput Units (PTUs)**  
- Supporting enterprise and consumer deployment strategies  

---

## 📂 Repository Structure


---

## ⚙️ Methods Summary

The paper builds on the **logistic growth equation**:



\[
A(t) = \frac{K}{1 + \left(\frac{K - A_0}{A_0}\right)e^{-rt}}
\]



Where:
- \(A(t)\): Active users at time \(t\)  
- \(K\): Carrying capacity (max potential user base)  
- \(r\): Intrinsic growth rate  
- \(A_0\): Initial adoption level  

Extensions include:
- **Token caching heuristics** (semi-dynamic prompts, static prompts, highly dynamic prompts)  
- **Multi-agent environments** using A2A and MCP protocols  
- **Compute mapping** via Azure OpenAI PTU metrics  

---

## 📊 Key Findings

- Adoption follows a **slow start → exponential growth → equilibrium plateau**.  
- Real-world adoption deviates into a **damped oscillatory pattern** due to hype, churn, and recovery.  
- Token caching significantly reduces compute demand for GPT-4.1 and GPT-5 models.  
- Example scenario:  
  - Target user base: **350,000**  
  - Growth rate: **r ≈ 0.4232 per month** (derived from FEDS Notes & BTOS survey data)  
  - Compute requirement: **~40 PTUs (gpt-5)** or **~60 PTUs (gpt-4.1)** for initial deployment.  

---

## 📑 References

- Crane, L., Green, M., & Soto, P. (2025). *Measuring AI Uptake in the Workplace*. Federal Reserve FEDS Notes, Feb 5, 2025.  
- Wang et al. (2025). *AgentTaxo: Benchmarking Token Distribution in Multi-Agent Systems*. ICLR Workshop.  
- Zhu et al. (2025). *MultiAgentBench: Evaluating Collaboration and Competition of LLM Agents*.  
- Lee et al. (2025). *Reliable Decision-Making for Multi-Agent LLM Systems*. Hitachi America, Ltd.  
- Ding et al. (2025). *MCP-Enabled Agents Performance Characterization*.  

---

## 🚀 Getting Started

1. Clone the repository:
   ```bash
   git clone https://github.com/<your-org>/<repo-name>.git
   cd <repo-name>

