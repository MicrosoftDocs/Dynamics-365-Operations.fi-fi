---
title: Ostoreskontran kirjaukset
description: Tässä ohjeaiheessa on tietoja siitä, miten kirjaukset on konfiguroitu ostoreskontraan, sekä esimerkkejä kirjauskonfiguraatioista.
author: rachel-profitt
ms.date: 01/19/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendPosting, VendPaymMode, VendCashDiscount, MarkupTable\_Vend, VendPaymFee
audience: Application User
ms.reviewer: twheeloc
ms.custom: ''
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-03
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fb3ebad31c9f41e405b9fc31a0f71df05fa1cc60
ms.sourcegitcommit: 10b85a09e8a550155a69aa2a8877a7c88b887242
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/20/2022
ms.locfileid: "8014450"
---
# <a name="accounts-payable-posting"></a>Ostoreskontran kirjaus

[!include [banner](../includes/banner.md)]

**Ostoreskontra**-moduulin ensisijainen kirjausprofiili on toimittajan kirjausprofiili. Tämä kirjausprofiili määrittää yhteenvetotilin, jota käytetään, kun toimittajan saldot kirjataan kirjanpitoon. Yhteenvetotili on päätili. Sitä kutsutaan myös ostoreskontran kauppatiliksi.

Lisätietoja on kohdassa [Toimittajan kirjausprofiilit](../accounts-payable/vendor-posting-profiles.md).

Ostoreskontrassa on käytettävissä useita kirjauskonfiguraatioita sekä toimittajan kirjausprofiili. Seuraavissa osissa on lisätietoja muista kirjausmäärityksistä.

## <a name="methods-of-payment-posting-accounts"></a>Maksutapojen kirjaustilit

Maksutavat määrittävät, miten maksu kirjataan kirjanpitoon. Ne ohjaavat myös maksun tuotoksen toimintaa. Tavallisesti kullekin organisaatiolle luotavalle maksutyypille luodaan yksi maksutapa (esimerkiksi käteinen, sekki, luottokortti, maksumääräys ja tilisiirto).

**Maksutavat**-sivun **Yleiset**-välilehden (**Ostoreskontra > Maksuasetukset > Maksutavat**) **Kirjaus**-osan kentät ohjaavat, miten maksu kirjataan kirjanpitoon. Ensin on valittava arvo **Tilityyppi**-kentästä. Valittava tilityyppi ohjaa **Maksutili**-kentän toimintaa. On suositeltavaa valita **Tilityyppi**-kentästä **Pankki** ja valita pankkitili **Maksutili**-kentästä. Tämän menetelmän etuna on se, että järjestelmä kirjaa maksun pankin alareskontraan, joka tukee täsmäytystä ja muita käteistä liittyviä prosesseja. Seuraavassa taulukossa on esimerkki kirjausprofiilin konfiguraatiosta, jos käytät **Kassan- ja pankkihallinta** -moduulia.

| Kirjaustyyppi | Tilityyppi | Maksutilin nimen esimerkki | Tilityyppi | Veloitus/hyvitys? | Selvitystili | Kuvaus |
|--------------|--------------|------------------------------|--------------|---------------|------------------|-------------|
| Pankki | Pankki | Bank of America | Käyttöomaisuuserään linkitetty pankkitili | Debit | Ei | Määritä kunkin maksutavan päätili **Maksutili**-kenttään. |

Jos et aio käyttää käteisen ja pankin hallintaa, valitse **Tilityyppi**-kentästä **Kirjanpito** ja valitse sitten päätili **Maksutili**-kentästä. Seuraavassa taulukossa on esimerkki kirjausprofiilin konfiguraatiosta, jos **Et** käytä Kassan- ja pankkihallintaa.

| Kirjaustyyppi | Tilityyppi |Maksutilin esimerkki | Tilityyppi | Veloitus/hyvitys? | Selvitystili | Kuvaus |
|--------------|--------------|------------------------|--------------|---------------|------------------|-------------|
| Ledger | Ledger | 100100: Bank of America | Resurssi | Debit | Ei | Määritä kunkin maksutavan päätili **Maksutili**-kenttään. |

## <a name="bridging-accounts"></a>Välitilit

Välitiliöinti on kaksivaiheinen prosessi, jota käytetään maksuja kirjattaessa. Tämä on valinnainen toiminto, jota voidaan käyttää esimerkiksi nollasaldoisten pankkitilien kanssa. Se voi auttaa varmistamaan pankin täsmäytysprosessin, joka on joustavampi ja ajan tasalla. Ensimmäisessä vaiheessa maksu kirjataan väliaikaiselle tilille (suojaustilille). Toisessa vaiheessa kirjattu tapahtuma palautetaan ja kirjataan pankkitilille, kun maksu tyhjentää pankin. Seuraavassa taulukossa on esimerkki välitilikirjauksen kirjausprofiilin konfiguroinnista.

| Kirjaustyyppi | Päätiliesimerkki. | Päätilin nimen esimerkki | Tilityyppi | Veloitus/hyvitys? | Selvitystili | Kuvaus |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-------------|
| Kirjanpidon kirjauskansio | 130725 | Lunastettu käteinen | Velat | Debit | Kyllä | Määritä kunkin maksutavan päätili **Välitili**-kenttään. |

Lisätietoja on kohdassa [Välitilimaksujen määrittäminen ja käsitteleminen](../accounts-receivable/set-up-and-process-bridged-payments.md).

## <a name="customer-cash-discounts-posting-accounts"></a>Asiakkaan käteisalennusten kirjaustilit

Jos organisaatiosi saa käteisalennuksia toimittajilta pikamaksua vastaan, käteisalennuskoodit on määritettävä ja alennukset on kirjattava kirjanpitoon. Voit määrittää asiakkaan käteisalennuksen kirjaamiseen käytetyn päätilin useilla eri asetuksilla.

Lisätietoja on kohdassa [Kassa-alennukset](../cash-bank-management/cash-discounts.md).

## <a name="payment-fee-posting-accounts"></a>Toimitusmaksun kirjaustilit

Toimitusmaksut sallivat maksun lisäämisen automaattisesti toimittajamaksuun, kun ehtoja on määritetty. Toimitusmaksuja voidaan maksaa toimittajalle tai ne voidaan kirjata pankkitilille kuluna. Seuraavassa on muutamia esimerkkejä:

- Toimittaja veloittaa 3 prosenttia maksun kokonaissummasta, jos maksat luottokortilla.
- Pankkisi veloittaa sinulta 1,00 $ jokaisesta käsittelemästäsi pankkisiirrosta, ja pankkisiirtomaksu kirjataan kuluksi.

Jos määrität toimittajan toimitusmaksun konfiguroinnissa **Veloitus**-kentän arvoksi **Toimittaja**, **päätili**-kenttä ei ole käytettävissä ja järjestelmä kirjaa maksun toimittajan kirjausprofiilin avulla. Jos määrität **Veloitus**-kentän arvoksi **Kirjanpito**, määritä **päätili**-kentän arvoksi päätili, jolle toimitusmaksu kirjataan. Tästä päätilistä tulee tavallisesti kulutili. Seuraavassa taulukossa on esimerkki toimitusmaksun kirjauksen kirjausprofiilin konfiguroinnista.

| Kirjaustyyppi | Päätiliesimerkki. | Päätilin nimen esimerkki | Tilityyppi | Veloitus/hyvitys? | Selvitystili | Kuvaus |
|--------------|----------------------|---------------------------|--------------|----------------|------------------|-------------|
| Kirjanpidon kirjauskansio | 618190 | Pankkikulu | Kulut | Debit | Ei | Jos **Kulu**-kenttään on valittu **Kirjanpito**, voit valita tämän tilin **Päätili**-kentässä **Toimitusmaksu**-sivulla. |

Lisätietoja on ohjeaiheessa [Toimittajan toimitusmaksujen määrittäminen](../accounts-payable/tasks/define-vendor-payment-fees.md).

## <a name="charges-code-posting-accounts"></a>Kulukoodien kirjaustilit

Jos haluat seurata ostosummia rivinimikkeiden lisäksi, voit käyttää kulukoodeja. Toimittaja voi esimerkiksi veloittaa rahti- ja käsittelymaksuja tai kulua osasta rahti- ja käsittelymaksuja sisäisesti. Voit määrittää, kirjataanko nämä summat kulutileille vai lisätäänkö summat nimikkeiden kustannuksiin.

Voit luoda veloituksia myyntireskontralle ja ostoreskontralle. Kun konfiguroit kulukoodin, kirjaus on määritettävä. Kirjaus ohjaa sekä debet- että kredit-tiliä. Kun luot kulukoodeja, voit valita kullekin veloituskoodille käytettävän kirjaustyypin. Seuraavassa taulukossa on esimerkkejä ostoreskontran tavallisista veloituskoodeista **Veloituskoodit**-sivulla.

| Kirjaustyyppi | Päätiliesimerkki. | Päätilin nimen esimerkki | Tilityyppi | Veloitus/hyvitys? | Selvitystili | Kuvaus |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-------------|
| Ostopalkkio | Jätä kenttä tyhjäksi. | Ei käytettävissä | Nimike | Debit | Ei | **Esimerkki nimikkeen ostomaksusta:** </p><ul><li>**Veloitustyyppi**-kenttä = **Nimike**</li><li>  **Hyvitystyyppi**-kenttä = **Asiakas/Toimittaja**.</li><li> Nimikekirjaus käyttää varaston kirjausprofiilin päätiliä. |
| Tilausrahti | 600120 | Rahti kohteessa | Myyntituotto | Debit | Ei | **Esimerkki toimittajalle maksettavasta rahdista:** </p><ul><li>**Veloitustyyppi**-kenttä = **Kirjanpitotili**</li><li> **Hyvitystyyppi**-kenttä = **Asiakas/Toimittaja** |
| Hyvitys  \* | 503160 | Toimittajan ostohyvityksen peruste (Vastatili MTKUST)| Kulut | Luotto | Ei | **Esimerkki toimittajan ostohyvityksestä:**</p><ul><li>**Veloitustyyppi**-kenttä = **Asiakas/Toimittaja**</li><li>**Hyvitystyyppi**-kenttä = **Kirjanpitotili** |

\*Ostohyvitysesimerkkiä käytetään vain, kun kulukoodi lisätään ostotilauksen ylätunnisteeseen tai riville. Microsoftin Dynamics 365 Supply Chain Managementin lisähyvitystoiminnot ohjaavat ja automatisoivat ostohyvityksiä entistä enemmän. Lisätietoja on kohdassa [Ostohyvitykset](../../supply-chain//procurement/vendor-rebates.md).

Edellisessä taulukossa on kolme tyypillistä esimerkkiä kirjaustyypeistä, joita voidaan käyttää kulukoodeissa. Sitä tulee käyttää ohjeena ja näytevalikoimana. Se ei näytä kattavaa luetteloa kaikista mahdollisista yhdistelmistä tai kirjaustyypeistä, joita voidaan käyttää.

Lisätietoja on kohdassa [Kulukoodien luominen](../accounts-receivable/create-charges-codes.md).
