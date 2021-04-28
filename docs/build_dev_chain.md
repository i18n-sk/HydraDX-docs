---
id: build_dev_chain
title: Set up a development chain
---

import useBaseUrl from '@docusaurus/useBaseUrl';

Táto sekcia ťa prevedie procesom nastavenia lokálnej HydraDX chain inštancie pre rozvoj.

:::poznámka
Chceš nastaviť node na účel validácie? Presuň sa prosím na [sprievodcu pre validátorov](/node_setup). 
:::

## 01 Inštalačné závislosti

Na to aby bola lokálna HydraDX chain inštancia pripravená na ďalší development, tvoje zariadenie potrebuje pokryť všetky závislosti pre chod Substrate chainu. Budeš si musieť nainštalovať Rust developer prostredie a uistiť sa, že je nakonfigurované správne na kompilovanie Substrate runtime kódu do WebAssembly (Wasm). 

Všetky závislosti si môžeš nainštalovať manuálne s pomocou tohto [Substrate sprievodcu](https://substrate.dev/docs/en/knowledgebase/getting-started), alebo môžeš všetku prácu nechať na nasledujúci script: 

```bash
$ curl https://getsubstrate.io -sSf | bash -s -- --fast
$ source ~/.cargo/env
```

## 02 Build

Zostav Wasm a natívne prostredia na exekúciu:

```bash
# Načíta zdroj najnovšieho stabilného vydania
$ git clone https://github.com/galacticcouncil/HydraDX-node -b stable

#Vybuduj binárku
$ cd HydraDX-node/
$ cargo build --release
```

Build by si mal nájsť pod `./target/release/hydra-dx`.

## 03 Spustenie

Pred spustením svojho buildu môžeš prečistiť akékoľvek existujúce vývojové chainy na tvojom zariadení (toto budeš musieť v procese developmentu robiť často):

```bash
$ ./target/release/hydra-dx purge-chain --dev
```

Spusti svoj build pomocou jedného z nasledujúcich príkazov:

```bash
$ ./target/release/hydra-dx --dev

#Spusti s podrobným protokolovaním
$ RUST_LOG=debug RUST_BACKTRACE=1 ./target/release/hydra-dx -lruntime=debug --dev
```

## 04 Pripoj sa ku svojej lokálnej chainovej inštancií

Ku svojmu lokálnemu HydraDX vývojovému nodu sa môžeš pripojiť pomocou Polkadot/apps zmenou networku na `Development`. Môžeš však na to použiť aj tento link: https://polkadot.js.org/apps/?rpc=ws%3A%2F%2F127.0.0.1%3A9944#/explorer


<img alt="connect to node" src={useBaseUrl('/building/connect-to-node.jpg')} />
