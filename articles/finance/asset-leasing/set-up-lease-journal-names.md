---
title: Vuokrakirjauskansioiden nimien määrittäminen
description: Tässä ohjeaiheessa kerrotaan, miten vuokrakirjauskansioiden nimet määritetään. Vuokrakirjauskansioiden nimien määrittävät kirjauskansiot, joihin resurssin vuokrauksen viennit kirjataan.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: e8b1b908dfd6d1d6072b6efa83f13ae5784c85c1
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4442959"
---
# <a name="set-up-lease-journal-names"></a>Vuokrakirjauskansioiden nimien määrittäminen

[!include [banner](../includes/banner.md)]

Vuokrakirjauskansioiden nimien määrittävät kirjauskansiot, joihin resurssin vuokrauksen tapahtumat kirjataan. Vain **Resurssin vuokraus** -kirjauskansiotyypin kirjauskansioiden nimet näkyvät **Alkuperäinen tuloutus**- ja **Kuukausittaisen kirjauskansion nimi** -kentissä **Resurssin vuokraparametrit** -sivulla. Vain **Toimittajan laskun tallentaminen** -kirjauskansiotyyppi voidaan liittää **Laskukirjauskansion nimi** -kenttään.

Voit määrittää vuokrakirjauskansioiden nimet seuraavasti.

1. Siirry kohtaan **Resurssin vuokraus \> Asetukset \> Resurssin vuokrausparametrit**.
2. Valitse **Yleistiedot**-välilehden **Alkuperäisen tuloutuksen kirjauskansion nimi** -kentässä kirjauskansio. Kaikki alkuperäisen tuloutuksen kirjauskansioviennit kirjataan tähän kirjauskansioon.
3. Valitse **Laskukirjauskansion nimi** -kentässä kirjauskansio. Jos **Maksa toimittajalle** -vaihtoehdon arvoksi on määritetty **Kyllä** vuokrasopimuskirjassa, vuokrasopimuksen ja kulun maksujen laskut kirjataan tähän kirjauskansioon.
4. Valitse **Vuokrakirjauskansion nimi** -kentässä kirjauskansio. Kaikki poistot, korot ja lyhytaikaiset uudelleenluokitusviennit kirjataan tähän kirjauskansioon. Jos **Maksa toimittajalle** -vaihtoehdon arvoksi on määritetty **Ei** vuokrasopimuskirjassa, vuokrien ja kulun maksujen viennit kirjataan myös tähän kirjauskansioon.
