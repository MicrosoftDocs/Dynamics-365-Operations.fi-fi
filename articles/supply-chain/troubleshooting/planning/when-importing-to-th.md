---
title: Näyttöön tule kehote tallentaa nimikkeen kattavuusasetukset, vaikka et olisi tehnyt muutoksia
description: Näyttöön tule kehote tallentaa nimikkeen kattavuusasetukset, vaikka et olisi tehnyt muutoksia.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: DataManagementWorkspace_
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: angarmas
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 3dfa974740420433af1e1b37630b22509510c91b
ms.sourcegitcommit: 3c15a26e9708adc9a75082dc551f0a3a0a7d89f4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/17/2021
ms.locfileid: "6049464"
---
# <a name="youre-prompted-to-save-item-coverage-settings-even-though-you-made-no-changes"></a>Näyttöön tule kehote tallentaa nimikkeen kattavuusasetukset, vaikka et olisi tehnyt muutoksia

Tietopankin numero: 4615588

## <a name="symptoms"></a>Oireet

Joissakin tilanteissa näyttöön saattaa tulla seuraava sanoma, kun **nimikkeen kattavuus** -sivu avataan sen jälkeen, kun nimikkeet on tuotu *nimikkeen kattavuuden V2* -yksikön kautta:

> Haluatko tallentaa muutokset ennen sulkemista?

Saat tämän viestin, vaikka et ole tehnyt muutoksia.

## <a name="resolution"></a>Ratkaisu

**Nimikkeen kattavuus** -sivulla on monimutkainen oletuslogiikka, joka saattaa aiheuttaa sen, että viesti näkyy sen jälkeen, kun tietokantaan on tehty suoria muutoksia, esimerkiksi yksikön tuonnin kautta. `AREGENERALSETTINGSOVERRIDDEN`-yksikkökentän arvoksi määritetään esimerkiksi *Ei*, mutta tuot tiedoston, joka sisältää uudet tai muokatut arvot esimerkiksi `PRODUCTCOVERAGEGROUPID`- ja/tai `VENDORACCOUNTNUMBER`-kentissä. Tässä tapauksessa, koska `AREGENERALSETTINGSOVERRIDDEN`-kentän arvoksi on määritetty *Ei*, arvot poistetaan automaattisesti kentistä, kun **nimikkeen kattavuus** -sivu avataan ensimmäistä kertaa tuonnin jälkeen. Jos tallennat muutokset sanomaruudun kehotteen mukaan, ne tallennetaan tietokantaan. Muussa tapauksessa saat saman viestin, kun seuraavan kerran avaat sivun.

Jos haluat estää tämän toiminnan mutta myös sisällyttää arvoja, kuten `PRODUCTCOVERAGEGROUPID`entiteetin tuonnin kautta, valitse `AREGENERALSETTINGSOVERRIDDEN`-arvoksi *Kyllä*, kun tuot tietoja.
