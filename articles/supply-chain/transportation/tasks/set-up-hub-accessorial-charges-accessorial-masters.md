---
title: Määritä keskuksen lisämaksut ja lisämaksun päätiedot
description: Tässä menettelyssä kerrotaan, miten keskuksen lisämaksun päätiedot luodaan ja miten päätietoja käytetään keskuksen lisämaksun luomisessa.
author: ShylaThompson
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1ea59326a85d97d53795104f80486f2fac24148a
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148514"
---
# <a name="set-up-hub-accessorial-charges-and-accessorial-masters"></a>Määritä keskuksen lisämaksut ja lisämaksun päätiedot

[!include [banner](../../includes/banner.md)]

Tässä menettelyssä kerrotaan, miten keskuksen lisämaksun päätiedot luodaan ja miten päätietoja käytetään keskuksen lisämaksun luomisessa. Menettelyssä käytetään USMF-tietojoukkoa. Kuljetuskoordinaattori määrittää tämän yleensä.


## <a name="set-up-a-hub-master"></a>Määritä keskuksen päätietoja
1. Valitse Kuljetustenhallinta > Asetukset > Luokitus > Lisämaksun päätiedot.
2. Valitse Uusi.
3. Kirjoita arvo Lisämaksun päätiedot -kenttään.
4. Kirjoita arvo Nimi-kenttään.
5. Valitse Lisämaksun tyyppi -kentässä Keskus.
6. Valitse Tallenna.
7. Sulje sivu.

## <a name="set-up-a-hub-accessorial-charge"></a>Keskuksen lisämaksun määrittäminen
1. Valitse Kuljetustenhallinta > Asetukset > Luokitus > Keskuksen lisämaksut.
2. Valitse Uusi.
3. Kirjoita Keskuksen lisämaksun tunnus -kenttään arvo.
4. Avaa haku valitsemalla Keskus-kentässä avattavan valikon painike.
5. Etsi haluamasi tietue luettelosta ja valitse se.
6. Valitse vaihtoehto Keskuksen sijainti -kentässä.
    * Voit luoda joko nouto- tai jättökulun. Kulu kohdistetaan valintaasi vastaavaan kuljetussegmenttiin reitillä.  
7. Avaa haku valitsemalla Lisämaksun päätiedot -kentässä avattavan valikon painike.
8. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
    * Valitse juuri luomasi päätiedot.  
9. Valitse Tallenna.
10. Sulje sivu.

