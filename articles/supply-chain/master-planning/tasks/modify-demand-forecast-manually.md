---
title: 'Opas: kysynnän ennusteen manuaalinen muokkaaminen'
description: Tässä artikkelissa kerrotaan, miten nimikkeen ennustetta muokataan
author: t-benebo
ms.date: 08/12/2019
ms.topic: business-process
ms.search.form: EcoResProductDetailsExtended, ForecastSales
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6275749f85c9b9d5a8b89da6340beeafbe22c2d4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8859253"
---
# <a name="guide-modify-a-demand-forecast-manually"></a>Opas: kysynnän ennusteen manuaalinen muokkaaminen

[!include [banner](../../includes/banner.md)]

Tässä menettelyssä kerrotaan, miten nimikkeen ennustetta muokataan. Tämä menettely on tarkoitettu tuotannon suunnittelijalle.

## <a name="modify-the-forecast-for-a-selected-item"></a>Valitun nimikkeen ennusteen muokkaaminen

Valitun nimikkeen ennusteen muokkaaminen:

1. Mene **Moduulit \> Tuotetietojen hallinta \> Tuotteet \> Vapautetut tuotteet**.
1. Etsi haluamasi tietue luettelosta ja valitse se. Valitse nimike, jonka ennustetta haluat muokata.
1. Avaa toimintoruudun **Suunnitelma**-välilehti ja valitse **Kysyntäennuste**.
1. Valitse luettelosta rivi. Jos ennusterivejä ei ole, luo uusi rivi valitsemalla toimintoruudusta **Uusi**.  
1. Syötä positiivinen luku **Myyntimäärä**-kenttään. Tämä luku kertoo nimikkeen ennustetun määrän. Näyttöön tulee virheilmoitus, jos olet syöttänyt negatiivisen luvun.
1. Täytä muiden kenttien tarvittavat tiedot.
1. Valitse toimintoruudussa **Tallenna**.

## <a name="modify-the-forecast-for-one-or-more-items-with-microsoft-excel"></a>Yhden tai useamman nimikkeen ennusteen muokkaaminen Microsoft Excelissä

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
