---
title: Kustannustapahtuman yksiköt
description: Tässä artikkelissa on tietoja kustannustapahtuman yksiköistä, joiden avulla kustannuksen arvo voidaan jakaa kustannusalueen sisältöön käyttämällä jako-osuuden menetelmän valintaa.
author: yufeihuang
ms.date: 05/27/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-05-27
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 0084d47bf85050749b2668d273db07670aaeae2a
ms.sourcegitcommit: 5b34b41ae74269ba639e2876bc5862ef468da1cc
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/15/2022
ms.locfileid: "9166800"
---
# <a name="cost-transaction-entities"></a>Kustannustapahtuman yksiköt

[!include [banner](../includes/banner.md)]

## <a name="apportionment"></a>Jako-osuus

Aiheutunut kustannus mahdollistaa kustannuksen arvon jakamisen kustannusalueen (esim. matka, lähetyskontti) sisältöön käyttämällä jako-osuuden menetelmän valintaa. Jako-osuuden menetelmä määritetään osana automaattisten kustannusten määritystä, joka perustuu liiketoimintasääntöihin. Se vedetään läpi kustannuksen osana, kun matkarivi luodaan.

### <a name="configure-the-apportionment-mapping-for-use-with-data-entities"></a>Jako-osuuden yhdistämisen määrittäminen tietoyksikkökäyttöä varten

Kun kustannus luodaan ulkoisesta lähteestä, kuten huolitsijasta, tämä ulkoinen lähde ei voi määrittää kustannusarvon ensisijaista jako-osuuden menetelmää. Jako-osuuden yhdistäminen määrittelee oletusarvoisen jako-osuuden menetelmän kutakin kustannustyyppikoodia kohden. Jako-osuuden yhdistämismäärityksen taulukkoa käytetään **Jako-osuuden yhdistämismääritys** -sivulta Microsoft Dynamics 365 Supply Chain Managementissa (**Aiheutunut kustannus \> Kustannuslaskennan asetukset \> Jako-osuuden yhdistämismääritys**).

Jos yhdistämiskombinaatio on määritetty ja kustannustyyppikoodia vastaava kustannus on luotu käyttämällä kustannustapahtuman yksikköä, käytetään yhdistettyä jako-osuuden menetelmää sen sijaan, että käytettäisiin mitään yksikölle annettua arvoa.

Jos määritystaulukossa ei ole arvoa, mutta yksikölle on annettu arvo, käytetään annettua arvoa.

Jos arvo puuttuu joko yhdistämistaulukosta tai yksikölle lähetetystä tietueesta, luonti epäonnistuu.

### <a name="apportionment-mapping-itmapportionmentmapping"></a>Jako-osuuden yhdistämismääritys (ITMApportionmentMapping)

Jako-osuuden yhdistämismäärityksen yksikkö (`ITMApportionmentMapping`) luo jako-osuuden yhdistämismäärityksen suhteita ja antaa käyttäjille mahdollisuuden luoda ja päivittää tietueita.

| Nimi | Yhdistämismääritys | Tietotyyppi | Avain | Pakollinen |
|---|---|---|---|---|
| Jakomenetelmä | ITMApportionmentMapping.ApportionmentMethod | Int | En | En |
| Kustannustyypin koodi | ITMApportionmentMapping.ShipCostTypeId | Nvarchar(20) | **Kyllä** | En |

## <a name="voyage-costs-itmcosttransvoyageentity"></a>Matkan kustannukset (ITMCostTransVoyageEntity)

Matkan kustannusyksikkö (`ITMCostTransVoyageEntity`) luo matkan kustannustapahtumat, joita käytetään matkatasolla. Tuontiprosessin aikana järjestelmä käyttää **Luokka**- ja **Jako-osuuden menetelmä** -arvoja, jotka sisältyvät yksikköön, jotta voidaan määrittää, miten kustannuksen arvo jaetaan matkan sisällössä.

| Nimi | Yhdistämismääritys | Tietotyyppi | Avain | Pakollinen |
|---|---|---|---|---|
| Jakomenetelmä | ITMCostTrans.ApportionmentMethod | Int | En | En |
| Kustannusarvo | ITMCostTrans.CostValue | Numeric(32, 6) | En | En |
| Valuutta | ITMCostTrans.CurrencyCode | Nvarchar(3) | En | **Kyllä** |
| Rivinumero | ITMCostTrans.LineNum | Numeric(32, 16) | **Kyllä** | En |
| Linkitetty kustannustyyppi | ITMCostTrans.LinkCostTypeId | Nvarchar(20) | En | En |
| Vähimmäiskustannus | ITMCostTrans.MinCostAmount | Numeric(32, 6) | En | En |
| Luokka | ITMCostTrans.ShipCostCategory | Int | En | En |
| Kustannustyypin koodi | ITMCostTrans.ShipCostTypeId | Nvarchar(20) | En | En |
| Yritys | ITMCostTrans.ShipDataArea | Nvarchar(4) | En | **Kyllä** |
| Matka | ITMCostTrans.TransRecId | Nvarchar(20) | **Kyllä** | En |
| Nimikkeen arvonlisäveroryhmä | ITMCostTrans.TaxItemGroup | Nvarchar(10) | En | En |

## <a name="shipping-container-costs-itmcosttransshippingcontainerentity"></a>Lähetyskontin kustannukset (ITMCostTransShippingContainerEntity)

Lähetyskontin kustannusten yksikkö (`ITMCostTransShippingContainerEntity`) luo lähetyskontin kustannukset, joita käytetään lähetyskonttitasolla. Tuontiprosessin aikana järjestelmä käyttää **Luokka**- ja **Jako-osuuden menetelmä** -arvoja, jotka sisältyvät yksikköön, jotta voidaan määrittää, miten kustannuksen arvo jaetaan lähetyskontin sisällössä.

Kentät **Yhdistelmä**, **Etappi** ja **Linkitetty etappi** kuuluvat tietueille, joissa **Kustannusalue**-arvo on *Lähetyskontti*. Siksi niitä ei ole muiden kustannusalueiden tietoyksiköissä.

| Nimi | Yhdistämismääritys | Tietotyyppi | Avain | Pakollinen |
|---|---|---|---|---|
| Yhdistelmä | ITMCostTrans.AggregatedCost | Int | En | En |
| Jakomenetelmä | ITMCostTrans.ApportionmentMethod | Int | En | En |
| Kustannusarvo | ITMCostTrans.CostValue | Numeric(32, 6) | En | En |
| Valuutta | ITMCostTrans.CurrencyCode | Nvarchar(3) | En | **Kyllä** |
| Rivinumero | ITMCostTrans.LineNum | Numeric(32, 16) | **Kyllä** | En |
| Linkitetty kustannustyyppi | ITMCostTrans.LinkCostTypeId | Nvarchar(20) | En | En |
| Linkitetty etappi | ITMCostTrans.LinkLegId | Nvarchar(20) | En | En |
| Vähimmäiskustannus | ITMCostTrans.MinCostAmount | Numeric(32, 6) | En | En |
| Lähetyskontti | ITMCostTrans.TransRecId | Nvarchar(20) | **Kyllä** | En |
| Luokka | ITMCostTrans.ShipCostCategory | Int | En | En |
| Kustannustyypin koodi | ITMCostTrans.ShipCostTypeId | Nvarchar(20) | En | En |
| Yritys | ITMCostTrans.ShipDataArea | Nvarchar(4) | En | **Kyllä** |
| Matka | ITMCostTrans.TransRecId | Nvarchar(20) | **Kyllä** | En |
| Etappi | ITMCostTrans.ShipLegId | Nvarchar(20) | En | En |
| Nimikkeen arvonlisäveroryhmä | ITMCostTrans.TaxItemGroup | Nvarchar(10) | En | En |

## <a name="folio-costs-itmcosttransfolioentity"></a>Pakkauksen kustannukset (ITMCostTransFolioEntity)

Pakkauksen kustannusyksikkö (`ITMCostTransFolioEntity`) luo kustannustapahtumatietueet, joita käytetään pakkaustasolla. Tuontiprosessin aikana järjestelmä käyttää **Luokka**- ja **Jako-osuuden menetelmä** -arvoja, jotka sisältyvät yksikköön, jotta voidaan määrittää, miten kustannuksen arvo jaetaan kunkin pakkauksen sisällössä.

| Nimi | Yhdistämismääritys | Tietotyyppi | Avain | Pakollinen |
|---|---|---|---|---|
| Jakomenetelmä | ITMCostTrans.ApportionmentMethod | Int | En | En |
| Kustannusarvo | ITMCostTrans.CostValue | Numeric(32, 6) | En | En |
| Valuutta | ITMCostTrans.CurrencyCode | Nvarchar(3) | En | **Kyllä** |
| Rivinumero | ITMCostTrans.LineNum | Numeric(32, 16) | **Kyllä** | En |
| Linkitetty kustannustyyppi | ITMCostTrans.LinkCostTypeId | Nvarchar(20) | En | En |
| Vähimmäiskustannus | ITMCostTrans.MinCostAmount | Numeric(32, 6) | En | En |
| Luokka | ITMCostTrans.ShipCostCategory | Int | En | En |
| Kustannustyypin koodi | ITMCostTrans.ShipCostTypeId | Nvarchar(20) | En | En |
| Yritys | ITMCostTrans.ShipDataArea | Nvarchar(4) | En | **Kyllä** |
| Lasku | ITMCostTrans.TransRecId | Nvarchar(20) | **Kyllä** | En |
| Nimikkeen arvonlisäveroryhmä | ITMCostTrans.TaxItemGroup | Nvarchar(10) | En | En |

## <a name="purchase-order-costs-itmcosttranspurchaseentity"></a>Ostotilauksen kustannukset (ITMCostTransPurchaseEntity)

Ostotilauksen kustannusyksikkö (`ITMCostTransPurchaseEntity`) luo kustannustapahtumat, joita käytetään ostotilauksen otsikossa. Tuontiprosessin aikana järjestelmä käyttää **Luokka**- ja **Jako-osuuden menetelmä** -arvoja, jotka sisältyvät yksikköön, jotta voidaan määrittää, miten kustannuksen arvo jaetaan kunkin pakkauksen sisällössä.

| Nimi | Yhdistämismääritys | Tietotyyppi | Avain | Pakollinen |
|---|---|---|---|---|
| Jakomenetelmä | ITMCostTrans.ApportionmentMethod | Int | En | En |
| Kustannusarvo | ITMCostTrans.CostValue | Numeric(32, 6) | En | En |
| Valuutta | ITMCostTrans.CurrencyCode | Nvarchar(3) | En | **Kyllä** |
| Rivinumero | ITMCostTrans.LineNum | Numeric(32, 16) | **Kyllä** | En |
| Linkitetty kustannustyyppi | ITMCostTrans.LinkCostTypeId | Nvarchar(20) | En | En |
| Vähimmäiskustannus | ITMCostTrans.MinCostAmount | Numeric(32, 6) | En | En |
| Ostotilaus | ITMCostTrans.TransRecId | Nvarchar(20) | **Kyllä** | En |
| Luokka | ITMCostTrans.ShipCostCategory | Int | En | En |
| Kustannustyypin koodi | ITMCostTrans.ShipCostTypeId | Nvarchar(20) | En | En |
| Yritys | ITMCostTrans.ShipDataArea | Nvarchar(4) | En | **Kyllä** |
| Nimikkeen arvonlisäveroryhmä | ITMCostTrans.TaxItemGroup | Nvarchar(10) | En | En |

## <a name="item-costs-itmcosttransitementity"></a>Nimikekustannukset (ITMCostTransItemEntity)

Nimikekustannusyksikkö (`ITMCostTransItemEntity`) luo kustannustapahtumat, joita käytetään nimiketasolla. Tämä yksikkö on vain ostotilausrivien nimikkeiden käytössä. Kustannusarvo kohdistetaan riville kokonaisuudessaan.

Kentät **Oikaisusumma** ja **Arvon oikaisu** ovat rivitason kustannusalueita varten. Siksi niitä ei ole muiden kustannusalueiden tietoyksiköissä.

| Nimi | Yhdistämismääritys | Tietotyyppi | Avain | Pakollinen |
|---|---|---|---|---|
| Oikaisusumma | ITMCostTrans.AdjustmentAmount | Numeric(32, 6) | En | En |
| Kustannusarvo | ITMCostTrans.CostValue | Numeric(32, 6) | En | En |
| Valuutta | ITMCostTrans.CurrencyCode | Nvarchar(3) | En | **Kyllä** |
| Rivinumero | ITMCostTrans.LineNum | Numeric(32, 16) | **Kyllä** | En |
| Linkitetty kustannustyyppi | ITMCostTrans.LinkCostTypeId | Nvarchar(20) | En | En |
| Vähimmäiskustannus | ITMCostTrans.MinCostAmount | Numeric(32, 6) | En | En |
| Ostotilaus | ITMCostTrans.TransRecId | Nvarchar(20) | **Kyllä** | En |
| Ostotilausrivin numero | ITMCostTrans.TransRecId | Nvarchar(20) | **Kyllä** | En |
| Luokka | ITMCostTrans.ShipCostCategory | Int | En | En |
| Kustannustyypin koodi | ITMCostTrans.ShipCostTypeId | Nvarchar(20) | En | En |
| Yritys | ITMCostTrans.ShipDataArea | Nvarchar(4) | En | **Kyllä** |
| Nimikkeen arvonlisäveroryhmä | ITMCostTrans.TaxItemGroup | Nvarchar(10) | En | En |
| Arvon oikaisu | ITMCostTrans.ValueAdjustmentMethod | Int | En | En |

## <a name="transfer-line-costs-itmcosttranstransferlineentity"></a>Siirtorivien kustannukset (ITMCostTransTransferLineEntity)

Siirtorivien kustannusyksikkö (`ITMCostTransTransferLineEntity`) luo kustannustapahtumat, joita käytetään siirtotilausrivitasolla. Näiden kustannusten arvo kohdistetaan siirtotilausriville kokonaisuudessaan.

Kentät **Oikaisusumma** ja **Arvon oikaisu** ovat rivitason kustannusalueita varten. Siksi niitä ei ole muiden kustannusalueiden tietoyksiköissä.

| Nimi | Yhdistämismääritys | Tietotyyppi | Avain | Pakollinen |
|---|---|---|---|---|
| Oikaisusumma | ITMCostTrans.AdjustmentAmount | Numeric(32, 6) | En | En |
| Kustannusarvo | ITMCostTrans.CostValue | Numeric(32, 6) | En | En |
| Valuutta | ITMCostTrans.CurrencyCode | Nvarchar(3) | En | **Kyllä** |
| Rivinumero | ITMCostTrans.LineNum | Numeric(32, 16) | **Kyllä** | En |
| Linkitetty kustannustyyppi | ITMCostTrans.LinkCostTypeId | Nvarchar(20) | En | En |
| Vähimmäiskustannus | ITMCostTrans.MinCostAmount | Numeric(32, 6) | En | En |
| Luokka | ITMCostTrans.ShipCostCategory | Int | En | En |
| Kustannustyypin koodi | ITMCostTrans.ShipCostTypeId | Nvarchar(20) | En | En |
| Yritys | ITMCostTrans.ShipDataArea | Nvarchar(4) | En | **Kyllä** |
| Siirtotilaus | ITMCostTrans.TransRecId | Nvarchar(20) | **Kyllä** | En |
| Siirtotilausrivin numero | ITMCostTrans.TransRecId | Nvarchar(20) | **Kyllä** | En |
| Nimikkeen arvonlisäveroryhmä | ITMCostTrans.TaxItemGroup | Nvarchar(10) | En | En |
| Arvon oikaisu | ITMCostTrans.ValueAdjustmentMethod | Int | En | En |

### <a name="transaction-table"></a>Tapahtumataulu

Kustannustapahtumatietue liitetään kustannusalueeseen määrittämällä tapahtumataulukon numero (`TransTableId`). Kun tietyt taulukon tunnukset ovat pakollisia, yksiköt jaetaan näiden arvojen perusteella siten, että kullakin kustannusalueella on yksikkö.

Tapahtumataulukon arvo (`TransTableId`) on implisiittinen kustannustapahtuman yksikön valinnassa.

### <a name="calculated-fields"></a>Lasketut kentät

Seuraavia kenttiä ei voi lisätä tai päivittää kustannustapahtuman yksikköä käytettäessä, koska nämä kentät määritetään vain, kun tietyt toimenpiteet tehdään matkan tietueen perusteella:

- **Arvioitu kustannus** – Tämä kenttä määritetään, kun matkalle kirjataan lasku (ostotilaus) tai vastaanotetaan siirto.
- **Arvioidun kustannuksen valuutta** – Tämä kenttä määritetään, kun matkalle kirjataan lasku (ostotilaus) tai vastaanotetaan siirto.
- **Todellinen kustannus** – Tämä kenttä määritetään, kun toimittajan lasku kirjataan. Se liittyy kustannukseen.

### <a name="find-auto-costs"></a>Hae automaattiset kustannukset

**Hae automaattiset kustannukset** -painike, joka on käytössä kullekin kustannusalueelle (esim. matka, lähetyskontti), tarjoaa tavan päivittää kyseisen kustannusalueen kustannustapahtumat käyttämällä konfiguraatiotaulukoiden tietoja. Kun valitset kustannusalueen painikkeen, järjestelmä tyhjentää kustannusalueen aiemmat kustannukset ja luo uusia tietueita perustuen automaattisten kustannusten määritystaulukoiden nykyiseen konfiguraatioon.

Tietoyksikköä käyttäen luodut kustannustapahtumatietueet merkitään tuoduiksi. Näitä tietueita ei poisteta, kun valitset **Hae automaattiset kustannukset**, koska niitä ei luoda uudelleen automaattisten kustannusten määritystaulukoista. Voit kuitenkin poistaa kustannustapahtumatietueen, joka on merkitty tuoduksi.

### <a name="linked-fields"></a>Linkitetyt kentät

Kukin kustannustapahtuma voidaan liittää toiseen tietueeseen samalla kustannusalueella. Liitos tehdään **Linkitetty kustannustyyppi** -kentän avulla. Sen avulla kustannuksen arvo lasketaan toisen kustannuksen prosenttiosuutena.

**Linkitetty kustannustyyppi** -kenttä voidaan vahvistaa vain, jos viitattu tietue käsitellään ensin tai jos se on jo taulukossa. Sama vaatimus koskee **Linkitetty etappi** -kenttää, jota käytetään kustannuksia varten vain lähetyskontin kustannusalueella.
