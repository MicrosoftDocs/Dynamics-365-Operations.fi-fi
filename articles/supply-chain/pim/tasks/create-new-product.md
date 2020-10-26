---
title: Luo uusi tuote
description: Tässä aiheessa kuvataan, kuinka uusi jaettu tuote luodaan.
author: ShylaThompson
manager: tfehr
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductInventoryDimensionGroups
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2a4745fe4fc44f85bcfd388ee573f5a6d0cd8519
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/10/2020
ms.locfileid: "3986165"
---
# <a name="create-a-new-product"></a>Luo uusi tuote

[!include [banner](../../includes/banner.md)]

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

