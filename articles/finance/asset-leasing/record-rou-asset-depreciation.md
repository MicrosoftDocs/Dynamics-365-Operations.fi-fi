---
title: Käyttöoikeusomaisuuserän poiston tallentaminen (esiversio)
description: Tässä artikkelissa kerrotaan, miten kirjauskansiovienti luodaan kuoletukselle, joka on pakollinen organisaation taseen vuokraussopimuksille.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseAssetSchedule
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 93e521cf409af4c01d625f27bdd7a7564e471bd9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8903273"
---
# <a name="record-right-of-use-asset-depreciation-preview"></a>Käyttöoikeusomaisuuserän poiston tallentaminen (esiversio)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]


Jos vuokrasopimukset ovat organisaation taseessa, käyttöoikeusomaisuuserä kuoletetaan kuukausittain. Tässä artikkelissa kerrotaan, miten kuoletuksen kirjauskansiovienti luodaan. Kuoletus veloittaa kulukirjauskansiotiliä ja hyvittää kumuloitua poistokirjauskansiotiliä kirjausprofiilin ja vuokrasopimustyypin määrityksen mukaan. Nämä viennit voidaan luoda jokaiselle vuokrasopimukselle tai ne voidaan luoda useille vuokrasopimuksille eräkirjauskansiotoiminnon avulla.

## <a name="asset-depreciation-schedule"></a>Resurssin poistoaikataulu

1. Valitse vuokrasopimus **Vuokrasopimusyhteenveto**-sivulla. Valitse sitten **Kirjat \> Käyttöomaisuuden poistoaikataulu**, jos haluat avata **Käyttöomaisuuden poistoaikataulu** -sivun.

    Käyttöoikeusomaisuuserän poistokulukirjauskansiovienti perustuu **Poistokulu**-sarakkeeseen. Myöhemmin tässä artikkelissa on esimerkki kirjanpitostandardin yhdenmukaisuusohjeesta [Käyttöoikeusomaisuuserän kuoletuskulun laskeminen rahoitusleasingsopimuksille](#calculation-of-rou-asset-amortization-expense-for-finance-leases).
    
2. Valitse poistokausi ja valitse sitten **Luo kirjauskansio**. Näyttöön tulee sanoma, joka ilmaisee, että poiston tallentamisessa käytettävä kirjauskansio on jo luotu.
3. Valitse **Kirjauskansiot \> Resurssin leasingkirjauskansiot**, jos haluat avata **Resurssin leasingkirjauskansio**-sivun, jossa voit tarkastella luotua poistokulukirjauskansiovientiä.

   Järjestelmä lukitsee tietyt taloushallinnon kentät ja estää niiden muokkaamisen. Tällä tavoin estetään tapahtumien ja aikataulujen väliset varianssit. Lukittuja ovat esimerkiksi seuraavat kentät: **Tili**, **Summat**, **Taloushallinnon dimensiot**, **Valuutta** ja **Tapahtumatyyppi**. Lisäksi kirjauskansiovientirivejä ei voi lisätä tai poistaa missään resurssin vuokrauskirjauskansion vienneissä, sillä se voi aiheuttaa aikataulujen ja tapahtumien välisiä variansseja.

4. Valitse kirjauskansiovienti ja valitse sitten **Kirjaa**, jos haluat tallentaa poistoviennin kirjanpitoon.

## <a name="calculation-of-rou-asset-amortization-expense-for-operating-leases"></a>Käyttöoikeusomaisuuserän kuoletuskulun laskeminen käyttöleasingsopimuksille

Käyttöleasingsopimuksen poistokulu lasketaan kuukausittaisen tasan vuokrakuluna ja kuukausittainen korkokulu vuokrasopimusvelassa ASC 842:n mukaan. Se on Yhdysvaltojen yleisti hyväksytty kirjanpitostardardi US GAAP. Tasapoistovuokrakulu lasketaan kaikkien vuokrien summana jaettuna vuokra-ajalla kuukausina. (Vuokramaksujen summa sisältää ennakkomaksut, alkuvaiheen välittömät menot, purkamiskustannukset ja vuokrasopimukseen liittyvät kannustimet.) Seuraavassa taulukossa on esimerkki käyttöleasingsopimuksen kuoletuskulusta.

### <a name="example-of-rou-asset-amortization-expense-for-operating-leases"></a>Käyttöoikeusomaisuuserän kuoletuskulun esimerkki käyttöleasingsopimuksille

| Kenttä                                          | Arvo       |
|------------------------------------------------|-------------|
| Maksun summa                                 | 1 000       |
| Maksun toistuvuus                              | Kuukausittain     |
| Vuokra-aika (kuukautta)                            | 24          |
| Vuokrat yhteensä                           | 24,000      |
| Inkrementaalinen lainakorko                     | 5 %          |
| Annuiteetin tyyppi                                   | Erääntyvä annuiteetti |
| Yhdistämisväli                           | Kuukausittain     |
| Tulevien vähimmäisvuokrien nykyinen arvo | 22,888.87   |

Kuten aiemmin mainittiin, tasapoistovuokrakulu lasketaan kokonaissummana jaettuna vuokra-ajalla. Järjestelmä laskee automaattisesti kuukausittaiset korkokulut velan kuoletusaikataulusta. Korkokulu lasketaan käyttämällä efektiivisen koron menetelmää. Järjestelmä käyttää tasavuokrakustannusta korkokulun vähentämisessä kuukausittain. Arvoa käytetään käyttöoikeusomaisuuserän vähentämisessä.

| Kuukausi | Tasavuokrakustannus | Korkokustannus                        | Käyttöoikeusomaisuuserän kuoletuskulun laskeminen |
|-------|--------------------------|-----------------------------------------|-----------------------------------------------|
| 1     | (24 000 ÷ 24) = 1 000,00 | (22 888,87 – 1 000) × (5 % ÷ 12) = 91,20 | 1 000 – 91,20 = 908,80                        |
| 2     | (24 000 ÷ 24) = 1 000,00 | (21 980,08 – 1 000) × (5 % ÷ 12) = 87,42 | 1 000 – 87,42 = 912,58                        |
| 3     | (24 000 ÷ 24) = 1 000,00 | (21 067,49 – 1 000) × (5 % ÷ 12) = 83,62 | 1 000 – 83,62 = 916,39                        |

> [!NOTE]
> ASC 842:n mukaan käyttöoikeusomaisuuserän poisto käyttöleasingsopimuksessa luokitellaan vuokrakuluksi tuloslaskelmassa. Käyttöoikeusomaisuuden vuokra kuvaa viennin käyttöoikeusomaisuuserän poistona. Veloitusvienti on kuitenkin määritettävä käyttöleasingsopimuksen kulutilille ja hyvitysvienti suoraan käyttöleasingsopimuksen käyttöoikeusomaisuuserälle. Vuokrasopimuksen parametreissa voidaan kuitenkin määrittää, että hyvitysviennit on tehtävä kumuloituun poistotiliin käyttöleasingin käyttöoikeusomaisuuserille.

Jos vuokra luokitellaan käyttövuokraksi, kuukausittainen poisto arvonalennuksen jälkeen lasketaan tasapoistomenetelmällä.

## <a name="calculation-of-rou-asset-amortization-expense-for-finance-leases"></a>Käyttöoikeusomaisuuserän kuoletuskulun laskeminen rahoitusleasingsopimuksille

Taloushallinnon luokituksen omaaville vuokrasopimuksille järjestemä laskee käyttöoikeusomaisuuserän kuoletuksen tasaisesti. Siksi poistokulut ovat samat jokaiselle kuukaudelle.

IFRS 16:n ja ASC 842:n mukaan käyttöoikeusomaisuus kuoletetaan joko vuokra-ajan tai resurssin käyttöiän perusteella sen mukaan, kumpi on lyhyempi. Lisäksi jos **Omistajuuden siirto** -parametri on käytössä tässä vuokrasopimuksessa, se poistetaan automaattisesti käyttöoikeusomaisuuden käyttöiän aikana.

### <a name="example-of-rou-asset-amortization-expense-for-finance-leases"></a>Käyttöoikeusomaisuuserän kuoletuskulun esimerkki rahoitusleasingsopimuksille

| Kenttä                                | Arvo                                   |
|--------------------------------------|-----------------------------------------|
| Aloituksen käyttöoikeusomaisuuserän saldo | 22,889.87                               |
| Vuokra-aika (kuukautta)                  | 24                                      |
| Käyttöomaisuuden käyttöikä (kuukautta)           | 36                                      |
| Kuukausi                                | Käyttöoikeusomaisuuserän kuoletuskulu |
| 1                                    | 22 889,87 ÷ 24 = 953,74                 |
| 2                                    | 22 889,87 ÷ 24 = 953,74                 |
| 3                                    | 22 889,87 ÷ 24 = 953,74                 |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
