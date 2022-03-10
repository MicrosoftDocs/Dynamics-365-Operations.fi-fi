---
title: Konsernin sisäisen myyntitilauksen luominen sisäiseen käyttöön
description: Tässä aiheessa käsitellään konsernin sisäisen myyntitilauksen luontia sisäistä käyttöä varten
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 0718a1560ec42df2a0a12e8b81484aa3be46d2d8
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548236"
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