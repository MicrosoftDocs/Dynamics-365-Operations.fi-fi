---
title: Suositusten lisääminen tapahtumanäyttöön
description: Tässä ohjeaiheessa kuvataan suositusten ohjausobjektin lisääminen myyntipisteen laitteen tapahtumanäytölle käyttämällä Microsoft Dynamics 365 Commercein näytön asettelun suunnittelutoimintoa.
author: bebeale
manager: AnnBe
ms.date: 05/26/2020
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
ms.openlocfilehash: af2450b27106325a86f6db68f9791637694cda63
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411855"
---
# <a name="add-recommendations-to-the-transaction-screen"></a>Suositusten lisääminen tapahtumanäyttöön

[!include [banner](includes/banner.md)]


Tässä ohjeaiheessa kuvataan suositusten ohjausobjektin lisääminen myyntipisteen laitteen tapahtumanäytölle käyttämällä Microsoft Dynamics 365 Commercein näytön asettelun suunnittelutoimintoa. Lisätietoja tuotesuositusominaisuuksista on [POS-dokumentaation tuotesuosituksissa](product.md).


Voit näyttää tuotesuosituksia myyntipisteen laitteessa, kun käytät Commercea. Voit näyttää tuotteen suosituksi lisäämällä ohjausobjektin tapahtumanäytölle näytön asettelun suunnittelutoiminnon avulla. 

## <a name="open-layout-designer"></a>Avaa asettelun suunnittelutoiminto

1. Siirry kohtaan **Retail ja Commerce** &gt; **Kanavan asetukset** &gt; **POS-asetukset** &gt; **Myyntipiste** &gt; **Näytön asettelut**.
2. Pikasuodattimen avulla voit etsiä näyttöä, johon haluat lisätä ohjausobjektin. Voit esimerkiksi suodattaa **Näyttöasettelun tunnus** -kentässä arvolla **F2CP16:9M**.
3. Etsi haluamasi tietue luettelosta ja valitse se. Valitse esimerkiksi **Nimi: F2CP16:9M Näyttöasettelun tunnus: F2CP16:9M**.
4. Valitse **Asettelun suunnittelutoiminto**.
5. Noudata kehotteita asettelun suunnittelutoiminnon käynnistämiseksi. Tunnistetietoja kysyttäessä anna samat tunnistetiedot, jotka olivat käytössä, kun asettelun suunnittelutoiminto käynnistettiin **Näytön asettelut** -sivulla.
6. Kun kirjaudut, tulee sivu, joka on samanlainen kuin alla oleva. Asettelu on erilainen riippuen oman myymälän tekemistä mukautuksista.


    [![Asettelun suunnittelutoiminto](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png)

## <a name="choose-a-display-option"></a>Näyttöasetuksen valitseminen

Käytettävissä on kaksi asetusta. Valitse vaihtoehto, joka sopii parhaiten myymälällesi ja noudata ohjeita loppuun viimeistelläksesi ohjausobjektin määrittämisen. Asetukset ovat:

- Suositukset ovat aina näkyvissä.
- **Suositukset**-välilehti näkyy ruudukossa näytön oikealla puolella.

### <a name="make-recommendations-always-visible"></a>Suositusten tuominen aina näkyviin


1. Pienennä tapahtumarivien erittelyalueen korkeutta niin, että se on samalla korkeudella kuin vasemmalla puolella oleva asiakaspaneeli.


    [![Tapahtumarivien erittelyalueen korkeutta vähennetty](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)

2. Vasemmanpuoleisesta valikosta vedä ja pudota suosituksien ohjausobjekti Tapahtumarivin tiedot -alueen ja painikeruudukon väliin näytön alareunassa keskellä. Muuta ohjausobjektin kokoa, jotta se mahtuu kyseiseen tilaan.

    [![Suositusten ohjaus lisätty asetteluun](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)


3. Valitse **X**, jotta tallennat ja poistut asettelun suunnittelutoiminnosta.
4. Valitse Commercessa **Retail ja Commerce** &gt; **Retail ja Commerce IT** &gt; **Jakeluaikataulut**.
5. Valitse luettelossa **1090, kassakoneet**.
6. Valitse **Suorita nyt**.


### <a name="add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a>Suositukset-välilehden lisääminen painikeruudukkoon näytön oikealla puolella

1. Napsauta hiiren kakkospainikkeella tyhjää tilaa sivun oikeassa reunassa painikeruudukon viimeisen välilehden alapuolella.

2. Valitse **Mukauta**.

    [![Mukautus - Välilehden ohjausvalintaikkuna](./media/pic-5.png)](./media/pic-5.png)

3. Valitse **Uusi välilehti**.
4. Etsi juuri lisäämäsi uusi välilehti. Näyttöä on ehkä vieritettävä alaspäin.
5. Valitse avattavassa **Sisältö**-valikossa **Suositellut tuotteet**.

    [![Suositeltujen tuotteiden valinta Sisältö-valikossa](./media/pic-6.png)](./media/pic-6.png)

6. Kirjoita **Otsikko**-kenttään suositusten välilehden nimi. Kirjoita esimerkiksi Suositellut tuotteet.
7. Valitse **Kuva**-kentässä välilehdessä näytettävä kuva.
8. Valitse **OK**. Painikeruudukkoon tulee uusi välilehti.
9. Valitse **X**, jotta tallennat ja poistut asettelun suunnittelutoiminnosta.
10. Valitse Commercessa **Retail ja Commerce** &gt; **Retail ja Commerce IT** &gt; **Jakeluaikataulut**.
11. Valitse luettelossa **1090, kassakoneet**.
12. Valitse **Suorita nyt**.

## <a name="additional-resources"></a>Lisäresurssit

[Tuotesuositusten yleiskatsaus](product-recommendations.md)

[Azure Data Lake Storagen käyttöönotto Dynamics 365 Commerce -ympäristössä](enable-adls-environment.md)

[Tuotesuositusten ottaminen käyttöön](enable-product-recommendations.md)

[Kohdennettujen suositusten ottaminen käyttöön](personalized-recommendations.md)

[Kohdennetuista tuotesuosituksista kieltäytyminen](personalization-gdpr.md)

["Osta samankaltaisia tyylejä" -suositusten käyttöönotto](shop-similar-looks.md)

[Tuotesuositusten lisääminen myyntipisteessä](product.md)

[AI-ML-suositusten tulosten muokkaaminen](modify-product-recommendation-results.md)

[Kuratoitujen suositusten manuaalinen luominen](create-editorial-recommendation-lists.md)

[Suositusten luominen esittelytietojen avulla](product-recommendations-demo-data.md)

[Tuotesuositukset – usein kysytyt kysymykset](faq-recommendations.md)
