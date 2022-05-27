---
title: Toimittajan maksatusehdotusten automatisointi
description: Tässä ohjeaiheessa kerrotaan, kuinka organisaatiot, jotka maksavat toimittajille toistuvassa aikataulussa, voivat automatisoida toimittajan maksuehdotusten luonnin.
author: kweekley
ms.date: 04/08/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 262034
ms.assetid: 9db38b3f-26b3-436e-8449-7ff243568a18
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-04-08
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: ad9b1929cb4773ae79c54f6c95d73c1a8d5f86ef
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/05/2022
ms.locfileid: "8712590"
---
# <a name="automate-vendor-payment-proposals"></a>Toimittajan maksatusehdotusten automatisointi

[!include [banner](../includes/banner.md)]

Organisaatiot, jotka maksavat toimittajille toistuvassa aikataulussa, voivat nyt automatisoida toimittajan maksuehdotusten luonnin. Toimittajan maksuehdotusten automaatiot määrittävät seuraavat tiedot:

- Kun maksuehdotukset suoritetaan
- Mitä kriteereitä käytetään maksettavien laskujen valitsemiseen
- Mihin toimittajan maksukirjauskansioon tuloksena olevat maksut tallennetaan

Maksuehdotuksen automaatiot eivät kirjaa maksuja automaattisesti. Tämän vuoksi voit jatkaa sellaisten oikeellisuustarkistus- ja työnkulkuprosessien käyttämistä, joiden avulla voit hyväksyä luodut maksutavat.

> [!NOTE]
> **Toimittajan maksuehdotusten automaatio** -ominaisuuden on oltava käytössä toimintojen hallinnassa, jotta tätä toimintoa voidaan käyttää. 

## <a name="define-the-occurrence-of-vendor-payment-proposals"></a>Toimittajan maksuehdotusten esiintymän määrittäminen

Toimittajan maksuehdotusten automaatiot käyttävät prosessin automaatiokehystä. Eri liiketoimintaprosessit käyttävät tätä kehystä valitun prosessin toistumisen määrittämiseen. Toimittajien maksuehdotuksissa automaatiota voi käyttää kohdasta **Ostoreskontra \> Maksumääritys \> Prosessin automatisointi**.

Käytä ensin **Luo uusi prosessi** -automaatiovaihtoehtoa ja valitse **Toimittajan maksuehdotus**. Ohjattutoiminto opastaa toimittajan maksuehdotuksen määrittämisessä.

## <a name="general-page"></a>Yleiset-sivu

Kirjoita ohjatun toiminnon **Yleiset**-sivulla luotavan toimittajan maksuehdotuksen nimi. Jos esimerkiksi maksat kaikki kotimaiset toimittajat sekillä maanantaina, kirjoita kuvaava nimi, kuten **Kotimainen\_sekki**. Syöttämäsi nimi näkyy **Toimittajamaksu**-työtilan prosessin automatisointi viikoittain -näkymässä.

Määritä seuraavaksi luotavan maksukirjauskansion omistaja. Omistaja on yleensä ostoreskontran (AP) maksuvirkailija, joka vastaa maksukirjauskansiosta sen luomisen jälkeen.

Muut sivun asetukset ovat yleisiä, ja niiden avulla määritetään toimittajan maksuehdotuksen tämän version esiintymämalli. Jos esiintymä on tarkoitettu esimerkiksi maanantaina suoritettavia sekkimaksuja varten, voit määrittää sen niin, että se suoritetaan viikoittain, ja voit valita maanantain viikon päiväksi, jolloin se suoritetaan. Voit myös määrittää aikaisen aikataulun ajan, kuten 2.00, jolloin prosessiautomaatio valmistuu ennen seuraavan työpäivän alkua.

On tärkeää, että ymmärrät, että käytät ohjattua toimintoa määrittääksesi, milloin toimittajan maksuehdotus käsitellään. Et määritä, milloin toimittajamaksuja luodaan, tulostetaan ja kirjataan. Viikoittain-näkymässä toimittajan maksuja koskevien ehdotusten prosessiautomaatio näkyy tapahtumarakenteessa valittuina päivinä.

Lisätietoja muut **Yleiset**-sivun kentistä on prosessiautomaation ohjeissa.

## <a name="vendor-payment-proposal-page"></a>Toimittajan maksuehdotus -sivu

Ohjatun toiminnon seuraava sivu on **Toimittajan maksuja koskeva ehdotus** -sivu. Sen avulla määritetään maksettavien toimittajalaskujen valintakriteerit. Samat vaihtoehdot löytyvät yleensä toimittajan maksukirjauskansion maksuehdotuksista. Poikkeuksia on kuitenkin muutamia. Esimerkiksi kaikki tämän sivun päivämäärät on määritettävä suhteellisina päivämäärinä, koska maksuehdotuksen päivämäärä muuttuu aina, kun ehdotus suoritetaan.

### <a name="journal-name"></a>Kirjauskansion nimi

**Kirjauskansion nimi** -kenttä määrittää sen kirjauskansion nimen, jossa toimittajan maksuja luodaan. Toimittajan maksuehdotuksen automaation tulokset luovat maksuja määritettyyn kirjauskansioon, mutta kirjauskansiota ei kirjata.

### <a name="from-date-and-to-date"></a>Päivämäärästä ja Päivämäärään

Sen sijaan, että määrittäisin laskun päivämäärästä- ja päivämäärään -kenttien avulla eräpäivän tai käteisalennuksen päivämäärän perusteella, sinun on käytettävä **Määritä päivämäärään** -ehtoa ja **päivien oikaisujen määrä** -kentän arvoksi päivämäärä, joka määrittää päättymispäivämäärän. Maksuehdotusautomaatioiden alkaen-päivästä ei ole käsitettä.

Oletusarvon mukaan **Määritä päättymispäivämäärä** -asetukseksi on valittu **Ei**. Jos käytät tätä oletusarvoa, prosessi valitsee kaikki maksettavat laskut, kun prosessi suoritetaan, koska päättymispäivämäärää ei ole määritetty.

Jos määrität **päivämäärän kriteerit** -asetukseksi **Kyllä**, käytä **Päivämääräoikaisu tähän päivään mennessä** -kenttää, jolloin laskut valitaan ennen prosessin suorituksen päivämäärää tai sen jälkeen, kun päivämääräkentän arvo on määritetty. Luku voi olla positiivinen, negatiivinen tai 0 (nolla). Tällöin järjestelmä maksaa laskut, joiden eräpäivä tai käteisalennuksen päivämäärä on määritetty päivinä ennen tai jälkeen, kun prosessi suoritetaan. Esimerkiksi perjantaina erääntyvien laskujen osalta maksusarjat luovat maksuja kaikille toimittajille sekillä keskiviikkona. Tässä tapauksessa määritä **Päivämääräoikaisu tähän päivään mennessä** -kentän arvoksi **2**. Kun maksuehdotuksen esiintymä suoritetaan keskiviikkona (25. maaliskuuta), kaikki laskut, joiden eräpäivä tai käteisalennuspäivämäärä on vähintään 27. maaliskuuta, valitaan maksettavaksi.

### <a name="minimum-payment-date"></a>Aikaisin maksupäivä

Aikaisin maksupäivä määrittää aikaisimman päivän, jota käytetään, kun maksuja luodaan. Määritä ensin **Määritä vähimmäismaksupäivämäärän kriteerit** -asetukseksi **Kyllä**. Tämän asetuksen avulla voit käyttää minimimaksupäivämäärä toimintoa. Jos asetuksen arvoksi on määritetty **Kyllä** käytä **Päivien lukumääräoikaisu vähimmäismaksupäivää varten** -kenttää, jolloin laskut valitaan ennen prosessin suorituksen päivämäärää tai sen jälkeen, kun päivämääräkentän arvo on määritetty. Luku voi olla positiivinen, negatiivinen tai 0 (nolla). Esimerkiksi maksusarja luo keskiviikkona maksut, jotka kattavat kaikki maksut, joilla on edellisen maanantain vähimmäismaksupäivämäärä. Tässä tapauksessa määritä **Päivien lukumääräoikaisu vähimmäismaksupäivää varten** -kentän arvoksi **-2**.

Tässä on esimerkki, joka osoittaa, kuinka saakka-päivän ja vähimmäismaksupäivän kentät toimivat yhdessä. Maksatusehdotuksen automaatio määritetään suoritettavaksi keskiviikkona. **Päivämääräoikaisu tähän päivään mennessä** -kentän arvoksi määritetään **1**, joka määrittää päivämäärän eräpäivän perusteella. **Päivien lukumääräoikaisu vähimmäismaksupäivää varten** -kentän arvoksi on asetettu **-2**. Jos maksuprosessiautomaatio alkaa keskiviikkona 25. maaliskuuta, kaikki laskut, jotka erääntyvät 26. maaliskuuta, sisällytetään maksatusehdotukseen. Maksatusehdotukset luodaan seuraavalla tavalla:

- Kaikkien laskujen, jotka erääntyvät 23. päivänä tai sitä ennen, eräpäivä on 23. maaliskuuta.
- Laskujen, jotka erääntyvät 24. päivänä, eräpäivä on 24. maaliskuuta.
- Laskujen, jotka erääntyvät 25. päivänä, eräpäivä on 25. maaliskuuta.
- Laskujen, jotka erääntyvät 26. päivänä, eräpäivä on 26. maaliskuuta.

### <a name="summarized-payment-date"></a>Maksuyhteenvedon päivämäärä

Maksuyhteenvedon päivämäärää käytetään vain, kun maksutavan **Kausi**-kentässä laskujen maksutavaksi on valittu **Yhteensä**. Jos **Kausi**-kentän arvoksi on määritetty maksutavoillesi **Kokonaismäärä**, määritä **Maksupäivämäärän yhteenvetoehdot** -asetukseksi **Kyllä**. Jos asetuksen arvoksi on määritetty **Kyllä** käytä **Päivien lukumääräoikaisu yhdistettyä maksupäivää varten** -kenttää, jolloin laskut valitaan ennen prosessin suorituksen päivämäärää tai sen jälkeen, kun päivämääräkentän arvo on määritetty. Luku voi olla positiivinen, negatiivinen tai 0 (nolla). Esimerkiksi sarja luo maksut keskiviikkona, ja yritys haluaa luoda yhteenvetomaksun keskiviikkona. Tässä tapauksessa määritä **Päivien lukumääräoikaisu maksuyhteenvedon päivämäärää varten** -kentän arvoksi **0**.

### <a name="records-to-include"></a>Sisällytettävät tietueet

Suodatusvaihtoehdot voidaan määrittää myös maksuehdotukselle. Jos suodatin on määritetty, suodatusehdot eivät näy ohjatun toiminnon sivulla. Niitä voidaan kuitenkin tarkastella avaamalla suodatin uudelleen.

Ehdotuksen muut kentät toimivat samalla tavalla kuin ne toimivat toimittajamaksuja koskevan kirjauskansion maksuja koskevassa ehdotuksessa. Lisätietoja muista kentistä on kohdassa [toimittajamaksun luominen maksuehdotuksen avulla](create-vendor-payments-payment-proposal.md).

> [!NOTE]
> Jotkin maa-/aluekohtaiset kentät ja tietyt julkisen sektorin kentät eivät ole vielä käytettävissä toimittajan maksuehdotusautomaatioiden yhteydessä.

Suosittelemme, että arvioit tarpeittesi mukaan, onko automaatio hyödyllinen organisaatiollesi.

## <a name="view-the-results-of-a-vendor-payment-proposal-automation"></a>Toimittajan maksatusehdotuksen automaation tulosten tarkasteleminen

Kun toimittajan maksatusehdotuksen automaatiosarja on tehty, kunkin suorituksen esiintymät näkyvät prosessiautomaation viikkonäkymässä. Toimittajamaksuissa prosessiautomaation viikkonäkymä on lisätty sekä **Toimittajamaksu**-työtilaan että **Prosessiautomaatio**-sivulle.

[![Toimittajamaksut-työtilan prosessiautomaation viikoittainen näkymä.](./media/vendor-payment-proposal-1.png)](./media/vendor-payment-proposal-1.png)

**Toimittajamaksut**-työtilan prosessiautomaation viikkonäkymä näyttää vain toimittajien maksuehdotusten automaatiot. Se näyttää kaikki nykyisen viikon maksujen esiintymät kaikille yrityksille, joihin kirjautuneen käyttäjän suojausoikeudet on määritetty. Jos esimerkiksi ostoreskontran työntekijä vastaa USMF- ja USSI-yritysten maksuista, hän näkee toimittajan maksuehdotuksen automatisoinnin esiintymät näille kahdelle yritykselle, mutta ei muille yrityksille.

[![Prosessiautomaation viikkonäkymä USMF- ja USSI-yrityksille.](./media/vendor-payment-proposal-2.png)](./media/vendor-payment-proposal-2.png)

Kukin esiintymä näyttää yrityksen, johon kirjauskansio on luotu tai tullaan luomaan. Jos maksuja luodaan keskitettyjen maksuerien avulla, näytettävä yritys on yritys, jolle maksu suoritetaan. Tapahtuma ei välttämättä näytä, mitkä yritysten laskut maksetaan.

Kunkin esiintymän nimi näkyy myös, jotta se voi tunnistaa maksatusehdotuksen.

Lisäksi näytetään kunkin esiintymän tila. Seuraavat tilat ovat käytössä:

- **Ajoitettu** – Maksatusehdotus on ajoitettu, mutta sitä ei ole vielä suoritettu.
- **Virhe** – Maksatusehdotus on suoritettu, mutta ilmeni virhe. Voit tarkastella virheitä valitsemalla **Näytä tulokset** -painikkeen.
- **Valmis** – Maksatusehdotus on suoritettu onnistuneesti. Voit tarkastella maksuja valitsemalla **Näytä maksut** -linkin. Tämä linkki avaa tapahtuman luoman maksukirjauskansion.

Kun maksut on tehty, voit tarkastella maksusummia kirjauskansiossa. Summat näytetään transaktiovaluuttana. Jos esimerkiksi maksukirjauskansio sisältää maksuja sekä Yhdysvaltain dollareina että Kanadan dollareina, kunkin valuutan kokonaismaksut näytetään. 

Voit poistaa maksukirjauskansion prosessin automaation luomisen jälkeen. Jos maksut poistetaan kokonaan, seuraavat tapahtumat toteutuvat:

- Viikon prosessiautomaation tila on edelleen **Valmis**.
- Prosessi poistaa maksun kokonaissummat, ja **Näytä maksut** -linkki korvataan **Näytä tulokset** -painikkeella.
- Kun tarkastelet tuloksia, näyttöön tulee sanoma, jonka mukaan alkuperäinen kirjauskansio poistettiin.

Kun olet poistanut laskun, laskut avataan uudelleen maksulle. Tämän jälkeen voidaan luoda uusi esiintymä laskujen maksamiseksi uudelleen.

## <a name="edit-a-vendor-payment-proposal-automation"></a>Toimittajan maksatusehdotuksen automatisoinnin muokkaus

Prosessiautomaatiojärjestelmän avulla voit muokata maksuja, sarjoja ja tapahtumia, jotka luodaan maksuehdotukselle. Sarjaa voi muokata joko **prosessin automatisointi** -sivulta tai prosessiautomaation viikkonäkymästä. Jos ostoreskontran esimies esimerkiksi päättää luoda kaikkien kotimaisten toimittajien sekit keskiviikkona maanantain asemesta, tämä voi löytää esiintymän viikkonäkymästä ja valita **Näytä/Muokkaa – sarjat**. Jos muokkaat sarjaa, järjestelmä kehottaa sinua määrittämään, tuleeko muutos tehdä kaikkiin aiemmin luotuihin esiintymiin vai vain uusiin esiintymiin. Historialliset esiintymät, joiden tila on jo **Päättynyt** tai jotka ovat päättyneet **Virhe**-tilaan, eivät muutu.

Voit myös lisätä uuden esiintymän tai muuttaa aiemmin luotua esiintymää. Esimerkiksi seuraava maksuehdotusesiintymä ajoitetaan suoritettavaksi keskiviikkona 1. tammikuuta, mutta päivämäärä on vapaapäivä. Voit muuttaa tapahtumaa joko prosessiautomaation viikoittaisesta näkymästä tai **Prosessin automatisointi** -sivulta. Näkyviin tulee sivu, jossa näkyvät aikataulutiedot ja maksuehdotusehdot. Tässä voit muokata ajoitettua kellonaikaa ja päivämäärää. Voit myös muokata maksuehdotuksen ehtoja, jos muutokset ovat pakollisia. Jos esimerkiksi muutat tapahtuman ajoitettua päivämäärää 1:stä tammikuuta - 2:seen tammikuuta, haluat ehkä muuttaa myös määräpäivämäärän suhteelliset päivämäärät.

Voit myös poistaa esiintymän tai sarjan käytöstä. Jos haluat poistaa esiintymän käytöstä ja keskeyttää sen käsittelyn, valitse se prosessiautomaation viikkonäkymässä ja valitse sitten **Poista käytöstä**. Voit poistaa sarjan käytöstä **Pprosessiautomaatio**-sivulla.

## <a name="security-for-payment-proposal-automations"></a>Maksatusehdotuksen automatisoinnin turvallisuus

Toimittajamaksujen ehdotusautomaatioita varten on lisätty seuraavat tehtävät ja oikeudet. Nämä tehtävät ja oikeudet ovat oletussuojausasetuksia, mutta niitä voidaan muuttaa organisaation tarpeiden mukaan. Esimerkiksi, jos ei vain ostoreskontran esimies, mutta myös ostoreskontran työntekijä voi muokata ja luoda aikataulun toistumisen, määrittää **ylläpidä aikataulun esiintymät** -velvollisuuden henkilölle ostoreskontran työntekijäroolissa.

| Tulli                              | Rooli                                                                       | Oikeudet |
|-----------------------------------|----------------------------------------------------------------------------|------------|
| Ylläpidä ajoitussarjaa          | Ostoreskontrapäällikkö                                                   | Tämä velvollisuus antaa oikeudet luoda ja ylläpitää maksuehdotuksen automaatiosarjoja ja esiintymiä seuraavien oikeuksien avulla:<ul><li>Ylläpidä ajoituksen esiintymiä</li><li>Ylläpidä ajoitussarjaa</li><li>ProcessScheduleOccurrenceListMaintain</li><li>Näytä esiintymät viikoittain -näkymä</li></ul> |
| Aikataulutapahtumien kysely | Ostoreskontran maksuvirkailija, ostoreskontran keskitetty maksuvirkailija | Tämä velvollisuus antaa oikeudet näyttää maksuehdotuksen automaatioesiintymiä seuraavien oikeuksien avulla:<ul><li>Näytä ajoituksen esiintymiä</li><li>Näytä esiintymä viikoittain -näkymä</li></ul> |
| Kohdista kyselyjä ajoitussarjoihin      | None                                                                       | Tämä velvollisuus antaa oikeudet näyttää sarjojen asetuksia ja esiintymiä seuraavien oikeuksien avulla:<ul><li>Näytä ajoituksen esiintymiä</li><li>Näytä esiintymät -luettelosivu</li><li>Näytä esiintymä viikoittain -näkymä</li></ul>|
| Ylläpidä ajoituksen esiintymiä     | None                                                                       | Tämä velvollisuus myöntää oikeuden luoda ja ylläpitää esiintymää seuraavien oikeuksien avulla:<ul><li>Ylläpidä ajoituksen esiintymiä</li><li>Näytä esiintymä viikoittain -näkymä</li></ul> |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
