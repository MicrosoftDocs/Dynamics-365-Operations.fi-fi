---
title: Kysynnän ennusteen manuaalinen muokkaaminen
description: Tässä ohjeaiheessa kerrotaan, miten nimikkeen ennustetta muokataan
author: ChristianRytt
ms.date: 08/12/2019
ms.topic: business-process
ms.search.form: EcoResProductDetailsExtended, ForecastSales
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5da1d5b1fbd91964e695a704681b1c9ee513a2f1
ms.sourcegitcommit: 4016c223a985c46e33f9941bf91ba5e1583e1cfd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/13/2021
ms.locfileid: "5889021"
---
# <a name="modify-a-demand-forecast-manually"></a>Kysynnän ennusteen manuaalinen muokkaaminen

[!include [banner](../../includes/banner.md)]

Tässä menettelyssä kerrotaan, miten nimikkeen ennustetta muokataan. Tämän menettelyn luomisessa käytetty esittely-yritys on USMF. Tämä menettely on tarkoitettu tuotannon suunnittelijalle.

## <a name="modify-the-forecast-for-a-selected-item"></a>Valitun nimikkeen ennusteen muokkaaminen

Valitun nimikkeen ennusteen muokkaaminen:

1. Mene **Moduulit \> Tuotetietojen hallinta \> Tuotteet \> Vapautetut tuotteet**.
1. Etsi haluamasi tietue luettelosta ja valitse se. Valitse nimike, jonka ennustetta haluat muokata.
1. Avaa toimintoruudun **Suunnitelma**-välilehti ja valitse **Kysyntäennuste**.
1. Valitse luettelosta rivi. Jos ennusterivejä ei ole, luo uusi rivi valitsemalla toimintoruudusta **Uusi**.  
1. Syötä positiivinen luku **Myyntimäärä**-kenttään. Tämä luku kertoo nimikkeen ennustetun määrän. Näyttöön tulee virheilmoitus, jos olet syöttänyt negatiivisen luvun.
1. Täytä muiden kenttien tarvittavat tiedot.
1. Valitse toimintoruudussa **Tallenna**.

## <a name="modify-the-forecast-for-one-or-more-items-microsoft-excel"></a>Yhden tai useamman nimikkeen ennusteen muokkaaminen Microsoft Excelissä

Yhden tai useamman nimikkeen ennusteen muokkaaminen Microsoft Excelissä:

1. Tee jompikumpi seuraavista toimista:
    - Avaa **Tarveennuste**-sivu nimikkeelle (ei merkitystä mikä niistä) edellisen osan ohjeiden mukaisesti.
    - Siirry kohtaan **Pääsuunnittelu \> Ennuste \> Manuaalinen ennusteen syöttö \> Kysynnän ennusteen rivit**.
1. Valitse toimintoruudussa **Avaa Microsoft Officessa \> Kysynnän ennusteen syöttö**.
1. Valitse ladatun tiedoston sijainti, tallenna ja avaa sitten ladattu tiedosto Excelissä.
1. Jos näyttöön tulee varoitus, valitse **Ota muokkaus käyttöön**.
1. Kirjaudu Excelissä Supply Chain Managementiin Microsoft Dynamicsin tehtäväruudun avulla. Kirjaudu sisään **Pysy sisäänkirjautuneena** -vaihtoehdolla, ja sinun on luotettava tietoyhteyssovellukseen.
1. Excel-taulukko näyttää nyt kaikki yrityksesi nykyiset tarve-ennusterivit.  Lisää, poista ja muokkaa kysynnän ennusterivejä tarpeen mukaan.
1. Valitse Microsoft Dynamics -tehtäväruudussa **Julkaise**, jos haluat ladata muutokset takaisin Supply Chain Managementiin.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
