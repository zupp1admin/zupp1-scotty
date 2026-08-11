# USS ZUPP1 — XO-008 Code Snippets Governance and Runtime Consolidation

**Date:** 2026-08-11  
**Scope:** All Code Snippets records in WordPress  
**Operating constraint:** Preserve the existing public UX. No visible behavior may be removed or altered during governance cleanup.

## Executive Summary

The Code Snippets inventory contains **49 records**: **25 active** and **24 inactive** after this mission. Before intervention, 26 were active and 23 inactive.

Only one immediate runtime change was made:

- **Snippet 43 — `TEMP — Reset Meta catalog products` was deactivated.** It is an admin-only, one-time Meta catalog deletion routine protected by a completion flag. It has no continuing operational purpose and leaving it active creates unnecessary catalog risk.

No snippet responsible for the storefront, navigation, heroes, product cards, prices, filters, checkout, affiliate links, Biblioteca, trust messages, support access, or other visible content was deactivated.

Public regression checks passed after the change:

| Surface | Expected visible state | Result |
|---|---|---|
| Homepage | H1 `Comprar ficou fácil. Escolher bem ficou difícil.`; navigation; products | Verified |
| Loja | H1 `Escolhas práticas para sua casa.`; navigation; 43 product/card elements | Verified |
| Cart | H1 `Carrinho`; navigation | Verified |
| Biblioteca | H1 `Toda boa escolha começa com compreensão.`; navigation; content/product output | Verified |
| Runtime | No visible fatal, parse, warning, or uncaught-error text | Verified |

## Governance Decision

The present snippet collection is functioning, but it is not yet a maintainable architecture. Important storefront behavior is distributed across large global snippets; some CSS is embedded in PHP despite the established Astra Custom CSS standard; several snippets overlap; one contains an internally duplicated code block; and 14 inactive copies of the Loja implementation remain in the database.

The correct next step is **controlled migration, not broad deactivation**.

## Complete Register

### Active after XO-008

| ID | Snippet | Operational role | Classification | Decision |
|---:|---|---|---|---|
| 1 | Tornar os nomes dos arquivos minúsculos no envio | Media filename hygiene | Utility | Keep |
| 2 | Desativar barra de administração | Hides admin bar from non-administrators | Access/UX | Keep; document role behavior |
| 3 | Permitir smilies | Sample filter affecting titles/widgets | Legacy utility | Keep for now; compare output before retirement |
| 6 | Pintrest | Adds featured images/namespaces to feeds | Distribution | Keep pending Pinterest feed comparison |
| 7 | Zupp1 - Imagem destacada no post | Despite its name, injects delivery/return information into product cards | Commerce UX | Keep; rename later because intent is unrecoverable from title |
| 10 | Zupp1 - Ocultar autor e data nos posts | Hides post metadata | Editorial UX | Keep |
| 11 | Zupp1 - Verificacao de dominio Pinterest | Pinterest verification meta tag | Integration | Keep until verification ownership is documented |
| 12 | woocommerce categorias | `[zupp_categorias_produtos]` product-category output | Commerce UX | Keep |
| 13 | Troca o botão da vitrine por "Veja detalhes" | Storefront CTA wording | Commerce UX | Keep |
| 15 | Zupp1 — Informações nos cards | Direct/partner delivery and return messages | Trust/commerce UX | Keep; reconcile overlap with ID 7 |
| 16 | Zupp1 – Mostrar 4 Produtos Relacionados | Related-product count/columns | Product UX | Keep |
| 18 | Zupp1 — Produtos aleatórios da categoria do post. | `[zupp_category_products]` editorial-to-product bridge | Content commerce | Keep |
| 19 | Zupp1 - Otimizacao de scripts front-end | Dequeues scripts and scopes Dropi reviews | Performance | Keep; remove internally duplicated block only after page tests |
| 20 | Zupp1 - Loja dividida em secoes por categoria (sem contagem) | Loja hero contract, H1/breadcrumb behavior, category sections, partner badges and extensive presentation CSS | Mission critical storefront | Freeze; migrate only through dedicated visual-regression mission |
| 21 | Zupp1 - Selos de confianca perto do botao de compra (produto) | Purchase benefits, trust badges and affiliate disclosure | Trust/commerce UX | Keep |
| 22 | Zupp1 - Ocultar quantidade exata de estoque | Prevents imported placeholder quantities from misleading customers | Trust | Keep |
| 38 | Zupp1 — Blog card images edge-to-edge | Biblioteca card presentation CSS | Content UX | Keep; later move CSS to Astra standard |
| 40 | Zupp1 — Promessa central da marca | Replaces public copy and renders community page content | Brand/content | Keep; migrate durable page content into WordPress content |
| 41 | Zupp1 — Busca, filtros e preços visíveis | Loja search, category/price/seller filters, visible pricing and related presentation | Mission critical storefront | Freeze; migrate as tested plugin module |
| 42 | Zupp1 — Substituir vídeo principal | Output-buffer replacement of homepage video URL | Hero compatibility patch | Keep until the canonical page source is corrected |
| 46 | remover comentarios no woocommerce | Removes WooCommerce review tab | Product UX | Keep pending product-template policy review |
| 48 | Zupp1 — Produto em destaque dentro do texto (uso manual). | Manual product shortcodes inside articles | Editorial commerce | Keep; move CSS to Astra standard later |
| 49 | Fix WooCommerce Pagar.me Thank You Redirect | Forces canonical order-received return URL | Checkout compatibility | Keep; Captain John confirms the current Pagar.me payment flow works, but the redirect snippet should remain until its specific necessity is isolated in staging |
| 50 | Zupp1 - Botão flutuante Telegram | Public Telegram support control | Support UX | Keep |
| 53 | Zupp1 Biblioteca Publication Gate — Runtime | Forces Draft Engine output to draft and records publication governance | Editorial safety | Keep; priority candidate for governed plugin module |

### Deactivated during XO-008

| ID | Snippet | Reason | Reversibility |
|---:|---|---|---|
| 43 | TEMP — Reset Meta catalog products | Completed one-time admin routine capable of deleting Meta catalog products; no ongoing mission | Still installed and can be reactivated; no code or configuration deleted |

### Already inactive

| ID | Snippet | Assessment | Recommended disposition |
|---:|---|---|---|
| 4 | Ano atual | Unused sample shortcode | Export, then retire with approval |
| 8 | Zupp1 - Centralizar Related Posts (CRP) | Superseded presentation experiment | Export, then retire with approval |
| 9 | Meta Pixel - Zupp1 | Historical custom Pixel implementation; must remain inactive because the official Meta integration owns tracking | Preserve as historical evidence; never activate alongside the official Pixel |
| 17 | Zupp1 — Posts relacionados da mesma categoria | Superseded related-content behavior | Export, then retire with approval |
| 23–36 | 14 copies of Loja divided by category | Duplicate historical copies | Export one archival copy and retire duplicates with approval |
| 37 | Trust badges copy | Duplicate of active trust behavior | Export, then retire with approval |
| 39 | Recomendações globais de menor preço | Inactive recommendation experiment | Keep inactive until commercial relevance is reevaluated |
| 47 | tamanho da foto do produto nos posts | Inactive presentation rule | Compare against Astra CSS, then retire or migrate |
| 51 | Promessa central da marca copy | Duplicate of active brand snippet | Export, then retire with approval |
| 52 | Biblioteca Governance — Stage 1 | Superseded by active runtime gate ID 53 | Preserve as historical context, then retire with approval |

## Overlap and Risk Findings

### Critical maintainability findings

1. **Loja is governed by two large coupled snippets (IDs 20 and 41).** They jointly control its DOM, product discovery, prices, categories, headings, hero behavior, badges and presentation. Neither can be safely deactivated in isolation.
2. **Presentation CSS exists inside PHP snippets**, especially IDs 20, 38, 41, 48 and 50. This conflicts with the approved rule that shared visual standards belong in Astra Custom CSS. Moving it prematurely would risk cascade/order changes, so migration requires before/after screenshots at desktop and mobile sizes.
3. **ID 19 contains a duplicated optimization block.** It repeats Dropi review registration and the script-tag filter. This should be corrected, but only in a separate tested change because product reviews are customer-facing.
4. **IDs 7 and 15 overlap around product-card policy information.** Their combined rendered behavior must be mapped before consolidation.
5. **ID 42 is a brittle output-buffer patch.** The durable fix is to update the canonical homepage hero source, verify the approved hero DOM, then remove the replacement snippet.
6. **ID 40 stores durable page content in executable code.** Page copy should ultimately live in the page/database, while code should supply behavior.
7. **Fourteen inactive Loja copies increase archaeology and error risk.** They do not affect runtime, but should be exported and retired after explicit deletion approval.

## Recommended Runtime Architecture

Create one version-controlled **Zupp1 Runtime** plugin, but migrate in stages:

1. **Governance module:** Biblioteca publication gate and audit metadata.
2. **Integration module:** Pinterest verification/feed behavior and Pagar.me compatibility.
3. **Editorial commerce module:** product shortcodes and guide-to-product behavior.
4. **WooCommerce trust module:** stock wording, disclosures, card information and product tabs.
5. **Storefront module:** Loja rendering, search and filters—last, because it has the greatest visible blast radius.

Shared CSS must remain in Astra Custom CSS. The plugin should provide semantic HTML and behavior, not duplicate the design system.

## Required Migration Gate

No visible snippet should be replaced or deactivated until all of the following are true:

- replacement code is installed but disabled or feature-flagged;
- exact hooks and priorities are mapped;
- desktop and mobile screenshots exist for homepage, Loja, category, product, Biblioteca and cart;
- search, category, price and marketplace filters are exercised;
- direct-sale and Amazon/Shopee product paths are checked;
- affiliate identifiers and Meta Pixel ownership are verified unchanged;
- the Pagar.me return path remains unchanged and is compared against Captain John's previously successful controlled payment evidence;
- rollback is one action and documented;
- cache is cleared and anonymous rendering is compared;
- the old snippet is deactivated only after equivalence is proven.

## Standards Proposed for The Book

### ES-015 — Snippet admission

Every runtime snippet must state purpose, owner, scope, dependencies, rollback method and verification method. Temporary snippets must carry an expiry or removal trigger.

### ES-016 — Public UX preservation

No customer-facing snippet may be deactivated during consolidation until its replacement has passed functional and visual equivalence checks.

### ES-017 — Presentation ownership

Shared public styling belongs in Astra Custom CSS. PHP snippets may emit semantic classes but should not establish a parallel design system.

### ES-018 — One behavior, one owner

A runtime responsibility must have one canonical implementation. Copies may exist only as inactive, clearly labeled recovery artifacts for a limited period.

## Files / Database Content Changed

- WordPress Code Snippets record **ID 43**: status changed from active to inactive.
- No snippet code was edited.
- No snippet was deleted.
- No CSS, theme file, plugin file, page content, product, affiliate identifier, Pixel configuration or checkout setting was changed.

## Verification Status

- **Inventory:** VERIFIED — 49 records classified.
- **Active code inspection:** VERIFIED — all 26 originally active snippets reviewed.
- **Safe immediate intervention:** VERIFIED — ID 43 inactive and reversible.
- **Public UX preservation:** VERIFIED for homepage, Loja, cart and Biblioteca smoke checks.
- **Full visual equivalence across devices/products/checkout:** NOT YET PROVEN; required before runtime consolidation.
- **Future deletion of inactive duplicates:** NOT AUTHORIZED and not performed.

## Final Status

**XO-008: PARTIALLY VERIFIED.** Governance and the safe administrative cleanup are complete. The public runtime remains intentionally unchanged. Consolidation is ready to proceed as a separate staged engineering mission with visual regression and rollback gates.
