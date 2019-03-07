---
title: Tuotteen elinkaaren oletustilan luominen
description: Tässä menettelyssä kerrotaan, miten tuotteen elinkaaren oletustila luodaan sekä miten oletustila liitetään julkaistuihin tuotteisiin.
author: cvocph
manager: AnnBe
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6e7e637157ee06a3d07a1a9c5da71295eb75b424
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "310826"
---
# <a name="create-a-default-product-lifecycle-state"></a>Tuotteen elinkaaren oletustilan luominen

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tässä menettelyssä kerrotaan, miten tuotteen elinkaaren oletustila luodaan sekä miten oletustila liitetään julkaistuihin tuotteisiin.


## <a name="create-a-default-lifecycle-state"></a>Elinkaaren oletustilan luominen
1. Valitse Tuotetietojen hallinta > Asetukset > Tuotteen elinkaaren tila.
2. Valitse Uusi.
3. Kirjoita arvo Tila-kenttään.
4. Valitse Oletusarvo vapautettaessa yritykselle -kentässä Kyllä.
5. Kirjoita arvo Kuvaus-kenttään.
6. Valitse On käytettävissä suunnitteluun -kentässä Ei.

> [!NOTE]
> Jos uutta vapautettua tuotetta ei sisällytetä pääsuunnitteluun, valitse Ei. Jos se sisällytetään pääsuunnitteluun, älä muuta ohjausobjektin oletusarvoa Kyllä.  

## <a name="create-a-new-released-product"></a>Uuden julkaistun tuotteen luominen
1. Sulje sivu.
2. Mene Tuotetietojen hallinta > Tuotteet > Vapautetut tuotteet.
3. Valitse Uusi.
4. Kirjoita arvo Tuotenumero-kenttään.
5. Kirjoita arvo Tuotteen nimi -kenttään.
6. Kirjoita arvo Hakunimi-kenttään.
7. Syötä tai valitse arvo Nimikemalliryhmä-kentässä.
8. Anna tai valitse arvo Nimikeryhmä-kentässä.
9. Syötä tai valitse arvo Varastodimensioryhmä-kentässä.
10. Syötä tai valitse arvo Seurantadimensioryhmä-kentässä.
11. Valitse OK.

> [!NOTE]
> Tuotteen elinkaaren oletustila on yleinen määritys.  

## <a name="change-the-product-to-an-active-state"></a>Tuotteen tilan muuttaminen aktiiviseksi
1. Syötä tai valitse arvo Tuotteen elinkaaren tila -kenttään.

> [!NOTE]
> Oletetaan, että olet määrittänyt aktiivisen tilan. Voit nyt valita aktiivisen tilan ja sallia tuotteen käyttämisen pääsuunnittelussa ja tuoterakennetason laskennassa. Luonnollisesti tämä kannattaa tehdä vain, jos kaikki yhdenmukaisen suunnittelun vaatimat tuotetiedot on määritetty.  

