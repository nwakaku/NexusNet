# NexusNet - Decentralized AI Model Routing & Inference Market

<div align="center">

**Round I Submission - Bittensor Subnet Ideathon (Dec 23, 2025 - Feb 25, 2026)**

[Video Presentation](https://youtu.be/0TO5DAM7wWE) · [Pitch Deck](https://docs.google.com/presentation/d/1zp693M0B3bgB_iyOgO01dqbE1Hp7MysSXhERIeTGb90/edit?usp=sharing) · [Proposal PDF](./NexusNet_v3_Final.pdf)

</div>

---

![NexusNet Architecture](./public/NexusNet-Subnet%20(3).jpg)

## Executive Summary

NexusNet is a decentralized AI inference marketplace that addresses the centralization problem in AI services by creating a permissionless network where inference miners compete to deliver fast, high-quality AI responses. The subnet introduces a **Query Router** mechanism that intelligently routes user queries to the best-performing miners based on real-time performance metrics, ensuring quality and speed while maintaining incentive alignment through a novel **NexusScore** reputation system.

---

## Submission Contents

| Document | Description | Link |
|----------|-------------|------|
| **Subnet Design Proposal** | Full technical design, incentive mechanism, and architecture | [NexusNet_v3_Final.pdf](./NexusNet_v3_Final.pdf) |
| **Pitch Deck** | 10-slide business pitch for investors and judges | [Google Slides](https://docs.google.com/presentation/d/1zp693M0B3bgB_iyOgO01dqbE1Hp7MysSXhERIeTGb90/edit?usp=sharing) |
| **Explanation Video** | 5-10 minute walkthrough of architecture and mechanism design | [YouTube](https://youtu.be/0TO5DAM7wWE) |

---

## Problem & Solution

### The Problem
- **Centralization**: AI inference is dominated by centralized cloud providers (AWS, GCP, Azure)
- **High Costs**: Vendor lock-in creates expensive, inflexible pricing
- **Limited Access**: No permissionless marketplace for AI inference
- **Quality Uncertainty**: No standardized way to compare AI inference providers

### NexusNet Solution
A decentralized marketplace where:
- **Miners** compete by running AI models and serving inference requests
- **Validators** (Query Routers) intelligently route queries based on performance
- **Users** get fast, cost-effective AI inference from a competitive network

---

## Core Architecture

```
┌─────────────────────────────────────────────────────────────────┐
│                        NexusNet Subnet                          │
├─────────────────────────────────────────────────────────────────┤
│                                                                  │
│   ┌──────────┐      ┌──────────────────┐      ┌─────────────┐  │
│   │  Users  │─────▶│  Query Router   │─────▶│ Inference   │  │
│   │(Request)│      │  (Validator)     │      │   Miners    │  │
│   └──────────┘      └──────────────────┘      └─────────────┘  │
│                              │                      │            │
│                              ▼                      ▼            │
│                     ┌──────────────────┐      ┌─────────────┐    │
│                     │   NexusScore    │◀─────│  Response  │    │
│                     │  (Reputation)   │      │  Validation│    │
│                     └──────────────────┘      └─────────────┘    │
│                                                                  │
└─────────────────────────────────────────────────────────────────┘
```

### Key Components

1. **Query Router (Validator)**
   - Receives user queries
   - Routes to best-performing miners via weighted round-robin
   - Validates responses for quality and format
   - Updates NexusScore in real-time

2. **Inference Miners**
   - Run AI models (LLMs, image generation, etc.)
   - Serve inference requests from routed queries
   - Earn TAO based on successful, high-quality responses

3. **NexusScore System**
   - Weighted metric: 40% success rate, 30% latency, 30% quality score
   - Determines query routing weights
   - Updated after each inference cycle

---

## Incentive Mechanism

### Emission Logic

| Component | Distribution | Criteria |
|-----------|--------------|----------|
| **Miner Rewards** | 80% of emissions | Based on successful inferences + NexusScore |
| **Validator Rewards** | 20% of emissions | Based on routing accuracy + network uptime |

### Incentive Alignment

- **Miners**: Higher NexusScore → More queries → More earnings → Strong incentive for quality
- **Validators**: Accurate routing → User satisfaction → Higher validator stake → More emissions
- **Users**: Pay competitive rates for verified quality inference

### Anti-Sybil / Adversarial Protection

- **Minimum Stake**: Validators require minimum TAO stake to operate
- **Query Verification**: Multiple miner responses compared for consistency
- **Slashing Mechanism**: Malicious validators/miners lose stake
- **Reputation Decay**: Inactive miners see NexusScore decrease

---

## Why Bittensor?

### Fit for Bittensor
- Leverages Bittensor's existing validator/miner infrastructure
- Creates real demand for compute while generating value for the network
- Complements existing subnets (Ptah for training, Ionia for RLHF)
- Permissionless participation aligns with Bittensor's vision

### Competitive Landscape

| Solution | Type | NexusNet Advantage |
|----------|------|-------------------|
| **AWS/GCP** | Centralized | Decentralized, permissionless, competitive pricing |
| **Render Network** | GPU Compute | Specialized for AI inference, not general rendering |
| **Akash Network** | Cloud Marketplace | Purpose-built for AI with routing intelligence |
| **Bittensor (Ionia/Ptah)** | AI Training | Complements training with inference focus |

---

## Business Model

- **Transaction Fee**: 0.5% on each inference payment
- **Premium Services**: Priority routing, dedicated compute
- **Enterprise API**: Commercial-grade endpoints for businesses

### Go-To-Market Strategy

1. **Phase 1**: Bootstrap with AI developer community
2. **Phase 2**: Partner with Web3-native AI projects
3. **Phase 3**: Expand to enterprise AI inference customers

---

## Quick Navigation

For Judges - Start Here:

1. **[NexusNet_v3_Final.pdf](./NexusNet_v3_Final.pdf)** - Complete subnet design proposal
2. **[Video Presentation](https://youtu.be/0TO5DAM7wWE)** - Visual walkthrough (recommended first)
3. **[Pitch Deck](https://docs.google.com/presentation/d/1zp693M0B3bgB_iyOgO01dqbE1Hp7MysSXhERIeTGb90/edit?usp=sharing)** - Business case summary

---

## Contact

For questions about this submission, please refer to the proposal document or video presentation.

---

<div align="center">

**NexusNet: Democratizing AI Inference**

*Built on Bittensor - Proof of Intelligence through Decentralized Inference*

</div>
