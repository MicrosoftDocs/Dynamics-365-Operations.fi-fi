---
title: Määritä verokoodit
description: Tässä artikkelissa kuvataan, miten verokoodit määritetään Veron laskenta -palvelussa.
author: wangchen
ms.date: 11/30/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable, TaxData
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-10-26
ms.dyn365.ops.version: Version 10.0.21
ms.openlocfilehash: 1bc250716763ce9d8e25c8850c8a3676bf65fb0c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8862925"
---
# <a name="set-up-tax-codes"></a>Määritä verokoodit

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kuvataan, miten verokoodit määritetään Veron laskenta -palvelussa. Se sisältää yksinkertaisen skenaarion määrityksen, joka auttaa verokoodin suorittamisessa, sekä tietoja monimutkaisissa tilanteissa lisäverokooditoiminnosta.

> [!IMPORTANT]
> Verokoodien määrittäminen Veron laskentapalvelussa on yrityksestä riippumaton. Nämä asetukset voi tehdä Regulatory Configuration Service (RCS) -palvelussa vain kerran. Verokoodit synkronoidaan automaattisesti Microsoft Dynamics 365 Financeen, kun otat veronlaskentapalvelun käyttöön valitulle oikeushenkilölle Financessa.

## <a name="simple-setup"></a>Yksinkertaiset asetukset

Noudattamalla näitä ohjeita voit käyttää verokoodia yksinkertaisessa skenaariossa, kuten tilanteessa, jossa veroprosentteja on vain yksi.

1. Kirjaudu [Regulatory Configuration Service](https://marketing.configure.global.dynamics.com/) -palveluun.
2. Siirry kohtaan **Työtilat** \> **Globalisointiominaisuudet** \> **Veronlaskenta**.
3. Valitse määritettävä ominaisuus ja versio ja valitse sitten **Muokkaa**.
4. Valitse **Yleiset**-välilehdestä **Konfiguraatioversio**.
5. Valitse **Verokoodit**-välilehdessä **Lisää** ja kirjoita verokoodi sekä kuvaus.
6. Valitse **Laskennan perusteet**. Laskennan perusteet on ryhmä tapoja, jotka on määritetty valitsemasi verokonfiguraation version mukaan. Valitse tämän yksinkertaisen skenaarion **nettosumman** mukaan.
7. Valitse **Tallenna**. Käytettävissä on lisää kenttiä valitsemasi laskentaperusteen perusteella.
8. Valitse **Verot**-pikavälilehdestä **Lisää**, jos haluat lisätä tälle verokoodille yhden veroprosentin.
9. Valitse **Tallenna**.

## <a name="calculation-origin"></a>Laskelman alkuperä

Laskennan alkuperä määrittää, miten veron peruste ja veron summa lasketaan. Se on määritetty veromäärittelynä kohdassa **Sähköinen raportointi** -työtila. **Laskennan alkuperä** -kentässä ovat käytettävissä seuraavat arvot:

- Nettosumman mukaan
- Bruttosumman mukaan
- Määrän mukaan
- Katteen mukaan
- Veron vero

### <a name="by-net-amount"></a>Nettosumman mukaan

Jos valitset **Laskennan alkuperä** -kentässä **Nettosumman mukaan**, veron summa lasketaan oston tai myyntisumman prosenttiosuutena ilman muita verokoodeja.

Esimerkiksi veroprosentti on 25 prosenttia, laskurivin nimikkeiden määrä on 10 ja kappalehinta 1,00, ja asiakkaalle sallitaan 10 prosentin rivialennus. Tässä tapauksessa poikkeamasummat lasketaan seuraavasti:

- **Nettosumma:** (10 × 1.00) – 10 % = 9,00 
- **Arvonlisävero:** 9,00 × 25 % = 2,25 
- **Laskun kokonaissumma:** = 9,00 + 2,25 = 11,25.

### <a name="by-gross-amount"></a>Bruttosumman mukaan

Jos valitset **Laskenta-alkuperä** -kentässä **Bruttosumman mukaan**, verosumma lasketaan prosentteina myynnin bruttomäärästä. Bruttosumma on rivin nettosumma plus kaikki rivin verot ja maksut paitsi yhtä veroa, jossa **Laskelman alkuperä** -kentän arvoksi on asetettu **Bruttosummalla**.

Esimerkiksi, verottaja on säätänyt tätä kohdetta koskevia erikoismaksuja. Erikoismaksusummat lisätään nettosummaan ennen veron laskemista. Seuraavat verokoodit ovat käytössä:

- **Maksu 1** – Hinta on 10 prosenttia, ja **Nettosumman mukaan** -laskentatapaa käytetään.
- **Maksu 2** – Hinta on 20 prosenttia, ja **Nettosumman mukaan** -laskentatapaa käytetään.
- **Veroprosentti** – Hinta on 25 prosenttia, ja **Bruttosumman mukaan** -laskentatapaa käytetään.

Jos nettosumma on 10,00, Maksu 1 1,00 (10,00 × 10 prosenttia) ja Maksu 2 -summa 2,00 (10,00 × 20 prosenttia). Tässä tapauksessa poikkeamasummat lasketaan seuraavasti: 

- **Bruttosumma:** = Nettosumma + Maksu 1 + Maksu 2 = 10,00 + 1,00 + 2,00 = 13,00 
- **Veron määrä:** 13,00 × 25 % = 3,25 
- **Tullit ja verot yhteensä:** 1,00 + 2,00 + 3,25 = 6,25 
- **Laskun kokonaissumma:** = 10,00 + 6,25 = 16,25.

### <a name="by-quantity"></a>Määrän mukaan

Jos valitset **Määrän mukaan** **Laskennan alkuperä** -kentässä, verosumma lasketaan kiinteänä summana yksikköä kohti ja kerrotaan tositeriville syötetyllä määrällä. Yksikkökohtainen summa määritetään **Hinnat**-pikavälilehdessä.

Verokoodiksi määritetään esimerkiksi 1,20 per yksikkö. Myyntilaskurivillä 25 yksikköä nimikettä on myyty. Tässä tapauksessa verosumma lasketaan 25 x 1,20 = 30,00.

### <a name="by-margin"></a>Katteen mukaan

Jos valitset **Katteen mukaan** -kentässä **Bruttosumman mukaan**, verosumma lasketaan prosentteina myynnin katteesta. Myyntimarginaali on myyntisumma vähennettynä kustannussummalla. Tätä laskentatapaa käytetään vain myyntitapahtumiin.

Esimerkiksi veroprosentti on 25, laskurivillä näkyy 10 kappaleen määrä 10,00 kappale ja hinta per nimike on 6. Tässä tapauksessa poikkeamasummat lasketaan seuraavasti:

- **Myyntikate:** 10 × ( 10,00 – 6,00) = 40,00
- **Veron määrä:** 40,00 × 25 % = 10,00
- **Laskun kokonaissumma:** = 100,00 + 10,00 = 110,00.

### <a name="tax-on-tax"></a>Veron vero

Jos valitset **veron veron** **Laskennan alkuperä** -kentässä, arvonlisävero lasketaan prosenttiosuutena kaikista saman asiakirjarivin muista verosummista.

Esimerkiksi seuraavat verokoodit ovat käytössä:

- **Maksu 1** – Hinta on 10 prosenttia, ja **Nettosumman mukaan** -laskentatapaa käytetään.
- **Maksu 2** – Hinta on 20 prosenttia, ja **Nettosumman mukaan** -laskentatapaa käytetään.
- **Tulovero** – Hinta on 25 prosenttia, ja **Veron vero** -laskentatapaa käytetään.

Tässä tapauksessa poikkeamasummat lasketaan seuraavasti:

- **Nettosumma:** 10,00 
- **Tulli:** 10,00 × 10 prosenttia = 1,00 
- **Tulli:** 10,00 × 20 prosenttia = 2,00 
- **Tulovero:** 3,00 × 25 prosenttia = 0,75
- **Vero yhteensä:** 1,00 + 2,00 + 0,75 = 3,75 
- **Laskun kokonaissumma:** = 10,00 + 3,75 = 13,75.

## <a name="advanced-functionality"></a>Lisätoiminnot

Tässä osassa on tietoja verokoodiasetusten lisätoiminnosta monimutkaisia skenaarioita varten.

### <a name="tax-exemption"></a>Verovapautus

Jos määrität **Verovapaus**-asetuksen arvoksi **Kyllä** **Yleiset**-pikavälilehdessä, veron summa ohitetaan aina nollaksi todellisesta veroprosenttista riippumatta.

Voit määrittää vapautuksen syyn määrittämällä **vapautuskoodin** kentän. 

Voit ottaa perustietojen haun käyttöön **vapautuskoodi**-kentässä. Näin voit valita verovapauskoodiarvoista, jotka on määritetty Financessa. Lisätietoja perustietojen haun käyttöön määrityksestä on kohdassa [Veronlaskennan konfiguraation perustietojen haun ottaminen käyttöön](tax-service-set-up-environment-master-data-lookup.md).

Esimerkiksi veroprosentti on 25 prosenttia ja **On vapautus**-asetuksena on **Kyllä**. Laskurivillä näkyvä nimikemäärä on 10 ja hinta 1,00/nimike, ja asiakkaalle myönnetään 10 %:n rivialennus. Tässä tapauksessa poikkeamasummat lasketaan seuraavasti:

- **Nettosumma:** (10 × 1.00) – 10 % = 9,00 
- **Arvonlisävero:** 0,00 
- **Laskun kokonaissumma:** = 9,00 + 0,00 = 9,00.

### <a name="use-tax"></a>Käyttövero

Jos määrität **Yleiset**-pikavälilehdessä **Käytä veroa** -asetuksen arvoksi **Kyllä**, veron summa kirjataan **Toimittajan yhteenveto** -tilin asemesta **Käyttöveron maksettava** -tilille.

Esimerkiksi veroprosentti on 25 prosenttia ja **On käyttövero**-asetuksena on **Kyllä**. Laskurivillä näkyvä nimikemäärä on 10 ja hinta 1,00/nimike, ja asiakkaalle myönnetään 10 %:n rivialennus. Tässä tapauksessa poikkeamasummat lasketaan seuraavasti:

- **Nettosumma:** (10 × 1.00) – 10 % = 9,00 
- **Käyttövero:** 9,00 × 25 prosenttia = 2,25
- **Laskun kokonaissumma:** = 9,00 + 0,00 = 9,00.

> [!IMPORTANT]
> Jos sekä **On Vapautus** -vaihtoehto että **On käyttövero** -vaihtoehto on asetettu arvoon **Kyllä** verokoodissa, koodi tunnustetaan verovapaaksi myyntitapahtumissa ja käyttövero ostotapahtumissa.

### <a name="reverse-charges"></a>Käänteinen veloitus

Jos määrität **Käänteisen kulun** asetukseksi **Kyllä** **Yleiset**-pikavälilehdessä, veroprosentti voidaan konfiguroida negatiiviseksi. Käänteisen verotuksen skenaariossa suosittelemme, että määrität kaksi verokoodia: toisen, jolla on positiivinen verokanta ja toisen, jolla on negatiivinen veroprosentti. Molempien verokoodien taksa-arvon tulee olla sama, ja **Käänteisen kulun** vaihtoehdon pitäisi olla **Kyllä** sen verokoodin osalta, jonka veroprosentti on negatiivinen. Lisätietoja Financen käänteisen veloituksen ratkaisusta on kohdassa [ALV/GST-mallin käänteisen veloituksen mekanismi](emea-reverse-charge.md).

Esimerkiksi kaksi verokoodia määritetään yhdellä laskurivillä. Yksi veroprosentti on 25 prosenttia. Toinen veroprosentti on -25 prosenttia ja **On käänteinen vero**-asetuksena on **Kyllä** toisessa verokoodissa. Laskurivillä näkyy määrä, joka on 10 nimikettä, kukin 1,00. Tässä tapauksessa poikkeamasummat lasketaan seuraavasti:

- **Nettosumma:** (10 × 1,00) = 10,00 
- **Verokoodi 1:** 10,00 × 25 prosenttia = 2,50
- **Verokoodi 2:** 10 × -25 prosenttia = -2,50
- **Laskun kokonaissumma:** = 10,00 + 2,50 = 10,00.

### <a name="exclusion-from-base-amount-calculations"></a>Jätetään pois perussumman laskelmista

Jos määrität **Yleiset**-pikavälilehdessä, että **Jätä pois veron perusteen laskenta** -asetuksen arvoksi **Kyllä**, verokoodin laskettu verosumma jätetään pois veron perustesummasta muita hinnan sisällytysskenaarion verokoodilaskelmia varten.

Katso lisätietoja kohdasta [Veron laskeminen hintoihin, kun Hinnat sisältävät verot ‑asetus on otettu käyttöön](global-exclude-from-tax-base-amount-calculation.md).

### <a name="rates"></a>Asteet

**Veroprosentti**-pikavälilehdessä voit määrittää eri veroprosenttien asetukset eri verojen perussummia varten. Veron summan laskemista varten veron laskentapalvelu käyttää aina veroperusteen summaa vastaavaa veroprosenttia.

Veroasteet voidaan konfiguroida esimerkiksi seuraavassa taulukossa esitetyllä tavalla.

| Pienin summa | Enimmäissumma | Veroprosentti   |
| -------------- | -------------- | ---------- |
| 0              | 1 000          | 10 prosenttia |
| 1 000          | 5 000          | 15 prosenttia |
| 5 000          | 10,000         | 20 prosenttia |
| 10,000         | 0              | 30 prosenttia |

Tässä tapauksessa verosummat lasketaan seuraavasti:

- Jos veron peruste on 300,00, veroprosentti on 10 prosenttia ja veron summa on 300,00 × 10 prosenttia = 30,00.
- Jos veron peruste on 3.000,00, veroprosentti on 15 prosenttia ja veron summa on 3.000,00 × 15 prosenttia = 450,00.
- Jos veron peruste on 6.000,00, veroprosentti on 20 prosenttia ja veron summa on 6.000,00 × 10 prosenttia = 1.200,00.
- Jos veron peruste on 20.000,00, veroprosentti on 30 prosenttia ja veron summa on 20.000,00 × 30 prosenttia = 6.000,00.

> [!NOTE]
> Jos veron perustesumma voi täsmätä sekä yhden rivin enimmäissumman että toisen rivin vähimmäissumman, veron peruste käyttää veroprosenttia, joka vastaa vähimmäisperusteen summaa. Esimerkiksi, jos veron peruste on 1000,00, veroprosentti on 15 prosenttia ja veron summa on 1.000,00 × 15 prosenttia = 150,00.

### <a name="limits"></a>Rajat

**Rajat**-pikavälilehdellä voit määrittää verorajat, jotka ohittavat lasketun verosumman, jos verosumma laskee minimi-/maksimiarvoalueeseen.

- Jos laskettu verosumma on suurempi tai yhtä suuri kuin **Rajat**-pikavälilehdessä määritetty enimmäisverosumma, lopullinen verosumma on sama kuin enimmäisverosumma.
- Jos laskettu verosumma on pienempi kuin **Rajat**-pikavälilehdessä määritetty vähimmäisverosumma, lopullinen verosumma on 0 (nolla).

Verorajat määritetään esimerkiksi seuraavasti:

- **Vähimmäisverosumma:** 100 
- **Enimmäisverosumma:** 1,000

Jos laskettu verosumma on 2 000, veron loppusumma on 1 000.

Jos laskettu verosumma on 500, veron loppusumma on 500.

Jos laskettu verosumma on 80, veron loppusumma on 0 (nolla).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
