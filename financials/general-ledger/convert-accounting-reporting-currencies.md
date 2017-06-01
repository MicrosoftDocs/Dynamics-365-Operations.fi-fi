---
title: Kirjanpito- tai raportointivaluutan muuntaminen
description: 
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: RobinARH
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 78223
ms.assetid: 31c56f9a-9c64-40a2-90e3-1969a760614b
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 728af2fff6317c17e47d48ea07dbeb57068fbf3f
ms.contentlocale: fi-fi
ms.lasthandoff: 05/25/2017


---

# <a name="convert-accounting-or-reporting-currencies"></a>Kirjanpito- tai raportointivaluutan muuntaminen

[!include[banner](../includes/banner.md)]




Yritys, joka on muutettava kirjanpito- tai raportointivaluuttaansa, voi tehdä tämän kahdella tavalla. Ensimmäinen vaihtoehto on luoda uusi yritys kokonaan alusta. Toinen vaihtoehto on suorittaa kirjanpito- ja raportointivaluutan muuntoprosessi. Tämä on erittäin pitkäkestoisten prosessi, jossa jokainen järjestelmässä oleva tapahtuma muuttuu. Ennen prosessin suorittamista on myös määritettävä joitakin asetuksia.

## <a name="preparing-the-legal-entity-for-currency-conversion"></a>Yrityksen valmisteleminen valuutan muuntamiseen
Ennen kuin voit muuntaa yrityksesi valuutan, ulkomaanvaluutan uudelleenarvostuksen summat on palautettava asiakas- ja toimittajatileille ja aiemmat tilikaudet on suljettava. Sinun on myös valmisteltava tietokanta muunnokseen ja tehtävä sitten vaadittavat muutokset yrityksen tiliin, jolla valuuttamuunnos suoritetaan. Kun olet suorittanut valuuttamuunnoksen, sinun täytyy suorittaa vielä joitakin muita menettelyjä. Sinun täytyy täsmäyttää muunnettujen summien pyöristyserot, laskea liiketoimintatilastot uudelleen, viedä kirjanpitotapahtumat kirjauskansioon, rajoittaa muuntotyökalun käyttöoikeutta ja arvostaa asiakas- ja toimittajatilien valuuttamääräiset summat uudelleen.

## <a name="setting-up-accounts-for-automatic-transactions"></a>Automaattisten tapahtumien tilien määrittäminen
Valuuttamuunnosprosessin aikana voitot tai tappiot tai sentteinä mitattavat erot kirjataan tileille, jotka on määritetty **Automaattisten tapahtumien tilit** -sivulla. Päätilit on määritettävä seuraavantyyppisille tapahtumille ennen muuntoprosessin suorittamista:

-   Kirjanpitovaluutan konversion pyöristysvoitto
-   Kirjanpitovaluutan konversion pyöristystappio
-   Pyöristysero kirjanpitovaluuttana
-   Pyöristysero raportointivaluutassa
-   Vuoden lopun tulos

## <a name="posting-rounding-differences-and-sum-recalculations"></a>Pyöristyserojen kirjaaminen ja summien uudelleenlaskenta
Seuraavat tiedot kuvaavat, missä pyöristyseroja saattavat ilmetä:

-   Jos tuotteiden hinnaksi on muunnettu nolla, tulostuu raportti, jossa näkyvät tuotenumero, moduulityyppi, hinta ennen muunnosta sekä yksikkö.
-   Arvonlisäveron ja kirjanpidon välillä syntyneet pyöristyserot kirjataan kirjauskansioon.
-   Valuuttamääräiset uudelleenarvostuksen summat sekä asiakkaan ja toimittajan tapahtumasummat lasketaan uudelleen.
-   Asiakas- ja toimittajatilitystietueet luodaan jokaisen asiakas- ja toimittajatapahtuman pyöristyseroja varten.
-   Asiakkaiden ja toimittajien pyöristyserot kirjataan kirjauskansioon.
-   Selvitetyt kustannussummat ja kustannuserosummat suljetussa varastotapahtumissa lasketaan uudelleen.
-   Varastohallinnassa syntyneet pyöristyserot kirjataan kirjauskansioon.
-   Käytettävissä oleva varasto lasketaan uudelleen.
-   Kirjanpidon kirjauskansioiden kokonaissummat lasketaan uudelleen.
-   Kirjanpidon tilinpäätöserittelyt lasketaan uudelleen.
-   Kirjanpidon saldot lasketaan uudelleen.
-   Kirjanpidossa syntyneet pyöristyserot kirjataan kirjauskansioon.
-   Kirjanpidon avaustapahtumat lasketaan uudelleen.
-   Kirjanpidon saldojen lopullinen määrä lasketaan.

Jos muunnat uuteen kirjanpitovaluuttaan ja virhe on tapahtunut kokonaissummien uudelleenlaskennassa tai pyöristyserojen kirjauksessa, sinun on suljettava **Kirjanpidon valuuttamuunnos** -sivu. Kokonaissummat lasketaan uudelleen ja pyöristyserot kirjataan.

## <a name="processing-the-currency-conversion"></a>Valuuttamuunnoksen käsitteleminen
Kun käynnistät valuuttamuunnosprosessin, kaikkien käyttäjien on kirjauduttava ulos järjestelmästä. Sinun täytyy määrittää uusi kirjanpito- tai raportointivaluutta sekä vaihtokurssit. Kun valitset **OK**, prosessi suoritetaan, ja se päivittää jokaisen tapahtuman järjestelmään. Valuuttamuunnos voi kestää kauan. Kun se on valmis, kirjanpito- tai raportointivaluutta näkyy päivitettynä **Kirjanpito**-sivulla.

## <a name="completing-the-currency-conversion"></a>Valuuttamuunnoksen päättäminen
Kaikki täsmäytysraportit on suoritettava uudelleen valuuttamuunnoksen jälkeen, jotta voidaan varmistaa, että kaikki muunnetut summat ovat oikein.

-   Jos kirjanpitovaluutan muunnos aiheuttaa pyöristyseroja, niitä ei voi kirjata käyttämällä tositetta, jossa pyöristysero on muodostunut. Erot kirjataan sen sijaan käyttämällä muunnoskirjauksille syötetyillä tositteilla. Pyöristyserot tulostuvat muunnoksen jälkeen kaikkiin raportteihin, joissa tarkistus tehdään tositteittain ja päivämäärittäin. Tämä on täysin oikein, eikä siihen tarvitse kiinnittää huomiota.
-   Jos asiakkaan ja toimittajan täsmäytysraporttien kokonaissummarivillä näkyy eri summa eikä eroa ollut ennen muunnosta, erotussumma on kirjattava. Se kirjataan asiakkaiden ja toimittajien reskontratilille. Vastatili on muunnostappion tai -voiton kirjanpitotili.

Kun kaikki kirjanpidon tapahtumakirjauskansiot on poistettu, voit kirjata kirjanpitotapahtumat kirjauskansioon. Valitse **Kirjanpito** &gt; **Kausittainen** &gt; **Kirjauskansiot** &gt; **Kirjauskansion kirjanpito**. Voit tarvittaessa uudelleenarvostaa valuuttasummat valuuttamuunnoksen jälkeen. Voit uudelleenarvostaa valuuttasummat valitsemalla uudelleenarvostuksen **Menetelmä**-kentästä **Vakio**-vaihtoehdon.




