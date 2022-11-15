---
title: Suunnitelman historia- ja suunnittelulokien tarkasteleminen
description: Tässä artikkelissa kerrotaan, miten suunnittelutöiden historiatietoja voidaan tarkastella.
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
ms.openlocfilehash: ab469686a009364bf53cb963506fd2107075a283
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740928"
---
# <a name="view-plan-history-and-planning-logs"></a>Suunnitelman historia- ja suunnittelulokien tarkasteleminen

[!include [banner](../../includes/banner.md)]

Tässä artikkelissa kerrotaan, miten suunnittelutöiden historiatietoja voidaan tarkastella Microsoft Dynamics 365 Supply Chain Managementissa.

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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
