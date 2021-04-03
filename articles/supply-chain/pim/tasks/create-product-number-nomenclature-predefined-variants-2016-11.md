---
title: Luo tuotenumeroiden nimikkeistö esimääritetyille tuotevarianteille
description: Tässä ohjeessa kuvataan, miten tuotenumeroiden nimikkeistö määritetään esimääritetyille tuotevarianteille ja miten se voidaan liittää asianmukaiseen tuotedimensioryhmään.
author: ShylaThompson
manager: tfehr
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductDimensionGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6a4ad70a87cd8c6cab2e9853f4f6c52f574d318a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5257411"
---
# <a name="create-a-product-number-nomenclature-for-predefined-product-variants"></a>Luo tuotenumeroiden nimikkeistö esimääritetyille tuotevarianteille

[!include [banner](../../includes/banner.md)]

Tässä ohjeessa kuvataan, miten tuotenumeroiden nimikkeistö määritetään esimääritetyille tuotevarianteille ja miten se voidaan liittää asianmukaiseen tuotedimensioryhmään. Tämän menettelyn luomisessa käytetty esittely-yritys on USMF. Uuden tuotenumeroiden nimikkeistö on määritetty värin ja koon tuotedimensioryhmään. Tuotesuunnittelija tekee yleensä tämän tehtävän.


## <a name="create-a-product-number-nomenclature"></a>Tuotenumeroiden nimikkeistön luominen
1. Valitse **Tuotevarianttimallin määritys**.
2. Valitse **Tuotenumeron nimikkeistö**.
3. Valitse **Uusi**.
4. Kirjoita **Nimi**-kenttään nimikkeistön nimi, jolla kohteena olevan tuotedimensioryhmän tunnistaa, esimerkiksi `ColorSize`.
5. Kirjoita **Kuvaus**-kenttään arvo.
6. Valitse **Lisää**.
7. Valitse **Päätuotteen numero**.
8. Valitse **Lisää**.
9. Valitse **Tekstivakio**.
10. Kirjoita arvo **Teksti**-kenttään.
11. Valitse **Lisää**.
12. Valitse **Väri**.
13. Valitse **Lisää**.
14. Valitse **Tekstivakio**.
15. Kirjoita arvo **Teksti**-kenttään.
16. Valitse **Lisää**.
17. Valitse **Koko**.
18. Sulje sivu.

## <a name="assign-the-nomenclature-to-a-product-master"></a>Nimikkeistön määrittäminen päätuotteelle
1. Valitse **Tuotedimensioryhmät**.
2. Valitse **SizeCol-tuotedimensioryhmä**.
3. Valitse **Muokkaa**.
4. Valitse **Käytä nimikkeistöä** -kentässä **Kyllä**.
5. Syötä tai valitse arvo **Tuotevariantin numeron nimikkeistö** -kentässä.
6. Sulje sivu.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]