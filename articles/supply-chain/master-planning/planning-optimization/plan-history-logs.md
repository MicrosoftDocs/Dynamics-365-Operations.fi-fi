---
title: Suunnitelman historia- ja suunnittelulokien tarkasteleminen
description: Tässä ohjeaiheessa käsitellään, miten suunnittelun optimointitoiminnon käynnistämien suunnittelutöiden historiatietoja tarkastellaan.
author: ChristianRytt
ms.date: 10/30/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MPSPlanRegenerationJobList, MPSPlanRegenerationJobLogs
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 757d2103bd629c0107a3f29599196a56ea56d431a66cf1e69c7b3cf3d817c087
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6724817"
---
# <a name="view-plan-history-and-planning-logs"></a>Suunnitelman historia- ja suunnittelulokien tarkasteleminen

[!include [banner](../../includes/banner.md)]

Tässä ohjeaiheessa käsitellään, miten Microsoft Dynamics 365 Supply Chain Managementin suunnittelun optimointitoiminnon käynnistämien suunnittelutöiden historiatietoja tarkastellaan.

Voit tarkastella suunnitelman historiaa avaamalla suunnitelman valitsemalla ensin **Pääsuunnittelu** \> **Asetukset** \> **Suunnitelmat** \> **Pääsuunnitelmat** ja sitten **Historia**. Historiatiedoissa on luettelo kaikista valitun suunnitelman töistä. Luettelo sisältää valmiit ja aktiiviset työt.

Suunnittelun optimoinnin pääsuunnittelun ajojen töiden historia sisältää enintään 60 tietuetta pääsuunnitelmaa kohden. Kun suoritat uuden pääsuunnittelun laskennan, tämän suunnitelman varhaisin historiatietue poistetaan.

Töiden alkamisajan ja tilan lisäksi voit tarkastella tietyn työn lokia. Loki sisältää lisätietoja ja varoituksia. Kaikilla töillä ei ole lokia. Voit tarkastella työn lokia valitsemalla **Loki**. Lokimerkinnät tallennetaan vain 30 päivän ajan työn valmistumispäivämäärästä sen jälkeen, kun ne poistetaan automaattisesti.

Jos **Eräkäsittely-asetus** **Suorita taustalla** -pikavälilehdessä on otettu käyttöön pääsuunnittelun käsittelyn määritysten yhteydessä, erätyölokissa näkyy lisätietoja pääsuunnittelun suorittamisen aikana luoduista varoituksista ja virheistä. Esimerkiksi automaattisen korjauksen virheet siepataan vain erätyölokissa. Ne eivät näy **Historia**-sivun lokeissa.

Noudattamalla seuraavia ohjeita voit tarkastella automaattisia korjauksen virheitä sekä muita pääsuunnittelun suorittamisen aikana annettuja varoituksia tai virheitä.

1. Siirry kohtaa **Järjestelmänhallinta \> Kyselyt \> Erätyöt**.
1. Etsi ja valitse tietue, joka vastaa haluamaasi pääsuunnittelun suoritusta. (Esimerkiksi **Työn kuvaus** -kenttä voi alkaa sanoilla *Pääsuunnittelu*.)
1. Seuraa jotain näistä vaiheista riippuen siitä, käytetäänkö *parannettua lomaketta* vai *vanhaa (parantamatonta) lomaketta* **Erätyöt**-sivulla:

    - Jos käytät laajennettua lomaketta: Valitse toimintoruudusta **Erätyöhistoria**. Valitse sitten **Erätyöhistoria**-sivun toimintoruudusta **Loki**.
    - Jos käytät vanha lomaketta: Valitse toimintoruudusta **Erätyö**-välilehdeltä **Loki**.

1. Valitse **Sanoman tiedot** avataksesi **Sanoman tiedot** -ruudun, jossa voit tarkastella kaikkia käsittelyn aikana siepattuja varoituksia ja virheitä.

## <a name="related-resources"></a>Liittyvät resurssit

- [Suunnittelun optimoinnin yleiskatsaus](planning-optimization-overview.md)
- [Suunnittelun optimoinnin aloittaminen](get-started.md)
- [Suunnittelun optimoinnin sopivuusanalyysi](planning-optimization-fit-analysis.md)
- [Suodattimien käyttäminen suunnitelmaan](plan-filters.md)
- [Suunnittelutyön peruuttaminen](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
