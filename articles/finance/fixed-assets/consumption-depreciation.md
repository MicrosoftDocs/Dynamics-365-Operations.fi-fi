---
title: Kulutuspoisto
description: Tässä artikkelissa on yleiskuvaus poiston kulutusmenetelmästä.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.custom: 13751
ms.assetid: d25a681f-49a5-4bfc-aa76-1c6373e35dd8
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9a11389d1042eb62ed081d7615fea2f370de8255
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5826999"
---
# <a name="consumption-depreciation"></a>Kulutuspoisto

[!include [banner](../includes/banner.md)]

Tässä artikkelissa on yleiskuvaus poiston kulutusmenetelmästä.

Kun määrität käyttöomaisuuksien poistoprofiilin ja valitset **Poistoprofiilit**-sivun **Menetelmä**-kentässä **Kulutus**, poistoprofiiliin määritetyt käyttöomaisuudet perustuvat niiden käyttöön. Prosenttiosuuksia ja välejä ei tarvitse määrittää **Poistoprofiilit**-sivulla. Kun olet luonut kulutusmenetelmää käyttävän poistoprofiilin, voit määrittää menetelmän monella tavalla.

## <a name="set-up-and-use-consumption-depreciation"></a>Kulutuspoiston määrittäminen ja käyttö
1.  Luo poistoprofiili valitsemalla **Poistoprofiilit**-sivu. Kulutuslaskelmia varten poistoprofiililla on oltava tunnus ja nimi. Lisäksi **Menetelmä**-kentässä on valittava **Kulutus**.
2.  Määritä kulutuskertoimet **Kulutuskertoimet**-sivulla. Jokaisella kulutuskertoimelle on oltava tunnus ja nimi. Lisäksi kulutuskertoimen on oltava määritetty määräksi tai prosenttiosuudeksi.
3.  Määritä kulutusyksiköt **Kulutusyksiköt**-sivulla. Jokaisella kulutusyksiköillä on oltava tunnus ja nimi. Poistoyksiköitä käytetään laskemaan kulutuspoisto **Kulutuspoisto**-sivulla. Yksiköitä ovat esimerkiksi kilometri (km), kilogramma (kg) ja tunti.
4.  Määritä yksittäiset käyttöomaisuudet **Käyttöomaisuudet**-sivulla. Valitse kullekin käyttöomaisuudelle arvomallit ja poistokirjat, joilla on poistoprofiilit. Kulutuspoistolle on määritettävä arvomallit tai poistokirjat, jos jokin käyttöomaisuuksista käyttää kulutusmenetelmään perustuvia poistoprofiileja. Tämä määritys tehdään joko **Arvomallit**-sivun **Poisto**-välilehdessä tai **Poistoprofiili**-sivun **Yleinen**-pikavälilehdessä. Samaa arvomallia voi käyttää useissa käyttöomaisuuksissa. Poistoprofiilit ovat osa kullekin käyttöomaisuuserälle valittua arvomallia tai poistokirjaa. Ei voi lisätä etkä muokata poistoprofiileja suoraan **Käyttöomaisuudet**-sivulla. Voit muokata poistoprofiileja vain **Poistokirjat**-sivulla.
5.  Anna tiedot seuraaviin **Arvomallit**- tai **Poistokirjat**-sivun **Kulutuspoisto**-kenttäryhmän kenttiin:
    -   Kulutuskerroin
    -   Yksikkö
    -   Yksikköpoistot
    -   Arvioitu kulutus

    **Kirjattu kulutus** -kentässä näkyy yksikköinä kulutuspoisto, joka on jo kirjattu joko käyttöomaisuus- ja arvomalliyhdistelmälle tai poistokirjaan. Et voi päivittää tämän kentän arvoa manuaalisesti.

## <a name="examples"></a>Esimerkkejä
### <a name="example-1"></a>Esimerkki 1

Seuraava kulutuskerroin on määritetty tammikuun 31. päivälle:

-   Määrä on 1 000.
-   Kiinteälle omaisuudelle määritetty yksikön poistohinta on 1,5.

Tammikuun 31. päivän poistoehdotus on seuraava: määrä x yksikkö poisto 1 000 × 1,5 = 1 500 Jos käyttöomaisuudelle määritetty kerroin on prosenttikerroin, käyttöomaisuuden arvomallin **Arvioitu kulutus** -kentässä arvioitu määrä kerrotaan valitulle päättymispäivälle määritetyllä prosentilla. Tulokseksi saatavaa määrää ehdotetaan sitten kauden poistomääräksi.

### <a name="example-2"></a>Esimerkki 2

Seuraava kulutuspoiston kerroin on määritetty tammikuun 31. päivälle:

-   Prosentti on 10 prosenttia.
-   Kiinteälle omaisuudelle määritetty yksikön poistohinta on 1,5.
-   Käyttöomaisuuserän arvioitu määrä on 2 000.

Tammikuun 31. päivän poistoehdotus on seuraava: arvioitu määrä × prosentti × yksikköpoisto 2 000 × 0,10 × 1,5 = 300





[!INCLUDE[footer-include](../../includes/footer-banner.md)]