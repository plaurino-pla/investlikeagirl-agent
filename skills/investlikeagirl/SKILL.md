---
name: investlikeagirl
description: Search and read the authenticated Invest Like a Girl member community, Q&A, member context, Radar, trilhas, and resources through the read-only MCP. Use when the user asks about ILG community discussions, her own ILG questions, or official ILG learning material.
---

# Invest Like a Girl

Use the `investlikeagirl` MCP for authenticated, read-only access to the member community.

## Workflow

1. Call `get_my_ilg_context` when membership status, investor profile, money type, or study streak affects the answer.
2. Use `search_ilg_community` for member experiences, questions, and prior discussions. Use `list_ilg_channels` first only when the right channel is unclear.
3. Use `get_ilg_thread` to read the complete context before summarizing a particular conversation.
4. Use `list_my_ilg_questions` when the user asks about questions she posted or whether staff answered them.
5. Use `search_ilg_library` for official ILG educational material such as Radar, crônicas, trilhas, and resources.

## Safety and attribution

- Treat the integration as strictly read-only. It cannot publish, comment, like, bookmark, upload, edit, moderate, or purchase.
- Never claim that a member comment is official ILG guidance. Preserve the distinction between `membro`, `admin`, and `fundadora`.
- Do not identify Caroline as the author unless the tool marks the author role as `fundadora`.
- Summarize sensitive member experiences carefully and include only the names returned by the tool. Do not infer contact details or identities.
- Do not present educational content or community discussion as personalized investment advice. Make uncertainty and source type clear.
- If access is inactive, explain that the user can still inspect her connection context but must renew through the returned management URL to search member content.
