---
title: Inventory Visibilityn WMS-nimikkeiden tuki
description: Tässä artikkelissa käsitellään varaston näkyvyyden tukea nimikkeille, joissa on otettu käyttöön varastonhallintaprosessit (WMS-nimikkeet).
author: yufeihuang
ms.date: 11/04/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-03-10
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: bed402ecf20c19e81b2687efd90dba600460971a
ms.sourcegitcommit: 49f8973f0e121eac563876d50bfff00c55344360
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/14/2022
ms.locfileid: "9762736"
---
# <a name="inventory-visibility-support-for-wms-items"></a>Inventory Visibilityn WMS-nimikkeiden tuki

[!include [banner](../includes/banner.md)]

Tässä artikkelissa käsitellään varaston näkyvyyden tukea nimikkeille, joissa on otettu käyttöön varastonhallintaprosessit (WMS). Ominaisuus, joka lisää tämän ominaisuuden varaston näkyvyyteen, on nimeltään *Edistynyt WMS*.

## <a name="wms-items"></a>WMS-nimikkeet

WMS-nimike on nimike, jossa on käytössä WMS ja jota käsittelevässä varastossa WMS on otettu käyttöön.

Lisätietoja WMS:tä ja **Varastonhallinta**-moduulista ja Microsoft Dynamics 365 Supply Chain Managementissa on kohdassa [Varastonhallinnan yleiskuvaus](../warehousing/warehouse-management-overview.md).

## <a name="scope-of-the-feature"></a>Toiminnon laajuus

Edistynyt WMS keskittyy varaston näkyvyydessä käytettävissä olevan määrän laskentaan, jotka perustuvat käytettävissä olevan varaston kyselyihin. Toiminnon avulla ei ole tarkoitus varaston näkyvyyden avulla hallita varaston käsittelytoimia yleisesti. Varaston näkyvyys ei näytä varastokohtaisia käsitteitä käyttäjilleen. Esimerkkejä käsitteistä:

- Varaushierarkia
- Onko nimikkeelle tai varastolle otettu käyttöön WMS
- Yksikön sarjaryhmän tunnus
- Varastokohtaiset prosessit, kuten lähetykset, kuormaukset, aallot ja työt

Varaston näkyvyys päättelee nämä tiedot Supply Chain Managementista lähetettyjen tietojen perusteella. Käyttäjät eivät voi nähdä WMS-kohtaisia tietoja (toisin sanoen `WHSInventReserve`-taulun tietoja).

Kun käytät varaston näkyvyyden edistynyttä WMS:ää, kaikkien kyselyiden tulokset vastaavat suoraan Supply Chain Managementissa tehtyjen kyselyiden tuloksia. Ne eivät kuitenkaan ole identtiset niiden kyselyiden tulosten kanssa, jotka on tehty Warehouse Management -mobiilisovelluksen avulla, koska mobiilisovelluksessa käytetään hieman eri laskentalogiikkaa.

## <a name="when-to-use-the-feature"></a>Milloin käyttää toimintoa

Inventory Visibilityn WMS:ää kannattaa käyttää tilanteissa, joissa kaikki seuraavat ehdot täyttyvät:

- Supply Chain Managementin tiedot synkronoidaan varaston näkyvyyden kanssa.
- Käytät Supply Chain Managementissa WMS:ää.
- Käyttäjät tekevät varauksia WMS-nimikkeille, jotka varastotasoa alhaisemmalla tasolla (esimerkiksi rekisterikilven tasolla, koska käsiteltävänä on varastotyö).

Muissa tilanteissa käytettävissä olevan varaston kyselytulokset ovat samat riippumatta siitä, onko varaston näkyvyyden edistynyt WMS käytössä. Lisäksi suorituskyky paranee, jos toiminto ei ole käytössä näissä tilanteissa, koska laskelmia on vähemmän ja yleiskuormitus vähenee.

## <a name="enable-the-wms-feature-for-inventory-visibility"></a>Inventory Visibilityn WMS:n ottaminen käyttöön

Inventory Visibilityn WMS otetaan käyttöön alla olevien ohjeiden avulla.

1. Kirjaudu sisään Supply Chain Managementiin järjestelmänvalvojana.
1. Avaa [Ominaisuuksien hallinta](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) -työtila ja ota käyttöön seuraavat ominaisuudet tässä järjestyksessä:

    1. *Varaston näkyvyyden integrointi*
    1. *Ota varastonimikkeet käyttöön Varaston näkyvyys -kohdassa*

1. Valitse **Varastonhallinta \> Asetukset \> Varaston näkyvyyden integroinnin parametrit**.
1. Määritä **Ota WMS-nimikkeet käyttöön** -pikavälilehdessä **Ota WMS-nimikkeet käyttöön**-asetukseksi *Kyllä*.
1. Kirjaudu Power Apps -ympäristöön ja avaa **Varaston näkyvyys**.
1. Avaa **Määritys**-sivu ja ota sitten käyttöön *AdvancedWHS*-toiminto **Ominaisuuden hallinta** -välilehdessä.
1. Valitse Supply Chain Managementissa **Varastonhallinta \> Kausittaiset tehtävät \> Varaston näkyvyyden integraatio**.
1. Valitse toimintoruudussa **Poista käytöstä**, jos haluat poistaa varaston näkyvyyden tilapäisesti käytöstä.
1. Ota varaston näkyvyys uudelleen käyttöön valitsemalla toimintoruudussa **Ota käyttöön**. Lisäosa ladataan uudelleen, ja uusi toiminto on nyt käytössä. WMS:ään liittyvien tietojen synkronointi varaston näkyvyyteen aloitetaan.

## <a name="query-on-hand-quantities-of-wms-items"></a>Kohdista kyselyjä WMS-nimikkeiden käytettävissä oleviin varastosaldomääriin

Jos haluat tehdä kyselyn WMS-nimikkeistä, käytät samaa [ohjelmointirajapintaa (API) ja sanomasyntaksia](inventory-visibility-api.md), jota käytät muille kuin WMS-nimikkeille. Nimikettä ei tarvitse määrittää sen mukaan, onko nimike WMS-nimike vai ei. Varaston näkyvyys erottaa nimikkeet automaattisesti tallennettujen tietojen perusteella.

WMS-nimikkeiden kyselyiden tulokset ovat pohjimmiltaan samat kuin ei-WMS-nimikkeiden tulokset. Ainoa ero on se, että seuraavat `fno`-tietolähteen fyysiset mitat lasketaan Supply Chain Managementin WMS-logiikan perusteella:

- `AvailOrdered`
- `AvailPhysical`
- `ReservOrdered`
- `ReservPhysical`

Kaikki muut fyysiset mitat lasketaan samoin kuin silloin, kun Inventory Visibilityn WMS ei ole käytössä.

Yksityiskohtaisia tietoja WMS-nimikkeiden käytettävissä oleva varastosaldon laskennasta on [Varaukset varastonhallinnassa](https://www.microsoft.com/download/details.aspx?id=43284) -raportissa.

## <a name="on-hand-list-view-and-data-entity-for-wms-items"></a>WMS-nimikkeiden varastosaldon luettelonäkymä ja tietoyksikkö

**Varaston näkyvyyden yhteenvedon esilataus** -sivulla on *Käytettävissä olevan varaston indeksin kyselyn esilatauksen tulokset* -entiteetin näkymä. Toisin kuin *Varaston yhteenveto* -entiteetti, *Käytettävissä olevan varaston indeksin kyselyn esilatauksen tulokset* -entiteetti määrittää tuotteiden käytettävissä olevan varaston luettelon yhdessä valittujen dimensioiden kanssa. Varaston näkyvyys synkronoi esiladatut yhteenvetotiedot 15 minuutin välein.

Jos Inventory Visibility on käytössä WMS-nimikkeiden kanssa ja haluat tarkastella WMS-nimikkeiden varastosaldoluetteloa, on suositeltavaa ottaa käyttöön *Esilataa Inventory Visibility näkyvyys -yhteenveto* -ominaisuus (katso myös [Varastosaldon virtaviivaistetun kyselyn esilataaminen](inventory-visibility-power-platform.md#preload-streamlined-onhand-query)). Dataversen vastaava tietoyksikkö tallentaa kyselyn esilatauksen tulokset, jotka päivitetään 15 minuutin välein. Tietoyksikön nimi on `Onhand Index Query Preload Result`.

> [!IMPORTANT]
> Dataverse-yksikkö on vain luku -muotoinen. Voit tarkastella ja viedä Inventory Visibility -yksiköiden tietoja, mutta et voi **muokata niitä**.

Supply Chain Management -tietolähteeseen (`fno`) tallennettujen WMS-nimikkeiden määrien muutokset ovat kiellettyjä. Tämä toiminta vastaa Inventory Visibilityn muiden ominaisuuksien toimintaa. Tämä rajoitus on pakotettu käyttöön ristiriitojen estämiseksi.

## <a name="wms-item-compatibility-for-other-functions-in-inventory-visibility"></a>WMS-nimikkeen yhteensopivuus muiden Inventory Visibilityn toimintojen kanssa

WMS-nimikkeiden [alustavia varauksia](inventory-visibility-reservations.md) ja [varaston kohdistusta](inventory-visibility-allocation.md) tuetaan. Voit sisällyttää WMS:ään liittyviä fyysisiä mittoja alustavien varausten ja kohdistuksen laskentaan.

## <a name="calculate-available-to-promise-quantities"></a>Luvattavissa olevien määrien laskeminen

Ratkaisu tukee täysin WMS-nimikkeiden [luvattavissa oleva määrää](inventory-visibility-available-to-promise.md). Voit määrittää luvattavissa oleva määrän laskelmat WMS:ään liittyvistä tiedoista huolehtimatta.
