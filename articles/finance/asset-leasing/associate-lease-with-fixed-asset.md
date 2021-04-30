---
title: Käyttöomaisuuserien liittäminen vuokrasopimuksiin
description: Tässä ohjeaiheessa kerrotaan, miten aiemmin luotu käyttöomaisuuserä liitetään uuteen vuokrasopimukseen.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseDetail
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 02a17b8c995e8aa97384d8b855afb688324017d6
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881345"
---
# <a name="associate-fixed-assets-with-leases"></a>Käyttöomaisuuserien liittäminen vuokrasopimuksiin

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, miten aiemmin luotu käyttöomaisuuserä liitetään uuteen vuokrasopimukseen. Kun liität käyttöomaisuuserän vuokrasopimukseen, käyttöoikeusomaisuuserän arvo alkuperäisen tuloutuksen aikana on käyttöomaisuuserän hankintakustannus.

Ennen kuin voit liittää käyttöomaisuuserän vuokrasopimukseen, sinun on luotava käyttöomaisuuserälle tietue Käyttöomaisuuserät-kohdassa. Tämän jälkeen luodaan vuokrasopimus ja linkitetään siihen resurssi **Vuokrasopimusyhteenveto**-sivulla.

1. Lisää vuokrasopimus noudattamalla kohdan [Lisää tai kopioi vuokrasopimukset](add-lease.md) ohjeita. Valitse **Lisää vuokrasopimus** -sivun **Käyttöomaisuusnumero**-kentässä resurssi, jota ei ole vielä hankittu.
2. Valitse **Kirjat** ja vahvista maksuaikataulu.
3. Valitse **Alkuperäinen tunnustaminen**.
4. Valitse **Resurssin leasingkirjauskansio**.

    Vuokrasopimuksen alkuperäinen tuloutuksen kirjauskansiovienti veloittaa summasta käyttöomaisuuden, joka yleensä veloitetaan käyttöoikeusomaisuuserän tililtä.

    Voit nyt tarkastella käyttöomaisuuserän tapahtumatyyppiä ja kirjaa.

5. Valitse **Kirjauskansion tiedot**.
6. Valitse **Rivit**, jos haluat tarkastella kirjauskansioviennin yksittäisiä rivejä.
7. Valitse resurssin sisältävä kirjauskansiorivi ja valitse sitten **Käyttöomaisuuserät**-välilehti.

    **Käyttöomaisuuserät**-välilehdessä näkyy tapahtumatyyppi ja kirja. Oletusarvoisesti **Tapahtumatyyppi**-kentän arvoksi on määritetty **Hankinta** ja **Kirja**-kentän arvoksi käyttöomaisuuden nykyinen kirja.

Kun olet kirjannut alkuperäisen tuloutuksen kirjauskansioviennin, tapahtuma näkyy käyttöomaisuuserän hankintatapahtumana. Voit tarkastella tapahtumataulukkoa siirtymällä kohtaan **Käyttöomaisuuserät \> Käyttöomaisuuserät \> Käyttöomaisuuserät**, valitsemalla soveltuvan käyttöomaisuuden ja valitsemalla sitten **Arvostukset**. Näet, että alkuperäinen tuloutuksen kirjauskansiovienti on luonut määritetyn käyttöomaisuuserän hankintatapahtuman.

Käyttöomaisuus voidaan nyt poistaa Käyttöomaisuuserät-kohdan vakiopoistotoimintojen avulla. Lisätietoja poistosta on kohdassa [Poistomenetelmät ja -käytännöt](../fixed-assets/depreciation-methods-conventions.md).

> [!NOTE]
> Jos käyttöomaisuus liitetään vuokrasopimukseen, **Resurssin poisto** ja **Vuokrasopimuksen arvonalennus** -painikkeet eivät ole käytössä resurssin vuokrauksessa. Voit tarkastella resurssin poistoa ja vuokrasopimuksen arvonalennustapahtumia Käyttöomaisuuserät-kohdassa. **Resurssitapahtumat**-painike, joka avaa kyselylomakkeen, on myös poistettu käytöstä. Voit avata myös **Resurssitapahtumat**-kyselyn Käyttöomaisuuserät-kohdassa.  


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
