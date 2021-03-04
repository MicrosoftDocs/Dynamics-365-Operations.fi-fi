---
title: Kassanhallinnan ja itsepalvelutukun hallintatapahtumien muokkaaminen ja tarkastaminen
description: Tässä aiheessa kerrotaan, miten kassanhallinnan ja itsepalvelutukun hallintatapahtumia muokataan ja tarkistetaan Microsoft Dynamics 365 Commercessa.
author: josaw1
manager: AnnBe
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: c809f379dbd6824542d0b1768cfbf44f37461f4c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010196"
---
# <a name="edit-and-audit-cash-and-carry-and-cash-management-transactions"></a>Kassanhallinnan ja itsepalvelutukun hallintatapahtumien muokkaaminen ja tarkastaminen

[!include [banner](../includes/banner.md)]

Tässä aiheessa kerrotaan, miten kassanhallinnan ja itsepalvelutukun hallintatapahtumia muokataan ja tarkistetaan Microsoft Dynamics 365 Commercessa.

## <a name="overview"></a>Yleiskatsaus

Dynamics 365 Commerce -sovelluksen asiakkaat käyttävät sekä ensimmäisen että kolmannen osapuolen myyntipistesovelluksia. Ensimmäisen osapuolen myyntipistesovelluksessa myymälätapahtumat noudetaan kanavista Commercen pääkonttorisovellukseen eräprosessin kautta. Kolmannen osapuolen sovellusten kanssa tapahtumat noudetaan Commercen pääkonttorisovellukseen integroinnin kautta. Molemmissa tapauksissa on suoritettava yhdenmukaisuustarkistusprosessi tapahtumien siirryttyä Commercen pääkonttorisovellukseen. Tämä prosessi suorittaa tapahtumalle useita tarkistuksia. Vain tapahtumat, joiden tarkistus onnistuu, noudetaan laskelmaan Commercen pääkonttorisovellukseen kirjaamista varten.

Commerce-tapahtumien tarkistus voi epäonnistua useista eri syistä. Integrointikoodin tai myyntipistesovelluksen virhe voi aiheuttaa ei-yhdenmukaisia tietoja. Myös käyttäjän virhe voi aiheuttaa ei-yhdenmukaisia tietoja. Käyttäjä voi esimerkiksi poistaa tuotteen sen jälkeen, kun tuote on synkronoitu kanavaan, tai sulkea tilikauden ilman kyseisen kauden tapahtumien kirjaamista. Vaikka nämä tapahtumat merkitään ja suljetaan pois laskelmista, ne voivat keskeyttää asiakkaan päivittäisen myynnin kirjausprosessin myyntitietoihin. Commerce-sovelluksessa voit muokata tapahtumia, joiden tarkistus on epäonnistunut, samalla kun ylläpidät kaikkien muutosten valvontaa.

## <a name="edit-transactions"></a>Muokkaa tapahtumia

Commerce-sovelluksen versiossa 10.0.5 voi muokata vain itsepalvelutukkutapahtumia, kuten myyntiä ja palautuksia. Asiakastilauksia ja online-tilauksia ei voi muokata. Commerce-sovelluksen versiossa 10.0.6 ja uudemmissa versioissa myös kassanhallintatapahtumia voi muokata.

Voit muokata Commerce-pääkonttorisovelluksen tapahtumia seuraamalla alla olevia ohjeita.

1. Asenna [Microsoft Dynamics Office Add-in](https://appsource.microsoft.com/product/office/WA104379629?tab=Overview).
1. Avaa Commerce-pääkonttorisovelluksessa **Myymälän taloustiedot** -työtila. **Tapahtuman tarkistusvirheet** -ruudussa on sen tapahtumasivun esisuodatettu näkymä, jonka yksi tai usea tarkistussääntö on epäonnistunut.
1. Avaa tapahtumasivu ja valitse tietue, jonka tarkistus epäonnistui. Valitse **Office Add-in** ja valitse sitten **Muokkaa valittua tapahtumaa**. Valitun tapahtuman tiedot sisältävä Excel-tiedosto avataan. Tämä tiedosto sisältää seuraavat laskentataulukot:

    - **Rivit**: Tässä laskentataulukossa ovat tapahtuman otsikko- ja tuoterivit sekä niihin liittyvät tiedot.
    - **Maksut** – Tässä laskentataulukossa ovat tapahtuman maksurivien tiedot.
    - **Alennukset** – Tässä laskentataulukossa ovat tapahtuman alennukseen liittyvät tiedot.
    - **Verot** –Tässä laskentataulukossa ovat tapahtuman veroihin liittyvät tiedot.
    - **Kulut** – Tässä laskentataulukossa ovat tapahtuman kuluihin liittyvät tiedot.

1. Excel-tiedostossa muokataan soveltuvia kenttiä. Tämän jälkeen tiedot ladataan takaisin Commerce-pääkonttorisovellukseen Dynamics Excel -lisäosan julkaisutoiminnon avulla. Kun tiedot on julkaistu, ne näkyvät järjestelmässä. Julkaisemisen aikana käyttäjien tekemiä muutoksia ei tarkisteta.
1. Voit tarkastella muutosten täydellistä kirjausketjua valitsemalla otsikkotason muutoksille **Näytä kirjausketju** -kohdan **Vähittäismyyntitapahtuma**-otsikossa soveltuvan tapahtumasivun osassa ja tietueessa. Esimerkiksi kaikki myyntiriveihin liittyvät muutokset näkyvät **Myyntitapahtumat**-sivulla ja maksuihin liittyvät muutokset **Maksutapahtumat**-sivulla. Seuraavia tarkistustietoja muutetaan:

    - Muokkauksen päivämäärä ja aika
    - Kenttä
    - Vanha arvo
    - Uusi arvo
    - Muokannut

1. Suorita muutosten tekemisen ja julkaisemisen jälkeen **Tarkista myymälän tapahtumat** uudelleen ja tarkista, että tehdyt muutokset ovat yhdenmukaisia ja sallittuja.

> [!NOTE]
> Voit muokata vain tapahtumia, joiden tarkistus epäonnistui. Jos haluat muokata tarkistuksen läpäissyttä tapahtumaa, muuta muutettavan tapahtuman tarkistuksen tilaksi **Virhe** tai **Ei mitään** ja julkaise muutos. Tämän jälkeen voit muokata otsikon tai tapahtuman muun alitietueen tietoja ja julkaista otsikon tai tietueet.

## <a name="bulk-edit-transactions-that-are-linked-to-a-statement"></a>Laskelmaan linkitettyjen tapahtumien joukkomuokkaus

Commerce-sovelluksen versio 10.0.6 ja uudemmat versiot tukevat laskelmatason tapahtumien joukkomuokkausta.

Voit joukkomuokata laskelmaan Commerce-pääkonttorisovelluksessa linkitettyjä tapahtumia alla olevien ohjeiden avulla.

1. Avaa **Laskelmat**-sivu ja valitse laskelma, joka sisältää muokattavat tapahtumat.
1. Valitse **Avaa Microsoft Officessa** -painike.
1. Valitse jokin seuraavista vaihtoehdoista sen mukaan, mitä muokataan:

    - **Muokkaa itsepalvelutukkutapahtumia** – Tämän vaihtoehdon avulla voit muokata kaikkia laskelmaan sisältyviä itsepalvelutukkutapahtumia. Seuraavat Excel-laskentataulukot ovat käytettävissä:

        - **Tapahtuma** – Tässä laskentataulukossa ovat kaikki myyntitapahtumien otsikkotason tiedot.
        - **Myyntitapahtuma** – Tässä laskentataulukossa ovat kaikki myyntitapahtumien rivitason tiedot.
        - **Maksutapahtumat** – Tässä laskentataulukossa ovat kaikki myyntitapahtumien maksurivien tiedot.
        - **Alennustapahtumat** – Tässä laskentataulukossa ovat kaikki myyntitapahtumien alennusrivien tiedot.
        - **Verotapahtumat** – Tässä laskentataulukossa ovat kaikki myyntitapahtumien verorivien tiedot.
        - **Kulutapahtumat** – Tässä laskentataulukossa ovat kaikki myyntitapahtumien kulurivien tiedot.

    - **Muokkaa kassanhallinnan tapahtumia** – Tämän vaihtoehdon avulla voit muokata kaikkia laskelmaan sisältyviä kassanhallinnan tapahtumia. Seuraavat Excel-laskentataulukot ovat käytettävissä:

        - **Tapahtuma** – Tässä laskentataulukossa ovat kaikki kassanhallintatapahtumien otsikkotason tiedot.
        - **Pankin maksuvälinetapahtumat** – Tässä laskentataulukossa ovat kaikki tiedot pankkiin toimituksesta.
        - **Kassakaapin maksuvälinetapahtumat** – Tässä laskentataulukossa ovat kaikki tiedot kassakaappiin toimituksesta.
        - **Kassan laskeminen maksuvälineittäin** – Tässä laskentataulukossa ovat kaikki tiedot tapahtumasta, jossa lasketaan kassa maksuvälineittäin.
        - **Tulo-/kulutapahtumat** – Tässä laskentataulukossa on kaikki tulo-/kulutapahtumarivin tiedot.
        - **Maksutapahtumat** – Tässä laskentataulukossa ovat kaikki **Maksa lasku** -toimintoon ja tulo-/kulutapahtuman maksuun liittyvät tiedot.

1. Muokkaa tarvittavia tapahtumia.

    > [!NOTE]
    > Tarkistuksia ei tehdä joukkomuokattujen tapahtumien julkaisemisen yhteydessä. Varmista, että kaikki muokkaukset on tehty oikein ja että laskentataulukoiden tietojen tarkkuus säilyy. Jos esimerkiksi haluat muuttaa tapahtuman päivämäärää skenaarioiden hallinnan yhteydessä, kun avointen tapahtumien tili- tai varastokausi on suljettu, sinun on muutettava kaikkien niiden Excel-laskentataulukoiden päivämääriä, joissa on **Liiketoiminnan päivämäärä** -sarake. Voit tarkistaa tapahtumat niiden muokkaamisen jälkeen valitsemalla **Laskelmat**-sivun **Tarkista tapahtumat uudelleen** -vaihtoehdon. Odota, että tarkistustyö päättyy, ennen kuin kirjaat laskelman.

1. Jos kooste on jo luotu, avaa **Kootut tapahtumat** -sivu ja valitse **Luo myyntitilauksen xml uudelleen**.

## <a name="bulk-edit-transactions-that-arent-linked-to-a-statement"></a>NIiden tapahtumien joukkomuokkaus, joita ei ole liitetty laskelmaan

Commerce-sovelluksen versio 10.0.10 ja sitä uudemmat versiot tukevat niiden tapahtumien joukkomuokkausta, jotka epäonnistuvat tarkistuksessa ja joita ei ole linkitetty laskelmaan.

Voit joukkomuokata niitä tapahtumia, joita ei ole linkitetty laskelmaan Commerce-pääkonttorisovelluksessa, alla olevien ohjeiden avulla.

1. Avaa **Kaikki myymälät** -sivu ja valitse myymälä, jonka tapahtumia on muokattava.
1. Valitse **Avaa Microsoft Officessa** -painike ja valitse sitten **Muokkaa itsepalvelutukkutapahtumia**.
1. Muokkaa vaadittuja tapahtumia ja julkaise ne.

## <a name="additional-resources"></a>Lisäresurssit

[Online-tilauksen ja asynkronisten asiakastilausten tapahtumien muokkaaminen ja tarkistaminen](edit-order-trans.md)

[Vähittäismyyntitapahtumien taloushallinnon dimensioiden muokkaaminen](edit-financial-dim.md)

[Excel-työkirjan luominen vähittäismyyntitapahtumien muokkaamista varten](create-excel-edit.md)

[Kenttien lisääminen Excel-työkirjaan vähittäismyyntitapahtumien muokkaamista varten](add-fields-excel.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]