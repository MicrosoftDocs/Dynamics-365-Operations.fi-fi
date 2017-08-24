--- 
title: "Luo tuotenumero esimääritetyille tuotevarianteille"
description: "Tässä oppaassa kuvataan, miten tuotenumeroiden nimikkeistö määritetään esimääritetyille tuotevarianteille ja miten se voidaan liittää asianmukaiseen tuotedimensioryhmään."
author: BibiSp
manager: AnnBe
ms.date: 09/26/2016
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
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: f14ee57564ad70bb7f28cd9274fc97d07974ec32
ms.contentlocale: fi-fi
ms.lasthandoff: 07/28/2017

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


