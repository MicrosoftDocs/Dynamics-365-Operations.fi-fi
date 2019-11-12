---
title: Resurssilaskureiden manuaalinen päivitys
description: Tässä ohjeaiheessa kuvataan resurssilaskureiden manuaalista päivitystä resurssien hallinnassa.
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
ms.openlocfilehash: 3072ab204b53b16988d2973b28a697041cb84c27
ms.sourcegitcommit: deb87e518a151d8bb084891851a39758938a96e4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/15/2019
ms.locfileid: "2626130"
---
# <a name="manual-update-of-asset-counters"></a>Resurssilaskureiden manuaalinen päivitys

[!include [banner](../../includes/banner.md)]



Laskureita käytetään resurssin rekisteröintien luomiseen. Nämä rekisteröinnit koskevat esimerkiksi resurssin käytössäolotunteja tai tuotettua määrää.

Laskurille valittu laskurityyppi voidaan määrittää perimään laskuriarvoja. Toisin sanoen **Peri resurssilaskurin arvot** -asetuksen arvoksi asetetaan **Kyllä** **Laskurit**-sivun **Yleistä**-pikavälilehdessä (**Resurssienhallinta** > **Asetukset** > **Resurssityypit** > **Laskurit**). Kun tässä tapauksessa luot kyseistä tyyppiä edustavan laskuririvin, jokainen samaa laskurityyppiä käyttävä alilaskuri päivitetään automaattisesti.

**Kaikki resurssit** -sivulla voit luoda resurssille tuntien tai määrien laskurimerkintöjä resurssin lukemien perusteella.

1. Valitse **Resurssienhallinta** > **Yhteiset** > **Resurssit** > **Kaikki resurssit**.

2. Valitse resurssi ja sitten toimintoruudun **Resurssi**-välilehden **Ennaltaehkäisevä**-ryhmässä **Laskurit**. **Resurssilaskurit**-sivulla näkyy luettelo valitun resurssin kaikista aiemmista laskurirekisteröinneistä.

3. Luo uusi rekisteröinti valitsemalla **Uusi**. Resurssitunnus syötetään automaattisesti **Resurssi**-kenttään.

4. Valitse **Laskuri**-kentästä haluamasi laskuri. Vain resurssille valittuun resurssityyppiin liittyvät laskurit ovat vallittavissa. Liittyvä yksikkö syötetään automaattisesti **Yksikkö**-kenttään.

5. Valitse **Rekisteröity**-kentässä laskurirekisteröinnin päivämäärä ja aika.

6. Syötä **Arvo**-kenttään edellisestä laskurirekisteröinnistä kulunut numero. Vaihtoehtoisesti voit syöttää laskurin kokonaisnumeron **Koostettu arvo** -kenttään.

Huomaa seuraavat seikat:

- Jos asennat käyttöomaisuuserään uuden laskurin fyysisesti, sinun täytyy rekisteröidä käyttöomaisuuserän muutos **Resurssilaskurit**-sivulle. Seuraavaksi sinun on luotava kaksi rekisteröintiriviä, joilla on identtiset aikaleimat. Ensimmäisen rivin on oltava korvattavaa laskuria vartenn. Valitse uuteen laskuriin liittyvällä rivillä **Laskurin nollaus** -valintaruutu. **Summa**-kentässä laskurin kokonaissumma on kyseisen laskurityypin kaikkien kirjattujen arvojen laskurin summa.

- Jos resurssin **Laskurin nollaus** -valintaruutu on valittuna resurssille käyttämällä ylläpitosuunnitelmaa, jonka välityyppi on"Kerran alkaen..." tai "Kerran jälkeen...", laskuri on edelleen aktiivinen uudella laskuririvillä, koska luot erillisen laskuririvin ja aloitat alusta uuden laskurin avulla.

Seuraavassa kuvassa on esimerkki **Resurssilaskurit**-sivusta.

![Kuva 1](media/11-work-orders.png)

**Resurssilaskurit**-sivulla (**Resurssienhallinta** > **Kyselyt** > **Resurssit** > **Resurssilaskurit**), voit tarpeen mukaan suorittaa laskurirekisteröintejä useille resursseille samanaikaisesti

>[!NOTE]
>Voit määrittää välin määrittämään poikkeuksia manuaalisissa laskurirekisteröinneissä. Voit myös määrittää, minkälainen sanoma tulee näkyviin, jos rekisteröinnit poikkeavat määritetystä välistä. Lisätietoja laskureiden määrittämisestä esitetään kohdassa [Laskurit](../setup-for-objects/counters.md).

