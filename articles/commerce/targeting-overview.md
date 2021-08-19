---
title: Laite- ja markkinakohtainen sekä maantieteelliseen sijaintiin perustuva markkinointi
description: Tässä aiheessa käsitellään kohderyhmien ja kohteiden luontia, muokkausta ja hallintaa Microsoft Dynamics 365 Commercen sivuston luontityökalussa laite- ja markkinointitietoja sekä maantieteellistä sijaintia koskevia tietoja hyödyntämällä.
author: sushma-rao
ms.date: 07/30/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2021-07-31
ms.dyn365.ops.version: AX 10.0.21
ms.openlocfilehash: 3ecc04c97b42b17f257aa40f665136c70de398748b9bda0da860c7000c062807
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6730848"
---
# <a name="device-market-and-geolocation-targeting"></a>Laite- ja markkinakohtainen sekä maantieteelliseen sijaintiin perustuva markkinointi

[!include [banner](includes/banner.md)]

Tässä aiheessa käsitellään kohderyhmien ja kohteiden luontia, muokkausta ja hallintaa Microsoft Dynamics 365 Commercen sivuston luontityökalussa laite- ja markkinointitietoja sekä maantieteellistä sijaintia koskevia tietoja hyödyntämällä.

Dynamics 365 Commercessa on mahdollista mukauttaa sivun sisältöä (*kohdetta*) tietyn asiakasryhmän (*käyttäjäryhmän*) mukaan, mikä auttaa parantamaan käyttäjän aktivoitumista ja tyytyväisyyttä. Sekä käyttäjäryhmä että kohde voidaan luoda ensimmäisenä. Kohdistamisen onnistumiseen tarvitaan kuitenkin molemmat.

Käyttäjäryhmiä luodaan ja hallitaan Commercen sivuston luontityökalussa asiakastietojen perusteella. Näitä tietoja ovat esimerkiksi sijainti, laitetiedot, kirjautumistila ja muut asiakkaan verkkopyynnöistä dynaamisesti johdetut tiedot. Voit myös luoda ja hallita kohteita Commercen sivuston luontityökalun sähköisen kaupankäynnin moduuleissa ja katkelmissa.

**Vastuuvapauslauseke:** Vastaat itse siitä, että tätä ominaisuutta käytetään sovellettavien lakien ja määräysten, mukaan lukien kohdentamiseen ja profilointiin liittyvien lakien ja määräysten mukaisesti. 

## <a name="audiences"></a>Yleisöt

Käyttäjäryhmä on käyttäjistä koostuva ryhmä, jonka jäsenyys määräytyy dynaamisen sääntöjoukon perusteella. Nämä säännöt ovat yksinkertaisia loogisia testejä, joihin asiakaspyynnöistä ja muista käytettävissä olevista segmenteistä saatavia tietoja verrataan. Useita sääntöjä voidaan yhdistää JA- ja TAI-operaattorien avulla.

Commerce tukee perussegmenttejä, kuten laitetietoja, kirjautumistilaa, viittaajaa ja kyselyn merkkijonoparametreja. Se tukee myös laajennettavia segmenttejä hyödyntämällä kolmannen osapuolen palveluja.

### <a name="basic-segments"></a>Perussegmentit

Seuraavat segmentit ovat oletusarvoisesti käytettävissä, ja ne voidaan sisällyttää käyttäjäryhmän määrityksiin:

- **Kirjautumisen tila** – testaa, onko käyttäjä todennettu.
- **Laiteympäristö** – testaa seuraavat laitetyypit:

    - Matkapuhelin
    - Työpöytä
    - Tabletti
    - Muu

- **Laitteen käyttöjärjestelmä** – testaa seuraavat käyttöjärjestelmät:

    - Windows
    - Linux
    - iOS
    - Android, muu

- **Kyselymerkkijonon parametrit** – Testaa, onko pyynnön URL-osoitteen kyselymerkkijonon parametrissa avain- ja arvoparia. Esimerkiksi URL-osoitteelle `www.fabrikam.com/en-us/request?promo=true` voidaan kirjoittaa sääntö testaamaan, onko **promo**-parametrin arvo **tosi**.
- **Eväste** – Testaa pyynnön URL-osoitteessa toimialueelle määritetyn evästeen arvon. Esimerkiksi Fabrikam.com-pyyntö voi sisältää evästeen, jossa on nimi **CustomLayout** ja arvo **1**. Evästetesti tarkistaa evästeen olemassaolon mutta ei nimenomaisesti luo evästettä. Edellisessä esimerkissä JavaScriptin on täytynyt määrittää **CustomLayout**-eväste toisesta moduulista tai jostain muusta liiketoimintaprosessista.

    > [!NOTE]
    > Evästeiden käytön osalta on muistettava varmistaa, että sovellettavaa lainsäädäntöä noudatetaan.

- **Viittaaja** – jos käyttäjä pyytää sivua avaamalla linkin, viittaaja on sen sivun URL-osoite, joka isännöi linkkiä.

### <a name="extensible-segments"></a>Laajennettavat segmentit

Commercen avulla voidaan laajentaa käytettävissä olevien segmenttien luetteloa muodostamalla yhteys kolmannen osapuolen palveluihin. Segmentointipalvelu antaa kuvauksen käytettävissä olevien segmenttien tyypeistä. Lisätietoja yhteyden muodostamisesta maantieteelliseen sijainti- tai segmentointipalveluun on kohdassa [Yhdistimien määrittäminen ja ottaminen käyttöön](e-commerce-extensibility/connectors.md).

> [!NOTE]
> - Jos ulkoinen palvelu otetaan käyttöön, se voi muodostaa yhteyden palveluun, jonka suorituskykyä ei voi ennakoida. Käyttäjäkokemusta voidaan parantaa näyttämällä sivun oletusversio, jos käyttää pyytää kohdentamista käyttäjän sivun ja kyseinen sivu käyttää viitteenä käyttäjäryhmää, joka tarkistaa kolmannen osapuolen segmentointipalvelun.
> - Käyttäjän on hyväksyttävä evästeiden käyttö. Käyttäjän selain pyytää sitten kaikki segmentit soveltuvista palveluista, ja tulokset sijoitetaan evästeeseen, joka palautetaan käyttäjälle. Seuraavat sivulle tehtävät pyynnöt käyttävät näitä tietoja kohdennetun sisällön tarjoamiseen käyttäjälle. Lisätietoja evästeiden vaatimustenmukaisuudesta on kohdassa [Evästeiden vaatimustenmukaisuus](cookie-compliance.md).

**Vastuuvapauslauseke:** Jos otat tämän ominaisuuden käyttöön, tiedot jaetaan valittujen kolmannen osapuolten järjestelmien kanssa. Päätät itse, mitä tietoja kolmannelle osapuolelle mahdollisesti annetaan. Olet tietoinen siitä, että kolmannen osapuolen tietojen käsittely- ja vaatimustenmukaisuusstandardit voivat poiketa Microsoft Dynamics 365 Commercen standardeista. Tietosuojasi on tärkeää Microsoftille. Lisätietoja on [Tietosuoja ja evästeet -ilmoituksessa](https://privacy.microsoft.com/privacystatement).

### <a name="create-an-audience-in-site-builder"></a>Käyttäjäryhmän luominen sivuston luontityökalussa

Käyttäjäryhmä luodaan Commercen sivuston luontityökalussa seuraavasti:

1. Valitse vasemmassa siirtymisruudussa **Käyttäjäryhmät**.
1. Valitse **Uusi**.
1. Anna käyttäjäryhmälle nimi. Myös tunnisteita ja kuvaus voidaan lisätä.
1. Valitse ensin **Luo** ja sitten **Lisää uusi sääntölohko**. Sääntölohko on JA-ehdoilla yhteenliitetty sääntökokoelma. Lisäksi voidaan luoda useita sääntölohkoja, joiden välillä on TAI-ehtoja.
1. Valitse segmenttien tietolähde sekä määritä segmentin nimi, operaattori ja arvot. Sääntölohkossa voidaan luoda lisää sääntöjä tai poistaa niitä. Vaihtoehtoisesti voidaan luoda ja poistaa kokonaisia sääntölohkoja. Sääntölohkoja voidaan myös siirtää ylös- ja alaspäin tarpeen mukaan.

    > [!NOTE]
    > Luettelossa voi olla enintään 100 arvoa, ja kussakin luettelokohteessa voi olla enintään 50 merkkiä.

1. Kun olet tyytyväinen käyttäjäryhmän määritykseen, valitse **Lopeta muokkaaminen**. Sen jälkeen kun **Julkaise** on valittu, käyttäjäryhmää voi käyttää reaaliaikaisessa kohteessa. Vaihtoehtoisesti käyttäjäryhmä voidaan julkaista yhdessä kohteen kanssa. 

Käyttäjäryhmää muokataan valitsemalla sen hyperlinkki **Käyttäjäryhmät**-välilehdessä ja valitsemalla sitten **Muokkaa** avautuvassa käyttäjäryhmäeditorissa. Reaaliaikaisten kohteiden ja kohderyhmään viittaavien sivujen luetteloa voi tarkastella valitsemalla käyttäjäryhmän käyttäjäryhmän luettelonäkymässä ja valitsemalla sitten **Näytä tehtävät**. Käyttäjäryhmän voi poistaa käyttäjäryhmän luettelonäkymässä tai käyttäjäryhmäeditorissa peruuttamalla jo julkaistun käyttäjäryhmän julkaisun ja valitsemalla sitten komentopalkissa **Poista**.

> [!NOTE]
> Käyttäjäryhmät ovat sivustotason käsite Commercen sivuston luontityökalussa. Sama käyttäjäryhmä voidaan jakaa useissa kohteissa.

## <a name="targets"></a>Kohteet

Kohde on käyttökokemus, joka näytetään valittujen käyttäjäryhmien jäsenille. Se voi sisältää moduulien sivulla tai katkelmassa näytettäviä variaatioita. 

Kohteelle voidaan määrittää aikataulu määrittämään, kuinka kauan se pysyy aktiivisena. On huomattava, että tämä toiminto ei ole sama kuin julkaisuryhmän aikatauluttaminen, jolla määritetään, milloin sisältökokoelma julkaistaan. Kohteita voi myös esikatsella. Tällä tavoin nähdään, miltä ne näyttävät valittujen kohdeyleisöjen jäsenille. Lisäksi kohteet voidaan priorisoida määrittämällä, mitkä kohteet näytetään ristiriitatilanteessa.

### <a name="create-a-target"></a>Kohteen luominen

Sivumoduulien kohdeliittymä luodaan Commercen sivuston luontityökalulla seuraavasti:

1. Valitse vasemmanpuoleisessa siirtymisruudussa **Sivut**. Valitse sitten sen sivun hyperlinkki, jonka moduulit halutaan kohteeksi.
1. Kuittaa sivu ulos muokattavaksi valitsemalla **Muokkaa**.
1. Luo uusi kohdeliittymä valitsemalla **Kohde**-valikossa **Uusi kohde**. Sivulle voidaan luoda tarvittava määrä kohteita.
1. Anna kohteelle nimi ja kuvaus. Valitse sitten **Seuraava**.
1. Sisällytä käyttäjäryhmät, jotka näkevät kohdennetun sisällön, valitsemalla **Lisää**. Vaihtoehtoisesti käyttäjäryhmiä voidaan jättää pois. Valitse sitten **Seuraava**.

    > [!NOTE]
    > Käyttäjäryhmän määritys on valinnainen vaihe kohteen luonnin aikana. Ennen kohteen julkaisua on kuitenkin sisällytettävä ainakin yksi käyttäjäryhmä, sillä näin voidaan varmistaa, että suunnitellut käyttäjäryhmät näkevät kohdennetun sisällön.

1. Määritä aikaikkuna, jolloin kohde näytetään, valitsemalla aikavyöhyke sekä alkamis- ja päättymispäivät ja -ajat. Kohteen voi määrittää siten, että se näytetään koko ajan aikaikkunan aikana. Vaihtoehtoisesti voidaan valita tietyt päivät ja ajat. Kun olet valmis, valitse **Seuraava**.

    > [!NOTE]
    > Määritettävät ajat ja aikavyöhyke ovat maailmanlaajuisia. Jos kohdennus halutaan tehdä eri sijainteihin eri aikoina tai eri aikavyöhykkeillä, tätä varten on luotava erilliset kohteet ja kullekin sijainnille on määritettävä oma aikataulu.

1. Tarkista tiedot ja, jos kaikki näyttää olevan kunnossa, valitse ensin **Luo kohdekokemus** ja sitten **Siirry kohteeseen**. Kohdeliittymä luodaan. Siihen voi nyt lisätä moduuleja.
1. Valitse ensin moduuli kohteeseen, sitten kolme pistettä (**...**) ja lopuksi **Lisää nykyiseen kohteeseen**. Jos kohde on päämoduuli, kaikkien sen alimoduulit tuleva osaksi kyseistä kohdetta. Kohdennetut moduulit on korostettu vihreällä.
1. Tee kohteen moduuliin tarvittavat sisältöpäivitykset ja lisää kohteeseen tarvittaessa lisää moduuleja. Tallenna sitten kaikki muutokset valitsemalla **Tallenna**.
1. Muista tarkistaa kohde ennen julkaisua valitsemalla **Esikatselu**. Valittavana on seuraavat vaihtoehdot:

    - **Perusesikatselu** – kun tämä vaihtoehto valitaan, vain valittu variaatio (oletussivu tai kohde) valitaan ilman liitettyjä kohderyhmiä.
    - **Tarkennettu esikatselu** – Tämä vaihtoehto kannatta valita, jos sivulla on useita kohteita ja niitä halutaan esikatsella valittu käyttäjäryhmäjoukkoon kuuluvana käyttäjä tai tiettynä ajankohtana. Tee valinta soveltuvien käyttäjäryhmien luettelossa valitsemalla **Seuraava**. Suodatin voidaan myös poistaa, jolloin valittavana on kaikki käyttäjäryhmät.

1. Kun olet tyytyväinen kohteen määrityksiin, sivu on julkaistava, jotta kohde julkaistaan. Julkaise kohde heti valitsemalla **Julkaise**. Vaihtoehtoisesti sivun julkaisu voidaan aikatauluttaa julkaisuryhmän avulla. Lisätietoja julkaisuryhmistä on kohdassa [Julkaisuryhmien kanssa työskenteleminen](publish-groups.md).

Kohteena voi käyttää myös katkelmia. Menettelytapa on samankaltainen. Vaiheessa 1 vasemmassa siirtymisvalikossa valitaan kuitenkin **Katkelmat** eikä **Sivut**.

> [!NOTE]
> Kielteiset vaikutukset mittausarvoihin voidaan estää käyttämällä sivulla tai katkelmassa joko kokeilua tai kohteita. Käytössä ei voi olla sekä kokeilu että kohteet.

### <a name="manage-targets"></a>Kohteiden hallinta

Kohteita muokataan ja poistetaan sekä niistä tehdään kaksoiskappaleita siirtymällä oletussivulle tai katkelmaan ja toimimalla seuraavasti:

1. Valitse avattavassa valikossa ensin **Kohde** ja sitten **Kohteiden hallinta**.
1. Valitse muokattava tai poistettava kohde tai kohde, josta tehdään kaksoiskappale.
1. Jos samassa moduulissa on useita kohteita tai jos useiden kohteiden aikataulujen välillä on ristiriitoja, valitse **Priorisoi kohteet** ja määritä järjestys, jossa kohteet näytetään. Jos sivulle tai katkelmaan lisätään useampi kuin yksi kohde, **Priorisoi kohteet** -painike näkyy myös ilmoituspalkissa muistuttamassa kohteiden priorisoinnista. Jos prioriteettia ei määritetä, viimeisin kohde valitaan oletusarvoisesti.

### <a name="localize-targets"></a>Kohteiden lokalisointi

Sivuilla ja katkelmissa olevat kohteet sisällytetään automaattisesti, kun XLIFF-tiedostoja viedään ja tuodaan lokalisointia varten. Jos jotain kielialuetta ei tarvita, niiden kohteet voidaan poistaa lokalisoitujen XLIFF-tiedostojen tuonnin jälkeen.

> [!NOTE]
> Kohteita hallitaan kanava- ja kielialuekohtaisesti. Yhdessä kanavassa tai yhdellä kielialueella kohteeseen tehtyjä muutoksia ei välitetä automaattisesti muihin kanaviin tai muille kielialueille.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
