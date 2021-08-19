---
title: Tuotteen elinkaaren oletustilan luominen
description: Tässä menettelyssä kerrotaan, miten tuotteen elinkaaren oletustila luodaan sekä miten oletustila liitetään julkaistuihin tuotteisiin.
author: cvocph
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 470a8e0d2bbec53c8b9e24ca63bce72eca1886715e1c1d439d873a7f4fc62bea
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6728552"
---
# <a name="create-a-default-product-lifecycle-state"></a>Tuotteen elinkaaren oletustilan luominen

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]