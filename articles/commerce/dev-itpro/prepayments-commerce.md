---
title: Ennakkomaksut Dynamics 365 Commercessa
description: Tämä artikkeli tarjoaa yleiskatsauksen ennakkomaksutapahtumien käsittelystä Microsoft Dynamics 365 Commercessa.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2021-06-28
ms.openlocfilehash: 8262470f83481ef8840857a52948c0833d8b278e
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780354"
---
# <a name="prepayments-in-dynamics-365-commerce"></a>Ennakkomaksut Dynamics 365 Commercessa

[!include[banner](../includes/banner.md)]

Tämä artikkeli tarjoaa yleiskatsauksen ennakkomaksutapahtumien käsittelystä Microsoft Dynamics 365 Commercessa.

Dynamics 365 Commerce käsittelee seuraavia myyntireskontrassa ja Commercessa käytettäviä ennakkomaksutapahtumien maksutyyppejä:

- **Asiakastilin talletusmaksu** – Asiakas maksaa talletuksen myyntipisteessä. Commerce käsittelee talletusmaksun ennakkomaksutapahtumana. Kun kirjaat tapahtuman maksukirjauskansio luodaan ja kirjataan Commerce headquartersin **Kirjauskansion tosite** -sivulle. Maksukirjauskansiolle valitaan automaattisesti **Ennakkomaksukirjauskansion tosite** -valintaruutu **Maksu**-välilehdessä. Lisätietoja esimerkiksi ennakkomaksusta ja verokohtaisista tiedoista kohdealueella on kohdassa [Maa- tai aluekohtainen ohjesisältö](/dynamics365/fin-ops-core/dev-itpro/lcs-solutions/country-region?context=%2Fdynamics365%2Fcontext%2Ffinance#countryregion-specific-help-content).
- **Asiakastilaus, jolla on talletus** – Asiakas luo asiakastilauksen myyntipisteessä. Asiakas voi maksaa tilauksen talletuksen **Asiakastilaukset**-sivun oletustalletusprosentin perusteella Commerce headquartersissa (**Commerce-parametrit \> Asiakastilaukset**). Commerce käsittelee asiakastilauksen talletusmaksun ennakkomaksutapahtumana. Kun kirjaat tapahtuman maksukirjauskansio luodaan ja kirjataan **Kirjauskansion tosite** -sivulle. Maksukirjauskansiolle valitaan automaattisesti **Ennakkomaksukirjauskansion tosite** -valintaruutu **Maksu**-välilehdessä. Maksu selvitetään ja myyntilasku luodaan automaattisesti, kun tilaus kerätään tai toimitetaan.
- **Puhelinkeskuksen myyntitilaus** - Puhelinkeskuksen myyjä luo myyntitilauksen asiakkaan puolesta ja **ennakkomaksun** määritteeksi asetetaan **Kyllä** maksun sieppauksen aikana.

Commerce suorittaa ennakkomaksun käsittelemiseksi seuraavat tehtävät:

- **Käsittele asiakastilin talletusmaksu** – Asiakkaan tekemä talletusmaksu siirretään Commerceen käyttämällä tiedot synkronoivaa palvelua. Commerce luo maksulle vähittäismyyntimaksutapahtuman. Kun kirjaat vähittäismyyntitapahtuman, kirjataan käteisvarojen kirjauskansio tai asiakkaan maksukirjauskansio. Maksukirjauskansiolle valitaan automaattisesti **Ennakkomaksukirjauskansion tosite** -valintaruutu **Maksu**-välilehdessä **Kirjauskansion tosite** -sivulla Commerce headquartersissa. Ennakkomaksuja ei voi käsitellä, jos maksun summa on negatiivinen.
- **Käsittele asiakas- tai myyntistilaus, jolla on talletus** – Asiakas maksaa vaaditun talletuksen asiakastilaukselle käyttämällä Commerce Data Exchange: Reaaliaikainen palvelu -toimintoa. Commerce luo asiakkaan maksukirjauskansion tai käteisen kirjauskansion sen mukaan, mitä maksutapaa asiakas käyttää. Kirjauskansiolle valitaan automaattisesti **Ennakkomaksukirjauskansion tosite** -valintaruutu **Maksu**-välilehdessä **Kirjauskansion tosite** -sivulla Commerce headquartersissa. Jos asiakas käyttää osittaisten maksujen maksamiseen useita maksutapoja, Commerce käsittelee kunkin osamaksun käytetyn maksutavan perusteella.

Commerce lähettää luottokortin maksutapojen pohjana olevien digitaalisten luottokorttien ja digitaalisten allekirjoitusten yhteydessä "sieppauspyynnön" onnistuneen valtuutuksen jälkeen. (Varat siepataan ennen myyntitilauksen laskutusta.)

Jos peruutat asiakastilauksen, ennakkomaksun summa palautetaan ja talletussummalle kirjataan hyvityksen maksukirjauskansio. Hyvityssumma lasketaan ja kirjataan hyvitysmaksun kirjaamisen yhteydessä määritetyn maksutavan mukaan. Commerce saattaa käyttää peruutusmaksua Commerce headquartersin **Commerce-parametrit** -sivulla määritetyn prosenttiosuuden mukaan.

Jos palautat asiakastilauksen, luodaan palautustilaus ja hyvitysmaksun kirjauskansio. Kun kirjaat palautustilauksen, Commerce luo joko asiakkaan maksukirjauskansion tai käteisen kirjauskansion sen mukaan, mitä maksutapaa asiakas on käyttänyt alkuperäisessä tapahtumassa.
