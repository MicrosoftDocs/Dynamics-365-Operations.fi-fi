---
title: Supply Chain Managementin tallennetut vakionäkymät
description: Tässä aiheessa käsitellään käytettävissä olevia tallennettuja vakionäkymiä ja niiden käyttöön ottamista.
author: kamaybac
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 0709574ea44fcf841321044da31781862fcf1420
ms.sourcegitcommit: fcb8a3419e3597fe855cae9eb21333698518c2c7
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/09/2022
ms.locfileid: "8103685"
---
# <a name="standard-saved-views-for-supply-chain-management"></a>Supply Chain Managementin tallennetut vakionäkymät

[!include [banner](../../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management sisältää useita tallennettuja näkyviä, jotka voidaan ottaa käyttöön ja joita voidaan käyttää tarvittaessa. Osa näistä tallennetuista vakionäkymistä on optimoitu ja nimetty tietyn roolin tai tehtävän mukaan (kuten Laadunvalvonta tai Vastaanotto). Muut on optimoitu siten, että ne sisältävät vain kentät ja asetukset, joita asiakkaat Microsoftin käyttötilastojen mukaan käyttävät eniten. Näitä tallennettuja näkymiä kutsutaan yleensä *yksinkertaistetuiksi* näkymiksi. Tässä aiheessa käsitellään käytettävissä olevia tallennettuja vakionäkymiä sekä niiden käyttöön ottamista ja mukauttamista.

Lisätietoja tallennettujen näkymien, mukaan lukien tallennettujen vakionäkymien käyttämisestä sen jälkeen, kun ne on otettu käyttöön, on kohdassa [Tallennetut näkymät](../../fin-ops-core/fin-ops/get-started/saved-views.md?toc=/dynamics365/supply-chain/toc.json).

## <a name="customizing-the-standard-saved-views"></a>Tallennettujen vakionäkymien mukauttaminen

Tallennettuja vakionäkymiä voidaan mukauttaa samalla tavalla kuin omia tallennettuja näkymiä. Tallennettua vakionäkymää mukautettaessa mukautettu versio kannattaa kuitenkin tallentaa uudella nimellä. Muussa tapauksessa mukautukset saatetaan korvata, kun Supply Chain Management päivitetään.

Lisätietoja tallennettujen näkymien mukauttamisesta ja nimeämisestä uudelleen on kohdassa [Tallennetut näkymät](../../fin-ops-core/fin-ops/get-started/saved-views.md?toc=/dynamics365/supply-chain/toc.json).

## <a name="available-saved-views-and-how-to-enable-them"></a>Käytettävissä olevat tallennetut näkymät ja niiden ottaminen käyttöön

Tallennettujen näkymien käyttäminen riippumatta siitä, käytetäänkö tallennettuja vakionäkymiä, edellyttää, että *Tallennetut näkymät* -toiminto otetaan käyttöön [ominaisuuksien hallinnassa](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (versiosta 10.0.21 tämä toiminto on oletusarvoisesti käytössä).

Tämän aiheen muut osat koostuvat taulukoista, joissa käsitellään tällä hetkellä kussakin moduulissa käytettävissä olevia tallennettuja vakionäkymiä. Kussakin taulukossa on kunkin tallennetun näkymän nimi ja sen kuvaus sekä sivu, jolta sen löytää. Kussakin taulukossa on myös tallennetun näkymän sisältävän toiminnon nimi. Tallennettujen vakionäkymien näyttäminen järjestelmässä edellyttää, että määritetty toiminto otetaan käyttöön [ominaisuuksien hallinnassa](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md). Versiosta 10.0.25 alkaen kaikki luetellut näkymät ovat oletusarvoisesti käytössä.

## <a name="saved-views-for-the-inventory-management-module"></a>Inventoinnin- ja varastonhallintamoduulin tallennetut näkymät

Seuraavassa taulukossa käsitellään Inventoinnin- ja varastonhallintamoduulissa käytettävissä olevia tallennettuja näkymiä.

| Sivu | Näkymän nimi | Näkymän kuvaus | Toiminnon nimi |
|---|---|---|---|
| Varastoluettelo | Myyntitiedot | Tässä yksinkertaistetussa näkymässä voi keskittyä taloushallinnon tietoihin käytettävissä olevaa varastoa hallittaessa. | Inventoinnin- ja varastonhallinnan tallennetut näkymät<br><br>(Käytössä oletusarvoisesti versiosta 10.0.21 alkaen) |
| Varastoluettelo | Laadunvalvonta | Tässä yksinkertaistetussa näkymässä voi keskittyä laadunvalvontaan käytettävissä olevaa varastoa hallittaessa. | Inventoinnin- ja varastonhallinnan tallennetut näkymät<br><br>(Käytössä oletusarvoisesti versiosta 10.0.21 alkaen) |
| Varastoluettelo | Vastaanotto | Tässä yksinkertaistetussa näkymässä voi keskittyä vastaanottotoimintoihin käytettävissä olevaa varastoa hallittaessa. | Inventoinnin- ja varastonhallinnan tallennetut näkymät<br><br>(Käytössä oletusarvoisesti versiosta 10.0.21 alkaen) |
| Varastoluettelo | Toimitus | Tässä yksinkertaistetussa näkymässä voi keskittyä lähetystoimintoihin käytettävissä olevaa varastoa hallittaessa. | Inventoinnin- ja varastonhallinnan tallennetut näkymät<br><br>(Käytössä oletusarvoisesti versiosta 10.0.21 alkaen) |
| Tapahtumat | Yksinkertaistettu | Tässä yksinkertaistetussa näkymässä voi tarkastella varaston tilaa ilman taloushallinnon tietoja ja muita harvemmin käytettyjä kenttiä. | Inventoinnin- ja varastonhallinnan tallennetut näkymät<br><br>(Käytössä oletusarvoisesti versiosta 10.0.21 alkaen) |
| Siirtotilaukset | Toimitus | Tässä yksinkertaistetussa näkymässä voi keskittyä lähetystoimintoihin siirtotilauksia hallittaessa. | Inventoinnin- ja varastonhallinnan tallennetut näkymät<br><br>(Käytössä oletusarvoisesti versiosta 10.0.21 alkaen) |
| Siirtotilaukset | Vastaanotto | Tässä yksinkertaistetussa näkymässä voi keskittyä vastaanottotoimintoihin siirtotilauksia hallittaessa. | Inventoinnin- ja varastonhallinnan tallennetut näkymät<br><br>(Käytössä oletusarvoisesti versiosta 10.0.21 alkaen) |
| Siirtotilaukset | Laadunvalvonta | Tässä yksinkertaistetussa näkymässä voi keskittyä laadunvalvontaan siirtotilauksia hallittaessa. | Inventoinnin- ja varastonhallinnan tallennetut näkymät<br><br>(Käytössä oletusarvoisesti versiosta 10.0.21 alkaen) |
| Siirtotilaukset | Myyntitiedot | Tässä yksinkertaistetussa näkymässä voi keskittyä taloushallinnon tietoihin siirtotilauksia hallittaessa. | Inventoinnin- ja varastonhallinnan tallennetut näkymät<br><br>(Käytössä oletusarvoisesti versiosta 10.0.21 alkaen) |

## <a name="saved-views-for-the-master-planning-module"></a>Pääsuunnittelumoduulin tallennetut näkymät

Seuraavassa taulukossa käsitellään pääsuunnittelumoduulissa käytettävissä olevia tallennettuja näkymiä.

| Sivu | Näkymän nimi | Näkymän kuvaus | Toiminnon nimi |
|---|---|---|---|
| Suunnitellut tilaukset: Suunnitellun tilauksen tiedot -sivu | Yksinkertaistettu | Tämä yksinkertaistettu näkymä sisältää vain kentät, joita käytetään eniten yksittäisen suunnitellun tilauksen tietojen käsittelyyn. Tällä tavoin näkymästä saa nopean yleiskatsauksen ja työprosessi on sujuva. | Suunniteltujen tilausten tallennetut näkymät<br><br>(Käytössä oletusarvoisesti versiosta 10.0.25 alkaen) |
| Suunnitellut tilaukset: Suunniteltujen tilausten luettelosivu | Yksinkertaistettu | Tämä yksinkertaistettu näkymä sisältää vain kentät, joita käytetään eniten suunniteltujen tilausten luettelon käsittelyyn. Tällä tavoin näkymästä saa nopean yleiskatsauksen ja työprosessi on sujuva. | Suunniteltujen tilausten tallennetut näkymät<br><br>(Käytössä oletusarvoisesti versiosta 10.0.25 alkaen) |

## <a name="saved-views-for-the-procurement-and-sourcing-module"></a>Hankintamoduulin tallennetut näkymät

Seuraavassa taulukossa käsitellään hankintamoduulissa käytettävissä olevia tallennettuja näkymiä.

| Sivu | Näkymän nimi | Näkymän kuvaus | Toiminnon nimi |
|---|---|---|---|
| Ostotilauksen tiedot | Tilauksen luonti | Tämä yksinkertaistettu näkymä on optimoitu uusien ostotilausten luontia varten. | Ostotilausten tallennetut näkymät<br><br>(Käytössä oletusarvoisesti versiosta 10.0.25 alkaen) |
| Ostotilauksen tiedot | Inventoinnin- ja varastonhallinta | Tämä yksinkertaistettu näkymä on optimoitu varastoon liittyvien tehtävien suorittamiseen, kuten vastaanotetun varaston seurantaan, varaston vastaanottoon, nettotarpeiden tarkistamiseen ja tilausmäärien oikaisemiseen. | Ostotilausten tallennetut näkymät<br><br>(Käytössä oletusarvoisesti versiosta 10.0.25 alkaen) |
| Ostotilauksen tiedot | Taloushallinto | Tämä yksinkertaistettu näkymä on optimoitu taloushallintoon liittyvien tehtävien suorittamiseen, kuten laskutukseen sekä hintojen, yhteissummien ja kulujen tarkistamiseen. | Ostotilausten tallennetut näkymät<br><br>(Käytössä oletusarvoisesti versiosta 10.0.25 alkaen) |
| Ostotilauksen tiedot | Tilauksen hyväksyntä | Tämä yksinkertaistettu näkymä on optimoitu ostotilausten hyväksymiseen. | Ostotilausten tallennetut näkymät<br><br>(Käytössä oletusarvoisesti versiosta 10.0.25 alkaen) |

## <a name="saved-views-for-the-product-information-management-module"></a>Tuotetietohallintamoduulin tallennetut näkymät

Seuraavassa taulukossa käsitellään tuotetietohallintamoduulissa käytettävissä olevia tallennettuja näkymiä.

| Sivu | Näkymän nimi | Näkymän kuvaus | Toiminnon nimi |
|---|---|---|---|
| Julkaistujen tuotteiden luettelo | Tuotteen luonti | Yksinkertaistettu sivunäkymä, joka sisältää vain kentät, joita käytetään useimmin tuotteiden luonnin aikana. | Julkaistujen tuotteiden tallennetut näkymät<br><br>(Käytössä oletusarvoisesti versiosta 10.0.21 alkaen) |
| Vapautetun tuotteen tiedot | Tuotteen luonti | Yksinkertaistettu sivunäkymä, joka sisältää vain kentät, joita käytetään useimmin tuotteiden luonnin aikana. | Julkaistujen tuotteiden tallennetut näkymät<br><br>(Käytössä oletusarvoisesti versiosta 10.0.21 alkaen) |
| Vapautetun tuotteen tiedot | Logistiikkatietojen hallinta | Yksinkertaistettu sivunäkymä, joka sisältää vain kentät, joita käytetään useimmin tuotteiden logistiikkatietojen hallinnan aikana. | Julkaistujen tuotteiden tallennetut näkymät<br><br>(Käytössä oletusarvoisesti versiosta 10.0.21 alkaen) |
| Vapautetun tuotteen tiedot | Ostotietojen hallinta | Yksinkertaistettu sivunäkymä, joka sisältää vain kentät, joita käytetään useimmin tuotteiden ostotietojen hallinnan aikana. | Julkaistujen tuotteiden tallennetut näkymät<br><br>(Käytössä oletusarvoisesti versiosta 10.0.21 alkaen) |
| Vapautetun tuotteen tiedot | Myyntitietojen hallinta | Yksinkertaistettu sivunäkymä, joka sisältää vain kentät, joita käytetään useimmin tuotteiden myyntiin liittyvien tietojen hallinnan aikana. | Julkaistujen tuotteiden tallennetut näkymät<br><br>(Käytössä oletusarvoisesti versiosta 10.0.21 alkaen) |

## <a name="saved-views-for-the-production-control-module"></a>Tuotannonhallintamoduulin tallennetut näkymät

Seuraavassa taulukossa käsitellään tuotannonhallintamoduulissa käytettävissä olevia tallennettuja näkymiä.

| Sivu | Näkymän nimi | Näkymän kuvaus | Toiminnon nimi |
|---|---|---|---|
| Tuotantotilauksen tuoterakenne -sivu | Yksinkertaistettu | Tämä yksinkertaistettu näkymä sisältää vain eniten käytetyt kentät. Tällä tavoin näkymästä saa nopean yleiskatsauksen ja työprosessi on sujuva. | Tuotannonohjauksen tallennetut näkymät<br><br>(Käytössä oletusarvoisesti versiosta 10.0.21 alkaen) |
| Tuotantotilauksen tiedot -sivu | Yksinkertaistettu | Tämä yksinkertaistettu näkymä sisältää vain eniten käytetyt kentät. Tällä tavoin näkymästä saa nopean yleiskatsauksen ja työprosessi on sujuva. | Tuotannonohjauksen tallennetut näkymät<br><br>(Käytössä oletusarvoisesti versiosta 10.0.21 alkaen) |
| Tuotantotilauksen keräysluettelo -sivu | Yksinkertaistettu | Tämä yksinkertaistettu näkymä sisältää vain eniten käytetyt kentät. Tällä tavoin näkymästä saa nopean yleiskatsauksen ja työprosessi on sujuva. | Tuotannonohjauksen tallennetut näkymät<br><br>(Käytössä oletusarvoisesti versiosta 10.0.21 alkaen) |
| Tuotantotilauksen luettelosivu | Yksinkertaistettu | Tämä yksinkertaistettu näkymä sisältää vain eniten käytetyt kentät. Tällä tavoin näkymästä saa nopean yleiskatsauksen ja työprosessi on sujuva. | Tuotannonohjauksen tallennetut näkymät<br><br>(Käytössä oletusarvoisesti versiosta 10.0.21 alkaen) |

## <a name="saved-views-for-the-sales-and-marketing-module"></a>Myynti- ja markkinointimoduulin tallennetut näkymät

Seuraavassa taulukossa käsitellään myynti- ja markkinointimoduulissa käytettävissä olevia tallennettuja näkymiä.

| Sivu | Näkymän nimi | Näkymän kuvaus | Toiminnon nimi |
|---|---|---|---|
| Pakkausluettelokirjauskansio | Kirjauskansion tarkastelu | Tämä yksinkertaistettu näkymä sisältää vain pakkausluettelokirjauskansioiden tarkastelussa eniten käytetyt kentät. | Myynnin ja markkinoinnin tallennetut näkymät<br><br>(Käytössä oletusarvoisesti versiosta 10.0.25 alkaen) |
| Myyntitilaus | Tilauksen luonti | Tämä yksinkertaistettu näkymä sisältää vain myyntitilausten luonnissa eniten käytetyt kentät. | Myynnin ja markkinoinnin tallennetut näkymät<br><br>(Käytössä oletusarvoisesti versiosta 10.0.25 alkaen) |
| Myyntitilaus | Tilauksen tarkistus | Tämä yksinkertaistettu näkymä sisältää vain myyntitilausten tarkastelussa eniten käytetyt kentät. | Myynnin ja markkinoinnin tallennetut näkymät<br><br>(Käytössä oletusarvoisesti versiosta 10.0.25 alkaen) |
| Myyntitarjous | Tarjouksen luonti | Tämä yksinkertaistettu näkymä sisältää vain myyntitarjousten luonnissa eniten käytetyt kentät. | Myynnin ja markkinoinnin tallennetut näkymät<br><br>(Käytössä oletusarvoisesti versiosta 10.0.25 alkaen) |

## <a name="saved-views-for-the-warehouse-management-module"></a>Varastonhallintamoduulin tallennetut näkymät

Seuraavassa taulukossa käsitellään varastonhallintamoduulissa käytettävissä olevia tallennettuja näkymiä.

| Sivu | Näkymän nimi | Näkymän kuvaus | Toiminnon nimi |
|---|---|---|---|
| Kaikki kuormat | Saapuvien käsittely | Tämä yksinkertaistettu näkymä sisältää vain saapuvien kuormien käsittelyssä eniten käytetyt kentät. | Tallennetut näkymät kuorman käsittelyä varten<br><br>(Käytössä oletusarvoisesti versiosta 10.0.25 alkaen) |
| Kaikki kuormat | Lähtevien käsittely | Tämä yksinkertaistettu näkymä sisältää vain lähtevien kuormien käsittelyssä eniten käytetyt kentät. | Tallennetut näkymät kuorman käsittelyä varten<br><br>(Käytössä oletusarvoisesti versiosta 10.0.25 alkaen) |
| Kaikki lähetykset | Saapuvien käsittely | Tämä yksinkertaistettu näkymä sisältää vain saapuvien lähetysten käsittelyssä eniten käytetyt kentät. | Tallennetut näkymät lähetyksen käsittelyä varten<br><br>(Käytössä oletusarvoisesti versiosta 10.0.25 alkaen) |
| Kaikki lähetykset | Lähtevien käsittely | Tämä yksinkertaistettu näkymä sisältää vain lähtevien lähetysten käsittelyssä eniten käytetyt kentät. | Tallennetut näkymät lähetyksen käsittelyä varten<br><br>(Käytössä oletusarvoisesti versiosta 10.0.25 alkaen) |
| Kaikki aallot | Yksinkertaistettu | Tämä yksinkertaistettu näkymä sisältää vain eniten käytetyt kentät. Tällä tavoin näkymästä saa nopean yleiskatsauksen ja työprosessi on sujuva. | Tallennettu näkymä aallon käsittelyä varten<br><br>(Käytössä oletusarvoisesti versiosta 10.0.25 alkaen) |
| Kuormasuunnittelun työtila | Yksinkertaistettu | Tämä yksinkertaistettu näkymä sisältää vain eniten käytetyt kentät. Tällä tavoin näkymästä saa nopean yleiskatsauksen ja työprosessi on sujuva. | Tallennettu näkymä kuormasuunnittelun työtilaa varten<br><br>(Käytössä oletusarvoisesti versiosta 10.0.25 alkaen) |
| Työn tiedot | Yksinkertaistettu | Tämä yksinkertaistettu näkymä sisältää vain eniten käytetyt kentät. Tällä tavoin näkymästä saa nopean yleiskatsauksen ja työprosessi on sujuva. | Työn tietosivun tallennettu näkymä<br><br>(Käytössä oletusarvoisesti versiosta 10.0.25 alkaen) |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]