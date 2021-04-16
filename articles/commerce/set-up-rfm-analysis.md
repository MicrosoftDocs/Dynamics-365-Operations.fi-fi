---
title: Määritä Recency, Frequency, and Monetary (RFM) -analyysi
description: Tässä ohjeaiheessa kerrotaan, kuinka asiakkaidesi Recency, Frequency, and Monetary (RFM) -analyysi määritetään.
author: josaw1
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MCRRFMDefinition
audience: Application User
ms.reviewer: josaw
ms.custom: 78943
ms.assetid: 8ff9aac3-5ada-4150-85fd-18901c926d53
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 0eece0678335caa789f0b2c4a324deab6832b53c
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795474"
---
# <a name="set-up-recency-frequency-and-monetary-rfm-analysis"></a>Määritä Recency, Frequency, and Monetary (RFM) -analyysi

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, kuinka asiakkaidesi Recency, Frequency, and Monetary (RFM) -analyysi määritetään.

Recency, Frequency, and Monetary (RFM)-analyysi on työkalu, jonka avulla organisaatio voi arvioida asiakasostojen muodostamat tiedot. Kun olet määrittänyt RFM-analyysin, asiakkaille määritetään laskettu RFM-pistemäärä heidän tehdessään ostoksia. RFM-pisteytys voi olla kolmenumeroinen luokitus tai yhteenlaskettu numero, riippuen siitä, kuinka organisaatio on määrittänyt RFM-analyysin. Luokitus toimii seuraavasti, jos organisaatio käyttää pisteytykseen kolminumeroista luokitusta:

- Ensimmäinen numero on asiakkaan recency-luokitus, joka ilmaisee kuinka äskettäin asiakas teki oston organisaatiosta.
- Toinen numero on asiakkaan frequency-luokitus, joka ilmaisee kuinka usein asiakas tekee ostoja organisaatiosta.
- Kolmas numero on asiakkaan monetary-luokitus, joka ilmaisee paljonko rahaa asiakas käyttää tehdessään ostoja organisaatiosta.

Organisaatiosi on esimerkiksi asettanut luokitukset asteikolle 1-5, jossa 5 on korkein luokitus. Tässä tapauksessa asiakkaan luokitus 535 kertoo seuraavaa tietoa asiakkaasta:

- **Äskettäisyysluokitus 5** – Asiakas on tehnyt ostoksen äskettäin.
- **Toistuvuusluokitus 3** – Asiakas ostaa organisaatiosi tuotteita normaalilla aikavälillä.
- **Rahasummaluokitus 5** – Kun asiakas suorittaa oston, hän käyttää huomattavan summan rahaa.

Jos organisaatiosi käyttää tuloksena yhteenlaskettua lukua, yksittäiset luokitusluvut lasketaan yhteen. Saman esimerkin asiakkaalla on luokitus 13 (5 + 3 + 5).

## <a name="set-up-rfm-analysis-for-the-customers-in-your-organization"></a>Määritä RFM-analyysi organisaation asiakkaille

1. Valitse **Puhelinkeskus** \> **Kausittainen** \> **RFM-analyysi**.
2. Valitse **RFM-analyysi**-sivulla **Uusi**. Anna RFM-määrityksen nimi **RFM-määritys**-kentässä. Esimerkiksi voisit kutsua määritelmää RFM-A:ksi
3. Kirjoita alkamis- ja päättymispäivä tälle RFM-määritykselle.
4. Toimi **Yleiset**-pikavälilehdellä seuraavasti:

    - Jos kussakin RFM-pistemäärän osassa on oltava sama määrä asiakkaita, valitse **Tasainen jako** -valintaruutu.
    - Yhdistä kolme pistemäärää valitsemalla **Lisää pisteet** -valintaruutu. Tällä tavoin asiakkaan RFM-pistemääräksi tulisi esimerkiksi 13 eikä 535.
    - Valitse **Tallenna historia** -valintaruutu, jos haluat järjestelmän tallentavan asiakkaiden tilastotiedot siten, että tiedoilla voidaan laskea RFM-pistemäärä.

5. Toimi **Recency**-pikavälilehdellä seuraavasti:

    - Anna **Jaot**-kentässä niiden osastojen tai ryhmien määrä, joilla asiakkaiden recency-pistemäärä lasketaan. Esimerkiksi jos sinulla on 100 asiakasta, jako 5:llä tarkoittaa, että jokaiselle tulokselle on 20 asiakasta. 20:n viimeksi ostoja tehneen asiakkaan recency-pistemäärä on 5. Seuraavan 20 asiakkaan recency-pistemäärä on 4 ja niin edelleen. Jos sinulla on 50 asiakkaasta, 10 asiakkaan recency-tulos on 5-10, 10 asiakkaan recency-tulos on 4 ja niin edelleen.
    - Valitse **Prioriteetti**-kentässä, miten suuri painoarvo annetaan recency-parametrille suhteessa muihin, kun asiakkaalle lasketaan RFM-pisteet. Voit esimerkiksi antaa enemmän arvoa viimeaikaisuusarvolle kuin raha-arvolle.
    - Anna **Kerroin**-kenttään arvo, jolla recency-pistemäärä kerrotaan. Jos arvoa ei syötetä, pisteitä ei kerrota.
    - Valitse **Kausi**-kentässä ajanjakso, jolta recency-tulos lasketaan. Esimerkiksi viikoittain tai kuukausittain.

6. Toimi **Frequency**-pikavälilehdellä seuraavasti:

    - Anna **Jaot**-kentässä niiden osastojen tai ryhmien määrä, joilla asiakkaiden frequency-pistemäärä lasketaan.
    - Valitse **Prioriteetti**-kentässä, miten suuri painoarvo annetaan frequency-parametrille suhteessa muihin, kun asiakkaalle lasketaan RFM-pisteet.
    - Anna **Kerroin**-kenttään arvo, jolla frequency-pistemäärä kerrotaan. Jos arvoa ei syötetä, pisteitä ei kerrota.

7. Toimi **Monetary**-pikavälilehdellä seuraavasti:

    - Anna **Jaot**-kentässä niiden osastojen tai ryhmien määrä, joilla asiakkaiden monetary-pistemäärä lasketaan.
    - Valitse **Prioriteetti**-kentässä, miten suuri painoarvo annetaan monetary-parametrille suhteessa muihin, kun asiakkaalle lasketaan RFM-pisteet.
    - Anna **Kerroin**-kenttään arvo, jolla monetary-pistemäärä kerrotaan. Jos arvoa ei syötetä, pisteitä ei kerrota.
    - Valitse **Brutto/netto**-kentässä valitse, lasketaanko asiakkaan rahallinen pistemäärä brutto- vai nettolaskusummalla.
    - Jos asiakkaan palautuksen summat on vähennettävä asiakkaan kokonaislaskulaskelmasta, valitse **Vähennä palautukset** -valintaruutu.

## <a name="view-a-customers-rfm-score"></a>Näytä asiakkaan RFM-pistemäärä

Tämän menetelmän avulla voit tarkastella asiakkaan RFM-pistemäärää.

1. Valitse **Puhelinkeskus** \> **Kirjauskansiot** \> **Asiakaspalvelu**.
2. Valitse **Asiakaspalvelu**-sivun **Asiakaspalvelu**-ruudun hakukentissä haettava avainsanatyyppi ja kirjoita etsittävä teksti.
3. Valitse **Haku**.
4. Valitse **Asiakashaku**-sivulla ensin asiakastietua ja sitten **Valitse asiakas**.

RFM-pistemäärä näkyy **Tilaushistoria**-ryhmässä **Asiakaspalvelu**-sivun oikealla puolella.

## <a name="view-or-clear-the-history-of-an-rfm-analysis-record"></a>Tarkastele tai poista RFM-analyysitietueen historiatietoja.

Tämän toiminnon avulla voit tarkastella tai poistaa RFM-analyysitietueen historiatiedot.

1. Valitse **Puhelinkeskus** \> **Kausittainen** \> **RFM-analyysi**.
2. Valitse **RFM-analyysi**-sivulla tarkasteltava tietue.
3. Voit tarkastella tietueen historiatiedot valitsemalla **Historia**-pikavälilehden.
4. Voit tyhjentää tietueen historiatiedot valitsemalla **Tyhjennä historia**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]