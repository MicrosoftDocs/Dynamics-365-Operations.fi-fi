---
title: Myyntipisteen oheislaitteiden ja palveluiden kuntotarkistus
description: Tässä ohjeaiheessa on yleiskuvaus myyntipisteen kuntotarkistustoiminnosta.
author: rubendel
manager: AnnBe
ms.date: 03/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.custom: 141393
ms.assetid: e23e944c-15de-459d-bcc5-ea03615ebf4c
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2019-03-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 2c7e481b37a304188ab672308d915c714547d6f3
ms.sourcegitcommit: 02640a0f63daa9e509146641824ed623c4d69c7f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/16/2020
ms.locfileid: "3265546"
---
# <a name="health-check-for-pos-peripherals-and-services"></a>Myyntipisteen oheislaitteiden ja palveluiden kuntotarkistus

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa on tietoja myyntipisteen kuntotarkistustoiminnosta.

## <a name="overview"></a>Yleiskuvaus

Vähittäiskaupat voivat olla monimutkaisia ympäristöjä, joissa käytetään useita sovelluksia ja laitteita. Toimintojen kasvaessa voi olla vaikeaa varmistaa, että toiminnot sujuvat aina sujuvasti, koska esimerkiksi oheislaitteet voivat mennä epäkuntoon tai ne voidaan poistaa käytöstä vahingossa päivän aikana. Laitteisiin ja palveluihin liittyvien ongelmien vianmääritys voi olla kallista suurissa vähittäismyymälöissä. Pienille toimijoille se on yhtä lailla turhauttavaa.

Microsoft Dynamics 365 Commercen versio 10.0.10 ja uudemmat versiot sisältävät kuntotarkistustoiminnon, jonka avulla voi estää joitakin näistä kustannuksista ja osan turhautumisesta. Tämä toiminto tarjoaa menetelmän, jolla laitteet testataan suoraan myyntipisteessä normaalien toimintojen ulkopuolella. Tämän vuoksi se voi auttaa vähittäismyyjiä havaitsemaan ongelmia ennen kuin ne syntyvät.

## <a name="key-terms"></a>Tärkeimmät termit

| Kausi | kuvaus |
|---|---|
| Oheislaite | Kaikki laitteet, joita myyntipistesovellus käyttää myymälän tapahtumien ja muiden toimintojen suorittamisessa. Esimerkkejä ovat kassat, viivakoodiskannerit ja maksupäätteet. |
| Palveluala | Tässä ohjeaiheessa kerrotaan lisäsovelluksesta, jota myyntipistesovellus tarvitsee tapahtumien ja päivittäisten toimintojen suorittamisessa. Esimerkkejä ovat sovellukset, jotka auttavat vero- tai toimituslaskelmissa. |

## <a name="health-check-operation"></a>Kuntotarkistustoiminto

Kuntotarkistustoiminto on toiminto 717 **Myyntipistetoiminnot**-sivulla Commerce Headquarters -sovelluksessa. Sitä voidaan käyttää, kun myyntipisteen tila on muu kuin kassa. Laiteaseman on kuitenkin oltava aktiivinen.

Oletusarvon mukaan kuntotarkistus testaa vain laitteet, jotka on määritetty rekisterissä olevan laiteaseman laitteistoprofiilissa. Jos kassa käyttää useita laiteasemia päivän aikana, voit tehdä kaikille kuntotarkistuksen, jos yhteys muodostetaan yhteen laiteasemaan kerralla. Varastotason kuntotarkistusta ei ole. On kuitenkin mahdollista, että tämäntyyppinen tarkistus voidaan tehdä Commerce Server -laajennettavuuden kautta.

### <a name="out-of-box-health-checks"></a>Valmiit kuntotarkistukset

| Laji | Yhteys | Lisätietoja |
|---|---|---|
| Tulostin | OPOS | Tämä tarkistus testaa perusobjektien linkityksen ja upotuksen myyntipisteen (OPOS) toimintoihin. Seuraavassa on muutamia esimerkkejä:<ul><li>Avaa: **Avaa** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>Sulje: **DeviceEnabled=False** &gt; **ReleaseDevice** &gt; **Sulje**</li></ul> |
| Rivinäyttö | OPOS | Tämä tarkistus testaa OPOS-perustoiminnot. Seuraavassa on muutamia esimerkkejä:<ul><li>Avaa: **Avaa** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>Sulje: **DeviceEnabled=False** &gt; **ReleaseDevice** &gt; **Sulje**</li></ul> |
| Kaksi näyttöä | Windows | Tämä tarkistus varmistaa, että käyttöjärjestelmä havaitsee toisen Windows-näytön. | 
| Magneettinauhan lukulaite | OPOS | Tämä tarkistus testaa OPOS-perustoiminnot. Seuraavassa on muutamia esimerkkejä:<ul><li>Avaa: **Avaa** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>Sulje: **DeviceEnabled=False** &gt; **ReleaseDevice** &gt; **Sulje**</li></ul> |
| Kassa | OPOS | Tämä tarkistus testaa OPOS-perustoiminnot. Seuraavassa on muutamia esimerkkejä:<ul><li>Avaa: **Avaa** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>Sulje: **DeviceEnabled=False** &gt; **ReleaseDevice** &gt; **Sulje**</li></ul> | 
| Skanneri | OPOS | Tämä tarkistus testaa OPOS-perustoiminnot. Seuraavassa on muutamia esimerkkejä:<ul><li>Avaa: **Avaa** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>Sulje: **DeviceEnabled=False** &gt; **ReleaseDevice** &gt; **Sulje**</li></ul> | 
| Skaalaus | OPOS | Tämä tarkistus testaa OPOS-perustoiminnot. Seuraavassa on muutamia esimerkkejä:<ul><li>Avaa: **Avaa** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>Sulje: **DeviceEnabled=False** &gt; **ReleaseDevice** &gt; **Sulje**</li></ul> |
| PIN-näppäimistö | OPOS | Tämä tarkistus testaa OPOS-perustoiminnot. Seuraavassa on muutamia esimerkkejä:<ul><li>Avaa: **Avaa** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>Sulje: **DeviceEnabled=False** &gt; **ReleaseDevice** &gt; **Sulje**</li></ul> |
| Maksupääte | Maksujen SDK | Tämä tarkistus testaa maksujen SDK:n tarjoamat perusmaksupäätteen toiminnot. <ul><li>Lukitus</li><li>BeginTransaction</li><li>EndTransaction</li><li>ReleaseDevice</li><li>Sulje</li></ul> |

### <a name="using-the-health-check-operation-in-the-pos"></a>Kuntotarkistustoiminnon käyttäminen myyntipisteessä

Kun kuntotarkistustoiminto käynnistetään myyntipisteessä, oikeanpuoleinen ruutu sisältää määritettyjen laitteiden luettelon ja kunkin laitteen tilan. Jos haluat tehdä yksittäisen laitteen kuntotarkistuksen, valitse laite ja valitse sitten **Testaa valittu**. Jos haluat tehdä kuntotarkastuksen kaikille laitteille, valitse **Testaa kaikki**. **Testaa kaikki** -toiminto testaa kaikki laitteet yksi kerralla ja päivittää kunkin laitteen tilan **Tila**-sarakkeeseen.

**Viimeinen tarkistus** -sarakkeessa on tieto kunkin laitteen edellisestä kuntotarkistuksesta.

Jos laite läpäisee kuntotarkistuksen (eli jos virheitä ei löydy), laitteen tilaksi tulee **OK**. Jos kuntotarkistus epäonnistuu, tila osoittaa virheen. Tässä tapauksessa oikeanpuoleisessa ruudussa on virheeseen liittyvät tiedot tai se ohjaa käyttäjää ottamaan yhteyttä järjestelmänvalvojaan.

Joissakin laitteissa, kuten OPOS-näppäinlukituksissa, ei ole valmiita kuntotarkistustestejä. Jos käytettävän laitteen kuntotarkistustestiä ei tunnisteta jollekin käytössä olevalle laitteelle, tilaa **ei tueta**.

### <a name="extending-health-checks"></a>Kuntotarkistusten laajentaminen

Valmiit kuntotarkistustestit määritetään tarjoamaan käyttäjäystävällisiä sanomia tavallisista virheistä. Kaikkia skenaarioita ei kuitenkaan käsitellä. Laajennettavuuden avulla kauppiaat voivat yhdistää käyttäjäystävällisiä sanomia sellaisiin virheisiin, jotka saattavat olla ympäristökohtaisia.

Mukautettuja kuntotarkistuksia voidaan myös määrittää testaamaan laitteita, joita ei tueta, tai testaamaan palveluita, joista myyntipiste on riippuvainen.

## <a name="related-articles"></a>Liittyvät artikkelit

[Modern POS:n (MPOS) ja pilvimyyntipisteen käynnistimen laajennettavuus](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/modern-pos-trigger-extensibility)
