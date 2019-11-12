---
title: Resurssilaskureiden automaattinen päivitys
description: Tässä ohjeaiheessa kuvataan resurssilaskureiden automaattista päivitystä resurssien hallinnassa.
author: josaw1
manager: AnnBe
ms.date: 10/15/2019
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
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: d51b9a7684e460d555632c3896e9dd8a4e10d92c
ms.sourcegitcommit: deb87e518a151d8bb084891851a39758938a96e4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/15/2019
ms.locfileid: "2626175"
---
# <a name="automatic-update-of-asset-counters"></a>Resurssilaskureiden automaattinen päivitys

[!include [banner](../../includes/banner.md)]

Katso lisätietoja resurssilaskureiden manuaalisesta rekisteröinnistä kohdasta [Resurssilaskureiden manuaalinen päivitys](../work-orders/manual-update-of-asset-counters.md). Lisätietoja resurssilaskureiden määrittämisestä esitetään kohdassa [Laskurit](../setup-for-objects/counters.md).

Laskuriarvot voidaan päivittää myös automaattisesti tuotantorekisteröinneistä tuotantotuntien tai tuotantomäärän (eli tuotetun määrän) perusteella. Tämä päivitys suoritetaan **Päivitä resurssilaskurit** -sivulla. Voit päivittää yhden tai useita käyttöomaisuuksia määrittämällä yhden parametrin (**Alkamispäivämäärä**). Tämä parametri määrittää tuotantorekisteröintien (tuotantotuntien tai tuotantomäärien) aloituspäivämäärän. Toisin sanoen se määrittää, mistä päivämäärästä alkaen laskureiden arvoja päivitetään.

Kaikki resurssit, jotka liittyvät resurssiin *ja* joilla on resurssilaskurit, jotka on määritetty päivitettäviksi tuotetun määrän tai tuotantotuntien perusteella, sisällytetään automaattiseen päivitykseen. Uudet laskuriarvot luodaan.

Tuotantomäärään perustuvien laskureiden osalta määrään sisältyvät sekä rekisteröity tavaramäärä että rekisteröity virhemäärä. Jos tuotantomäärän rekisteröinnissä käytettävä yksikkö eroaa määrään käytettävän laskurin yksiköstä, määrä muunnetaan vastaamaan laskurin yksikköä.

Kuten edellä mainittiin, automaattiset laskurit voidaan päivittää tuotannon rekisteröinneistä. Siksi käyttöomaisuuserän, jonka laskurit haluat päivittää automaattisesti, on oltava yhteydessä resurssiin (koneeseen). Kun resurssille on rekisteröity tuotettuja määriä tai tuotantotunteja, voit päivittää liittyvät käyttöomaisuuslaskurit.

1. Valitse **Resurssienhallinta** > **Kausittainen** > **Resurssit** > **Päivitä resurssilaskurit**.

2. Valitse automaattisen päivityksen aloituspäivämäärä **Aloituspäivämäärä**-kentästä.

>[!NOTE]
>Tämän kentän päivämäärä on "keskeneräiset työt" -päivämäärä kohdasta **Reititystapahtumat** (**Tuotannonhallinta** > **Kyselyt ja raportit** > **Tuotanto** > **Reititystapahtumat** > **Fyysinen päivämäärä** -kenttä).

3. **Sisällytettävät tietueet** -pikavälilehdellä voit valita tiettyjä resursseja tai resurssityyppejä automaattisesti päivitettäväksi. Tee tarvittavat valinnat ja valitse **Suodata**.

4. **Suorita taustalla** -pikavälilehdessä voit määrittää automaattisen päivityksen erätyönä tarpeen mukaan.

Seuraavassa kuvassa on esimerkki **Päivitä resurssilaskurit** -valintaikkunasta.

![Kuva 1](media/12-work-orders.png)

5. Valitse **OK**. 

Kun automaattinen resurssilaskureiden päivitys on tehty, voit tarkastella resurssiin liittyviä laskurirekisteröintejä **Resurssilaskurit**-sivulla. Valitse **Resurssienhallinta** > **Yhteiset** > **Resurssit** > **Kaikki resurssit**, valitse resurssit ja valitse sitten **Laskurit** toimintoruudun **Ennaltaehkäisevä**-ryhmän **Resurssit**-välilehdessä.

Sivulta **Resurssilaskurien kokonaissumma** voit saada yleiskuvan kaikkien resurssien kaikkien laskurityyppien viimeisimmistä rekisteröinneistä. Valitse **Resurssienhallinta** > **Kyselyt** > **Resurssit** > **Resurssien koostettu arvo**. Tämä sivu muistuttaa sivua **Resurssilaskurit**, mutta et voi lisätä tai muokata rekisteröintejä. Se on vain yleiskatsausta varten.

Seuraavassa kuvassa on esimerkki **Resurssien koostettu arvo** -sivusta.

![Kuva 2](media/13-work-orders.png)

Huomaa seuraavat seikat:

- Voit edelleen luoda manuaalisia laskuriarvon rekisteröintejä automaattisesti päivitettäviä laskurityyppejä varten. Lisätietoja on kohdassa [Resurssilaskureiden manuaalinen päivitys](../work-orders/manual-update-of-asset-counters.md).

- Voit määrittää toisiin laskureihin liittyviä laskureita. Tällöin liittyvät laskurit päivitetään automaattisesti samalla kun päälaskuri päivitetään. Lisätietoja resurssilaskureiden määrittämisestä esitetään kohdassa [Laskurit](../setup-for-objects/counters.md).

