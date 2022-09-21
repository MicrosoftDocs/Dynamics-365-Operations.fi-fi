---
title: Laskurivien luominen toimittajan laskuja tuotaessa
description: Tässä artikkelissa kuvataan toiminto, jolla toimittajan laskuihin luodaan automaattisesti laskurivejä, kun laskuja tuodaan.
author: sunfzam
ms.date: 09/10/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2021-08-30
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 5cb2c1234de03e9777921c18e4cbb81eec7feef9
ms.sourcegitcommit: 9c637bcf4e2eb8f711290a861492f038feaf1568
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/09/2022
ms.locfileid: "9462271"
---
# <a name="generate-invoice-lines-when-you-import-vendor-invoices"></a>Laskurivien luominen toimittajan laskuja tuotaessa

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Tässä artikkelissa kuvataan toiminto, jolla toimittajan laskuihin luodaan automaattisesti laskurivejä, kun laskuja tuodaan.

Joskus toimittajan laskut sisältävät rajallisia tietoja esimerkiksi vastaanottajatietojen ja välisummien osalta. Ne eivät kuitenkaan sisällä rivinimikkeiden tietoja. Kun tuot laskuja, järjestelmä luo laskurivit automaattisesti vastaavan ostotilauksen tietojen perusteella.

Voit ottaa laskurivien automaattisen luonnin käyttöön noudattamalla seuraavia ohjeita.

1.  Valitse **Ostoreskontra \> Asetukset \> Ostoreskontran parametrit**.
2.  Määritä **Tuotujen laskujen automaattinen rivien luonti** -kohdan **Toimittajan laskujen automaatio** -välilehdessä **Luo laskurivejä automaattisesti** -asetuksen arvoksi **Kyllä**. 
4.  Valitse **Valitse laskurivien automaattisen luonnin oletusmäärä** -kentässä määrä, jota käytetään laskurivien automaattisessa luonnissa:

    - **Tilattu määrä** – Rivit luodaan ostotilauksen riveistä. Tämä arvo on oletusarvo.
    - **Vastaanotettu tuotemäärä** – Käytetään ostotilausnumeroa asianomaisten tuotteen vastaanottojen löytämiseen. Tämän jälkeen se käyttää tuotteen vastaanotettuja määriä laskurivien luomiseen.

## <a name="data-entity-changes"></a>Tietoyksikköjen muutokset

**Toimittajan laskun otsikko** -tietoyksikköä on parannettu, jotta se tukee tässä artikkelissa kuvattua toimintoa. Kolme kenttää on lisätty

- **HeaderOnlyImport** – Tämän kentän arvona on oltava **Kyllä**, jotta voidaan luoda laskuotsikkojen rivit.
- **PurchIdRange** – Ostotilausnumeroiden luettelo. Laskunumerot voivat olla alueita, kuten **PO0001..PO0009** (jossa kaksi pistettä erottavat alueen alun ja lopun), tai erillisiä arvoja, kuten **PO0001, PO0003, PO0006**. Kaikkien ostotilausten on kuuluttava samaan toimittajatiliin laskuotsikossa. Muussa tapauksessa saat seuraavan virhesanoman: Laskurivien luonti epäonnistui. Ostotilauksilla on eri toimittajatilit.
- **PackingslipRange** – Tuotteen vastaanottonumeroiden luettelo. Toimittajan laskun rivejä voi luoda tuotevastaanotoista. Tuotteen vastaanottonumeroita ei kuitenkaan yleensä sisällytetä toimittajan laskuihin. Syötä tähän kenttään tuotteen vastaanottonumeroita vain, jos pystyt selkeästi tunnistamaan, mitkä tuotteen vastaanotot kuuluvat mihinkin erillisiin laskuihin. Laskurivejä voidaan luoda tuotteiden vastaanottojen perusteella. Jos tätä kenttää käytetään, **Ostoreskontran parametrit** -sivun **Valitse laskurivien automaattisen luonnin oletusmäärä** -kentän asetusta ei oteta huomioon. 

**Rajoitus**: Jos syötät useita tuotteen vastaanottonumeroita, samalla laskunumerolla luodaan useita odottavia toimittajan laskuja. Ne on konsolidoitava manuaalisesti ennen laskun käsittelyn jatkamista. Tulevissa julkaisuissa aiomme mahdollistaa laskujen automaattisen konsolidoinnin, jolloin rajoitus poistuu.

Kaikkien tuotteen vastaanottojen on kuuluttava samaan toimittajatiliin laskuotsikossa.

## <a name="result"></a>Tulos

Jos rivit luodaan onnistuneesti, toimittajan laskun automaatiohistoriaan kirjataan seuraava sanoma: Automaattinen laskurivien luominen: Onnistui.

Jos rivejä ei pystytä luomaan, kirjataan seuraava virhesanoma: Automaattinen laskurivien luominen: Epäonnistui.
