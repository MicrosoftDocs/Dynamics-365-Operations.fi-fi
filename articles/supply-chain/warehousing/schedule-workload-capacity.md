---
title: Kuormituskapasiteetin ajoittaminen
description: Tässä ohjeaiheessa käsitellään, miten voit määrittää ja ajoittaa kuormituskapasiteetin varaston työntekijöille tai koko varastolle.
author: MarkusFogelberg
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSWorkloadCapacity
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1b1334dcba7d12f2da301f70e21a08fceb88e2b4
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1559026"
---
# <a name="schedule-workload-capacity"></a>Kuormituskapasiteetin ajoittaminen

[!include[banner](../includes/banner.md)]

Voit ajoittaa varastojen kuormituskapasiteettia ja myös projektin nykyistä ja tulevaa kuormitusta yksittäisten varastojen työntekijöille. Voit suunnitella kuormituksen koko varastolle tai erikseen tuleville ja lähteville työmäärille.

Kyeisten varastojen pääajoitustiedot on oltava saatavilla lähtevän kuormituksen suunnittelemiseksi. Lisätietoja on kohdassa [Pääsuunnitelmat](../master-planning/master-plans.md).

## <a name="schedule-and-view-workloads-for-a-warehouse"></a>Varaston kuormituksen ajoittaminen ja tarkasteleminen

Varaston kuormituksen ajoittamiseksi on luotava kuormitusasetus vähintään yhdelle varastolle, ja liitettävä kuormitusasetus pääsuunnitelmaan. Kuormituskapasiteettiasetuksessa voit määrittää saapuvien ja lähtevien tapahtumien kuormalavoihin liittyvät rajoitteet ja painon tai tilavuuden. Voit myös luoda useamman kuin yhden asetuksen jokaiselle varastolle ja liittää asetuksen yksittäisiin pääsuunnitelmiin. Voi tehdä tämän esimerkiksi työvoiman kausittaisten muutosten vuoksi.

Jos varaston työntekijät työskentelevät sekä saapuvien että lähtevien kuormien tapahtumien kanssa, voit määrittää varaston kapasiteettiasetukset kuormituksen suunnittelemiseksi yhdistetyssä näkymässä.

Jotta voit ajoittaa ja tarkastella varastojen kuormituksia, sinun on suoritettava seuraavat tehtävät:

1. Luo kuormituskapasiteettiasetus ja määritä kuormituskapasiteetin rajoitukset vähintään yhdelle varastolle.
2. Liitä kuormituskapasiteettiasetus pääsuunnitelmaan kuormitusennusteiden luomiseksi ja määrittääksesi, kuinka kauan kyseiset suunnitelmat ovat käytössä.

### <a name="create-a-workload-capacity-setup-for-a-warehouse"></a>Kuormituskapasiteettiasetuksen luonti varastolle

1. Valitse **Varastonhallinta** \> **Asetukset** \> **Varastonhallinta** \> **Kuormituskapasiteetti**.
2. Valitse toimintoruudussa **Uusi** luodaksesi kuormituskapasiteetin asetukset.
3. Valitse **Varastot**-pikavälilehdessä **Uusi** ja kirjoita sitten riville arvot liittääksesi varaston kuormituskapasiteettiasetuksen kanssa.
4. Valitse **Yhdistetty saapuva ja lähtevä kuormitus** -valintaruutu, jos **Kuormituskapasiteetti**-raportin tulee näyttää saapuvien ja lähtevien tapahtumien kokonaiskuormitus yhdessä näkymässä.
5. Valitse **Tapahtumatyypit**-pikavälilehdellä saapuvat ja lähtevät tapahtumatyypit, joihin kuormitusrajat kohdistuvat.

    > [!NOTE]
    > Sinun on valittava vähintään yksi tapahtumatyyppi sekä saapuville että lähteville kuormituksille.

#### <a name="define-limits-for-volume-or-weight"></a>Määritä paino- tai tilavuusrajat

Voit määrittää rajoitukset tilavuudelle tai painolle riippuen siitä, mitkä rajoitukset ovat varaston työntekijöille olennaisia. Määrittämäsi rajoitukset sisällytetään kuormituskapasiteetin suunnitelmaan, jota voit tarkastella **Kuormituskapasiteetti**-raportissa.

Jotta nimikkeiden tilavuuteen ja painoon liittyviä tietoja voidaan laskea, kaikkien tuotteiden osalta on määritettävä yhden varastonimikkeen tilavuus ja paino. Tarvittavat kentät ovat käytettävissä seuraavissa kenttäryhmissä **Varaston hallinta**- pikavälilehdessä **Vapautetun tuotteen tiedot** -sivulla:

- Käsittely
- Fyysiset mitat
- Painomitat

Jos näitä tietoja ei ole määritetty oikein, saat viestin luodessasi **Kuormituskapasiteetti**-raportin. Raportissa saat tarkempaa tietoa tunnistaaksesi tulevan kuormituksen suunnittelusta puuttuvat tiedot.

### <a name="associate-a-workload-capacity-setup-with-a-master-plan"></a>Kuormituskapasiteettiasetuksen liittäminen pääsuunnitelmaan

1. Valitse **Varastonhallinta** \> **Kausittainen** \> **Ajoita kuormitus**.
2. Valitse **Pääsuunnitelma**-kentässä kuormitusarvioille käytettävä pääsuunnitelma.
3. Määritä **Päivien määrä** -kentässä päivien lukumäärä, jonka kuormitusarvio kattaa.
4. Valitse **Kuormitus**-kentässä pääsuunnitelmaan liitettävä kuormitusasetus.

### <a name="view-workload-capacity"></a>Kuormituskapasiteetin tarkasteleminen

1. Valitse **Varastonhallinta** \> **Kyselyt ja raportit** \> **Fyysiset varastoraportit** \> **Kuormituskapasiteetti**.
2. Määritä **Sarakkeiden määrä** -kentässä raportissa näytettävien sarakkeiden määrä.
3. Valitse **Tilaustyyppi**-kentässä **Suunniteltu ja vahvistettu**, **Suunniteltu** tai **Vahvistettu** osoittaaksesi raportissa näytettävät tilaustyypit.
4. Valitse **Kuormatyyppi**-kentässä kuormatyyppi, joka määrittää arvioidaanko kuormituskapasiteetti tilavuuden vai painon mukaan.
5. Valitse kuormituskapasiteettiasetus **Kuormituskapasiteetti**-kentässä.
