---
title: Kassavirtaennuste (esiversio)
description: Tässä ohjeaiheessa kuvataan kassavirtaennusteominaisuutta.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/19/2020
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
ms.search.validFrom: 2020-05-19
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: f97b8fc0896f0f7b95bf5609f94367b3a8230ca7
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645245"
---
# <a name="cash-flow-forecast-preview"></a>Kassavirtaennuste (esiversio)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Kassavirta on kriittinen toiminto kaikille yrityksille. Jopa kannattavia yrityksiä voi kohdata maksukyvyttömyys, jos ne eivät ylläpidä kassavirtaa vastaamaan välittömiin tarpeisiin. Finance Insightsin kassavirran ennustusominaisuuden avulla yritykset voivat tarkkailla ja hallinnoida kassan saldoja tehokkaasti. Tämä toiminto auttaa yrityksiä ennustamaan kassavirtoja aiempaa paremmin koneoppimisen avulla. Se voi myös auttaa esimiehiä tekemään päätöksiä, jotka optimoivat mahdollisuudet nykyisen kassatilanteen mukaan. 

Useimmissa yrityksissä kassavirran hallinta ja kassavirtaennusteiden suorittaminen on työläs, toistuva ja manuaalinen prosessi. Useimmat yritykset luottavat Microsoft Excel -ratkaisuihin, jotka saattavat olla monimutkaisia. Kassavirran tarkan ennustamisen haasteet ovat seuraavat:

- Päätöksentekijät eivät aina voi käyttää tietoja, koska ne ovat hajallaan useissa paikoissa, kuten: 
  - Kirjanpito-tai yritysresurssien suunnittelujärjestelmä
  - Taloushallinnon suunnitteluohjelmisto
  - Excel
  - Muut ohjelmistosovellukset 
- Ennustaminen perustuu sisäiseen tietoon, joka sijaitsee kunkin domainin tai osaston siilossa.
- Kassavirtaennusteiden tarkkuuden mittaaminen sen jälkeen, kun myyntitiedot on saatu, on epävarmaa ja vaikeaa.
    
## <a name="details-of-the-cash-flow-forecasts-capability"></a>Kassavirtaennusteominaisuuden tiedot
Kassavirtaennusteominaisuus sisältää seuraavat toiminnot. 

- Kassavirtatietojen helppo integroiminen ulkoisista järjestelmistä Dynamics 365 Financeen. Kassavirtaennusteissa voi käyttää myös tietojen tuonti- ja vientikehystä. Tämän kehyksen avulla on helppo integroida tiedot Excel ODatan kanssa. Voit yhdistää tietoja useista lähteistä ja luoda kattavan kassavirtaratkaisun. 

- Esittelee älykkään kassatilanteen. Kassatilanne luodaan asiakkaan maksutoiminnan perusteella. Sen avulla ennustetaan, milloin yritys voi odottaa rahojen tulevan tilille. Se myös analysoi maksavien toimittajien aiempia malleja ja ennustaa, milloin tulevat laskut ja tilaukset todennäköisesti maksetaan. 

- Esittelee älykkäitä kassavirtaennusteita pitkän aikavälin ennustamista varten käyttämällä aikasarjojen ennustamista automaattisen integroinnin ja AI Builderin kautta.

- Mahdollisuus tallentaa tietty kassavirran tilanne tai ennusteet, muokata niitä ja tämän jälkeen vertailla helposti ja mitata ennusteen suorituskyky todellisten taloustietojen avulla.

- Ottaa käyttöön mitä jos -analyysin tilannevedoksen vertailun avulla. Voit esimerkiksi luoda useita tilannevedoksia, jotka edustavat optimistisia, pessimistisiä ja realistisia kassavirtanäkymiä. Tämän jälkeen voit verrata eroja ja tarkastella niitä.

- Mahdollisuus tarkastella kassavirtaennustetta useissa valuutoissa ja eri yrityksissä sekä suodattaa ja tarkastella pankkitiliin liittyvää kassavirtaa. 

- Voit suodattaa ja tarkastella taloushallinnon dimensioihin liittyviä pankkitilejä.

Dynamics 365 Financen kassavirtaennustetoiminnon avulla organisaatio voi muuntaa työlään, monimutkaisen ja silti toistuvan kassavirtaennusteen yksinkertaiseksi, automatisoiduksi prosessiksi. Kassavirtaennusteen työläimpien kohtien automatisointi mahdollistaa kriittiseen päätöksentekoon keskittymisen ja haluttujen tulosten saamisen.

## <a name="setting-up-dimensions-for-cash-flow-forecasting"></a>Kassavirran ennustamisen dimensioiden määrittäminen
**Kassavirran ennustamisen määritykset** -sivun uuden välilehden avulla voit määrittää, mitkä taloushallinnon dimensiot otetaan käyttöön suodatettaessa **Kassavirran ennustaminen** -työtilaa. Tämä välilehti näkyy vain, kun Kassavirtaennusteet-toiminto on käytössä. 

Valitse **Dimensiot**-välilehdessä suodatuksessa käytettävät dimensiot luettelosta ja siirrä ne oikeanpuoleiseen sarakkeeseen nuolinäppäinten avulla. Kassavirtaennustetietojen suodattamiseen voidaan valita vain kaksi dimensiota. 

#### <a name="privacy-notice"></a>Tietosuojatiedot
Esiversiot (1) voivat käyttää vähemmän tietosuojaa ja suojaustoimenpiteitä kuin Dynamics 365 Finance and Operations -palvelu, (2) eivät sisälly tämän huoltotilauksen palvelutasosopimukseen, (3) niitä ei ole tarkoitettu henkilötietojen tai muiden sellaisten tietojen käsittelemiseen, joihin liittyy lainsäädännön tai määräysten vaatimustenmukaisuusvaatimuksia ja (4) niillä on rajoitettu tuki.
