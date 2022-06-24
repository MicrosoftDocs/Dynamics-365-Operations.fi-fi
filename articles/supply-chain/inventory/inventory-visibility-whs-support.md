---
title: Inventory Visibilityn WHS-nimikkeiden tuki
description: Tässä artikkelissa kuvataan varaston näkyvyyden tuki nimikkeille, jotka on otettu käyttöön varaston lisäprosesseissa (WHS-nimikkeet).
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
ms.openlocfilehash: ec2254d6cf203216acea88fdfb54ad491abdeb49
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8895667"
---
# <a name="inventory-visibility-support-for-whs-items"></a>Inventory Visibilityn WHS-nimikkeiden tuki

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kuvataan varaston näkyvyyden tuki nimikkeille, jotka on otettu käyttöön varaston lisäprosesseissa (WHS-nimikkeet). Ominaisuus, joka lisää tämän ominaisuuden varaston näkyvyyteen, on nimeltään *Edistynyt varastonhallinta*.

## <a name="whs-items"></a>Varastonhallintanimikkeet

Varastonhallintanimike on nimike, joka on käytössä edistyneessä varastoprosesseissa (WHS), ja sitä käsitellään varastossa, jossa myös on WHS otettu käyttöön.

Lisätietoja WHS:tä ja **Varastonhallinta**-moduulista ja Microsoft Dynamics 365 Supply Chain Managementissa on kohdassa [Varastonhallinnan yleiskuvaus](../warehousing/warehouse-management-overview.md).

## <a name="scope-of-the-feature"></a>Toiminnon laajuus

Edistynyt varastonhallinta keskittyy varaston näkyvyydessä käytettävissä olevan määrän laskentaan, jotka perustuvat käytettävissä olevan varaston kyselyihin. Toiminnon avulla ei ole tarkoitus varaston näkyvyyden avulla hallita varaston käsittelytoimia yleisesti. Varaston näkyvyys ei näytä varastokohtaisia käsitteitä käyttäjilleen. Esimerkkejä käsitteistä:

- Varaushierarkia
- Onko nimikkeelle tai varastolle otettu käyttöön WHS
- Yksikön sarjaryhmän tunnus
- Varastokohtaiset prosessit, kuten lähetykset, kuormaukset, aallot ja työt

Varaston näkyvyys päättelee nämä tiedot Supply Chain Managementista lähetettyjen tietojen perusteella. Käyttäjät eivät voi nähdä WHS-kohtaisia tietoja (toisin sanoen `WHSInventReserve`-taulun tietoja).

Kun käytät varaston näkyvyyden edistyneen varastonhallinnan ominaisuutta, kaikkien kyselyiden tulokset vastaavat suoraan Supply Chain Managementissa tehtyjen kyselyiden tuloksia. Ne eivät kuitenkaan ole identtiset niiden kyselyiden tulosten kanssa, jotka on tehty Warehouse Management -mobiilisovelluksen avulla, koska mobiilisovelluksessa käytetään hieman eri laskentalogiikkaa.

## <a name="when-to-use-the-feature"></a>Milloin käyttää toimintoa

Varaston näkyvyyden lisätoimintoa kannattaa käyttää tilanteissa, joissa kaikki seuraavat ehdot täyttyvät:

- Supply Chain Managementin tiedot synkronoidaan varaston näkyvyyden kanssa.
- Käytät Supply Chain Managementissa WHS:ää.
- Käyttäjät tekevät varauksia WHS-nimikkeille, jotka ovat muulla tasolla kuin varastotasolla (esimerkiksi koska käytät varastotyötä).

Muissa tilanteissa käytettävissä olevan varaston kyselytulokset ovat samat riippumatta siitä, onko varaston näkyvyyden lisätoiminto käytössä. Lisäksi suorituskyky paranee, jos toiminto ei ole käytössä näissä tilanteissa, koska laskelmia on vähemmän ja yleiskuormitus vähenee.

## <a name="enable-the-advanced-whs-feature-for-inventory-visibility"></a>Varaston näkyvyyden lisäasetusten ottaminen käyttöön

Varaston näkyvyyden lisäasetusten ottaminen käyttöön tapahtuu seuraavasti.

1. Kirjaudu sisään Supply Chain Managementiin järjestelmänvalvojana.
1. Avaa [Ominaisuuksien hallinta](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) -työtila ja ota käyttöön seuraavat ominaisuudet tässä järjestyksessä:

    1. *Varaston näkyvyyden integrointi*
    1. *Ota varastonimikkeet käyttöön Varaston näkyvyys -kohdassa*

1. Valitse **Varastonhallinta \> Asetukset \> Varaston näkyvyyden integroinnin parametrit**.
1. Määritä **Ota WHS-nimikkeet käyttöön** -pikavälilehdessä **Ota WHS-nimikkeet käyttöön**-asetukseksi *Kyllä*.
1. Kirjaudu Power Apps -palveluun.
1. Avaa **Määritys**-sivu ja ota sitten käyttöön *AdvancedWHS*-toiminto **Ominaisuuden hallinta** -välilehdessä.
1. Valitse Supply Chain Managementissa **Varastonhallinta \> Kausittaiset tehtävät \> Varaston näkyvyyden integraatio**.
1. Valitse toimintoruudussa **Poista käytöstä**, jos haluat poistaa varaston näkyvyyden tilapäisesti käytöstä.
1. Ota varaston näkyvyys uudelleen käyttöön valitsemalla toimintoruudussa **Ota käyttöön**. Lisäosa ladataan uudelleen, ja uusi toiminto on nyt käytössä. WHS:ään liittyvien tietojen synkronointi varaston näkyvyyteen aloitetaan.

## <a name="query-on-hand-quantities-of-whs-items"></a>Kohdista kyselyjä WHS-nimikkeiden käytettävissä oleviin varastosaldomääriin

Jos haluat tehdä kyselyn WHS-nimikkeistä, käytät samaa [ohjelmointirajapintaa (API) ja sanomasyntaksia](inventory-visibility-api.md), jota käytät muille kuin WHS-nimikkeille. Nimikettä ei tarvitse määrittää sen mukaan, onko nimike WHS-nimike vai ei. Varaston näkyvyys erottaa nimikkeet automaattisesti tallennettujen tietojen perusteella.

WHS-nimikkeiden kyselyiden tulokset ovat pohjimmiltaan samat kuin ei-WHS-nimikkeiden tulokset. Ainoa ero on se, että seuraavat `fno`-tietolähteen fyysiset mitat lasketaan Supply Chain Managementin WHS-logiikan perusteella:

- `AvailOrdered`
- `AvailPhysical`
- `ReservOrdered`
- `ReservPhysical`

Kaikki muut fyysiset mitat lasketaan samoin kuin silloin, kun varaston näkyvyyden lisäasetusten toiminto ei ole käytössä.

Yksityiskohtaisia tietoja WHS-nimikkeiden käytettävissä oleva varastosaldon laskennasta on [Varaukset varastonhallinnassa](https://www.microsoft.com/download/details.aspx?id=43284) -raportissa.

Ne tietoentiteetit, jotka viedään Dataverseen, eivät voi vielä päivittää WHS-nimikkeiden määriä. Tietoyksiköissä näkyvät määrät ovat oikein sekä ei-WHS-nimikkeille että määrille, joihin WHS-logiikka ei vaikuta (eli muut mitat kuin `fno`-tietolähteen `AvailPhysical`, `AvailOrdered`, `ReservPhysical` ja `ReservOrdered`).

Supply Chain Management -tietolähteeseen tallennettujen WHS-nimikkeiden määrien muutokset ovat kiellettyjä. Kuten muut varaston näkyvyyden toiminnot, tätä rajoitusta käytetään ristiriitojen ehkäisemiseksi.

## <a name="soft-reservations-on-whs-items-in-inventory-visibility"></a>WHS-nimikkeiden alustava varaus varaston näkyvyydessä

Yleisesti WHS-nimikkeiden [alustavat varaukset](inventory-visibility-reservations.md) ovat tuettuja. Voit sisällyttää WHS:ään liittyviä fyysisiä mittoja alustavien varausten laskentaan. 

Tiedossa on rajoitus, jonka mukaan *varattavissa*-laskelmia ei tueta tällä hetkellä WHS-nimikkeille. Jos siis varauksia on olemassa niiden nykyisten dimensioiden yläpuolella, joita varten on tehty alustava varaus, *varattavissa*-laskenta on virheellinen. Alustavat varaukset eivät muutu, kun **ifCheckAvailForReserv** -asetus on poistettu käytöstä [alustavan varauksen sovellusliittymässä](inventory-visibility-api.md#create-one-reservation-event).

Tämä rajoitus koskee myös ominaisuuksia ja mukautuksia, jotka perustuvat alustaviin varauksiin (kuten kohdistus).

## <a name="calculate-available-to-promise-quantities"></a>Luvattavissa olevien määrien laskeminen

Ratkaisu tukee täysin [luvattavissa oleva määrää](inventory-visibility-available-to-promise.md) WHS-nimikkeille. Voit määrittää luvattavissa oleva määrän laskennat huolehtimatta WHS:ään liittyvistä tiedoista.
