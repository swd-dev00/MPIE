# MPIE

## Current release: MPIE Mobile v1.1.2

The authoritative mobile build is [MPIE-Mobile-v1.1.2-Full-OAuth-Account-Lifecycle-Ubuntu-Ready.zip](./MPIE-Mobile-v1.1.2-Full-OAuth-Account-Lifecycle-Ubuntu-Ready.zip).

- SHA-256: `9aa40cd885390a61149ba5101e33c33d809dc8ffd961ec46b41d676bfc141a31`
- Validation: [v1.1.2 release verification](./RELEASE_v1.1.2_VERIFICATION.md)
- Status: full Playbook, OAuth/account lifecycle prebuild, Ubuntu-ready deployment
- Security default: `MPIE_AUTH_ENABLED=false`

> `mpie_expanded_v1.1.0.zip` is retained as a legacy archive only. Use v1.1.2 as the current MPIE Mobile source of truth.

## Project overview

The Market Pressure Intelligence Engine (MPIE) is a proprietary predictive modeling system developed by Sierra Warren Developments, LLC. It is designed to forecast sports market outcomes by quantifying "pressure" as a primary analytical feature rather than treating it as random variance.

The Market Pressure Intelligence Engine (MPIE) is a proprietary predictive modeling system developed by Sierra Warren Developments, LLC. It is designed to forecast sports market outcomes by quantifying "pressure" as a primary analytical feature rather than treating it as random variance.  
Core Framework and Methodology
• Origin: MPIE is a generalization and productionized version of the NBA Playoff Pressure Index (NBAPPI), a methodology created to measure the impact of postseason conditions on player and team performance.  
• Core Thesis: Pressure possesses a computable structure and directional impact on performance that standard predictive models frequently overlook.  
• Key Concepts:
• Pressure Differential Score (PDS): A signed scalar value representing the delta between a player's regular-season baseline and their performance in high-stakes scenarios, normalized for game stakes and opponent quality.  
• Pressure Load Index (PLI): A composite measure of total situational, narrative, and organizational pressure on a team at a specific point in a series.  
• Performer Archetypes: A classification system that categorizes players as "Amplifiers," "Regulars," or "Regressors" to inform matchup modeling.  
Technical Architecture
The engine is engineered as a production-grade system using a multi-layer stack:  
• Dual-Engine ML: MPIE utilizes a dual-engine architecture featuring scikit-learn for baseline classical predictions and PyTorch for capturing complex pressure-interaction sequences.  
• API and Inference: The system uses a FastAPI service to provide low-latency inference, real-time probability distributions, and SHAP-style feature attribution to explain how specific pressure variables drive model outputs.  
• Data and Orchestration: MPIE incorporates Redis for high-frequency state and data caching, alongside Kubernetes for containerized inference and auto-scaling.  
Feature Engineering
MPIE decomposes pressure into five structured feature classes:
• Situational Pressure: Variables such as elimination game flags or series deficits.  
• Performer Historical Pressure Delta: An individual's measured response to elevated stakes.  
• Organizational Pressure Load: Metrics related to franchise-level factors like coaching tenure or ownership urgency.  
• Market Pressure Signal: Data derived from betting line movement and market sentiment.  
• Narrative Pressure Index: A composite index quantifying media attention and public load.
