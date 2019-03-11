---
title: Luo tuotenumeroiden nimikkeistö esimääritetyille tuotevarianteille
description: Tässä oppaassa kuvataan, miten tuotenumeroiden nimikkeistö määritetään esimääritetyille tuotevarianteille ja miten se voidaan liittää asianmukaiseen tuotedimensioryhmään.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductDimensionGroup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4b49e96677b94d5f669ea41861f64e62e118938c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "364876"
---
# <a name="create-a-product-number-nomenclature-for-predefined-product-variants"></a>Luo tuotenumeroiden nimikkeistö esimääritetyille tuotevarianteille

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tässä oppaassa kuvataan, miten tuotenumeroiden nimikkeistö määritetään esimääritetyille tuotevarianteille ja miten se voidaan liittää asianmukaiseen tuotedimensioryhmään. Tämän menettelyn luomisessa käytetty esittely-yritys on USMF. Uuden tuotenumeroiden nimikkeistö on määritetty värin ja koon tuotedimensioryhmään. Tuotesuunnittelija tekee yleensä tämän tehtävän.


## <a name="create-a-product-number-nomenclature"></a>Tuotenumeroiden nimikkeistön luominen
1. Valitse Tuotevarianttimallin määritys.
2. Valitse Tuotenimikkeistö.
3. Valitse Uusi.
4. Kirjoita nimikenttään nimikkeistön nimi, jolla kohteena olevan tuotedimensioryhmän tunnistaa, esimerkiksi ColorSize.
5. Kirjoita arvo Kuvaus-kenttään.
6. ValitseLisää.
7. Valitse Päätuotteen numero.
8. ValitseLisää.
9. Valitse Tekstivakio.
10. Kirjoita arvo Teksti-kenttään.
11. ValitseLisää.
12. Valitse Väri.
13. ValitseLisää.
14. Valitse Tekstivakio.
15. Kirjoita arvo Teksti-kenttään.
16. ValitseLisää.
17. Valitse Koko.
18. Sulje sivu.

## <a name="assign-the-nomenclature-to-a-product-master"></a>Nimikkeistön määrittäminen päätuotteelle
1. Valitse Tuotedimensioryhmät.
2. Valitse SizeCol-tuotedimensioryhmä.
3. Valitse Muokkaa.
4. Valitse Käytä nimikkeistöä -kentässä Kyllä.
5. Syötä tai valitse arvo Tuotevariantin numeron nimikkeistö -kentässä.
6. Sulje sivu.

