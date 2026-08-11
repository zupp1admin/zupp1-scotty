# USS Zupp1 — XO-007 Comprehensive Plugin Audit

**Mission:** XO-007 — Comprehensive WordPress Plugin Audit & Rationalization  
**Audit date:** 11 August 2026  
**Platform:** WordPress 7.0.3, PHP 8.3.30, Astra 4.13.9, WooCommerce 11.0.1  
**Verification status:** PARTIALLY VERIFIED — inventory and immediate actions verified; several production journeys still require controlled tests

## 1. Executive Summary

The audit identified **58 installed plugin entries**. Before XO-007, 54 were active and 4 inactive. Six evidence-backed components were deactivated during this mission, leaving **48 active and 10 inactive**. No plugin, configuration, license or historical data was deleted.

The platform is not suffering from one simple category of plugin excess. It contains a legitimate commerce core, a substantial custom Zupp1 operating layer, and several remnants of earlier experiments. The largest maintainability risk is the combined estate of **27 custom plugins plus 49 Code Snippets records, of which 26 are active**. Code Snippets is therefore operationally mission-critical even though individual snippets require a separate governance audit.

The most important rationalizations completed were:

- UpdraftPlus retained as the canonical backup system; Duplicator deactivated after a stale 1.49 GB job remained at 65% while verified UpdraftPlus backups operated correctly.
- Bit Social retained as the canonical social publisher; unconfigured Amazon and Shopee social-poster plugins deactivated.
- Zupp1 Redirect Manager retained as the canonical custom redirect system; the single-purpose Cookie Policy Redirect plugin deactivated after the identical rule was verified in Redirect Manager.
- The completed Dropi pricing pilot and obsolete automatic draft publisher were deactivated.
- Uncanny Automator was identified as unused, with five draft recipes and no active recipe. Normal deactivation did not persist and direct administrative navigation was blocked, so it remains active pending manual intervention.

## 2. Utility Classes

- **A — Mission Critical:** site, commerce, security, recovery, transactional communication or runtime dependency.
- **B — Strategic:** strong long-term value aligned with the Zupp1 operating model.
- **C — Useful:** measurable benefit, but the platform can operate without it.
- **D — Situational:** useful for specific interventions; normally inactive outside those missions.
- **E — Redundant:** function is replaced or duplicated elsewhere.
- **F — Obsolete:** no continuing operational mission.

## 3. Complete Third-Party Plugin Inventory

| Plugin | Version | State | Class | Maintainer / area | Configuration, dependency and rationale |
| --- | --- | --- | --- | --- | --- |
| AddToAny Share Buttons | 1.8.18 | Active | C | AddToAny / sharing | Configured for post sharing with centered presentation. Useful, modest frontend payload; retain while share engagement is measured. |
| All in One SEO | 5.0.0.1 | Active | B | AIOSEO / SEO | Primary SEO, sitemap and metadata layer. Configured and actively used across posts/products. Retain as canonical SEO system. |
| Bit Social | 1.16.0 | Active | B | Bit Apps / social publishing | Base runtime required by Bit Social Pro. Six connected destinations and active eight-hour schedule verified. |
| Bit Social Pro | 1.16.0 | Active | B | Bit Apps / social publishing | Pro capability layer for the configured social workflow. Intentional dependency on Bit Social base; not a duplicate installation. |
| Broken Link Checker by AIOSEO | 1.3.0 | Active | C | AIOSEO / link quality | Complements AIOSEO. Keep while broken-link monitoring is used; cloud/scan cadence remains to be documented. |
| Code Snippets | 3.9.6 | Active | A | Code Snippets Pro / custom runtime | 49 records, 26 active. Provides storefront, WooCommerce, Biblioteca and presentation behavior. High security and maintenance burden; cannot be removed until every active snippet is governed or migrated. |
| Content Views | 4.5.1 | Active | B | Content Views / content presentation | Eight published views verified for Biblioteca categories and recent posts. Active dependency of public presentation. |
| Duplicator | 1.5.16.1 | **Inactive — XO-007** | D | Duplicator / migration | Backup function replaced by UpdraftPlus. One stale 1.49 GB package remained at 65%. Retain inactive only for a future controlled migration/staging mission. |
| Classic Editor | 1.7.0 | Active | B | WordPress contributors / editing | Matches the approved HTML-first editorial workflow and supports existing meta boxes. Strategic operational dependency. |
| Fluent Support | 2.3.1 | Active | B | WPManageNinja / support | Local ticket source integrated into Mission Control. Current zero-ticket volume does not eliminate its customer-support mission. |
| MonsterInsights | 11.1.2 | Active | B | MonsterInsights / analytics | GA4 property connected and page measurement verified. Ecommerce events and reporting connector remain incomplete; retain but classify configuration as partial. |
| Optimole | 4.2.10 | Active | B | Optimole / image delivery | Connected; 54% of monthly allowance used, 27.28 MB saved, 90.94% average reduction. Smart lazy-loading and responsive scaling active. |
| Image Watermark | 2.0.12 | Active | B | dFactory / brand protection | Configured for automatic/manual watermarking with `Zupp1.com.br`, 15% scale and 25% opacity. Complements rather than duplicates Optimole. |
| IndexNow | 1.0.4 | Active | C | Microsoft Bing / discovery | Installed with no excluded paths, but no verified submissions in the last 48 hours. Retain temporarily; verify automation before deciding whether AIOSEO can replace it. |
| Joinchat | 6.3.2 | Active | C | Creame / WhatsApp | Customer-contact capability. Configuration screen is available; public visibility and approved home-only delay need a focused verification. |
| LiteSpeed Cache | 7.9 | Active | A | LiteSpeed Technologies / performance | Correct server-native caching layer for LiteSpeed. Canonical page/cache optimization system; avoid adding competing cache plugins. |
| Meta for WooCommerce | 3.7.6 | Active | B | Meta / campaign attribution | Pixel `2100702700874180` and ViewContent evidence verified. Plugin reports untested compatibility with WooCommerce 11.0.1; purchase/CAPI deduplication remains unproven. |
| Pagar.me for WooCommerce | 3.9.0 | Active | A | Pagar.me / payment | Primary payment gateway. Version 3.10.1 intentionally held because WordPress 7.0.3 compatibility is untested. Requires controlled payment test. |
| Stripe Gateway for WooCommerce | 10.8.5 | Active | C | Stripe / payment | Potential alternative/fallback gateway. Enabled-state and production necessity require Captain confirmation; do not remove until payment strategy is explicit. |
| Uncanny Automator | 7.5.0.3 | Active | E | Uncanny Owl / automation | Five recipes verified, all drafts. Bit Social and custom systems supply live automation. Normal deactivation did not persist; manual intervention required. |
| UpdraftPlus | 1.26.6 | Active | A | TeamUpdraft / recovery | Canonical backup system. Database/files every 12 hours, 14-set retention, Google Drive destination and successful complete transfer verified. |
| UserFeedback Lite | 1.11.3 | Inactive | D | UserFeedback / surveys | No active survey mission. Retain inactive pending deletion approval or a defined customer-research experiment. |
| Classic Widgets | 0.3 | Active | C | WordPress contributors / administration | Preserves classic widget workflow compatible with Astra and the operator’s editing preference. Low complexity. |
| WooCommerce | 11.0.1 | Active | A | Automattic / commerce | Canonical commerce platform and dependency of payments, Meta and many Zupp1 tools. Mission critical. |
| Wordfence Security | 9.0.0 | Active | A | Wordfence / security | Fresh scan completed with zero findings. WAF optimization and administrator 2FA remain deferred security interventions. |
| WP Headers and Footers | 3.1.5 | Active | C | WPBrigade / verification tags | Current audited use is a Bing verification tag. Candidate for consolidation into a governed verification mechanism after ownership is confirmed. |
| WP Mail SMTP | 4.9.0 | Active | A | WP Mail SMTP / transactional email | Connected to SendLayer with forced sender name. Essential for order/support email reliability; custom-domain sender and backup connection are future improvements. |
| WP RSS Aggregator | 5.4.0 | Active | C | RebelCode / external content feed | Fifteen feed items verified from an external source. Configuration is active but editorial/copyright/SEO governance and source display intent require review. |
| WPConsent | 1.1.8 | Active | A | WPConsent / privacy | Opt-in banner, script blocking and Consent Mode v2 previously verified. Custom affiliate tracker classification remains an unresolved consent gap. |
| WPForms Lite | 2.0.0.3 | Active | B | WPForms / forms | Three forms render on the contact page. Required for contact/customer journey; delivery depends on WP Mail SMTP. |

## 4. Complete Zupp1 Plugin Inventory

| Plugin | Version | State | Class | Area | Configuration, dependency and rationale |
| --- | --- | --- | --- | --- | --- |
| Zupp1 Affiliate Product Builder | 1.1.0 | Active | B | Amazon product drafting | Configured with Amazon tag `zupp1-20`, ASIN validation, draft-only output and editorial/SEO fields. Overlaps Amazon Importer but serves a richer editorial-first workflow. |
| Zupp1 Ajustador de Preços | 1.1.0 | Active | C | bulk pricing | Preview-first bulk percentage/fixed/psychological pricing. Retain while pricing governance is consolidated. |
| Zupp1 Amazon Importer | 1.0.0 | Active | B | Amazon importing | Supports batch import, image copying, status and visibility control. Overlaps Affiliate Builder; consolidation decision requires usage evidence. |
| Zupp1 Amazon Social Poster | 1.1.0 | **Inactive — XO-007** | E | social publishing | Failed because account IDs/tokens were not configured. Bit Social already supplies configured social destinations. Data and logs preserved. |
| Zupp1 Catalog Manager | 1.0.0 | Active | C | catalog operations | Checklist interface for categories and featured status. Distinct from bulk category cleanup. |
| Zupp1 Category Manager | 1.1.1 | Active | C | catalog operations | Preview, category cleanup and undo workflow. Partial overlap with Catalog Manager, but different operational safeguards. |
| Zupp1 Content Studio | 1.1.2 | Active | B | editorial operations | Central workspace for media, featured images, post HTML and affiliate-quality audits. Strategic Biblioteca governance tool. |
| Zupp1 Cookie Policy Redirect | 1.0.0 | **Inactive — XO-007** | E | redirects | Exact route already existed in Zupp1 Redirect Manager. Public 301 continued successfully after deactivation. |
| Zupp1 Direct Shopee Link Auditor | 1.0.0 | Inactive — XO-006 | D | affiliate audit | Explicitly temporary read-only diagnostic. Keep inactive for targeted future audits only. |
| Zupp1 Dropi Pricing — primary copy | 1.0.0 | **Inactive — XO-007** | D | pricing pilot | Five-product pilot completed with stored rollback log. Reactivate only for the documented pilot/rollback purpose. |
| Zupp1 Dropi Pricing — duplicate copy | 1.0.0 | Inactive | F | duplicate installation | Exact duplicate folder/entry. Candidate for deletion after Captain approval; no runtime mission. |
| Zupp1 Alt Text Manager | 1.0.0 | Active | C | accessibility/SEO | Fills missing alt text locally using post/product context. Complements Optimole; effectiveness should be periodically sampled. |
| Zupp1 Automatic Internal Links | 1.1.3 | Active | B | content continuity | Maintains related-guide sections using category/text similarity. Strategic for Biblioteca journeys; verify it does not duplicate manually curated sections. |
| Zupp1 Local Product Rewriter | 2.0.3 | Active | B | product editorial | Local, reviewable product rewriting with backups and SEO fields. Supports catalog quality without external API dependency. |
| Zupp1 Management System | 0.3.0 | Active | B | pricing governance | Seventy-one audited price changes with rollback history verified. Canonical applied-price audit trail. |
| Zupp1 Maintenance | 1.0.0 | Active | C | maintenance | Safe health and database-cleanup workstation. Some overlap with Site Health and LiteSpeed tools; retain until its unique actions are inventoried. |
| Zupp1 Mission Control | 1.1.0 | Active | B | operational intelligence | Admin-only aggregation, baseline, anomaly watch, campaign memory and Captain’s Briefing. No frontend payload. |
| Zupp1 Site & Affiliate Product Monitor | 1.0.2 | Active | B | affiliate/content maintenance | Monitors posts and product grids and removes unavailable product blocks. Strategic affiliate-quality control. |
| Zupp1 Metrics — Safe Attribution | 2.1.0 | Active | B | affiliate analytics | Canonical direct Shopee click evidence and UTM/Meta session attribution. Preserves links and affiliate IDs; Mission Control dependency. |
| Zupp1 Operations Center | 1.0.1 | Active | B | institutional memory | Private operational documentation library. Strategic implementation of The Book principles. |
| Zupp1 Pinterest Organic | 1.1.1 | Active | B | organic discovery | Provides optimized feeds and save controls. Intentional complement to Bit Social’s account publishing, not necessarily a duplicate. |
| Zupp1 Post Format Repair | 1.0.0 | Inactive — XO-006 | D | editorial repair | Explicitly temporary audit/repair tool. Reactivate only for approved targeted repairs. |
| Zupp1 Presentation Foundation | 1.0.2 | Active | B | presentation standards | Reusable hero and decision-support components. Preserves approved DOM/CSS consistency across storefront pages. |
| Zupp1 Price Suggestor | 1.0.0 | Active | B | pricing decision support | Display-only cost/freight/margin calculation. Distinct from Management System’s applied-price audit and bulk adjustment. |
| Zupp1 Automatic Publisher | 1.1.2 | **Inactive — XO-007** | F | draft generation | No next execution scheduled. Previous template batch belongs to the rejected draft-generation workflow and conflicts with the new publication gate. |
| Zupp1 Redirect Manager | 2.0.0 | Active | B | redirects | Canonical custom 301/302 register. Two active rules verified, including the cookie-policy consolidation. |
| Zupp1 Shopee Product Manager | 1.0.1 | Active | B | Shopee migration/catalog | Extensive migration evidence verified; preserves affiliate links including `an_18376601073`. Strategic affiliate catalog tool. |
| Zupp1 Shopee Social Poster | 1.1.0 | **Inactive — XO-007** | E | social publishing | No products and no publication log. Bit Social is the configured canonical publisher. |

## 5. Configuration Assessment

### Fully or substantially configured

WooCommerce, UpdraftPlus, Bit Social/Pro, Content Views, Optimole, Image Watermark, WP Mail SMTP, WPForms, AIOSEO, LiteSpeed Cache, Zupp1 Management, Mission Control, Shopee Product Manager, Metrics, Operations Center and Redirect Manager show evidence of active configuration or production use.

### Partially configured or requiring production proof

- **MonsterInsights:** traffic collection works; ecommerce event contract/reporting remains incomplete.
- **Meta for WooCommerce:** Pixel and ViewContent verified; purchase/CAPI deduplication and WooCommerce 11.0.1 compatibility remain unproven.
- **Wordfence:** scanning works; WAF optimization and 2FA are incomplete.
- **Pagar.me/Stripe:** payment roles and controlled transaction verification remain incomplete.
- **WPConsent:** custom affiliate tracker consent classification remains unresolved.
- **IndexNow:** no recent submission evidence.
- **WP RSS Aggregator:** imported items exist; source/display/editorial governance is unclear.
- **Joinchat:** public scope and delay should be checked against the approved home-only behavior.
- **Broken Link Checker:** monitoring cadence and ownership are not documented.

### Inactive/situational or nonfunctional

UserFeedback, Duplicator, the two social-poster plugins, Cookie Policy Redirect, Direct Shopee Link Auditor, both Dropi Pricing copies, Post Format Repair and Automatic Publisher are inactive. Uncanny Automator is functionally unused but remains active pending manual intervention.

## 6. Functional Overlap Analysis

| Area | Components | Assessment |
| --- | --- | --- |
| Backups | UpdraftPlus, Duplicator | UpdraftPlus is canonical and verified; Duplicator moved to inactive situational status. |
| Social publishing | Bit Social/Pro, Uncanny Automator, Amazon Social Poster, Shopee Social Poster | Bit Social is configured and canonical. Custom posters deactivated. Automator has only drafts and should be manually deactivated. |
| Redirects | Zupp1 Redirect Manager, Cookie Policy Redirect, AIOSEO redirects | Redirect Manager is canonical custom register. Single-purpose cookie plugin deactivated. AIOSEO redirect capability should remain disabled/unlicensed unless deliberately adopted. |
| Amazon importing | Affiliate Product Builder, Amazon Importer | Genuine overlap. Builder is editorial/SEO-first and draft-only; Importer is operational/batch/image-first. Collect usage before consolidation. |
| Pricing | Price Suggestor, Management System, Ajustador de Preços, Dropi Pricing | Roles differ: suggestion, audit/rollback, bulk adjustment and completed pilot. Pilot deactivated; remaining three require a unified pricing doctrine. |
| Analytics | MonsterInsights/GA4, Meta, Zupp1 Metrics, WooCommerce Analytics, Mission Control | Intentional source specialization. Mission Control aggregates but does not replace tracking. No duplicate Meta Pixel was introduced. |
| Images | Optimole, Image Watermark, Alt Text Manager | Complementary: delivery, branding and accessibility. No consolidation recommended. |
| SEO/discovery | AIOSEO, Broken Link Checker, IndexNow, Pinterest Organic, Internal Links | Mostly complementary. IndexNow effectiveness and internal-link duplication require measurement. |
| Maintenance | WordPress Site Health, LiteSpeed tools, Zupp1 Maintenance, Wordfence | Different layers, but Zupp1 Maintenance actions should be inventoried to prevent duplicate cleanup operations. |
| Content automation | Automatic Publisher, RSS Aggregator, Content Studio, Biblioteca publication gate | Automatic Publisher conflicts with the editorial gate and was deactivated. RSS remains curation input; Content Studio/publication gate governs Zupp1-owned publishing. |

## 7. Plugins Deactivated

1. Duplicator
2. Zupp1 Amazon Social Poster
3. Zupp1 Shopee Social Poster
4. Zupp1 Automatic Publisher
5. Zupp1 Dropi Pricing active pilot copy
6. Zupp1 Cookie Policy Redirect

Earlier XO-006 deactivations retained:

- Zupp1 Direct Shopee Link Auditor
- Zupp1 Post Format Repair

All deactivations are reversible. No data was deleted.

## 8. Items Requiring Captain or Manual Intervention

- Manually deactivate Uncanny Automator after confirming no hidden dependency; ordinary deactivation did not persist.
- Approve deletion of confirmed obsolete/inactive copies only after an observation period.
- Decide whether Stripe is an intended production gateway or an unused fallback.
- Approve consolidation strategy for Affiliate Product Builder versus Amazon Importer.
- Review active Code Snippets, especially the active `TEMP — Reset Meta catalog products` snippet, outside the plugin-only authorization boundary.
- Confirm whether WP Headers and Footers should remain solely for Bing verification.
- Resolve the Pagar.me update only after compatibility and payment testing.

## 9. Performance Impact Assessment

The highest likely runtime contributors are WooCommerce, Meta for WooCommerce, MonsterInsights, WPConsent, LiteSpeed Cache, Optimole, Joinchat, AddToAny, Bit Social hooks, Content Views and the 26 active Code Snippets. Not every active admin plugin adds frontend payload, but 48 active plugins increase hook execution, update burden and conflict probability.

The six XO-007 deactivations mainly remove admin/cron/background load. They should reduce scheduled-task complexity and eliminate a stale large Duplicator process without changing the public design. A numeric before/after performance benchmark is not yet available, so no speed improvement is claimed as proven.

## 10. Security Considerations

- Every custom plugin and active snippet is code maintained outside a marketplace update channel.
- Code Snippets is a concentrated execution surface and should receive its own doctrine, ownership and review register.
- Wordfence scan returned zero findings, but WAF and administrator 2FA remain incomplete.
- Inactive plugins remain attack-surface files until deleted; deletion requires separate approval after observation.
- Pagar.me remains intentionally behind one update because compatibility is uncertain.
- Affiliate identifiers and Meta Pixel were preserved during all changes.

## 11. Long-Term Simplification Plan

### Stage 1 — Observe deactivations

Keep deactivated plugins installed for a defined observation window. Monitor checkout, affiliate clicks, social publishing, content presentation, backups and redirects.

### Stage 2 — Govern custom code

Create one register for every custom plugin and active snippet: owner, purpose, dependencies, last use, verification method, rollback and retirement trigger. Move stable related snippets into tested, versioned domain plugins rather than accumulating more snippets.

### Stage 3 — Consolidate operational domains

- Choose one Amazon product-entry workflow or define exact boundaries.
- Publish a unified pricing architecture covering suggestion, bulk changes and audit/rollback.
- Keep Bit Social as canonical social publisher unless a verified capability gap emerges.
- Keep Redirect Manager as canonical redirect register.

### Stage 4 — Retire files

After a stable observation period and Captain approval, delete only the plugins classified E/F or obsolete duplicate copies. Preserve exportable configuration and decision history before deletion.

## 12. Strategic Recommendations

Do not install another optimization, security, analytics, redirect, backup, SMTP or social-publishing plugin. Existing systems already cover those domains. The next strategic investment should be governance and controlled verification, not additional plugin capability.

## 13. Intelligence Gaps

- Controlled checkout and payment evidence for Pagar.me and Stripe.
- GA4 ecommerce and Meta purchase/CAPI deduplication.
- Exact frontend performance contribution by plugin.
- Hidden dependency preventing Uncanny Automator deactivation.
- Usage frequency of the two Amazon import tools.
- Joinchat public scope/delay compliance.
- IndexNow submission effectiveness.
- WP RSS Aggregator’s intended public display and editorial rights model.
- Complete dependency map for 26 active snippets and 27 custom plugins.

## 14. Verification Evidence

After rationalization, the following remained operational:

- Homepage and approved H1.
- Loja hero and 43 product displays.
- Eight Shopee affiliate links using `an_18376601073`.
- Meta Pixel `2100702700874180` scripts.
- Cart.
- Contact page and three forms.
- Mission Control.
- UpdraftPlus backup interface and stored backups.
- `/cookie-policy/` public redirect to `/politica-de-cookies/` after the single-purpose redirect plugin was deactivated.

**Final status:** PARTIALLY VERIFIED. Inventory, classification, deactivations and immediate regression checks are verified. Payment, analytics attribution, hidden dependencies and long-term observation remain open.
