---
title: Luo ja ylläpidä varastoesto
description: Tässä artikkelissa kerrotaan, miten fyysisen käytettävissä olevan varaston varaaminen estetään muilta lähteviltä asiakirjoilta varastoeston avulla.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventBlocking, InventItemIdLookupSimple, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ba95b689bedfc76598dfa81548a074f4fb7c833a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8859340"
---
# <a name="create-and-maintain-an-inventory-blocking"></a>Luo ja ylläpidä varastoesto

[!include [banner](../../includes/banner.md)]

Tässä artikkelissa kerrotaan, miten fyysisen käytettävissä olevan varaston varaaminen estetään muilta lähteviltä asiakirjoilta varastoeston avulla. Aloita tämän artikkelin menettelyt vasta, kun käytettävissä on fyysistä käytettävissä olevaa varastoa omaava nimike.

## <a name="block-inventory"></a>Varastoesto

Noudattamalla näitä ohjeita voit luoda varaston estotietueen varaston eston mahdollistamiseksi.

1. Valitse **Varastonhallinta \> Kausittaiset tehtävät \> Varastoesto**.
1. Valitse toimintoruudussa **Uusi**.
1. Uuden estotietueen otsikossa määritä **Nimiketunnus**-kenttä estettävään nimikkeeseen ja kirjoita kuvaus.
1. Kirjoita **Yleiset**-pikavälilehden **Määrä**-kenttään estettävien nimikkeiden määrä.
1. Määritä **Varastodimensiot**-pikavälilehdessä paikka ja varasto, jossa estettävät nimikkeet sijaitsevat tällä hetkellä.
1. Valitse toimintoruudussa **Tallenna**.

## <a name="update-the-conditions-of-the-inventory-blocking"></a>Varastoeston ehtojen päivittäminen

Päivitä varaston estotietue noudattamalla seuraavia vaiheita.

1. Valitse **Varastonhallinta \> Kausittaiset tehtävät \> Varastoesto**.
1. Valitse luetteloruudusta asianmukainen estotietue.
1. Muokkaa tietuetta tarvittaessa. Esimerkiksi ehkä haluat muuttaa **Odotettu päivämäärä** -kentän arvoa ja määrittää, milloin estetyn varaston odotetaan olevan varattavissa. Jos **Oletetut vastaanotot** -asetus on valittuna, oletetussa tapahtumassa näkyy päivämäärä. (**Oletetut vastaanotot** -asetus on oletusarvon mukaan valittuna, kun estotietue luodaan manuaalisesti.)
1. Valitse toimintoruudussa **Tallenna**.

## <a name="unblock-inventory"></a>Poista varaston esto

Noudattamalla näitä ohjeita voit poistaa varaston estotietueen varaston eston poiston mahdollistamiseksi.

1. Valitse **Varastonhallinta \> Kausittaiset tehtävät \> Varastoesto**.
1. Valitse luetteloruudusta asianmukainen estotietue.
1. Valitse toimintoruudussa **Poista**.
1. Järjestelmä pyytää vahvistamaan toiminnon. Jatka valitsemalla **Kyllä**.
1. Sulje sivu.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
