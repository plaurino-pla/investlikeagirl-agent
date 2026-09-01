# Claude Connectors Directory submission

Prepared for the Claude.ai remote MCP submission portal. Do not submit until the test-account section is complete and an authorized Invest Like a Girl representative has accepted Anthropic's directory terms.

## Access required

- Claude Team or Enterprise organization
- Organization Owner, Primary Owner, or Enterprise role with Directory permission
- Portal: `https://claude.ai/admin-settings/directory/submissions/new`

## 1. Connection

- Server URL: `https://www.investlikeagirl.com.br/mcp`
- Transport: Streamable HTTP
- Connection model: Every user connects to the same URL
- Authentication: OAuth 2.0 with Dynamic Client Registration (`oauth_dcr`)
- PKCE: S256
- Hosted Claude callback accepted: `https://claude.ai/api/mcp/auth_callback`
- Scopes: `profile:read community:read learning:read`

## 2. Tools

All tools have a human-readable `title`, `readOnlyHint: true`, `destructiveHint: false`, `idempotentHint: true`, and `openWorldHint: false`.

| Tool | Human-readable title | Purpose |
| --- | --- | --- |
| `get_my_ilg_context` | Ver meu contexto ILG | Read the connected member's educational profile, access status, and learning streak. |
| `list_ilg_channels` | Listar canais da comunidade | List the community spaces and channels visible to the connected member. |
| `search_ilg_community` | Pesquisar a comunidade ILG | Search community questions, posts, and replies by keyword. |
| `get_ilg_thread` | Ler uma conversa da comunidade | Read one community post and its replies by post ID. |
| `list_my_ilg_questions` | Listar minhas perguntas | List the connected member's Q&A posts and whether staff replied. |
| `search_ilg_library` | Pesquisar a biblioteca ILG | Search published Radar, essays, learning paths, and resources. |

Prompts: none. Resources: none. Write tools: none.

## 3. Listing

- Server name: `Invest Like a Girl`
- Tagline (43/55): `Pesquise a comunidade e a biblioteca da ILG`
- Permanent slug: `invest-like-a-girl`
- Suggested categories: Education, Financial services, Productivity
- Documentation URL: `https://www.investlikeagirl.com.br/integracoes/claude`
- Privacy policy URL: `https://www.investlikeagirl.com.br/legal/privacy`
- Support contact: `contato@investlikeagirl.com.br`
- Icon URL: `https://www.investlikeagirl.com.br/images/ilg-logo.png`

### Description

Conecte o Claude à sua conta da Invest Like a Girl para pesquisar a comunidade privada e encontrar conteúdos educativos oficiais sem sair da conversa. O conector pode listar canais, pesquisar posts e respostas, ler uma conversa completa, acompanhar as perguntas que você publicou no Q&A e buscar Radar, crônicas, trilhas e recursos da ILG.

O acesso respeita a assinatura e as permissões da pessoa conectada. Todas as ferramentas são somente de leitura: o conector não publica, edita ou exclui conteúdo, não realiza pagamentos ou transações financeiras e não expõe e-mails, diretório de membros, anexos, dados de pagamento, registros de moderação ou aulas privadas. A autoria das participantes é preservada e o conteúdo da fundadora/equipe é identificado. Todo conteúdo financeiro é educativo e não constitui recomendação personalizada de investimento.

## 4. Use cases

### Primary use cases

1. Search past community conversations before asking a repeated question.
2. Read a relevant thread with its replies while preserving each author's name and community role.
3. Check which of the connected member's Q&A questions have received a staff response.
4. Find official ILG learning material related to a financial-education topic.
5. Discover the best community channel for a topic.

### Example prompts

1. `Usando a Invest Like a Girl, procure conversas da comunidade sobre reserva de emergência e resuma os pontos mais úteis, preservando a autoria.`
2. `Quais perguntas eu já publiquei no Q&A da ILG e quais receberam resposta da equipe?`
3. `Encontre na biblioteca da ILG materiais oficiais sobre renda fixa para iniciantes.`
4. `Liste os canais da Comunidade ILG e me diga onde é mais adequado conversar sobre previdência.`

### Prerequisites

- An Invest Like a Girl account is required.
- An active trial or paid membership is required to search community and learning content.
- The connected member can still read her own profile and access status without an active membership.
- Content and support are primarily in Brazilian Portuguese.

### Capabilities declaration

- Reads data: Yes
- Writes data: No
- Executes financial transactions: No
- Generates AI image, video, or audio: No
- Collects Claude conversation history, memory, summaries, or files: No

## 5. Company

- Company/product name: Invest Like a Girl
- Website: `https://www.investlikeagirl.com.br`
- Primary contact name: **Complete in the portal from the authorized account**
- Primary contact email: `contato@investlikeagirl.com.br`

## 6. Authentication

- Mode: OAuth with Dynamic Client Registration
- Authorization-server metadata: `https://www.investlikeagirl.com.br/.well-known/oauth-authorization-server`
- Protected-resource metadata: `https://www.investlikeagirl.com.br/.well-known/oauth-protected-resource`
- Client registration: `https://www.investlikeagirl.com.br/oauth/register`
- Authorization: `https://www.investlikeagirl.com.br/oauth/authorize`
- Token: `https://www.investlikeagirl.com.br/oauth/token`
- Revocation: `https://www.investlikeagirl.com.br/oauth/revoke`
- Access-token lifetime: 1 hour
- Refresh-token lifetime: up to 30 days, rotated on use

## 7. Data handling

- Underlying API/data source: First-party Invest Like a Girl service and database
- Server domain matches the service: Yes
- Third-party proxy: No
- Personal health data: No
- Sponsored content: No
- Conversation-data collection: No. The server receives only the tool name and arguments Claude sends for the requested call.
- Search terms and filters: Used transiently to query first-party data; not stored as community content.
- OAuth secrets: Opaque access and refresh tokens are stored only as irreversible hashes.
- Returned personal data: Connected member name, educational profile, membership state, learning streak, community posts/replies visible to the member, and published learning metadata.
- Explicit exclusions: Email addresses, member directory, attachments, payment data, moderation logs, private lesson bodies/files.
- Privacy and retention details: `https://www.investlikeagirl.com.br/legal/privacy#conector-ia`

## 8. Test and launch

### Test account — BLOCKED UNTIL COMPLETED

Anthropic requires a fully populated test account with credentials and end-to-end setup instructions. The normal ILG login is passwordless magic-link authentication, which does not give an external reviewer reusable credentials.

Before submission, create a dedicated reviewer account that:

- has a non-production, non-personal email controlled for review;
- can authenticate without depending on the product owner's inbox;
- has an active test membership;
- has a representative profile and streak;
- owns at least two Q&A posts, including one with a staff response;
- can see representative community channels, posts, replies, and learning-library results;
- contains no real member personal data beyond content already visible to any active member;
- can be revoked immediately after the review.

Portal instructions should include the exact login URL, username/email, password or reviewer-access method, expected consent screen, and four example prompts above. Never commit the credentials to this repository.

### Verification to record before submitting

- [ ] Every tool exercised successfully in MCP Inspector
- [ ] Every tool exercised successfully through a Claude custom connector
- [ ] OAuth connect, refresh, reconnect, and revoke tested
- [ ] Active-member account tested
- [ ] Inactive-member error tested and found actionable
- [ ] Invalid and missing arguments tested for each parameterized tool
- [ ] Documentation and privacy URLs are live in production
- [ ] Icon URL loads publicly
- [ ] Test reviewer account is fully populated and credentials are stored securely

## 9. Compliance acknowledgments

The authorized submitter must read and personally confirm every portal acknowledgment. Technical facts prepared for that review:

- Directory policy: implementation is designed to comply.
- First-party API: yes; Invest Like a Girl owns and controls the endpoint and underlying data service.
- Financial transactions: none.
- AI media generation: none.
- Prompt injection: tool descriptions contain no behavioral override, hidden instruction, or direction to invoke unrelated software.
- Conversation collection: none beyond the exact tool arguments needed to perform a requested query.
- Public documentation: provided at the documentation URL above.
- Directory terms: must be accepted by an authorized representative; this document does not accept them on anyone's behalf.

## 10. Launch notes

- Connector status: Production remote MCP is live.
- Availability: Read-only beta suitable for directory review.
- User-facing language: Brazilian Portuguese.
- Maintenance/support owner: Invest Like a Girl via `contato@investlikeagirl.com.br`.
- Allowed link URIs: Not applicable; this connector does not use the MCP Apps `ui/open-link` capability.
- Carousel screenshots: Not applicable; this is not an MCP App.
