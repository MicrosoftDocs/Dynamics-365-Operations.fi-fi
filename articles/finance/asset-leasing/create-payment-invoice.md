---
title: Maksulaskujen luominen
description: Tässä ohjeaiheessa käsitellään kuukausittaisia vuokrauksen laskuja. Voit luoda laskuja yksittäisille vuokrasopimuksille tai voit luoda eräkäsittelyn avulla useita vuokrasopimuksia.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeasePaymentSchedule
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 8d0b10993c61c64dadc00046907485f3886e2e01
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881177"
---
# <a name="create-payment-invoices"></a>Maksulaskujen luominen

[!include [banner](../includes/banner.md)]

Voit luoda kuukausittaisia laskuja yksittäisille vuokrasopimuksille tai voit luoda eräkäsittelyn avulla useita vuokrasopimuksia. Seuraavassa kuvataan, miten yksittäisen vuokravienti voidaan luoda, kun **Maksa toimittajalle** -parametri **Vuokrasopimuksen kirjan asetukset** -sivulla on käytössä.

1. Valitse **Vuokrasopimusyhteenveto**-sivulla vuokrasopimus ja valitse sitten **Kirjat \> Maksuaikataulu**.
2. Valitse suoritettava maksu ja valitse sitten **Luo kirjauskansio**. Näyttöön tulee sanoma, joka osoittaa, että valitulle maksulle on luotu kirjauskansio.
3. Valitse **Laskun kirjauskansiot** ja valitse sitten maksettava lasku.
4. Tarkista **Rivit**-välilehdessä kirjauskansiovienti ennen sen kirjaamista kirjanpitoon.

    > [!NOTE]
    > Oletusarvon mukaan luotavat toimittajan laskurivit käyttävät toimittajan kirjausprofiilia **Ostoreskontran parametrit** -sivulta.

5. Valitse oikea kirjauskansio ja valitse sitten maksettava lasku.

    Tässä esimerkissä vuokrasopimuksen kirjan **Maksa toimittajalle** -parametri on käytössä. Näin ollen lasku on laskun kirjauskansiossa. **Yleiskatsaus**-osassa näkyy kirjauskansioviennin yhteenveto, ja **Rivit**-osassa näkyvät todellisten kirjauskansiorivien tiedot.

    > [!NOTE]
    > Jos **Maksa toimittajalle** -parametri on poistettu käytöstä, maksun kirjauskansioviennit ovat vuokrasopimuksen kirjan **Resurssin vuokraus** -sivulla. Järjestelmä luo resurssin vuokrauksen viennin laskun sijaan. Vuokravienti kirjataan kirjauskansioon, joka määritetään **Kuukausittaisen vuokrauksen kirjauskansio** -kentässä.

6. Kun tapahtuma on kirjattu, voit tarkastella tapahtuman tietoja ja vuokrasopimusvelan arvoa valitsemalla **Velkatapahtumat** vuokrasopimuksen kirjassa.

    Maksuaikataulussa valitaan **Kirjauskansio kirjattu** -valintaruutu. Rivi näkyy laskun kirjauskansion numerossa. Kun olet luonut kirjauskansion ja viennin luodulle kirjauskansiolle, vienti on peruutettava ennen kuin se voidaan luoda uudelleen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
