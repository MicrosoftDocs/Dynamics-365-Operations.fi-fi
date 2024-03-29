---
title: Asiakkaiden kopioiminen käyttämällä jaettuja numerosarjoja
description: Tässä artikkelissa kerrotaan, miten jaettujen numerosarjojen avulla asiakas kopioidaan toiseen yritykseen pitäen asiakastunnus ennallaan.
author: abruer
ms.date: 08/31/2018
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: CustTable
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 54639356007198f256f0d80fce9bfa2013f7b2b7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8899982"
---
# <a name="copy-customers-by-using-shared-number-sequences"></a>Asiakkaiden kopioiminen käyttämällä jaettuja numerosarjoja

[!include [banner](../includes/banner.md)]

Asiakastunnukset voidaan määrittää jaettujen numerosarjojen avulla. Jaettujen numerosarjojen avulla voidaan kopioida asiakkaita yrityksestä toiseen ja käyttää samoja asiakastunnuksia molemmissa yrityksissä.

## <a name="setup"></a>Määritys

Toiminto on käytössä, kun asiakastunnukset määritetään jaettujen numerosarjojen avulla. Samaa numerosarjaa on käytettävä kaikissa yrityksissä, joihin asiakas halutaan kopioida. Asiakkaan numerosarjan voi muuttaa kunkin yrityksen **Myyntireskontran parametrit** -sivulla. Valitse **Myyntireskontra** \> **Parametrit** ja **Numerosarjat**-välilehti.

Asiakasnumerosarjat voidaan määrittää jokaiselle asiakasryhmälle. Myös nämä numerosarjat on jaettava. Asiakasryhmän numerosarja käytetään ensin. Jos asiakasryhmälle ei ole määritetty numerosarjaa, käytetään **Myyntireskontran parametrit** -sivulla määritettyä numerosarjaa.

Asiakkaita voidaan kopioida yritysten välillä myös käytettäessä manuaalisia asiakastunnuksia. Jos asiakas yritetään kopioida yritykseen, jossa asiakastunnus on jo käytössä, kopiointiprosessia ei voi käynnistää.

## <a name="copy-a-customer"></a>Asiakkaan kopioiminen

Asiakas kopioidaan valitsemalla **Kaikki asiakkaat** -luettelosivulla **Uusi**. **Luo asiakas** -valintaikkuna avautuu. Uutta asiakastunnusta ei määritetä heti. Tämä toiminnallisuus eroaa aiempien versioiden toiminnallisuuksista. Asiakasryhmää ei ole vielä valittu, joten järjestelmä ei voi määrittää oikeaa käytettävää numerosarjaa. Se ei voi myöskään määrittää, halutaanko luoda uusi asiakas vai kopioida asiakas. Siksi asiakastunnus määritetään vasta kun valitset **Tallenna**-vaihtoehdon valintaikkunan alareunassa.

Jos luot uutta asiakasta, voit jatkaa täyttämään kaikki kentät tavalliseen tapaan. Kun olet valmis ja valitset **Tallenna**, huomaat, että asiakastunnus määritettiin automaattisesti. Jos käytetään manuaalisia numerosarjoja, huomaat, että käytettiin manuaalista asiakastunnusta.

Voit kopioida asiakkaan syöttämällä **Nimi**-kenttään vähintään yhden merkin, joka edustaa etsittävää asiakasta. Hakuvalintaikkunassa näkyy luettelo, jossa etsittävä asiakas saattaa näkyä. Kun valitset jonkun osapuolen, valintaikkunan oikealla puolella näkyy lisätietoja:

- **Yleistä**-välilehdessä näkyy osapuolen puhelinnumero ja osoite.
- Valitun osapuolen mahdolliset roolit ja yritykset näkyvät **Roolit**-välilehdessä.
- Osapuolen verotunnukset näkyvät **Verorekisteröintitunnus**-välilehdessä.

Voit kopioida osapuolen vain, jos sen rooli on asiakas ja jos sillä on tämä rooli muussa kuin nykyisessä yrityksessä. Kun olet löytänyt nämä ehdot täyttävän osapuolen, toimi seuraavasti.

1. Näkyviin tulee **Kopioi asiakas** -vaihtoehto. Tämä vaihtoehto on oletusarvoisesti **Ei**. Voit kopioida asiakkaan nykyiseen yritykseen valitsemalla **Kyllä**. 
2. **Yritys**-kenttä tulee näkyviin. Valitse yritys, josta asiakas kopioidaan Jos asiakas kuuluu vain yhteen yritykseen, kenttään määritetään tämä yritys oletusarvoisesti.
3. Valitse **Valitse**. Uusi asiakas luodaan.

## <a name="validation"></a>Valintasäännöt

Kun asiakas kopioidaan, järjestelmä yrittää tallentaa uuden asiakkaan tiedot. Valintasääntöjen avulla tarkistetaan, että kopioidut tiedot ovat oikein. Jos valintasääntötarkistus tuottaa virheellisen tuloksen, näkyviin tulee virheilmoitus. Virheilmoituksessa kerrotaan, mitä tietoja on päivitettävä. Asiakkaan kopio tallennetaan vasta kun tarkistuksessa havaitut virheet on korjattu.

## <a name="copy-a-customer-by-using-tax-exempt-number-search-feature"></a>Asiakkaan kopioiminen käyttämällä verovapausnumeron hakua

Asiakkaat voi kopioida myös hakemalla verovapausnumeron perusteella **Kaikki asiakkaat**-sivun **Asiakas**-välilehden **Rekisteröinti**-ryhmän toimintoruudussa. Näkyviin tulevassa **Verovapausnumeron haku** -valintaikkunassa näkyvät verovapausnumerot, asiakastunnus, asiakkaan nimi ja yritys, jossa verovapaustunnusta käytetään. Asiakas voidaan kopioida vain, jos se on muu yritys kuin nykyinen yritys. Kun olet valinnut nämä ehdot täyttävän asiakkaan, toimi seuraavasti.

1. Näkyviin tulee **Kopioi asiakas** -vaihtoehto. Tämä vaihtoehto on oletusarvoisesti **Ei**. Voit kopioida asiakkaan nykyiseen yritykseen valitsemalla **Kyllä**. 
2. Valitse **Valitse**. Uusi asiakas luodaan.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
