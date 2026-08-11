# MQ-UX-04 — Evaluation of Zupp1 Top-Level Navigation

**Mission:** Evaluate `Início / Explorar / Aprender / Loja / Sobre / Atendimento`  
**Date:** 11 August 2026  
**Archive status:** Completed — Strategic Assessment  
**Validation status:** Deferred  
**Overall confidence:** Moderate  
**Decision improved:** Select a navigation model that makes sense to first-time visitors while preserving Zupp1’s education-led positioning.

**Closure note:** The strategic assessment produced sufficient value for Zupp1’s present stage. Visitor validation was deliberately deferred because additional evidence would not materially improve an immediate operational decision. The mission may be reactivated when Meta campaigns generate significant traffic, customer behavior can be observed directly, and navigation becomes a measurable business variable rather than a design hypothesis.

## Executive conclusion

**Assessment:** The proposed menu has a reasonable size and represents Zupp1’s major functions, but it is not ready to deploy unchanged. The primary weakness is not the number of items. It is the ambiguous boundary between **Explorar**, **Aprender**, and **Loja**.

**Recommendation:** Preserve Zupp1’s three strategic pathways—discovery, education, and transaction—but give each a destination-specific label. The strongest provisional version is:

> **Início | Inspiração | Guias de compra | Loja | Sobre | Atendimento**

This is a provisional information architecture, not a validated final answer. If “Explorar” contains room-based browsing rather than inspiration, use **Ambientes e ideias**. If “Aprender” includes more than purchase guidance, use **Guias** rather than **Guias de compra**.

**Recommendation:** Keep **Atendimento** only if the destination is a genuine service hub covering FAQs, order help, exchanges, support channels, and pre- and post-purchase assistance. If the page contains only a form, email address, telephone number, or social links, label it **Contato**.

## Evidence

### Clear labels and distinct destinations

Navigation labels need strong “information scent”: visitors should be able to predict what they will find before clicking. Nielsen Norman Group specifically identifies vague verbs such as “Explore” and “Learn” as ineffective navigation-category names because they provide too little differentiation and do not support an informed choice ([Nielsen Norman Group](https://www.nngroup.com/articles/3-ia-mistakes/)).

Categories should also have distinct identities rather than overlap in meaning. Nielsen Norman Group recommends descriptive, relatable labels based on users’ mental models and identifies card sorting and tree testing as appropriate ways to verify category labels ([Nielsen Norman Group](https://www.nngroup.com/articles/category-names-suck/)).

**Assessment:** **Explorar** and **Aprender** both describe activities rather than destinations. A new visitor cannot reliably infer whether product comparisons, room ideas, buying guides, recommendations, or educational articles belong under one or the other. **Loja** then creates a third possible location for products, increasing the chance that the same user goal appears to fit multiple paths.

### Ecommerce navigation

Baymard’s ecommerce testing finds that users rely on navigation to understand the product catalog and begin browsing. On mobile, hiding all product categories behind a generic “Shop” or similar item can make it harder for visitors to understand what the store sells; exposing product categories is particularly important for large or diverse catalogs ([Baymard Institute](https://baymard.com/blog/main-navigation-product-categories)).

The same research also finds that a well-organized “Shop” menu can work for small or homogeneous catalogs. On desktop, nesting categories under “Shop” generally creates less friction than on mobile ([Baymard Institute](https://baymard.com/blog/main-navigation-product-categories)).

Baymard recommends preserving broad, clickable parent categories and using curated intermediary pages to help visitors choose a narrower path. On those pages, subcategory navigation should remain primary rather than being displaced by promotional or auxiliary content ([Baymard Institute](https://baymard.com/blog/ecommerce-navigation-best-practice)).

**Assessment:** **Loja** is acceptable during Zupp1’s early stage if the catalog is small enough to understand within one menu or landing page. It becomes less effective as the catalog expands across many home and lifestyle categories. At that point, the top-level navigation or first mobile-menu level should expose meaningful product categories.

### Educational positioning

Educational positioning can justify a navigation model that differs from a conventional store. Hybrid category pages can combine category explanation, subcategory links, representative imagery, selected products, promotions, and advice. Nielsen Norman Group gives the example of an REI category page that included product subcategories, brands, seasonal information, and buying advice, while still giving shoppers direct routes to product listings ([Nielsen Norman Group](https://www.nngroup.com/articles/category-pages/)).

**Assessment:** Zupp1 should not hide its education layer merely to imitate conventional ecommerce. However, being different does not justify being ambiguous. Education is most useful when its label and placement clearly state what visitors can learn and when it is relevant to a purchase.

**Recommendation:** Treat educational content as a first-class pathway and also integrate it contextually into product and category pages. The menu should not force a false choice between “learning” and “shopping.” A visitor viewing sofas should be able to reach sofa-selection guidance without leaving the product decision context.

## First-time visitor comprehension

| Label | Likely first impression | Assessment | Recommendation |
|---|---|---|---|
| **Início** | Return to the homepage | Clear and familiar | Keep, although the logo should also link home |
| **Explorar** | Browse something, but the object is unknown | Low information scent and overlaps with Aprender/Loja | Replace with **Inspiração**, **Ambientes e ideias**, or another noun phrase matching the actual content |
| **Aprender** | Educational material, but scope and format are unclear | Strategically aligned but too broad | Prefer **Guias**, **Guias de compra**, or a tested destination-specific label |
| **Loja** | Browse products or purchase | Clear at a high level | Keep while the catalog is small; expose product categories as the catalog grows |
| **Sobre** | Company, purpose, or story | Clear and conventional | Keep if philosophy and credibility are important at the top level; otherwise move to footer later |
| **Atendimento** | Obtain help or service from the company | Clear if the destination is a service hub | Keep for comprehensive support; use **Contato** for contact details only |

**Assessment:** A first-time visitor can understand four of the six labels at a high level. The visitor is most likely to hesitate when deciding among **Explorar**, **Aprender**, and **Loja**. This hesitation matters because Meta traffic will arrive without prior knowledge of Zupp1’s internal content model.

## “Atendimento” versus “Contato”

Brazilian ecommerce guidance uses the terms differently in practice. Ecommerce Brasil describes **atendimento** or support as help spanning pre-sale, the sale itself, and post-sale, while **contato** refers to the channels through which communication occurs. The same guidance gives `suporte@` as an example for customers and `contato@` for noncustomers, although it does not prescribe navigation labels ([Ecommerce Brasil](https://www.ecommercebrasil.com.br/artigos/suporte-ne-commerce-como-fazer)).

Google’s Brazilian Merchant Center interface groups a support-site URL, email, telephone, live chat, and chatbot under **Atendimento ao cliente**, reinforcing the term’s broader service meaning ([Google Merchant Center Help](https://support.google.com/merchants/answer/13661344?hl=pt-BR-)).

Nuvemshop instructs merchants to use **Contato** as the menu label when the destination displays the business’s contact information ([Nuvemshop](https://atendimento.nuvemshop.com.br/pt_BR/informacao-de-contato/como-adicionar-um-menu-contato-no-menu-principal-ou-no-rodape-da-loja)).

**Assessment:** In an ongoing customer relationship, **Atendimento** better communicates a promise of assistance and resolution. **Contato** better communicates access to communication details. The distinction depends more on destination scope than on abstract word preference.

**Recommendation:** Use **Atendimento** for Zupp1 because its intended system includes guidance, FAQs, support workflows, and continuing customer assistance. Inside that hub, provide a clearly labeled **Fale conosco** or **Canais de contato** section. This gives the broad service relationship an accurate top-level label without making contact information harder to find.

## Zupp1’s educational model

**Assessment:** Zupp1’s positioning justifies a nontraditional navigation model only where the difference helps visitors make a better decision. The educational philosophy should change the architecture in two ways:

- **Education remains visible:** Buying guides and explanatory content deserve a top-level route rather than being buried in a blog or footer.
- **Education is contextual:** Relevant guidance should also appear inside product, category, comparison, and recommendation journeys.
- **Commerce remains legible:** Visitors with direct purchase intent should not have to pass through educational content before seeing products.
- **Language remains concrete:** Zupp1’s philosophy should be expressed through page content and system coherence, not through vague menu labels.

**Recommendation:** Build three complementary paths:

1. **Inspiration/discovery:** Browse by room, need, problem, or idea.
2. **Understanding:** Consult guides, comparisons, criteria, and explanations.
3. **Transaction:** Browse product categories and products directly.

The paths may cross-link, but their top-level labels and landing-page purposes should remain distinct.

## Recommended provisional model

### Option A: Best fit for the current concept

> **Início | Inspiração | Guias de compra | Loja | Sobre | Atendimento**

Use this if:

- **Inspiração** contains ideas, rooms, styles, projects, or needs.
- **Guias de compra** contains criteria, comparisons, explainers, and decision support.
- **Loja** contains the transactional catalog.

### Option B: If exploration is organized by the home

> **Início | Ambientes e ideias | Guias | Loja | Sobre | Atendimento**

Use this if visitors browse primarily through rooms and use cases.

### Option C: Later-stage catalog navigation

As the catalog grows, replace or expand **Loja** with visible product departments in the menu, particularly on mobile. Keep **Guias** as a separate route, while embedding relevant guides inside each department and product journey.

## Risks

- **Label-content mismatch:** Renaming a destination without narrowing its contents will preserve the ambiguity.
- **Over-separation:** Treating education and commerce as isolated silos may make guidance harder to discover at the moment of decision.
- **Educational detours:** Forcing high-intent shoppers through explanatory pages can add unnecessary steps.
- **Catalog concealment:** A generic **Loja** label may prevent first-time mobile visitors from quickly understanding what Zupp1 sells as the catalog expands.
- **Service overpromise:** **Atendimento** implies assistance. A thin contact page under that label could weaken trust.
- **Desktop-only reasoning:** A six-item horizontal desktop menu does not reveal how the hierarchy will behave in the constrained mobile menu used by much Meta traffic.

## Intelligence gaps

- No direct usability test has yet measured how Brazilian Zupp1 visitors interpret the six proposed labels.
- No verified comparative study was found showing that Brazilian users universally prefer **Atendimento** over **Contato** as a navigation label.
- The exact content boundaries of **Explorar**, **Aprender**, and **Loja** have not been supplied for this mission.
- Zupp1’s current catalog size, category diversity, and expected growth are not defined here.
- The expected mobile navigation design and the proportion of campaign traffic arriving on mobile are not yet part of this assessment.

## Validation plan

**Recommendation:** Before implementation, write a one-sentence destination rule for every label: “This section contains X and does not contain Y.” If the team cannot make **Explorar**, **Aprender**, and **Loja** mutually distinct in that exercise, visitors are unlikely to distinguish them.

Run a lightweight Portuguese tree test with first-time participants. Give them tasks such as:

- “Você quer entender como escolher um sofá que dure. Onde procuraria?”
- “Você quer ver opções de luminárias para comprar agora. Onde clicaria?”
- “Você quer ideias para organizar uma sala pequena. Onde procuraria?”
- “Você já comprou e precisa verificar uma troca. Onde clicaria?”
- “Você só quer encontrar o WhatsApp ou e-mail da empresa. Onde procuraria?”

Measure first-choice success, time to choose, backtracking, and the explanations participants give. Treat misrouting between discovery, education, and store destinations as the primary failure signal.

## Final recommendation

**Recommendation:** Do not deploy the proposed labels unchanged. Preserve the model’s intent, but replace **Explorar** and **Aprender** with labels that name their contents. Retain **Loja** while the catalog remains small, and retain **Atendimento** because Zupp1 intends to provide a continuing help relationship rather than only contact information.

The working navigation should therefore be:

> **Início | Inspiração | Guias de compra | Loja | Sobre | Atendimento**

This recommendation should remain provisional until a small tree test confirms that Brazilian first-time visitors correctly distinguish inspiration, education, shopping, and service.
