--- 
title: "Luo tuotenumero esimääritetyille tuotevarianteille"
description: "Tässä oppaassa kuvataan, miten tuotenumeroiden nimikkeistö määritetään esimääritetyille tuotevarianteille ja miten se voidaan liittää asianmukaiseen tuotedimensioryhmään."
author: BibiSp
manager: AnnBe
ms.date: 11/03/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 3a1bfd4bd5f396c05277159ac112eaa8197d5818
ms.openlocfilehash: c423aab341ddad9383c4c95b9dbb63c9875c99ef
ms.contentlocale: fi-fi
ms.lasthandoff: 11/03/2017

---
# <a name="create-a-product-number-for-predefined-product-variants"></a>Luo tuotenumero esimääritetyille tuotevarianteille

[!include[task guide banner](../../includes/task-guide-banner.md)]

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


