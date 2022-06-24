---
title: Luo tuotenumeroiden nimikkeistö esimääritetyille tuotevarianteille
description: Tässä artikkelissa kuvataan, miten tuotenumeroiden nimikkeistö määritetään esimääritetyille tuotevarianteille ja miten se voidaan liittää asianmukaiseen tuotedimensioryhmään.
author: t-benebo
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductDimensionGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e77c8eabe1657f7fbfef71747627207dccff3b60
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8887309"
---
# <a name="create-a-product-number-nomenclature-for-predefined-product-variants"></a>Luo tuotenumeroiden nimikkeistö esimääritetyille tuotevarianteille

[!include [banner](../../includes/banner.md)]

Tässä artikkelissa kuvataan, miten tuotenumeroiden nimikkeistö määritetään esimääritetyille tuotevarianteille ja miten se voidaan liittää asianmukaiseen tuotedimensioryhmään. Tämän menettelyn luomisessa käytetty esittely-yritys on USMF. Uuden tuotenumeroiden nimikkeistö on määritetty värin ja koon tuotedimensioryhmään. Tuotesuunnittelija tekee yleensä tämän tehtävän.


## <a name="create-a-product-number-nomenclature"></a>Tuotenumeroiden nimikkeistön luominen

1. Valitse **Tuotetietojen hallinta \> Asetukset \> Tuotenimikkeistö**.
1. Valitse **Uusi**.
1. Kirjoita **Nimi**-kenttään nimikkeistön nimi, jolla kohteena olevan tuotedimensioryhmän tunnistaa, esimerkiksi `ColorSize`.
1. Kirjoita **Kuvaus**-kenttään arvo.
1. Valitse **Lisää**.
1. Valitse **Päätuotteen numero**.
1. Valitse **Lisää**.
1. Valitse **Tekstivakio**.
1. Kirjoita arvo **Teksti**-kenttään.
1. Valitse **Lisää**.
1. Valitse **Väri**.
1. Valitse **Lisää**.
1. Valitse **Tekstivakio**.
1. Kirjoita arvo **Teksti**-kenttään.
1. Valitse **Lisää**.
1. Valitse **Koko**.
1. Sulje sivu.

## <a name="assign-the-nomenclature-to-a-product-master"></a>Nimikkeistön määrittäminen päätuotteelle

1. Valitse **Tuotedimensioryhmät**.
2. Valitse **SizeCol-tuotedimensioryhmä**.
3. Valitse **Muokkaa**.
4. Valitse **Käytä nimikkeistöä** -kentässä **Kyllä**.
5. Syötä tai valitse arvo **Tuotevariantin numeron nimikkeistö** -kentässä.
6. Sulje sivu.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]