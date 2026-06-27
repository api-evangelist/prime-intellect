---
title: "RL at 1T Scale: prime-rl Performance Deep Dive"
url: "https://www.primeintellect.ai/blog/rl-at-1t-scale"
date: "2026-06-21"
author: "Prime Intellect Team and Matej Sirovatka"
feed_url: "https://www.primeintellect.ai/blog"
---
Prime Intellect released version 0.6.0 of prime-rl, enabling training of trillion-parameter scale models on heavy agentic workloads at high efficiency. The system trains GLM-5 on software engineering tasks at 131k sequence length with sub-5-minute step times using only 28 H200 nodes, through optimizations spanning low-precision inference, prefill/decode separation, and disaggregated trainer-inference architectures.
