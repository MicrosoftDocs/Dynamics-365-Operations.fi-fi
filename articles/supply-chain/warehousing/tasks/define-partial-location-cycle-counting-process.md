---
title: Määritä sijainnin osittainen inventointiprosessi
description: Kun inventointisuunnitelmia käytetään inventointityön luomisessa, voit ohjata toteutuneita inventointitoimintoja pyytämällä vain tiettyjen tuotteiden ja tuotevarianttien inventointia sijainnin koko käytettävissä olevan varaston inventoinnin sijaan.
author: ShylaThompson
manager: tfehr
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItemCycleCount, WHSCycleCountPlan, WHSCycleCountPlanListPage, WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0778cc7c1703dcfd5ea77979aafc99f4f040830d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977135"
---
# <a name="define-partial-location-cycle-counting-process"></a>Määritä sijainnin osittainen inventointiprosessi 

[!include [banner](../../includes/banner.md)]

Kun inventointisuunnitelmia käytetään inventointityön luomisessa, voit ohjata toteutuneita inventointitoimintoja pyytämällä vain tiettyjen tuotteiden ja tuotevarianttien inventointia sijainnin koko käytettävissä olevan varaston inventoinnin sijaan. Tiettyjen tuotteiden suodattaminen auttaa varastopäällikköä pienentämään tarkistuksen yleiskustannuksia, estämään konsolidointivirheitä ja säästämään aikaa. Yleensä nämä määritystehtävät suorittaa varastopäällikkö. Voit käyttää tässä menettelyssä USMF-yrityksen demotietoja tai käyttää omia tietojasi.


## <a name="create-a-cycle-counting-work-template"></a>Inventointityömallin luominen
1. Valitse Varastonhallinta > Asetukset > Työ > Työmallit.
2. Valitse Työtilauksen tyyppi -kentässä Inventointi.
3. Valitse Uusi.
4. Syötä Järjestysnumero-kenttään numero.
    * Lajittelujärjestys on pienimmästä numerosta suurimpaan. Arvon on oltava suurempi kuin 0 (nolla).  
5. Merkitse valittu rivi luettelossa.
6. Kirjoita Työmalli-kenttään arvo.
7. Kirjoita Työmallin kuvaus -kenttään arvo.
8. Anna tai valitse Työpoolin tunnus-kentän arvo.
9. Syötä numero Työn prioriteetti -kenttään.
10. Valitse Tallenna.
11. Valitse Uusi.
12. Merkitse valittu rivi luettelossa.
13. Valitse Työtyyppi-kentässä Inventointi.
14. Syötä tai valitse arvo Työluokan tunnus -kenttään.
15. Valitse Tallenna.
16. Valitse Työrivin tauot.
17. Valitse Uusi.
18. Syötä Järjestysnumero-kenttään numero.
    * Lajittelujärjestys on pienimmästä numerosta suurimpaan. Arvon on oltava suurempi kuin 0 (nolla).  
19. Valitse Tallenna.
20. Sulje sivu.
21. Sulje sivu.

## <a name="create-a-cycle-counting-plan"></a>Inventointisuunnitelman luominen
1. Valitse Varastonhallinta > Asetukset > Inventointi > Inventointisuunnitelmat.
2. Valitse Uusi.
3. Kirjoita Inventointisuunnitelman tunnus -kenttään arvo.
4. Kirjoita Kuvaus-kenttään arvo.
5. Lisää Inventointien enimmäismäärä -kenttään luku.
6. Anna tai valitse Työmalli-kentän arvo.
7. Valitse Uusi.
8. Syötä Järjestysnumero-kenttään numero.
    * Lajittelujärjestys on pienimmästä numerosta suurimpaan. Arvon on oltava suurempi kuin 0 (nolla).  
9. Kirjoita arvo Kuvaus-kenttään.
10. Valitse Tallenna.
11. Valitse Määritä tuotekysely.
12. Merkitse valittu rivi luettelossa.
13. Syötä tai valitse arvo Ehdot-kenttään.
14. Valitse OK.
15. Sulje sivu.

