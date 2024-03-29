---
title: Varaston varastotasojen oikaisu (perusvarastointi)
description: Tässä menettelyssä selvitetään varaston oikaisun kirjauskansion luonti- ja kirjausprosessi, jolla voidaan oikaista varastossa olevien tuotteiden varastotasoja.
author: yufeihuang
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventJournalLossProfit, InventJournalCreate, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 02458d588c9925a1f4cb9afeada793dfc55a2071
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/29/2021
ms.locfileid: "7573822"
---
# <a name="adjust-stock-levels-in-the-warehouse-basic-warehousing"></a>Varaston varastotasojen oikaisu (perusvarastointi)

[!include [banner](../../includes/banner.md)]

Tässä menettelyssä selvitetään varaston oikaisun kirjauskansion luonti- ja kirjausprosessi, jolla voidaan oikaista varastossa olevien tuotteiden varastotasoja. Ennen aloittamista varasto-oikaisuille on oltava määritettynä varaston oikaisun kirjauskansio. Voit käydä tämän menettelyn läpi emotietojen yrityksen USMF avulla tai käyttää omia tietojasi. Yleensä varastotyöntekijä tekee nämä tehtävät.


## <a name="create-an-inventory-adjustment-journal"></a>Luo varaston oikaisun kirjauskansio
1. Valitse Inventoinnin- ja varastonhallinta > Kirjauskansioviennit > Nimikkeet > Varaston oikaisu.
2. Valitse Uusi.
3. Avaa haku valitsemalla Nimi-kentässä avattavan valikon painike.
4. Valitse luettelosta varaston oikaisun kirjauskansio, jota haluat käyttää.
    * Joidenkin kenttien tiedot voidaan lisätä valitsemasi varaston oikaisun kirjauskansion asetusten perusteella.  
5. Valitse OK.

## <a name="create-journal-lines"></a>Tämän kirjauskansion rivit
1. Valitse Uusi.
2. Merkitse luettelossa nimiketunnuskenttä.
3. Valitse Nimiketunnus-kentässä nimike. Jos käytät USMF-yrityksen demotietoja, kirjoita D0001.
4. Avaa haku napsauttamalla Toimipaikka-kentässä avattavan valikon painiketta.
5. Valitse luettelosta toimipaikka.
6. Avaa haku valitsemalla Varasto-kentässä avattavan valikon painike.
7. Valitse luettelosta varasto.
    * Jos olet valinnut nimikkeen, jossa sijainti on pakollinen dimensio, sijainti on määritettävä tässä.  
8. Kirjoita numero Määrä-kenttään.
    * Kustannushinnan kenttä määrittää varastovastaanottojen yksikkökohtaisen kustannuksen. Jos nimiketunnukselle ei ole määritetty kustannusta tai haluat muuttaa sitä manuaalisesti, voit tehdä sen tässä.  

## <a name="validate-and-post-the-inventory-adjustment-journal"></a>Vahvista ja kirjaa varaston oikaisun kirjauskansio
1. Valitse Vahvista.
2. Valitse OK.
3. Valitse Kirjaa.
    * Kun kirjaat tämäntyyppisen kirjauskansion, järjestelmä kirjaa varastovastaanoton tai varasto-oton, muuttaa varastotason ja -arvon sekä luo kirjanpitotapahtumat.  
4. Valitse OK.
5. Sulje lomake.
6. Sulje sivu.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]