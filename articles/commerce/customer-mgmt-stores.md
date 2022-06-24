---
title: Myymälöiden asiakashallinta
description: Tässä artikkelissa on tietoja siitä, miten vähittäismyyjät voivat ottaa käyttöön asiakashallintatoimintoja myyntipisteessä Microsoft Dynamics 365 Commercessa.
author: gvrmohanreddy
ms.date: 12/10/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: shajain
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 805d0b5894b18e2fc34f481bdc32ada7a4b1aee0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8863484"
---
# <a name="customer-management-in-stores"></a>Myymälöiden asiakashallinta

[!include [banner](includes/banner.md)]

Tässä artikkelissa on tietoja siitä, miten vähittäismyyjät voivat ottaa käyttöön asiakashallintatoimintoja myyntipisteessä Microsoft Dynamics 365 Commercessa.

On tärkeää, että myymälän myyjät voivat luoda ja muokata asiakastietueita myyntipisteessä. Näin he voivat siepata asiakastietojen päivityksiä, kuten sähköpostiosoitteen, puhelinnumeron ja osoitteen. Näistä tiedoista on hyötyä esimerkiksi markkinoinnissa, koska näiden järjestelmien tehokkuus riippuu asiakkaiden tietojen tarkkuudesta.

Myyjät voivat käynnistää asiakkaan luonnin työnkulun kahdesta myyntipisteen kohdasta. He voivat valita painikkeen, joka on yhdistetty **Asiakas – lisää** -toimintoon, tai he voivat valita hakutulossivulla sovelluspalkissa **Luo asiakas**. Molemmissa tapauksissa näyttöön tulee **Uusi asiakas** -valintaikkuna, jossa myyjät voivat syöttää tarvittavat asiakastiedot, kuten asiakkaan nimen, sähköpostiosoitteen, puhelinnumeron, osoitteen sekä mahdolliset yrityksen kannalta olennaiset tiedot. Nämä lisätiedot voi siepata käyttäen asiakkaaseen liittyviä asiakkaan määritteitä. Lisätietoja asiakkaan määritteistä on kohdassa [Asiakkaan määritteet](dev-itpro/customer-attributes.md).

Myyjät voivat myös siepata toissijaisia sähköpostiosoitteita ja puhelinnumeroita. Lisäksi he voivat siepata asiakkaan toivomuksen markkinointitietojen vastaanottamisesta minkä tahansa toissijaisen sähköpostiosoitteen tai puhelinnumeron kautta. Jotta tämä ominaisuus voidaan ottaa käyttöön, vähittäismyyjien on otettava käyttöön **Kerää useita sähköpostiviestejä ja puhelinnumeroita sekä suostumus näille yhteyshenkilöille** -toiminnon **ominaisuudenhallinnan** työtilassa Commerce headquartersissa (**Järjestelmän hallinta \> Työtilat \> Ominaisuuksien hallinta)**.

## <a name="default-customer-properties"></a>Asiakkaan oletusominaisuudet

Vähittäismyyjät voivat käyttää Commerce headquartersin **Kaikki myymälät** -sivua (**Retail ja Commerce \> Kanavat \> Myymälät**), kun halutaan liittää oletusasiakas kuhunkin myymälään. Commerce kopioi sitten oletusasiakkaalle määritetyt ominaisuudet kaikkiin uusiin asiakastietueisiin, jotka luodaan. Esimerkiksi **Luo asiakas** -valintaikkunassa näkyvät myymälään liitetyltä oletusasiakkaalta periytyvät ominaisuudet. Ominaisuuksia ovat **asiakastyyppi**, **asiakasryhmä**, **kuittiasetus**, **kuittisähköposti** **valuutta** ja **kieli**. Myös mahdolliset **liitokset** (asiakkaiden ryhmittelyt) periytyvät myös oletusasiakkaalta. **Taloushallinnon dimensiot** periytyvät kuitenkin oletusasiakkaaseen liittyvältä asiakasryhmältä, ei itse oletusasiakkaalta.

> [!NOTE]
> **Kuittisähköposti**-arvo kopioidaan oletusasiakkaalta vain, jos juuri luoduille asiakkaille ei ole määritetty kuitin sähköpostitunnusta. Jos kuittien sähköpostitunnus on oletusasiakkaalla, kaikki sähköisen kaupan sivustosta luodut asiakkaat saavat saman kuitin sähköpostitunnuksen kuin käyttöliittymää ei ole, joka siepaisi asiakkaan sähköpostitunnuksen. On suositeltavaa jättää **kuittisähköposti**-kenttä tyhjäksi myymälän oletusasiakkaalle ja käyttää sitä vain, jos käytössä on liiketoimintaprosessi, joka riippuu kuitin sähköpostiosoitteesta. 

Myyjät voivat siepata useita asiakkaan osoitteita. Asiakkaan nimi ja puhelinnumero periytyvät kuhunkin osoitteeseen liittyvästä yhteyshenkilöstä. Asiakastietueen **Osoitteet**-pikavälilehdessä on **Tarkoitus**-kenttä, jota myyjät voivat muokata. Jos asiakastyyppi on **Henkilö**, oletusarvo on **Koti**. Jos asiakastyyppi on **Organisaatio**, oletusarvo on **Yritys**. Muita tämän kentän tukemia arvoja ovat **Koti**, **Toimisto**  ja **Postilokero**. Osoitteen **Maa**-kentän arvo periytyy Commerce headquartersissa **Toimintayksikkö**-sivulla (**Organisaation hallinto \> Organisaatiot \> Toimintayksiköt**) määritetystä ensisijaisista osoitteesta.



## <a name="additional-resources"></a>Lisäresurssit

[Asynkroninen asiakkaan luontitila](async-customer-mode.md)

[Asynkronisten asiakkaiden muuntaminen synkronisiksi asiakkaiksi](convert-async-to-sync.md)

[Asiakkaan määritteet](dev-itpro/customer-attributes.md)

[Offline-tietojen poissulkeminen](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion)
