---
title: Yksittäisten numerosarjojen määrittäminen
description: Tässä artikkelissa selitetään, miten numerosarjat määritetään yksittäin.
author: SunilGarg
ms.date: 08/16/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: NumberSequenceTableListPage, NumberSequenceDetails
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7be72d348957c5c6494958276b2baa9c67d63c58
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904985"
---
# <a name="set-up-number-sequences-on-an-individual-basis"></a>Yksittäisten numerosarjojen määrittäminen

[!include [banner](../../includes/banner.md)]

Tässä artikkelissa selitetään, miten numerosarjat määritetään yksittäin. Numerosarjoja käytetään muodostamaan päätietotietueille ja niitä tarvitsevilla tapahtumatietueille luettavia, yksilöllisiä tunnisteita. Tunnisteen vaativaa päätietoa tai tapahtumatietuetta kutsutaan numellä viite. Ennen kuin voit luoda viitteelle uusia tietueita, määritä numerosarja ja kohdista se viitteeseen. Voit määrittää kaikki tarvittavat numerosarjat samaan aikaan käyttämällä **Määritä numerosarjat** -ohjattua toimintoa tai voit luoda tai muokata yksittäisiä numerosarjoja käyttämällä **Numerosarjat**-sivua.

1. Siirry kohtaan **Siirtymisruutu > Moduulit > Organisaation hallinta > Numerosarjat > Numerosarjat**.
2. Valitse **Numerosarja**.
3. Kirjoita arvo **Numerosarjan koodi** -kenttään.
4. Kirjoita arvo **Nimi**-kenttään.
5. Valitse **Laajuuden parametrit** -pikavälilehdellä numerosarjan alue ja valitse alueen arvot avattavasta luettelosta. Laajuus määrittää mitkä organisaatiot käyttävät numerosarjaa. Lisäksi numerosarjoilla joiden alue on muu kuin **Jaettu** voi olla osia, jotka vastaavat niiden aluetta. Esimerkiksi numerosarja, jonka vaikutusalue on **Oikeushenkilö**, voi sisältää yrityssegmentin. Lisätietoja laajuuksista on [Numerosarjan esittely](../number-sequence-overview.md) -kohdan ohjeaiheessa. 
6. Laajenna **Segmentit**-osa.
    - Määritä numerosarjalle muoto lisäämällä, poistamalla ja uudelleenjärjestelemällä segmenttejä.  
    - Kaikkien alueiden numerosarjat voivat sisältää *kiinteitä segmenttejä* ja *aakkosnumeerisia segmenttejä*. Kiinteät segmentit sisältävät sarjan aakkosnumeerisia merkkejä, jotka eivät muutu. Tämän segmenttityypin avulla voit lisätä väliviivan tai muun erottimen numerosarjasegmenttien välille. Aakkosnumeeriset segmentit sisältävät yhdistelmän ristikkomerkkejä (#) ja et-merkkejä (&). Nämä merkit vastaavat kirjaimia ja numeroita, jotka kasvavat aina, kun sarjan numeroa käytetään. Käyttää ristikkomerkkiä (#) osoittamaan kasvavia numeroita ja et-merkkiä (&) osoittamaan kasvavia kirjaimia. Esimerkiksi muodon `#####_2014` avulla luodaan sarja `00001_2014`, `00002_2014` jne. Käytössä on oltava vähintään yksi aakkosnumeerinen segmentti. Alueen osat, kuten yritys tai oikeushenkilö, eivät ole pakollisia. Vaikka et sisällytä alueen segmenttejä muotoon, valitun viitteen numerot luodaan edelleen aluekohtaisesti.  
7. Laajenna **Viitteet**-osa. Valitse asiakirjan tyyppi tai tietue jolle tämä numerosarja määritetään. Tämä vaihe on valinnainen niille numerosarjoille, jotka on määritetty erityisiä sovelluksia varten. Näissä tilanteissa uusi numero luodaan ilman viittausta käyttämällä numerosarjan koodin tai tunnuksen arvoa. Esimerkki erityisestä hakemuksen käyttötavasta on tositesarja jota käytetään tiettyihin kirjauskansion nimiin. Emme kuitenkaan suosittele, että käytät näitä kuvioita.  
8. Laajenna **Yleiset**-osa. Määritä Yleinen-pikavälilehdellä, onko numerosarja manuaalinen, jatkuva tai ei-jatkuva. Kirjoita lisäksi pienimmät ja suurimmat numerosarjassa käytettävät numerot. Emme suosittele ei-jatkuvan numerosarjan muuttamista jatkuvaksi numerosarjaksi. Numerosarja ei ole todellisuudessa jatkuva. Tämä muutos saattaa myös aiheuttaa tietokannassa päällekkäisten avainten virheitä. Lisäksi jatkuvilla numerosarjoilla on suurempi vaikutus suorituskykyyn.   
9. Valitse **Tallenna**.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
