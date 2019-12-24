# Rational Exchange

This repository contains all the code used for paper **"Rational Exchange: Incentives in Atomic Cross Chain Swaps"** by *Janick Rueegger* and *Dr. Guilherme Sperb Machado*.

**Please note:** *This paper is currently under review. Hence we cannot currently publish its contents. Thank you for understanding.*

## Abstract

The exchange of digital currencies between distrusting parties across discrete blockchain-technologies bears enormous potential. As a fundamental capability for interoperability, it might play a critical role in the tokenization of commerce. In contrast to traditional financial systems and centralized crypto-exchanges, protocols based on Hash Time Lock Contracts (HTLCs) provide a method to trade crypto-currencies in a peer-to-peer manner, without the mediation of a trusted third- party authority. However, considering the omission of central coordination, remarkable price fluctuations of traded assets and the protocol’s extensive time-to-completion, involved parties might be incentivized to deviate from the protocol. Without the guarantee of a successful exchange, it is required to analyze the protocol’s prevalent incentive-structures. Thus, this paper introduces and tests a model of rationality to further quantify its impact on potential historical trades, using real exchange-rates. Analyzing different crypto-currency trading pairs we highlight the probabilistic nature of a typical HTLC-based protocol. The results show that although the protocol does not offer a guarantee for a successful trade, it is applicable in scenarios of exchange-rates with low drift, low volatility, and optimized time-to-completion.

*Index Terms* — Decentralized Finance, Rational Protocols, Hash Time Lock Contracts, Atomic Cross Chain Swaps, Rational Verification, Game Theory.

## Setup

To run the tests, we advise you to have [anaconda](https://www.anaconda.com/distribution/) installed. Anaconda supports *jupyter notebooks*, which are really handy to not only write and run *python* scripts, but allow you to vizualise its results in your browser of choice.

Additionally, anaconda supports the use of *markdown*, which allows us to not only add additional details to the code, but also to describe the example provided. For more information and a detailled documentation, please head to the [jupyter notebook](https://jupyter.readthedocs.io/en/latest/tryjupyter.html) website.

## Code

In this paper, two *rational verifications* are executed, to achieve the following goals:

1. Describe and test the introduced *model of rationality*
2. Quantify the model of rationality's *impact* on potential *historical trades*

The code therefore had been structured into the following components:

- **Strategic Game** (incl. *backwards induction algorithm*), defining the specific game
- **Geometric Brownian Motion**, defining the functionality for a GBM
- **Game Solver** (incl. *utility function*), needed for finding thee *Nash equilibrium*
- **TestSeries**, defining a single test-series using a number of GBM
- **Rational Verification**, describing the model's behavior in a *Monte Carlo simulation*
- **Historic Price Curve**, describing a historic trajectory using real exchange data
- **Rational Verification Historical Series**, quantify the model's impact on historical trades using real exchange data

## Data

The data used in this paper was provided by [Coinbase Pro API](https://docs.pro.coinbase.com/) and [Poloniex API](https://docs.poloniex.com/#introduction). All data are publicly available and can be downloaded using *public APIs*. We thank both entities for offering these services for free!

Future use of the provided data has to be compliant with the regulations of these entities.

## Issues and Feedback

If you experience problems, find inconsistencies or generelly want to provide us with feedback, please open an [issue](https://github.com/unnmdnwb3/rational-exchange/issues) and describe your experience. Thank you in advance!
