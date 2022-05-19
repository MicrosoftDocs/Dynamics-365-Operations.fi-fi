---
title: Tuottokirjauksen uudelleenkohdistus
description: Tässä ohjeaiheessa kerrotaan uudelleenkohdistuksesta, jonka avulla organisaatiot voivat laskea tuottohinnat uudelleen, kun sopimusmyynnin ehtoja muutetaan. Se sisältää linkkejä muihin aiheisiin, joissa kuvataan, miten tuotto kirjataan erilaisissa skenaarioissa.
author: kweekley
ms.date: 09/09/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-21
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 7528202ed140dc2c0a7fc8c595178f155c3c1f75
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/07/2022
ms.locfileid: "8726124"
---
# <a name="revenue-recognition-reallocation"></a>Tuottokirjauksen uudelleenkohdistus

[!include [banner](../includes/banner.md)]

Uudelleenkohdistuksen avulla organisaatiot voivat laskea tuottohinnat uudelleen, kun sopimusmyynnin ehtoja muutetaan. Tuottokirjaustarkoitusta varten myyntitilausasiakirjoja pidetään sopimuksena.

Organisaation on itse määritettävä, tarvitaanko uudelleenkohdistusta. Uuden rivin lisääminen myyntitilaukseen tai uuden myyntitilauksen lisääminen asiakkaalle ei välttämättä tarkoita sopimuksen muutosta. Seuraavat skenaariot saattavat edellyttää uudelleenkohdistusta:

- Asiakas on lisännyt nimikkeitä myyntitilaukseen tai poistanut nimikkeitä myyntitilauksesta sen jälkeen, kun tilaus on laskutettu kokonaan tai osittain.
- Samalle neuvotellulle sopimukselle on syötetty useita myyntitilauksia joko vahvistetussa tilassa tai laskutetussa tilassa.
- Asiakas on palauttanut tai saanut hyvityksen nimikkeestä sen jälkeen, kun alkuperäinen myyntitilaus on laskutettu kokonaan tai osittain.

Uudelleenkohdistusprosessissa on muutamia tärkeitä rajoituksia:

- Prosessi voidaan suorittaa vain kerran. Siksi on tärkeää, että suoritat sen vasta, kun kaikki muutokset on tehty.

    - Tämä rajoitus poistetaan versiosta 10.0.17 ja sitä myöhemmistä versioista.

- Prosessia ei voi suorittaa projektin myyntitilauksille.

    - Tämä rajoitus poistetaan versiosta 10.0.17 ja sitä myöhemmistä versioista.

- Jos prosessiin liittyy useita myyntitilauksia, niiden on oltava samalle asiakastilille.
- Kaikkien uudelleenkohdistettavien myyntitilausten tapahtumavaluutan on oltava sama.
- Prosessia ei voi peruuttaa tai kumota sen jälkeen, kun se on suoritettu.

    - Tämä rajoitus poistetaan versiosta 10.0.17 ja sitä myöhemmistä versioista.

- Uudelleenkohdistuksen voi tehdä vain joko myyntitilauksille tai projektin myyntitilauksille. Sitä ei voi tehdä myyntitilausten ja projektin myyntitilausten yhdistelmälle.

    - Tämä rajoitus poistetaan versiosta 10.0.17 ja sitä myöhemmistä versioista.

## <a name="set-up-reallocation"></a>Uudelleenkohdistuksen määrittäminen

Uudelleenkohdistusprosessiin vaikuttaa yksi parametri.

Koska uudelleenkohdistus voidaan tehdä osittain tai kokonaan laskutetulle myyntitilaukselle, laskun aiemmat kirjanpitomerkinnät on korjattava käyttämällä uusia, uudelleenkohdistettuja tuottohintoja. Tämä korjaus tehdään peruuttamalla alkuperäisen laskun kirjanpitomerkintä ja kirjaamalla uusi kirjanpitomerkintä, joka perustuu uudelleenkohdistettuihin tuottohintoihin.

Organisaation on päätettävä, päivittääkö korjaus vain kirjanpidon vai päivittääkö se myös myyntireskontran. Tehty päätös määrittää oikean **Kirjaa laskun korjaukset myyntireskontraan** ‑asetuksen **Kirjanpitoparametrit**-sivun **Tuottokirjaus**-välilehdessä (**Tuottokirjaus \> Asetukset \> Kirjanpitoparametrit**). Sopiva asetus riippuu kyseessä olevasta skenaariosta. Saat lisätietoja mahdollisista skenaarioista jäljempänä tässä ohjeaiheessa olevan [Uudelleenkohdistusskenaariot](#scenarios-for-reallocation)-osan linkeistä.

[![Kirjanpitoparametrit-sivun Tuottokirjaus-välilehti.](./media/01_RevRecScenarios.png)](./media/01_RevRecScenarios.png)

Jos **Kirjaa laskujen korjaukset myyntireskontraan** -asetuksena on **Kyllä**, uudelleenkohdistusprosessi tuottaa seuraavan tuloksen:

- Myyntireskontraan luodaan hyvitysasiakirja, joka peruuttaa korjausta edellyttävän laskun.

    - Hyvitysasiakirjassa käytetään alkuperäistä laskun numeroa, mutta siihen lisätään ”-1”.
    - Hyvitysasiakirja selvitetään automaattisesti alkuperäistä laskua vasten. Jos alkuperäinen lasku on jo selvitetty toisella hyvitysasiakirjalla tai maksulla, selvitys peruutetaan automaattisesti.
    - Hyvitysasiakirja kirjataan kirjanpitoon alkuperäiseen laskuun kirjatun kirjanpitomerkinnän peruuttamiseksi. Varastotapahtumien ja myytyjen tuotteiden kustannustapahtumien (MTKUST) merkintöjä ei kuitenkaan peruuteta.

- Myyntireskontraan luodaan uusi lasku, joka perustuu uudelleenkohdistettuihin hintasummiin.

    - Uudessa laskussa käytetään alkuperäistä laskun numeroa, mutta siihen lisätään ”-2”.
    - Uusi lasku selvitetään automaattisesti kaikkia sellaisia hyvitysasiakirjoja ja maksuja vastaan, jotka on aiemmin selvitetty alkuperäisen laskun kanssa.
    - Uusi lasku kirjataan kirjanpitoon käyttämällä uusia, uudelleenkohdistettuja tuottohintasummia. Sitä ei kirjata uudelleen varasto- ja MTKUST-tileille, koska kyseisiä merkintöjä ylläpidetään alkuperäisen laskun kirjanpitomerkinnässä.

Jos **Kirjaa laskujen korjaukset myyntireskontraan** -asetuksena on **Ei**, uudelleenkohdistusprosessi tuottaa seuraavan tuloksen:

- Peruuttava kirjanpitomerkintä kirjataan vain kirjanpitoon. Kaikki alkuperäisen laskun kirjanpito peruutetaan lukuun ottamatta varasto- ja MTKUST-tilivientejä.
- Uusi kirjanpitomerkintä kirjataan vain kirjanpitoon uusien, uudelleenkohdistettujen tuottohintojen perusteella. Sitä ei kirjata uudelleen varasto- ja MTKUST-tileille, koska kyseisiä merkintöjä ylläpidetään alkuperäisen laskun kirjanpitomerkinnässä.
- **Asiakastapahtumat**-sivulla oleva lasku ei muutu, mutta se vastaa edelleen alkuperäistä kirjanpitomerkintää. Peruuttaviin tai uusiin kirjanpitomerkintöihin ei ole viittausta.

Voit siis päivittää vain kirjanpidon tai sekä kirjanpidon että myyntireskontran. Molemmilla lähestymistavoilla on etunsa ja haittansa. On suositeltavaa arvioida organisaation tarpeet ja valita vaihtoehto niiden mukaan. Jos päivität sekä kirjanpidon että myyntireskontran, oikeat kirjanpitomerkinnät näkyvät uudessa laskussa ja niitä voi tarkastella **Asiakastapahtumat**-sivulla olevasta asiakirjasta. Lisäksi selvitysprosessissa käytetään päivitettyjä kirjanpitomerkintöjä käteisalennusten sekä voittojen tai tappioiden kirjaamiseen. Toisaalta hyvitysasiakirja ja uusi lasku näkyvät asiakkaan tiliotteissa ja erääntymisraporteissa, aivan kuten muut hyvityslaskut ja myyntilaskut. Näiden asiakirjojen kuvaus ilmaisee, että ne on luotu kirjanpidon korjauksen kautta.

## <a name="run-the-reallocation-process"></a>Uudelleenkohdistusprosessin suorittaminen

Voit käynnistää uudelleenkohdistusprosessin valitsemalla **Uudelleenkohdista hinta uusilla tilausriveillä** missä tahansa myyntitilauksessa, joka on kohdistettava uudelleen. Vaihtoehtoisesti voit siirtyä kohtaan **Tuottokirjaus \> Kausittaiset tehtävät \> Uudelleenkohdista hinta uusilla tilausriveillä** ja syöttää sitten tarvittavat suodattimet, kuten asiakastilin.

[![Uudelleenkohdista hinta uusilla tilausriveillä ‑sivu.](./media/02_RevRecScenarios.png)](./media/02_RevRecScenarios.png)

**Uudelleenkohdista hinta uusilla tilausriveillä** ‑sivun ylemmän ruudukon nimi on **Myynti**. Siinä on lueteltu asiakkaan myyntitilaukset. Valitse myyntitilaukset, jotka on kohdistettava uudelleen. Jos myyntitilauksella on uudelleenkohdistustunnus, toinen käyttäjä on jo merkinnyt sen uudelleenkohdistettavaksi. Jos jotkin myyntitilaukset on uudelleenkohdistettu jo aiemmin ja sisällytettävä nyt toiseen uudelleenkohdistukseen, kyseisten myyntitilausten uudelleenkohdistus on ensin kumottava. Sen jälkeen ne voidaan sisällyttää uuteen uudelleenkohdistukseen. Lisätietoja on jäljempänä tässä ohjeaiheessa kohdissa [Uudelleenkohdistuksen kumoaminen](#undo-a-reallocation) ja [Uudelleenkohdistaminen useita kertoja](#reallocate-multiple-times).

Sivun alemman ruudukon nimi on **Rivit**. Kun olet valinnut **Myynti**-ruudukosta yhden tai useamman myyntitilauksen, myyntitilausrivit näkyvät **Rivit**-ruudukossa. Valitse myyntitilausrivit, jotka on kohdistettava uudelleen. Jos olet valinnut vain yhden myyntitilauksen, saman myyntitilauksen rivit on kohdistettava uudelleen. Näin voi tapahtua, kun jokin myyntitilausriveistä on laskutettu aiemmin ja sitten on lisätty uusi rivi tai aiemmin luotu rivi on poistettu tai peruutettu. Jos rivi on poistettu, se ei näy ruudukossa. Näin ollen sitä ei voi valita. Se otetaan kuitenkin edelleen huomioon, kun uudelleenkohdistusprosessi suoritetaan.

Kun olet valinnut tarvittavat myyntitilausrivit, käytä toimintoruudun painikkeita seuraavien ohjeiden mukaan:

- **Päivitä uudelleenkohdistus** – laske valittujen myyntitilausrivien uudet tuottohintasummat. Jos jokin rivi on poistettu tai peruutettu, uudelleenkohdistus tehdään vain valitsemillesi olemassa oleville riveille. Seuraavassa kuvassa on esimerkki myyntitilausriveistä ennen uudelleenkohdistuksen päivittämistä.

    [![Myyntitilausrivit ennen uudelleenkohdistuksen päivittämistä.](./media/03_RevRecScenarios.png)](./media/03_RevRecScenarios.png)

    Uudet tuottohintasummat näkyvät **Rivit**-ruudukon **Uudelleenkohdistettu summa** -sarakkeessa. Tässä vaiheessa uudelleenkohdistus on käsitelty, mutta sitä ei ole vielä laskettu. Seuraavassa kuvassa on esimerkki myyntitilausriveistä uudelleenkohdistuksen päivittämisen jälkeen.

    [![Myyntitilausrivit uudelleenkohdistuksen päivittämisen jälkeen.](./media/04_RevRecScenarios.png)](./media/04_RevRecScenarios.png)

- **Käsittele** – käsittele tai kirjaa uudelleenkohdistetut tuottohinnat. Kun olet valinnut tämän painikkeen, uudelleenkohdistusta ei voi peruuttaa. Jos et ole valinnut **Päivitä uudelleenkohdistus** -painiketta ennen **Käsittele**-painikkeen valitsemista, uudelleenkohdistus suoritetaan automaattisesti.

    - Jos myyntitilausriviä ei ole laskutettu, tuottohintasummat päivitetään kaikkiin uudelleenkohdistettaviksi valittuihin myyntitilauksiin.
    - Jos vähintään yksi myyntitilausrivi on laskutettu, korjaavat kirjanpitomerkinnät kirjataan ja laskutetulle myyntitilausriville luodut tuottoaikataulun tiedot korjataan.

- **Odotettu tosite** – näytä laskutetuille myyntitilausriveille luotujen kirjanpitomerkintöjen esikatselu. Jos yhtään riviä ei ole laskutettu, mitään ei näytetä. Jos et ole valinnut **Päivitä uudelleenkohdistus** -painiketta ennen **Odotettu tosite** ‑painikkeen valitsemista, uudelleenkohdistus suoritetaan automaattisesti.
- **Tuoton uudelleenkohdistus** – avaa sivu, jossa näkyy kaikkien valittujen rivien tuottohinnan kohdistus. Et voi muuttaa sivulla olevia tietoja. Siinä näkyvät uudelleenkohdistuksessa käytetyt rivisummat.

    [![Uudelleenkohdistuksessa käytetyt rivisummat.](./media/05_RevRecScenarios.png)](./media/05_RevRecScenarios.png)

- **Tyhjennä valitun asiakkaan tiedot** – jos uudelleenkohdistusprosessi on aloitettu, mutta se ei ole valmistunut, tyhjennä uudelleenkohdistustaulun tiedot vain valitun asiakkaan osalta. Tällainen on esimerkiksi tilanne, jossa merkitset useita myyntitilausrivejä uudelleenkohdistusta varten ja jätät sivun auki valitsematta **Käsittele**, minkä jälkeen sivu aikakatkaistaan. Tällöin myyntitilausrivit säilyvät merkittyinä eivätkä ne ole toisen käyttäjän käytettävissä uudelleenkohdistusprosessin viimeistelyä varten. Sivu saattaa jopa olla tyhjä, kun se avataan. Tässä tilanteessa voit tyhjentää käsittelemättömät myyntitilaukset **Tyhjennä valitun asiakkaan tiedot** -painikkeen avulla, jotta toinen käyttäjä voi viimeistellä uudelleenkohdistusprosessin.

## <a name="undo-a-reallocation"></a>Uudelleenkohdistuksen kumoaminen

Uudelleenkohdistus kumotaan suorittamalla toinen uudelleenkohdistus. Uudelleenkohdistus tehdään uudelleen, ja käyttäjä valitsee eri myyntitilausrivit sisällytettäviksi toiseen uudelleenkohdistusprosessiin.

Jos uudelleenkohdistus on tehty kahdelle tai useammalle erilliselle myyntitilaukselle, sen voi kumota valitsemalla **Kohdista hinta uudelleen uusille tilausriveille** missä tahansa myyntitilauksessa, joka sisältyy uudelleenkohdistukseen. Et voi kumota uudelleenkohdistusta valitsemalla **Tuottokirjaus \> Kausittaiset tehtävät \> Kohdista hinta uudelleen uusille tilausriveille**, koska tällä tavalla avautuvalla sivulla näkyvät vain myyntitilaukset, joilla ei ole uudelleenkohdistustunnusta. Uudelleenkohdistustunnus määritetään sen jälkeen, kun asiakirja on kohdistettu uudelleen.

Poista **Kohdista hinta uudelleen uusille tilausriveille** ‑sivulla sellaisten myyntitilausten merkintä, jotka tulisi jättää pois sopimuksesta. Käytä uudelleenkohdistuksen käsittelyyn asianmukaisia toimintoruudun painikkeita, kuten **Päivitä uudelleenkohdistus** ja **Käsittele**. Jos kaikilta myyntitilauksilta paitsi aktiiviselta myyntitilaukselta puuttuu merkintä, uudelleenkohdistus tunnus poistetaan, kun muutos käsitellään.

Jos uudelleenkohdistus on tehty lisäämällä uusi rivi kokonaan tai osittain laskutettuun myyntitilaukseen, uudelleenkohdistuksen voi kumota vain poistamalla kyseinen rivi myyntitilauksesta ja suorittamalla sitten uudelleenkohdistus uudelleen. Myyntitilausrivi on poistettava, koska kaikkien myyntitilauksen rivien oletetaan olevan osa samaa sopimusta. Et voi poistaa myyntitilausrivin merkintää, kun olet **Kohdista hinta uudelleen uusille tilausriveille** ‑sivulla.

## <a name="reallocate-multiple-times"></a>Uudelleenkohdistaminen useita kertoja

Samalle myyntitilaukselle voi tehdä useita uudelleenkohdistuksia, jos sopimukseen on tehty useita muutoksia. Jokainen uudelleenkohdistus aiheuttaa uudelleenkohdistustunnuksen määrittämisen myyntitilaukselle tai myyntitilausryhmälle muutosten ryhmittelyä varten. Jos uudelleenkohdistuksia tehdään useita, jokainen uusi uudelleenkohdistus käyttää samaa uudelleenkohdistustunnusta kuin ensimmäinen uudelleenkohdistus.

Esimerkki: Syötetään myyntitilaus 00045, jossa on useita rivejä. Kun myyntitilaus on laskutettu kokonaan, siihen lisätään uusi myyntitilausrivi. Tämän jälkeen suoritetaan uudelleenkohdistus avaamalla **Kohdista hinta uudelleen uusille tilausriveille** ‑sivu joko myyntitilauksesta 00045 tai valitsemalla **Tuottokirjaus \> Kausittaiset tehtävät \> Kohdista hinta uudelleen uusille tilausriveille**. Myyntitilaukselle määritetään uudelleenkohdistustunnus **Reall000001**.

Samalle sopimukselle luodaan toinen myyntitilaus 00052. Uudelleenkohdistuksen voi suorittaa uudelleen avaamalla **Kohdista hinta uudelleen uusille tilausriveille** ‑sivun myyntitilauksesta 00045, mutta ei myyntitilauksesta 00052. Jos avaat **Kohdista hinta uudelleen uusille tilausriveille** ‑sivun myyntitilauksesta 00052, myyntitilausta 00045 ei näytetä, koska sille on määritetty uudelleenkohdistustunnus. Sivulla näkyvät vain myyntitilaukset, joilla ei ole uudelleenkohdistustunnusta.

Toisen uudelleenkohdistuksen voi tehdä kahdella tavalla. Voit kumota myyntitilauksen 00045 uudelleenkohdistuksen. Tässä tapauksessa uudelleenkohdistustunnus poistetaan, minkä jälkeen voit tehdä uudelleenkohdistuksen joko myyntitilauksesta 00045 tai myyntitilauksesta 00052. Vaihtoehtoisesti voit avata **Kohdista hinta uudelleen uusille tilausriveille** ‑sivun myyntitilauksesta 00045 ja lisätä toisen myyntitilauksen. Kun uudelleenkohdistusta käsitellään, uudelleenkohdistustunnus **Reall000001** määritetään sekä myyntitilaukselle 00045 että myyntitilaukselle 00052.

## <a name="scenarios-for-reallocation"></a>Uudelleenkohdistusskenaariot

Seuraavissa ohjeaiheissa käsitellään erilaisia tuottojen kirjaamisen skenaarioita:

- [Tuottokirjauksen uudelleenkohdistus – skenaario 1](rev-rec-reallocation-scenario-1.md) – kaksi myyntitilausta syötetään, mutta ne ainoastaan vahvistetaan. Sama skenaario tuottaa samanlaisia tuloksia, jos enemmän kuin kaksi myyntitilausta on vahvistetussa tilassa.
- [Tuottokirjauksen uudelleenkohdistus – skenaario 2](rev-rec-reallocation-scenario-2.md) – kaksi myyntitilausta syötetään, ja sitten asiakas lisää nimikkeen sopimukseen ensimmäisen myyntitilauksen laskuttamisen jälkeen.
- [Tuottokirjauksen uudelleenkohdistus – skenaario 3 ](rev-rec-reallocation-scenario-3.md) – aiemmin luotuun, laskutettuun myyntitilaukseen lisätään uusi rivi.
- [Tuottokirjauksen uudelleenkohdistus – skenaario 4 ](rev-rec-reallocation-scenario-4.md) – aiemmin luodusta, osittain laskutetusta myyntitilauksesta poistetaan rivi.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
