---
title: Ominaisuuksien hallinnan yleiskatsaus
description: Tässä ohjeaiheessa käsitellään ominaisuuksien hallintatoimintoa ja sen käyttöä.
author: mikefalkner
manager: AnnBe
ms.date: 04/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: IT Pro, Application user
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: 10.0.2
ms.openlocfilehash: e75e42926db22d4fccda86c755b12d9d121a9c0e
ms.sourcegitcommit: be447fc81bc874982bc0185fcb4d87d99bd742c5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/08/2019
ms.locfileid: "1538685"
---
# <a name="feature-management-overview"></a>Ominaisuuksien hallinnan yleiskatsaus

[!include[banner](../../includes/banner.md)]
[!include [banner](../../includes/preview-banner.md)]

Ominaisuudet lisätään ja päivitetään jokaisessa Microsoft Dynamics 365 for Finance and Operations -versiossa. Ominaisuuksien hallintakokemus tarjoaa työtilan, jossa voit tarkastella kussakin julkaisussa toimitettujen ominaisuuksien luetteloa. Uudet asetukset ovat oletusarvoisesti poissa käytöstä. Työtilan avulla voit ottaa ne käyttöön ja tarkastella niiden dokumentaatiota.

## <a name="the-feature-management-workspace"></a>Ominaisuushallinnan työtila

Voit avata **Ominaisuuksien hallinnan** työtilan valitsemalla koontinäytön hallintapaneelista haluamasi ruudun. Näkyviin tulee sivu, joka sisältää kaikkien ominaisuuksien hallinnan tukemien versioiden ominaisuusluettelon. Ajan mittaan Microsoft parantaa ominaisuuksien hallintakokemusta, jotta se sisältää toimintoja, jotka helpottavat ominaisuuksien hallintaa.

Ominaisuusluettelossa on seuraavat tiedot:

- **Toiminnon nimi** – lisätyn ominaisuuden kuvaus.
- **Käytössä oleva tila** – symboli ilmaisee, onko toiminto otettu käyttöön (valintamerkki), ei ole käytössä (tyhjä), on ajoitettu käyttöön (kello) tai pakollinen käytössä (lukitus). Tässä näkyvää asetusta käytetään kaikilla yrityksillä. Huomaa, että vaikka ominaisuus olisi otettu käyttöön, se on edelleen tietoturvan hallinnassa. Tämän vuoksi ominaisuus on vain niiden käyttäjien käytettävissä, joilla on käyttöoikeus rooliinsa. Se on myös vain niiden yritysten käytettävissä, joihin käyttäjällä on käyttöoikeus.
- **Käyttöönottopäivä** – päivämäärä, jolloin toiminto on otettu käyttöön tai otetaan käyttöön, jos päiväys on tuleva päivämäärä.
- **Ominaisuus lisätty** – toiminto lisättiin ympäristöön. Tämä päivämäärä syötetään automaattisesti, kun päivität ympäristöäsi kuukausittaisten julkaisujaksojen aikana.
- **Moduuli** – moduuli, johon uusi ominaisuus vaikuttaa.

Kun valitset toiminnon, lisätiedot näkyvät ominaisuusluettelon oikealla puolella olevassa tietoruudussa. Ruudun yläosassa näkyy toiminnon nimi, ominaisuuden lisäämisen päiväys, moduuli, johon ominaisuus vaikuttaa, ja **Lisä tietoja** -linkki. Valitse tämä linkki, jos haluat tarkastella toiminnon dokumentaatiota. Jos dokumentaatio ei ole käytettävissä, sinut viedään väliaikaiselle sivulle. Tieto ruudussa on myös **Kommentit**-kenttä, johon voit lisätä omia kommentteja ominaisuudesta.

**Ominaisuuksien hallinta** -työtilassa on myös useita välilehtiä, joissa on luettelon ominaisuuksista. 
- **Uusi** - Näyttää kaikki ominaisuudet, jotka on lisätty viimeisimmän kuukausittaisen päivityksen jälkeen. Jos olet ohittanut kaikki kuukausittaiset päivitykset, se sisältää kaikki uudet ominaisuudet edellisen päivityskerran jälkeen. Uusimmat ominaisuudet näkyvät luettelon yläosassa. Uusien ominaisuuksien kokonaismäärä näkyy myös sivun yläosassa olevassa ruudussa.
- **Ei käytössä** - Näyttää kaikki ominaisuudet, joita ei ole otettu käyttöön. Uusimmat ominaisuudet näkyvät luettelon yläosassa. Uusien ominaisuuksien kokonaismäärä näkyy myös sivun yläosassa olevassa ruudussa.
- **Ajoitettu** - Näyttää kaikki ominaisuudet, jotka on suunniteltu otettavaksi käyttöön tulevana päivänä. Luettelon yläosaan tulee näkyviin ominaisuudet, joiden ajoituspäivämäärä on varhaisin. Uusien ominaisuuksien kokonaismäärä näkyy myös sivun yläosassa olevassa ruudussa.
- **All** - Näyttää kaikki ominaisuudet. Uusimmat ominaisuudet näkyvät luettelon yläosassa.


## <a name="enable-a-feature"></a>Ota ominaisuus käyttöön

Jos ominaisuutta ei ole otettu käyttöön, tietoruudussa näkyy **Ota käyttöön** -painike. Tämän painikkeen avulla voit ottaa toiminnon käyttöön.

1. Valitse ominaisuus, jonka haluat ottaa käyttöön, ja valitse sitten tieto ruudusta **Ota käyttöön**.
2. Näyttöön tulee liukusäädin, jossa voit määrittää, milloin toiminto otetaan käyttöön. Oletusarvoisesti tämä päivämäärä on nykyinen päivämäärä.
3. Ota ominaisuus käyttöön valitsemalla **Ota käyttöön**.

Joitakin toimintoja ei voi poistaa käytöstä sen jälkeen, kun ne on otettu käyttöön. Jos toimintoa, jota yrität ottaa käyttöön, ei voi poistaa käytöstä, näyttöön tulee varoitus. Tässä vaiheessa voit peruuttaa toiminnon valitsemalla **Peruuta** ja jättää toiminnon pois käytöstä. Jos kuitenkin valitset **Ota käyttöön** -toiminnon ja otat sen käyttöön, et voi poistaa sitä käytöstä myöhemmin.

Kun ominaisuus on otettu käyttöön, **Lisätietoja**-linkin alla tietoruudussa näkyy viesti. Tämä sanoma ilmaisee, että ominaisuus on otettu käyttöön tai että ominaisuus otetaan käyttöön tulevaisuudessa. Jos käytät tulevaa päivää, ominaisuus tulee näkyviin **Ajoitettuun** luetteloon. Tämä sanoma tulee näkyviin aina, kun valitset ominaisuuden ominaisuusluettelosta. Tulevaisuudessa ajoitetut ominaisuudet otetaan käyttöön keskiyöllä järjestelmäpäivämäärän ilmaiseman aikavyöhykkeen mukaisessa eräprosessissa. 

## <a name="reschedule-a-feature"></a>Toiminnon ajoittaminen uudelleen

Jos ominaisuus on otettu käyttöön tulevaisuudessa, tietoruudussa näkyy **Ajoita uudelleen** -painike. Tämän painikkeen avulla voit muuttaa **Ota käyttöön päiväys** -arvon eri päiväksi.

1. Valitse ajoitettu ominaisuus, jonka haluat ajoittaa uudelleen ja valitse sitten tieto ruudusta **Ajoita uudelleen**.
2. Näyttöön tulee liukusäädin, jossa voit määrittää, milloin toiminto otetaan käyttöön. 
3. Valitse **Ota käyttöön** ajoittaaksesi toiminnon uudelleen tai **Poista käytöstä** peruuttaaksesi ajoituksen.

## <a name="disable-a-feature"></a>Poista ominaisuus käytöstä

Jos ominaisuutta on jo otettu käyttöön, tietoruudussa näkyy **Poista käytöstä** -painike. Tämän painikkeen avulla voit poistaa toiminnon käytöstä. **Poista käytöstä** -painike ei ole käytettävissä, jos ominaisuutta ei voi poistaa käytöstä sen jälkeen, kun se on otettu käyttöön.

- Valitse ominaisuus, jonka haluat poistaa käytöstä, ja valitse sitten tietoruudusta **Poista käytöstä**.

- Toiminto on poistettu käytöstä, ja sen valinta poistetaan.

Kun ominaisuus on poistettu käytöstä, **Lisätietoja**-linkin alla tietoruudussa näkyy viesti. Tämä sanoma ilmaisee, että ominaisuutta ei ole vielä otettu käyttöön ja se näkyy **Ei käytössä** -luettelossa. Sanoma tulee näkyviin aina, kun valitset ominaisuuden ominaisuusluettelosta.

## <a name="features-that-must-be-enabled"></a>Ominaisuudet, jotka on otettava käyttöön

Voit toimittaa tärkeän toiminnon, joka on otettava käyttöön automaattisesti päivityksen yhteydessä. Se otetaan käyttöön automaattisesti järjestelmän **Käyttöönottopäivänä**. Tietoruudun **Lisätietoja**-linkin alapuolelle tulee näkyviin sanoma. Tämä sanoma ilmoittaa, että ominaisuus on otettu käyttöön tai otetaan käyttöön automaattisesti-järjestelmän **Käyttöönottopäivänä**. Se tulee näkyviin aina, kun valitset ominaisuuden ominaisuusluettelosta.

## <a name="assigning-roles"></a>Määrittää rooleja

Järjestelmän ylläpitäjät voivat avata **Ominaisuuksien hallinta** -työtilan, ja käyttäjät, jotka on määritetty ominaisuuksien hallinnan käyttökokemusta tukeville ominaisuuksien hallinta- tai ominaisuuskatseluohjelman rooleille, jotka on luotu tukemaan Ominaisuuksien hallinta -kokemusta. Ominaisuuksien hallinta -roolin käyttäjät voivat ottaa minkä tahansa ominaisuuden käyttöön tai poistaa sen käytöstä. He voivat myös päivittää ominaisuuden kommenttiosan. Ominaisuuksien katseluohjelma -roolin käyttäjät voivat tarkastella vain **Ominaisuuksien hallinta** -työtilaa. He eivät voi ottaa toimintoja käyttöön tai poistaa niitä käytöstä.

Ominaisuuksien hallinnan roolin ja toiminnon katseluohjelman rooli eivät ohita käyttäjän aiemmin luotua suojausta. Roolit määrittävät vain käyttöoikeudet, jotka mahdollistavat ominaisuuksien käytön. Se ei anna pääsyä itse ominaisuuksiin.

## <a name="using-feature-management-to-enable-isv-features-or-custom-features"></a>ISV-ominaisuuksien tai mukautettujen ominaisuuksien ottaminen käyttöön ominaisuuksien hallinnan avulla

Ominaisuuksien hallintaprosessi ei ole tällä hetkellä käytettävissä ISV-ominaisuuksien tai mukautettujen ominaisuuksien osalta. Lisäämme lisätoimintoja, jotka parantavat ominaisuuksien hallintaa, ja kun nämä parannukset ovat valmiit, avaamme ominaisuuksien hallinnan kaikille ominaisuuksille ja annamme tarkat ohjeet siitä, miten voit päivittää toiminnon käyttämään sitä.

## <a name="feature-management-and-flighting"></a>Ominaisuuksien hallinta ja väliversiotestaus

Ominaisuuksien hallinnan avulla voit hallita kuhunkin julkaisuun toimitettuja ominaisuuksia. Väliversiotestaus-toiminnon avulla Microsoft Teamsit voivat vapauttaa toimintoja rajoitetulle määrälle asiakkaita, jotta ominaisuudet voidaan testata ja vahvistaa ilman, että se vaikuttaa kaikkiin asiakkaisiin. Ominaisuuksien hallinta ei hallitse minkään ominaisuuden väliversiotestaus-ominaisuutta.
