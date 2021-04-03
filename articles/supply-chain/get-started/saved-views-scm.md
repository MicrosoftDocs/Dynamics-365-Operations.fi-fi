---
title: Supply Chain Managementin tallennetut vakionäkymät
description: Tässä aiheessa käsitellään käytettävissä olevia tallennettuja vakionäkymiä ja niiden käyttöön ottamista.
author: kamaybac
manager: annbe
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 08002a1ff40c8baca475bc19a1220fe4c4b23bcd
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500691"
---
# <a name="standard-saved-views-for-supply-chain-management"></a>Supply Chain Managementin tallennetut vakionäkymät

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Microsoft Dynamics 365 Supply Chain Management sisältää useita tallennettuja näkyviä, jotka voidaan ottaa käyttöön ja joita voidaan käyttää tarvittaessa. Osa näistä tallennetuista vakionäkymistä on optimoitu ja nimetty tietyn roolin tai tehtävän mukaan (kuten Laadunvalvonta tai Vastaanotto). Muut on optimoitu siten, että ne sisältävät vain kentät ja asetukset, joita asiakkaat Microsoftin käyttötilastojen mukaan käyttävät eniten. Näitä tallennettuja näkymiä kutsutaan yleensä *yksinkertaistetuiksi* näkymiksi. Tässä aiheessa käsitellään käytettävissä olevia tallennettuja vakionäkymiä sekä niiden käyttöön ottamista ja mukauttamista.

Lisätietoja tallennettujen näkymien, mukaan lukien tallennettujen vakionäkymien käyttämisestä sen jälkeen, kun ne on otettu käyttöön, on kohdassa [Tallennetut näkymät](../../fin-ops-core/fin-ops/get-started/saved-views.md?toc=/dynamics365/supply-chain/toc.json).

## <a name="customizing-the-standard-saved-views"></a>Tallennettujen vakionäkymien mukauttaminen

Tallennettuja vakionäkymiä voidaan mukauttaa samalla tavalla kuin omia tallennettuja näkymiä. Tallennettua vakionäkymää mukautettaessa mukautettu versio kannattaa kuitenkin tallentaa uudella nimellä. Muussa tapauksessa mukautukset saatetaan korvata, kun Supply Chain Management päivitetään.

Lisätietoja tallennettujen näkymien mukauttamisesta ja nimeämisestä uudelleen on kohdassa [Tallennetut näkymät](../../fin-ops-core/fin-ops/get-started/saved-views.md?toc=/dynamics365/supply-chain/toc.json).

## <a name="available-saved-views-and-how-to-enable-them"></a>Käytettävissä olevat tallennetut näkymät ja niiden ottaminen käyttöön

Tallennettujen näkymien käyttäminen riippumatta siitä, käytetäänkö tallennettuja vakionäkymiä, edellyttää, että *Tallennetut näkymät* -toiminto otetaan käyttöön [ominaisuuksien hallinnassa](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Tämän aiheen muut osat koostuvat taulukoista, joissa käsitellään tällä hetkellä kussakin moduulissa käytettävissä olevia tallennettuja vakionäkymiä. Kussakin taulukossa on kunkin tallennetun näkymän nimi ja sen kuvaus sekä sivu, jolta sen löytää. Kussakin taulukossa on myös tallennetun näkymän sisältävän toiminnon nimi. Tallennettujen vakionäkymien näyttäminen järjestelmässä edellyttää, että määritetty toiminto otetaan käyttöön [ominaisuuksien hallinnassa](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="saved-views-for-the-inventory-management-module"></a>Inventoinnin- ja varastonhallintamoduulin tallennetut näkymät

Seuraavassa taulukossa käsitellään Inventoinnin- ja varastonhallintamoduulissa käytettävissä olevia tallennettuja näkymiä.

| Sivu | Näkymän nimi | Näkymän kuvaus | Toiminnon nimi |
|---|---|---|---|
| Varastoluettelo | Myyntitiedot | Tässä yksinkertaistetussa näkymässä voi keskittyä taloushallinnon tietoihin käytettävissä olevaa varastoa hallittaessa. | Inventoinnin- ja varastonhallinnan tallennetut näkymät |
| Varastoluettelo | Laadunvalvonta | Tässä yksinkertaistetussa näkymässä voi keskittyä laadunvalvontaan käytettävissä olevaa varastoa hallittaessa. | Inventoinnin- ja varastonhallinnan tallennetut näkymät |
| Varastoluettelo | Vastaanotto | Tässä yksinkertaistetussa näkymässä voi keskittyä vastaanottotoimintoihin käytettävissä olevaa varastoa hallittaessa. | Inventoinnin- ja varastonhallinnan tallennetut näkymät |
| Varastoluettelo | Lähetys | Tässä yksinkertaistetussa näkymässä voi keskittyä lähetystoimintoihin käytettävissä olevaa varastoa hallittaessa. | Inventoinnin- ja varastonhallinnan tallennetut näkymät |
| Tapahtumat | Yksinkertaistettu | Tässä yksinkertaistetussa näkymässä voi tarkastella varaston tilaa ilman taloushallinnon tietoja ja muita harvemmin käytettyjä kenttiä. | Inventoinnin- ja varastonhallinnan tallennetut näkymät |
| Siirtotilaukset | Lähetys | Tässä yksinkertaistetussa näkymässä voi keskittyä lähetystoimintoihin siirtotilauksia hallittaessa. | Inventoinnin- ja varastonhallinnan tallennetut näkymät |
| Siirtotilaukset | Vastaanotto | Tässä yksinkertaistetussa näkymässä voi keskittyä vastaanottotoimintoihin siirtotilauksia hallittaessa. | Inventoinnin- ja varastonhallinnan tallennetut näkymät |
| Siirtotilaukset | Laadunvalvonta | Tässä yksinkertaistetussa näkymässä voi keskittyä laadunvalvontaan siirtotilauksia hallittaessa. | Inventoinnin- ja varastonhallinnan tallennetut näkymät |
| Siirtotilaukset | Myyntitiedot | Tässä yksinkertaistetussa näkymässä voi keskittyä taloushallinnon tietoihin siirtotilauksia hallittaessa. | Inventoinnin- ja varastonhallinnan tallennetut näkymät |

## <a name="saved-views-for-the-master-planning-module"></a>Pääsuunnittelumoduulin tallennetut näkymät

Seuraavassa taulukossa käsitellään pääsuunnittelumoduulissa käytettävissä olevia tallennettuja näkymiä.

| Sivu | Näkymän nimi | Näkymän kuvaus | Toiminnon nimi |
|---|---|---|---|
| Suunnitellut tilaukset: Suunnitellun tilauksen tiedot -sivu | Yksinkertaistettu | Tämä yksinkertaistettu näkymä sisältää vain kentät, joita käytetään eniten yksittäisen suunnitellun tilauksen tietojen käsittelyyn. Tällä tavoin näkymästä saa nopean yleiskatsauksen ja työprosessi on sujuva. | Suunniteltujen tilausten tallennetut näkymät |
| Suunnitellut tilaukset: Suunniteltujen tilausten luettelosivu | Yksinkertaistettu | Tämä yksinkertaistettu näkymä sisältää vain kentät, joita käytetään eniten suunniteltujen tilausten luettelon käsittelyyn. Tällä tavoin näkymästä saa nopean yleiskatsauksen ja työprosessi on sujuva. | Suunniteltujen tilausten tallennetut näkymät |

## <a name="saved-views-for-the-procurement-and-sourcing-module"></a>Hankintamoduulin tallennetut näkymät

Seuraavassa taulukossa käsitellään hankintamoduulissa käytettävissä olevia tallennettuja näkymiä.

| Sivu | Näkymän nimi | Näkymän kuvaus | Toiminnon nimi |
|---|---|---|---|
| Ostotilauksen tiedot | Tilauksen luonti | Tämä yksinkertaistettu näkymä on optimoitu uusien ostotilausten luontia varten. | Ostotilausten tallennetut näkymät |
| Ostotilauksen tiedot | Inventoinnin- ja varastonhallinta | Tämä yksinkertaistettu näkymä on optimoitu varastoon liittyvien tehtävien suorittamiseen, kuten vastaanotetun varaston seurantaan, varaston vastaanottoon, nettotarpeiden tarkistamiseen ja tilausmäärien oikaisemiseen. | Ostotilausten tallennetut näkymät |
| Ostotilauksen tiedot | Taloushallinto | Tämä yksinkertaistettu näkymä on optimoitu taloushallintoon liittyvien tehtävien suorittamiseen, kuten laskutukseen sekä hintojen, yhteissummien ja kulujen tarkistamiseen. | Ostotilausten tallennetut näkymät |
| Ostotilauksen tiedot | Tilauksen hyväksyntä | Tämä yksinkertaistettu näkymä on optimoitu ostotilausten hyväksymiseen. | Ostotilausten tallennetut näkymät |

## <a name="saved-views-for-the-production-control-module"></a>Tuotannonhallintamoduulin tallennetut näkymät

Seuraavassa taulukossa käsitellään tuotannonhallintamoduulissa käytettävissä olevia tallennettuja näkymiä.

| Sivu | Näkymän nimi | Näkymän kuvaus | Toiminnon nimi |
|---|---|---|---|
| Tuotantotilauksen tuoterakenne -sivu | Yksinkertaistettu | Tämä yksinkertaistettu näkymä sisältää vain eniten käytetyt kentät. Tällä tavoin näkymästä saa nopean yleiskatsauksen ja työprosessi on sujuva. | Tuotannonhallinnan tallennetut näkymät |
| Tuotantotilauksen tiedot -sivu | Yksinkertaistettu | Tämä yksinkertaistettu näkymä sisältää vain eniten käytetyt kentät. Tällä tavoin näkymästä saa nopean yleiskatsauksen ja työprosessi on sujuva. | Tuotannonhallinnan tallennetut näkymät |
| Tuotantotilauksen keräysluettelo -sivu | Yksinkertaistettu | Tämä yksinkertaistettu näkymä sisältää vain eniten käytetyt kentät. Tällä tavoin näkymästä saa nopean yleiskatsauksen ja työprosessi on sujuva. | Tuotannonhallinnan tallennetut näkymät |
| Tuotantotilauksen luettelosivu | Yksinkertaistettu | Tämä yksinkertaistettu näkymä sisältää vain eniten käytetyt kentät. Tällä tavoin näkymästä saa nopean yleiskatsauksen ja työprosessi on sujuva. | Tuotannonhallinnan tallennetut näkymät |

## <a name="saved-views-for-the-sales-and-marketing-module"></a>Myynti- ja markkinointimoduulin tallennetut näkymät

Seuraavassa taulukossa käsitellään myynti- ja markkinointimoduulissa käytettävissä olevia tallennettuja näkymiä.

| Sivu | Näkymän nimi | Näkymän kuvaus | Toiminnon nimi |
|---|---|---|---|
| Pakkausluettelokirjauskansio | Kirjauskansion tarkastelu | Tämä yksinkertaistettu näkymä sisältää vain pakkausluettelokirjauskansioiden tarkastelussa eniten käytetyt kentät. | Myynnin ja markkinoinnin tallennetut näkymät |
| Myyntitilaus | Tilauksen luonti | Tämä yksinkertaistettu näkymä sisältää vain myyntitilausten luonnissa eniten käytetyt kentät. | Myynnin ja markkinoinnin tallennetut näkymät |
| Myyntitilaus | Tilauksen tarkastelu | Tämä yksinkertaistettu näkymä sisältää vain myyntitilausten tarkastelussa eniten käytetyt kentät. | Myynnin ja markkinoinnin tallennetut näkymät |
| Myyntitarjous | Tarjouksen luonti | Tämä yksinkertaistettu näkymä sisältää vain myyntitarjousten luonnissa eniten käytetyt kentät. | Myynnin ja markkinoinnin tallennetut näkymät |

## <a name="saved-views-for-the-warehouse-management-module"></a>Varastonhallintamoduulin tallennetut näkymät

Seuraavassa taulukossa käsitellään varastonhallintamoduulissa käytettävissä olevia tallennettuja näkymiä.

| Sivu | Näkymän nimi | Näkymän kuvaus | Toiminnon nimi |
|---|---|---|---|
| Kaikki kuormat | Saapuvien käsittely | Tämä yksinkertaistettu näkymä sisältää vain saapuvien kuormien käsittelyssä eniten käytetyt kentät. | Tallennetut näkymät kuorman käsittelyä varten |
| Kaikki kuormat | Lähtevien käsittely | Tämä yksinkertaistettu näkymä sisältää vain lähtevien kuormien käsittelyssä eniten käytetyt kentät. | Tallennetut näkymät kuorman käsittelyä varten |
| Kaikki lähetykset | Saapuvien käsittely | Tämä yksinkertaistettu näkymä sisältää vain saapuvien lähetysten käsittelyssä eniten käytetyt kentät. | Tallennetut näkymät lähetyksen käsittelyä varten |
| Kaikki lähetykset | Lähtevien käsittely | Tämä yksinkertaistettu näkymä sisältää vain lähtevien lähetysten käsittelyssä eniten käytetyt kentät. | Tallennetut näkymät lähetyksen käsittelyä varten |
| Kaikki aallot | Yksinkertaistettu | Tämä yksinkertaistettu näkymä sisältää vain eniten käytetyt kentät. Tällä tavoin näkymästä saa nopean yleiskatsauksen ja työprosessi on sujuva. | Tallennettu näkymä aallon käsittelyä varten |
| Kuormasuunnittelun työtila | Yksinkertaistettu | Tämä yksinkertaistettu näkymä sisältää vain eniten käytetyt kentät. Tällä tavoin näkymästä saa nopean yleiskatsauksen ja työprosessi on sujuva. | Työsuunnittelun työtilan tallennettu näkymä |
| Työn tiedot | Yksinkertaistettu | Tämä yksinkertaistettu näkymä sisältää vain eniten käytetyt kentät. Tällä tavoin näkymästä saa nopean yleiskatsauksen ja työprosessi on sujuva. | Työn tietosivun tallennettu näkymä |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]