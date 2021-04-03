---
title: Myymälöiden asiakashallinta
description: Tässä ohjeaiheessa on tietoja siitä, miten vähittäismyyjät voivat ottaa käyttöön asiakashallintatoimintoja myyntipisteessä Microsoft Dynamics 365 Commercessa.
author: josaw1
manager: AnnBe
ms.date: 03/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: shajain
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 8a1b360ba6a2d32e38e101f25f108094a00190c8
ms.sourcegitcommit: 8a14eac1c27f10c2b1b02ac9ad82339f5e127602
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/05/2021
ms.locfileid: "5555044"
---
# <a name="customer-management-in-stores"></a>Myymälöiden asiakashallinta

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa on tietoja siitä, miten vähittäismyyjät voivat ottaa käyttöön asiakashallintatoimintoja myyntipisteessä Microsoft Dynamics 365 Commercessa.

On tärkeää, että myymälän myyjät voivat luoda ja muokata asiakastietueita myyntipisteessä. Näin he voivat siepata asiakastietojen päivityksiä, kuten sähköpostiosoitteen, puhelinnumeron ja osoitteen. Näistä tiedoista on hyötyä esimerkiksi markkinoinnissa, koska näiden järjestelmien tehokkuus riippuu asiakkaiden tietojen tarkkuudesta.

Myyjät voivat käynnistää asiakkaan luonnin työnkulun kahdesta myyntipisteen kohdasta. He voivat valita painikkeen, joka on yhdistetty **Asiakas – lisää** -toimintoon, tai he voivat valita hakutulossivulla sovelluspalkissa **Luo asiakas**. Molemmissa tapauksissa näyttöön tulee **Uusi asiakas** -valintaikkuna, jossa myyjät voivat syöttää tarvittavat asiakastiedot, kuten asiakkaan nimen, sähköpostiosoitteen, puhelinnumeron, osoitteen sekä mahdolliset yrityksen kannalta olennaiset tiedot. Nämä lisätiedot voi siepata käyttäen asiakkaaseen liittyviä asiakkaan määritteitä. Lisätietoja asiakkaan määritteistä on kohdassa [Asiakkaan määritteet](dev-itpro/customer-attributes.md).

Myyjät voivat myös siepata toissijaisia sähköpostiosoitteita ja puhelinnumeroita. Lisäksi he voivat siepata asiakkaan toivomuksen markkinointitietojen vastaanottamisesta minkä tahansa toissijaisen sähköpostiosoitteen tai puhelinnumeron kautta. Jotta tämä ominaisuus voidaan ottaa käyttöön, vähittäismyyjien on otettava käyttöön **Kerää useita sähköpostiviestejä ja puhelinnumeroita sekä suostumus näille yhteyshenkilöille** -toiminnon **ominaisuudenhallinnan** työtilassa Commerce headquartersissa (**Järjestelmän hallinta \> Työtilat \> Ominaisuuksien hallinta)**.

## <a name="default-customer-properties"></a>Asiakkaan oletusominaisuudet

Vähittäismyyjät voivat käyttää Commerce headquartersin **Kaikki myymälät** -sivua (**Retail ja Commerce \> Kanavat \> Myymälät**), kun halutaan liittää oletusasiakas kuhunkin myymälään. Commerce kopioi sitten oletusasiakkaalle määritetyt ominaisuudet kaikkiin uusiin asiakastietueisiin, jotka luodaan. Esimerkiksi **Luo asiakas** -valintaikkunassa näkyvät myymälään liitetyltä oletusasiakkaalta periytyvät ominaisuudet. Ominaisuuksia ovat asiakastyyppi, asiakasryhmä, kuittiasetukset, valuutta ja kieli. Myös mahdolliset liitokset (asiakkaiden ryhmittelyt) periytyvät myös oletusasiakkaalta. Taloushallinnon dimensiot periytyvät kuitenkin oletusasiakkaaseen liittyvältä asiakasryhmältä, ei itse oletusasiakkaalta.

Myyjät voivat siepata useita asiakkaan osoitteita. Asiakkaan nimi ja puhelinnumero periytyvät kuhunkin osoitteeseen liittyvästä yhteyshenkilöstä. Asiakastietueen **Osoitteet**-pikavälilehdessä on **Tarkoitus**-kenttä, jota myyjät voivat muokata. Jos asiakastyyppi on **Henkilö**, oletusarvo on **Koti**. Jos asiakastyyppi on **Organisaatio**, oletusarvo on **Yritys**. Muita tämän kentän tukemia arvoja ovat **Koti**, **Toimisto**  ja **Postilokero**. Osoitteen **Maa**-kentän arvo periytyy Commerce headquartersissa **Toimintayksikkö**-sivulla (**Organisaation hallinto \> Organisaatiot \> Toimintayksiköt**) määritetystä ensisijaisista osoitteesta.

## <a name="sync-customers-and-async-customers"></a>Synkroniset asiakkaat ja asynkroniset asiakkaat

Commercessa asiakkaan luomisessa on kaksi eri tilaa: Synkroninen ja Asynkroninen. Oletusarvon mukaan asiakkaat luodaan synkronisesti. Toisin sanoen ne luodaan Commerce headquarters -sovelluksessa reaaliaikaisesti. Synkroninen asiakkaan luontitila on hyödyllinen, koska uusia asiakkaita voidaan hakea välittömästi eri kanavien kautta. Sillä on kuitenkin myös haittapuolensa. Koska se luo [Commerce Data Exchange: Real-time Service](dev-itpro/define-retail-channel-communications-cdx.md#realtime-service) -kutsuja Commerce headquarters -sovelluksessa, suorituskykyyn voi vaikuttaa, jos tehdään samanaikaisia asiakkaan luontikutsuja.

Jos **Luo asiakas asynkronisessa tilassa** -asetus on **Kyllä** myymälän toimintoprofiilissa (**Retail ja Commerce \> Kanavan asetukset \> Verkkokaupan määritys \> Toimintoprofiilit**), Real-time Service -kutsuja ei käytetä asiakastietueiden luomiseen kanavatietokannassa. Asynroninen asiakkaan luontitila ei vaikuta Commerce headquarters -ohjelman suorituskykyyn. Jokaiselle uudelle asynkroniselle asiakastietueelle liitetään väliaikainen, yleinen yksilöivä tunnus (GUID), jota käytetään asiakastilin tunnuksena. GUID ei näy myyntipisteen käyttäjille. Sen sijaan käyttäjät näkevät **Odottaa synkronointia** asiakastilin tunnuksena. Vaikka tämä konfiguraatio pakottaa asynkroniseen asiakkaiden luontiin, asiakastietueiden muokkaaminen tapahtuu aina synkronisesti.

### <a name="convert-async-customers-to-sync-customers"></a>Asynkronisten asiakkaiden muuntaminen asynkronisiksi asiakkaiksi

Jos haluat muuntaa asynkroniset asiakkaat synkronoiduksi asiakkaiksi, sinun on ensin suoritettava P-työ, jotta asynkroniset asiakkaat voidaan lähettää Commerce headquarters -ohjelmaan. Suorita sitten **Synkronoi asiakkaat ja yrityskumppanit asynkronisesta tilasta** -työ asiakastilien tunnusten luontia varten. Synkronoi lopuksi uudet asiakastilitunnukset kanaviin suorittamalla **1010**-työ.

### <a name="async-customer-limitations"></a>Asynkronisen asiakkaan rajoitukset

Asynkronisen asiakkaan toiminnallisuuteen liittyy tällä hetkellä seuraavat rajoitukset:

- Asynkronisen asiakkaan tietueita ei voi muokata, ellei asiakasta ole luotu Commerce headquarters -sovelluksessa ja uutta asiakastilin tunnusta ole synkronoitu takaisin kanavaan.
- Liitoksia ei voi liittää asynkronisiin asiakkaisiin. Siksi uudet asynkroniset asiakkaat eivät peri liitoksia oletusasiakkaalta.
- Kanta-asiakaskortteja ei voi myöntää asynkronisille asiakkaille, ellei uutta asiakastilitunnusta ole synkronoitu takaisin kanavaan.
- Toissijaisia sähköpostiosoitteita ja puhelinnumeroita ei voi siepata asynkronisille asiakkaille.

### <a name="customer-creation-in-pos-offline-mode"></a>Asiakkaan luonti myyntipisteen offline-tilassa

Jos myyntipiste siirtyy offline-tilaan, kun asynkronisen asiakkaan luontitila on käytössä, uudet asiakastietueet luodaan asynkronisesti. Jos myyntipiste siirtyy offline-tilaan, kun asynkronisen asiakkaan luontitila on poistettu käytöstä, järjestelmä siirtyy automaattisesti asynkroniseen asiakkaan luontitilaan. Toisin sanoen asiakstietueet voidaan luoda asynkronisesest, vaikka asynkroninen asiakkaan luontitila ei ole käytössä. Siksi Commerce headquartersin järjestelmänvalvojien on luotava ja ajoitettava toistuva erätyö P-työlle, **Synkronoi asiakkaat ja yrityskumppanit asynkronisesta tilasta** -työlle ja **1010**-työlle, jotta kaikki asynkroniset asiakkaat muunnetaan Commerce headquartersissa synkronoiduiksi asiakkaiksi.

> [!NOTE]
> Jos **Suodata jaetut asiakastietotalut** -asetus on **Kyllä** **Commerce-kanavan rakenne** -sivulla (**Retail ja Commerce \> Headquartersin asetuukset \> Commerce-ajastus \> Kanavan tietokantaryhmä**), asiakastietueita ei luoda myyntipisteen offline-tilassa. Lisätietoja on kohdassa [Offline-tietojen poissulkeminen](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion).

## <a name="additional-resources"></a>Lisäresurssit

[Asiakkaan määritteet](dev-itpro/customer-attributes.md)

[Offline-tietojen poissulkeminen](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion)
