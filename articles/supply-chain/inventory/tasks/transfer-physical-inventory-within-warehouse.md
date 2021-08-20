---
title: Fyysisen varaston siirtäminen varastossa
description: Tässä menettelyssä käsitellään varastosiirtokirjauskansion luominen ja kirjaaminen, jotta nimikkeen siirto varastosijainnista toiseen voidaan rekisteröidä.
author: MarkusFogelberg
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventJournalTransfer, InventJournalCreate, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9557187d0c9f322729bbdd707525e18b54df34cd27aeed09adf4820e3c3d0f3d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6754008"
---
# <a name="transfer-physical-inventory-within-the-warehouse"></a>Fyysisen varaston siirtäminen varastossa

[!include [banner](../../includes/banner.md)]

Tässä menettelyssä käsitellään varastosiirtokirjauskansion luominen ja kirjaaminen, jotta nimikkeen siirto varastosijainnista toiseen voidaan rekisteröidä. Ennen aloittamista varastosiirroille on oltava määritettynä varastokirjauskansio. Voit käyttää menettelyssä USMF-yrityksen demotiedoissa näytettyjä esimerkkiarvoja tai omia tietojasi, jos sinulla on määritettyjä tuotteita ja sijainteja. Yleensä varastotyöntekijä tekee nämä tehtävät.


## <a name="create-an-inventory-transfer-journal"></a>Luo varastosiirtokirjauskansio
1. Siirry **siirtymisruudussa** kohtaan **Varastonhallinta > Kirjauskansioviennit > Nimikkeet > Siirto**.
2. Valitse **Uusi**.
3. Anna tai valitse arvo **Nimi**-kentässä.
4. Valitse **OK**. Kunkin kirjauskansion rivin määrittämiseen on lähtö- ja kohdedimensioasetus. Ne ovat välttämättömiä tässä kirjauskansiotyypissä. Voit siirtää nimikkeitä sijainteihin eri säännöillä. Tässä esimerkissä nimike siirretään samassa varastossa rekisterikilvellä ohjatusta sijainnista sijaintiin, jota ei ohjata rekisterikilvellä.   

## <a name="create-journal-lines"></a>Luo kirjauskansion rivejä
1. Valitse **Kirjauskansion rivit** -pikavälilehdessä **Uusi**.
2. Syötä tai valitse arvo **Nimiketunnus**-kentässä. Jos käytössä on USMF, voit valita A0001.  
3. Anna tai valitse **Toimipaikasta**-kentässä arvo. Jos käytössä on USMF, voit valita 2.  
4. Anna tai valitse **Toimipaikkaan**-kentässä arvo. Jos käytössä on USMF, voit valita 2.  
5. Anna tai valitse **Varastosta**-kentässä arvo. Jos käytössä on USMF, voit valita 24.  
6. Anna tai valitse **Varastoon**-kentässä arvo. Jos käytössä on USMF, voit valita 24.  
7. Anna tai valitse **Lähtösijainti** -kentässä arvo. Jos käytössä on USMF, voit valita FL-001.  
8. Anna tai valitse **Kohdesijainti**-kentässä arvo. Jos käytössä on USMF, voit valita BULK-001.  
9. Anna **Määrä**-kentässä numero.
10. Valitse **Rivin tiedot** -pikavälilehdessä **Varastodimensiot** -välilehti.
11. Kirjoita tai valitse arvo **Varastodimensioista**-kohdan **Rekisterikilpi**-kenttään. Jos käytössä on USMF, voit valita 24.  
12. Valitse **Tallenna**.

## <a name="post-the-inventory-transfer-journal"></a>Kirjaa varastosiirtokirjauskansio
1. Valitse **toimintoruudussa** **Kirjaa**.
2. Valitse **OK**.

## <a name="view-inventory-transactions"></a>Näytä varastotapahtumat
1. Valitse **Varasto**.
2. Valitse **Tapahtumat**. Tässä on näkyvissä tapahtumat, jotka luotiin kirjauskansioon kirjattaessa.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]