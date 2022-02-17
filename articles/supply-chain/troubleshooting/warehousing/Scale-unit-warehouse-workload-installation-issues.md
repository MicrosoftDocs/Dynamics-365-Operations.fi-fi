---
title: Käsittelyongelmat tapahtuvat, kun skaalausyksikön varaston työkuorma on asennettu
description: Tässä aiheessa kuvataan ongelmia, jotka voivat ilmetä nopeasti skaalausyksikön varaston kuormituksen asennuksen jälkeen, ja antaa ohjeita niiden korjaamisesta.
author: perlynne
ms.date: 1/13/2022
ms.topic: troubleshooting
ms.search.form: WHSLoadPlanningWorkbench, WHSOutboundLoadPlanningWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2022-01-13
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: f589ffed61b695f471989ab1dd693f30cd5d5262
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/31/2022
ms.locfileid: "8071634"
---
# <a name="processing-issues-occur-after-a-scale-unit-warehouse-workload-is-installed"></a>Käsittelyongelmat tapahtuvat, kun skaalausyksikön varaston työkuorma on asennettu

Tässä aiheessa kuvataan ongelmia, jotka voivat ilmetä nopeasti skaalausyksikön varaston kuormituksen asennuksen jälkeen, ja antaa ohjeita niiden korjaamisesta.

## <a name="issue-1-error-after-a-load-is-released-from-a-load-planning-workbench"></a>Ongelma 1: Virhe sen jälkeen, kun kuorma on vapautettu kuormitussuunnittelusta

### <a name="symptoms-of-issue-1"></a>Ongelman 1 oireet

Kun vapautat kuorman **Kuormasuunnittelun työtila**- tai **Lähtevän kuormasuunnittelun työtila** -sivulta, näkyviin tulee virhesanoma, joka on seuraavassa muodossa:

> Poikkeus kirjattaessa kuormaa %1, kuormaa ei voitu vapauttaa.
> 
> UPDATE WHSSHIPMENTTABLE SET ...
> 
> Shipments-tietuetta ei voi muokata (WHSShipmentTable). Lähetyksen tunnus: ...

Tässä on todellinen esimerkki, joka sisältää esimerkkitiedot:

> Poikkeus kirjattaessa kuormaa USMF-000033, kuormaa ei voitu vapauttaa.
istunto 5133 (järjestelmänvalvoja)
>
> UPDATE WHSSHIPMENTTABLE SET ORDERNUM=?,RECVERSION=?,MODIFIEDDATETIME=?,MODIFIEDBY=? WHERE ((RECID=?) AND (RECVERSION=?))  
> [Microsoft][ODBC Driver 17 for SQL Server][SQL Server]Scale Unit @@ attempted to update records owned by Scale Unit @A.  
> Objektipalvelin – Azure:
>
> Shipments-tietuetta ei voi muokata (WHSShipmentTable). Lähetyksen tunnus: USMF-000031, USMF-000033. SQL-tietokanta on ilmoittanut virheen.

### <a name="cause-of-issue-1"></a>Ongelman 1 syy

Tämä ongelma voi ilmetä, jos skaalausyksikön varaston kuormitusta asentaessa on olemassa seuraava ehtojen yhdistelmä:

- Järjestelmä sisältää vapauttamattoman kuormituksen, jossa on useita rivejä liitettynä eri tilauksiin, ja joitakin kuormarivejä ei ole liitetty lähetykseen.
- Järjestelmä on määritetty käyttämään lähetyksen konsolidointia.

Jaetussa hybriditopologiassa jokainen kuorma- ja lähetystietue on merkitty tietyn skaalausyksikön tai keskuksen omistamaksi. Kun vapautat kuormituksen **Kuormasuunnittelun työtila** -sivulta, järjestelmä muuttaa määritettyä omistajaa. Aiemmin lueteltujen ehtojen vuoksi järjestelmä ei ehkä kuitenkaan voi ratkaista tietojen omistajaa. Näin ollen kuormaa ei vapauteta varastoon.

### <a name="resolution-of-issue-1"></a>Ongelman 1 ratkaisu

Jaa kuorma kahteen pienempään kuormaan, ennen kuin vapautat sen varastoon.

## <a name="issue-2-error-while-a-wave-is-processed-on-a-scale-unit"></a>Ongelma 2: Virhe, kun aalto käsitellään skaalausyksikössä

### <a name="symptoms-of-issue-2"></a>Ongelman 2 oireet

Kun käsittelet aaltoa skaalausyksikössä, saat virhesanoman, joka on seuraavassa muodossa:

> Et voi muokata kuormariviä, jonka RecId = %1, kuormatunnus = %2, koska sen omistaa edelleen yritystoiminto. Varmista, että vastaava lähtevä kuorma on vapautettu skaalausyksikköön ja että näin luodaan varastotilausrivit.

Tässä on todellinen esimerkki, joka sisältää esimerkkitiedot:

> Infoloki työlle Suorita aalto USMF-000000012 (9223377668365210)  
> Infoloki tehtävälle Suorita aalto USMF-000000012 (9223377668370462)  
> Et voi muokata kuormariviä, jonka RecId = 68719478242, kuormatunnus = USMF-000034, koska sen omistaa edelleen yritystoiminto. Varmista, että vastaava lähtevä kuorma on vapautettu skaalausyksikköön ja että näin luodaan varastotilausrivit.

### <a name="cause-of-issue-2"></a>Ongelman 2 syy

Jaetussa hybriditopologiassa jokainen kuorma- ja lähetystietojen omistajuus on määritetty tietylle skaalausyksikölle tai keskukselle. Osana aaltokäsittelyä tietojen omistusoikeuden odotetaan olevan määritettynä skaalausyksikölle.

Jos asennat skaalausyksikön varaston työkuorman, järjestelmä ei voi hallita tietojen omistajuutta, jos avoimeen lähetykseen on liitetty kuorma ja aalto. Sen vuoksi aallon käsittely epäonnistuu skaalausyksikössä.

### <a name="resolution-of-issue-2"></a>Ongelman 2 ratkaisu

Vapauta kuorma varastoon keskuksesta.

## <a name="troubleshoot-issues-by-viewing-a-records-ownership-and-destination"></a>Ongelmien vianmääritys tarkastelemalla tietueen omistajaa ja kohdetta

Jaetussa hybriditopologiassa monen tyyppiset tietueet on merkitty tietyn skaalausyksikön tai keskuksen omistamaksi. Kun siirryt jaettuun hybriditopologiaan ja/tai määrität uuden skaalausyksikön varaston työkuorman, järjestelmä liittää omistajuuden kuhunkin asiaankuuluvaan tietueeseen. Tämä prosessi voi joskus aiheuttaa virheitä tai odottamattomia tuloksia. Siksi tietueen omistuksen ja siirtokohteen tiedot voivat auttaa näiden muutosten jälkeisten ongelmien vianmäärityksessä.

Noudattamalla näitä ohjeita voit tarkastella tietueen omistajuuden ja siirtokohteen tietoja.

1. Avaa asiaankuuluva tietue.
1. Valitse **Asetukset**-välilehden **Tietueen tiedot** -ryhmän toimintoruudussa **Näytä kaikki kentät**.
1. Avautuvalla sivulla näkyvät kaikkien kenttien arvot, jotka ovat käytettävissä valitulle tietueelle. Tarkista seuraavat kentät:

    - **SYSSCALEUNITID** – Tässä kentässä näkyy tietueen nykyinen omistaja.
    - **SYSTARGETSCALEUNITID** – Tässä kentässä näkyy sen keskuksen tai skaalausyksikön tunnus, jonne tietue siirretään, kun nykyinen omistaja on saanut sen valmiiksi. Tämän kentän arvoa käyttävät erätyöt, jotka hallitsevat tämäntyyppistä prosessia. Vaikka tämä kenttä ei liity suoraan omistajuuteen, omistajuus voi muuttua, kun tietue siirretään. Joissakin tapauksissa tämä kenttä on tyhjä.
