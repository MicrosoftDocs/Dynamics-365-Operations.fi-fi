---
title: "Kopioi toimittajat käyttämällä jaettuja numerosarjoja"
description: "Tässä ohjeaiheessa kerrotaan, miten jaettujen numerosarjojen avulla toimittaja kopioidaan toiseen yritykseen pitäen toimittajatunnus ennallaan."
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: index-page
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.1
ms.translationtype: HT
ms.sourcegitcommit: c5d4fb53939d88fcb1bd83d70bc361ed9879f298
ms.openlocfilehash: 4c27e0f75a45a2e4290ec4b6f72ee67d792449a0
ms.contentlocale: fi-fi
ms.lasthandoff: 10/01/2018

---

# <a name="copy-vendors-by-using-shared-number-sequences"></a>Kopioi toimittajat käyttämällä jaettuja numerosarjoja

[!include [banner](../includes/banner.md)]

Toimittajatunnukset voidaan määrittää jaettujen numerosarjojen avulla. Jaettujen numerosarjojen avulla voidaan kopioida toimittajia yrityksestä toiseen ja käyttää samoja toimittajatunnuksia molemmissa yrityksissä.

## <a name="setup"></a>Määritys

Toiminto on käytössä, kun toimittajatunnukset määritetään jaettujen numerosarjojen avulla. Samaa numerosarjaa on käytettävä kaikissa yrityksissä, joihin toimittaja halutaan kopioida. Toimittajan numerosarjan voi muuttaa kunkin yrityksen **Ostoreskontran parametrit** -sivulla. Valitse **Ostoreskontra** \> **Asetukset** \> **Ostoreskontran parametrit** ja **Numerosarjat**-välilehti.

Toimittajanumerosarjat voidaan määrittää jokaiselle toimittajaryhmälle. Myös nämä numerosarjat on jaettava. Toimittajaryhmän numerosarja käytetään ensin. Jos toimittajaryhmälle ei ole määritetty numerosarjaa, käytetään **Ostoreskontran parametrit** -sivulla määritettyä numerosarjaa.

Toimittajia voidaan kopioida yritysten välillä myös käytettäessä manuaalisia toimittajatunnuksia. Jos toimittaja yritetään kopioida yritykseen, jossa toimittajatunnus on jo käytössä, kopiointiprosessia ei voi käynnistää.

## <a name="copy-a-vendor"></a>Kopioi toimittaja

Toimittaja kopioidaan valitsemalla **Kaikki toimittajat** -luettelosivulla **Uusi**. **Kaikki toimittajat, uusi tietue** -sivu avautuu. Uutta toimittajatunnusta ei määritetä heti. Tämä toiminto eroaa aiemmista Microsoft Dynamics 365 for Finance and Operations -versioista. Toimittajaryhmää ei ole vielä valittu, joten järjestelmä ei voi määrittää oikeaa käytettävää numerosarjaa. Se ei voi myöskään määrittää, halutaanko luoda uusi toimittaja vai kopioida toimittaja. Siksi toimittajatunnus määritetään vasta kun valitset **Tallenna**-vaihtoehdon sivun alareunassa.

Jos luot uutta toimittajaa, voit jatkaa täyttämään kaikki kentät tavalliseen tapaan. Kun olet valmis ja valitset **Tallenna**, huomaat, että toimittajatunnus määritettiin automaattisesti. Jos käytetään manuaalisia numerosarjoja, huomaat, että käytettiin manuaalista toimittajatunnusta.

Voit kopioida toimittajan syöttämällä **Nimi**-kenttään vähintään yhden merkin, joka edustaa etsittävää toimittajaa. Hakuvalintaikkunassa näkyy luettelo, jossa etsittävä toimittaja saattaa näkyä. Kun valitset jonkun osapuolen, valintaikkunan oikealla puolella näkyy lisätietoja:

- **Yleistä**-välilehdessä näkyy osapuolen puhelinnumero ja osoite.
- Valitun osapuolen mahdolliset roolit ja yritykset näkyvät **Roolit**-välilehdessä.
- Osapuolen verotunnukset näkyvät **Verorekisteröintitunnus**-välilehdessä.

Voit kopioida osapuolen vain, jos sen rooli on toimittaja ja jos sillä on tämä rooli muussa kuin nykyisessä yrityksessä. Kun olet löytänyt nämä ehdot täyttävän osapuolen, toimi seuraavasti.

1. Näkyviin tulee **Kopioi toimittaja** -vaihtoehto. Tämä vaihtoehto on oletusarvoisesti **Ei**. Voit kopioida toimittajan nykyiseen yritykseen valitsemalla **Kyllä**. 
2.  **Yritys**-kenttä tulee näkyviin. Valitse yritys, josta toimittaja kopioidaan Jos toimittaja kuuluu vain yhteen yritykseen, kenttään määritetään tämä yritys oletusarvoisesti.
3. Valitse **Valitse**. Uusi toimittaja luodaan.

## <a name="validation"></a>Valintasäännöt

Kun toimittaja kopioidaan, järjestelmä yrittää tallentaa uuden toimittajan tiedot. Valintasääntöjen avulla tarkistetaan, että kopioidut tiedot ovat oikein. Jos valintasääntötarkistus tuottaa virheellisen tuloksen, näkyviin tulee virheilmoitus. Virheilmoituksessa kerrotaan, mitä tietoja on päivitettävä. Toimittajan kopio tallennetaan vasta kun tarkistuksessa havaitut virheet on korjattu.

## <a name="copy-a-vendor-by-using-the-tax-exempt-number-search-feature"></a>Toimittajan kopioiminen käyttämällä verovapautusnumeron hakua

Toimittajat voi kopioida myös hakemalla verovapausnumeron perusteella **Kaikki asiakkaat**-sivun **Toimittaja**-välilehden **Kaikki toimittajat** -ryhmän toimintoruudussa. Näkyviin tulevassa **Verovapausnumeron haku** -valintaikkunassa näkyvät verovapausnumerot, toimittajatunnus, toimittajan nimi ja yritys, jossa verovapaustunnusta käytetään. Toimittaja voidaan kopioida vain, jos se on muu yritys kuin nykyinen yritys. Kun olet valinnut nämä ehdot täyttävän toimittajan, toimi seuraavasti.

1. Näkyviin tulee **Kopioi toimittaja** -vaihtoehto. Tämä vaihtoehto on oletusarvoisesti **Ei**. Voit kopioida toimittajan nykyiseen yritykseen valitsemalla **Kyllä**.
2. Valitse **Valitse**. Uusi toimittaja luodaan.

