---
title: Tietojen etsiminen hakujen avulla
description: Tässä artikkelissa tutustutaan hakuominaisuuksiin ja annetaan joitain vinkkejä, joiden avulla käytät järjestelmän hakuja optimaalisesti.
author: jasongre
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 269934
ms.assetid: f20cbd2c-14e0-47e7-b351-8e60d3537f96
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ee309330c165dfb0b67f647afc3514d4c827dad1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8901520"
---
# <a name="find-information-by-using-lookups"></a>Tietojen etsiminen hakujen avulla

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Monessa kentässä on hakuja, jotka auttavat sinua löytämään oikean tai halutun arvo. Hakuihin on lisätty useita parannuksia, jotka helpottavat näiden ohjausobjektien käyttöä ja parantavat käyttäjien tuottavuutta. Tässä artikkelissa tutustutaan uusiin hakuominaisuuksiin ja annetaan joitain vinkkejä, joiden avulla käytät järjestelmän hakuja optimaalisesti.

## <a name="responsive-lookups"></a>Reagoivat haut

Aiemmissa versioissa haku-ohjausobjektin käyttäminen edellytti käyttäjiltä valikon avaamista erikseen. Tämä saattoi olla toteutettu kirjoittamalla ohjausobjektiin tähti (\*), jolla hakua suodatettiin ohjausobjektin nykyisen arvon mukaisesti, napsauttamalla valikon painiketta, tai käyttämällä **Alt**+**Alanuoli** -pikanäppäintä. Hakuobjekteja on muutettu seuraavilla tavoilla, jotta ne vastaisivat nykyisiä verkkosivukäytäntöjä:

- Haku-pudotusvalikot aukeavat nyt automaattisesti hetken kuluttua, kun kirjoittaminen on päättynyt, ja valikon sisältö suodatetaan hakuobjektin arvon mukaisesti.

    Huomaa, että vanha tapa avata hakuvalikko automaattisesti tähden (\*) kirjoittamisen jälkeen on poistunut.

- Kun hakuvalikko on avattu, tapahtuu seuraavaa:

    - Kohdistin jää hakuobjektiin (sen sijaan, että se siirtyisi valikkoon), jotta voit jatkaa hakusanan kirjoittamista. Käyttäjä voi kuitenkin käyttää **Ylä**- ja **Alanuoli** -näppäimiä vaihtaakseen valikon riviä ja Enter-painiketta valitakseen valikossa valitun rivin.
    - Valikon sisältö mukautuu hakuobjektin muutosten mukaisesti.

Otetaan esimerkiksi hakukenttä **Kaupunki**.

Kun kohdistus on **Kaupunki**-kentässä, voit aloittaa haluamasi kaupungin etsinnän kirjoittamalla muutaman kirjaimen, kuten "col". Kun lopetat kirjoittamisen, haku avautuu automaattisesti ja se suodatetaan näyttämään kaupungit, jotka alkavat kirjaimilla "col".

[![typeaheadLookupExample.](./media/typeaheadlookupexample.png)](./media/typeaheadlookupexample.png)

Tässä vaiheessa kohdistin on edelleen hakukentässä. Jos jatkat kirjoittamista, niin, että arvo on "colum", haun sisältö mukautuu automaattisesti vastaamaan hakuobjektin uusinta arvoa.

![updateFilterLookupExample.](./media/updatefilterlookupexample.png)

Vaikka kohdistus on yhä hakuobjektissa, voit käyttää lisäksi **Ylä-** ja **Alanuoli**-näppäimiä korostaaksesi rivin, jonka haluat valita. Painamalla **Enter**-näppäintä korostettu rivi valitaan hausta ja ohjausobjektin arvo päivittyy.

![changingSelectionLookup.](./media/changingselectionlookup.png)

## <a name="typing-in-more-than-ids"></a>Muiden kuin tunnisteiden kirjoittaminen

Kun kirjoitat tietoja, on luonnollista yrittää tunnistaa yksikkö, kuten asiakas tai toimittaja, nimen perusteella yksikköä edustavan tunnisteen perusteella. Monet (mutta eivät kaikki) haut sallivat nyt kontekstitietojen syöttämisen. Tämä ominaisuus sallii käyttäjän kirjoittaa tunnisteen tai sitä vastaavan nimen hakuobjektiin.

Esimerkkinä voimme käyttää **Asiakkaan tili** -kenttää, kun luot myyntitilausta. Tässä kentässä näytetään asiakkaan **Tilitunnus**, mutta käyttäjä kirjoittaa yleensä mieluummin tähän kenttään **tilin nimen** **tilitunnuksen** sijaan luodessaan myyntitilauksia, kuten "Forest Wholesales" "US-003":n sijaan.

Jos käyttäjä syöttää **tilitunnuksen** hakuobjektiin, valikko aukeaa automaattisesti edellisessä osassa kuvatun mukaisesti, ja käyttäjä näkee alla olevan kuvan mukaisen haun.

[![Kontekstihaku, kun asiakkaan tilitunnus on syötetty.](./media/howtocontextuallookups-1.png)](./media/howtocontextuallookups-1.png)

Käyttäjät voivat nyt myös aloittaa **tilin nimen** kirjoittamisen. Jos tämä havaitaan, käyttäjä näkee seuraavanlaisen haun. Huomaa, kuinka **Nimi**-sarake siirretään haun ensimmäiseen sarakkeeseen ja kuinka haku järjestetään ja suodatetaan **Nimi**-sarakkeen perusteella.

[![Kontekstihaku, kun asiakkaan tilin nimi on syötetty.](./media/howtocontextuallookups-2.png)](./media/howtocontextuallookups-2.png)

## <a name="using-grid-column-headers-for-more-advanced-filtering-and-sorting"></a>Ruudukon sarakeotsikoiden käyttäminen edistyneempään suodattamiseen ja lajitteluun

Edellisissä osiossa käsitellyt haun parannukset helpottavat käyttäjän mahdollisuuksia siirtyä haun rivien välillä "alkaa"-tyyppisen **tunnus**- tai **nimi**-kenttähaun perusteella. On kuitenkin tilanteita, joissa oikean rivin löytäminen vaatii edistyneempiä suodattimia tai lajittelua. Näissä tilanteissa käyttäjän on käytettävä haun sisäisiä ruudukon sarakeotsikoiden suodatus- ja lajitteluasetuksia. Otetaan esimerkiksi työntekijä, joka on syöttämässä myyntitilausriviä, johon on haettava oikea "kaapeli" tuotteeksi. Kirjoittamalla "kaapeli" **Nimiketunnus**-objektiin ei auta, sillä järjestelmässä ei ole "kaapeli"-alkuisia tuotenimiä.

![emptyitemlookup.](./media/emptyitemlookup.png)

Sen sijaan käyttäjän on tyhjennettävä hakuobjektin arvo ja avattava haun valikko, jota hänen on suodatettava ruudukon sarakeotsikon avulla, alla olevan kuvan mukaisesti. Hiiren (tai kosketusnäytön) käyttäjä voi yksinkertaisesti napsauttaa (tai koskettaa) mitä tahansa sarakkeen otsikkoa avatakseen kyseisen sarakkeen suodatus- ja lajitteluvaihtoehdot. Näppäimistön käyttäjän on yksinkertaisesti painettava **Alt**+**Ala** **nuoli**-näppäintä toisen kerran, joka siirtää kohdistuksen avattavaan valikkoon, jonka jälkeen käyttäjä siirtyä oikeaan sarakkeeseen sarkaimella ja painaa sitten **Ctrl**+**G** -pikanäppäintä avatakseen ruudukon sarakeotsikon valikon.

[![gridfilteritemlookup.](./media/gridfilteritemlookup.png)](./media/gridfilteritemlookup.png)

Kun suodatin on otettu käyttöön (ks. alla oleva kuva), käyttäjä voi paikantaa rivin tavalliseen tapaan.

![filtereditemlookup.](./media/filtereditemlookup.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]