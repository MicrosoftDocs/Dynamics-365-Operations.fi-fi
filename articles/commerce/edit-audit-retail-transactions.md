---
title: Vähittäismyyntitapahtumien muokkaaminen ja valvominen
description: Tässä ohjeaiheessa kerrotaan myymälätapahtumien muokkaus- ja valvontatoiminnoista.
author: josaw1
manager: AnnBe
ms.date: 10/14/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-29
ms.dyn365.ops.version: ''
ms.openlocfilehash: 97211ee36dbaa704d3a967e9b742ff1cae708707
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004386"
---
# <a name="edit-and-audit-retail-store-transactions"></a>Vähittäismyyntitapahtumien muokkaaminen ja valvominen

[!include [banner](includes/banner.md)]



Dynamics 365 Commerce -sovelluksen asiakkaat käyttävät sekä ensimmäisen että kolmannen osapuolen myyntipistesovelluksia. Ensimmäisen osapuolen myyntipistesovelluksen kanssa myymälätapahtumat noudetaan kanavista Headquarters-sovellukseen eräprosessin kautta. Kolmannen osapuolen sovellusten kanssa tapahtumat noudetaan Headquarters-sovellukseen integroinnin kautta. Molemmissa tapauksissa suoritetaan yhdenmukaisuustarkistus sen jälkeen, kun tapahtumat on noudettu Headquarters-sovellukseen. Prosessissa tapahtumille suoritetaan useita tarkistuksia, jotta vain tarkistetut tapahtumat noudetaan Headquarters-sovellukseen kirjattavaan laskelmaan. 

Kauppatapahtumien tarkistus voi epäonnistua useista eri syistä. Esimerkiksi integrointikoodin tai myyntipistesovelluksen virhe saattaa aiheuttaa epäyhtenäisiä tietoja. Myös käyttäjän virhe, kuten tuotteen poistaminen kanavaan synkronoimisen jälkeen tai tilikauden sulkeminen ilman kyseisen kauden tapahtumien kirjaamista voi aiheuttaa epäyhtenäisiä tietoja.

Kun nämä tapahtumat merkitään ja suljetaan pois laskelmista, tapahtumat voivat keskeyttää asiakkaan päivittäisen myynnin kirjausprosessin myyntitietoihin.

Commerce-sovelluksessa voit muokata tiettyjä tapahtumia, joiden tarkistus on epäonnistunut kaikkien muutosten valvonnan ylläpidon yhteydessä. 

## <a name="edit-and-audit-transactions"></a>Tapahtumien muokkaaminen ja valvominen

Retail-sovelluksen versiossa 10.0.5 voi muokata vain itsepalvelutukkutapahtumia, kuten myyntiä ja palautuksia. Asiakas- ja online-tilausten muokkaamista ei tueta. Retail-sovelluksen versiossa 10.0.6 ja uudemmissa versioissa tuetaan myös käteisvarojen hallintatapahtumien muokkaamista.

1. Asenna Dynamics Excel -lisäosa.

2. Siirry **Myymälän myyntitiedot** -työtilaan. **Tapahtuman tarkistusvirheet** -ruudussa on sen tapahtumalomakkeen esisuodatettu näkymä, jonka yksi tai usea tarkistussääntö on epäonnistunut.
 
3. Avaa lomake. Valitse tietue, jonka tarkistus epäonnistui. Valitse **Office-lisäosa** ja valitse sitten **Muokkaa valittua tapahtumaa**. Näkyviin tulevat valitun tapahtuman tiedot sisältävä Excel-tiedosto ja seuraavat laskentataulukot:

    - Rivit: Tässä laskentataulukossa ovat tapahtuman otsikko- ja tuoterivit sekä niihin liittyvät tiedot.
    - Maksut: Tässä laskentataulukossa ovat tapahtuman maksurivien tiedot.
    - Alennukset: Tässä laskentataulukossa ovat tapahtuman alennukseen liittyvät tiedot.
    - Verot: Tässä laskentataulukossa ovat tapahtuman veroihin liittyvät tiedot.
    - Kulut: Tässä laskentataulukossa ovat tapahtuman kuluihin liittyvät tiedot.

4. Excel-tiedostossa muokataan soveltuvia kenttiä. Tämän jälkeen tiedot ladataan takaisin Headquarters-sovellukseen Dynamics Excel -lisäosan julkaisutoiminnon avulla. Kun muutokset on julkaistu, ne näkyvät järjestelmässä. Julkaisemisen aikana käyttäjien tekemiä muutoksia ei tarkisteta.

5. Voit tarkastella muutosten täydellistä kirjausketjua valitsemalla otsikkotason muutoksille **Näytä kirjausketju** -kohdan **Vähittäismyyntitapahtuma**-otsikossa soveltuvan tapahtumasivun osassa ja tietueessa. Esimerkiksi kaikki myyntiriviin liittyvät muutokset näkyvät **Myyntitapahtumat**-sivulla ja maksuihin liittyvät muutokset näkyvät **Maksutapahtumat**-sivulla. Seuraavassa esitellään muutosten valvontaan liittyvät tiedot.

   - Muokkauksen päivämäärä ja aika
   - Kenttä 
   - Vanha arvo
   - Uusi arvo
   - Muokannut

6. Suorita muutosten tekemisen ja julkaisemisen jälkeen **Tarkista myymälän tapahtumat** -vaihtoehto uudelleen ja tarkista, että tehdyt muutokset ovat yhdenmukaisia ja sallittuja.

> [!NOTE]
> Voit muokata vain tapahtumia, joiden tarkistus epäonnistui. Jos haluat muokata tarkistuksen läpäisseitä tapahtumia, muuta muutettavan tapahtuman tarkistuksen tilaksi **Virhe** tai **Ei mitään**. Tämän jälkeen voit muokata sitä. 


## <a name="bulk-edit-transactions"></a>Tapahtumien joukkomuokkaus

Retail-sovelluksen versio 10.0.6 ja uudemmat versiot tukevat laskelmatason tapahtumien joukkomuokkausta. 

1. Avaa muokattavat tapahtumat sisältävä laskelma Excel-lisäosan avulla käyttämällä yllä mainittuja vaiheita 1–3.

2. Valitse jokin alla olevista vaihtoehdoista.

    - **Muokkaa itsepalvelutukkutapahtumia**. Tämän vaihtoehdon avulla voit muokata kaikkia laskelman itsepalvelutukkutapahtumia. Seuraavat Excel-laskentataulukot ovat käytettävissä.
    
       - **Tapahtuma**: Tässä laskentataulukossa ovat kaikki myyntitapahtumien otsikkotason tiedot.
       - **Myyntitapahtuma**: Tässä laskentataulukossa ovat kaikki myyntitapahtumien rivitason tiedot.
       - **Maksutapahtumat**: Tässä laskentataulukossa ovat kaikki myyntitapahtumien maksurivien tiedot.
       - **Alennustapahtumat**: Tässä laskentataulukossa ovat kaikki myyntitapahtumien alennusrivien tiedot.
       - **Verotapahtumat**: Tässä laskentataulukossa ovat kaikki myyntitapahtumien verorivien tiedot.
       - **Kulutapahtumat**: Tässä laskentataulukossa ovat kaikki myyntitapahtumien kulurivien tiedot.

    - **Käteisvarojen hallintatapahtumien muokkaus**. Tämän vaihtoehdon avulla voit muokata kaikkia laskelman käteisvarojen hallintatapahtumia. Seuraavat Excel-laskentataulukot ovat käytettävissä.
     
       - **Tapahtuma**: Tässä laskentataulukossa ovat kaikki käteisvarojen hallintatapahtumien otsikkotason tiedot.
       - **Pankin maksuvälinetapahtumat**: Tässä laskentataulukossa ovat kaikki tiedot pankkiin toimituksesta.
       - **Kassakaapin maksuvälinetapahtumat**: Tässä laskentataulukossa ovat kaikki tiedot kassakaappiin toimituksesta.
       - **Kassan laskeminen maksuvälineittäin**: Tässä laskentataulukossa ovat kaikki tiedot tapahtumasta, jossa lasketaan kassa maksuvälineittäin.
       - **Tulo-/kulutapahtumat**: Tässä laskentataulukossa on kaikki tulo-/kulutapahtumarivin tiedot.
       - **Maksutapahtumat**: Tässä laskentataulukossa ovat kaikki **Maksa lasku** -toiminnon sekä tulo-/kulutapahtuman maksuun liittyvät tiedot.

3.  Tarkistuksia ei suoriteta joukkomuokattujen tapahtumien julkaisemisen yhteydessä. Sinun on varmistettava, että kaikki muokkaukset on tehty oikein ja että laskentataulukoiden tietojen tarkkuus säilyy. Jos esimerkiksi haluat muuttaa tapahtuman päivämäärää skenaarioiden hallinnan yhteydessä, kun avointen tapahtumien tili- tai varastokausi on suljettu, sinun on muutettava kaikkien niiden Excel-laskentataulukoiden päivämääriä, joissa on **Liiketoiminnan päivämäärä** -sarake. Voit tarkistaa tapahtumat niiden muokkaamisen jälkeen **Laskelmat**-sivun **Tarkista tapahtumat uudelleen** -vaihtoehdon avulla.
