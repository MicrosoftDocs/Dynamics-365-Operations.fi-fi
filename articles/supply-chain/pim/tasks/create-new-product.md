---
title: Luo uusi tuote
description: Tässä tehtävässä esitellään uuden jaetun tuotteen luominen.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductInventoryDimensionGroups
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7a603d89749242a4c6039ab83da286ec6ab727d8
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "328536"
---
# <a name="create-a-new-product"></a>Luo uusi tuote

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tässä tehtävässä esitellään uuden jaetun tuotteen luominen. Tehtävän suorittaa yleensä tuotesuunnittelija. Tämän tehtävän luomisessa käytetty esittely-yritys on USMF.

1. Valitse Tuotetietojen hallinta > Tuotteet > Tuotteet.

## <a name="create-a-product"></a>Luo tuote
1. Valitse Uusi.
2. Kirjoita arvo Tuotenumero-kenttään.
    * Jos numerosarjaa ei ole määritetty tuotetunnukselle, se on syötettävä manuaalisesti.  
3. Kirjoita arvo Tuotteen nimi -kenttään.
    * Tuotenimen oletusarvoksi määritetään hakunimi. Arvoa voi muuttaa tarvittaessa.  
4. Valitse OK.

## <a name="set-up-dimension-groups"></a>Määritä dimensioryhmät
1. Avaa valintaikkunalomake valitsemalla Dimensioryhmät.
2. Syötä tai valitse arvo Varastodimensioryhmä-kentässä.
    * Varastodimensioryhmä määrää, mitä varastodimensioita kullekin tuotteen tapahtumalle on syötettävä, ja miten sitä seurataan varastossa.  
3. Syötä tai valitse arvo Seurantadimensioryhmä-kentässä.
    * Seurantadimensioryhmä määrää, mitä seurantadimensioita kullekin tuotteen tapahtumalle on syötettävä, ja miten sitä käsitellään varastossa.  
4. Valitse OK.

