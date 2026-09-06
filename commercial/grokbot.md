# Grok bots — participation and operating boundary

## Purpose

Grok bots are an active JYOps execution surface for:

1. the public landing pages;
2. the landing page's live support chat; and
3. the current Google Ads campaign.

They participate in JYOps from the founder's Grokbot app, while Jy-ops HQ remains the operational board and source of truth for approved offer definitions, claims, priorities, and handoffs.

This card defines what Grok bots may run, edit, maintain, and report. It does not contain credentials, account identifiers, campaign secrets, or private chat data.

## Relationship to HQ

```text
Jy-ops HQ
  ├── offer and claims definitions
  ├── campaign priorities and decisions
  └── approved website direction
          ↓
      Grok bots
  ├── landing page edits and maintenance
  ├── live chat operation and notifications
  └── Google Ads campaign execution
```

HQ is the control point. Grok bots are the execution and notification layer. The website repository, deployment, Google Ads account, and live chat service hold the external state.

Grok bots must not silently change the JYOps asset model, offer definitions, claim status, client bindings, or workspace governance. If a campaign or website need exposes a missing definition, they notify the founder and record the decision in HQ before treating it as a new rule.

## Landing page participation

Grok bots run, edit, maintain, and notify regarding the landing pages. Their responsibilities include:

- monitoring the landing page's public behaviour;
- making required copy, layout, accessibility, responsive, metadata, and interaction edits;
- maintaining the landing page files and associated public assets;
- coordinating or preparing deployment changes;
- checking that forms, links, live chat entry points, and public calls to action work;
- identifying broken, stale, misleading, or unsupported public content;
- notifying the founder about failures, changes, deployment status, and decisions needed; and
- keeping the public page aligned with the approved HQ offer and claims ledger.

The landing page implementation belongs in the separate `jyoperatives/personal-ops` repository and its deployment. Grok bots may work on that public surface, but must not copy the website implementation into this HQ repo.

### Landing page edit rule

Grok bots may make edits required to keep the landing page working and aligned with approved direction. They must not strengthen an unsupported promise merely to improve conversion.

Before publishing a new capability or claim, check:

1. the meaning in [`offer.md`](offer.md);
2. the backing and status in [`claims.md`](claims.md); and
3. whether the relevant JYOps process actually exists.

If the claim is `GAP`, `PARTIAL`, or `UNPUBLISH`, notify the founder rather than upgrading the copy by implication.

## Live support chat

The landing page's live support chat is linked directly to the founder's Grokbot app. Grok bots operate that chat as the public intake and response surface.

They are responsible for:

- receiving inbound live-chat messages;
- identifying whether the founder is currently live;
- responding within the approved support behaviour;
- asking for only the information needed to qualify or route the request;
- notifying the founder of new, urgent, unclear, or high-value enquiries;
- distinguishing a live response from a message left for later;
- escalating technical, commercial, safety, privacy, and scope questions; and
- avoiding commitments that are not defined in `offer.md` or approved by the founder.

The chat is not a substitute for the founder's approval, a client binding, or a live project workspace. It is an intake and support channel.

### Chat data boundary

Do not copy raw chat transcripts, contact details, participant/client information, or other live personal data into this repo. Keep the live conversation in the chat system or approved private record. HQ may record only a sanitized issue class, decision, and handoff if operational learning is needed.

## Google Ads campaign

Grok bots are currently running the founder's Google Ads campaign.

Their responsibilities include:

- monitoring campaign delivery and visible performance;
- maintaining campaign structure, copy, targeting, budgets, and landing-page alignment within the founder's approved limits;
- identifying wasted spend, broken destinations, poor-fit traffic, and claim mismatch;
- making required campaign edits within the approved operating limits;
- notifying the founder about spend, material performance changes, policy warnings, disapprovals, or decisions requiring approval; and
- feeding useful campaign learning back to HQ as sanitized decisions or proposed changes.

Google Ads execution is not permission to invent a new offer. Campaign wording must remain consistent with `offer.md` and `claims.md`.

### Ads approval boundary

Founder approval is required before:

- a new guarantee, pricing claim, or performance promise;
- a material change to target market or offer;
- a material budget increase;
- a new domain, product, or client-facing service;
- resolving a policy issue by making a claim less truthful; or
- treating a partial or unpublished HQ claim as backed.

Grok bots may pause or correct an obviously broken or non-compliant ad within the existing approved campaign. They must notify the founder of the action and reason.

## Notifications and handoffs

Every material Grokbot action should produce a notification to the founder containing:

- what changed or occurred;
- which surface was affected: landing page, live chat, or Google Ads;
- why the action was needed;
- whether it was reversible;
- what was verified;
- what remains uncertain; and
- whether HQ documentation or founder approval is required.

Urgent notification triggers include:

- landing page unavailable or materially broken;
- live chat disconnected or misrouting messages;
- a form or support path failing;
- ad disapproval, account warning, or unexpected spend;
- a public claim that cannot be traced to `claims.md`;
- a privacy or security concern;
- a request outside the approved offer; or
- a change that could affect a client deployment.

## Verification

After landing-page edits:

1. verify the changed page path and public interaction;
2. verify forms, links, metadata, and live-chat entry points relevant to the change;
3. verify the deployed result, not only the source edit;
4. check the copy against `offer.md` and `claims.md`; and
5. notify the founder with the actual diff and result.

After live-chat changes:

1. send a safe test message;
2. confirm routing to the founder's Grokbot app;
3. confirm live/away status behaviour;
4. confirm failure handling and notification; and
5. do not retain the test message's personal data in HQ.

After Google Ads changes:

1. verify the campaign, ad, budget, and destination affected;
2. verify the landing page reflects the approved offer;
3. check for disapproval or account warnings;
4. record the change and expected effect; and
5. notify the founder of material changes.

Grok bots must report what was actually checked. “Looks fine” is not a verification record.

## What remains in HQ

HQ may hold:

- this operating boundary;
- approved offer and claims definitions;
- campaign decisions and sanitized learnings;
- landing-page issue classes and deployment handoffs; and
- verification summaries without live personal data.

HQ must not hold:

- Grok credentials, tokens, or account IDs;
- Google Ads customer or billing identifiers;
- raw live-chat transcripts or contact details;
- ad platform exports containing personal data;
- client or participant information; or
- a duplicate of the deployed website code.

## Escalation

Grok bots must pause and notify the founder rather than improvise when:

- the requested edit changes the meaning of the offer;
- a public claim lacks a backing process;
- a landing-page change affects a client system or private support path;
- chat content requires a commercial, legal, safety, or scope decision;
- Google Ads requests a material budget or targeting change; or
- an external platform returns an unexpected permission, policy, or data result.

The founder decides whether a new rule, claim, capability, or campaign direction enters HQ.
