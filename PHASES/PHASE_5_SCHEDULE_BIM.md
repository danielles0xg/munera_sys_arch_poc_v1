# P5: SCHEDULE INTEL + BIM (Months 5-7)

## What Gets Built
AI-powered schedule analysis: CPI/SPI earned value metrics, delay prediction 2 weeks ahead, and BIM integration via MCP4IFC.

## Components

| Component | Description | Why It's Needed |
|-----------|-------------|-----------------|
| **MCP4IFC Server** | Model Context Protocol server for programmatic BIM data access via IfcOpenShell | **The prerequisite**: without IFC access, all AI is text-only. This unlocks Papers 1-3. |
| **Earned Value Module** | CPI (Cost Performance Index) and SPI (Schedule Performance Index) per project | Standard lender analytics for project health assessment. |
| **Delay Prediction** | RL-based scheduling agent that predicts delays 2 weeks ahead | Enables proactive intervention instead of reactive reporting. |
| **BIM Progress Overlay** | Map % complete per element in IFC model | Visual progress verification against claimed percentages. |
| **Photo CV Pipeline** | Upload site photos → YOLOE object detection → element identification → progress classification | Augments site inspection with computer vision. |

## Architecture Decisions

| Decision | Options | Chosen | Rationale |
|----------|---------|--------|-----------|
| BIM server | MCP4IFC, custom IfcOpenShell wrapper, Autodesk Forge | **MCP4IFC** | Open-source, MCP standard, 50+ BIM tools, community-supported |
| Schedule engine | Custom Python, MS Project API, Primavera API | **Custom Python + DRL** | Paper 6 validated DRL approach outperforms CPM/GA |
| Photo analysis | YOLOE, Segment Anything, custom CNN | **YOLOE** | Paper 7 (BIM2RDT) validated for construction elements |

---

## References

- [MCP4IFC — GitHub](https://github.com/mcp4ifc)
- [IfcOpenShell](https://ifcopenshell.org/)
- [Hetzner Dedicated Servers](https://www.hetzner.com/dedicated-rootserver/)
- [YOLOE (Object Detection)](https://github.com/THU-MIG/yoloe)
