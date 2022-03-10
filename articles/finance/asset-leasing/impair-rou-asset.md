---
title: Käyttöoikeusomaisuuserän arvon alentaminen
description: Tässä ohjeaiheessa kuvataan toiminto, joka tallentaa arvonalentumisen ja muuttaa ASC 842:n mukaista resurssin poistoaikataulua käyttöleasingsopimuksessa.
author: moaamer
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: b104cec399a368ada64a73688c42476e6fbd9e52
ms.sourcegitcommit: 304a482dfcc31dcb61849f710ae73432324ddef3
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/29/2021
ms.locfileid: "7947337"
---
# <a name="impair-right-of-use-assets"></a>Käyttöoikeusomaisuuserän arvon alentaminen

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Jos käyttöoikeusomaisuuserän kirjanpitosumma ei ole palautettavissa, käyttäjän on ehkä testattava, onko resurssin arvoa alennettu. Jos resurssin arvoa on alennettu, resurssin vuokraus ei voi tallentaa arvonalenemista ja oikaista poistoaikataulua vastaavasti. Tässä ohjeaiheessa kuvataan toiminto, joka tallentaa arvonalentumisen ja muuttaa ASC 842:n mukaista poistoaikataulua käyttöleasingsopimuksessa. Sama menetelmä koskee myös IFRS 16 -vuokrasopimuksia.

Jäljellä oleva käyttöoikeusomaisuuserän saldo kuoletetaan jäljellä olevien kausien määrän perusteella tasaisesti siitä huolimatta, onko vuokrasopimus luokitelty rahoitusleasingsopimukseksi IFRS 16:n avulla vai käyttöleasingsopimukseksi ASC 842:n avulla.

## <a name="impair-an-rou-asset"></a>Käyttöoikeusomaisuuserän arvonalentaminen

1. Jos haluat siirtyä vuokrasopimukseen, jonka arvoa on alennettu, siirry kohtaan **Kirjat**.
2. Valitse toimintoruudussa **Arvonalennus**.
3. Syötä näyttöön tulevan valintaikkunan **Arvonalennussumma**-kenttään resurssin arvonalennuksen summa. Jos haluat pienentää käyttöoikeusomaisuuserää, anna positiivinen arvo.
4. Anna **Tapahtumapäivämäärä**-kenttään päivämäärä, jona arvonalennusviennin kirjaus tulisi tehdä.
5. Anna **Jäljellä olevat kaudet** -kenttään jäljellä olevien kuoletettavien kuukausien määrä.
6. Määritä **Esikatselu**-vaihtoehto nähdäksesi ehdotetun omaisuuserän saldon ja rahoitusmerkinnän ennen niiden luomista tai kirjaamista.
7. Määritä **Sulje kirja** -asetuksen arvoksi **Kyllä**, jos haluat sulkea vuokrauskirjan. Voit peruuttaa tämän toiminnon käyttämällä **Avaa vuokra uudelleen** -tilaa. Vientejä ei voi kirjata suljettuihin vuokrasopimuksiin, eikä suljettuja vuokrasopimuksia voi oikaista. 
8. Luo tai kirjaa arvonalennusvienti valitsemalla **Kirjaa**.

    > [!NOTE]
    > Sen jälkeen, kun tapahtuma on kirjattu, luodaan uusi kirjaversio.

    > Jos vuokra luokitellaan käyttövuokraksi, kuukausittainen poisto arvonalennuksen jälkeen lasketaan tasapoistomenetelmällä.

9. Voit tarkastella sitä resurssin poistoaikataulua, jonka arvoa on alennettu, ja avata vuokrauskirjan resurssin poistoaikataulun. Käyttöomaisuus poistetaan nyt **Kausia jäljellä** -kentään syötettyjen kuukausien määrän perusteella tasaisesti.
10. Voit tarkastella kulukirjauskansiovientiä, jonka arvoa alennettiin, valitsemalla **Käyttöomaisuuserän leasingkirjauskansio** arvonalennuksen vuokrauskirjan toimintoruudussa. Järjestelmä luo kirjauskansioviennin, joka veloittaa arvonalennuksen kulukirjauksen tiliä ja hyvittää vuokrauksen resurssin tiliä. 
11. Jos haluat tarkastella käyttöoikeusomaisuuserän kirjanpitoarvoa, valitse **Käyttöomaisuustapahtumat** vuokrauskirjan toimintoruudussa.

## <a name="example-of-rou-asset-impairment"></a>Käyttöoikeusomaisuuserän arvonalennuksen esimerkki

Tässä esimerkissä vuokrasopimus on ei-erikoistunut resurssi, joka ei siirrä omistajuutta tai myönnä vuokralle ottajalle osto-oikeutta.

### <a name="setup"></a>Luo perustiedot

Seuraavissa taulukoissa ovat arvot, jotka on määritetty **Yleistiedot**- ja **Maksuaikataulun rivit** -välilehdille vuokrasopimuksessa, jota käytetään tässä esimerkeissä.

**Yleinen-välilehti**

| Kenttä                      | Arvo            |
|----------------------------|------------------|
| Resurssin käypä arvo    | 600,000          |
| Inkrementaalinen lainakorko | 7 %               |
| Yhdistämisväli       | Vuosittain         |
| Käyttöomaisuuden käyttöikä (kuukautta) | 600              |
| Annuiteetin tyyppi               | Tavallinen annuiteetti |
| Aloituspäivämäärä          | 1.1.2019       |

**Maksusuunnitelmarivit-välilehti**

| Kenttä             | Arvo      |
|-------------------|------------|
| Aloituspäivä        | 1.1.2019   |
| Kausiväli   | Kuukausittain    |
| Kaudet           | 120        |
| Päättymispäivämäärä          | 31.12.2028 |
| Maksun toistuvuus | Vuosittain   |
| Maksun summa    | 10,000     |

### <a name="steps"></a>Vaiheet

1. Kun olet luonut vuokrasopimuksen aiemmin tässä ohjeaiheessa kuvatulla tavalla, siirry vuokrauskirjaan ja vahvista maksuaikataulu. Kirjaa sitten alkuperäinen tuloutuksen kirjauskansiovienti. ALkuperäisen käyttöoikeusomaisuuserän ja vuokrasopimusvelan on oltava 70 235,81 $. Tässä esimerkissä vuokrasopimus luokiteltiin käyttöleasingsopimukseksi ASC 842:n mukaan.
2. Suorita kirjauskansion eräprosessi kolme kertaa, jotta voit simuloida kolmen vuoden kulumista vuokrille, korkokuluille ja poistokuluille.
3. Kun kaikki kolme erätyötä on suoritettu, siirry takaisin vuokrauskirjaan ja avaa velka- ja resurssitapahtumien taulukot tarkastellaksesi resurssin ja vuokrasopimusvelan nykyistä kirjanpitoarvoa. Kolmen vuoden kuluttua velan arvon on oltava noin -53 893,00 dollaria ja resurssin arvon noin 53 893,00 dollaria. 

    Kolmen vuoden jälkeen yritys tekee arvonalentumisen testit ja määrittää, että käyttöoikeusomaisuuserän arvonalennus on 35 000 dollaria. Tämä arvonalennus on nyt tallennettava.
    
4. Siirry vuokrauskirjaan ja valitse toimintoruudussa **Arvonalennus**.
5. Syötä **Arvonalennusparametri**-sivulla seuraavat tiedot.

    | Kenttä                  | Arvo    |
    |------------------------|----------|
    | Arvonalennuksen summa      | 35,000   |
    | Tapahtuman päivämäärä       | 1.1.2022 |
    | Kausia jäljellä      | 84       |
    | Kirjaa                   | Kyllä      |
    | Esikatsele ennen kirjausta | Ei       |
    | Sulje kirja             | Ei       |

6. Arvonalentumisen kulukirjauskansiovienti on luotu ja kirjattu. Voit tarkastella sitä siirtymällä resurssin leasingkirjauskansioon vuokrauskirjassa. Huomaa, että arvonalennuksen summa on veloitettu arvonalennuksen kulukirjaustililtä ja käyttöoikeusomaisuuserän kirjaustiliä on hyvitetty.

7. Voit tarkastella arvonalennuksen nettovaikutusta siirtymällä velka- ja resurssitapahtumien taulukoihin. Huomaa, että arvonalennuksen kulu on vähentänyt käyttöoikeusomaisuuserää, mutta vuokrasopimusvelan kirjanpitosumma ei ole muuttunut.

Arvonalennuksella on toinen vaikutus, joka tulee ottaa huomioon. Koska käyttöoikeusomaisuuserän summa on nyt pienempi kuin vuokrasopimusvelka, summa on vähennettävä eri tavalla kuin ennen. Resurssi on nyt vähennetty tasapoistomenetelmällä kaikista vuokrasopimuksen jäljellä olevista 84 kuukaudesta tapahtumapäivämäärästä alkaen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
