---
title: Yritysten välinen suunnittelu
description: Tässä artikkelissa käsitellään konsernin sisäistä suunnittelua ja konsernin sisäisen suunnittelun määrittämistä Microsoft Dynamics 365 Supply Chain Managementin suunnittelun optimoinnin avulla.
author: t-benebo
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 6ef551e1c2c4d90510f967855a5aa61646dc8eab
ms.sourcegitcommit: d3f7a56eaf788d223ece4cedac4a319eaf5f6112
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/19/2022
ms.locfileid: "9538562"
---
# <a name="intercompany-planning"></a>Konsernin sisäinen suunnittelu

[!include [banner](../../includes/banner.md)]

Joissakin organisaatioissa logistiikkatoiminnot ovat riippuvaisia organisaation muista yrityksistä. Näitä toimintoja käsitellään konsernin sisäisten myyntien ja ostojen avulla, koska kullakin yrityksellä on erillinen tilikartta.

Tässä artikkelissa käsitellään konsernin sisäistä suunnittelua ja konsernin sisäisen suunnittelun määrittämistä Microsoft Dynamics 365 Supply Chain Managementin suunnittelun optimoinnin avulla.

Tässä artikkelissa käytetään seuraavia tärkeitä konsernin sisäisiä käsitteitä:

- **Yläpuolinen** – Suhteellinen viittaus vahvistus- tai toimitusketjussa. Se ilmaisee raaka-aineen toimittajaan päin suuntautuvaa liikettä.
- **Alapuolinen** – Suhteellinen viittaus vahvistus- tai toimitusketjussa. Se ilmaisee asiakkaaseen päin suuntautuvaa liikettä.
- **Suunniteltu konsernin sisäinen kysyntä** – tuotteen suunniteltu kysyntä yrityksessä sen perusteella, mikä on tuotteen suunniteltu kysyntä alapuolisessa yrityksessä.

Pääsuunnittelussa yhden yrityksen suunnitelma voi sisältää suunnitellun konsernin sisäisen kysynnän, joka liittyy suunniteltuihin tilaukseen toisen yrityksen suunnitelmasta: Tämä ominaisuus on kätevä, sillä sen avulla saada täysi näkyvyys eri yritysten suunniteltuihin tilauksiin. Se myös varmistaa, että kaikki tarvittavat suunnittelut toimitustilaukset luodaan ilman, että kyseiset suunnitellut tilaukset olisi vahvistettava konsernin sisäistä kysyntää varten.

Jos pääsuunnittelu suoritetaan pääsuunnitelmasta, joka sisältää suunnitellun alapuolisen kysynnän, liittyvien konsernin sisäisten toimittajien suunnitellut ostotilaukset sisällytetään suunnitelmaan kysyntänä.

## <a name="required-setup"></a>Tarvittavat määritykset

Järjestelmä on valmisteltava konsernin sisäisen suunnittelun käyttöä varten seuraavasti:

1. Tarvittavat tuotteet on vapautettava kaikkiin tarvittaviin yrityksiin. Lisätietoja on kohdassa [Konsernin sisäisen kaupan määrittäminen ja käyttäminen Dynamics 365 Supply Chain Managementissa](/training/modules/configure-use-intercompany-trade-dyn365-supply-chain-mgmt/).
1. Alapuolinen kysyntä on katettava ostoilla sellaiselta toimittajalta, jolla on konsernin sisäinen suhde yläpuoliseen yritykseen ja tarvittaviin oletusvarastodimensioihin (toimipaikka ja varasto) asiakkaalla. Lisätietoja on kohdassa [Konsernin sisäisen kaupan määrittäminen ja käyttäminen Dynamics 365 Supply Chain Managementissa](/training/modules/configure-use-intercompany-trade-dyn365-supply-chain-mgmt/).
1. Yläpuolisen yrityksen pääsuunnitelman on sisällettävä suunniteltu alapuolinen kysyntä. Alapuolisissa suunnitelmissa on myös määritettävä tarvittava yritys ja pääsuunnitelma.

## <a name="include-planned-downstream-demand"></a>Sisällytä suunniteltu tuotantovirran kysyntä

Pääsuunnitelma määritetään sisältämään suunniteltu alapuolinen kysyntä seuraavasti:

1. Siirry kohtaan **Pääsuunnittelu \> Määritykset \> Suunnitelmat \> Pääsuunnitelmat**.
1. Valitse tai luo pääsuunnitelma.
1. Määritä **Konsernin sisäinen suunnittelu** -pikavälilehdessä seuraavat kentät:

    - **Sisällytä suunniteltu alapuolinen kysyntä** – määritä asetukseksi *Kyllä*, jolloin konsernin sisäinen suunnittelu on käytössä pääsuunnitelmassa:
    - **Alapuoliset suunnitelmat** – jos **Sisällytä suunniteltu alapuolinen kysyntä** -asetukseksi on määritetty *Kyllä*, lisää muiden yritysten pääsuunnitelmia työkalurivin ja ruudukon avulla.

## <a name="peg-across-companies-by-using-multilevel-pegging"></a>Yritysten välinen tarvekohdistus monitasoisen tarvekohdistuksen avulla

Monitasoisessa tarvekohdistuksessa yritysten välistä tarvekohdistusta tarkastelemalla nähdään toimituksen kattaman kysynnän alkuperäinen lähde:

Monitasoisen tarvekohdistuksen tietoja voi tarkastella seuraavasti:

1. Valitse **Pääsuunnittelu \> Pääsuunnittelu \> Suunnitellut tilaukset**.
1. Valitse tai avaa suunniteltu tilaus.
1. Valitse sitten toimintoruudussa **Näytä**-välilehden **Tarpeet**-ryhmässä **Monitasoinen tarvekohdistus**.

### <a name="intercompany-example-that-involves-two-companies"></a>Kaksi konsernin sisäistä yritystä sisältävä esimerkki

Tässä esimerkissä suunniteltu tuotantotilaus luodaan USMF-yrityksessä kattamaan myyntitilaus DEMF-yrityksessä. USMF-yrityksessä suora kysyntä on suunniteltu konsernin sisäinen kysyntä. Jotta tämä kysyntä näkyisi USMF-yrityksessä, pääsuunnittelu suoritetaan ensin DEMF- ja sitten USMF-yrityksessä.

Seuraavassa kuvassa näkyy, miltä tämä esimerkki näyttäisi suunnittelun tuotantotilauksen **Monitasoinen tarvekohdistus** -sivulla.

![Kaksi konsernin sisäistä yritystä sisältävä esimerkki.](media/IntercompanyPlanning1.png)

### <a name="intercompany-example-that-involves-three-companies"></a>Kolme konsernin sisäistä yritystä sisältävä esimerkki

Tässä esimerkissä suunniteltu ostotilaus luodaan USMF-yrityksessä kattamaan myyntitilaus FRRT-yrityksessä. DEMF- ja USMF-yrityksissä suora kysyntä on suunniteltu konsernin sisäinen kysyntä. Jotta tämä kysyntä näkyisi USMF-yrityksessä, pääsuunnittelu suoritetaan ensin FRRT-, sitten DEMF- ja lopulta USMF-yrityksessä.

Seuraavassa kuvassa näkyy, miltä tämä esimerkki näyttäisi suunnittelun tuotantotilauksen **Monitasoinen tarvekohdistus** -sivulla.

![Kolme konsernin sisäistä yritystä sisältävä esimerkki.](media/IntercompanyPlanning2.png)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
