---
title: Inventory Visibilityn WMS-nimikkeiden tuki
description: Tässä artikkelissa käsitellään varaston näkyvyyden tukea nimikkeille, joissa on otettu käyttöön varastonhallintaprosessit (WMS-nimikkeet).
author: yufeihuang
ms.date: 03/10/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-03-10
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: 54ce637d2d7b590988f7590eae5248276bcc4b96
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/29/2022
ms.locfileid: "9066607"
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

Varaston näkyvyyden edistynyttä WMS:ää kannattaa käyttää tilanteissa, joissa kaikki seuraavat ehdot täyttyvät:

- Supply Chain Managementin tiedot synkronoidaan varaston näkyvyyden kanssa.
- Käytät Supply Chain Managementissa WMS:ää.
- Käyttäjät tekevät varauksia WMS-nimikkeille, jotka ovat muulla tasolla kuin varastotasolla (esimerkiksi koska käytät varastotyötä).

Muissa tilanteissa käytettävissä olevan varaston kyselytulokset ovat samat riippumatta siitä, onko varaston näkyvyyden edistynyt WMS käytössä. Lisäksi suorituskyky paranee, jos toiminto ei ole käytössä näissä tilanteissa, koska laskelmia on vähemmän ja yleiskuormitus vähenee.

## <a name="enable-the-advanced-wms-feature-for-inventory-visibility"></a>Varaston näkyvyyden edistyneen WMS:n ottaminen käyttöön

Varaston näkyvyyden edistynyt WMS otetaan käyttöön seuraavasti.

1. Kirjaudu sisään Supply Chain Managementiin järjestelmänvalvojana.
1. Avaa [Ominaisuuksien hallinta](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) -työtila ja ota käyttöön seuraavat ominaisuudet tässä järjestyksessä:

    1. *Varaston näkyvyyden integrointi*
    1. *Ota varastonimikkeet käyttöön Varaston näkyvyys -kohdassa*

1. Valitse **Varastonhallinta \> Asetukset \> Varaston näkyvyyden integroinnin parametrit**.
1. Määritä **Ota WMS-nimikkeet käyttöön** -pikavälilehdessä **Ota WMS-nimikkeet käyttöön**-asetukseksi *Kyllä*.
1. Kirjaudu Power Apps -palveluun.
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

Kaikki muut fyysiset mitat lasketaan samoin kuin silloin, kun varaston näkyvyyden edistys WMS ei ole käytössä.

Yksityiskohtaisia tietoja WMS-nimikkeiden käytettävissä oleva varastosaldon laskennasta on [Varaukset varastonhallinnassa](https://www.microsoft.com/download/details.aspx?id=43284) -raportissa.

Ne tietoentiteetit, jotka viedään Dataverseen, eivät voi vielä päivittää WMS-nimikkeiden määriä. Tietoyksiköissä näkyvät määrät ovat oikein sekä ei-WMS-nimikkeille että määrille, joihin WMS-logiikka ei vaikuta (eli muut mitat kuin `fno`-tietolähteen `AvailPhysical`, `AvailOrdered`, `ReservPhysical` ja `ReservOrdered`).

Supply Chain Management -tietolähteeseen tallennettujen WMS-nimikkeiden määrien muutokset ovat kiellettyjä. Kuten muut varaston näkyvyyden toiminnot, tätä rajoitusta käytetään ristiriitojen ehkäisemiseksi.

## <a name="soft-reservations-on-wms-items-in-inventory-visibility"></a>WMS-nimikkeiden alustava varaus varaston näkyvyydessä

Yleisesti WMS-nimikkeiden [alustavat varaukset](inventory-visibility-reservations.md) ovat tuettuja. Voit sisällyttää WMS:ään liittyviä fyysisiä mittoja alustavien varausten laskentaan. 

Tiedossa on rajoitus, jonka mukaan *varattavissa*-laskelmia ei tueta tällä hetkellä WMS-nimikkeille. Jos siis varauksia on olemassa niiden nykyisten dimensioiden yläpuolella, joita varten on tehty alustava varaus, *varattavissa*-laskenta on virheellinen. Alustavat varaukset eivät muutu, kun **ifCheckAvailForReserv** -asetus on poistettu käytöstä [alustavan varauksen sovellusliittymässä](inventory-visibility-api.md#create-one-reservation-event).

Tämä rajoitus koskee myös ominaisuuksia ja mukautuksia, jotka perustuvat alustaviin varauksiin (kuten kohdistus).

## <a name="calculate-available-to-promise-quantities"></a>Luvattavissa olevien määrien laskeminen

Ratkaisu tukee täysin WMS-nimikkeiden [luvattavissa oleva määrää](inventory-visibility-available-to-promise.md). Voit määrittää luvattavissa oleva määrän laskelmat WMS:ään liittyvistä tiedoista huolehtimatta.
