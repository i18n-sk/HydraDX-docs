---
id: claim
title: Nárokuj si svoje HDX tokeny
---

import useBaseUrl from '@docusaurus/useBaseUrl';

Svoje HDX si môžeš nárokovať pomocou xHDX tokenov (ERC-20), ktoré si získal/a za obdobie, keď bola spustená naša služba [Balancer LBP](https://hydradx.substack.com/p/lbp-announcement).

:::poznámka

Nemáš žiadne xHDX tokeny ale aj napriek tomu by si rád/a získal/a nejaké HDX? Ďakujeme ti za záujem no aktuálne nie je bohužiaľ možné zakúpiť si akékoľvek HDX tokeny - ich transfery sú zmrazené až do spustenia mainnetu. Keď však budeme blízko ku spusteniu mainnetu, spustíme motivačné komunitné programy, ktoré ti môžu priniesť nejaké HDX tokeny o niečo skôr. Ak ťa to zaujalo, [prihlás sa na odber newslettera](https://hydradx.substack.com) a pridaj sa na náš Discord server kde dostaneš všetky updates. 

:::

## Predpoklady {#prequisites}

Na získanie svojich HDX tokenov musíš mať splnené dva predpoklady, jedným je inštalácia [prehliadačového rozšírenia Polkadot.js](https://polkadot.js.org/extension/), ktoré bude použité na vytvorenie tvojej HDX peňaženky. Ako druhé budeš potrebovať prístup ku svojim xHDX tokenom, ktoré by mali byť uložené v peňaženke podporujúcej podpisovanie správ týkajúcich sa ERC-20 tokenov (napr. Matemask).

Ak máš svoje xHDX tokeny uložené v Coinbase peňaženke, budeš potrebovať použiť jedno z nasledujúcich náhradných riešení, aby si mohol/la získať svoje HDX tokeny, keďže táto peňaženka nepodporuje podpisovanie vyššie spomenutých správ:

* Metamask: Môžeš použiť rozšírenie Matemask a importovať svoju peňaženku pomocou seed frázy.

* MEW (MyEtherWallet): Môžeš na to použiť aj MEW, tiež buď importovaním svojej recovery seed frázy (*Mnemonickej frázy*) alebo použitím možnosti pripojenia cez Walletlink. Obidve možnosti môžeš nájsť na [stránke MEW wallet access](https://www.myetherwallet.com/access-my-wallet). Ak používaš Coinbase peňaženku, môžeš použiť Walletlink, ktorý nájdeš v nastaveniach Coinbase peňaženky.  

## Proces nárokovania tokenov {#claim-process}

Po tom čo sa uistíš, že si splnil/a obidva predpoklady opísané vyššie, môžeš ísť do [HydraDX Claim aplikácie](https://claim.hydradx.io) a pokračovať v nárokovacom procese. 

Počas tohto procesu budeš používať xHDX tokeny (ERC-20) na získanie svojich HDX tokenov.

### 00 Autorizácia {#00-authorize}

HydraDX Claim aplikácia bude požadovať autorizáciu od Polkadot.js rozšírenia.

:::pozor

Uisti sa, že si sa nestal/a obeťou phishingového útoku a dávaj si pozor na autorizačné popup okno: Aplikácia by sa mala identifikovať ako **CLAIM.HYDRADX.IO** a žiadosť by mala prísť od **https://claim.hydradx.io**.

:::

<img alt="authorize" src={useBaseUrl('/claim/authorize.jpg')} />

Po autorizácií sa zobrazí výzva na aktualizáciu metadát pre Polkadot.js rozšírenie. Toto dovolí Polkadot.js vytvoriť adresu špecifickú pre HydraDX, ktorá je potrebná na dokončenie nárokovacieho procesu.

<img alt="authorize" src={useBaseUrl('/claim/metadata.jpg')} />

### 01 Vyber svoju ETH adresu {#01-select-your-eth-address}

V prvom kroku nárokovacieho procesu sa zobrazí výzva na výber účtu, na ktorom máš svoje xHDX tokeny. Môžeš to urobiť buď pripojením ku svojej peňaženke, ktorá drží tvoje xHDX tokeny (napr. Matemask) alebo manuálnym zadaním tvojej ETH adresy do input boxu (v tomto prípade budeš musieť neskôr podpísať správy manuálne).

Po zadaní tvojej ETH adresy by si mal vidieť množstvo HDX tokenov, ktoré si môžeš nárokovať obsahujúce aj [náhradu gas fees](https://hydradx.substack.com/p/first-governance-vote), ktoré si utratil/a na získanie xHDX tokenov na Balanceri.

:::poznámka

Na náhradu gas fees nemáš nárok ak si získal/a svoje xHDX tokeny niekde inde než oficálne cez Balancer pool (napríklad na Uniswap) alebo ak si presunul/a svoje tokeny mimo peňaženky, do ktorej si ich originálne kúpil/a.

:::

<img alt="authorize" src={useBaseUrl('/claim/claim-01.jpg')} />

### 02 Vytvor a vyber svoju HDX adresu {#02-create-and-select-an-hdx-address}

V druhom kroku sa zobrazí výzva na výber tvojej HDX adresy.

Na vytvorenie novej HDX adresy otvor rozšírenie Polkadot.js a klikni na '+', aby si vytvoril/a nový účet. V prvom kroku vytvárania nového účtu uvidíš 12-slovnú mnemonickú frázu, ktorá môže byť použitá na obnovu tvojho účtu. Po tom čo si túto frázu uložíš na nejakom bezpečnom mieste môžeš kliknúť na *Next step*. Tu by si mal/a zmeniť **Network** vybratím možnosti **HydraDX Snakenet**. Zadaj meno a heslo pre svoj účet a dokonči jeho kreáciu.

<img alt="authorize" src={useBaseUrl('/claim/create-account.png')} />

:::pozor

Uisti sa, že máš svoju recovery seed frázu zálohovanú na bezpečnom mieste a nikdy ju s nikým nezdieľaj. Použitie tejto frázy je jediný spôsob ako si obnoviť účet a pokiaľ ju stratíš alebo niekomu prezradíš, tvoje prostriedky môžu byť ohrozené. Prosím pamätaj, že prístup ku tvojej peňaženke musí byť zabezpečený až do spustenia mainnetu, keďže všetky bilancie sú aktuálne uzamknuté. Ak stratíš prístup ku svojej HDX peňaženke, stratíš aj všetky svoje HDX tokeny.

:::

Po vytvorení svojho HDX účtu by si mal/a byť schopný/á vybrať si ju v HydraDX Claim aplikácií. Po tom, čo to urobíš, aplikácia by ti mala poskytnúť prehľad ETH a HDX adries použitých v nárokovacom procese. Klikni na *Next* a pokračuj s podpísaním správy.

<img alt="authorize" src={useBaseUrl('/claim/claim-02.jpg')} />

### 03 Podpíš nárokovaciu správu {#03-sign}

V treťom kroku nárokovacieho procesu sa ti v HydraDX Claim aplikácií zobrazí možnosť podpísať správu, ktorá potvrdzuje použitie tvojich xHDX tokenov na získanie HDX tokenov.

:::poznámka

Upozorňujeme, že v tomto kroku uvidíš **public key** svojej HDX adresy, a nie adresu v bežne čitateľnej forme, ktorá bola vystavená v predchádzajúcom kroku a v rozšírení Polkadot.js (pre viac detailov navštív [ss58 docs](https://polkadot.js.org/docs/keyring/start/ss58)). Ak si podnikol/la všetky kroky popísané vyššie, nemusíš sa ničoho obávať a je bezpečné pokračovať v podpisovaní správy. Taktiež overíme, či účet HDX, ktorý používaš na podpísanie nárokovacej transakcie, v poslednom kroku zodpovedá účtu, ktorý prijíma nárokované HDX tokeny.

:::

V závislosti na možnosti, ktorú si si vybral/a v prvom kroku, máš dve možnosti, ako podpísať správu o použití tokenov xHDX v procese nárokovania:

* Ak používaš ** Metamask **, po kliknutí na tlačidlo *Sign* ťa Metamask vyzve na podpísanie správy. Postupuj podľa pokynov v Metamask.

* Ak si zadal/a svoju ETH adresu manuálne, budeš musieť správu podpísať cez externú peňaženku, ktorá obsahuje súkromné kľúče tvojich xHDX tokenov. Po podpísaní správy skopíruj podpis (začínajúci *0x*) do príslušného poľa v aplikácii HydraDX Claim.

<img alt="authorize" src={useBaseUrl('/claim/claim-03.jpg')} />

### 04 Získanie tokenov {#04-claim}

Po podpísaní správy v peňaženke, ktorá obsahuje tvoje xHDX tokeny, by sa malo otvoriť rozšírenie Polkadot.js a zobrazí sa výzva na podpísanie transakcie s cieľom získať nárok na HDX na tvoj účet. Zadaj heslo svojho účtu HDX a klikni na *Sign the transaction*.

<img alt="authorize" src={useBaseUrl('/claim/claim-sign.jpg')} />

Týmto si dokončil/a proces nárokovania tokenov a stal/a ste sa tak oficiálne vlastníkom HDX!

Svoj zostatok môžeš skontrolovať pomocou aplikácie [Polkadot / apps](https://polkadot.js.org/apps/?rpc=wss%3A%2F%2Frpc-01.snakenet.hydradx.io#/accounts) pripojenej k sieti HydraDX Snakenet. Upozorňujeme, že tvoje množstvo HDX tokenov neuvidíš priamo v rozšírení prehliadača Polkadot.js.


### Čo ďalej? {#05-whats-next}

Po dokončení procesu nárokovania zostanú tokeny HDX uzamknuté v peňaženke až do spustenia mainnetu.

Na druhej strane tokeny xHDX (ktoré si použil/a na získanie HDX tokenov) zostanú v tvojej peňaženke ERC-20 uzamknuté navždy, čo znamená, že ich môžeš vo svojej peňaženke skryť (alebo ich ponechať viditeľné ako odznak early-adoptera).

Chceš využiť svoje HDX tokeny a pomôcť zlepšiť zabezpečenie siete HydraDX? Môžeš sa zapojiť do nášho motivačného testnetu s názvom **Snakenet** stakeovaním svojich tokenov. Ak máš záujem, môžeš pokračovať oboznámením sa so [stakingovým procesom](/staking) a potom sa môžeš rozhodnúť či sa staneš [validátorom](/start_validating) alebo [nominátorom](/start_nominating).

