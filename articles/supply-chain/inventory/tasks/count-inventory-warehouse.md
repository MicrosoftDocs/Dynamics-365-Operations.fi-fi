---
title: Varaston kokonaismäärän laskeminen
description: Tässä artikkelissa kuvataan varaston inventointikirjauskansion luonti- ja kirjausprosessi, jolla voidaan inventoida tietty nimike varastosijainnissa.
author: yufeihuang
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventJournalCount, InventJournalCreate, HcmWorkerLookUp, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7c8712b88867dc4be48bbdb4b905993e3ccbc73f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8870634"
---
# <a name="count-inventory-in-a-warehouse"></a>Varaston kokonaismäärän laskeminen

[!include [banner](../../includes/banner.md)]

Tässä artikkelissa kuvataan varaston inventointikirjauskansion luonti- ja kirjausprosessi, jolla voidaan inventoida tietty nimike varastosijainnissa. Menettely koskee Inventoinnin- ja varastonhallinta -moduulin varastoinnin perustoimintoja. Se ei koske Varastonhallinta-moduulin varastointitoimintoja. Voit käydä tämän menettelyn läpi emotietojen yrityksen USMF avulla tai käyttää omia tietojasi. Jos käytät omia tietoja, varmista, että olet määrittänyt tuotteita ja sijainteja ja että olet luonut inventointikirjauskansioille varastokirjauskansion. Varastoinventoinnin suorittaa tavallisesti varastotyöntekijä.


## <a name="create-an-inventory-counting-journal"></a>Luo varaston inventointikirjauskansio
1. Valitse **Siirtymisruutu > Moduulit > Inventoinnin- ja varastonhallinta > Kirjauskansioviennit > Inventointi > Inventointi**.
2. Valitse **Uusi**.
3. Valitse **Nimi**-kentässä avattavasta luettelosta varastoinventoinnin kirjauskansion nimi, jota haluat käyttää. Joidenkin kenttien tiedot voidaan lisätä valitsemasi varaston inventointikirjauskansion asetusten perusteella.  
4. Avaa haku valitsemalla **Työntekijä**-kentässä avattavan valikon painiketta.
5. **Valitse** luettelosta työntekijä, jota haluat käyttää.
6. Valitse **OK**.

## <a name="create-journal-lines"></a>Luo kirjauskansion rivejä
1. Valitse **Uusi**.
2. Valitse **Nimiketunnus**-kentässä avattavasta valikosta haluttu tietue. Jos käytät USMF-yrityksen demotietoja, valitse **A0001**.  
3. Valitse **Toimipaikka**-kentässä avattavasta valikosta haluttu tietue. Jos käytät USMF-yrityksen demotietoja, valitse toimipaikka **2**.
4. Valitse **Varasto**-kentässä avattavasta valikosta haluttu tietue. Jos käytät USMF-yrityksen demotietoja, valitse varasto **24**.  
5. Valitse **Sijainti**-kentässä avattavasta valikosta haluttu tietue. Jos käytät USMF-yrityksen demotietoja, valitse sijainti **BULK-001**.  
6. Lisää Inventoitu-kenttään numero. Jos annat inventoitu määrä, joka poikkeaa **Varastosaldo**-kentässä olevasta numerosta, **Määrä**-kenttä päivitetään näyttämään ristiriita.  
7. Valitse **Tallenna**.

## <a name="post-the-inventory-counting-journal"></a>Kirjaa varaston inventointikirjauskansio
1. Valitse **Kirjaa**. Jos varaston inventointikirjauskansiota kirjatessa kirjataan varastovastaanoton **Varastosaldo**-kentässä tai varasto-otossa olevasta määrästä eroava inventoitu määrä, varastotaso ja arvo muuttuvat ja kirjanpitotapahtumat muodostetaan.
2. Valitse **OK**.

## <a name="view-inventory-transactions"></a>Näytä varastotapahtumat
1. Valitse **Varasto**.
2. Valitse **Tapahtumat**. Tässä näkyvät kaikki liittyvät tapahtumat, jotka luodaan, kun varaston inventointikirjauskansioon kirjataan.   



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]