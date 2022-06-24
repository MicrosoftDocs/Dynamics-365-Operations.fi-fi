---
title: Konsernin sisäisen myyntitilauksen luominen sisäiseen käyttöön
description: Tässä artikkelissa käsitellään konsernin sisäisen myyntitilauksen luontia sisäistä käyttöä varten
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: a37b8ab1b3df10cdbd3bbb87410bc3dc70dc0ed0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8873518"
---
# <a name="create-an-intercompany-sales-order-for-internal-use"></a>Konsernin sisäisen myyntitilauksen luominen sisäiseen käyttöön

[!include [banner](../../includes/banner.md)]

Konsernin sisäinen myyntitilaus luodaan tyypillisesti automaattisesti konsernin sisäisen ostotilauksen perusteella. Konsernin sisäinen myyntitilaus voidaan luoda myös manuaalisesti, ja se puolestaan luo konsernin sisäisen ostotilauksen konsernin sisäisen asiakkaan yrityksessä.

![Konsernin sisäinen myyntiprosessi](media/intercompanyinternalsalesprocess.png)

## <a name="create-an-intercompany-sales-order-manually"></a>Konsernin sisäisen myyntitilauksen luominen manuaalisesti

Suorita nämä vaiheet yrityksessä B kuvassa esitetyllä tavalla.

1. Valitse **Myyntireskontra \> Myyntitilaukset \> Kaikki myyntitilaukset**.
1. Luo myyntitilaus valitsemalla toimintoruudussa **Myyntitilaus**.
1. Valitse asiakastili **Luo myyntitilaus** -sivulla. Varmista **Yleiset**-pikavälilehdessä, että **Konsernin sisäinen** -valintaruutu on valittu. Se ilmaisee, että valittu asiakas on konsernin sisäinen asiakas.
1. Anna tai muokkaa tietoja, valitse **OK** ja täytä sitten tilausrivit tavalliseen tapaan.

    **Toimitusosoite**-kentän arvo kopioidaan konsernin sisäisen myyntitilauksen otsikosta konsernin sisäisen ostotilauksen otsikkoon. **Nimikekentän**-kentän arvo tuotedimensiot mukaan lukien sekä **Toimituspäivä**- ja **Valuuttakoodi**-kenttien arvot kopioidaan konsernin sisäisen myyntitilauksen riveiltä konsernin sisäisen ostotilauksen riveille.

1. Liittyvää konsernin sisäistä ostotilausta voi tarkastella valitsemalla tilauksen otsikossa **Konsernin sisäinen**.
1. Konsernin sisäisen kaupan käytettävissä olevan varaston tietoja voi tarkastella valitsemalla tilausriveillä **Konsernin sisäinen**.

> [!TIP]
> Konsernin sisäisiä myyntitilauksia voi tarkastella **Konsernin sisäiset tilaukset**-sivulla.

> [!NOTE]
> Jos toiminta tapahtuu konsernin sisäisesti, **Poista tilaus laskutuksen jälkeen** -valintaruudun valinta kannattaa poistaa **Myyntireskontran parametrit** -sivulla. Muutoin liittyvä ostotilaus poistetaan. **Poista ostotilaus laskutuksen jälkeen** -valintaruudun valinta kannattaa poistaa **Ostoreskontran parametrit** -sivulla.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
