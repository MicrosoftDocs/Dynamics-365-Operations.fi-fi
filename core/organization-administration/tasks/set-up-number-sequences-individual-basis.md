--- 
title: "Yksittäisten numerosarjojen määrittäminen"
description: "Numerosarjoja käytetään muodostamaan päätietotietueille ja niitä tarvitsevilla tapahtumatietueille luettavia, yksilöllisiä tunnisteita."
author: sericks007
manager: AnnBe
ms.date: 06/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 5c63022586f24cc1a50f7734910f15b237d35216
ms.contentlocale: fi-fi
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-number-sequences-on-an-individual-basis"></a>Yksittäisten numerosarjojen määrittäminen

[!include[task guide banner](../../includes/task-guide-banner.md)]

Numerosarjoja käytetään muodostamaan päätietotietueille ja niitä tarvitsevilla tapahtumatietueille luettavia, yksilöllisiä tunnisteita. Tunnisteen vaativaa päätietoa tai tapahtumatietuetta kutsutaan numellä viite. Ennen kuin voit luoda viitteelle uusia tietueita, määritä numerosarja ja kohdista se viitteeseen. Voit määrittää kaikki tarvittavat numerosarjat samaan aikaan käyttämällä Määritä numerosarjat -ohjattua toimintoa tai voit luoda tai muokata yksittäisiä numerosarjoja käyttämällä Numerosarjat-sivua.

1. Siirry kohtaan Organisaation hallinta > Numerosarjat > Numerosarjat.
2. Napsauta Numerosarja.
3. Kirjoita arvo Numerosarjan koodi -kenttään.
4. Kirjoita arvo Nimi-kenttään.
5. Laajenna Laajuuden parametrit -osa.
    * Valitse Laajuuden parametrit -pikavälilehdellä numerosarjan alue ja valitse alueen arvot.     Laajuus määrittää mitkä organisaatiot käyttävät numerosarjaa. Lisäksi numerosarjoilla joiden alue on muu kuin Jaettu voi olla osia, jotka vastaavat niiden aluetta. Esimerkiksi numerosarja, jonka vaikutusalue on Oikeushenkilö, voi sisältää yrityssegmentin. Lisätietoja laajuuksista on Numerosarjan esittely -kohdan ohjeaiheessa.  
6. Laajenna Segmentit-osa.
    * Määritä Segmentit-pikavälilehdellä numerosarjalle muoto lisäämällä, poistamalla ja uudelleenjärjestelemällä segmenttejä.  
    * Kaikkien alueiden numerosarjat voivat sisältää kiinteitä ja aakkosnumeerisia segmenttejä. Kiinteät segmentit sisältävät sarjan aakkosnumeerisia merkkejä, jotka eivät muutu. Tämän segmenttityypin avulla voit lisätä väliviivan tai muun erottimen numerosarjasegmenttien välille. Aakkosnumeeriset segmentit sisältävät yhdistelmän ristikkomerkkejä (#) ja et-merkkejä (&). Nämä merkit vastaavat kirjaimia ja numeroita, jotka kasvavat aina, kun sarjan numeroa käytetään. Käyttää ristikkomerkkiä (#) osoittamaan kasvavia numeroita ja et-merkkiä (&) osoittamaan kasvavia kirjaimia. Esimerkiksi muodon #####_2014 avulla luodaan sarja 00001_2014, 00002_2014 jne.     Käytössä on oltava vähintään yksi aakkosnumeerinen segmentti. Alueen osat, kuten yritys tai oikeushenkilö, eivät ole pakollisia. Vaikka et sisällytä alueen segmenttejä muotoon, valitun viitteen numerot luodaan edelleen aluekohtaisesti.  
7. Laajenna Viitteet-osa.
    * Valitse Viitteet-pikavälilehdellä asiakirjan tyyppi tai tietue jolle tämä numerosarja määritetään.     Tämä vaihe on valinnainen niille numerosarjoille, jotka on määritetty erityisiä sovelluksia varten. Näissä tilanteissa uusi numero luodaan ilman viittausta käyttämällä numerosarjan koodin tai tunnuksen arvoa. Esimerkki erityisestä hakemuksen käyttötavasta on tositesarja jota käytetään tiettyihin kirjauskansion nimiin. Emme kuitenkaan suosittele, että käytät näitä kuvioita.  
8. Laajenna Yleiset-osa.
    * Määritä Yleinen-pikavälilehdellä, onko numerosarja manuaalinen, jatkuva tai ei-jatkuva. Kirjoita lisäksi pienimmät ja suurimmat numerosarjassa käytettävät numerot.     Emme suosittele ei-jatkuvan numerosarjan muuttamista jatkuvaksi numerosarjaksi. Numerosarja ei ole todellisuudessa jatkuva. Tämä muutos saattaa myös aiheuttaa tietokannassa päällekkäisten avainten virheitä. Lisäksi jatkuvilla numerosarjoilla on suurempi vaikutus suorituskykyyn.   
9. Valitse Tallenna.


