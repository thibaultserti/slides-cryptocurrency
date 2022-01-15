---
title: Cryptomonnaies
author: Thibault Ayanides
theme: white
highlightTheme: stackoverflow-dark
width: 1920
revealOptions:
  transition: "none"
  slideNumber: true
  width: 1920
  height: 1080
---

<link href="css/style.css" rel="stylesheet"/>

# Blockchain et cryptomonnaies

<br/>
<br/>
<br/>

Thibault Ayanides

---

## Sommaire

<!-- .slide: class="align-left big-slide" -->

### 1. La blockchain

#### 1.1 Blocs, fonctions de hachage, signature

#### 1.2 Arbre de merkle et anatomie des blocs

### 2. Le Bitcoin

#### 2.1 Cryptomonnaies

#### 2.2 Les wallets

#### 2.3 Décentralisation

#### 2.4 Cheminement d'une transaction

#### 2.5 Minage

#### 2.6 Dimensionnement du Bitcoin

#### 2.7 Anonymat

#### 2.8 Critiques

#### 2.9 Limitations du Bitcoin

---

## Sommaire

<!-- .slide: class="align-left big-slide" -->

### 3. Les Altcoins

### 4. Investissements ?

---

# 1. La blockchain

---

## Blockchain

- Technologie de transmission et de stockage et de stockage d'information
- Base de données distribuée ou non
- Registre d'enregistrement
- Incorpore des mécanismes de sécurisation et de protection contre la falsification fondées sur la cryptographie

<!-- .slide: data-background="./img/blockchain.png" data-background-opacity="0.2" -->

---

## Vous avez dit blocs ?

- Composées de plusieurs blocs
- Chaque bloc contient un certain nombre d'enregistrement (transactions, documents, ...)

<img src="img/blocks.png" /><!-- .element: class="fragment" -->

# Mais d'abord un point de cryptographie !

---

## Les fonctions de hachage

On appelle <em>h</em>, fonction de hachage si elle répond aux caractéristiques suivantes :

<ul>
  <li> <em>h(m)</em> se calcule facilement</li> <!-- .element: class="fragment" -->
  <li> pour une valeur <em>d</em> donnée, il est très difficile de trouver <em>m</em> tel que <em>h(m)=d</em> </li> <!-- .element: class="fragment" -->
  <li> on ne peut modifier un message m sans changer son hash </li> <!-- .element: class="fragment" -->
  <li> étant donné <em>m<sub>1</sub></em>, il est très difficile de trouver <em>m<sub>2</sub></em> tel que <em>h(m<sub>1</sub>)= h(m<sub>2</sub>)</em></li> <!-- .element: class="fragment" -->
</ul>

<div class="row">
  <div class="column"><!-- .element: class="fragment" -->
    <img src="img/hash_ex.png" width=600px/>
  </div>
  <div class="column"><!-- .element: class="fragment" -->
    <p>Exemples :</p>
    <ul>
      <li>MD5</li>
      <li>SHA-1</li>
      <li>SHA-2</li>
  </div>
</div>

---

## Les signatures électroniques

<!-- .slide: class="big-slide" -->

<img src="img/sig_ex.png" width=75%/>

---

## Caractéristiques d'une signature numérique

- Identification du propriétaire de la signature
- Garantie de la non altération du document entre la signature et la lecture
  - authentique
  - infalsifiable
  - non réutilisable
  - inaltérable
  - irrévocable

---

## Arbre de Merkle

<!-- .slide: class="big-slide" -->

<img src="img/merkle_tree.png" height=80%/>

---

## Intérêt des arbres de Merkle

<!-- .slide: class="big-slide" -->

<img src="img/merkle_tree2.png" width=60%/>

Permet de vérifier un enregistrement sans tout télécharger.
Sans ça chaque utilisateur de la blockchain devrait la stocker en local !

---

## Anatomie d'un bloc

<!-- .slide: class="big-slide" -->

<img src="img/block_anatomy.png" height=80%/>

---

## Anatomie de la blockchain

<img src="img/blockchain_structure.png" width=80%/>

---

# 2. Le Bitcoin

---

## Cryptomonnaies

- Cryptoactifs, cryptodevises, monnaies numériques, ... (nom sujet à débat)
- Émise de pair à pair sans passer par une banque centrale
- Souvent décentralisée
- Repose sur la cryptographie pour sécuriser les transactions

<br/>
<br/>

Plusieurs objectifs initiaux :

</br>
</br>

<div class="row">
  <div class="column">
    <img src="img/icon1.svg" style="vertical-align: middle" />
    se passer de tiers de confiance
  </div>
  <div class="column">
    <img src="img/icon2.svg"  style="vertical-align: middle"/>
    être rapide et fiable
  </div>
  <div class="column">
    <img src="img/icon3.svg"  style="vertical-align: middle"/>
    éviter l'hyperinflation
  </div>
</div>

---

## Bitcoin

Une cryptomonnaie parmi beaucoup d'autres !

<div class="row">
  <div class="column">
    <ul>
      <li>Une cryptomonnaie</li><!-- .element: class="fragment" -->
      <li>Un protocole</li><!-- .element: class="fragment" -->
      <li>Une blockchain</li><!-- .element: class="fragment" -->
    </ul>
  </div>
  <div class="column">
    <img src="img/btc_logo.png" width=50%>
  </div>
</div>
---

## La naissance du Bitcoin

<div class="row">
  <div class="column">
    <ul>
      <li>v1.0 sort en 2009</li>
      <li>Créé par Satoshi Nakamoto</li>
      <li>Première cryptomonnaie</li>
      <li>Limité à 21 millions de coins</li>
      <li>Minable par preuve de travail (PoW)</li>
    </ul>
  </div>
  <div class="column">
    <img src="img/btc.png" width=50%>
  </div>
</div>
---

## Une transaction Bitcoin

<!-- .slide: class="big-slide" -->

<img src="img/bitcoin_transaction.png" width=60%>

---

## Les wallets

<ul>
  <li>Une identité</li>
  <li>Une clé publique et une clé privée</li>
  <li>Logiciel permettant de gérer sa cryptomonnaie</li>
  <li>Hardware wallet vs Software wallet</li>
</ul>

<br/>

Exemples:

<div class="row">
  <div class="column">
    <img src="img/coinbasewallet_logo.png"/>
  </div>
  <div class="column">
    <img src="img/metamask_logo.png" style="vertical-align: middle"/>
  </div>
  <div class="column">
    <img src="img/maiar_logo.png" style="vertical-align: middle"/>
  </div>
  <div class="column">
    <img src="img/trustwallet_logo.png" style="vertical-align: middle"/>
  </div>
  <div class="column">
    <img src="img/ledger_logo.png" style="vertical-align: middle"/>
  </div>
  <div class="column">
    <img src="img/ledger.jpg" style="vertical-align: middle"/>
  </div>
</div>

---

## Hot wallet vs Cold Wallet

<div class="row">
  <div class="column">
    <img src="img/hot_wallet.png" style="vertical-align: middle"/>

  </div>
  <div class="column">
    <img src="img/cold_wallet.png" style="vertical-align: middle"/>

  </div>
</div>
<div class="row">
  <div class="column">
    <ul>
      <li>Fonds accessibles rapidement</li>
      <li>Connecté à Internet</li>
      <li>Vulnérable au phishing</li>
      <li>Vulnérable à la réglementation</li>
    </ul>
  </div>
  <div class="column">
    <ul>
      <li>Fonds moins accessibles</li>
      <li>Pas connecté à Internet</li>
      <li>Plus sécurisé</li>
      <li>Invulnérable à la réglementation</li>
    </ul>
  </div>
</div>

---

## Une transaction Bitcoin

<!-- .slide: class="big-slide" -->

<img src="img/bitcoin_transaction.png" width=60%>

---

## Modèle centralisé vs modèle décentralisé

<!-- .slide: class="big-slide" -->

<div class="row">
  <div class="column">
    <img src="img/centralized.png" width=60%/>
    <ul>
      <li>Pas de confiance entre les pairs</li>
      <li>Confiance en un tiers</li>
      <li>Point de défaillance</li>
    </ul>
  </div>
  <div class="column">
    <img src="img/decentralized.png" width=60%/>
    <ul>
      <li>Pas de confiance entre les pairs</li>
      <li>Pas de dépendance en un tiers</li>
      <li>Pas de point de défaillance</li>
      <li>Difficulté d'évolution du protocole</li>
    </ul>
  </div>
</div>

---

## Validation d'une transaction

- Vérification de la syntaxe
- Vérification de la taille de la transaction ( < 1MB et > 100B)
- Vérification que input >= output
- Vérification que l’input n’est pas trop petit
- Vérification que les clefs publiques input possèdent bel et bien le bitcoin en question
- Parcours de l’entièreté de la blockchain pour retrouver le bitcoin en question et vérifier s’il appartient bien à la même clef
- La possession des bitcoins se fait à travers l’historique des transactions !

---

## Une transaction Bitcoin

<!-- .slide: class="big-slide" -->

<img src="img/bitcoin_transaction.png" width=60%>

---

## Le minage

<div class="row">
  <div class="column">
    <ul>
      <li>Création d'un bloc à partir des transactions en attente</li>
      <li>Résolution du problème dit de <em>Proof of work</em></li>
      <li>Le premier mineur résolvant le problème l'annonce sur le réseau</li>
      <li>Il créé une transaction spéciale qui le crédite d'un certain nombre de Bitcoin</li>
      <li>Les autres blocs vérifient que le problème est bien résolu</li>
    </ul>
  </div>
  <div class="column">
    <img src="img/mining.png" width=60%>
  </div>
</div>
---

## Le proof of work

<div class="row">
  <div class="column">
    <img src="img/block_anatomy.png" height=100%/>
  </div>
  <div class="column">
    <ul>
      <li>Résoudre un problème de force brute</li>
      <li>Trouver un hash tq <em>h(h(header)) < d</em></li>
      <ul>
        <li><em>h</em> est la fonction de hachage</li>
        <li><em>nonce</em> est un entier sur 4 octet que le mineur peut faire varier</li>
        <li><em>d</em> est la difficulté du minage</li>
      </ul>
    </ul>
  </div>
</div>

---

## Un hardware très spécialisé

<!-- .slide: class="big-slide" -->

<div class="row">
  <div class="column">
    <img src="img/evolution_mining.png" height=90%/>
  </div>
  <div class="column">
    <ul>
      <li>GPU</li>
      <ul>
        <li>permet de paralléliser beaucoup plus les calculs qu'un CPU</li>
      </ul>
      <li>FPGA</li>
      <ul>
        <li>reprogrammable</li>
        <li>plus efficace énergétiquement</li>
        <li>très abordable, utilisé pour le prototypage rapide</li>
      </ul>
      <li>ASIC</li>
      <ul>
        <li>non reprogrammable</li>
        <li>encore plus efficace énergétiquement</li>
        <li>très cher</li>
      </ul>
    </ul>
  </div>
</div>

---

## Une transaction Bitcoin

<!-- .slide: class="big-slide" -->

<img src="img/bitcoin_transaction.png" width=60%>

---

# Pourquoi ce mécanisme sécurise-t-il la blockchain ?

---

## Quelques datas sur le Bitcoin

- La fonction de hachage utilisée est _sha256_
- Actuellement la récompense est de 6.25 BTC par bloc miné (divisé par 2 tous les 4 ans)
- 21 millions de Bitcoin maximum
- 1 bloc contient entre 1000 et 2000 transactions (limité par un taille max de bloc de 1Mo)
- 1 bloc toutes les 10 minutes
- Donc 1 moyenne de 7 transations par seconde
- Difficulté ajustée tous les 2016 blocs(2 semaines environ)
- La blockchain pèse 370 Go (2021), la taille augmente de 1Go tous les 2 mois
- https://www.blockchain.com/explorer
---

## Mécanismes de consensus

Que se passe-t-il si les blocs n'arrivent pas dans le bonne ordre et que la blockchain se "désynchronise" ?

- Le protocole impose de ne conserver que la chaîne qui a demandé le plus de travail
  - celle ci devient la chaine principale
  - les autres sont des _forks_
- On attend un certain nombre de confirmations (généralement 6) pour considérer que la transaction a bien été ajoutée à la chaîne principale

<br>

**Les mécanismes de consensus sont un élément capital pour assurer d'une homogénéité de chaque copié de la blockchain détenue par les nœuds !**

---

Qui pense que le BTC monte sans les particuliers et qu'on est sur deuxième top, hmm pas moi.

## Une transaction Bitcoin

<!-- .slide: class="big-slide" -->

<img src="img/bitcoin_transaction.png" width=60%>

---

## Le bitcoin et l'anonymat

**Le Bitcoin ne permet pas l'anonymat !**

<div class="row">
  <div class="column">
    <ul>
      <li>Adresses IP traçables
      <li>KYC sur les sites permettant d'acheter du BTC
      <li>Anonymat des adresses mais tout au plus pseudonymat des utilisateurs
      <li>Exemple de Silkroad
    </ul>
  </div>
  <div class="column">
    <img src="img/anonymat.png" width=60%>
  </div>
</div>

L'historique de toutes les transactions est dans la blockchain !

---

## Avantages et limites du protocle Bitcoin

<div class="row">
  <div class="column">
    <h3>Avantages</h3>
    <ul>
      <li>Décentralisation</li>
      <li>Traçabilité</li>
      <li>Réapproptiation de la valeur monétaire</li>
      <li>Rapidité (par rapport à un virement)</li>
    </ul>
  </div>
  <div class="column">
    <h3>Inconvénients</h3>
    <ul>
      <li>Scalabilité</li>
      <li>Consommation énergétique du PoW</li>
      <li>Rapidité (par rapport à un paiement VISA)</li>
    </ul>
  </div>
</div>

---

# Critiques

---

## Le Bitcoin est-il une pyramide de Ponzi

---

## Le Bitcoin participe au financement du terrorisme

---

## Proof of Work et énergie

---

## Le Bitcoin est l'aboutissement d'un système ultracapitaliste

---

## Limitations du Bitcoin

---

# 3. Les Altcoins

---

## Des altcoins à foison

---

## Ethereum

---

## Une nouvelle méthode de consensus

---

## Le staking

---

## Les Smart Contracts

---

## De nouveaux usages

---

## La Defi

---

## Les NFT

---

## Les PlayToEarn

---

## Les Stablecoins

---

## Les limites d'Ethereum

---

## Les layers 2

---

## L'apparition de nouvelles blockchains

---

## Quelques projets en vrac

---

# 4. Investissements ?

---

## Les échangeurs centralisés (CEX)

---

## Les échangeurs décentralisés (DEX)

---

## Cyclicité du Bitcoin et des cryptomonnaies

---

## Comment repérer les bons projets ?

---

## Stratégies d'investissements

---

## Random

<!-- .slide: class="big-slide" -->

En vrac tous les trucs dont je veux parler :

- attaque des 51%
- ETH, BSC (etherscan, bscscan)
- les générations de blockchains (présentation de qqs blockchains d'infrastructure)
- eth 2.0
- NFT
- Defi (lending/borrowing, liquidity providing, DEX)
- Proof of Stake, Staking
- les échangeurs (CEX, orders books, ...)
- les stablecoins
- comment se renseigner sur un projet (whitepaper, coinmarketcap, ...)
- les layers 2
- stratégies d'investissements (DCA, support, trading, ...)
- cyclicité du BTC et des cryptomonnaies
- les Play2Earn

---

# Questions ?

---

## Sources, références, pour aller plus loin

- https://github.com/thibaultserti/slides-cryptocurrency
- https://www.coursera.org/learn/cryptocurrency
- https://github.com/bitcoinbook/bitcoinbook
- https://github.com/ethereumbook/ethereumbook
- https://coinmarketcap.com

---

## Mes referals 🤑

<!-- .slide: class="big-slide" -->

- **Swissborg** : https://join.swissborg.com/r/thibauOYKV
- **Nexo** : https://nexo.io/ref/hxkgumrvxz?src=android-link
- **Crypto.com App** : https://crypto.com/app/7p7jkbp5sj
- **Crypto.com Exchange** : https://crypto.com/exch/7p7jkbp5sj
- **Binance** : https://accounts.binance.com/fr/register?ref=81135148
- **FTX** : https://ftx.com/#a=12460172
- **Maiar** : https://get.maiar.com/referral/tp1qokr73z

- **BTC** : bc1qyk62saxsgl5ng2mk54ue6ftgudkjyg0a0x3xrk
- **ETH** : 0xf39b36242bd9E3aa1269C40367369e012936342B
- **BNB** : bnb1w6hgq4tgde0my9nrasexqy2q02maqx9v3q2752
- **EGLD** : erd1xy53cvkp2vajqe6szs3p2xayltvxp6twu8c3rhreu5wczlv6hxwse99w25

(ou simplement @thibaultserti)

## À mentionner

- les oracles
- les blockchains privées (hyperledger, ...)
