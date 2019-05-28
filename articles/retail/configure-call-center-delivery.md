---
title: Määritä puhelinkeskuksen toimitustavat ja kulut
description: Tässä aiheessa kuvataan, miten puhelinkeskuksen toimitustavat ja kulut määritetään Microsoft Dynamics 365 for Retailissa.
author: josaw1
manager: AnnBe
ms.date: 04/26/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailMCRChannelDetailPage, MCROrderParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-04-30
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 2571b4ffd6c13dbf755ef2dfa93b757822890d96
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1553596"
---
# <a name="configure-call-center-delivery-modes-and-charges"></a>Määritä puhelinkeskuksen toimitustavat ja kulut

[!INCLUDE [banner](includes/banner.md)]

Kun myyntitilaus on luotu Microsoft Dynamics 365 for Retailissa ja jos henkilö, joka syötti myyntitilauksen, on linkitetty puhelinkeskuskanavaan, liiketoimintalogiikkaa ja sääntöjä käytetään vahvistamaan tilauksen toimituksen (toimitustapa) ja laskemaan tilauksen kulut.

Kun luot myyntitilauksen, voit valita toimitustavan myyntitilauksen otsikossa ja myyntitilausriveillä. Oletuksena otsikossa valittua toimitustapaa käytetään kaikilla myyntitilausriveillä. Voit kuitenkin ohittaa yksittäisillä myyntiriveillä toimituksen oletustilan tarpeen mukaan. Voit myös määrittää toimitustilan asiakastietueessa. Kun asiakkaalle luodaan tilauksia, tätä toimitustapaa käytetään oletuksena myyntitilauksen otsikossa.

Retailissa on ominaisuuksia, joiden avulla käyttäjät voivat rajoittaa toimitustapoja, joita kanava tai tuote voi käyttää, ja toimitustapoja, jotka ovat voimassa tiettyihin kohteisiin toimitettaessa. Kulut voidaan määrittää myös siten, että lisämaksut lisätään asiakkaan tilaukseen toimitustapojen perusteella, jotka on valittu kyseiselle myyntitilaukselle ja tilauksen kokonaisarvolle.

## <a name="define-delivery-modes"></a>Toimitustapojen määrittäminen

Ennen kuin määrität puhelinkeskuksen tilausten toimitustavat ja määrität liittyvät säännöt ja kulut, on määritettävä toimitustavat. Siirry kohtaan **Myynti ja markkinointi \> Asetukset \> Jakelu \> Toimitustavat**. Luo uusi toimitustila valitsemalla **Uusi**. Voit myös valita aiemmin luodun toimitustavan luettelosta ja valita sitten **Muokkaa** tehdäksesi muutoksia.

**Toimitustapa**-kenttään voit syöttää minkä tahansa yhdistelmän aakkosnumeerisia merkkejä liiketoimintasi tarpeen mukaan. **Kuvaus**-kentässä voit antaa lisätietoja. **Kuluryhmä**- ja **Nopeuta**-kentät ovat valinnaisia ja ne selitetään tässä ohjeaiheessa tarkemmin myöhemmin.

**Vähittäismyyntikanavat**-pikavälilehdessä voit lisätä kaikki vähittäismyyntikanavat, joiden tulisi voida käyttää tätä toimitustapaa kyseisen kanavan myyntitapahtumien luonnin yhteydessä.

**Tuotteet**-pikavälilehdessä voit määrittää, mille tuotteille ja/tai tuoteryhmille tätä toimitustapaa voi käyttää ja mille ei. Jos esimerkiksi tuotetta ei voi toimitta lentorahtina vaarallisen materiaalin (hazmat) rajoitusten vuoksi, varmista, että tuote tai tuoteluokka jätetään pois kaikista toimitustavoista, joihin liittyy lentokuljetus.

**Osoitteet**-pikavälilehdessä voit määrittää, mille maille, alueille tai osavaltioille tätä toimitustapaa voi käyttää ja mille ei. Esimerkiksi tilaukset, jotka toimitetaan Havaijille tai Alaskaan, eivät ole käytettävissä maakuljetustoimitusta varten. Siksi nämä osavaltiot on suljettava pois kaikista maakuljetukseen liittyvistä toimitustavoisrta, mutta ne sisältyvät kaikkiin toimitustapoihin, joka liittyy käytettäessä lentorahtia.

## <a name="validate-delivery-modes-for-a-call-center-order"></a>Vahvista puhelinkeskuksen tilauksen toimitustavat

Kun toimitustavat on määritetty, sinun on suoritettava **Käsittele toimitustilat** -erätyö. Tämä työ tekee toimitustavoista käytettäviä siten, että niitä voidaan käyttää myyntitilauksen prosesseissa vähittäismyynnin kanavien osalta. Voit suorittaa **Käsittele toimitustilat** -työn siirtymällä kohtaan **Vähittäismyynti \> Vähittäismyynnin IT \>Käsittele toimitustilat**. Tämä työn pitää suorittaa aina, kun vähittäismyynnin kanavaan lisätään uusia toimitustapoja tai kun tehdään muutoksia toimitustapojen ja kanavien suhteisiin.

Kun olet suorittanut **Käsittele toimitustilat** -eräajon, voit siirtyä kohtaan **Vähittäismyynti \> Kanavat \> Puhelinkeskukset \> Kaikki puhelinkeskukset**. Valitse **Kaikki puhelinkeskukset** -sivun toimintoruudun **Asetukset** -välilehdessä **Toimitustavat**. **Toimitustavat**-sivulla näkyy luettelo kaikista valitun puhelinkeskuskanavan voimassa oelvista toimitustavoista. Voit muokata aiemmin luotuja toimitustapoja tai lisätä uusia toimitustapoja valitsemalla **Ylläpidä toimitustapoja**. Huomaa, että **Käsittele toimitustilat** -työ on suoritettava aina, kun muutoksia tehdään.

## <a name="define-charges-for-delivery-services"></a>Määritä toimituspalveluiden kulut

Kun myyntitilauksia luodaan asiakkaille, yrityksen kannattaa lisätä kuluja, jotka lasketaan automaattisesti tilaukselle valittujen toimitustapojen perusteella. Nämä kulut voidaan määrittää niin, että ne ovat samat kaikille asiakkaille ja toimitustavoille. Vaihtoehtoisesti kulut voivat vaihdella asiakkaan ja/tai myyntitilaukselle valitun toimitustavan perusteella.

Voit määrittää kulut kohdassa **Vähittäismyynti \> Kanavan asetukset \> Kulut \>Automaattiset kulut**. Valitse **Uusi**, jotta voit lisätä uusia kuluja. Voit myös valita aiemmin luodun kulun ja sitten **Muokkaa**.

Kulut voidaan määrittää siten, että ne ovat voidaan laskea tilausotsikon tai tilausrivien tasolla. **Taso**-kentän avulla voit valita haluamasi tason.

Kulut voidaan määrittää tietylle asiakkaalle, asiakasryhmälle tai kaikille asiakkaille. Valitse **Tilikoodi**-kenttään **Taulu** määrittääksesi kulut, joita käytetään vain tietylle asiakkaalle. Valitse **Ryhmä**, jotta voit määrittää tietyn asiakasryhmän kulut. Valitse **Kaikki** kohdistaaksesi kulut jokaiselle asiakkaalle, joka luo myyntitilauksen, jotka käyttää liittyvää toimitustapaa. Jos olet valinnut **Taulu** tai **Ryhmä** **Tilikoodi**-kentässä, valitse asiakas tai asiakasryhmä **Tilisuhde**-kentässä.

Kulut voidaan määrittää niin, että niitä käytetään tietylle toimitustavalle, toimitustaparyhmälle tai kaikille toimitustavoille. Jos valitset **Taulu** **Toimitustapakoodi**-kentässä, sinun on valittava tietty toimitustapa- **Toimitustapasuhde**-kentässä. Jos valitset **Ryhmä**, sinun on valittava toimitustaparyhmä **Toimitustapasuhde**-kentässä. Toimitustaparyhmät määritetään kohdassa **Vähittäismyynti \> Kanavan asetukset \> Kulut \> Toimituksen kuluryhmä**. Ne sitten voidaan linkittää yhteen tai useampaan toimitustapaan **Toimitustavat**-sivulla. Jos kuluja määrittäessäsi valitset ryhmän, kaikki toimitustavat, jotka on linkitetty valittuun toimitusryhmään, käyttävät näitä kuluja. Lopuksi, jos valitset **Kaikki** **Toimitustapakoodi**-kentässä, kaikki toimitustavat käyttävät näitä kuluja. Siksi et valitse arvoa **Toimitustapasuhde**-kentässä.

**Rivit**-osassa voit määrittää yhdet tai useammat kulut valuutan mukaan tarpeen mukaan. Kulut on linkitettävä kulukoodiin, joka määrittää tämän kulun taloushallinnon kirjaussäännöt. **Luokka**-kenttää käytetään määrittämään, miten kulut lasketaan. Esimerkiksi jos asiakkailta tulisi veloittaa 9,95 dollarin kiinteä hinta tilauksen toimittamiseksi tietyn toimitustavan mukaan, käytä **Kiinteä**-luokkaa. Jos yritys päättää laskuttaa asiakkailta prosenttiosuuden tilauksen loppusummasta toimituskulujen kattamiseksi, käytä **Prosentti**-luokkaa. Asiakkaan todelliset kulut on määritetty **Kulujen arvo** -kentässä.

Vähittäismyyntiyritykset määrittävät usein kulut eri tasoille. Tällöin summa, jonka asiakkaat maksavat toimitusta varten, perustuu tilauksen arvoon. Voit määrittää kulutasot kirjoittamalla arvot **Summasta**- ja **Summaan**-kenttiin sen lisäksi, että määrität itse kulun **Kulujen arvo** -kenttään. Esimerkiksi tilauksille, joiden arvo on pienempi kuin 50 dollaria, kauppa veloittaa 5,95 dollaria maakuljetustoimituksesta. Tilauksista, joiden arvo on vähintään 50 dollaria mutta pienempi kuin 100 dollaria, myyjä veloittaa 7,95 dollaria. Lopuksi, tilauksista, joiden arvo on vähintään 100 dollaria, myyjä tarjoaa ilmaisen toimituksen. Seuraavassa kuvassa on tällaisten kulujen määritys.

![Esimerkki: kiinteät kulut tasoittain](media/fixedtieredcharges.png)

Voit käyttää luokkien yhdistelmiä kuluille liiketoiminnan tarpeiden mukaan. Esimerkiksi kaikille tilauksille, joiden arvo on pienempi kuin 100 dollaria, veloitetaan kiinteä 9,95 dollaria toimituksesta. Tällöin tilauksille, joiden arvo vähintään 100 dollaria, toimituksen kuluiksi lasketaan 5 prosenttia tilauksen arvosta. Seuraavassa kuvassa on tällaisten kulujen määritys.

![Esimerkki: kulutasojen yhdistelmä](media/mixedtieredcharges.png)

## <a name="apply-delivery-modes-during-order-entry-in-a-call-center"></a>Käytä toimitustapoja puhelinpalvelukeskuksen tilausta syötettäessä

Kun uusi myyntitilaus luodaan, arvo on määritettävä **Toimitustapa**-kenttään **Toimitus**-pikavälilehdessä myyntitilauksen otsikossa. Tämä kenttä voidaan täyttää automaattisesti asiakastietueen oletusarvojen mukaan.

Toimitustapa, joka on määritetty tilauksen otsikkotiedoissa kopioidaan automaattisesti myyntitilauksen riveille niiden luonnin yhteydessä. Voit kuitenkin muuttaa tietyn rivinimikkeen toimitustapa-asetusta **Toimitus**-välilehden **Rivin erittely** -osassa myyntitilauksen syöttösivulla.

Jos valittu toimitustapa ei ole kelvollinen tuotteelle tai toimitusosoitteelle, joka on määritetty tilaukseen tai tilausriville, saat virhesanoman. Sitten sinun on valittava toimitustapa, joka on määritetty tukemaan kyseisen osoitteen tai tuotteen kokoonpanoa.

## <a name="calculation-of-delivery-charges-during-entry-of-order"></a>Tilauksen toimituksen kulujen laskenta tilauksen syöttämisen aikana

Jos **Ota käyttöön tilausten viimeistely** -asetus on otettu käyttöön puhelinkeskuskanavassasi, kuljetusmaksut lasketaan automaattisesti myyntitilauksille käyttäjien valitessa **Viimeistele**. Näyttöön tulee seuraava sanoma **Myyntitilauksen yhteenveto** -sivun yläosassa: ”Maksutasot laskettu”. Lasketut kulut lisätään **Myynti yhteensä** -kentän arvoon. **Summa**-pikavälilehden **Kulut**-kenttä näyttää kaikkien kulujen yhteissumman, jotka on laskettu tilaukselle ja riveille. Kulujen yksityiskohtaisen erittelyn näet valitsemalla **Tilaus** **Myyntitilauksen yhteenveto** -sivulla ja valitsemalla sitten **Kulut**-vaihtoehto, jolloin voit tarkastella, lisätä tai muokata kuluja. Huomaa, että toimituskulujen laskenta tilausotsikossa perustuu toimitustapaan, joka on linkitetty otsikkoon. Rivitason toimituskulut lasketaan perustuen toimitustapaan, joka on määritetty myyntiriville. Jos käytetään useita toimitustapoja eri riveillä, nämä monet kulut saatetaan kohdistaa ja laskea yhteen. Kokonaissumma näkyy **Kulut**-kentässä **Myyntitilauksen yhteenveto** -sivulla.

Jos **Ota käyttöön tilausten viimeistely** -asetus ole käytössä, käyttäjien on manuaalisesti käynnistettävä kulujen laskenta. Valitse **Myyntitilaus**-sivun toimintoruudun **Myy**-välilehden **Laske**-ryhmässä **Maksutasot**. Näkyviin tulee sanoma ”Maksutasot laskettu”. Voit sitten valita **Kulut**-asetukse **Myynti**-välilehdessä, ja voit tarkastella, muokata tai poistaa laskettuja kuluja.

## <a name="use-expedited-delivery-modes-on-call-center-orders"></a>Käytä nopeutettuja toimitustapoja puhelinkeskuksen tilauksissa

Halutessasi voit linkittää kaikkiin toimitustapoihin nopeutuskoodin. Tätä koodia käytetään priorisointilajittelun ja raportoinnin työkaluna. Se ei tällä hetkellä aiheuta tilaukseen kohdistettavia lisämaksuja. Voit määrittää nopeutuskoodeja siirtymällä kohtaan **Myynti ja markkinointi \> Asetukset \> Toimitukset \> Nopeutuskoodit**.

Esimerkiksi tilauksille, jotka toimitetaan seuraavana päivänä lentorahtina, keräys on tehtävä varastossa kello 23 päivittäin. Tässä tapauksessa nopeutuskoodi voidaan luoda ja koodi voidaan linkittää kaikkiin seuraavan päivän toimitustapoihin, jotka on määritetty järjestelmässä. Kun varasto luo keräilyaallon, soveltuvaa nopeutuskoodia **Nopeuta**-kentässä voidaan käyttää suodattimena siten, että keräily suoritetaan vain tilauksille, joilla on toimitustapa, joka on linkitetty tähän koodiin.

Lisäksi, kun luodaan puhelinkekuksen tilaus, kun nopeutuskoodia voidaan manuaalisesti käyttää joko myyntitilauksen otsikkoon tai yksittäiseen myyntitilausriviin. Edelleen tätä koodia voidaan käyttää lajitteluun ja raportointiin. Joskus tilausta on käsiteltävä huolellisesti asiakaspalvelun ongelman vuoksi. Tässä tapauksessa tietty nopeutusvoidaan ottaa käyttöön tilauksen otsikossa tai riveillä, jotta tilaus voidaan tunnistaa ja priorisoida tilauslupausta toteutettaessa.
