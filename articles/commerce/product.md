---
title: Tuotesuositusten lisääminen myyntipisteessä
description: Tässä ohjeaiheessa kuvataan myyntipisteen (POS) tuotesuositusten käyttöä.
author: bebeale
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 7afe9225b8fc966ca154a5eb7421e8d4cc7c3023
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4412081"
---
# <a name="add-product-recommendations-on-pos"></a>Tuotesuositusten lisääminen myyntipisteessä

[!include [banner](includes/banner.md)]

Tuotesuositukset ovat uudistava yrityssovellus, joka ulottuu kaikkiin kaupan tiloihin monipuolisten, sitouttavien ja räätälöityjen tuotteiden löytämisen kokemusten luomiseksi. Jos haluat ottaa tämän toiminnon käyttöön myyntipisteessä, noudata ohjeita [Suositusten lisääminen POS-laitteisiin.](add-recommendations-control-pos-screen.md) 

Lisätietoja tuotesuositusominaisuuksista on kohdassa [Tuotesuositusten yleiskatsaus](../commerce/product-recommendations.md). 

## <a name="scenarios"></a>Skenaariot

Tuotteen suosituksia on käytössä seuraavissa myyntipisteskenaarioissa. Ne ovat saatavissa Cloud POS - ja Modern POS (MPOS) -myyntipisteissä.

1. **Tuotteen tiedot** -sivulla:

    - Jos myyjä käy **Tuotteen tiedot** -sivulla tarkastellessaan aiempia tapahtumia eri kanavissa, suosituspalvelu ehdottaa muita nimikkeitä, jotka todennäköisesti voi ostaa yhdessä.

    [![Tuotetiedot-sivun suositukset](./media/proddetails.png)](./media/proddetails.png)

2. **Tapahtuma**-sivulla:

    - Suositusmoduuli ehdottaa nimikkeitä, jotka perustuvat niiden korissa olevien nimikkeiden luetteloon, jotka ostetaan usein yhdessä.

    > [!NOTE]
    > Jotta suositukset voitaisiin näyttää **Tapahtuma**-sivulla, vähittäismyyjän pitää päivittää näytön asettelu Dynamics 365 Commerceissa. **Suositukset**-ohjausobjekti on pudotettava **Tapahtuma**-sivulle.

    [![Tapahtumasivun suositukset](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)

## <a name="configure-commerce-to-enable-pos-recommendations"></a>Commercen määrittäminen ottamaan käyttöön myyntipisteen suositukset

Voit määrittää tuotesuositukset noudattamalla seuraavia ohjeita:

1. Varmista, että palvelu on päivitetty **10.0.6-versioon.**
2. Noudata ohjeita: [tuotesuositusten käyttöönotto](../commerce/enable-product-recommendations.md).
3. Valinnainen: Jos haluat näyttää suositukset Tapahtuma-näytössä, siirry kohtaan **Näytön asettelu**, valitse näyttöasettelu, käynnistä **Näytön asettelun suunnittelutoiminto** ja pudota **Suositukset**-ohjausobjekti haluamaasi paikkaan.
4. Siirry kohtaan **Commercen parametrit**, valitse **Automaattianalyysipalvelut** ja valitse **Kyllä** kohdassa **Ota käyttöön myyntipisteen suositukset**.
5. Saat suositukset näkyviin myyntipisteessä suorittamalla yleisen konfiguraatiotyön **1110**. Saat myyntipisteen näytön asetteluun tehdyt muutokset näkyviin suorittamalla kanavan konfigurointityön **1070**.

## <a name="troubleshoot-issues-where-you-have-product-recommendations-already-enabled"></a>Jo käyttöönotettuihin tuotesuosituksiin liittyvien ongelmien vianmääritys

- Valitse **Commercen parametrit** \> **Suositusluettelot** \> **Poista tuotesuositukset käytöstä** ja suorita **Yleinen konfiguraatiotyö \[9999\]**. 
- Jos lisäsit **suositusten ohjausobjektin** tapahtumanäyttöön **näytön asettelun suunnittelutoiminnolla**, poista myös se.
- Jos sinulla on lisäkysymyksiä, lisätietoja kohdassa [Tuotesuositusten usein kysytyt kysymykset](../commerce/faq-recommendations.md).

## <a name="additional-resources"></a>Lisäresurssit

[Tuotesuositusten yleiskatsaus](product-recommendations.md)

[Azure Data Lake Storagen käyttöönotto Dynamics 365 Commerce -ympäristössä](enable-adls-environment.md)

[Tuotesuositusten ottaminen käyttöön](enable-product-recommendations.md)

[Kohdennettujen suositusten ottaminen käyttöön](personalized-recommendations.md)

[Kohdennetuista tuotesuosituksista kieltäytyminen](personalization-gdpr.md)

["Osta samankaltaisia tyylejä" -suositusten käyttöönotto](shop-similar-looks.md)

[Suositusten lisääminen tapahtumanäyttöön](add-recommendations-control-pos-screen.md)

[AI-ML-suositusten tulosten muokkaaminen](modify-product-recommendation-results.md)

[Kuratoitujen suositusten manuaalinen luominen](create-editorial-recommendation-lists.md)

[Suositusten luominen esittelytietojen avulla](product-recommendations-demo-data.md)

[Tuotesuositukset – usein kysytyt kysymykset](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]