---
title: Suunnitelman historia- ja suunnittelulokien tarkasteleminen
description: Tässä artikkelissa käsitellään, miten suunnittelun optimointitoiminnon käynnistämien suunnittelutöiden historiatietoja tarkastellaan.
author: t-benebo
ms.date: 06/01/2020
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
ms.author: benebotg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: b2c9257fc67a06b57418b2f5b035b2b540131405
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8863937"
---
# <a name="view-plan-history-and-planning-logs"></a>Suunnitelman historia- ja suunnittelulokien tarkasteleminen

[!include [banner](../../includes/banner.md)]

Tässä artikkelissa käsitellään, miten Microsoft Dynamics 365 Supply Chain Managementin suunnittelun optimointitoiminnon käynnistämien suunnittelutöiden historiatietoja tarkastellaan.

Voit tarkastella suunnitelman historiaa avaamalla suunnitelman valitsemalla ensin **Pääsuunnittelu** \> **Asetukset** \> **Suunnitelmat** \> **Pääsuunnitelmat** ja sitten **Historia**. Historiatiedoissa on luettelo kaikista valitun suunnitelman töistä. Luettelo sisältää valmiit ja aktiiviset työt.

Järjestelmä säilyttää pääsuunnitelmaa kohden enintään 60 historiatietuetta ja poistaa tietueita, jotka ovat yli 30 päivää vanhoja. Aina kun suoritat uuden pääsuunnittelun laskennan, järjestelmä lisää uuden historiatietueen ja puhdistaa sitten vanhimmat tietueet tarpeen mukaan.

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
