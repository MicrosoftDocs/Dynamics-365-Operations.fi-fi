---
title: Aiheutunut kustannus -moduuli
description: Aiheutunut kustannus -moduulin avulla yritykset voivat tehostaa saapuvien lähetysten toimintoja antamalla käyttäjille tuodun rahdin täydellisen taloudellisen ja logistisen hallinnan valmistajalta varastoon.
author: sherry-zheng
manager: tfehr
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 9d04c377080a1d301efb771b98c249f610a3289d
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500329"
---
# <a name="landed-cost-module"></a>Aiheutunut kustannus -moduuli

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

**Aiheutunut kustannus** -moduulin avulla yritykset voivat tehostaa saapuvien lähetysten toimintoja antamalla käyttäjille tuodun rahdin täydellisen taloudellisen ja logistisen hallinnan valmistajalta varastoon. Tuotujen tuotteiden osalta aiheutuneet kustannukset voivat olla 40 prosenttia tai enemmän kunkin tuodun nimikkeen kokonaiskustannuksista. Sen vuoksi haasteena on tehdä tarkat arviot aiheutuneista kustannuksista.

Yritykset voivat käyttää aiheutunutta kustannusta seuraavien tehtävien suorittamiseen:

- Aiheutuneiden kustannusten arviointi merikuljetuksen luontihetkellä.
- Aiheutuneet kustannukset voidaan jakaa useisiin nimikkeisiin ja ostotilauksiin tai siirtotilauksiin yhdessä merikuljetuksessa.
- Tukemaan tavaroiden siirtoa fyysisten sijaintien välillä tunnustamalla aiheutuneet kustannukset.
- Kuljetettaviin tavaroihin liittyvien jaksotusten tunnistaminen.

Aiheutuneet kustannukset antavat tarkat ja ajantasaiset aiheutuneiden kustannusten yleiskustannusarviot. Samalla se lisää taloudellista ja logistista näkyvyyttä laajennettuun toimitusketjuun. Se helpottaa myös kustannuslaskennan ja kustannuslaskentavirheiden hallintaa.

## <a name="highlights"></a>Kohokohdat

### <a name="voyages"></a>Matkat

Aiheutuneissa kustannuksissa merikuljetus on tietty liike lähtevästä sijainnista tiettyjen kohteiden kautta tietyltä ajanjaksolta määritettyyn saapuvien varastosijaintiin. Ostotilaukset ja tilausrivit voidaan lisätä joko yhteen konttiin tai useaan konttiin merikuljetuksessa, ja kustannukset kohdistetaan taksisin nimikeriville oikein. Tilaukset ja tilausrivit voidaan myös lisätä eri yrityksille yhden merimatkan kohdalla.

### <a name="item-ownership"></a>Nimikkeen omistus

Microsoft Dynamics 365 Supply Chain Managementissa tavarat vastaanotetaan yleensä varaston kohteeseen ja sitten laskutetaan. Useimpien kansainvälisten kauppasopimusten mukaan yritys kuitenkin ottaa tavaroiden omistajuuden siitä lähtien, kun ne poistuvat alkuperäisestä satamasta, ennen kuin ne on vastaanotettu fyysisesti. Aiheutuneet kustannukset mahdollistavat yritysten laskuttaa tuotteita ennen tuotteiden fyysistä vastaanottamista. Tätä käsitettä kutsutaan kuljetettavien tuotteiden tilaukseksi. Se luo uudentyyppisen tilauksen, jolla hallitaan tavaroiden vastaanottoa sen jälkeen, kun alkuperäinen ostotilaus on laskutettu.

### <a name="costs"></a>Kustannukset

Kun luot merikuljetuksen aiheutuneissa kustannuksissa, kustannukset voidaan lisätä siihen automaattisesti. Nämä kustannukset määritetään aiheutuneissa kustannuksissa, ja niihin voi käyttää useita kustannusvaihtoehtoja ja kustannusperusteita. Kukin kustannus voidaan määrittää eri merikuljetuksen tasoille ja jakaa nimiketasolle jakamissääntöjen kautta, jotka tukevat määrää, tilavuutta, painoa, summaa ja määritettyjä tilavuusjakajia. Nämä arvioidut kustannukset antavat tarkan arvion merikuljetuksen kaikista kustannuksista.

Sen jälkeen arvioidut aiheutuneet kustannukset kirjataan alustavasti tai jaksotetaan. Näin voidaan varmistaa, että arvioidut kustannukset lasketaan tarkasti, kun merikuljetusta luodaan. Koska nämä automaattiset kustannukset laskutetaan, arvioidut kustannukset peruutetaan ja korvataan toteutuneilla kustannuksilla kustannuslaskujen perusteella.

Todelliset kustannukset ovat kustannusten laskutuksen aikana kirjattuja käänteisiä aiheutuneita kustannuksia käyttämällä selvitystilejä, jotka on määritetty kullekin kustannustyypille (esimerkiksi verot, rahti ja vakuutus). Kirjaukset noudattavat tiettyyn nimikkeeseen liittyvää kirjaustapaa. Ne päivittävät automaattisesti varastokirjauksen riippumatta siitä, onko kirjaustyyppi FIFO, LIFO, liukuva painotettu keskiarvo vai liukuva keskiarvo. Kaikkia varastomalliryhmän kirjaustyyppejä tuetaan. Liukuvassa keskiarvossa ja standardikustannusten kirjauksen yhteydessä voidaan kirjata ostohinnan varianssitilit arvioitujen kustannusten ja toteutuneiden kustannusten erojen kirjaamista varten.

### <a name="item-and-order-tracking"></a>Nimikkeiden ja tilausten seuranta

Kun merikuljetus siirtyy alkuperäisestä lähtösijainnista lopulliseen kohdevarastoon, käyttäjät voivat tarvittaessa päivittää matkan kunkin vaiheen tai *etapin*. Jokaisen etapin läpimenoaika sekä lähetyksen tila tunnistetaan. Lisäksi tunnistetaan vahvistetut toimituspäivät siirtymisessä matkan seuraavaan etappiin. Yhdessä nämä toimituspäivät antavat tavaroiden arvioidun toimituspäivän saapuvien varastoon. Käyttäjät voivat muuttaa näitä toimituspäiviä. Tällöin tavaroiden arvioitu toimituspäivä päivitetään automaattisesti matkan läpimenoaikojen ja etappien mukaan. Näkyvyys kuljetettaviin tuotteisiin merimatkan ja aluksen mukaan on saatavissa konttikohtaisesti ennen tuotteiden vastaanottamista. Koska päivämäärät päivitetään jokaisella ostotilausrivillä, yrityksillä on parempi logistiikan ja varastosuunnittelun hallinta.

## <a name="landed-cost-concepts"></a>Aiheutuneiden kustannusten käsitteet

Seuraavassa taulukossa on yhteenveto joistakin aiheutuneiden kustannusten peruskäsitteistä.

| Konsepti | kuvaus |
|---|---|
| Matka | Tavallisesti merikuljetus on yksi alus. Käytäntöjen ja menettelyiden mukaan se voi kuitenkin olla yksi toimittaja tai yksi ostotilaus. Tämän käsitteen käytöstä ei ole rajoituksia. |
| Lasku | Pakkaus määräytyy usein tullisäännösten mukaan. Se voi koostua yhden toimittajan tuotteista yhdelle yksikölle tai yritykselle lähetystä kohden. Pakkauksen tuotteet voivat olla yhdessä kontissa tai jakautuneet useisiin kontteihin. |
| Lähetyskontti | Kuljetuskonttien myymälän ostotilausrivit. Ne ovat lähetystason alapuolella oleva taso. Niitä käytetään yleensä silloin, kun kustannukset on jaettu tuotteisiin konttia kohden tai kun vastaanotto tapahtuu konttia kohden. |
| Lähetyskontin tyyppi | Kuljetuskonttityypit voivat määrittää kustannustyypin (esimerkiksi rahdin) hinnan. Niissä on myös hyödyllisiä lähetystietoja. |
| Kustannustyyppi | Kustannustyypit yksilöivät tuontiin liittyvät kustannukset, kuten verot, rahtikulut ja vakuutuskustannukset. |
| Automaattinen kustannus | Automaattiset kustannukset toimivat kuten kauppasopimukset. Automaattinen kustannus linkitetään merikuljetuksen tasoon. |
| Portti | Satamat ovat alueita, joilla tavaroita vastaanotetaan ja siirretään. |
| Alus | Alus on väline, jolla kuljetetaan tavaroita, kuten laiva tai lentokone. |
| Matkalla olevat tavarat | Asetusten mukaan tavarat laitetaan kuljetuksessa-varastoon laskun päivittämisen jälkeen. |
| Tehtävä | Toimintoja voidaan käyttää tallentamaan matkan jokainen tärkeä vaihe kahden sataman välillä. Niiden avulla voidaan päivittää päivämääriä. |
| Matkamalli | Matkamallit ovat reittejä, joilla tuotteet kulkevat kahden sataman välillä. |

Lisätietoja **Aiheutunut kustannus**- ja **Kuljetustenhallinta** (TMS) -moduulien välisten termien ja ominaisuuksien vertailusta on kohdassa [Aiheutunut kustannus vs. kuljetustenhallinta](landed-cost-vs-tms.md).
