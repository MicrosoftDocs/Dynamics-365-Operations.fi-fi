---
title: Kopioi toimittajat käyttämällä jaettuja numerosarjoja
description: Tässä ohjeaiheessa kerrotaan, miten jaettujen numerosarjojen avulla toimittaja kopioidaan toiseen yritykseen pitäen toimittajatunnus ennallaan.
author: sunfzam
ms.date: 08/24/2018
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: VendTable
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 4cea8269082b39e2374ffb3c3dc82def8ce35679
ms.sourcegitcommit: 9cbff8a2cdeaf606488fb0044b3de4ab4409c9dc
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/26/2022
ms.locfileid: "8358462"
---
# <a name="copy-vendors-by-using-shared-number-sequences"></a>Kopioi toimittajat käyttämällä jaettuja numerosarjoja

[!include [banner](../includes/banner.md)]

Toimittajatunnukset voidaan määrittää jaettujen numerosarjojen avulla. Jaettujen numerosarjojen avulla voidaan kopioida toimittajia yrityksestä toiseen ja käyttää samoja toimittajatunnuksia molemmissa yrityksissä.

## <a name="setup"></a>Määritys

Toiminto on käytössä, kun toimittajatunnukset määritetään jaettujen numerosarjojen avulla. Samaa numerosarjaa on käytettävä kaikissa yrityksissä, joihin toimittaja halutaan kopioida. Toimittajan numerosarjan voi muuttaa kunkin yrityksen **Ostoreskontran parametrit** -sivulla. Valitse **Ostoreskontra** \> **Asetukset** \> **Ostoreskontran parametrit** ja **Numerosarjat**-välilehti.

Toimittajanumerosarjat voidaan määrittää jokaiselle toimittajaryhmälle. Myös nämä numerosarjat on jaettava. Toimittajaryhmän numerosarja käytetään ensin. Jos toimittajaryhmälle ei ole määritetty numerosarjaa, käytetään **Ostoreskontran parametrit** -sivulla määritettyä numerosarjaa.

Toimittajia voidaan kopioida yritysten välillä myös käytettäessä manuaalisia toimittajatunnuksia. Jos toimittaja yritetään kopioida yritykseen, jossa toimittajatunnus on jo käytössä, kopiointiprosessia ei voi käynnistää.

## <a name="copy-a-vendor"></a>Kopioi toimittaja

Toimittaja kopioidaan valitsemalla **Kaikki toimittajat** -luettelosivulla **Uusi**. **Kaikki toimittajat, uusi tietue** -sivu avautuu. Uutta toimittajatunnusta ei määritetä heti. Tämä toiminnallisuus eroaa aiempien versioiden toiminnallisuuksista. Toimittajaryhmää ei ole vielä valittu, joten oikeaa käytettävää numerosarjaa ei voi määrittää. Ei voi myöskään määrittää, halutaanko luoda uusi toimittaja vai kopioida toimittaja. Siksi toimittajatunnus määritetään vasta kun valitset **Tallenna**-vaihtoehdon sivun alareunassa.

Jos luot uutta toimittajaa, voit jatkaa täyttämään kaikki kentät tavalliseen tapaan. Kun olet valmis ja valitset **Tallenna**, toimittajatunnus määritetään automaattisesti. Jos käytetään manuaalisia numerosarjoja, huomaat, että käytettiin manuaalista toimittajatunnusta.

Voit kopioida toimittajan syöttämällä **Nimi**-kenttään vähintään yhden merkin, joka edustaa etsittävää toimittajaa. Hakuvalintaikkunassa näkyy luettelo, jossa etsittävä toimittaja saattaa näkyä. Kun valitset jonkun osapuolen, valintaikkunan oikealla puolella näkyy lisätietoja:

- **Yleistä**-välilehdessä näkyy osapuolen puhelinnumero ja osoite.
- Valitun osapuolen mahdolliset roolit ja yritykset näkyvät **Roolit**-välilehdessä.
- Osapuolen verotunnukset näkyvät **Verorekisteröintitunnus**-välilehdessä.

Voit kopioida osapuolen vain, jos sen rooli on toimittaja ja jos sillä on tämä rooli muussa kuin nykyisessä yrityksessä. Kun olet löytänyt nämä ehdot täyttävän osapuolen, toimi seuraavasti.

1. Näkyviin tulee **Kopioi toimittaja** -vaihtoehto. Tämä vaihtoehto on oletusarvoisesti **Ei**. Voit kopioida toimittajan nykyiseen yritykseen valitsemalla **Kyllä**. 
2. **Yritys**-kenttä tulee näkyviin. Valitse yritys, josta toimittaja kopioidaan Jos toimittaja kuuluu vain yhteen yritykseen, kenttään määritetään tämä yritys oletusarvoisesti.
3. Valitse **Valitse**. Uusi toimittaja luodaan.

## <a name="validation"></a>Tarkistus

Kun toimittaja kopioidaan, uuden toimittajan tiedot yritetään tallentaa. Tarkistusten avulla tarkistetaan, että kopioidut tiedot ovat oikein. Jos valintasääntötarkistus tuottaa virheellisen tuloksen, näkyviin tulee virheilmoitus. Virheilmoituksessa kerrotaan, mitä tietoja on päivitettävä. Toimittajan kopio tallennetaan vasta kun tarkistuksessa havaitut virheet on korjattu.

## <a name="copy-a-vendor-by-using-the-tax-exempt-number-search-feature"></a>Toimittajan kopioiminen käyttämällä verovapautusnumeron hakua

Toimittajat voi kopioida myös **Verovapausnumero**-haun avulla **Kaikki toimittajat** -sivun toimintoruudun **Toimittaja**-välilehden **Rekisteröinti**-ryhmässä. Näkyviin tulevassa **Verovapausnumeron haku** -valintaikkunassa näkyvät verovapausnumerot, toimittajatunnus, toimittajan nimi ja yritys, jossa verovapaustunnusta käytetään. Toimittaja voidaan kopioida vain, jos se on muu yritys kuin nykyinen yritys. Kun olet valinnut nämä ehdot täyttävän toimittajan, toimi seuraavasti.

1. Näkyviin tulee **Kopioi toimittaja** -vaihtoehto. Tämä vaihtoehto on oletusarvoisesti **Ei**. Voit kopioida toimittajan nykyiseen yritykseen valitsemalla **Kyllä**.
2. Valitse **Valitse**. Uusi toimittaja luodaan.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
