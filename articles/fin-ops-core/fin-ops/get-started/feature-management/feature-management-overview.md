---
title: Ominaisuuksien hallinnan yleiskatsaus
description: Tässä ohjeaiheessa käsitellään ominaisuuksien hallintatoimintoa ja sen käyttöä.
author: Peakerbl
ms.date: 01/10/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: IT Pro, Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: 10.0.2
ms.openlocfilehash: c98bdbd64ee5488da20de3f5b23ae18ebce8c23f
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/31/2022
ms.locfileid: "8068006"
---
# <a name="feature-management-overview"></a>Ominaisuuksien hallinnan yleiskatsaus

[!include [banner](../../includes/banner.md)]


[!INCLUDE [PEAP](../../../../includes/peap-1.md)]

Ominaisuudet lisätään ja päivitetään jokaisessa versiossa. Ominaisuuksien hallintakokemus tarjoaa työtilan, jossa voit tarkastella kussakin julkaisussa toimitettujen ominaisuuksien luetteloa. Työtilassa voi sitten tarkastelle ominaisuuden ohjeita sekä ottaa ominaisuuksia käyttöön tai poistaa niitä käytöstä.

## <a name="the-feature-management-workspace"></a>Ominaisuushallinnan työtila

Voit avata **Ominaisuuksien hallinnan** työtilan valitsemalla koontinäytön hallintapaneelista haluamasi ruudun. Näkyviin tulee sivu, joka sisältää kaikkien ominaisuuksien hallinnan tukemien versioiden ominaisuusluettelon. 

Ominaisuusluettelossa on seuraavat tiedot:

- **Toiminnon nimi** – lisätyn ominaisuuden kuvaus.
- **Tila** – Symboli ilmaisee, onko ominaisuus otettu käyttöön (valintamerkki), poistettu käytöstä (tyhjä), aikataulutettu käyttöönotettavaksi (kello) tai onko se pakollinen (lukko), onko siinä tehtävä jotakin ennen käyttöönottoa (varoitussymboli) tai eikä sitä voi ottaa käyttöön (X). Tässä näkyvää asetusta käytetään kaikilla yrityksillä. Huomaa, että vaikka ominaisuus olisi otettu käyttöön, se on edelleen tietoturvan hallinnassa. Tämän vuoksi ne käyttäjät voivat käyttää ominaisuutta, joiden käyttöoikeusrooli sallii ominaisuuden käytön. Se on myös vain niiden yritysten käytettävissä, joihin käyttäjällä on käyttöoikeus.
- **Ota käyttöön päivämäärä** – Päivämäärä, jolloin toiminto on otettu käyttöön tai on ajoitettu käyttöön.
- **Ominaisuus lisätty** – toiminto lisättiin ympäristöön. Tämä päivämäärä syötetään automaattisesti, kun päivität ympäristöäsi kuukausittaisten julkaisujaksojen aikana.
- **Ominaisuuden tila** – Ominaisuuden elinkaaren nykyinen tila: **esiversio**, **julkaistu** (näkyy tyhjänä), **käytössä oletusarvoisesti** ja **pakollinen**. Tiloja käsitellään enemmän jäljempänä tässä aiheessa. 
- **Moduuli** – moduuli, johon uusi ominaisuus vaikuttaa.

> [!NOTE]
> **Ominaisuuden tila** -sarake on ollut käytössä versiosta 10.0.21 alkaen.

Kun valitset toiminnon, lisätiedot näkyvät toimintoluettelon oikealla puolella olevassa tietoruudussa. Ruudun yläosassa näkyy toiminnon nimi, ominaisuuden lisäämisen päiväys, moduuli, johon ominaisuus vaikuttaa, ja **Lisä tietoja** -linkki. Valitse tämä linkki, jos haluat tarkastella toiminnon dokumentaatiota. Jos dokumentaatio ei ole käytettävissä, sinut viedään väliaikaiselle sivulle. Tieto ruudussa on myös **Kommentit**-kenttä, johon voit lisätä omia kommentteja ominaisuudesta.

**Ominaisuuksien hallinta** -työtilassa on myös useita välilehtiä, joissa kussakin on luettelo ominaisuuksista.

- **Uusi** - Tämä välilehti näyttää kaikki ominaisuudet, jotka on lisätty viimeisimmän kuukausittaisen päivityksen jälkeen. Jos olet ohittanut kaikki kuukausittaiset päivitykset, välilehdessä näkyvät kaikki uudet ominaisuudet, jotka on lisätty viimeisimmän päivityksen jälkeen. Uusimmat ominaisuudet näkyvät luettelon yläosassa. Uusien ominaisuuksien kokonaismäärä näkyy myös sivun yläosassa olevassa ruudussa.
- **Ei käytössä** – Tässä välilehdessä näkyvät kaikki ominaisuudet, joita ei ole otettu käyttöön. Uusimmat ominaisuudet näkyvät luettelon yläosassa. Lisäksi sivun yläosassa on ruutu, jossa näkyy tällä hetkellä käytöstäpoistettujen uusien ominaisuuksien kokonaismäärä.
- **Ajoitettu** – Tämä välilehti näyttää kaikki ominaisuudet, jotka on suunniteltu otettavaksi käyttöön tulevaisuudessa. Luettelon yläosaan tulee näkyviin ominaisuudet, joiden ajoituspäivämäärä on varhaisin. Sivun yläosassa olevassa ruudussa on lisäksi aikataulutettujen ominaisuuksien kokonaismäärä.
- **Kaikki** – Tässä välilehdessä näkyvät kaikki ominaisuudet. Uusimmat ominaisuudet näkyvät luettelon yläosassa.

## <a name="feature-states"></a>Ominaisuuden tilat
Ominaisuudet voivat siirtyä tilasta alkaen siitä, kun ne otetaan ensimmäisen kerran käyttöön ominaisuuksien hallinnassa, ja päättyen siihen, että ominaisuus muuttuu tuotteessa pakolliseksi. Tässä osassa käsitellään ominaisuuden hyväksyttyjä tiloja.

### <a name="preview-features-optional"></a>Esiversio-ominaisuudet (valinnainen)

Tuotetiimit voivat päättää aloittaa uuden ominaisuuden käytön esiversio-ominaisuutena. Esiversio-ominaisuuksia ei oteta oletusarvoisesti käyttöön, ja ne ovat valinnaisia. Ominaisuudet omistava tuotetiimi voi päivittää ominaisuudet julkaistaviksi sen jälkeen, kun onnistunut esiversiojakso on päättynyt.

> [!NOTE]
> Esiversio-ominaisuuksia koskevat erityiset esiversion [käyttöehdot](https://go.microsoft.com/fwlink/?linkid=2105274). 

### <a name="released-features-optional"></a>Julkaistut ominaisuudet (valinnainen)

Näiden ominaisuuksien **Ominaisuuden tila** -sarake on tyhjä. Ominaisuuksia, jotka lisätään alun perin julkaistuina, ei oteta oletusarvoisesti käyttöön, ja niiden käyttöönottaminen on valinnaista. Esiversiosta päivitettyjen ominaisuuksien käyttöönottotila pysyy ennallaan.

### <a name="on-by-default-features-optional"></a>Oletusarvoisesti käyttöönotetut ominaisuudet (valinnainen)

Vaikka **oletusarvoisesti käyttöönotetuiksi** päivitetyt ominaisuudet otetaan oletusarvoisesti käyttöön, ne voidaan poistaa käytöstä. Kun ominaisuudet, jotka voidaan poistaa käytöstä, ovat olleet **Julkaistu**-tilassa vähintään kuusi kuukautta, niiden odotetaan siirtyvän tähän tilaa seuraavassa pääversion julkaisussa. Oletuksena on, että **Oletusarvoisesti käyttöönotettu**-tilaan siirtyvistä ominaisuuksista ilmoitetaan julkaisun aiheessa [Uudet ominaisuudet](../whats-new-changed.md). Ominaisuuden omistava tuotetiimi käynnistää päivityksen.

> [!NOTE]
> Koska nämä ominaisuudet otetaan automaattisesti käyttöön, on tärkeää selvittää, onko organisaatio valmis ottamaan nämä ominaisuudet käyttöön vai tarvitaanko vielä lisäaikaa. Jos lisäaikaa tarvitaan, nämä ominaisuudet on ehkä poistettava tilapäisesti käytöstä. Kannattaa muistaa, että ominaisuuden siirtyminen **Oletusarvoisesti käyttöönotettu** -tilaan tapahtuu yleensä pääversion julkaisussa, ennen kuin ominaisuudesta on tarkoitus tulla **pakollinen**. Sen jälkeen ominaisuutta ei voi enää poistaa käytöstä. 

### <a name="mandatory"></a>Pakollinen

**Pakollinen** on ominaisuuksien odotettu viimeinen tila. Se ilmaisee, että ominaisuudet on otettu käyttöön ja ettei niitä voi poistaa käytöstä muutoin kuin ottamalla yhteyttä Microsoftiin. Valinnaisten ominaisuuksien odotetaan muuttuvan pakollisiksi kahden pääversion julkaisun jälkeen. Tärkeät ominaisuudet voidaan poikkeuksellisesti ottaa käyttöön pakollisina.

## <a name="example-of-expected-feature-lifecycles"></a>Esimerkki ominaisuuksien odotettavissa olevista elinkaarista

Ominaisuuksien, jotka voidaan poistaa käytöstä ja jotka lisättiin julkaistuina ja valinnaisina tai huhtikuun julkaisun osana, voidaan odottaa siirtyvän **oletusarvoisesti käyttöönotetuiksi** seuraavaan lokakuun julkaisuun mennessä. Niiden odotetaan sitten muuttuvan **pakollisiksi** seuraavan vuoden huhtikuussa.

Ominaisuutta, jota ei voi poistaa käytöstä ja joka lisättiin aiemmin julkaistuna ja valinnaisena tai huhtikuun julkaisun osana, voidaan odottaa siirtyvän **pakolliseksi** seuraavan vuoden huhtikuussa.

## <a name="enable-a-feature"></a>Ota ominaisuus käyttöön

Jos ominaisuutta ei ole otettu käyttöön, tietoruudussa näkyy **Ota käyttöön nyt** -painike. Tämän painikkeen avulla voit ottaa toiminnon käyttöön.

Joitakin toimintoja ei voi poistaa käytöstä sen jälkeen, kun ne on otettu käyttöön. Jos ominaisuutta, jota yritetään ottaa käyttöön, voi ottaa käyttöön, näyttöön tulee varoitus. Tässä vaiheessa ominaisuus voidaan peruuttaa valitsemalla **Peruuta** ja jättämällä ominaisuus pois käytöstä. Jos ominaisuus kuitenkin otetaan käyttöön valitsemalla **Ota käyttöön**, sitä ei voi poistaa käytöstä myöhemmin.

Joissakin ominaisuuksissa näytetään lisätietoja sisältävä sanoma ennen käyttöönottoa. Nämä ominaisuudet on merkitty keltaisella varoitussymbolilla. Nämä lisätiedot on luettava huolellisesti ja varmistettava, että tiedetään, mitä tapahtuu, kun ominaisuus otetaan käyttöön. Ominaisuus voidaan kuitenkin ottaa käyttöön valitsemalla **Ota käyttöön**.

Jotkin ominaisuudet näyttävät sanoman, että toimintoa ei voi ottaa käyttöön, ennen kuin toimia on suoritettu. Nämä ominaisuudet on merkitty punaisella X-symbolilla. Sinun on toteutettava kuvauksessa kuvatut toimet, ennen kuin ominaisuus otetaan käyttöön. Jos et esimerkiksi pysty käyttämään ominaisuutta, ennen kuin konfigurointiavain on poistettu käytöstä, sinun on ensin poistettava määritysavain käytöstä ja palattava sitten ominaisuuksien hallintaan, jotta ominaisuus otetaan käyttöön.

Kun ominaisuus on otettu käyttöön, tietoruutuun **Lisätietoja**-linkin alapuolelle avautuu sanoma. Tämä sanoma joko ilmaisee, että ominaisuus on otettu käyttöön, tai päivämäärän, jolloin ominaisuus on aikataulutettu käyttöönotettavaksi. Se tulee näkyviin aina, kun valitset ominaisuuden ominaisuusluettelosta.

Ominaisuudet, jotka on ajoitettu otettavaksi käyttöön tulevaisuudessa, näkyvät **Ajastettu**-välilehdessä. Eräkäsittely ottaa ne käyttöön määritettynä päivänä keskiyöllä järjestelmän päivämäärän ilmaiseman aikavyöhykkeen mukaan.

## <a name="reschedule-a-feature"></a>Toiminnon ajoittaminen uudelleen

Jos ominaisuus on suunniteltu otettavaksi käyttöön tulevaisuudessa, tietoruudussa näkyy **Aikataulu**-painike. Tämän painikkeen avulla voit muuttaa **Ota käyttöön päiväys** -arvon eri päiväksi.

1. Valitse ajoitettu ominaisuus uudelleenajoitettavaksi ja valitse sitten tietoruudusta **Ajoita**.
2. Määritä näyttöön avautuvassa valintaikkunassa **Käyttöönottopäivämäärä**-kentässä uusi päivämäärä, jolloin ominaisuus on otettava käyttöön.
3. Valitse **Ota käyttöön** ajoittaaksesi toiminnon uudelleen tai **Poista käytöstä** peruuttaaksesi ajoituksen.

## <a name="disable-a-feature"></a>Poista ominaisuus käytöstä

Jos ominaisuus on otettu käyttöön, tietoruudussa on **Poista käytöstä** -painike. Tämän painikkeen avulla voit poistaa toiminnon käytöstä. **Poista käytöstä** -painike ei ole käytettävissä, jos ominaisuutta ei voi poistaa käytöstä. 

Kun ominaisuus on poistettu käytöstä, tietoruutuun **Lisätietoja**-linkin alapuolelle avautuu sanoma. Tämä sanoma ilmoittaa, ettei ominaisuutta ole otettu käyttöön. Se tulee näkyviin aina, kun valitset ominaisuuden ominaisuusluettelosta. Ominaisuudet, joita ei ole vielä otettu käyttöön, näkyvät **Ei käytössä** -välilehdessä.

## <a name="features-that-must-be-enabled"></a>Ominaisuudet, jotka on otettava käyttöön

Joskus toimitettava ominaisuus on niin tärkeä, että se on otettava käyttöön automaattisesti päivityksen yhteydessä. Nämä ominaisuudet otetaan käyttöön automaattisesti **Käyttöönottopäivämäärä**-kentässä määritettynä päivänä. Näitä ominaisuuksia koskien tietoruudussa näkyy **Lisätietoja**-linkin alla viesti. Tämä sanoma ilmaisee joko sen, että ominaisuus joko on otettu käyttöön, tai sen tulevan päivämäärän, jolloin ominaisuus otetaan käyttöön. Se tulee näkyviin aina, kun valitset ominaisuuden ominaisuusluettelosta.

## <a name="enable-all-features"></a>Ota käyttöön kaikki ominaisuudet

Voit ottaa käyttöön kaikki ominaisuudet valitsemalla **Ota kaikki käyttöön** -painikkeen. 

Kun **Ota kaikki käyttöön** valitaan, näyttöön tulee vaihtoehto, jossa on annettava seuraavat tiedot:

- Luettelo kaikista ominaisuuksista, jotka edellyttävät vahvistusta, ennen kuin ne voidaan ottaa käyttöön. Jos haluat ottaa käyttöön luettelon ominaisuudet, valitse **Kyllä** **Ota käyttöön vahvistusta edellyttävät ominaisuudet** -painikkeessa.
- Näytetään luettelo kaikista ominaisuuksista, joita ei voi ottaa käyttöön. Nämä ominaisuudet eivät ole käytössä.

Kaikki toiminnot, jotka voidaan ottaa käyttöön, otetaan käyttöön. Jos ominaisuus on jo ajoitettu käyttöön tulevaisuudessa, aikataulu ei muutu. 

## <a name="enable-all-features-automatically"></a>Kaikkien ominaisuuksien automaattinen käyttöönotto

Jos kaikki uudet ominaisuudet halutaan kuitenkin ottaa automaattisesti käyttöön, uusien ominaisuuksien lisäämiseen liittyviä tietoja voidaan muuttaa käyttämällä työtilan otsikon alla olevaa avattavaa luetteloa.

- Valitsemalla **Ota uudet ominaisuudet automaattisesti käyttöön** voidaan ottaa automaattisesti käyttöön kaikki uudet ominaisuudet, kun ne lisätään omaan ympäristöön.
- Valitse **Älä ota uusia ominaisuuksia automaattisesti käyttöön**, jos kaikkien soveltuvien uusien ominaisuuksien pitäisi olla oletusarvoisesti käytöstäpoistettuja, kun ne lisätään omaan ympäristöön.

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

- Jos **Käytössä**-kentän arvoksi vaihdetaan **Kyllä**, ominaisuus on otettu käyttöön ja **Käyttöönottopäivämäärä**-kentän arvoksi määritetään kuluva päivämäärä.
- Jos **Käytössä**-kentän arvoksi vaihdetaan **Ei** tai **EnableDate**-kenttä jätetään tyhjäksi, ominaisuus on poistettu käytöstä ja **Käyttöönottopäivämäärä**-kenttä on tyhjä. Käytöstä ei voi poistaa pakollista ominaisuutta eikä ominaisuutta, jota ei voi poistaa käytöstä käyttöönoton jälkeen.
- Jos muutat **EnableDate**-kentän arvon tulevaksi päiväksi, toiminto ajoitetaan kyseisenä päivänä.
- Jos **Käytössä**-kentän arvoksi vaihdetaan **Kyllä**, ja **EnableDate**-kentän arvoksi määritetään tuleva päivämäärä, ominaisuus ajastetaan tuolle päivämäärälle. 
- Jos **Käytössä**-kentän arvoksi vaihdetaan **Ei**, mutta samalla **EnableDate**-kentän arvo muutetaan tulevaksi päivämääräksi, ominaisuus ajastetaan tuolle päivämäärälle.
- Jos ominaisuus on otettu käyttöön ja lisätään **EnableDate**-kenttä, jonka arvoksi on määritetty tuleva päivämäärä, ominaisuus pysyy käyttöönotettuna. Ominaisuuden voi aikatauluttaa uudelleen muuttamalla **Käytössä** -kentän arvoksi **Ei**.

## <a name="feature-management-and-flighting"></a>Ominaisuuksien hallinta ja väliversiotestaus

Ominaisuuksien hallinnan avulla voit hallita kuhunkin julkaisuun toimitettuja ominaisuuksia. Väliversiotestaus-toiminnon avulla Microsoft Teamsit voivat vapauttaa toimintoja rajoitetulle määrälle asiakkaita, jotta näitä ominaisuuksia voidaan testata ja vahvistaa ilman, että se vaikuttaa kaikkiin asiakkaisiin. Ominaisuuksien hallinta ei hallitse minkään ominaisuuden väliversiotestaus-ominaisuutta.

## <a name="using-feature-management-to-turn-on-isv-features-or-custom-features"></a>ISV-ominaisuuksien tai mukautettujen ominaisuuksien ottaminen käyttöön ominaisuuksien hallinnan avulla

Ominaisuuksien hallinta ei ole tällä hetkellä käytettävissä itsenäisten ohjelmistotoimittajien (ISV) ja mukautettujen ominaisuuksien ominaisuuksista. Microsoft kuitenkin lisää toimintoja, jotka parantavat ominaisuuksien hallintaa. Kun nämä parannukset on tehty, Microsoft tekee ominaisuuksien hallinnan käytettäväksi kaikille toiminnoille ja antaa ohjeita toimintojen päivittämiseksi käyttöä varten.

## <a name="frequently-asked-questions-faq"></a>Usein kysytyt kysymykset

### <a name="when-are-features-added-removed-or-changed"></a>Milloin toimintoja lisätään, poistetaan tai muutetaan? 
Ominaisuudet omistavat tuotetiimit voivat lisätä, poistaa ja muuttaa ominaisuuksia koodia muuttamalla. Ympäristöt on päivitettävä näitä muutoksia varten.

### <a name="does-a-feature-become-mandatory-automatically"></a>Tuleeko toiminnosta pakollinen automaattisesti? 
Ei. Ominaisuudesta ei tule automaattisesti pakollista. Ominaisuuden omistavan tuotetiiminen on tehtävä koodimuutos.

### <a name="why-isnt-there-a-specific-mandatory-enabled-date"></a>Miksi käytössä ei ole erityistä pakollista käyttöönottopäivää? 
Päivitysjulkaisujen ajoitus vaihtelee, ympäristöpäivityksen ajoitus vaihtelee ja asiakkaat voivat halutessaan ohittaa joitakin päivityksiä. Tämän vuoksi tietyt päivämäärät ovat vaikeasti määritettävissä. 

### <a name="wheres-the-documentation-for-features-that-are-mandatory"></a>Missä on pakollisten toimintojen ohjeistus? 
Tämä ohjeistus saadaan kultakin Dynamics 365 -sovellusryhmältä. Nämä toiminnot mainitaan usein [asiakasohjelman ominaisuuksien päivityksissä](/dynamics365-release-plan/2021wave1/finance-operations/finance-operations-crossapp-capabilities/updates-client-feature-states) tai [poistetuissa tai vanhentuneissa ominaisuuksissa](../../../dev-itpro/migration-upgrade/deprecated-features.md). 

### <a name="is-there-an-in-product-notification-or-signal-that-a-feature-is-going-to-be-mandatory-enabled"></a>Onko tuotteessa käytössä sisäinen ilmoitus tai signaali, että toiminnon käyttöönotto tulee olemaan pakollista? 
Tällä hetkellä ei ole olemassa toiminnon pakollisuuteen liittyvää ilmoitusmekanismia.

### <a name="do-features-ever-get-enabled-without-the-customer-knowing-about-it"></a>Otetaanko toimintoja koskaan käyttöön niin, että asiakas ei tiedä siitä? 
Kyllä. Ominaisuudet voidaan ottaa seuraavissa tilanteissa käyttöön ilman, että asiakas olisi siitä tietoinen:
- Ominaisuus siirretään **Oletusarvoisesti käyttöönotettu** -tilaan. Ominaisuus voidaan vielä poistaa käytöstä tässä tilassa. 
- Ominaisuus päivitetään **pakolliseksi**. Tätä muutos tehdään vain pääversion julkaisun yhteydessä. Tärkeitä ominaisuudet voidaan poikkeuksellisesti siirtää **Pakollinen**-tilaan missä tahansa päivityksessä.

### <a name="what-is-feature-flighting-and-how-does-it-relate-to-feature-management"></a>Mitä toiminnon väliversiotestaus tarkoittaa ja miten se liittyy toiminnon hallintaan? 
Toiminnon väliversiotestaukset on reaaliaikaisia Microsoftin hallitsemia päälle/pois-kytkimiä. Ne ovat erillään asiakkaan toimintojen hallinnan avulla tapahtuvasta hallinnasta. 
- Yksityisiä esiversiotoimintoja ei mainita toimintojen hallinnassa, ennen kuin ne ovat väliversiotestauksessa. Tuotannossa asiakkaan on hyväksyttävä erikoisohjelmaan osallistuminen, jotta näin voi tapahtua.
- Julkisen esiversion ja julkaistut (yleisesti saatavana olevat) toiminnot mainitaan toimintojen hallinnassa, ellei niiden väliversiotestaus ole pois käytöstä. Toiminnon väliversiotestauksen poistaminen on tuotantoryhmien viimeinen vaihtoehto, jos löytyy kriittinen ongelma ja se on yleensä asiakaskohtainen toiminta.

### <a name="do-features-ever-get-flighted-off-without-the-customer-knowing-about-it"></a>Otetaanko toimintoja koskaan pois väliversiotestauksesta siten, että asiakas ei tiedä siitä? 
Kyllä, jos toiminto vaikuttaa ympäristön toimintaan silloin, kun niillä ei ole toiminnallista vaikutusta, jolloin ne voidaan ottaa oletusarvoisesti käyttöön.

### <a name="how-can-feature-enablement-be-checked-in-code"></a>Miten ominaisuuden käyttöönotto tarkistetaan koodissa?
Käytä **FeatureStateProvider**-luokassa **isFeatureEnabled**-menetelmää siirtämään siihen ominaisuusluokan esiintymä. Esimerkki: 

```xpp
if (FeatureStateProvider::isFeatureEnabled(BatchContentionPreventionFeature::instance()))
```

### <a name="how-can-feature-enablement-be-checked-in-metadata"></a>Miten ominaisuuden käyttöönotto tarkistetaan metatiedoissa?
**FeatureClass**-ominaisuudella voidaan ilmaista, että ominaisuuteen on liitetty metatietoja. Ominaisuudelle on käytettävä luokan nimeä, kuten **BatchContentionPreventionFeature**. Nämä metatiedot näkyvät vain kyseisessä ominaisuudessa, **FeatureClass**-ominaisuus on käytettävissä valikoissa, valikkovaihtoehdoissa, valintalistan arvoissa sekä taulukko- ja näkymäkentissä.

### <a name="what-is-a-feature-class"></a>Mikä on ominaisuusluokka?
Ominaisuuksien hallinnan ominaisuudet on määritetty *ominaisuusluokiksi*. Ominaisuusluokka **toteuttaa IFeatureMetadata-ominaisuuden** ja käyttää luokkamääritettä määrittämään itsensä Ominaisuuksien hallinta -työtilassa. Käytettävissä on useita ominaisuusluokkaesimerkkejä, joiden käyttöönotto koodissa voidaan tarkistaa **FeatureStateProvider**-ohjelmointirajapinnan avulla ja metatiedoissa **FeatureClass**-ominaisuuden avulla. Esimerkki: 

```xpp
[ExportAttribute(identifierStr(Microsoft.Dynamics.ApplicationPlatform.FeatureExposure.IFeatureMetadata))]
internal final class BankCurrencyRevalGlobalEnableFeature implements IFeatureMetadata
```

### <a name="what-is-the-ifeaturelifecycle-implemented-by-some-feature-classes"></a>Mikä on joissakin ominaisuus luokissa käyttöönotettu IFeatureLifecycle?
IFeatureLifecycle on Microsoftin sisäinen mekanismi, joka ilmaisee ominaisuuden elinkaaren vaiheen. Mahdolliset ominaisuudet:
- `PrivatePreview` – näkymistä varten tarvitaan väliversio.
- `PublicPreview` – näytetään oletusarvoisesti, mutta mukana on varoitus siitä, ominaisuus on esiversio.
- `Released` – kokonaan vapautettu.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
