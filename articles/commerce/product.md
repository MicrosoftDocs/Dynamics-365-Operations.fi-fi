---
title: Tuotesuositusten lisääminen myyntipisteessä
description: Tässä artikkelissa kuvataan myyntipisteen (POS) tuotesuositusten käyttöä.
author: bebeale
ms.date: 09/08/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 170e2bf18aefc79a796620818c7100ff8e6e689a
ms.sourcegitcommit: f88273627ba105ede27f28fe67ccec2d7f78261c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/09/2022
ms.locfileid: "9460053"
---
# <a name="add-product-recommendations-on-pos"></a>Tuotesuositusten lisääminen myyntipisteessä

[!include [banner](includes/banner.md)]

Tuotesuositukset ovat uudistava yrityssovellus, joka ulottuu kaikkiin kaupan tiloihin monipuolisten, sitouttavien ja räätälöityjen tuotteiden löytämisen kokemusten luomiseksi. Jos haluat ottaa tämän toiminnon käyttöön myyntipisteessä, noudata ohjeita [Suositusten lisääminen POS-laitteisiin.](add-recommendations-control-pos-screen.md) 

Lisätietoja tuotesuositusominaisuuksista on kohdassa [Tuotesuositusten yleiskatsaus](../commerce/product-recommendations.md). 

## <a name="scenarios"></a>Skenaariot

Tuotteen suosituksia on käytössä seuraavissa myyntipisteskenaarioissa. Ne ovat saatavissa Cloud POS - ja Modern POS (MPOS) -myyntipisteissä.

1. **Tuotteen tiedot** -sivulla:

    - Jos myyjä käy **Tuotteen tiedot** -sivulla tarkastellessaan aiempia tapahtumia eri kanavissa, suosituspalvelu ehdottaa muita nimikkeitä, jotka todennäköisesti voi ostaa yhdessä. Palvelun apuohjelmista riippuen jälleenmyyjät voivat näyttää **Osta samanlaisia** - ja **Osta samankaltaisesti kuvattuja tuotteita** -suosituksia tuotteille sekä henkilökohtaisia suosituksia käyttäjille, joilla on ostohistoriaa.

    [![Tuotetiedot-sivun suositukset.](./media/proddetails.png)](./media/proddetails.png)

2. **Tapahtuma**-sivulla:

    - Suositusmoduuli ehdottaa nimikkeitä, jotka perustuvat niiden korissa olevien nimikkeiden luetteloon, jotka ostetaan usein yhdessä.

    > [!NOTE]
    > Jotta suositukset voitaisiin näyttää **Tapahtuma**-sivulla, vähittäismyyjän pitää päivittää näytön asettelu Dynamics 365 Commercessa. **Suositukset**-ohjausobjekti on pudotettava **Tapahtuma**-sivulle.

    [![Tapahtumasivun suositukset.](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)

## <a name="configure-commerce-to-enable-pos-recommendations"></a>Commercen määrittäminen ottamaan käyttöön myyntipisteen suositukset 

Jos haluat määrittää tuotesuosituksia, vahvista, että olet tehnyt valmisteluprosessin Commerce-tuotteen suosituksille kohdan [Tuotesuositusten ottaminen käyttöön](../commerce/enable-product-recommendations.md) ohjeiden avulla. Oletusarvoisesti suositukset näkyvät sekä **Tuotetiedot**- että **Asiakastiedot**-sivulla sen jälkeen, kun valmisteluvaiheet on suoritettu ja tiedot on käsitelty oikein. 

## <a name="add-recommendations-to-the-transaction-screen"></a>Suositusten lisääminen tapahtumanäyttöön

1. Voit lisätä suosituksia tapahtumanäyttöön kohdan [Suositusten lisääminen tapahtumanäyttöön](add-recommendations-control-pos-screen.md) ohjeiden avulla.
1. Jos haluat myyntipisteen näytön asettelun suunnittelutoiminnon muutokset näkyviin, suorita kanavan määritystyö **1070** Commerce headquartersissa.

> [!NOTE] 
> Jos haluat ottaa käyttöön myyntipisteen suositukset käyttämällä RecoMockin CSV-tiedostoa, ota käyttöön CSV-tiedosto Microsoft Dynamics Lifecycle Services (LCS) -resurssikirjastossa ennen asettelun hallintaohjelman määrittämistä. Jos käytät RecoMockin CSV-tiedostoa, suosituksia ei tarvitse ottaa käyttöön. CSV-tiedosto on käytettävissä vain esittelytarkoituksia varten. Sitä suositellaan asiakkaille ja ratkaisuarkkitehdeille, jotka haluavat matkia suositusluetteloiden ulkonäköä esittelytarkoituksissa ilman apuohjelman SKU:n ostamista.

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
