---
title: Mukautettujen tuotesuositusten yleiskuvaus
description: "Dynamics 365 for Operationsissa voidaan näyttää suosituksia myyntipisteen laitteessa. Suositukset ovat nimikkeitä, joista asiakas on mahdollisesti kiinnostunut ostohistorian, toiveluettelon ja muiden asiakkaiden verkosta tai kivijalkakaupasta ostamien tuotteiden perusteella. Myyjillä, joilla on laajat tuoteluettelot, suositukset auttavat asiakasta löytämään uusia tuotteita. Esittämällä tuotesuosituksia, jotka on kohdistettu asiakkaan kiinnostuksen kohteisiin, kauppiaat parantavat lisä- ja ristiinmyyntiään ja tehostavat asiakkaiden sitoutumista. Dynamics 365 for Operationsin tuotesuositukset toimivat kognitiivisten palveluiden ja Microsoft Azuren koneoppimisen avulla."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
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
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: edacd4cc9f9db59617bc579cb106e8e1017b8957
ms.contentlocale: fi-fi
ms.lasthandoff: 05/25/2017


---

# <a name="personalized-product-recommendations-overview"></a>Mukautettujen tuotesuositusten yleiskuvaus

[!include[banner](includes/banner.md)]


Dynamics 365 for Operationsissa voidaan näyttää suosituksia myyntipisteen laitteessa. Suositukset ovat nimikkeitä, joista asiakas on mahdollisesti kiinnostunut ostohistorian, toiveluettelon ja muiden asiakkaiden verkosta tai kivijalkakaupasta ostamien tuotteiden perusteella. Myyjillä, joilla on laajat tuoteluettelot, suositukset auttavat asiakasta löytämään uusia tuotteita. Esittämällä tuotesuosituksia, jotka on kohdistettu asiakkaan kiinnostuksen kohteisiin, kauppiaat parantavat lisä- ja ristiinmyyntiään ja tehostavat asiakkaiden sitoutumista. Dynamics 365 for Operationsin tuotesuositukset toimivat kognitiivisten palveluiden ja Microsoft Azuren koneoppimisen avulla.

<a name="scenarios"></a>Skenaariot
---------

Tuotteen suosituksia on käytössä seuraavissa myyntipisteskenaarioissa. Ne ovat saatavissa Cloud POS - ja Modern POS (MPOS) -myyntipisteissä.

1.  **Tuotteen tiedot** -sivulla:

-   Jos myymälän päällikkö käy **Tuotteen tiedot** -sivulla tarkastelleessaan aiempia tapahtumia eri kanavissa, moduuli ehdottaa muita nimikkeitä, jotka todennäköisesti voi ostaa yhdessä.
-   Jos myymäläpäällikkö lisää asiakkaan tapahtumaan ja käy sitten **Tuotteen tiedot** -sivulla, suositusmoduuli antaa mukautettuja suosituksia käyttäen asiakkaan tapahtumahistoriaa.

[![proddetails](./media/proddetails.png)](./media/proddetails.png)

2.  **Tapahtuma**-sivulla:

-   Suositusmoduuli ehdottaa nimikkeitä kaikkien ostoskorissa olevien tuotteiden perusteella.
-   Jos myymäläpäällikkö lisää asiakkaan tapahtumaan, suositusmoduuli antaa henkilökohtaisia suosituksia käyttäen asiakkaan tapahtumahistoriaa ja ostoskorissa olevien nimikkeiden tietoja.

**Huomautus** Jotta suositukset voitaisiin näyttää **Tapahtuma**-sivulla, vähittäismyyjän pitää päivittää näytön asettelu Dynamics 365 for Operationsissa. **Suositukset**-ohjausobjekti on pudotettava **Tapahtuma**-sivulle. [![transactionscreenmultipleproductslargemessengersbag-5](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)

3.  **Asiakastiedot**-sivulla:
    -   Suositusmoduuli ehdottaa nimikkeitä käyttäjätunnuksen ja asiakkaan toivelistassa olevien tuotteiden perusteella.

[![customerdetailsrecommendations](./media/customerdetailsrecommendations.png)](./media/customerdetailsrecommendations.png)

## <a name="configure-dynamics-365-for-operations-to-enable-pos-recommendations"></a>Määritä myyntipisteen suoritukset käyttöön Dynamics 365 for Operationsissa
Voit määrittää tuotesuositukset seuraavasti.

1.  Varmista, että olet valinnut oikean **yrityksen**.
2.  Siirry kohtaan **Yksikkösäilö**, valitse **Vähittäismyynti** ja sitten **Päivitä**.** **Tämä käyttää demotietoja (tai omia tietojasi) toiminnallisesta tietokannasta ja siirtää ne yksikkösäilöön.
3.  Valinnainen: Jos haluat näyttää suositukset Tapahtuma-näytössä, siirry kohtaan **Näytön asettelu**, valitse näyttöasettelu, käynnistä **Näytön asettelun suunnittelutoiminto** ja pudota **Suositukset-ohjausobjekti** haluamaasi paikkaan.
4.  Siirry kohtaan **Vähittäismyynnin parametrit**, valitse **Automaattianalyysipalvelut** ja valitse **Kyllä** kohdassa **Ota käyttöön myyntipisteen suositukset**.
5.  Saat suositukset näkyviin myyntipisteessä suorittamalla yleisen konfiguraatiotyön **1110**. Saat myyntipisteen näytön asetteluun tehdyt muutokset näkyviin suorittamalla kanavan konfigurointityön **1070**.

## <a name="how-does-it-work"></a>[]()Miten se toimii?
Kun päivität **Yksikkösäilö**-yksikön, seuraavat toiminnot tapahtuvat.

-   Dynamics 365 for Operationsin toiminnallisesta tietokannasta poimitaan tiedot kognitiivisten palveluiden edellyttämässä muodossa ja lähetetään yksikkösäilöön.
-   Azure Data Factory (ADF) käyttää tietoja puhdistaakseen tiedot käyttäen Hive-skriptejä osana ADF-toimintoja. Puhdistetut tiedot tallennetaan blob-säilöpalveluun.
-   Kognitiivisten palvelujen API käyttää blob-etäsäilöpalvelun tietoja harjoittaakseen suositusmallia.

Kun otat käyttöön **Ota suositukset käyttöön** -asetuksen ja suoritat konfiguraatiotyöt, tapahtuu seuraavat toiminnot.

-   Mallin tunnistetiedot ja tunnus noudetaan API-liittymästä ja tallennetaan Dynamics 365 for Operationsin operatiiviseen tietokantaan, AOS:n web.config-tiedostoon sekä Retail-palvelimelle.
-   Mallin tunnistetiedot ja tunnus annetaan saataville CRT:lle niin, että tuotteen suosituspyynnöt online-tilassa olevista Cloud POS- ja MPOS -myyntipisteistä voidaan suorittaa.


<a name="see-also"></a>Lisätietoja
--------

[Suositusten ohjausobjektin lisääminen myyntipisteen laitteen tapahtumasivulle](add-recommendations-control-pos-screen.md)




