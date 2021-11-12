---
title: Laskurivien luominen toimittajan laskuja tuotaessa
description: Tässä aiheessa kuvataan toiminto, jolla toimittajan laskuihin luodaan automaattisesti laskurivejä, kun laskuja tuodaan.
author: sunfzam
ms.date: 09/10/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2021-08-30
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 87dec3c142ae296975ab98432421be4548085c80
ms.sourcegitcommit: 9e8d7536de7e1f01a3a707589f5cd8ca478d657b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/18/2021
ms.locfileid: "7647885"
---
# <a name="generate-invoice-lines-when-you-import-vendor-invoices"></a>Laskurivien luominen toimittajan laskuja tuotaessa

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Tässä aiheessa kuvataan toiminto, jolla toimittajan laskuihin luodaan automaattisesti laskurivejä, kun laskuja tuodaan.

Joskus toimittajan laskut sisältävät rajallisia tietoja esimerkiksi vastaanottajatietojen ja välisummien osalta. Ne eivät kuitenkaan sisällä rivinimikkeiden tietoja. Kun tuot laskuja, järjestelmä voi luoda laskurivejä automaattisesti vastaavan ostotilauksen tietojen perusteella.

Voit ottaa laskurivien automaattisen luonnin käyttöön noudattamalla seuraavia ohjeita.

1.  Valitse **Ostoreskontra \> Asetukset \> Ostoreskontran parametrit**.
2.  Määritä **Tuotujen laskujen automaattinen rivien luonti** -kohdan **Toimittajan laskujen automaatio** -välilehdessä **Luo laskurivejä automaattisesti** -asetuksen arvoksi **Kyllä**. 
4.  Valitse **Valitse laskurivien automaattisen luonnin oletusmäärä** -kentässä määrä, jota järjestelmä käyttää laskurivien automaattisessa luonnissa:

    - **Tilattu määrä** – Järjestelmä luo rivejä ostotilauksen riveistä. Tämä arvo on oletusarvo.
    - **Vastaanotettu tuotemäärä** – Järjestelmä käyttää ostotilausnumeroita asianomaisten tuotteen vastaanottojen löytämiseen. Tämän jälkeen se käyttää tuotteen vastaanotettuja määriä laskurivien luomiseen.

## <a name="data-entity-changes"></a>Tietoyksikköjen muutokset

**Toimittajan laskun otsikko** -tietoyksikköä on parannettu, jotta se tukee tässä aiheessa kuvattua toimintoa. Kolme kenttää on lisätty

- **HeaderOnlyImport** – Tämän kentän arvona on oltava **Kyllä**, jotta järjestelmä luo laskuotsikkojen rivejä.
- **PurchIdRange** – Ostotilausnumeroiden luettelo. Laskunumerot voivat olla alueita, kuten **INV0001..INV0009** (jossa kaksi pistettä erottavat alueen alun ja lopun), tai erillisiä arvoja, kuten **INV0001, INV0003, INV0006**. Kaikkien ostotilausten on kuuluttava samaan toimittajatiliin laskuotsikossa. Muussa tapauksessa saat seuraavan virhesanoman: Laskurivien luonti epäonnistui. Ostotilauksilla on eri toimittajatilit.
- **PackingslipRange** – Tuotteen vastaanottonumeroiden luettelo. Toimittajan laskun rivejä voi luoda tuotevastaanotoista. Tuotteen vastaanottonumeroita ei kuitenkaan yleensä sisällytetä toimittajan laskuihin. Syötä tähän kenttään tuotteen vastaanottonumeroita vain, jos pystyt selkeästi tunnistamaan, mitkä tuotteen vastaanotot kuuluvat mihinkin erillisiin laskuihin. Laskurivejä voidaan luoda tuotteiden vastaanottojen perusteella. Jos tätä kenttää käytetään, **Ostoreskontran parametrit** -sivun **Valitse laskurivien automaattisen luonnin oletusmäärä** -kentän asetusta ei oteta huomioon. 

**Rajoitus**: Jos syötät useita tuotteen vastaanottonumeroita, samalla laskunumerolla luodaan useita odottavia toimittajan laskuja. Ne on konsolidoitava manuaalisesti ennen laskun käsittelyn jatkamista. Tulevissa julkaisuissa aiomme mahdollistaa järjestelmälle laskujen automaattisen konsolidoinnin, jolloin rajoitus poistuu.

Kaikkien tuotteen vastaanottojen on kuuluttava samaan toimittajatiliin laskuotsikossa.

## <a name="result"></a>Tulos

Jos järjestelmä luo rivejä onnistuneesti, toimittajan laskun automaatiohistoriaan kirjataan seuraava sanoma: Automaattinen laskurivien luominen: Onnistui.

Jos järjestelmä ei pysty luomaan rivejä, kirjataan seuraava virhesanoma: Automaattinen laskurivien luominen: Epäonnistui.
