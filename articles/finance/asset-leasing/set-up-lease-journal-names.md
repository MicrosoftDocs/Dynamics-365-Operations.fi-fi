---
title: Vuokrakirjauskansioiden nimien määrittäminen
description: Tässä artikkelissa kerrotaan, miten vuokrakirjauskansioiden nimet määritetään. Vuokrakirjauskansioiden nimien määrittävät kirjauskansiot, joihin resurssin vuokrauksen viennit kirjataan.
author: moaamer
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeasePostingAccounts
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 678587e0846f6ce6d6d8113290a90b3f4d1988cc
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8874693"
---
# <a name="set-up-lease-journal-names"></a>Vuokrakirjauskansioiden nimien määrittäminen

[!include [banner](../includes/banner.md)]


Vuokrakirjauskansioiden nimien määrittävät kirjauskansiot, joihin resurssin vuokrauksen tapahtumat kirjataan. Vain **Resurssin vuokraus** -kirjauskansiotyypin kirjauskansioiden nimet näkyvät **Alkuperäinen tuloutus**- ja **Kuukausittaisen kirjauskansion nimi** -kentissä **Resurssin vuokraparametrit** -sivulla. Vain **Toimittajan laskun tallentaminen** -kirjauskansiotyyppi voidaan liittää **Laskukirjauskansion nimi** -kenttään.

Järjestelmä lukitsee tietyt taloushallinnon kentät ja estää niiden muokkaamisen. Tällä tavoin estetään tapahtumien ja aikataulujen väliset varianssit. Lukittuja ovat esimerkiksi seuraavat kentät: **Tili**, **Summat**, **Taloushallinnon dimensiot**, **Valuutta** ja **Tapahtumatyyppi**. Lisäksi kirjauskansiovientirivejä ei voi lisätä tai poistaa missään resurssin vuokrauskirjauskansion vienneissä, sillä se voi aiheuttaa aikataulujen ja tapahtumien välisiä variansseja.


Voit määrittää vuokrakirjauskansioiden nimet suorittamalla seuraavat vaiheet.

1. Siirry kohtaan **Resurssin vuokraus \> Asetukset \> Resurssin vuokrausparametrit**.
2. Valitse **Yleistiedot**-välilehden **Alkuperäisen tuloutuksen kirjauskansion nimi** -kentässä kirjauskansio. Kaikki alkuperäisen tuloutuksen kirjauskansioviennit kirjataan tähän kirjauskansioon.
3. Valitse **Laskukirjauskansion nimi** -kentässä kirjauskansio. Jos **Maksa toimittajalle** -vaihtoehdon arvoksi on määritetty **Kyllä** vuokrasopimuskirjassa, vuokrasopimuksen ja kulun maksujen laskut kirjataan tähän kirjauskansioon.
4. Valitse **Vuokrakirjauskansion nimi** -kentässä kirjauskansio. Kaikki poistot, korot ja lyhytaikaiset uudelleenluokitusviennit kirjataan tähän kirjauskansioon. Jos **Maksa toimittajalle** -vaihtoehdon arvoksi on määritetty **Ei** vuokrasopimuskirjassa, vuokrien ja kulun maksujen viennit kirjataan myös tähän kirjauskansioon.
5. Valitse **Vuokran muokkauskirjauskansion nimi** -kentässä kirjauskansio. Tähän kirjauskansion nimeen kirjataan vuokraoikaisut, irtisanomiset ja arvonalennustapahtumat. Valitsemaani kirjauskansion nimeen ei saa liittää työnkulkua tai hyväksyntää. Jos vuokramuutoksen kirjauskansion nimeä ei ole määritetty, vuokrasopimusten oikaisut, irtisanomiset ja irtisanomistapahtumat kirjataan **Vuokrakirjauskansion nimi** -kentässä valittuun kirjauskansion nimeen. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
