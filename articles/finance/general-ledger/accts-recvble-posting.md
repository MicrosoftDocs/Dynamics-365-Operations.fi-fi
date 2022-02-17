---
title: Myyntireskontran kirjaus
description: Tässä ohjeaiheessa on tietoja siitä, miten kirjaukset on konfiguroitu myyntireskontraan, sekä esimerkkejä kirjauskonfiguraatioista.
author: rachel-profitt
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustPosting, CustPaymMode, CustCashDiscount, CommissionPosting, MarkupTable\_Cust, CustPaymFee
audience: Application User
ms.reviewer: twheeloc
ms.custom: ''
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-03
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5e664c42461e4f2995cac9a747d85d0f2a0fdf85
ms.sourcegitcommit: 96f936267d3f314f06da6ce6f809eba2ec3b205f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/24/2022
ms.locfileid: "8021601"
---
# <a name="accounts-receivable-posting"></a>Myyntireskontran kirjaus

[!include [banner](../includes/banner.md)]

**Myyntireskontra**-moduulin ensisijainen kirjausprofiili on asiakkaan kirjausprofiili. Tämä kirjausprofiili määrittää yhteenvetotilin, jota käytetään, kun asiakkaan saldot kirjataan kirjanpitoon. Yhteenvetotili on päätili. Sitä kutsutaan myös myyntireskontran kauppatiliksi.

Lisätietoja on kohdassa [Asiakkaan kirjausprofiilit](../accounts-receivable/customer-posting-profiles.md).

Myyntireskontrassa on käytettävissä useita kirjauskonfiguraatioita sekä asiakkaan kirjausprofiili. Seuraavissa osissa on lisätietoja muista kirjausmäärityksistä.

## <a name="posting-accounts-for-methods-of-payment"></a>Maksutapojen kirjaustilit

Maksutavat määrittävät, miten maksu kirjataan kirjanpitoon. Ne ohjaavat myös maksun tuotoksen toimintaa. Tavallisesti kullekin organisaation hyväksymälle maksutyypille luodaan yksi maksutapa (esimerkiksi käteinen, sekki, luottokortti, maksumääräys ja tilisiirto).

**Yleiset**-pikavälilehden **Kirjaus**-osan kentät ohjaavat, miten maksu kirjataan kirjanpitoon. Ensin on valittava arvo **Tilityyppi**-kentästä. Valittava tilityyppi ohjaa **Maksutili**-kentän toimintaa. On suositeltavaa valita **Tilityyppi**-kentästä **Pankki** ja valita pankkitili **Maksutili**-kentästä. Tämän menetelmän etuna on se, että järjestelmä kirjaa maksun pankin alareskontraan, joka tukee täsmäytystä ja muita käteistä liittyviä prosesseja. Seuraavassa taulukossa on esimerkki kirjausprofiilin konfiguraatiosta, jos käytät **Kassan- ja pankkihallinta** -moduulia.

| Kirjaustyyppi | Tilityyppi | Päätilin nimen esimerkki | Tilityyppi | Veloitus/hyvitys? | Selvitystili | Kuvaus |
|--------------|--------------|---------------------------|--------------|---------------|------------------|-------------|
| Pankki | Pankki | Bank of Contoso | Käyttöomaisuuserään linkitetty pankkitili | Luotto | Ei | Määritä kunkin maksutavan päätili **Maksutili**-kenttään. |

Jos et aio käyttää käteisen ja pankin hallintaa, valitse **Tilityyppi**-kentästä **Kirjanpito** ja valitse sitten päätili **Maksutili**-kentästä. Seuraavassa taulukossa on esimerkki kirjausprofiilin konfiguraatiosta, jos et käytä Kassa- ja pankkihallintaa.

| Kirjaustyyppi | Tilityyppi | Päätilin nimen esimerkki | Tilityyppi | Veloitus/hyvitys? | Selvitystili | Kuvaus |
|--------------|--------------|---------------------------|--------------|---------------|------------------|-------------|
| Ledger | Ledger | 100100: Bank of Contoso | Resurssi | Luotto | Ei | Määritä kunkin maksutavan päätili **Maksutili**-kenttään. |

## <a name="bridging-accounts"></a>Välitilit

Välitiliöinti on kaksivaiheinen prosessi, jota käytetään maksuja kirjattaessa. Tämä on valinnainen toiminto, jota voidaan käyttää esimerkiksi nollasaldoisten pankkitilien kanssa. Se voi auttaa varmistamaan pankin täsmäytysprosessin, joka on joustavampi ja ajan tasalla. Ensimmäisessä vaiheessa maksu kirjataan väliaikaiselle tilille (suojaustilille). Toisessa vaiheessa kirjattu tapahtuma palautetaan ja kirjataan pankkitilille, kun maksu tyhjentää pankin. Seuraavassa taulukossa on esimerkki välitilikirjauksen kirjausprofiilin konfiguroinnista.

| Kirjaustyyppi | Päätiliesimerkki. | Päätilin nimen esimerkki | Tilityyppi | Veloitus/hyvitys? | Selvitystili | Kuvaus |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-------------|
| Kirjanpidon kirjauskansio | 130725 | Lunastettu käteinen | Velat | Debit | Kyllä | Määritä kunkin maksutavan päätili **Välitili**-kenttään. |

Lisätietoja on kohdassa [Välitilimaksujen määrittäminen ja käsitteleminen](../accounts-receivable/set-up-and-process-bridged-payments.md).

## <a name="posting-accounts-for-customer-cash-discounts"></a>Asiakkaan käteisalennusten kirjaustilit

Jos organisaatiosi tarjoaa käteisalennuksia asiakkaille pikamaksua vastaan, käteisalennuskoodit on määritettävä ja alennukset on kirjattava kirjanpitoon. Voit määrittää asiakkaan käteisalennuksen kirjaamiseen käytetyn päätilin useilla eri asetuksilla.

Lisätietoja on kohdassa [Kassa-alennukset](../cash-bank-management/cash-discounts.md).

## <a name="posting-accounts-for-payment-fees"></a>Toimitusmaksun kirjaustilit

Toimitusmaksut sallivat maksun lisäämisen automaattisesti asiakasmaksuun, kun ehtoja on määritetty. Toimitusmaksuja voidaan veloittaa asiakkaalta tai ne voidaan kirjata pankkitilille kuluna. Seuraavassa on muutamia esimerkkejä:

- Veloitat asiakkailta 3 prosenttia maksun kokonaissummasta, jos he maksavat luottokortilla.
- Pankkisi veloittaa sinulta 1,00 $ jokaisesta käsittelemästäsi pankkisiirrosta, ja pankkisiirtomaksu kirjataan kuluksi.

Jos määrität asiakkaan toimitusmaksun konfiguroinnissa **Veloitus**-kentän arvoksi **Asiakas**, **päätili**-kenttä ei ole käytettävissä ja järjestelmä kirjaa maksun asiakkaan kirjausprofiilin avulla. Jos määrität **Veloitus**-kentän arvoksi **Kirjanpito**, määritä **päätili**-kentän arvoksi päätili, jolle toimitusmaksu kirjataan. Tästä päätilistä tulee tavallisesti kulutili. Seuraavassa taulukossa on esimerkki toimitusmaksun kirjauksen kirjausprofiilin konfiguroinnista.

| Kirjaustyyppi | Päätiliesimerkki. | Päätilin nimen esimerkki | Tilityyppi | Veloitus/hyvitys? | Selvitystili | Kuvaus |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-------------|
| Kirjanpidon kirjauskansio | 618190 | Pankkikulu | Kulut | Debit | Ei |  Jos **Kulu**-kenttään on valittu **Kirjanpito**, voit valita tämän tilin **Päätili**-kentässä toimitusmaksulle. |

Lisätietoja on ohjeaiheessa [Asiakkaan toimitusmaksujen määrittäminen](../accounts-receivable/tasks/establish-customer-payment-fees.md).

## <a name="posting-accounts-for-charges-codes"></a>Kulukoodien kirjaustilit

Jos haluat seurata myyntisummia rivinimikkeiden lisäksi, voit käyttää kulukoodeja. Voit esimerkiksi veloittaa rahti- ja käsittelymaksuja tai kuluja asiakkailta, tai osasta rahti- ja käsittelymaksuja sisäisesti. Voit määrittää, kirjataanko nämä summat kulutileille vai lisätäänkö summat nimikkeiden kustannuksiin.

Voit luoda veloituksia myyntireskontralle ja ostoreskontralle. Kun konfiguroit kulukoodin, kirjaus on määritettävä. Kirjaus ohjaa sekä debet- että kredit-tiliä. Kun luot kulukoodeja, voit valita kullekin koodille käytettävän kirjaustyypin. Seuraavassa taulukossa on yleisiä esimerkkejä myyntireskontran veloituskoodeista.

| Kirjaustyyppi | Päätiliesimerkki. | Päätilin nimen esimerkki | Tilityyppi | Veloitus/hyvitys? | Selvitystili | Kuvaus |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-------------|
| Toimitusmaksu | 411400 | Tuotto – Maksut | Myyntituotto | Luotto | Ei | **Esimerkki, jossa ei ole riittävästi varoja:** Asiakkaan/toimittajan debet ja kirjanpitotilin kredit |
| Tilausrahti | 403500 | Tuotto – Rahti | Myyntituotto | Luotto | Ei | **Esimerkki asiakkaalta veloitettavalta rahdista:** Asiakkaan/toimittajan debet ja kirjanpidon kredit |
| Hyvitys  \* | 403200 | Alennus | Myyntituotto | Debit | Ei | **Esimerkki asiakkaan ostohyvityksestä:** Kirjanpitotilin debet ja asiakkaan/toimittajan kredit |

\*Ostohyvitysesimerkkiä käytetään vain, kun kulukoodi lisätään ostotilauksen ylätunnisteeseen tai riville. Microsoftin Dynamics 365 Supply Chain Managementin lisähyvitystoiminnot ohjaavat ja automatisoivat ostohyvityksiä entistä enemmän. Lisätietoja on kohdassa [Asiakkaan ostohyvitykset](../../supply-chain/sales-marketing/tasks/process-customer-rebates.md).

Edellisessä taulukossa on kolme tyypillistä esimerkkiä kirjaustyypeistä, joita voidaan käyttää kulukoodeissa. Sitä tulee käyttää ohjeena ja esimerkkinä. Se ei näytä kattavaa luetteloa kaikista mahdollisista yhdistelmistä tai kirjaustyypeistä, joita voidaan käyttää.

Lisätietoja on kohdassa [Kulukoodien luominen](../accounts-receivable/create-charges-codes.md).

## <a name="posting-accounts-for-commissions"></a>Provisioiden kirjaustilit

Voit vaihtoehtoisesti määrittää järjestelmän laskemaan myyntiedustajan tai myyntiedustajaryhmän provisiot tietystä myyntitilauksesta. Jos otat tämän toiminnon käyttöön, sinun on määritettävä kirjaustili, jota käytetään provision laskemiseen. Tämä konfigurointi tehdään **Myynti ja markkinointi** -moduulin **Provision kirjaus** -sivulla.

Lisätietoja on ohjeaiheessa [Myyntiprovisiosääntöjen määrittäminen](../../supply-chain/sales-marketing/tasks/set-up-sales-commission-rules.md).
