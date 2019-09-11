---
title: Resurssilaskureiden manuaalinen päivitys
description: Tässä ohjeaiheessa kuvataan resurssilaskureiden manuaalista päivitystä resurssien hallinnassa.
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
ms.openlocfilehash: 1e7c5ec288404c18b00f9dcd0e66f50744d0aa2f
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875632"
---
# <a name="manual-update-of-asset-counters"></a>Resurssilaskureiden manuaalinen päivitys

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


Laskurien avulla luodaan käyttöomaisuuserän rekisteröinnit, jotka koskevat esimerkiksi käytössä olevien tuntien määrää tai tuotettuja määriä.

Jos laskurille valittu laskurityyppi on asetettu perimään laskuriarvot (**Resurssien hallinta** > **Asetukset** > **Resurssityypit** > **Laskurit** > **Yleiset**-pikavälilehti > **Peri resurssilaskurin arvot** -vaihtopainikkeen arvoksi "Kyllä"), ja kun luot uuden tämän tyypin laskuririvin, samaa laskurityyppiä käyttävät kaikki alemman tason resurssit päivitetään automaattisesti.

**Kaikki resurssit** -kohdassa voit luoda käyttöomaisuuserälle tuntien tai määrien laskurimerkintöjä käyttöomaisuuserän lukemien perusteella.

1. Valitse **Resurssien hallinta**  >  **Yhteiset**  >  **Resurssit**  >  **Kaikki resurssit**.

2. Valitse käyttöomaisuus luettelosta ja valitse sitten **Laskurit**. **Resurssilaskurit**-lomakkeessa näkyy luettelo valitun käyttöomaisuuserän kaikista aiemmista laskurirekisteröinneistä.

3. Luo uusi rekisteröinti valitsemalla **Uusi**. Resurssitunnus lisätään automaattisesti.

4. Valitse **Laskuri**-kentästä haluamasi laskuri. Vain käyttöomaisuuserälle valittuun käyttöomaisuuslajiin liittyvät laskurit ovat käytettävissä. Liittyvä yksikkö lisätään automaattisesti **Yksikkö**-kenttään.

5. Valitse laskurin rekisteröinnille päivämäärä ja aika.

6. Lisää **Arvo**-kenttään numero edellisen laskurikirjauksen jälkeen tai lisää laskurin summaluku **Koostettu arvo** -kenttään.

- Jos asennat käyttöomaisuuserään uuden laskurin fyysisesti, sinun täytyy rekisteröidä käyttöomaisuuserän muutos **Resurssilaskurit**-kohdassa. Seuraavaksi sinun on luotava kaksi kirjausriviä, joilla on samat aikaleimat, ja uuden laskurin rivillä on valittava **Laskurin nollaus** -valintaruutu. Kun luot kaksi kirjausriviä, ensimmäisen rivin on oltava korvattavien laskurien kohdalla. **Summa-** kentässä laskurin kokonaissumma on kyseisen laskurityypin kaikkien kirjattujen arvojen laskurin summa.  
- Jos resurssin **Laskurin nollaus** -valintaruutu on valittuna käyttöomaisuuserälle käyttämällä huoltosuunnitelmaa, jonka vältyyppi on"Kerran alkaen..." tai "Kerran jälkeen...", laskuri on edelleen aktiivinen uudella laskuririvillä, koska luot erillisen laskuririvin ja aloitat alusta uuden laskurin avulla.

![Kuva 1](media/11-work-orders.png)


Jos haluat tehdä laskurikirjauksia useille käyttöomaisuuserille, se voidaan tehdä kohdaas **Resurssien hallinta** > **Kyselyt** > **Resurssit** > **Resurssilaskurit.**

>[!NOTE]
>Voit määrittää alueen, joka määrittää manuaalisten laskurirekisteröintien poikkeamat, sekä sanoman tyypin, joka tulee näkyviin, jos rekisteröinnit ovat määritetyn alueen ulkopuolella. Lisätietoja laskurien määrittämisestä on kohdassa [Laskurit](../setup-for-objects/counters.md).
