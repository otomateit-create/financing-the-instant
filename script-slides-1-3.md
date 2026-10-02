# Script · Slides 1 à 3

## Slide 1 · Context

**Titre + tuiles $4.0 tn et 3.77 m**

$4 trillion of US stocks change hands every day. That is 386 million trade sides, on infrastructure built for a market that opens at 9:30 and closes at 4.

Part of that market is already leaving those hours. 3.77 million people hold tokenised stocks today, up 78 % in a month.

Why? Not because it is cheaper. Four reasons.

**Bloc 1 · Why the market wants on-chain + tuiles 53 h et T+1**

First, hours. Clients trade when news breaks. The NSCC and Nasdaq are stretching their clocks, but they still stop for the weekend: 53 hours a week with no market, and no dollars moving either.

Second, collateral. A share settled on-chain can be pledged the same second, anywhere.

Third, reporting. One ledger everyone reads: reconciliation becomes a lookup.

Fourth, reach. Clients fund in stablecoins from anywhere in the world.

**Bloc 2 · Why now**

And why now. DTCC ran real tokenised trades in July, the SEC opened on-chain trading of US stocks in September, and Robinhood sells stock tokens in over 120 countries.

**Phrase de chute**

So the opportunity is not cheaper settlement. It is the clients, the hours and the uses this system cannot serve.

---

## Slide 2 · The idea

**Titre**

So the market wants to go on-chain. Here is the catch.

**Colonne gauche · The catch, puce 1**

On a public blockchain, nobody stands in the middle. No clearing house, so no netting and no credit. Delivery and payment happen in the same second, or they do not happen at all. That is atomic settlement.

**Tuiles 100 % et ~70×**

What netting does today: the NSCC nets 98.6 % of what it clears. A broker that buys 1,000 shares and sells 990 pays for 10. On-chain, it pays for 1,000. About 70 times more cash for the same trades, as a market average.

**Colonne gauche · The catch, puces 2 et 3**

And the client's cash is not there yet. It still travels on bank rails and lands a business day later. So the broker has two options: park a stablecoin float sized to its busiest day on its own balance sheet, or turn the order away.

**Colonne droite · Our protocol, les quatre étapes**

We finance that instant. One smart contract, one atomic transaction, four steps. A flash loan advances 100 % of the price. The tokenised share is bought and delivered against that cash. The share is pledged as collateral in the same transaction. And a secured loan against that share repays the flash loan. If any step fails, none of them happened.

**Note sous les étapes**

What survives is an ordinary secured loan. It runs for a few hours, at most a day, until the broker repays it from its client's cash.

---

## Slide 3 · How it works

**Eyebrow**

Where does the money come from?

**Schéma · Lenders et Curated pools**

Lenders, anywhere in the world, deposit idle capital into pools. Each pool is run by a professional curator, who sets the rules: which tokens it accepts, at what haircut, up to what limit.

**Schéma · Our protocol et The broker**

The pools do not lend to us. They lend through us: our smart contract is the rail. For one transaction, it routes the full price from the pool to the broker. The broker settles atomically, repays with a fee, and the yield travels back to the lenders.

Three parties, three incomes: lenders earn the interest, curators earn a performance fee, and we take a fee on every advance.

**Titre**

We are not a lender. We are the rail: we route the float for the seconds it is needed, and the curators price the hours that follow.

**Transition**

That is the machine. My colleague will now show you why blockchain is necessary. 
