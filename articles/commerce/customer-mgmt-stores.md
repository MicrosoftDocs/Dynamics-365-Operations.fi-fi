---
title: Myymälöiden asiakashallinta
description: Tässä ohjeaiheessa on tietoja siitä, miten vähittäismyyjät voivat ottaa käyttöön asiakashallintatoimintoja myyntipisteessä Microsoft Dynamics 365 Commercessa.
author: josaw1
ms.date: 09/01/2021
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
ms.openlocfilehash: 395bc7049ba32c1e572730e482b81613a4873c59
ms.sourcegitcommit: 1707cf45217db6801df260ff60f4648bd9a4bb68
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/23/2021
ms.locfileid: "7675222"
---
# <a name="customer-management-in-stores"></a>Myymälöiden asiakashallinta

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa on tietoja siitä, miten vähittäismyyjät voivat ottaa käyttöön asiakashallintatoimintoja myyntipisteessä Microsoft Dynamics 365 Commercessa.

On tärkeää, että myymälän myyjät voivat luoda ja muokata asiakastietueita myyntipisteessä. Näin he voivat siepata asiakastietojen päivityksiä, kuten sähköpostiosoitteen, puhelinnumeron ja osoitteen. Näistä tiedoista on hyötyä esimerkiksi markkinoinnissa, koska näiden järjestelmien tehokkuus riippuu asiakkaiden tietojen tarkkuudesta.

Myyjät voivat käynnistää asiakkaan luonnin työnkulun kahdesta myyntipisteen kohdasta. He voivat valita painikkeen, joka on yhdistetty **Asiakas – lisää** -toimintoon, tai he voivat valita hakutulossivulla sovelluspalkissa **Luo asiakas**. Molemmissa tapauksissa näyttöön tulee **Uusi asiakas** -valintaikkuna, jossa myyjät voivat syöttää tarvittavat asiakastiedot, kuten asiakkaan nimen, sähköpostiosoitteen, puhelinnumeron, osoitteen sekä mahdolliset yrityksen kannalta olennaiset tiedot. Nämä lisätiedot voi siepata käyttäen asiakkaaseen liittyviä asiakkaan määritteitä. Lisätietoja asiakkaan määritteistä on kohdassa [Asiakkaan määritteet](dev-itpro/customer-attributes.md).

Myyjät voivat myös siepata toissijaisia sähköpostiosoitteita ja puhelinnumeroita. Lisäksi he voivat siepata asiakkaan toivomuksen markkinointitietojen vastaanottamisesta minkä tahansa toissijaisen sähköpostiosoitteen tai puhelinnumeron kautta. Jotta tämä ominaisuus voidaan ottaa käyttöön, vähittäismyyjien on otettava käyttöön **Kerää useita sähköpostiviestejä ja puhelinnumeroita sekä suostumus näille yhteyshenkilöille** -toiminnon **ominaisuudenhallinnan** työtilassa Commerce headquartersissa (**Järjestelmän hallinta \> Työtilat \> Ominaisuuksien hallinta)**.

## <a name="default-customer-properties"></a>Asiakkaan oletusominaisuudet

Vähittäismyyjät voivat käyttää Commerce headquartersin **Kaikki myymälät** -sivua (**Retail ja Commerce \> Kanavat \> Myymälät**), kun halutaan liittää oletusasiakas kuhunkin myymälään. Commerce kopioi sitten oletusasiakkaalle määritetyt ominaisuudet kaikkiin uusiin asiakastietueisiin, jotka luodaan. Esimerkiksi **Luo asiakas** -valintaikkunassa näkyvät myymälään liitetyltä oletusasiakkaalta periytyvät ominaisuudet. Ominaisuuksia ovat **asiakastyyppi**, **asiakasryhmä**, **kuittiasetus**, **kuittisähköposti** **valuutta** ja **kieli**. Myös mahdolliset **liitokset** (asiakkaiden ryhmittelyt) periytyvät myös oletusasiakkaalta. **Taloushallinnon dimensiot** periytyvät kuitenkin oletusasiakkaaseen liittyvältä asiakasryhmältä, ei itse oletusasiakkaalta.

> [!NOTE]
> **Kuittisähköposti**-arvo kopioidaan oletusasiakkaalta vain, jos juuri luoduille asiakkaille ei ole määritetty kuitin sähköpostitunnusta. Jos kuittien sähköpostitunnus on oletusasiakkaalla, kaikki sähköisen kaupan sivustosta luodut asiakkaat saavat saman kuitin sähköpostitunnuksen kuin käyttöliittymää ei ole, joka siepaisi asiakkaan sähköpostitunnuksen. On suositeltavaa jättää **kuittisähköposti**-kenttä tyhjäksi myymälän oletusasiakkaalle ja käyttää sitä vain, jos käytössä on liiketoimintaprosessi, joka riippuu kuitin sähköpostiosoitteesta. 

Myyjät voivat siepata useita asiakkaan osoitteita. Asiakkaan nimi ja puhelinnumero periytyvät kuhunkin osoitteeseen liittyvästä yhteyshenkilöstä. Asiakastietueen **Osoitteet**-pikavälilehdessä on **Tarkoitus**-kenttä, jota myyjät voivat muokata. Jos asiakastyyppi on **Henkilö**, oletusarvo on **Koti**. Jos asiakastyyppi on **Organisaatio**, oletusarvo on **Yritys**. Muita tämän kentän tukemia arvoja ovat **Koti**, **Toimisto**  ja **Postilokero**. Osoitteen **Maa**-kentän arvo periytyy Commerce headquartersissa **Toimintayksikkö**-sivulla (**Organisaation hallinto \> Organisaatiot \> Toimintayksiköt**) määritetystä ensisijaisista osoitteesta.

## <a name="sync-customers-and-async-customers"></a>Synkroniset asiakkaat ja asynkroniset asiakkaat

> [!IMPORTANT]
> Kun myyntipiste siirtyy offline-tilaan, järjestelmä luo asiakkaat automaattisesti asynkronisesti, vaikka asynkronisen asiakasluonnin tila olisi pois käytöstä. Siksi Commerce-pääkonttorin järjestelmänvalvojien on riippumatta siitä, oletko valinnut synkronisen vai asynkronisen asiakasluonnin, luotava ja ajoitettava toistuva erätyö **P-työlle**, **Synkronoi asiakkaat ja yrityskumppanit asynkronisesta tilasta** -työlle (ennen "**Synkronoi asiakkaat ja yrityskumppanit asynkronisesta tilasta** -työ") ja **1010**-työlle, jotta kaikki asynkroniset asiakkaat muunnetaan Commerce-pääkonttorissa synkronoiduiksi asiakkaiksi.

Commercessa asiakkaan luomisessa on kaksi eri tilaa: Synkroninen ja Asynkroninen. Oletusarvon mukaan asiakkaat luodaan synkronisesti. Toisin sanoen ne luodaan Commerce headquarters -sovelluksessa reaaliaikaisesti. Synkroninen asiakkaan luontitila on hyödyllinen, koska uusia asiakkaita voidaan hakea välittömästi eri kanavien kautta. Sillä on kuitenkin myös haittapuolensa. Koska se luo [Commerce Data Exchange: Real-time Service](dev-itpro/define-retail-channel-communications-cdx.md#realtime-service) -kutsuja Commerce headquarters -sovelluksessa, suorituskykyyn voi vaikuttaa, jos tehdään samanaikaisia asiakkaan luontikutsuja.

Jos **Luo asiakas asynkronisessa tilassa** -asetus on **Kyllä** myymälän toimintoprofiilissa (**Retail ja Commerce \> Kanavan asetukset \> Verkkokaupan määritys \> Toimintoprofiilit**), Real-time Service -kutsuja ei käytetä asiakastietueiden luomiseen kanavatietokannassa. Asynroninen asiakkaan luontitila ei vaikuta Commerce headquarters -ohjelman suorituskykyyn. Jokaiselle uudelle asynkroniselle asiakastietueelle liitetään väliaikainen, yleinen yksilöivä tunnus (GUID), jota käytetään asiakastilin tunnuksena. GUID ei näy myyntipisteen käyttäjille. Sen sijaan käyttäjät näkevät **Odottaa synkronointia** asiakastilin tunnuksena. 

### <a name="convert-async-customers-to-sync-customers"></a>Asynkronisten asiakkaiden muuntaminen asynkronisiksi asiakkaiksi

Jos haluat muuntaa asynkroniset asiakkaat synkronoiduksi asiakkaiksi, sinun on ensin suoritettava **P-työ**, jotta asynkroniset asiakkaat voidaan lähettää Commerce headquarters -ohjelmaan. Suorita sitten **Synkronoi asiakkaat ja yrityskumppanit asynkronisesta tilasta** -työ (ennen "**Synkronoi asiakkaat ja yrityskumppanit asynkronisesta tilasta** -työ) luodaksesi asiakastilitunnuksia. Synkronoi lopuksi uudet asiakastilitunnukset kanaviin suorittamalla **1010**-työ.

### <a name="async-customer-limitations"></a>Asynkronisen asiakkaan rajoitukset

Asynkronisen asiakkaan toiminnallisuuteen liittyy tällä hetkellä seuraavat rajoitukset:

- Asynkronisen asiakkaan tietueita ei voi muokata, ellei asiakasta ole luotu Commerce headquarters -sovelluksessa ja uutta asiakastilin tunnusta ole synkronoitu takaisin kanavaan. Siksi osoitetta ei voi tallentaa asynkroniselle asiakkaalle, ennen kuin asiakas on synkronoitu Commerce-pääkonttoriin, koska asiakkaan osoitteen lisääminen toteutetaan sisäisesti asiakasprofiilin muokkaustoimintona. Jos **Ota asiakkaiden osoitteiden asynkroninen luonti käyttöön** -ominaisuus sen sijaan on käytössä, asiakkaiden osoitteet voidaan tallentaa myös asynkronisten asiakkaiden osalta.
- Liitoksia ei voi liittää asynkronisiin asiakkaisiin. Siksi uudet asynkroniset asiakkaat eivät peri liitoksia oletusasiakkaalta.
- Kanta-asiakaskortteja ei voi myöntää asynkronisille asiakkaille, ellei uutta asiakastilitunnusta ole synkronoitu takaisin kanavaan.
- Toissijaisia sähköpostiosoitteita ja puhelinnumeroita ei voi siepata asynkronisille asiakkaille.

Vaikka jotkin edellä mainituista rajoituksista saavat sinut kallistumaan asiakkaiden synkronoinnin puoleen yrityksessäsi, Commerce-tiimi pyrkii tekemään asynkronisten asiakkaiden ominaisuudet vastaamaan tarkemmin synkronoitujen asiakkaiden ominaisuuksia. Esimerkiksi Commerce-versiosta 10.0.22 alkaen uusi **Ota asiakkaiden osoitteiden asynkroninen luonti käyttöön** -toiminto, joka voidaan ottaa käyttöön **Ominaisuuksien hallinta** -työtilassa, tallentaa uudet asiakkaiden osoitteet asynkronisesti sekä asynkronisten että synkronoitujen asiakkaiden osalta. Näiden osoitteiden Commerce-pääkonttorin asiakasprofiiliin tallentamista varten sinun on luotava ja ajoitettava toistuva erätyö **P-työlle**, **Synkronoi asiakkaat ja yrityskumppanit asynkronisesta tilasta** -työlle ja **1010**-työlle, jotta kaikki asynkroniset asiakkaat muunnetaan Commerce-pääkonttorissa synkronoiduiksi asiakkaiksi.

### <a name="customer-creation-in-pos-offline-mode"></a>Asiakkaan luonti myyntipisteen offline-tilassa

Kun myyntipiste siirtyy offline-tilaan, järjestelmä luo asiakkaat automaattisesti asynkronisesti, vaikka asynkronisen asiakasluonnin tila olisi pois käytöstä. Siksi, kuten aiemmin mainittiin, Commerce-pääkonttorin järjestelmänvalvojien on luotava ja ajoitettava toistuva erätyö **P-työlle**, **Synkronoi asiakkaat ja yrityskumppanit asynkronisesta tilasta** -työlle ja **1010**-työlle, jotta kaikki asynkroniset asiakkaat muunnetaan Commerce-pääkonttorissa synkronoiduiksi asiakkaiksi.

> [!NOTE]
> Jos **Suodata jaetut asiakastietotalut** -asetus on **Kyllä** **Commerce-kanavan rakenne** -sivulla (**Retail ja Commerce \> Headquartersin asetuukset \> Commerce-ajastus \> Kanavan tietokantaryhmä**), asiakastietueita ei luoda myyntipisteen offline-tilassa. Lisätietoja on kohdassa [Offline-tietojen poissulkeminen](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion).

## <a name="additional-resources"></a>Lisäresurssit

[Asiakkaan määritteet](dev-itpro/customer-attributes.md)

[Offline-tietojen poissulkeminen](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion)
