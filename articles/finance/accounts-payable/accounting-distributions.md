---
title: Kirjanpidolliset jaot
description: Tässä aiheessa on tietoja kirjanpidollisista jaoista ja niiden käsittelyvaihtoehdoista.
author: ShylaThompson
ms.date: 09/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AccountingDistribution
audience: Application User
ms.reviewer: roschlom
ms.custom: 17231
ms.assetid: 9030355d-8e6e-408b-9e7d-7b346eaa652c
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c17c2e00c8c3b32062f70baf1da76a04dcd5d924
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5820952"
---
# <a name="accounting-distributions"></a>Kirjanpidolliset jaot

[!include [banner](../includes/banner.md)]

Tässä aiheessa on tietoja kirjanpidollisista jaoista ja niiden käsittelyvaihtoehdoista. Kirjanpidollisia jakoja käytetään kohdistettaessa lähdeasiakirjan rahasummat tietyille kirjanpitotileille. 

Kirjanpidolliset jaot ovat koko ohjelman kattavia ominaisuuksia, joita käytetään ja jotka ulottuvat kuhunkin lähdeasiakirjaan, esimerkiksi ostotilaukseen, toimittajalaskuun, kuluraporttiin ja vapaatekstilaskuihin. Oletusarvona, kirjanpidon jaon oletusarvo luodaan jokaiselle asiakirjan lähderiville ja rahasummalle, ja se on käytössä ehdollisesti muokattavana. 

> [!NOTE] 
> Jotkut asiakirjat tukevat myös asiakirjan otsikon rahasummia, kuten tilaus- ja laskukuluja. 

Yleiset kirjanpidolliset jako-ominaisuudet tarjoavat seuraavia vaihtoehtoja kirjanpidollisten jakojen käsittelyyn:

-   **Jakosummat** – Tarkastele ja muokkaa yksittäisen asiakirjaotsikon tai rivin tai minkä tahansa alirivin kirjanpidollisia jakoja, kuten veroja tai maksuja.
    -   Ylimmissä rahasummien jaoissa (ylätason jaot), päätilin ja taloushallinnon dimensiot saattavat olla muokattavia suoraan segmentoidussa kulunvalvonta ruudukossa. Tämä laajennettu hinta on tyypillinen esimerkki ylätason jaosta.
    -   Jaot summat perustuvat asiakirjan termivaluuttaan. Tämä valuutta on tavallisesti tapahtuman valuuttana. Valuuttasummien raportointi ja kirjanpito luodaan osana alareskontran kirjanpitoa.
    -   Jaot näyttävät kirjauspäivän ja kirjanpitotapahtuman. Yleensä kirjanpitotapahtuma määritetään **tyhjäksi** kunnes asiakirja on kirjattu kirjauskansioon. Siinä vaiheessa kirjanpitotapahtumasta tulee **alkuperäinen**. Sen jälkeen kun jaot on kirjattu, jakoja ei voida enää muokata.
    -   **Jaa**-painikkeen voi ottaa käyttöön ylätason jakoihin. **Jaa**-painike luo uudet kirjanpidon jaot ja jako voidaan perustaa prosenttiosuuteen, summaan tai määrään.
    -   **Jaetaan tasan** -painiketta voidaan käyttää yhdessä **jako** -painikkeen kanssa jakamaan summa automaattisesti tasan eri jakoihin.
    -   **Palauta** -painike voi olla käytössä ylätason jaoille, silloin kun enemmän kuin yksi jakelu on luotu. **Palauta**-painike kumoaa kaikki jaon manuaaliset muutokset poistamalla kaikki olemassa olevat jaot ja luomalla uudelleen jaot oletusarvon mukaan.
    -   Alemman tason jakelut, kuten alennus, kulut ja arvonlisävero noudattavat aina ylätason jakoa. Voit tarkastella päätason ja alitasojen suhdetta kohdassa **Viite** &gt; > **Ylätason tiedot**.
    -   Päätili ja taloushallinnon dimensiot saattavat olla muokattavia myös alatasolla.
    -   Taloushallinnon dimensiot kirjanpidollisissa jaoissa noudattavat oletusarvokuviota, jossa tiedoston voi laajentaa.
    -   Varianssijaokoja voidaan luoda vastaavissa skenaarioita, kuten vastaava toimittajalasku ja ostotilaus. Voit tarkastella kirjanpidollisten jakojen täsmäytyksen suhteita kohdassa **Viite** > &gt; **Asiakirjan tiedot**.
    -   **Oikaise**-painike tulee näkyviin ja on käytössä niille asiakirjoille, jotka tukevat oikaisuja. **Korjaa** luo uusia jakoja. Ensin luodaan jakaumat, jotka peruuttavat alkuperäiset jaot. Näitä jakoja ei voi muokata. Luodaan seuraavaksi uudet oikeat kirjanpidolliset jaot. Näitä jakoja voidaan muokata, jos alkuperäisiä jakoja voidaan muokata.
    -   **Projektin tiedot**-painike on käytettävissä jatkeena silloin kun rivi liittyy projektiin. Projektin kirjanpidollisien jakojen avulla voit muokata tietoja, kuten rahoituksen lähde- ja riviominaisuudet.
    -   Voit tarkastella nykyisen asiakirjan kirjanpidollista tilaa kohdassa **Viite**. Tila on koko asiakirjalle ja ilmaisee, onko asiakirja on keskeneräinen tai valmis.
-   **Tarkastele jakoja** – Näytä asiakirjan kirjanpidolliset jaot kaikille riveille ja rahasummille. Et voi muokata kirjanpidollisia jakoja tästä näkymästä.

Versioon 10.0.13 on lisätty toiminto, joka vahvistaa kirjanpidon jakotaulukon sen varmistamiseksi, että uudet kentät on määritetty oikein. Tämän toiminnon nimi on **Ota lisävahvistus asiakirjojen tiedoille käyttöön käyttämällä lähdeasiakirjan kirjanpitokehystä**. Jos haluat käyttää ominaisuutta, sinun on otettava se käyttöön **Toiminnonhallinta**-työtilan avulla. Jos haluat ottaa toiminnon käyttöön, etsi sen nimeä **Toiminnonhallinta**-sivun **Haku**-kentässä ja valitse sitten **Ota käyttöön nyt**.

Lisätietoja on kohdassa [Toimittajan laskujen kirjanpidolliset jaot ja alatason kirjauskansion merkinnät](accounting-distributions-subledger-journal-entries-vendor-invoices.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]