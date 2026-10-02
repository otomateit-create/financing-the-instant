# Refonte du deck « Financing the Instant » : propositions page par page

*Site relu : instanty.vercel.app, le 22 septembre 2026. Les textes proposés sont en anglais, la langue du deck ; les justifications sont en français. Les chiffres sont vérifiés au 22 septembre 2026, et les sources sont listées en fin de document.*

---

## Le fil directeur

Le deck actuel s'ouvre sur les coûts de la NSCC (4 000 Md$ par jour, 33,5 Md$ de collatéral, 250 k$ de dépôt). Il consacre ensuite trois pages aux questions « data » du cours. Un investisseur retient donc « moins cher que la NSCC », et la conclusion doit ensuite expliquer que ce n'est pas le cas.

La refonte inverse l'ordre :

1. Le marché veut trader à toute heure.
2. La blockchain le permet.
3. Mais elle exige de payer 100 % comptant, à la seconde où l'on achète.
4. Nous finançons cette seconde.

Le coût n'apparaît plus qu'à un seul endroit : ce que le broker paie avec nous, comparé au cash qu'il devrait sinon immobiliser.

Trois faits récents rendent cette histoire plus solide qu'il y a un mois :

- **Le marché classique s'étire, mais sans combler le trou.** La NSCC compense 24 h sur 24 en semaine depuis le 29 juin 2026, et Nasdaq passe à 23 h sur 24 le 6 décembre 2026. Pourtant, rien ne bouge le week-end, le règlement reste à T+1, et Fedwire (le circuit des dollars) ne fonctionne pas le week-end : il n'ouvrira le dimanche qu'en 2028-2029.
- **La SEC a ouvert la porte, et fermé celle du financement.** Depuis le 17 septembre 2026, une exemption de cinq ans autorise les actions américaines tokenisées à s'échanger dans des pools on-chain. Mais elle interdit aux plateformes de financer les achats : le financement doit venir d'ailleurs.
- **La demande on-chain existe.** On compte 3,77 millions de détenteurs d'actions tokenisées, soit +78 % en 30 jours.

## La nouvelle structure

| # | Nouvelle page | Remplace | Idée à retenir |
|---|---|---|---|
| 1 | Context | Section 1 (Context) | Le marché veut rester ouvert en permanence, ses infrastructures ne le peuvent pas |
| 2 | Why on-chain | Haut de la section 2 + Question I (partie 2) | Ce que la blockchain apporte, et son défaut : payer 100 % comptant à la seconde |
| 3 | Our protocol | Bas de la section 2 | La transaction atomique, et ce que le broker y gagne |
| 4 | How it works | Section 3 (schéma) | D'où vient la liquidité, et qui gagne quoi |
| 5 | Business model | Question I, supprimée | Le broker paie des heures d'emprunt, pas une réserve de cash |
| 6 | Risks | Questions II et III | L'atomicité, plus quatre flux de données, dont le risque du week-end |
| 7 | Conclusion | Conclusion | On ne concurrence pas la NSCC sur le prix : on rend finançable le marché qui ne ferme jamais |

**Navigation proposée :** Context · Why on-chain · Our protocol · How it works · Business model · Risks · Conclusion

---

## Page 1 — Context

### 1.1 · Titre

> **Actuel**
> $4 trillion of US stock trades settle every day through one clearing house, one day after the trade.

> **Proposé**
> US stocks are learning to trade around the clock. *Their settlement still takes a day, and stops for the weekend.*

**Pourquoi.** Le titre actuel fait de la NSCC la référence, par sa taille et donc par son coût. C'est la comparaison qu'on ne veut pas mener. Le nouveau titre désigne le vrai trou : le temps. Il reste vrai après le passage de Nasdaq à 23 h sur 24.

### 1.2 · Les quatre chiffres

> **Actuel**
> - **$4.0 tn** · cleared by the NSCC every single day · 386 m trade sides · Q1 2026
> - **T+1** · settlement cycle in the US since 28 May 2024 · EU, UK, CH follow 11 Oct 2027
> - **$33.5 bn** · collateral demanded in one morning · 28 Jan 2021 · $16.2 bn normally
> - **$250 k** · minimum deposit before your first trade · plus membership, capital, US domicile

> **Proposé**
> - **32.5 h → 115 h** · Nasdaq's trading week, out of 168 hours · 23 hours a day, 5 days a week, from 6 Dec 2026
> - **53 h** · still dark every week · no trading from Friday 20:00 to Sunday 21:00 ET, plus daily one-hour pauses
> - **T+1** · even a trade at 3 a.m. settles a business day later · and the dollars move on Fedwire, weekdays only until 2028–29
> - **3.77 m** · holders of tokenised stocks, +78 % in 30 days · rwa.xyz, 22 Sep 2026 · $3.15 bn held on-chain

**Pourquoi.** Les quatre chiffres actuels parlent de coût (4 000 Md$, 33,5 Md$) et d'accès (250 k$), deux angles abandonnés. Les nouveaux racontent l'histoire en quatre temps :

1. la demande de trading permanent, puisque Nasdaq lui-même s'y met ;
2. le trou qui reste ;
3. la lenteur du règlement ;
4. la demande on-chain.

**Calculs :**

- 32,5 h = 6,5 h × 5 jours.
- 115 h = de dimanche 21 h à vendredi 20 h, soit 119 h, moins quatre pauses d'une heure.
- 53 h = 168 − 115.

Le chiffre de 4 000 Md$ reste en conclusion, où il sert à dire « ce n'est pas notre marché ».

### 1.3 · Bloc 1

> **Actuel**
> **The cost is not the fee, it is the overnight call**
> - Clearing fees are trivial: about half a cent on a $10,000 trade. The binding constraint is collateral, recalculated every night.
> - Margin scales with volatility: $2.80 held per $100 of net position becomes $18.60 when volatility jumps. In cash, before the open.
> - 28 Jan 2021: the call on Robinhood went from $0.7 bn to $3.7 bn overnight; it restricted trading and raised $3.4 bn in four days.

> **Proposé**
> **Clients trade when news breaks, not when the market opens**
> - The incumbents are stretching their clocks: the NSCC clears 24 hours a day on weekdays since 29 Jun 2026, and Nasdaq trades 23 hours a day from 6 Dec 2026.
> - They stretch; they don't change. Every trade still settles a business day later, and nothing moves on Saturday or Sunday. Even Nasdaq's tokenised shares, approved by the SEC on 18 Mar 2026, keep T+1.
> - A public blockchain has no closing time: trades settle in seconds, 24/7/365, and the share can be reused the moment it lands.

**Pourquoi.** Ce bloc portait toute la thèse du coût : frais, marge, appel de marge sur Robinhood. On le remplace par la thèse du temps, appuyée sur des faits de 2026. Les acteurs historiques allongent eux-mêmes leurs horaires, ce qui prouve la demande, mais ils ne peuvent pas aller jusqu'au bout.

La phrase sur Nasdaq désamorce l'objection « la tokenisation se fera sans vous ». Tokeniser une action n'accélère rien si le règlement reste celui de la DTC : la SEC a précisé que les délais de règlement restaient inchangés.

L'épisode Robinhood de 2021 peut rester à l'oral, en réponse à une question.

### 1.4 · Bloc 2 « Why now »

On garde le titre et le troisième paragraphe (stablecoins, repo tokenisé). On modifie les deux premiers.

> **Actuel**
> DTCC ran real tokenised stock trades on 15 Jul 2026 with 30+ firms; public launch Oct 2026. SEC cleared Nasdaq to trade tokenised shares (Mar 2026).

> **Proposé**
> DTCC ran real tokenised stock trades on 15 Jul 2026 with 30+ firms; public launch Oct 2026. And on 17 Sep 2026, the SEC let tokenised US stocks trade in on-chain liquidity pools for five years.

**Pourquoi.** L'exemption de la SEC est le fait « why now » le plus fort, et il date de cinq jours. La mention de Nasdaq passe au bloc 1, où elle sert l'argument.

> **Actuel**
> Demand is already proven: $10 bn+ traded in tokenised stocks before Kraken acquired Backed (Dec 2025); Ondo Stocks above $1 bn.

> **Proposé**
> Demand is already on-chain: 3.77 m holders and $3.15 bn of tokenised stocks (rwa.xyz, 22 Sep 2026); Robinhood has sold 24/7 stock tokens in 120+ countries since 1 Jul 2026.

**Pourquoi.** Ces chiffres sont plus récents et mesurent l'adoption (le nombre de détenteurs) plutôt qu'un volume cumulé passé. Ils répondent directement à la question « les clients retail en veulent-ils ? », puisque notre client est le broker retail.

### 1.5 · Phrase de chute

> **Actuel**
> The opportunity is not cheaper settlement: it is the clients, hours and assets this system cannot serve.

> **Proposé** : garder telle quelle.

**Pourquoi.** C'est exactement la nouvelle thèse, et elle arrive au bon endroit.

### 1.6 · Sources de la page

> **Actuel**
> Sources: NSCC CPMI-IOSCO disclosure Q1 2026; NSCC fee guide 2026; testimony of V. Tenev (18 Feb 2021) and M. Bodson (6 May 2021), House Financial Services Committee; NSCC minimum deposit per SEC rule filing, Federal Register 14 May 2021 (re-verify); SEC Release 34-105047 (18 Mar 2026); DTCC 15 Jul 2026; Kraken Dec 2025; Ondo Jul 2026; DefiLlama 8 Sep 2026; Broadridge 7 Jul 2026.

> **Proposé**
> Sources: SEC approval of Nasdaq extended hours (2026) and Nasdaq launch notice; DTCC, NSCC 24x5 clearing live (29 Jun 2026); Federal Reserve, Fedwire operating days (9 Oct 2025); SEC Release 34-105047 (18 Mar 2026); DTCC 15 Jul 2026; SEC innovation exemption (17 Sep 2026); Robinhood (1 Jul 2026); rwa.xyz (22 Sep 2026); DefiLlama 8 Sep 2026; Broadridge 7 Jul 2026.

**Pourquoi.** « (re-verify) » est une note interne visible par le public. Les sources doivent suivre les nouveaux chiffres.

---

## Page 2 — Why on-chain (nouvelle page)

Elle remplace le haut de l'actuelle section 2 et la partie 2 de la Question I.

### 2.1 · Titre

> **Actuel** (titre de la section 2, déplacé en page 3)
> No clearing house means no credit: every trade must be paid in full, instantly. *We finance that instant.*

> **Proposé**
> On-chain, a share trades at any hour, settles in seconds and works as collateral at once. *The catch: it must be paid in full, the second it is bought.*

**Pourquoi.** On sépare « pourquoi aller on-chain » (page 2) de « comment on lève l'obstacle » (page 3). Aujourd'hui, les avantages du on-chain tiennent en trois puces, sous un titre qui parle déjà de crédit. Ils sont pourtant le cœur de la nouvelle thèse.

### 2.2 · Les avantages

> **Actuel**
> **Why brokers move on-chain**
> - Revenue, not cost: 24/7 trading, fractional shares, and clients the US system will never onboard.
> - Tokenised securities become usable as collateral instantly, anywhere, without a custody chain.
> - The demand is already there, the products exist, the settlement rail is what is missing.

> **Proposé**
> **Why brokers move on-chain** · *four reasons, none of them cost*
> - **Open when clients are.** 24/7/365, weekends included: the 53 hours Nasdaq will still be dark.
> - **Settled at execution.** Delivery and payment in the same second: no day of exposure to the other side.
> - **Reusable at once.** The share just bought can be pledged in the same second. DTCC's own pilot is built for "real-time collateral mobility".
> - **Global by default.** Clients fund in stablecoins from anywhere; Robinhood already sells stock tokens in 120+ countries.

**Pourquoi.** Chaque avantage est distinct et vérifiable.

- **« Fractional shares » est retiré** : Robinhood ou Schwab proposent déjà des fractions d'actions sans blockchain, et un investisseur le relèvera.
- **« Revenue, not cost » devient le sous-titre**, parce que c'est l'idée qui porte la thèse.
- **La troisième puce actuelle** (« the settlement rail is what is missing ») est reprise en 2.3, de façon plus précise.

### 2.3 · L'obstacle (nouveau bloc, repris de la Question I)

> **Actuel** (Question I, partie 2)
> **And blockchain cannot inherit the fix**
> - As we said: no company stands in the middle of a public chain, so no one can vouch for a stranger's ability to pay.
> - The safety net disappears with the middleman: the buyer must pay in full, at execution.
> - That is the constraint our protocol exists to answer.

> **Proposé**
> **The catch**
> - No clearing house stands in the middle of a public chain: no netting, no credit. Every client purchase must be paid 100 %, at execution, in dollars already on-chain.
> - For a broker, that means parking a stablecoin float sized to its busiest weekend, on its own balance sheet, or turning the order away.
> - The NSCC nets 98.6 % of what it clears (DTCC, Q3 2026). On-chain, a broker funds every dollar: about 70 times more for the same trades.

**Pourquoi.** C'est le meilleur passage de la Question I : il explique pourquoi le on-chain n'est pas encore adopté malgré ses avantages. On le déplace là où il sert, juste avant la solution.

- La deuxième puce traduit le problème dans la langue du client, c'est-à-dire du trésorier du broker.
- La troisième le chiffre : 1 ÷ (1 − 0,986) ≈ 71. C'est une moyenne sur tout le marché ; pour un broker donné, l'écart peut être plus grand ou plus petit.

### 2.4 · Les deux chiffres de marché

> **Actuel**
> - **$12.85 bn** · traded every month in tokenised stocks, today · rwa.xyz, 14 Sep 2026 · monthly volume up 33× in eight months
> - **$2.6–3.6 tn** · Citi's 2030 forecast for tokenised equities alone · McKinsey forecasts under $2 tn for all tokenised assets; the spread between them is the honest answer

> **Proposé** : les déplacer en page 5 (business model). Le premier chiffre y est remplacé par le stock détenu on-chain (3,15 Md$).

**Pourquoi.**

- **« Traded » est inexact.** Rwa.xyz mesure un volume de *transferts*, pas d'échanges.
- **Le chiffre est très volatil** : 12,67 Md$ au 22 septembre, soit −77 % sur 30 jours.
- **Le « 33× en huit mois » n'est plus défendable** après la chute du dernier mois.

Le stock détenu, lui, est stable et en hausse (+19 % sur 30 jours).

---

## Page 3 — Our protocol

### 3.1 · Titre

> **Proposé** : reprendre tel quel l'actuel titre de la section 2.
> No clearing house means no credit: every trade must be paid in full, instantly. *We finance that instant.*

**Pourquoi.** Il répond maintenant mot pour mot à « The catch » de la page 2. C'est le meilleur titre du deck.

### 3.2 · Les quatre étapes

On garde les quatre étapes et la phrase « All four steps commit together or none of them happened. », puis on ajoute une ligne :

> **Proposé** (ajout sous le schéma)
> Then, outside the transaction: the broker repays the secured loan when its client's cash lands — Monday morning for a Saturday trade.

**Pourquoi.** Le deck ne dit nulle part comment le prêt garanti se termine. C'est pourtant la première question d'un investisseur : qui rembourse, et quand ? La réponse montre en plus la valeur du protocole : il fait le pont entre une blockchain ouverte le week-end et des virements bancaires qui ne le sont pas.

### 3.3 · Nouveau bloc « What the broker gets »

> **Proposé**
> **What the broker gets**
> - No stablecoin float: its capital stays in the business.
> - It pays for the hours it uses the money, not for a float held all year.
> - It says yes to every weekend order, whatever the size of the rush.

**Pourquoi.** Il faut traduire le mécanisme en bénéfices pour le client choisi, le broker retail. Sans ce bloc, la page décrit une technique sans dire ce qu'elle rapporte.

---

## Page 4 — How it works (le schéma)

### 4.1 · Étiquettes du schéma

> **Actuel**
> LENDERS · worldwide, idle capital
> CURATED POOLS · curators set the limits
> OUR PROTOCOL · advances 100 % of the price, then redistributes
> THE BROKER · settles atomically

> **Proposé**
> LENDERS · vetted, worldwide
> CURATED POOLS · curators set the rules: which tokens, what haircut, weekend limits
> OUR PROTOCOL · advances 100 % of the price, for one transaction
> THE BROKER · settles 24/7, repays when client cash lands

**Pourquoi.**

- **« Worldwide, idle capital » évoque de l'argent anonyme.** Un broker régulé ne peut pas emprunter à des inconnus (règles anti-blanchiment), et la SEC exige des participants autorisés (*permissioned*) sur les plateformes d'actions tokenisées.
- **« Then redistributes » est flou.**
- **Les règles des curateurs deviennent concrètes**, et le week-end apparaît, parce que c'est là que se concentre le risque (page 6).

### 4.2 · Légende

> **Actuel**
> Capital from anywhere, risk curated by professionals.

> **Proposé**
> Capital from vetted lenders, risk priced by curators, *used by brokers only for the hours they need it.*

**Pourquoi.** La fin de phrase ramène à la thèse : le broker paie des heures, pas une réserve.

### 4.3 · Ajout « Who earns what »

> **Proposé**
> Lenders earn the interest · curators earn a performance fee · we take a fee on every advance.

**Pourquoi.** Un investisseur doit voir d'où vient notre revenu avant la page business model.

---

## Page 5 — Business model (nouvelle page, remplace la Question I)

> **Actuel** (toute la Question I)
> Titre : The data isn't corrupted, it's just not settled yet. *People pay for that one-day gap.*
> Blocs : « Who pays for the gap » · « And blockchain cannot inherit the fix »
> Chiffres : $16.2 bn immobilised at the clearing house at all times · 95 % of that collateral is held in cash · 3 of 149 foreign firms among NSCC participants
> Chute : The record isn't wrong. It is simply unfinished for a full day, and someone has to be paid to carry that day.

> **Proposé**
> **Brokers pay for the hours they use, *not for a float they hold all year.***
>
> **How we earn.** A fee on every advance, and a share of the interest on the secured loan. Curators earn a performance fee; lenders keep the rest.
>
> **One weekend, one broker** *(illustrative)*. Clients buy $20 m of tokenised stocks between Friday night and Sunday. Without us, the broker parks $20 m of its own money on-chain before Friday. With us, it borrows $20 m for about 48 hours: about $6,600 of interest at 6 % a year, repaid on Monday from client cash.
>
> **How it scales.** Every $1 bn of weekend purchases financed for 48 hours at 6 % pays $329 k of interest. At a 10 % take rate: $33 k per weekend, $1.7 m a year.
>
> Chiffres :
> - **$3.15 bn** · tokenised stocks held on-chain · rwa.xyz, 22 Sep 2026 · +19 % in 30 days
> - **$2.6–3.6 tn** · Citi's 2030 forecast for tokenised equities alone · McKinsey: under $2 tn for all tokenised assets
> - **0.25–2.5 %** · the most of a stock's volume one venue may trade under the SEC exemption · Tier 1 / Tier 2 stocks, for five years

**Pourquoi.**

- **La Question I était entièrement bâtie sur le coût** (« people pay for that one-day gap », 16,2 Md$ immobilisés, 95 % en cash) **et sur l'accès des brokers étrangers**, deux angles abandonnés. Son passage « blockchain cannot inherit the fix » est repris en page 2.
- **Un deck pour investisseurs doit dire comment on gagne de l'argent**, et le deck actuel ne le dit nulle part.
- **Le seul coût qui reste est celui du client** : ce que le broker paie avec nous, comparé au cash qu'il devrait immobiliser.
- **Le plafond de volume de la SEC est un point honnête** : pendant cinq ans, la réglementation limite le marché accessible. Mieux vaut le dire avant qu'on nous le demande.

**Calculs :**

- 20 M$ × 6 % × 48/8 760 = 6 575 $.
- 1 Md$ × 6 % × 48/8 760 = 328 767 $ ; × 10 % = 32 877 $ ; × 52 semaines = 1,71 M$.

Les hypothèses (20 M$, 6 %, 48 h, 10 %) sont à valider en groupe.

---

## Page 6 — Risks (remplace les Questions II et III)

### 6.1 · Titre

> **Actuel** (Question II)
> We advance a stranger the full purchase price. The incentive to disappear is real, *so we remove the opportunity, not the motive.*
>
> **Actuel** (Question III)
> Entirely. NSCC asks you to trust one company. We ask you to trust four data feeds. *That is the whole trade, and it cuts both ways.*

> **Proposé**
> We lend a stranger the full price for one transaction. *Atomicity makes that safe; four data feeds must stay true for the rest.*

**Pourquoi.** On fusionne deux pages en une. Le professeur a proposé ces questions comme une simple piste, et dans un projet financier la « donnée » n'est pas le sujet. Un investisseur attend en revanche une page de risques. On garde le meilleur des deux pages : l'atomicité et les quatre flux de données.

### 6.2 · Les quatre tentations

On garde les quatre tentations et le bloc « One move, not four » tels quels. On condense les paragraphes qui suivent.

> **Actuel**
> The atomic construction removes the risk of the settlement instant. What survives the transaction is an ordinary secured loan.
> For the seconds of the advance we lend to a stranger with nothing held against it, and it is still safe. Not because we trust them, but because the alternative cannot execute.
> Trust does not vanish. Someone still sets the lending limits, something still has to price the collateral, and the hours that follow the trade are a secured loan. That residual window is exactly what curators are paid to price. We removed trust from the one place that used to cost billions, not from everywhere.

> **Proposé**
> The atomic construction removes the risk of the settlement instant. What survives the transaction is an ordinary secured loan, and pricing that loan is exactly what curators are paid for.

**Pourquoi.** Trois paragraphes disent la même chose. Une page de risques doit se lire en trente secondes.

### 6.3 · Flux « The Token »

> **Actuel**
> BREAKS IF it's a synthetic wrapper with no rights (STA flagged ~$2 bn of such tokens to the SEC, July 2026). Then our collateral is worthless: Danielle's step 4.
> SAFEGUARD accept only onshore, transfer-agent-backed tokens.

> **Proposé**
> BREAKS IF the token is a synthetic wrapper with no shareholder rights, like most of the ~$2 bn in circulation (transfer agents' letter to the SEC, 13 Jul 2026). Then our collateral is worthless: temptation 4.
> SAFEGUARD accept only issuer-sponsored or rights-parity tokens: the only kind the SEC exemption covers.

**Pourquoi.**

- **« Danielle's step 4 » est une référence interne** (un prénom), incompréhensible pour le public.
- **La mesure de protection gagne en force** grâce à l'exemption de la SEC, qui exclut les jetons synthétiques.
- **Point à assumer à l'oral** : les jetons de Robinhood sont des titres de dette sans droits d'actionnaire, donc exclus des garanties que nous acceptons.

### 6.4 · Flux « The Price »

> **Actuel**
> BREAKS IF the feed is manipulated. Flash loans are the number one tool for oracle attacks: Euler $197 m (2023), Balancer $116 m (Nov 2025, after 10+ audits); about 20 % of all value stolen in DeFi.
> SAFEGUARD multi-source oracles (DTCC chose Chainlink for its own collateral chain, May 2026), conservative haircuts, time-weighted prices.

> **Proposé**
> BREAKS IF the price is stale or manipulated. The weekend is the hard case: no reference market for 53 hours, and thin on-chain liquidity (four leading stock-token pools held $6.07 m on Sunday 30 Aug 2026).
> SAFEGUARD weekend haircuts and lending caps set by curators, multi-source oracles, time-weighted prices.

**Pourquoi.** Il y a d'abord une erreur de fond à corriger :

- **Euler et Balancer ne sont pas des attaques d'oracle.** Euler a exploité une faille de logique dans le prêt. Balancer a exploité une erreur d'arrondi, et la perte est de 128 M$ selon Check Point, pas 116 M$. Dans les deux cas, les flash loans ont amplifié la faille. Un expert relèvera l'erreur.
- **Le « 20 % » n'a pas de source.**

Surtout, notre thèse du 24/7 crée un risque propre que le deck ne traite pas : le prix du week-end, quand la bourse de référence est fermée. Mieux vaut le nommer nous-mêmes.

La mention Chainlink/DTCC (mai 2026) est à vérifier avant de la garder.

### 6.5 · Les trois chiffres « The paradox, in numbers »

On garde 98.6 % et $500 bn. On remplace le troisième.

> **Actuel**
> **~20 %** · of DeFi losses come from flash-loan-enabled attacks · the tool we use is the tool used against data

> **Proposé**
> **$128 m** · drained from Balancer in under 30 minutes (3 Nov 2025): a rounding error, amplified by flash loans · its token holders vote on a wind-down this month

**Pourquoi.** Un fait sourcé et récent remplace un chiffre sans source, et le message reste le même : l'outil que nous utilisons amplifie les failles.

### 6.6 · Nouvel encadré : la grille du cours en trois lignes

> **Proposé**
> **The course's viability test, in three lines**
> - *Is the data corrupted?* No: the ledger is public and final. What can be wrong is what a token represents (see The Token).
> - *Do outsiders have an incentive to corrupt it?* Yes, at every step. Atomicity removes the opportunity, not the motive.
> - *How much do we depend on trusted data?* Entirely: on four feeds, each with a named safeguard.

**Pourquoi.** On montre au professeur qu'on a appliqué sa grille, en trois lignes au lieu de trois pages.

### 6.7 · Phrase de chute

> **Actuel**
> Trust doesn't disappear on a blockchain. It moves from one institution you cannot audit to four data feeds you can. Our business is not a lending business; it is a data-verification business that happens to lend.

> **Proposé**
> Trust doesn't disappear on a blockchain. It moves from one institution you cannot audit to four data feeds you can. We lend to make on-chain settlement usable; getting those four feeds right is how we stay in business.

**Pourquoi.** « A data-verification business » contredit le positionnement choisi (rendre le on-chain viable pour les brokers) et brouille le message pour un investisseur. On garde les deux premières phrases, qui sont bonnes.

La phrase « One feed being wrong for twelve seconds… » peut rester.

---

## Page 7 — Conclusion

### 7.1 · Titre

> **Actuel**
> The data isn't corrupted, the incentive to corrupt it is real, and we depend on it completely. *So the product only works where the clearing house doesn't.*

> **Proposé**
> We don't compete with the clearing house on price. *We make the market that never closes possible to fund.*

**Pourquoi.** L'ancien titre résumait les trois questions « data », qui ne structurent plus le deck. Le nouveau reprend la thèse en une phrase et répond d'avance à l'objection « vous êtes plus chers que la NSCC ».

### 7.2 · Bloc 1

> **Actuel**
> **What the three questions told us**
> - Q1: The record is right, it's just a day late. That day costs $10 to 20 bn in locked collateral and, in a crisis, a broker's ability to trade.
> - Q2: A stranger has every reason to run with the money. Atomicity removes the opportunity, not the motive: all steps complete together or none do.
> - Q3: The business is 100 % dependent on four data feeds being trustworthy. It replaces institutional trust with verifiable data, and inherits data's failure modes.

> **Proposé**
> **What we showed**
> - Demand: clients trade outside market hours; incumbents are stretching to 23/5; on-chain already runs 24/7.
> - Barrier: on-chain, every purchase is paid in full the second it happens, which means a float no broker wants to hold.
> - Answer: one atomic transaction advances the price and pledges the share, turning the float into an hourly bill.

**Pourquoi.** On reprend le fil de la présentation (demande, obstacle, solution), et non plus celui de la grille du cours.

### 7.3 · Bloc 2 « Where it works, and where it doesn't »

**Première puce : on garde, en datant la citation.**

> **Actuel**
> … "Faster is not always better" (SIFMA, June 2026) is arithmetic, not lobbying.

> **Proposé**
> … "Faster is not always better" (SIFMA, 22 Jun 2026) is arithmetic, not lobbying.

**Pourquoi.** La citation est exacte (billet de SIFMA sur le règlement atomique) et cet aveu renforce notre crédibilité. Dans le texte d'origine, la phrase vise les market makers, obligés de porter plus de stock : c'est à garder en tête si la question vient.

**Deuxième puce : on la réécrit.**

> **Actuel**
> Works where NSCC is absent. Tokenised stocks ($10 bn+ traded via Backed, $1 bn+ on Ondo), 24/7 and weekend trading, non-US and small brokers who can't meet the $250 k plus capital plus legal bar. There, the alternative isn't netting; it's no market at all.

> **Proposé**
> Works where the NSCC can't reach: the 53 hours a week it is closed, trades that must settle in seconds, shares that must work as collateral at once, clients outside the US. There, the alternative isn't netting; it's no trade at all.

**Pourquoi.** On aligne cette puce sur les quatre avantages de la page 2, et on retire les chiffres Backed et Ondo, remplacés plus haut. Les petits brokers étrangers ne sont plus le client principal.

**Troisième puce (« Works better with a clock ») : on garde.**

**Pourquoi.** C'est la feuille de route, et elle répond à l'objection du « ×70 ».

On garde aussi le graphique « What must be funded per $100 traded » et sa note.

### 7.4 · Les chiffres « The market we're actually in »

On garde « $4 tn / day · cleared by NSCC · not our market ». On remplace les deux autres.

> **Actuel**
> - **~$26 bn** · all tokenised real-world assets today (excl. stablecoins) · our market, small and growing
> - **11 Oct 2027** · Europe moves to T+1 · the day the funding gap becomes a European problem too

> **Proposé**
> - **$3.15 bn** · tokenised stocks on-chain, 3.77 m holders · our starting market (rwa.xyz, 22 Sep 2026)
> - **17 Sep 2026** · the SEC opens on-chain trading of US stocks, and bars the venues from financing it · the funding has to come from outside: that is us

**Pourquoi.**

- **Les 26 Md$ ne mesurent pas notre marché.** Ils couvrent tous les actifs tokenisés (obligations, fonds, immobilier), et le chiffre a vieilli.
- **Le passage de l'Europe à T+1 est un argument de coût**, pas de temps.
- **L'exemption de la SEC est l'argument « why now » le plus fort.** Elle interdit aux plateformes de financer les achats (« may not provide financing or extend credit »), ce qui laisse la place à un financement extérieur. C'est notre lecture du texte : à présenter comme telle à l'oral.

### 7.5 · Phrase finale

> **Actuel**
> We don't replace the clearing house. We finance the trades it was never built to clear.

> **Proposé** : garder telle quelle.

**Pourquoi.** Elle résume déjà la nouvelle thèse.

---

## À valider en groupe avant d'intégrer

1. **Hypothèses du business model** : 20 M$ d'achats sur un week-end, un taux de 6 % par an, une durée de 48 h et un take rate de 10 %. Ce sont des ordres de grandeur illustratifs, pas des données.
2. **Garanties acceptées.** Si l'on n'accepte que des jetons qui donnent des droits d'actionnaire, la plupart des jetons actuels sont exclus (Ondo, xStocks, Robinhood). Le marché éligible démarre alors avec les jetons émis par les sociétés elles-mêmes et ceux du service de la DTC, lancé en octobre 2026. C'est cohérent avec la page Risks, mais cela réduit le marché de départ : à assumer à l'oral.
3. **Prêteurs identifiés (« vetted lenders »)** : c'est un choix de conception, à confirmer.
4. **Lecture de l'exemption SEC.** Les plateformes ne peuvent pas financer les achats ; notre protocole prête au broker, pas au client de la plateforme. C'est une interprétation, pas un avis juridique.
5. **Date de Nasdaq (6 décembre 2026)** : elle dépend encore d'une dernière validation de la SEC. Le 23/5 a été approuvé au deuxième trimestre 2026.
6. **Éléments conservés du site mais non revérifiés ici** : 306 Md$ de stablecoins (DefiLlama), les prévisions Citi et McKinsey, la proposition européenne sur la finalité du règlement (déc. 2025), Chainlink retenu par la DTCC (mai 2026), l'USDC à 0,87 $ (mars 2023).

---

## Sources

- Site revu : [instanty.vercel.app](https://instanty.vercel.app/), lu le 22 sept. 2026
- Horaires de Nasdaq : [Alston & Bird, mai 2026](https://www.alston.com/en/insights/publications/2026/05/looking-ahead-to-nasdaqs-extended-trading-hours) · [Arnold & Porter, avr. 2026](https://www.arnoldporter.com/en/perspectives/advisories/2026/04/sec-approves-nasdaq-proposal-to-expand-trading-hours) · [Bitcoin.com, lancement le 6 déc. 2026](https://news.bitcoin.com/finance/nasdaq-23-hour-trading-december-2026-launch/)
- [DTCC, NSCC 24x5, 29 juin 2026](https://www.dtcc.com/news/2026/june/29/nscc-now-live-with-clearing-hours-extended)
- [Federal Reserve, jours d'ouverture de Fedwire](https://www.frbservices.org/resources/financial-services/wires/expand-operating-days)
- [CoinDesk, SEC et tokenisation Nasdaq, 18 mars 2026](https://www.coindesk.com/policy/2026/03/18/sec-approves-nasdaq-s-move-to-allow-tokenized-securities-trading)
- [DTCC, pilote de tokenisation du 15 juil. 2026](https://www.dtcc.com/press-releases/2026/dtcc-turns-tokenization-into-reality)
- SEC, Innovation Exemption, 17 sept. 2026 : [communiqué](https://www.sec.gov/newsroom/press-releases/2026-90-sec-issues-innovation-exemption-facilitate-trading-tokenized-nms-stock-request-comment) · [Morrison Foerster](https://www.mofo.com/resources/insights/260921-sec-issues-innovation-exemption) · [Sullivan & Cromwell](https://www.sullcrom.com/insights/memo/2026/September/SEC-Issues-Innovation-Exemption-for-Tokenized-Securities) · [Unchained](https://unchainedcrypto.com/sec-grants-five-year-innovation-exemption-for-onchain-trading-of-tokenized-stocks-unchained/)
- [The Block, Robinhood Chain et stock tokens, 1er juil. 2026](https://www.theblock.co/news/business/2026-07-01-robinhood-chain-goes-live-mainnet-alongside-24-7-tokenized-stocks-lighter-perps-planned-crypto-agentic-trading-406918)
- [rwa.xyz, actions tokenisées](https://app.rwa.xyz/stocks), consulté le 22 sept. 2026
- [DTCC, CNS (compensation à 98,6 %)](https://www.dtcc.com/products-and-services/clearing-settlement-services/equities-clearing/cns)
- [CryptoSlate, prix et liquidité le week-end, 30 août 2026](https://cryptoslate.com/coinbase-stock-tokens-stayed-within-0-6-of-friday-prices-through-the-weekend-as-aave-collateral-remained-pending/)
- [crypto.news, RedStone et le trou de prix du week-end, 18 sept. 2026](https://crypto.news/tokenized-stocks-face-24-7-pricing-gap-redstone-coo/)
- [CoinDesk, lettre des agents de transfert à la SEC, 13 juil. 2026](https://www.coindesk.com/policy/2026/07/13/wall-street-transfer-agents-lobby-sec-warning-that-third-party-tokens-pose-risks-to-market-integrity)
- Balancer : [Check Point Research](https://research.checkpoint.com/2025/how-an-attacker-drained-128m-from-balancer-through-rounding-error-exploitation/) · [Tech Times, vote de liquidation, 15 sept. 2026](https://www.techtimes.com/articles/327575/20260915/balancer-shuts-down-bal-holders-vote-sep-25-claim-9m-treasury-forfeit.htm)
- [Chainalysis, Euler Finance](https://www.chainalysis.com/blog/euler-finance-flash-loan-attack/)
- [SIFMA, « Analyzing Atomic Settlement in Equities Markets », 22 juin 2026](https://www.sifma.org/news/blog/the-future-of-markets-analyzing-atomic-settlement-in-equities-markets)
