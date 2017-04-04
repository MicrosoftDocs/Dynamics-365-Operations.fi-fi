---
title: Omat suositukset tuotekuvaus
description: "Tuotteen suosituksia voi näkyä Dynamics 365 operaatioille, siten myyntiä (POS)-laite. Suositukset kohteita asiakas mahdollisesti kiinnostuneita mukaan ostohistorian, niiden haluavansa luettelon kohteet ja kohteet, joita muut asiakkaat ostaa online- ja Tiili ja laastin kaupat. Suositukset auttavat asiakkaan kuvastojen suurten vähittäiskauppiaiden, tuotteen etsiminen. Näennäiskonepohjainen tuotteita, jotka on kohdistettu asiakkaan kiinnostuksen kohteita ja ostava käyttöä, tuote-suositukset auttavat vähittäiskauppiaita ylös-myy ja cross-myy ja voit parantaa asiakkaan pidätys. Dynamics 365 operaatioille tuote-suositukset ovat powered kognitiivisia ja Microsoftin Azure machine learning."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: af1f4ba1ed5efe0e35d08d37d09e7ada4a4c1b7a
ms.lasthandoff: 03/31/2017


---

# <a name="personalized-product-recommendations-overview"></a>Omat suositukset tuotekuvaus

Tuotteen suosituksia voi näkyä Dynamics 365 operaatioille, siten myyntiä (POS)-laite. Suositukset kohteita asiakas mahdollisesti kiinnostuneita mukaan ostohistorian, niiden haluavansa luettelon kohteet ja kohteet, joita muut asiakkaat ostaa online- ja Tiili ja laastin kaupat. Suositukset auttavat asiakkaan kuvastojen suurten vähittäiskauppiaiden, tuotteen etsiminen. Näennäiskonepohjainen tuotteita, jotka on kohdistettu asiakkaan kiinnostuksen kohteita ja ostava käyttöä, tuote-suositukset auttavat vähittäiskauppiaita ylös-myy ja cross-myy ja voit parantaa asiakkaan pidätys. Dynamics 365 operaatioille tuote-suositukset ovat powered kognitiivisia ja Microsoftin Azure machine learning.

<a name="scenarios"></a>Skenaariot
---------

Tuotteen suosituksia on käytössä seuraavissa tilanteissa POS. Ne ovat saatavissa Cloud POS tai Moderni POS (MPOS).

1.  - **Tuotetiedot** sivulla:

-   Jos liittää myymälä vierailut **tuotetiedot** sivulle, kun paljasta aiempiin tapahtumiin eri kanavien kautta suositus moottorin ehdottaa muita kohteita, jotka ovat todennäköisesti voi ostaa yhdessä.
-   Jos myymälä liittää Lisää asiakas tapahtumaan ja käy sitten **tuotetiedot** sivun suositus moottorin neuvoo mukautetun käyttäen Asiakkaan tapahtumahistorian.

[![proddetails](./media/proddetails.png)](./media/proddetails.png)

2.  - **Tapahtuma** sivulla:

-   Moottori suositus ehdottaa koko luetteloa korissa perusteella.
-   Jos myymälä liittää Lisää asiakas tapahtumaan, suositus moottorin ja neuvoo omat ja asiakkaan Tapahtumahistorian kohteita luetteloon käyttämällä korissa.

**Huomautus** suosituksia näkyy **tapahtuma** sivun vähittäismyyjän on päivitettävä työvaiheiden 365 Dynamics-näyttöasettelun. **Suosituksia** valvonta on jätettävä, **tapahtuman** sivulla. [![transactionscreenmultipleproductslargemessengersbag-5](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)

3.  - **Asiakkaan tiedot** sivulla:
    -   Moottori suositus ehdottaa Käyttäjätunnus ja asiakkaan haluavansa luettelon kohteiden perusteella.

[![customerdetailsrecommendations](./media/customerdetailsrecommendations.png)](./media/customerdetailsrecommendations.png)

## <a name="configure-dynamics-365-for-operations-to-enable-pos-recommendations"></a>365 Dynamics POS suosituksia käyttöön toimintojen määrittäminen
Määritä tuotteen suosituksia, tarvitset seuraavasti.

1.  Varmista, että olet valinnut oikean **yritys**.
2.  Siirry **yksikön store**, valitse **Retail-myynti**, ja valitse sitten **päivittää**. ** ** Tämä demo-data (tai tietoja) käyttää toiminnallisia tietokannasta ja yksikkö myymälä siirtyy.
3.  Valinnainen: Jos haluat Näytä suositusten tapahtuman näytössä, siirry ** näyttöasettelun **näyttöasettelun valitsemiseen, käynnistää **näytön asettelun suunnittelutoiminto**,** ** ja pudota ** suositusten valvonta ** tarvittaessa.
4.  Siirry **vähittäismyynnin parametreja**, valitse **koneen opiskelun**, valitse ** Kyllä ** alla **Ota POS suosituksia**.
5.  Saat suosituksia POS yleismääritysten työ suoritetaan **1110**. Kanavan määritys työ suoritetaan POS-näytön asettelun suunnittelutoiminto muutosten mukaisiksi **1070**.

## <a name="how-does-it-work"></a>[]()Miten se toimii?
Kun päivität **yksikön myymälä** yritys, seuraavat toiminnot tapahtuvat.

-   Kognitiiviset palvelujen edellyttämään muotoon tietoja toimintojen toiminnassa tietokannan Dynamics-365-uutetaan ja lähettää kohteen myymälään.
-   Tietoja käytetään Azure Data Factory (Arkinsyöttölaite) puhdistaa tiedot käyttämällä komentosarjoja rakenteen Arkinsyöttölaite toiminnan osana. Puhdistettu tiedot tallennetaan blob-etäsäilöpalvelun.
-   Kognitiiviset services API käyttää tietoja blob-etäsäilöpalvelun suosituksen mallin junaan.

Kun otat käyttöön **käyttöön suosituksia** kokoonpano-työt suoritetaan ja seuraavat toiminnot tapahtuvat.

-   Mallin tunnistetiedot ja tunnus noudettu API-liittymästä ja toimien operatiivisten tietokannan Dynamics-365, AOS Web.config-tiedostossa ja myös vähittäiskaupan Server tallennettu.
-   Mallin tunnistetiedot ja tunnus saataville CRT niin, että puhelut tuotteen suositukset Cloud POS ja MPOS online-tilassa voi käyttää.


<a name="see-also"></a>Lisätietoja
--------

[Tapahtuman sivulla on POS-laitteen suositusten ohjausobjektin lisääminen](add-recommendations-control-pos-screen.md)


