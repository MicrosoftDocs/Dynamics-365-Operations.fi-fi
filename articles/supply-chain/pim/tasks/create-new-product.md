---
title: Luo uusi tuote
description: Tässä aiheessa kuvataan, kuinka uusi jaettu tuote luodaan.
author: ShylaThompson
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductInventoryDimensionGroups
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 722414eee1e738e1438bbb40dbd9b8ca606f9245
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844798"
---
# <a name="create-a-new-product"></a>Luo uusi tuote

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tässä aiheessa kuvataan, kuinka uusi jaettu tuote luodaan. Tehtävän suorittaa yleensä tuotesuunnittelija. Tämän tehtävän luomisessa käytetty esittely-yritys on USMF.


## <a name="create-a-product"></a>Luo tuote
1. Valitse siirtymisruudussa **Moduulit > Tuotetietojen hallinta > Tuotteet > Tuotteet**.
2. Valitse **Uusi**.
3. Kirjoita arvo **Tuotenumero**-kenttään. Jos numerosarjaa ei ole määritetty tuotetunnukselle, se on syötettävä manuaalisesti.  
4. Kirjoita arvo **Tuotteen nimi**-kenttään. Tuotenimen oletusarvoksi määritetään hakunimi. Arvoa voi muuttaa tarvittaessa.  
5. Valitse **OK**.

## <a name="set-up-dimension-groups"></a>Määritä dimensioryhmät
1. Avaa valintaikkunalomake valitsemalla **Dimensioryhmät**.
2. Syötä tai valitse arvo **Varastodimensioryhmä**-kentässä. Varastodimensioryhmä määrää, mitä varastodimensioita kullekin tuotteen tapahtumalle on syötettävä, ja miten sitä seurataan varastossa.  
3. Syötä tai valitse arvo **Seurantadimensioryhmä**-kentässä. Seurantadimensioryhmä määrää, mitä seurantadimensioita kullekin tuotteen tapahtumalle on syötettävä, ja miten sitä käsitellään varastossa.  
4. Valitse **OK**.

