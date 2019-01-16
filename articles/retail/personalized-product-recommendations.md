---
title: Mukautetut tuotesuositukset
description: "Tässä ohjeaiheessa on tietoja Dynamics 365 for Retailin tuotesuosituksista, jotka voidaan näyttää myyntipisteen laitteessa."
author: ashishmsft
manager: AnnBe
ms.date: 02/05/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
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
ms.translationtype: HT
ms.sourcegitcommit: 190d0b59ad2e232b33b3c0d1700cbaf95c45aeca
ms.openlocfilehash: d6706cbb7630aeb230bc9eb1c187397897c9de68
ms.contentlocale: fi-fi
ms.lasthandoff: 01/04/2019

---

# <a name="personalized-product-recommendations"></a>Mukautetut tuotesuositukset

[!include [banner](includes/banner.md)]

> [!NOTE]
> Tuotesuosituspalvelun nykyinen versio ollaan poistamassa, sillä toiminto suunnitellaan uudelleen käyttämällä parempaa algoritmia ja uudempia vähittäismyyntiin soveltuvia ominaisuuksia. Lisätietoja on kohdassa [Poistetut tai vanhentuneet ominaisuudet](../dev-itpro/migration-upgrade/deprecated-features.md).

Dynamics 365 for Retailissa voidaan näyttää suosituksia myyntipisteen laitteessa. Suositukset ovat nimikkeitä, joista asiakas on mahdollisesti kiinnostunut ostohistorian, toiveluettelon ja muiden asiakkaiden verkosta tai kivijalkakaupasta ostamien tuotteiden perusteella. Myyjillä, joilla on laajat tuoteluettelot, suositukset auttavat asiakasta löytämään uusia tuotteita. Esittämällä tuotesuosituksia, jotka on kohdistettu asiakkaan kiinnostuksen kohteisiin, kauppiaat parantavat lisä- ja ristiinmyyntiään ja tehostavat asiakkaiden sitoutumista. Dynamics 365 for Retailin tuotesuositukset toimivat kognitiivisten palveluiden ja Microsoft Azuren koneoppimisen avulla.

## <a name="scenarios"></a>Skenaariot

Tuotteen suosituksia on käytössä seuraavissa myyntipisteskenaarioissa. Ne ovat saatavissa Cloud POS - ja Modern POS (MPOS) -myyntipisteissä.

1. **Tuotteen tiedot** -sivulla:

    - Jos myymälän päällikkö käy **Tuotteen tiedot** -sivulla tarkastelleessaan aiempia tapahtumia eri kanavissa, moduuli ehdottaa muita nimikkeitä, jotka todennäköisesti voi ostaa yhdessä.
    - Jos myymäläpäällikkö lisää asiakkaan tapahtumaan ja käy sitten **Tuotteen tiedot** -sivulla, suositusmoduuli antaa mukautettuja suosituksia käyttäen asiakkaan tapahtumahistoriaa.

    [![proddetails](./media/proddetails.png)](./media/proddetails.png)

2. **Tapahtuma**-sivulla:

    - Suositusmoduuli ehdottaa nimikkeitä kaikkien ostoskorissa olevien tuotteiden perusteella.
    - Jos myymäläpäällikkö lisää asiakkaan tapahtumaan, suositusmoduuli antaa henkilökohtaisia suosituksia käyttäen asiakkaan tapahtumahistoriaa ja ostoskorissa olevien nimikkeiden tietoja.

    > [!NOTE]
    > Jotta suositukset voitaisiin näyttää **Tapahtuma**-sivulla, vähittäismyyjän pitää päivittää näytön asettelu Dynamics 365 for Retailissa. **Suositukset**-ohjausobjekti on pudotettava **Tapahtuma**-sivulle.

    [![transactionscreenmultipleproductslargemessengersbag-5](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)

3. **Asiakastiedot**-sivulla:

    - Suositusmoduuli ehdottaa nimikkeitä käyttäjätunnuksen ja asiakkaan toivelistassa olevien tuotteiden perusteella.

    [![customerdetailsrecommendations](./media/customerdetailsrecommendations.png)](./media/customerdetailsrecommendations.png)

## <a name="configure-dynamics-365-for-retail-to-enable-pos-recommendations"></a>Dynamics 365 for Retailin määrittäminen ottamaan käyttöön myyntipisteen suositukset

Voit määrittää tuotesuositukset seuraavasti.

1. Varmista, että olet valinnut oikean **yrityksen**.
2. Siirry kohtaan **Yksikkösäilö**. Valitse **Vähittäismyynti** ja valitse sitten **Päivitä**. Nyt käytössä ovat esittelytiedot (tai omat tiedot) toiminnallisesta tietokannasta. Ne siirretään yksikkösäilöön.
3. Valinnainen: Jos haluat näyttää suositukset Tapahtuma-näytössä, siirry kohtaan **Näytön asettelu**, valitse näyttöasettelu, käynnistä **Näytön asettelun suunnittelutoiminto** ja pudota **Suositukset**-ohjausobjekti haluamaasi paikkaan.
4. Siirry kohtaan **Vähittäismyynnin parametrit**, valitse **Automaattianalyysipalvelut** ja valitse **Kyllä** kohdassa **Ota käyttöön myyntipisteen suositukset**.
5. Saat suositukset näkyviin myyntipisteessä suorittamalla yleisen konfiguraatiotyön **1110**. Saat myyntipisteen näytön asetteluun tehdyt muutokset näkyviin suorittamalla kanavan konfigurointityön **1070**.

## <a name="how-does-it-work"></a>Miten se toimii?

Kun päivität **Yksikkösäilö**-yksikön, seuraavat toiminnot tapahtuvat.

- Dynamics 365 for Retailin toiminnallisesta tietokannasta poimitaan tiedot kognitiivisten palveluiden edellyttämässä muodossa ja ne lähetetään yksikkösäilöön.
- Azure Data Factory (ADF) käyttää tietoja puhdistaakseen tiedot käyttäen Hive-skriptejä osana ADF-toimintoja. Puhdistetut tiedot tallennetaan blob-säilöpalveluun.
- Kognitiivisten palvelujen API käyttää blob-etäsäilöpalvelun tietoja harjoittaakseen suositusmallia.

Kun otat käyttöön **Ota suositukset käyttöön** -asetuksen ja suoritat konfiguraatiotyöt, tapahtuu seuraavat toiminnot.

- Mallin tunnistetiedot ja tunnus noudetaan ohjelmointirajapinnasta ja tallennetaan Dynamics 365 for Retailin operatiiviseen tietokantaan, AOS:n web.config-tiedostoon sekä Retail-palvelimelle.
- Mallin tunnistetiedot ja tunnus annetaan saataville CRT:lle niin, että tuotteen suosituspyynnöt online-tilassa olevista Cloud POS- ja MPOS -myyntipisteistä voidaan suorittaa.

## <a name="troubleshoot-issues-where-you-have-product-recommendations-already-enabled"></a>Jo käyttöönotettuihin tuotesuosituksiin liittyvien ongelmien vianmääritys

- Valitse **Vähittäismyynnin parametrit** \> **Automaattianalyysipalvelut** \> **Poista tuotesuosituksen käytöstä** ja suorita **Yleinen konfiguraatiotyö \[1110\]**. Jos et löydä **Automaattianalyysipalvelut** -välilehtiä, ota yhteys Dynamics-tukeen.
- Jos lisäsit **suositusten ohjausobjektin** tapahtumanäyttöön **näytön asettelun suunnittelutoiminnolla**, poista myös se.

## <a name="additional-resources"></a>Lisäresurssit

[Suositusten ohjausobjektin lisääminen myyntipisteen laitteen tapahtumasivulle](add-recommendations-control-pos-screen.md)

