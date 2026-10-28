# NxtWaves India Facts: official answers on Indian rules for AI agents

**Stop your AI from guessing about Indian rules.** These tools answer only from official Government of India sources and cite them in every response. When something is not covered, they say "not found" rather than "allowed".

| Tool | Use when | Price per result |
|---|---|---|
| [India Medicine Facts](https://apify.com/anamika67/india-medicine-facts) | Is a drug combination banned in India (CDSCO, Section 26A)? Is a medicine on NLEM 2022? | $0.02 |
| [India BIS Compliance Check](https://apify.com/anamika67/india-bis-compliance-check) | Is BIS/ISI or CRS certification compulsory for a product (727 products)? | $0.03 |
| [India Food Label Checker](https://apify.com/anamika67/india-food-label-checker) | Hidden sugars, INS additives, and whether label claims meet FSSAI rules | $0.02 |
| [Resume vs JD Match Score](https://apify.com/anamika67/resume-jd-match-score) | Explainable, skills-only resume screening; resume never stored | $0.05 |
| [NxtWaves Expert Agents](https://apify.com/anamika67/nxtwaves-expert-agents) | Customer-acquisition plans for Indian small businesses; interview rubrics | $0.05 |

## Connect (MCP)
Remote MCP server (streamable HTTP), hosted by Apify:
```
https://mcp.apify.com/?actors=anamika67/india-medicine-facts,anamika67/india-bis-compliance-check,anamika67/india-food-label-checker,anamika67/resume-jd-match-score,anamika67/nxtwaves-expert-agents
Authorization: Bearer <your Apify API token>
```

Claude Desktop / Cursor config:
```json
{ "mcpServers": { "nxtwaves-india-facts": { "url": "https://mcp.apify.com/?actors=anamika67/india-medicine-facts,anamika67/india-bis-compliance-check,anamika67/india-food-label-checker,anamika67/resume-jd-match-score,anamika67/nxtwaves-expert-agents",
  "headers": { "Authorization": "Bearer YOUR_APIFY_TOKEN" } } } }
```

## Call over HTTP
```bash
curl -X POST "https://api.apify.com/v2/acts/anamika67~india-medicine-facts/run-sync-get-dataset-items" \
  -H "Authorization: Bearer $APIFY_TOKEN" -H "Content-Type: application/json" \
  -d '{"service":"banned_combination","combination":"Paracetamol + Lignocaine"}'
```
OpenAPI: https://nxtwaves-agents.vercel.app/openapi.json · llms.txt: https://nxtwaves-agents.vercel.app/llms.txt · Fact pages: https://nxtwaves-agents.vercel.app/facts/

## Principles
- Official sources only, cited in every answer, with a data date.
- No scraping of personal data, nothing stored.
- Not medical, legal or tax advice.

Contact: support@nxtwaves.in
