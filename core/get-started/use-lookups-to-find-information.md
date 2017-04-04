---
title: Tietoja hakujen avulla.
description: "Microsoft Dynamics-365 operaatioille monta kentissä on hakuja, jotka auttavat sinua löytämään oikean tai haluttu arvo. Useita parannuksia on lisätty hakuja, tehdä näitä ohjausobjekteja voi käyttää enemmän ja tehdä käyttäjien tuottavuutta. Tässä ohjeaiheessa tutustutaan ominaisuuksista haku ja tulee joitakin hyödyllisiä vinkkejä, kuinka optimaalisesti hakujen ulkopuolella järjestelmän."
author: jasongre
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 269934
ms.assetid: f20cbd2c-14e0-47e7-b351-8e60d3537f96
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4bb647cfd3f012efbffa93a81462c538a24ac850
ms.openlocfilehash: 6a25593632575dcd71fa4a3c9cf5b83c9f8ecd39
ms.lasthandoff: 03/31/2017


---

# <a name="use-lookups-to-find-information"></a>Tietoja hakujen avulla.

Microsoft Dynamics-365 operaatioille monta kentissä on hakuja, jotka auttavat sinua löytämään oikean tai haluttu arvo. Useita parannuksia on lisätty hakuja, tehdä näitä ohjausobjekteja voi käyttää enemmän ja tehdä käyttäjien tuottavuutta. Tässä ohjeaiheessa tutustutaan ominaisuuksista haku ja tulee joitakin hyödyllisiä vinkkejä, kuinka optimaalisesti hakujen ulkopuolella järjestelmän.  

<a name="responsive-lookups"></a>Vastaa haut
------------------

Dynamics 365 toimintoja, kun haku ohjausobjektin käsitellyt aiemmissa versioissa käyttäjä on toteutettava nimenomaisen toiminnon avattavasta valikosta Avaa. Tämä on saattanut kirjoittamalla tähden (\*) napsauttamalla avattavan painikkeen ohjausobjektin Suodatinhaku-ohjausobjektin nykyisen arvon perusteella, tai käyttämällä **Alt**+**alaspäin osoittavaa nuolta** pikanäppäin. Komponenttien valinta on muutettu tehokkaimman nykyisen web-käytäntöjä seuraavilla tavoilla:

-   Haku-pudotusvalikoista nyt Avaa automaattisesti jälkeen hieman keskeyttää kirjoittamisen, avattavasta-valikosta sisältö suodatetaan haku-ohjausobjektin arvo.
    -   Huomaa, että vanha ongelma automaattinen avattavan valikon avaamisen jälkeen kirjoittamalla tähden (\*) on vähentynyt.
-   Kun haku-pudotusvalikosta on avattu, tapahtuu seuraavaa:
    -   Kohdistin jää valintaohjausobjekti (sen sijaan, että ne avattavasta valikosta siirtämällä kohdistin) niin voit tehdä muutoksia ohjausobjektin arvo. Kuitenkin, käyttäjä voi silti käyttää **ylös** ja **nuoli alas** muuttaa rivien avattavasta valikosta ja Syötä nykyisen rivin Valitse avattavasta valikosta.
    -   Kun muutokset on tehty haku-ohjausobjektin arvo muuttaa avattavan valikon sisällön.

Otetaan esimerkiksi kutsua hakukentän **Kaupunki**. 

Kun kohdistus on **Kaupunki** kenttä, voit aloittaa etsiä kaupungin, jonka haluat kirjoittamalla muutaman kirjaimen, kuten "col".  Kun lopetat kirjoittamisen, haku avautuu automaattisesti, suodatetaan ne kaupungit, jotka alkavat "col". 

[![typeaheadLookupExample](./media/typeaheadlookupexample.png)](./media/typeaheadlookupexample.png) 

Tässä vaiheessa kohdistin on edelleen hakukentän. Jos jatkat kirjoittamista, joten arvo on "sarakkeita", haku sisällön muuttuvat automaattisesti vastaamaan uusinta-ohjausobjektin arvon. 

![updateFilterLookupExample](./media/updatefilterlookupexample.png) 

Vaikka yhä haku ohjausobjektissa on kohdistus, voit käyttää myös **ylös** tai **nuoli alas** näppäimet Korosta rivi, jonka haluat valita. Jos painat **Enter** korostettu rivi merkitään valituksi hausta ja ohjausobjektin arvo päivitetään. 

![changingSelectionLookup](./media/changingselectionlookup.png)

## <a name="typing-in-more-than-ids"></a>Kirjoittanut yli tunnukset
Kun kirjoitat tietoja, on luonnollista yrittää kohde, kuten asiakkaan tai toimittajan osalta nimen sijasta kohteen tunnus tunnistaa käyttäjät. Nykyisessä versiossa Dynamics 365 toimintoja, monet (mutta ei kaikkien) hakuja nyt Tilannekohtaisten tietojen syöttö on sallittu. Tämä tehokas ominaisuus käyttäjä kirjoittaa haun ohjausobjektin tunnus tai vastaava nimi. 

Oletetaan, **asiakastili** kenttä, kun luot myyntitilauksen. Tässä kentässä näkyy **Tilitunnus**, asiakas, mutta käyttäjä yleensä mieluummin Anna **tilin nimi** sijaan **tilin tunnus** tähän kenttään, kun luot myyntitilauksen, kuten "Toimialuepuuryhmän Wholesales" sijasta "US-003."

Jos käyttäjä syöttää **Account ID** haku ohjausobjektiin avattavasta valikosta automaattisesti Avaa edellisessä osassa kuvatulla tavalla ja käyttäjä näkee haun seuraavassa kuvatulla tavalla.

[![Kun syötetään asiakkaan Tilitunnus tilannekohtaiset haku](./media/howtocontextuallookups-1.png)](./media/howtocontextuallookups-1.png)

Käyttäjä voi kuitenkin myös nyt syöttää alku **nimi** myös. Jos tämä havaitaan, käyttäjä näkee seuraavat haku. Ilmoitus siitä, kuinka **nimi** saraketta siirretään Lookup on ensimmäinen sarake ja miten haku on lajiteltu ja suodatettu perusteella **nimi** sarakkeeseen.

[![Kun syötetään asiakkaan nimi tilannekohtaiset haku](./media/howtocontextuallookups-2.png)](./media/howtocontextuallookups-2.png)

## <a name="using-grid-column-headers-for-more-advanced-filtering-and-sorting"></a>Ruudukon sarakkeiden otsikoita käyttämällä kehittyneempiä suodattaminen ja lajitteleminen
Haku parannusten aiheena kahdessa edellisessä osiossa huomattavasti parantaa käyttäjän mahdollisuutta siirtyä rivien perusteella "alkaa merkillä"-haku haku **ID** tai **nimi** haku-kenttään. Kuitenkin tilanteita, joissa kehittyneempiä suodatus (lajittelu) tarvitaan tai löytääkseen oikean rivin. Näissä tilanteissa käyttäjän on käytettävä suodatuksen ja lajittelun asetukset hakua sisällä ruudukon sarakkeiden otsikoita. Otetaan esimerkiksi työntekijän myyntitilausrivin joka tarvitsee etsiä oikea "kaapeli" kuin tuote. Kirjoittamalla "kaapeli" **Tavaraerän numero** komponentti, ei ole hyötyä, koska ei ole tuotenimiä, jotka alkavat "kaapeli". 

![emptyitemlookup](./media/emptyitemlookup.png) 

Sen sijaan käyttäjä tarvitsee Tyhjennä haku-ohjausobjektin arvon ja hakukentän avattavan valikon avaaminen suodattaa pudotusvalikosta käytetään ruudukon sarakkeen otsikon, kuten kuvassa. Hiiri (tai touch) käyttäjä voi yksinkertaisesti valitsemalla (tai kosketa) suodattaminen ja lajitteleminen sarakkeen asetukset käyttämään mitä tahansa sarakeotsikkoa. Näppäimistö käyttäjän, käyttäjän yksinkertaisesti täytyy painaa **Alt**+**alas****nuolta** siirtää kohdistuksen avattavasta valikosta, minkä jälkeen käyttäjä voi oikea sarake-välilehti ja paina sitten toisen kerran **Ctrl**+**G** voit avata ruudukon sarakkeen otsikon avattavasta valikosta. 

[![gridfilteritemlookup](./media/gridfilteritemlookup.png)](./media/gridfilteritemlookup.png) 

Kun suodatin on otettu käyttöön (Katso alla olevaa kuvaa), käyttäjä voi etsiä ja valitse rivin tavalliseen tapaan. 

![filtereditemlookup](./media/filtereditemlookup.png)


