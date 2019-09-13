---
title: Resurssilaskureiden automaattinen päivitys
description: Tässä ohjeaiheessa kuvataan resurssilaskureiden automaattista päivitystä resurssien hallinnassa.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 97e6912cd37d6f82d8bf022141f04645a3364ee1
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875637"
---
# <a name="automatic-update-of-asset-counters"></a>Resurssilaskureiden automaattinen päivitys

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Edellisessä osassa on kuvattu käyttöomaisuuslaskureiden manuaalinen rekisteröiminen. Käyttöomaisuuslaskureiden määritys on kuvattu [Laskurit](../setup-for-objects/counters.md)-kohdassa.

Laskuriarvot voidaan päivittää myös automaattisesti tuotantorekisteröinneistä tuotantotuntien tai tuotantomäärän perusteella. Tämä tehdään kohdassa **Päivitä resurssilaskurit**. Voit päivittää yhden tai useita käyttöomaisuuksia lisäämällä yhden parametrin (**Alkamispäivämäärä**). Tämä parametri määrittää tuotantorekisteröintien alkamispäivän (tunnit tai tuotetut määrät) eli alkamispäivämäärän, josta lähtien laskurin arvot päivitetään.

Kaikki resurssit, jotka liittyvät resurssiin *ja* joilla on käyttöomaisuuslaskurit, jotka on määritetty päivitettäviksi tuotetun määrän tai tuotantotuntien perusteella, sisällytetään automaattiseen päivitykseen ja uudet laskuriarvot luodaan.

Liittyvät, tuotantomäärään, hyvään tuotantomäärään ja huonoon tuotantomäärään perustuvat laskurit, sisällytetään laskentaan. Jos tuotetun määrän rekisteröinnissä käytettävä yksikkö poikkeaa laskussa käytetystä yksiköstä, määrä muunnetaan vastaamaan laskuriyksikköä.

Kuten edellä mainittiin, automaattiset laskurit voidaan päivittää tuotannon rekisteröinneistä. Siksi käyttöomaisuuserän, jonka laskurit haluat päivittää automaattisesti, on oltava yhteydessä resurssiin (koneeseen). Seuraavissa kuvauksissa on yhteenveto tuotantotilausten asetuksista ja käsittelystä (**Tuotannonhallinta**-moduulissa), jota käytetään käyttöomaisuuserän laskureiden automaattisen päivityksen pohjana **Resurssien hallinta** -moduulissa.

Kun resurssille on rekisteröity tuotettuja määriä tai tuotantotunteja, voit päivittää liittyvät käyttöomaisuuslaskurit.

1. Valitse **resurssien hallinta** > **Kausittainen** > **resurssit** > **Päivitä resurssilaskurit**.

2. Valitse automaattisen päivityksen aloituspäivämäärä **Aloituspäivämäärä**-kentästä.

>[!NOTE]
>Tämän kentän päivämäärä on "keskeneräiset työt" -päivämäärä kohdasta **Reititystapahtumat** (**Tuotannonhallinta** > **Kyselyt ja raportit** > **Tuotanto** > **Reititystapahtumat** > **Fyysinen päivämäärä** -kenttä).

3. Jos haluat määrittää tiettyjen resurssien, resurssityyppien tai kohderesurssien automaattiset päivitykset valitsemalla **Sisällytettävät tietueet** -pikavälilehdessä **Suodata** ja valitse sitten haluamasi kohteet.

4. **Suorita taustalla** -pikavälilehdessä voit määrittää automaattisen päivityksen erätyönä tarpeen mukaan.

![Kuva 1](media/12-work-orders.png)

5. Valitse **OK**. Kun automaattinen käyttöomaisuuslaskurin päivitys on valmis, voit nähdä käyttöomaisuuteen liittyvät laskurirekisteröinnit kohdassa **Resurssilaskurit** (**Resurssien hallinta** > **Yhteiset** > **Resurssit** > **Kaikki resurssit** > valitse käyttöomaisuus > **Laskurit**-painike).

Kohdassa **Resurssilaskurien kokonaissumma**voit saada yleiskuvan kaikkien omaisuuserien kaikkien laskurityyppien viimeisimmistä rekisteröinneistä. Valitse **Resurssien hallinta** > **Kyselyt** > **Resurssit** > **Resurssien koostettu arvo**. Näkymä on hyvin samankaltainen kuin **Resurssilaskurit**, mutta et voi lisätä tai muokata **Resurssien koostettu arvo** -kohdan rekisteröintejä. Se on vain yleiskatsausta varten.

![Kuva 2](media/13-work-orders.png)


- On edelleen mahdollista luoda manuaaliset laskuriarvon rekisteröinnit automaattisesti päivitettäviä laskurityyppejä varten. Lisätietoja on Resurssilaskureiden manuaalinen päivitys-osassa.
- Voit määrittää toiseen laskuriin liittyviä laskureita, mikä tarkoittaa, että kun laskuri päivitetään, siihen liittyvät laskurit päivitetään automaattisesti samaan aikaan. Lisätietoja liittyvien laskurien määrittämisestä on kohdassa [Laskurit](../setup-for-objects/counters.md).
