# AI Agents

> 32 AI agents to rebuild on the new platform

## Agent List

1. `orchestrator`
2. `music_orchestrator`
3. `revenue_orchestrator`
4. `fan_engagement_agent`
5. `merch_visual_agent`
6. `merch_sales_agent`
7. `social_grid_architect`
8. `pricing_optimiser`
9. `shipping_optimisation`
10. `sync_licensing_agent`
11. `link_integrity_agent`
12. `memorial_visual_director`
13. `partnership_agent`
14. `ganozmix_direct`
15. `security_secrets_agent`
16. `academic_writing_coach`
17. `master_blueprint_agent`
18. `email_revenue_agent`
19. `metricool_agent`
20. `stripe_revenue_protection`
21. `booking_revenue_agent`
22. `qa_systems_auditor`
23. `streaming_royalty_agent`
24. `release_launch_agent`
25. `api_setup_assistant`
26. `approval_gate`
27. `superfan_converter`
28. `literature_researcher`
29. `content_revenue_agent`
30. `site_auditor`
31. `workbook_writer`
32. `order_support`

## Agent Architecture

Each agent is a JSON config file in `base44/agents/{name}.jsonc` containing:
- **Instructions** — system prompt for the agent
- **Model** — LLM model to use
- **Tools** — entity permissions, backend function permissions, connector permissions
- **Channels** — WhatsApp, Telegram, or in-app chat

## Key Agents to Rebuild First

1. **orchestrator** — Central coordinator, routes tasks to other agents
2. **music_orchestrator** — Release pipeline management
3. **revenue_orchestrator** — Monetization and pricing
4. **fan_engagement_agent** — Community and fan interaction
5. **literature_researcher** — Credible web research for content
6. **academic_writing_coach** — Content quality review

## Migration Notes

- Agent configs are in `base44/agents/*.jsonc`
- On Emergent, rebuild as AI agent configs or custom LLM workflows
- Each agent needs: system prompt, tool permissions, model selection
- Agent memory is stored in: AgentMemory, MusicAgentMemory, MemoryGraphNode entities
- Agent approval queue: ApprovalQueue, ApprovalQueueItem entities
