---
title: Nimikehintojen vertailun varastoraportti
description: Lisätietoja nimikehintojen vertailun varastoraportin luomisesta ja tuloksen selaamisesta ja/tai viemisestä.
author: AndersGirke
manager: tfehr
ms.date: 01/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace, InventItemPriceCompareStorage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2020-03-01
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 6c8c72a631d361d7dffb8d18e00636e51e7998d3
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2020
ms.locfileid: "3201936"
---
# <a name="compare-item-prices-storage-report"></a>Nimikehintojen vertailun varastoraportti

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, miten **nimikehintojen vertailun varasto** -raportti suoritetaan ja miten tulos määritetään käytettäväksi digitaalisesti interaktiivisena sivuna Dynamics 365 Supply Chain Management -sovelluksessa tai vietynä asiakirjana jossakin useista muodoista.

Kun tarkastelet raporttia selaimessa, sarakkeita ja yhdistettyjä saldoja muutetaan dynaamisesti määritetyn asettelun perusteella. Voit esimerkiksi lajitella tulokset, suodattaa ne ja porautua tietoihin.

Raportin tulokset tallennetaan **Vertaa nimikehintoja** -tietoentiteettiin. Sen avulla voit suodattaa ja viedä tulokset esimerkiksi CSV- tai Microsoft Excel -muodossa.

**Nimikehintojen vertailun varasto** -raportti on hyödyllinen silloin, kun tuloksissa on useita rivejä. Tuloksissa voi olla useita rivejä esimerkiksi silloin, jos yli 40 000 nimikettä sisältää odottavan nimikehinnan kustannuslaskennan versiossa.

## <a name="enable-compare-item-prices-storage"></a>Nimikehintojen vertailun varaston käyttöönotto

Ennen kuin käytät tätä toimintoa, sinun on otettava se käyttöön järjestelmässä. Järjestelmänvalvojat voivat käyttää [toimintojen hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) asetuksia ja tarkistaa toiminnon tilan sekä ottaa sen käyttöön tarvittaessa. Toiminto näkyy seuraavasti:

- **Moduuli** - kustannustenhallinta
- **Toiminnon nimi** - nimikehintojen vertailun varasto

## <a name="generate-a-compare-item-prices-storage-report"></a>Nimikehintojen vertailun varastoraportin luominen

Seuraavien vaiheiden avulla voit luoda ja tallentaa **Nimikehintojen vertailun varasto** -raportin:

1. Siirry kohtaan **Kustannustenhallinta > Kyselyt ja raportit > Ennalta määritetyt kustannusraportit > Nimikehintojen vertailun varasto**.

1. Valitse **Uusi**, jos haluat avata **Vertaa nimikehintoja** -ruudun. Määritä seuraavat vaihtoehdot, jos haluat määrittää, mitä hintoja raportissa vertaillaan:

    - Anna **Parametrit**-pikavälilehdessä raportille yksilöivä **nimi** ja määritä **Odottavat hinnat, joita vertaillaan**- ja **Vertailussa käytettävät hinnat** -osien avulla vertailtavat hinnat ja päivämäärät.
    - Määritä **Sisällytettävät tietueet** -pikavälilehdessä suodattimet ja rajoitteet, joiden avulla määritetään raporttiin sisällytettävät tiedot.
    - Määritä **Suorita taustalla** -pikavälilehdessä miten, milloin ja miten usein raportti luodaan.
    > [!NOTE]
    > Tämä raportti suoritetaan aina osana erätyötä.

1. Ota asetukset käyttöön valitsemalla **OK** ja sulje ruutu.

1. Kun erätyö on tehty, se näkyy **Nimikehintojen vertailun varasto** -sivulla. Sinun on ehkä päivitettävä sivu, jotta näet raportin.

## <a name="explore-the-compare-item-prices-storage-report"></a>Nimikehintojen vertailun varastoraporttiin tutustuminen

Kun olet luonut raportin, voit tarkastella sitä ja tutustua sen tietoihin milloin tahansa seuraavasti:

1. Siirry kohtaan **Kustannustenhallinta > Kyselyt ja raportit > Ennalta määritetyt kustannusraportit > Nimikehintojen vertailun varasto**.

1. Valitse luettelosta raportti.

1. Tee jompikumpi seuraavista toimista:

    - Voit hakea raportin tulosten yleiskatsauksen valitsemalla **Yleiskatsaus**-kohdan.
    - Valitsemalla **Näytä tiedot** saat tarkemman näkymän raportista

1. Kun valittu näkymä avautuu, voit tehdä seuraavat toiminnot:

    - Valitse lähes mikä tahansa sarakeotsikko, kun haluat lajitella tai suodattaa taulun kyseisen sarakkeen arvojen mukaan. Näin voi tehdä lähes missä tahansa vakiolomakkeessa Supply Chain Management -sovelluksessa. Ota huomioon, että et voi lajitella tai suodattaa **Nettohinnan muutos-%** -sarakkeen mukaan, koska se on laskettu kenttä.
    - Valitse **Dimension näyttö**, jos haluat avata ruudun ja valita lomakkeeseen sisällytettävän dimensiosarakkeen. Määritä **Tallenna asetukset** -kohdan arvoksi **Kyllä**, jos haluat tallentaa asetukset niin, että ne ovat käytettävissä raportin seuraavalla avauskerralla. Ota asetukset käyttöön valitsemalla **OK** ja sulje.
    - Valitse mikä tahansa lomakkeen rivi ja valitse sitten **Näytä tiedot**, jos haluat katsella valitun nimikkeen lisätietoja. Voit porautua tietoihin tästä.
    - Valitse mikä tahansa lomakkeen rivi ja valitse sitten **Näytä vertailukaavio**, jos haluat nähdä vuorovaikutteisen graafisen esityksen tuloksista, jotka liittyvät valitsemaasi nimikkeeseen. Voit tutustua näihin tuloksiin valitsemalla kaavion ja kaavion selitteen erilaisia graafisia elementtejä.
    - Valitse mikä tahansa lomakkeen rivi ja valitse sitten **Näytä laskelman tiedot**, jos haluat katsella valittuun nimikkeeseen liittyviä laskelmia. Voit porautua tietoihin tästä.

## <a name="export-the-compare-item-prices-storage-report"></a>Nimikehintojen vertailun varastoraportin vieminen

Kaikki luodut raportit tallennetaan **Vertaa nimikehintoja** -tietoentiteettiin. Voit käyttää Supply Chain Management -sovelluksen vakiotiedonhallintatoimintoja, jos haluat viedä tämän entiteetin tiedot mihin tahansa tuettuun tietomuotoon, kuten CSV- tai Microsoft Excel -muotoon.

Seuraavassa on esimerkki siitä, miten **Nimikehintojen vertailun varasto** -raporttia viedään:

1. Siirry kohtaan **Järjestelmänhallinta > Työtilat > Tietojen hallinta**.

1. Valitse **Vie**-painike **Tietojen hallinta** -osassa.

1. Näkyviin tulee **Vienti**-sivu, jonka avulla vientityö määritetään. Aloita antamalla työlle **Ryhmän nimi**.

1. Valitse **Valitut entiteetit** -osassa **Lisää entiteetti** ja avaa valintaikkuna, jossa määritetään seuraavat asetukset:

    - **Yksikön nimi** - Valitse **Vertaa nimikehintoja**.
    - **Kohdetietojen muoto** - Valitse muoto, johon haluat viedä.

1. Valitse **Lisää**, jos haluat lisätä uuden rivin. Valitse sitten **Sulje**, jolloin valintaikkuna suljetaan.

1. Tavallisesti viedään yksi raportti kerralla. Voit tehdä tämän määrittämällä **suodattimen** **Kysely**-ruudussa lisätylle riville. Näin voit määrittää, mitkä raportit **Vertaa nimikehintoja** -entiteetistä sisällytetään raporttiin. Vie yksi raporttiin määrittämällä seuraavat suodatusvalinnat:

    - Valitse **Väli**-välilehdessä **Lisää**, jos haluat lisätä uuden rivin.
    - Määritä **Taulu**-kohdan arvoksi **Vertaa nimikehintoja**.
    - Määritä **Johdettu taulu** -kohdan arvoksi **Vertaa nimikehintoja**.
    - Määritä **Kenttä** sille kentälle, jonka mukaan haluat suodattaa. Yleensä käytetään **suorituksen nimeä** tai **suorituksen aikaa**.
    - Määritä **Ehdot** arvolle valitusta kentästä, jota haluat etsiä (joko raportin nimi tai sen luontiaika).
    - Lisää tarvittaessa rivejä **Väli**-taulukkoon, kunnes olet yksilöinyt etsittävän raportin.

1. Tallenna asetukset valitsemalla **OK** ja sulje.

1. Tallenna vientiasetukset valitsemalla **Tallenna**.

1. Avaa **Vientiasetukset**-välilehti ja luo vientitiedosto valitsemalla **Vie nyt**.

1. Näkyviin tulee **Suorituksen yhteenveto** -sivu, jolla näkyy vientityön tila ja vietyjen entiteettien luettelo. Valitse **Vertaa nimikehintoja** -entiteetti, joka on **Entiteetin käsittelyn tila** -alueella. Lataa tästä entiteetistä viedyt tiedot valitsemalla **Lataa tiedosto**.

Lisätietoja tietojen hallinnan käyttämisestä tietojen viemisessä on kohdassa [Tietojen tuonti- ja vientitöiden yleiskatsaus](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).
