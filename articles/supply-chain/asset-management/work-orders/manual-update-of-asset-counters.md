---
title: Resurssilaskureiden manuaalinen päivitys
description: Tässä ohjeaiheessa kuvataan resurssilaskureiden manuaalista päivitystä resurssien hallinnassa.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetCounter
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5318bac961682f88e192ac70c4993c62b69b399c
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/16/2021
ms.locfileid: "5020877"
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

