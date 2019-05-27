---
title: Suositusten ohjausobjektin lisääminen myyntipisteen laitteen tapahtumaruudulle
description: Tässä ohjeaiheessa kuvataan suositusten ohjausobjektin lisääminen myyntipisteen laitteen tapahtumanäytölle käyttämällä Microsoft Dynamics 365 for Retailin näytön asettelun suunnittelutoimintoa.
author: ashishmsft
manager: AnnBe
ms.date: 02/05/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 213b47422a5e31c2cfc2d173b8c7d9efdecc7568
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1573369"
---
# <a name="add-a-recommendations-control-to-the-transaction-screen-on-pos-devices"></a>Suositusten ohjausobjektin lisääminen myyntipisteen laitteen tapahtumaruudulle

[!include [banner](includes/banner.md)]

> [!NOTE]
> Tuotesuosituspalvelun nykyinen versio ollaan poistamassa, sillä toiminto suunnitellaan uudelleen käyttämällä parempaa algoritmia ja uudempia vähittäismyyntiin soveltuvia ominaisuuksia. Lisätietoja on kohdassa [Poistetut tai vanhentuneet ominaisuudet](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/migration-upgrade/deprecated-features).

Tässä ohjeaiheessa kuvataan suositusten ohjausobjektin lisääminen myyntipisteen laitteen tapahtumanäytölle käyttämällä Microsoft Dynamics 365 for Retailin näytön asettelun suunnittelutoimintoa.

Voit näyttää tuotesuosituksia myyntipisteen laitteessa, kun käytät Microsoft Dynamics 365 for Retailia. *Suositukset* ovat nimikkeitä, joista asiakas on mahdollisesti kiinnostunut ostohistorian, toiveluettelon ja muiden asiakkaiden verkosta tai kivijalkakaupasta ostamien tuotteiden perusteella. Voit näyttää tuotteen suosituksi lisäämällä ohjausobjektin tapahtumanäytölle näytön asettelun suunnittelutoiminnon avulla.

## <a name="open-layout-designer"></a>Avaa asettelun suunnittelutoiminto

1. Siirry kohtaan **Vähittäismyynti** &gt; **Kanavan asetukset** &gt; **POS-asetukset** &gt; **Myyntipiste** &gt; **Näytön asettelut**.
2. Pikasuodattimen avulla voit etsiä näyttöä, johon haluat lisätä ohjausobjektin. Voit esimerkiksi suodattaa **Näyttöasettelun tunnus** -kentässä arvolla F2CP16:9M.
3. Etsi haluamasi tietue luettelosta ja valitse se. Valitse esimerkiksi Nimi: F2CP16:9M Näyttöasettelun tunnus: F2CP16:9M.
4. Valitse **Asettelun suunnittelutoiminto**.
5. Noudata kehotteita asettelun suunnittelutoiminnon käynnistämiseksi. Tunnistetietoja kysyttäessä anna samat tunnistetiedot, jotka olivat käytössä, kun asettelun suunnittelutoiminto käynnistettiin **Näytön asettelut** -sivulla.
6. Kun kirjaudut, tulee sivu, joka on samanlainen kuin alla oleva. Asettelu on erilainen riippuen oman myymälän tekemistä mukautuksista.

    [![screenlayout-pic-1](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png)

## <a name="choose-a-display-option"></a>Näyttöasetuksen valitseminen

Käytettävissä on kaksi asetusta. Valitse vaihtoehto, joka sopii parhaiten myymälällesi ja noudata ohjeita loppuun viimeistelläksesi ohjausobjektin määrittämisen. Asetukset ovat:

- Suositukset ovat aina näkyvissä.
- A **Suositukset**-välilehti näkyy oikealla puolella näytön ruudukossa.

### <a name="make-recommendations-always-visible"></a>Suositusten tuominen aina näkyviin

1. Pienennä tapahtumarivien tiedot -alueen korkeutta niin, että se on samalla korkeudella kuin asiakaspaneeli vasemmalla puolellaan.

    [![screenlayout-pic-2](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)

2. Vasemmanpuoleisesta valikosta vedä ja pudota suosituksien ohjausobjekti Tapahtumarivin tiedot -alueen ja painikeruudukon väliin näytön alareunassa keskellä. Muuta ohjausobjektin kokoa, jotta se mahtuu kyseiseen tilaan.

    [![screenlayout-pic-3](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)

3. Valitse **X**, jotta tallennat ja poistut asettelun suunnittelutoiminnosta.
4. Valitse Dynamics 365 for Retailissa **Vähittäismyynti** &gt; **Vähittäismyynnin IT** &gt; **Jakeluaikataulut**.
5. Valitse luettelossa  **1090, kassakoneet**.
6. Valitse **Suorita nyt**.

### <a name="add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a>Suositukset-välilehden lisääminen painikeruudukkoon näytön oikealla puolella

1. Napsauta hiiren kakkospainikkeella tyhjää tilaa sivun oikeassa reunassa painikeruudukon viimeisen välilehden alapuolella.
2. Valitse **Mukauta**.

    [![pic-5](./media/pic-5.png)](./media/pic-5.png)

3. Valitse **Uusi välilehti**.
4. Etsi juuri lisäämäsi uusi välilehti. Näyttöä on ehkä vieritettävä alaspäin.
5. Valitse avattavassa **Sisältö**-valikossa **Suositellut tuotteet**.

    [![pic-6](./media/pic-6.png)](./media/pic-6.png)

6. Kirjoita **Otsikko**-kenttään suositusten välilehden nimi. Kirjoita esimerkiksi Suositellut tuotteet.
7. Valitse **Kuva**-kentässä välilehdessä näytettävä kuva.
8. Valitse **OK**. Painikeruudukkoon tulee uusi välilehti.
9. Valitse **X**, jotta tallennat ja poistut asettelun suunnittelutoiminnosta.
10. Valitse Dynamics 365 for Retailissa **Vähittäismyynti** &gt; **Vähittäismyynnin IT** &gt; **Jakeluaikataulut**.
11. Valitse luettelossa  **1090, kassakoneet**.
12. Valitse **Suorita nyt**.

## <a name="additional-resources"></a>Lisäresurssit

[Mukautettujen tuotesuositusten yleiskatsaus](personalized-product-recommendations.md)
