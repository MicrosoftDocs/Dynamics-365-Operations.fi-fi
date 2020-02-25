---
title: Määritä jatkuvuuden aikataulut
description: Tässä ohjeaiheessa neuvotaan jatkuvuusohjelman määrittäminen (toiselta nimeltään toistuvat tilaukset).
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MCRContinuitySchedule, EcoResProductDetailsExtended
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a438656730863f345080bc99fef24cfff724f528
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022382"
---
# <a name="define-continuity-schedules"></a>Määritä jatkuvuuden aikataulut

[!include[task guide banner](../includes/task-guide-banner.md)]

Tässä ohjeaiheessa neuvotaan jatkuvuusohjelman määrittäminen (toiselta nimeltään toistuvat tilaukset). Aiheessa käytetään esittelytietojen USRT-yritystä.


## <a name="create-continuity-program"></a>Luo jatkuvuusohjelma
1. Siirry kohtaan Retail ja Commerce > Jatkuvuus > Jatkuvuusohjelmat.
2. Valitse Uusi.
3. Kirjoita Aikataulun tunnus -kenttään jatkuvuusaikataulun tunnus.
4. Valitse Tilauksen aloitus -kentässä Valitse 'Ensimmäinen tapahtuma'.
    * Jos asiakas tekee uuden jatkuvuusohjelman tilauksen, tuotteen toimitukselle on kaksi vaihtoehtoa: 1. Ensimmäinen tapahtuma: jatkuvuusohjelman ensimmäinen tuote toimitetaan.  2. Nykyinen tapahtuma: nykyinen tuote toimitetaan. Esimerkki: kolme kuukautta ohjelmaa tilanneet asiakkaat saavat ohjelman kolmannen tuotteen.  
5. Valitse Kyllä, jos haluat kehotteen tilauksen alkamispäivämäärästä.
6. Valitse Lisää rivi.
7. Anna Nimiketunnus-kenttään ensimmäisen tuotteen tunnus (0013).
8. Kirjoita "CP".
9. Anna päivämäärä, jona ensimmäinen tuote on tilattavissa.
10. Valitse Lisää rivi.
11. Kirjoita Nimiketunnus-kenttään 0014.
12. Poista Päivämäärävälin koodi -kentän arvon niin, että kenttä on tyhjä.
    * Poista päivämääräväli tätä toimintaohjetta varten. Päivämäärä määritetään kasvavana ensimmäisen nimikkeen aloituspäivämäärästä alkaen.  
13. Tähän kenttään syötetään väli, jona tuotteet toimitetaan. Anna arvoksi 30.
    * Kuukausittaisen ohjelman aikaväliksi täytetään 30 päivää.  
14. Valitse Lisää rivi.
15. Kirjoita Nimiketunnus-kenttään 0015.
16. Kirjoita "End".
17. Valitse Tallenna.

## <a name="assign-to-continuity-item"></a>Liitä jatkuvuusnimikkeeseen
1. Mene Tuotetietojen hallinta > Tuotteet > Vapautetut tuotteet.
2. Valitse nimike 0016.
    * Tässä menettelyssä valitaan nimiketunnus 0016. Tavallisesti luotaisiin vapautettu tuote, johon käytetään jatkuvuuden liiketoimintalogiikkaa silloin, kun se lisätään myyntitilaukseen puhelinkeskuksesta.  
3. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
4. Valitse Muokkaa.
5. Laajenna tai tiivistä Myydä-osa .
6. Syötä tähän kenttään jatkuvuusohjelma, jota nimike vastaa. Kirjoita aiemmin luotu aikataulun tunnus.
    * Kun tämä nimike myydään puhelinkeskuksessa, valitun jatkuvuusohjelman liiketoimintalogiikkaa sovelletaan nimikkeeseen.  
7. Valitse Tallenna.

