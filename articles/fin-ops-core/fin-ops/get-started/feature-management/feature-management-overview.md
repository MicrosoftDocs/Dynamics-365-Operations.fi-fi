---
title: Ominaisuuksien hallinnan yleiskatsaus
description: Tässä ohjeaiheessa käsitellään ominaisuuksien hallintatoimintoa ja sen käyttöä.
author: mikefalkner
manager: AnnBe
ms.date: 09/12/2019
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
ms.openlocfilehash: a9be51c4a5cdadd968de160dc0b1406c95382eeb
ms.sourcegitcommit: 260a820038c29f712e8f1483cca9315b6dd3df55
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/08/2019
ms.locfileid: "2778702"
---
# <a name="feature-management-overview"></a>Ominaisuuksien hallinnan yleiskatsaus

[!include [banner](../../includes/banner.md)]

Ominaisuudet lisätään ja päivitetään jokaisessa versiossa. Ominaisuuksien hallintakokemus tarjoaa työtilan, jossa voit tarkastella kussakin julkaisussa toimitettujen ominaisuuksien luetteloa. Uudet asetukset ovat oletusarvoisesti poissa käytöstä. Työtilan avulla voit ottaa ne käyttöön ja tarkastella niiden dokumentaatiota.

## <a name="the-feature-management-workspace"></a>Ominaisuushallinnan työtila

Voit avata **Ominaisuuksien hallinnan** työtilan valitsemalla koontinäytön hallintapaneelista haluamasi ruudun. Näkyviin tulee sivu, joka sisältää kaikkien ominaisuuksien hallinnan tukemien versioiden ominaisuusluettelon. Ajan mittaan Microsoft parantaa ominaisuuksien hallintakokemusta, jotta se sisältää toimintoja, jotka helpottavat ominaisuuksien hallintaa.

Ominaisuusluettelossa on seuraavat tiedot:

- **Toiminnon nimi** – lisätyn ominaisuuden kuvaus.
- **Käytössä**-tila – Symboli ilmaisee, onko ominaisuus otettu käyttöön (valintamerkki), ei ole otettu käyttöön (tyhjä), on ajoitettu käyttöön (kello), on pakollisesti päällä (lukko), vaatii huomiota ennen kuin otat sen käyttöön (varoitus), tai ei voi ottaa käyttöön (X). Tässä näkyvää asetusta käytetään kaikilla yrityksillä. Huomaa, että vaikka ominaisuus olisi otettu käyttöön, se on edelleen tietoturvan hallinnassa. Tämän vuoksi ominaisuus on vain niiden käyttäjien käytettävissä, joilla on käyttöoikeus rooliinsa. Se on myös vain niiden yritysten käytettävissä, joihin käyttäjällä on käyttöoikeus.
- **Ota käyttöön päivämäärä** – Päivämäärä, jolloin toiminto on otettu käyttöön tai on ajoitettu käyttöön.
- **Ominaisuus lisätty** – toiminto lisättiin ympäristöön. Tämä päivämäärä syötetään automaattisesti, kun päivität ympäristöäsi kuukausittaisten julkaisujaksojen aikana.
- **Moduuli** – moduuli, johon uusi ominaisuus vaikuttaa.

Kun valitset toiminnon, lisätiedot näkyvät ominaisuusluettelon oikealla puolella olevassa tietoruudussa. Ruudun yläosassa näkyy toiminnon nimi, ominaisuuden lisäämisen päiväys, moduuli, johon ominaisuus vaikuttaa, ja **Lisä tietoja** -linkki. Valitse tämä linkki, jos haluat tarkastella toiminnon dokumentaatiota. Jos dokumentaatio ei ole käytettävissä, sinut viedään väliaikaiselle sivulle. Tieto ruudussa on myös **Kommentit**-kenttä, johon voit lisätä omia kommentteja ominaisuudesta.

**Ominaisuuksien hallinta** -työtilassa on myös useita välilehtiä, joissa kussakin on luettelo ominaisuuksista.

- **Uusi** - Tämä välilehti näyttää kaikki ominaisuudet, jotka on lisätty viimeisimmän kuukausittaisen päivityksen jälkeen. Jos olet ohittanut kaikki kuukausittaiset päivitykset, välilehdessä näkyvät kaikki uudet ominaisuudet, jotka on lisätty viimeisimmän päivityksen jälkeen. Uusimmat ominaisuudet näkyvät luettelon yläosassa. Uusien ominaisuuksien kokonaismäärä näkyy myös sivun yläosassa olevassa ruudussa.
- **Ei käytössä** – Tässä välilehdessä näkyvät kaikki ominaisuudet, joita ei ole otettu käyttöön. Uusimmat ominaisuudet näkyvät luettelon yläosassa. Sivun yläosassa olevassa ruudussa näkyy myös niiden uusien ominaisuuksien kokonaismäärä, joita ei ole otettu käyttöön.
- **Ajoitettu** – Tämä välilehti näyttää kaikki ominaisuudet, jotka on suunniteltu otettavaksi käyttöön tulevaisuudessa. Luettelon yläosaan tulee näkyviin ominaisuudet, joiden ajoituspäivämäärä on varhaisin. Uusien ominaisuuksien aikataulujen kokonaismäärä näkyy myös sivun yläosassa olevassa ruudussa.
- **Kaikki** – Tässä välilehdessä näkyvät kaikki ominaisuudet. Uusimmat ominaisuudet näkyvät luettelon yläosassa.

## <a name="turn-on-a-feature"></a>Toiminnon ottaminen käyttöön

Jos ominaisuus ei ole käytössä, tietoruudussa näkyy **Ota käyttöön nyt** -painike. Tämän painikkeen avulla voit ottaa toiminnon käyttöön.

- Valitse ominaisuus, jonka haluat ottaa käyttöön, ja valitse sitten tietoruudusta **Ota käyttöön nyt**. Toiminto on käytössä.

Joitakin toimintoja ei voi poistaa käytöstä sen jälkeen, kun ne on otettu käyttöön. Jos toimintoa, jota yrität ottaa käyttöön, ei voi poistaa käytöstä, näyttöön tulee varoitus. Tässä vaiheessa voit peruuttaa toiminnon valitsemalla **Peruuta** ja jättää toiminnon pois käytöstä. Jos kuitenkin valitset **Ota käyttöön** -toiminnon ja otat sen käyttöön, et voi poistaa sitä käytöstä myöhemmin.

Jotkin ominaisuudet näyttävät sanoman, jossa on lisätietoja, ennen kuin otat ne käyttöön. Nämä ominaisuudet on merkitty keltaisella varoitussymbolilla. Lue lisätiedot huolellisesti, jotta ymmärrät paremmin, mitä tapahtuu, kun ominaisuus on käytössä. Voit kuitenkin ottaa ominaisuuden käyttöön valitsemalla **Ota käyttöön**.

Jotkin ominaisuudet näyttävät sanoman, että toimintoa ei voi ottaa käyttöön, ennen kuin toimia on suoritettu. Nämä ominaisuudet on merkitty punaisella X-symbolilla. Sinun on toteutettava kuvauksessa kuvatut toimet, ennen kuin ominaisuus otetaan käyttöön. Jos et esimerkiksi pysty käyttämään ominaisuutta, ennen kuin konfigurointiavain on poistettu käytöstä, sinun on ensin poistettava määritysavain käytöstä ja palattava sitten ominaisuuksien hallintaan, jotta ominaisuus otetaan käyttöön.

Kun ominaisuus on otettu käyttöön, **Lisätietoja**-linkin alla tietoruudussa näkyy viesti. Tämä sanoma joko ilmaisee, että ominaisuus on otettu käyttöön tai ilmaisee päivämäärän, jolloin ominaisuus otetaan tulevaisuudessa käyttöön. Se tulee näkyviin aina, kun valitset ominaisuuden ominaisuusluettelosta.

Toiminnot, jotka on ajoitettu käyttöön tulevaisuudessa, näkyvät **Ajoitetut**-välilehdessä. Eräkäsittely ottaa ne käyttöön määritettynä päivänä keskiyöllä järjestelmän päivämäärän ilmaiseman aikavyöhykkeen mukaan.

## <a name="reschedule-a-feature"></a>Toiminnon ajoittaminen uudelleen

Jos ominaisuus on suunniteltu otettavaksi käyttöön tulevaisuudessa, tietoruudussa näkyy **Ajoita**-painike. Tämän painikkeen avulla voit muuttaa **Ota käyttöön päiväys** -arvon eri päiväksi.

1. Valitse ajoitettu ominaisuus uudelleenajoitettavaksi ja valitse sitten tietoruudusta **Ajoita**.
2. Määritä näyttöön tulevassa valintaikkunassa **Ota käyttöön päivämäärä** -kentässä uusi päivämäärä, jolloin toiminto otetaan käyttöön.
3. Valitse **Ota käyttöön** ajoittaaksesi toiminnon uudelleen tai **Poista käytöstä** peruuttaaksesi ajoituksen.

## <a name="turn-off-a-feature"></a>Toiminnon ottaminen pois käytöstä

Jos ominaisuus on jo käytössä, tietoruudussa näkyy **Poista käytöstä** -painike. Tämän painikkeen avulla voit ottaa toiminnon pois käytöstä. **Poista käytöstä** -painike ei ole käytettävissä, jos ominaisuutta ei voi poistaa käytöstä sen jälkeen, kun se on otettu käyttöön.

- Valitse käytöstä poistettava ominaisuus ja valitse sitten tietoruudusta **Poista käytöstä**. Toiminto on poistettu käytöstä ja **Ota käyttöön päivämäärä** -kenttä on tyhjennetty.

Kun ominaisuus on poistettu käytöstä, **Lisätietoja**-linkin alla tietoruudussa näkyy viesti. Tässä sanomassa todetaan, että ominaisuutta ei ole vielä otettu käyttöön. Se tulee näkyviin aina, kun valitset ominaisuuden ominaisuusluettelosta. Ominaisuudet, joita ei ole otettu käyttöön näkyvät **Ei käytössä** -välilehdessä.

## <a name="features-that-must-be-turned-on"></a>Ominaisuudet, jotka on otettava käyttöön

Joskus toimitetaan tärkeä toiminto, joka on otettava käyttöön automaattisesti päivityksen yhteydessä. Nämä toiminnot otetaan käyttöön automaattisesti **Ota käyttöön päivämäärä** -kentässä määritettynä päivänä. Näitä ominaisuuksia koskien tietoruudussa näkyy **Lisätietoja**-linkin alla viesti. Tämä sanoma joko ilmaisee, että ominaisuus on otettu käyttöön tai ilmaisee päivämäärän, jolloin ominaisuus otetaan käyttöön. Se tulee näkyviin aina, kun valitset ominaisuuden ominaisuusluettelosta.

## <a name="enable-all-features"></a>Ota käyttöön kaikki ominaisuudet

Oletusarvon mukaan kaikki ympäristöön lisätyt ominaisuudet poistetaan käytöstä. Voit ottaa käyttöön kaikki ominaisuudet valitsemalla **Ota kaikki käyttöön** -painikkeen. 

Kun valitset **Ota kaikki käyttöön**, näyttöön tulee vaihtoehto, jossa on annettava seuraavat tiedot:
- Luettelo kaikista ominaisuuksista, jotka edellyttävät vahvistusta, ennen kuin ne voidaan ottaa käyttöön. Jos haluat ottaa käyttöön luettelon ominaisuudet, valitse **Kyllä** **Ota käyttöön vahvistusta edellyttävät ominaisuudet** -painikkeessa.
- Näytetään luettelo kaikista ominaisuuksista, joita ei voi ottaa käyttöön. Nämä ominaisuudet eivät ole käytössä.

Kaikki toiminnot, jotka voidaan ottaa käyttöön, otetaan käyttöön. Jos ominaisuus on jo ajoitettu käyttöön tulevaisuudessa, aikataulu ei muutu. 

## <a name="turn-on-all-features-automatically"></a>Kaikkien toimintojen automaattinen käyttöönotto

Oletusarvon mukaan kaikki ympäristöön lisätyt ominaisuudet poistetaan käytöstä, elleivät ne ole pakollisia toimintoja. Jos kuitenkin haluat ottaa kaikki uudet ominaisuudet automaattisesti käyttöön, voit muuttaa uusien ominaisuuksien lisäämisen tietoja käyttämällä työtilan otsikon alla olevaa avattavaa luetteloa.

- Valitse **Ota uudet ominaisuudet automaattisesti käyttöön** ottaaksesi automaattisesti käyttöön kaikki uudet ominaisuudet, kun ne lisätään omaan ympäristöön.
- Valitse **Älä ota uusia ominaisuuksia automaattisesti käyttöön** ottaaksesi automaattisesti pois käytöstä kaikki uudet ominaisuudet, kun ne lisätään omaan ympäristöön.


Kun otat kaikki ominaisuudet käyttöön automaattisesti, se ottaa käyttöön kaikki ominaisuudet, jotka olisivat käytössä, kun napsautat **Ota kaikki käyttöön**-painiketta. Se ei ota käyttöön vahvistusta edellyttäviä ominaisuuksia tai ominaisuuksia, joita ei voi ottaa käyttöön, ennen kuin toimia on suoritettu.

## <a name="check-for-updates"></a>Tarkista päivitysten saatavuus

Ominaisuudet lisätään ympäristöösi jokaisen päivityksen jälkeen. Voit kuitenkin tarkistaa päivitykset manuaalisesti napsauttamalla **Tarkista päivitykset** -painiketta. Mikä tahansa ominaisuus, joka lisättiin järjestelmään päivityksen jälkeen, lisätään ominaisuuksien luetteloon. Jos esimerkiksi ominaisuus on otettu käyttöön julkaisun jälkeen, voit tarkistaa päivitykset ja ominaisuus lisätään luetteloon.

## <a name="assigning-roles"></a>Määrittää rooleja

Järjestelmän ylläpitäjät voivat avata **Ominaisuuksien hallinta** -työtilan, ja käyttäjät, jotka on määritetty ominaisuuksien hallinnan käyttökokemusta tukeville ominaisuuksien hallinta- tai ominaisuuskatseluohjelman rooleille. Nämä kaksi roolia on luotu tukemaan ominaisuuksien hallinnan käyttökokemusta. Ominaisuuksien hallinta -roolin käyttäjät voivat ottaa minkä tahansa ominaisuuden käyttöön tai poistaa sen käytöstä. He voivat myös päivittää ominaisuuden **Kommentti**-kentän. Ominaisuuksien katseluohjelma -roolin käyttäjät voivat tarkastella vain **Ominaisuuksien hallinta** -työtilaa. He eivät voi ottaa toimintoja käyttöön tai poistaa niitä käytöstä.

Ominaisuuksien hallinnan roolin ja toiminnon katseluohjelman rooli eivät ohita käyttäjän aiemmin luotua suojausta. Ne vain määrittävät, voiko käyttäjä ottaa ominaisuudet käyttöön ja poistaa ne käytöstä. Ne eivät anna pääsyä itse ominaisuuksiin.

## <a name="features-that-use-configuration-keys"></a>Konfigurointiavaimia käyttävät toiminnot

Jos ominaisuus käyttää määritysavainta, mutta määritysavain ei ole käytössä, **Ominaisuuksien hallinnan** työtila ei näytä ominaisuutta käytettävissä olevien ominaisuuksien luettelossa. Kun olet määrittänyt määritysavaimen, sinun on päivitettävä ominaisuusluettelo käyttämällä **Tarkista päivitys** -valikon vaihtoehtoa. Ominaisuus näkyy ominaisuusluettelossa.

Jos poistat määritysavaimen käytöstä, ominaisuutta ei poisteta ominaisuusluettelosta.

## <a name="data-entities"></a>Tietoyksiköt

**Ominaisuuksien hallinta** -tietoyksikön avulla voit viedä ominaisuuksien hallinta-asetukset yhdestä ympäristöstä ja tuoda ne sitten toiseen ympäristöön. Tämä yksikkö päivittää vain aiemmin luodut ominaisuudet. Kohteen liiketoimintalogiikan avulla voidaan myös varmistaa, että samoja sääntöjä käytetään **Ominaisuuksien hallinta** -työtilassa, kun tuonti suoritetaan. Et voi esimerkiksi ohittaa pakollista ominaisuusasetusta poistamalla päivämäärän tuonnin aikana.

Seuraavissa esimerkeissä kuvataan, mitä tapahtuu, kun tietojen tuomiseen käytetään **Ominaisuuksien hallinta** -yksikköä.

- Jos **Käytössä**-kentän arvoksi vaihdetaan **Kyllä**, toiminto on käytössä ja **Ota käyttöön päivämäärä** -kentän arvoksi määritetään kuluva päivämäärä.
- Jos **Käytössä**-kentän arvoksi vaihdetaan **Ei** tai jätetään **EnableDate**-kenttä tyhjäksi, ominaisuus on poissa käytöstä ja **Ota käyttöön päivämäärä** -kenttä tyhjä. Et voi poistaa pakollista ominaisuutta tai ominaisuutta, jota ei voi poistaa käytöstä sen jälkeen, kun se on otettu käyttöön.
- Jos muutat **EnableDate**-kentän arvon tulevaksi päiväksi, toiminto ajoitetaan kyseisenä päivänä.
- Jos **Käytössä**-kentän arvoksi vaihdetaan **Kyllä**, ja **EnableDate**-kentän arvoksi määritetään tuleva päivämäärä, ominaisuus ajastetaan tuolle päivämäärälle. 
- Jos **Käytössä**-kentän arvoksi vaihdetaan **Ei**, mutta samalla **EnableDate**-kentän arvo muutetaan tulevaksi päivämääräksi, ominaisuus ajastetaan tuolle päivämäärälle.
- Jos toiminto on käytössä ja lisäät **EnableDate**-kentän, joka on määritetty tulevaan päivään, toiminto pysyy käytössä. Jos haluat ajoittaa toiminnon uudelleen, sinun on muutettava **Käytössä** -kentän arvoksi **Ei**.

## <a name="feature-management-and-flighting"></a>Ominaisuuksien hallinta ja väliversiotestaus

Ominaisuuksien hallinnan avulla voit hallita kuhunkin julkaisuun toimitettuja ominaisuuksia. Väliversiotestaus-toiminnon avulla Microsoft Teamsit voivat vapauttaa toimintoja rajoitetulle määrälle asiakkaita, jotta näitä ominaisuuksia voidaan testata ja vahvistaa ilman, että se vaikuttaa kaikkiin asiakkaisiin. Ominaisuuksien hallinta ei hallitse minkään ominaisuuden väliversiotestaus-ominaisuutta.

## <a name="using-feature-management-to-turn-on-isv-features-or-custom-features"></a>ISV-ominaisuuksien tai mukautettujen ominaisuuksien ottaminen käyttöön ominaisuuksien hallinnan avulla

Ominaisuuksien hallinta ei ole tällä hetkellä käytettävissä itsenäisten ohjelmistotoimittajien (ISV) ja mukautettujen ominaisuuksien ominaisuuksista. Microsoft kuitenkin lisää toimintoja, jotka parantavat ominaisuuksien hallintaa. Kun nämä parannukset on tehty, Microsoft tekee ominaisuuksien hallinnan käytettäväksi kaikille toiminnoille ja antaa ohjeita toimintojen päivittämiseksi käyttöä varten.
