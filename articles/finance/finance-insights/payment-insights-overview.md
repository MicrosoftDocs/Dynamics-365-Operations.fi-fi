---
title: Asiakkaan maksuennusteet (esiversio)
description: Tässä ohjeaiheessa kerrotaan maksuennusteiden ominaisuudesta. Sen avulla saat lisätietoja asiakkaan tyypillisistä maksutavoista. Tämän toiminnon avulla voit myös määrittää olosuhteet, joiden vuoksi perintäprosessit ehkä aloitetaan normaalia aikaisemmin.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2019-11-06
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: b321fdc185e175d9fe2673c9f1e16486efd8e798
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645670"
---
# <a name="customer-payment-predictions-preview"></a>Asiakkaan maksuennusteet (esiversio)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Tässä ohjeaiheessa kerrotaan maksuennusteiden ominaisuudesta. Sen avulla saat lisätietoja asiakkaan tyypillisistä maksutavoista. Tämän toiminnon avulla voit myös määrittää olosuhteet, joiden vuoksi perintäprosessit ehkä aloitetaan normaalia aikaisemmin.

## <a name="overview"></a>Yleiskuvaus

Organisaatiot pitävät usein haastavana ennustaa milloin asiakkaat maksavat laskut. Tiedonpuute voi aiheuttaa seuraavia ongelmia:

- Vähemmän tarkkoja kassavirtaennusteita
- Liian myöhään alkavat perintäprosessit
- Tilausten vapauttaminen asiakkaille, jotka voivat jättää laskut maksamatta

Asiakkaan maksuennusteet (esiversio) auttaa organisaatioita ennustamaan, milloin myyntilasku maksetaan. Näin voidaan luoda perintästrategioita, joiden avulla voidaan nostaa ajoissa maksamisen todennäköisyyttä.

## <a name="predictions"></a>Ennusteet

Maksuennusteiden avulla organisaatiot voivat parantaa liiketoimintaprosesseja. Ennusteet auttavat tunnistamaan laskut, jotka todennäköisesti maksetaan myöhässä. Organisaatio voi käyttää näitä tietoja sellaisten toimintojen yhteydessä, jotka parantavat ajoissa maksamista.

Asiakkaan maksuennusteet -toiminto käyttää koneoppimismallia. Sen avulla voidaan tarkasti ennustaa, milloin asiakas maksaa maksamattoman laskun. Tämä koneoppimismalli sisältää aiempia laskuja, maksuja ja asiakastietoja.

Toiminto määrittää jokaiselle avoimelle laskulle kolme maksutodennäköisyyttä:

- Todennäköisyys, että maksun suorittaminen tapahtuu ajoissa
- Todennäköisyys, että maksun suorittaminen tapahtuu myöhässä
- Todennäköisyys, että maksun suorittaminen tapahtuu erittäin paljon myöhässä

Toiminto sisältää myös odotettujen maksujen koostetun näkymän.

[![Maksuennusteiden koostenäkymä](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)

Kullekin laskulle määritetään todennäköisyys ajoissa maksamisesta. Laskut, joiden ajoissa maksamisen todennäköisyys on alle 50 prosenttia, merkitään punaisella ympyrällä. Se osoittaa, että ne ehkä tarvitsevat perintäasiamiehen huomiota.

[![Maksun todennäköisyyksien luettelo](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)

Asiakkaan maksuennusteiden toiminto sisältää myös tilannekohtaista tietoa, joka selittää ennustusta. Nämä tiedot sisältävät ennusteeseen vaikuttaneet tärkeimmät tekijät, asiakkaan liikesuhteen nykyisen tilan ja tietoja asiakkaan aiemmasta maksutoiminnasta.

Monissa yrityksissä perintäprosessi on ollut reaktiivinen toiminto. Toisin sanoen perintäprosessi ei käynnisty, ennen kuin laskut erääntyvät. Asiakkaan maksuennusteiden avulla organisaatiot voivat olla proaktiivisempia perinnän suhteen. Niiden ei enää tarvitse odottaa, että tapahtuma erääntyy, ennen kuin perintäprosessi aloitetaan. Sen sijaan ne voivat selvittää maksuennusteiden ominaisuuden avulla, parantaako ennakkoiva perintä todennäköisyyttä ajoissa tapahtuvasta maksun maksamisesta.

## <a name="methodology"></a>Metodologia

Aiemmin on yleensä ollut vaikeaa kehittää ja käyttää tekoälyratkaisuja. Tämä prosessi vaati tiimin, joka sisältää datatieteilijöitä, aihealueen asiantuntijoita ja teknikoita, jotka käyttävät paljon aikaa käyttökelpoisen tekoälyratkaisun muotoiluun, kehittämiseen, käyttöönottamiseen ja ylläpitoon. Asiakkaan maksuennusteiden avulla on helppo ottaa käyttöön ja käyttää tekoälysovellusta Microsoft Dynamics 365 Financessa. Microsoft toimittaa valmiiksi pakattuja tekoälyratkaisuja, jotka on muodostettu Microsoft AI Builderin pohjalta. Tämän vuoksi käyttäjät voivat ottaa tekoälysovelluksen käyttöön yhdellä hiiren napsautuksella. Näin he saavat käyttöönsä älykkäät ennusteet. Jos et ole tyytyväinen ennusteiden tarkkuuteen, tehokäyttäjä voi lisätä (jälleen yhdellä hiiren napsautuksella) AI Builderin laajennuskokemuksen ja sitten valita ennusteiden muodostamiseen käytettäviä kenttiä tai poistaa niiden valinnan. Kun olet valmis, voit kouluttaa mallia ja julkaista muutokset. Juuri koulutettu malli valitaan automaattisesti ja ennusteet luodan Dynamics 365 Financessa.

## <a name="release-details"></a>Julkaisun tiedot

Finance Insightsin julkinen esiversio on saatavilla käyttöönotoissa kokeilua varten Yhdysvalloissa, Euroopassa ja Yhdistyneessä kuningaskunnassa. Microsoft lisää tukea jatkuvasti myös muilla alueilla.

Julkisen esiversion ominaisuudet tulee ottaa käyttöön vain Taso 2 -eristysympäristöissä. Eristysympäristössä luotuja määrityksiä ja tekoälymalleja ei ehkä siirretä tuotantoympäristöön. Lisätietoja on kohdassa [Microsoft Dynamics 365 -esiversioiden lisäkäyttöehdot](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/public-preview-terms).

## <a name="privacy-notice"></a>Tietosuojatiedot

Esiversiot (1) voivat käyttää vähemmän tietosuojaa ja suojaustoimenpiteitä kuin Dynamics 365 Finance and Operations -palvelu, (2) eivät sisälly tämän huoltotilauksen palvelutasosopimukseen, (3) niitä ei ole tarkoitettu henkilötietojen tai muiden sellaisten tietojen käsittelemiseen, joihin liittyy lainsäädännön tai määräysten vaatimustenmukaisuusvaatimuksia ja (4) niillä on rajoitettu tuki.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]