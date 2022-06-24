---
title: Saapuvien merikuljetusten ja kuljetuskonttien matkojen seuranta
description: Tässä artikkelissa kerrotaan, miten Saapuvien jäljitys -sivun avulla voit seurata merikuljetusten ja kuljetuskonttien matkojen etenemistä.
author: Weijiesa
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMContainerActivityTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 17874f984945b27e036eafda841ec1fd95d345be
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8854352"
---
# <a name="track-inbound-voyages-and-shipping-container-journeys"></a>Saapuvien merikuljetusten ja kuljetuskonttien matkojen seuranta

[!include [banner](../../includes/banner.md)]

**Saapuvien jäljitys** -sivun avulla voit seurata merikuljetusten ja kuljetuskonttien matkojen etenemistä. Kullakin merikuljetuksella ja matkalla on jako *tehtäviin*, ja jokaisella on sivulla oma rivi. Sivulla voit tarkastella ja määrittää arvioituja päivämääriä ja toteutuneita päivämääriä tehtävän mukaan.

[Jäljityksen hallintakeskuksen](delivery-information-setup.md#tracking-control-center) asetusten mukaan nämä tehtävät näyttävät automaattisesti arvioidun saapumispäivämäärän lopullisessa kohteessa. Myös asetusten mukaan päättymispäivä päivittää yleensä ostotilausrivien toimituspäivän tai vahvistetun päivämäärän. Siirtotilausrivien kohdalla voit määrittää järjestelmän päivittämään vastaanottopäivän.

Avaa **Saapuvien jäljitys** -sivu, valitse **Aiheutunut kustannus \> Jäljitys \> Saapuvien jäljitys**.

## <a name="filter-the-activities-list"></a>Suodata tehtäväluettelo

Voit käyttää **Matka**- ja **Kuljetuskontti**-kenttiä **Saapuvien jäljitys** -sivulla siten, että sivulla näkyvät vain valittuun merikuljetukseen ja/tai kuljetuskonttiin liittyvät tehtävät.

## <a name="update-tracking-information"></a>Seurantatietojen päivitys

Jos haluat päivittää merikuljetuksen tai matkan aikataulua, kirjoita ensimmäisen tehtävän alkamispäivämäärä. Tämän jälkeen viimeisen tehtävän arvioitu päättymispäivämäärä päivitetään. Kunkin etappi- ja matkamallin asetukset [Jäljityksen hallintakeskuksessa](delivery-information-setup.md#tracking-control-center) määrittävät arvioidut läpimenoajat. Arvioiduissa päättymispäivämäärissä käytetään läpimenoaikaa tehtävän aloituspäivästä alkaen. Kun todellinen päättymispäivä tallennetaan, seuraavan tehtävän aloituspäivämääräksi päivitetään samaksi päivämääräksi kuin edellisen tehtävän todellinen päättymispäivä. Varsinainen läpimenoaika päivitetään niin, että vertailu ja analyysi voidaan tehdä. Voit lisätä huomautuksia **Huomautus**-kenttään.

Ruudukon toimintojen järjestys määräytyy sen mukaan, mikä järjestys etapeilla on asianmukaisessa matkamallissa. Jos oheisena olevan matkan etappien järjestys muuttuu, myös jäljityksenhallinta muuttuu.

Voit päivittää kaikkien konttien päivämäärät valitsemalla toimintoruudussa **Päivitä alkamispäivä** tai **Päivitä todellinen päättymispäivä**. Vaihtoehtoisesti voit syöttää päivämäärät lähetyksen konttia kohti. Tämä on joustavampaa, koska kontit voidaan jakaa monietappisen matkan ympäristössä.

## <a name="buttons-on-the-action-pane"></a>Toimintoruudun painikkeet

**Saapuvien jäljitys** -sivun toimintoruudun painikkeiden avulla voit käyttää saapuvia merikuljetuksia ja matkoja. Seuraava taulukko kuvaa käytettävissä olevat painikkeet.

| Painike | kuvaus |
|---|---|
| Muokkaa | Muokkaa merikuljetuksen tai kuljetuskontin matkaa. |
| Luo uusi | Luo uusi merikuljetuksen tai kuljetuskontin matka. |
| Delete-näppäin | Poista valittu merikuljetuksen tai kuljetuskontin matka. |
| Päivitä alkamispäivä | Päivitä tehtävän alkamispäivämäärä kaikkien matkan konttien osalta. Kun matkan tietyn tehtävän tai etapin aloituspäivä päivitetään, seuraavat arvioidut aloituspäivämäärät päivitetään määritetyn läpimenoajan perusteella. |
| Päivitä todellinen päättymispäivä | Päivitä tehtävän päättymispäivämäärä kaikkien matkan konttien osalta. Kun matkan tietyn tehtävän päättymispäivä päivitetään, seuraavat tehtävät päivitetään määritetyn läpimenoajan perusteella. |
| Lisää tehtäviä | Lisää tehtävä matkaan manuaalisesti. Voit lisätä esimerkiksi kaasutustehtävän. Lisäys saattaa aiheuttaa sen, että aluksen tuotteiden tai matkan vahvistettu toimituspäivä voi muuttua. Kun tehtävä on lisätty matkaan, arvioituja päiviä ei lisätä, ennen kuin matkan etapin alkamispäivämäärä päivitetään. |

## <a name="information-and-settings-on-the-overview-tab"></a>Yhteenveto-välilehden tiedot ja asetukset

**Yhteenveto**-välilehdessä näkyy luettelo kaikista toiminnoista, jotka kuuluvat sivun yläosassa valittuun merikuljetukseen ja/tai kuljetuskonttiin. Seuraavassa taulukossa kuvataan kentät, jotka ovat käytettävissä kunkin tehtävän osalta.

| Kenttä | kuvaus |
|---|---|
| Etappi | Tehtävän etappitunnus matkamallissa määritetyllä tavalla. |
| Toimitustapa | Tehtävän odotettu toimitustapa. |
| Tehtävä | Tämä kenttä määrittää yleensä tehtävään liittyvän työn tai tehtävän. Tavallisia esimerkkejä ovat *Merellä* ja *Selvitys*. |
| kuvaus | Tehtävän pidempi kuvaus. |
| Aloituspäivä | Tässä kentässä näkyy alustavasti tehtävän arvioitu aloituspäivä. Todellinen aloituspäivä näytetään kuitenkin sen jälkeen, kun edellisen tehtävän todellinen päättymispäivä on syötetty. Tätä kenttää käytetään läpimenoajan perusteella arvioidun päättymispäivän määrittämiseen. |
| Arvoitu päättymispäivä | Tämän kentän arvo lasketaan alkamispäivämäärän ja läpimenoajan perusteella. Tavallisesti arvoa ei muokata suoraan. |
| Todellinen päättymispäivä | Käyttäjän on päivitettävä tämä kenttä mahdollisimman nopeasti tehtävän suorituksen jälkeen. Varsinainen läpimenoaika päivitetään sitten. |
| Arvioidut päivät | Arvioitu aika (päivinä), joka tarvitaan tehtävän loppuunsaattamiseksi. |
| Todelliset päivät | Todellinen aika (päivinä), joka tarvitaan tehtävän loppuunsaattamiseksi. |
| Seteli | Tämän kentän avulla voit lisätä muita huomautuksia ja tietoja tehtävästä. |

## <a name="information-and-settings-on-the-general-tab"></a>Yleiset-välilehden tiedot ja asetukset

**Yleiset**-välilehdessä näkyvät **Yhteenveto**-välilehdessä valitun etapin tiedot. Vaikka se toistaakin joitakin **Yhteenveto**-välilehdessä näkyviä tietoja, se sisältää myös lisätietoja valitusta etapista.
