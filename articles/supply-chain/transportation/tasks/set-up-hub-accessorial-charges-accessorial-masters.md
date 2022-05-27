---
title: Määritä keskuksen lisämaksut ja lisämaksun päätiedot
description: Tässä menettelyssä kerrotaan, miten keskuksen lisämaksun päätiedot luodaan ja miten päätietoja käytetään keskuksen lisämaksun luomisessa.
author: Weijiesa
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TMSCarrierAccessorial,TMSAccessorialMaster, TMSHubAccessorial
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: weijiesa
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1ae7580e0c2a2f776512a7cf4c378266f1a878e9
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/03/2022
ms.locfileid: "8672623"
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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]