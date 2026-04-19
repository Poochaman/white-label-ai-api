# API Specification

## Endpoint

POST /v1/chat

---

## Headers

- Content-Type: application/json
- x-api-key: API key for authentication

---

## Request Body

- agentId (string)
- messages (array)
- context (object, optional)
- tools (object, optional)

---

## Example Structure

{
  "agentId": "sales-agent",
  "messages": [
    { "role": "system", "content": "..." },
    { "role": "user", "content": "..." }
  ],
  "context": {
    "industry": "financial services"
  }
}

---

## Response

- message (assistant output)
- routing metadata
- tool results (optional)
- next actions (optional)

---

## Notes

- API is stateless
- full message history required per request
- structured responses preferred for downstream integration
