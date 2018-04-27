---
title: Toimittajien aktivointi
description: "Tässä aiheessa käsitellään uusien toimittajien aktivointiprosessia. Siinä selitetään toiminnot, joita eri rooleilta edellytetään tämän prosessin aikana."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendProspectiveVendorRegistrationRequests,SysUserRequestListPage
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.3
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 325cf12345afcf531181f65a41d0e5262798c14f
ms.contentlocale: fi-fi
ms.lasthandoff: 04/13/2018

---

# <a name="onboard-vendors"></a>Toimittajien aktivointi
[!INCLUDE [banner](../includes/banner.md)]

---

Uudet toimittajat voidaan aktivoida ja rekisteröidä toimittajiksi Microsoft Dynamics 365 for Finance and Operations -sovelluksessa toimittajaa edustavalta henkilöltä kerättävien tietojen perusteella.

Prosessissa on seuraavat vaiheet, joissa eri roolit suorittavat järjestelmän tehtäviä.

1. **OData-tietojenhallinta** – yksikön tuonti – Alkuperäinen pyyntö on mahdollisen toimittajan rekisteröintipyyntö. Yleensä tämä pyyntö tulee lähteestä, kuten nimettömän käytön sallivasta asiakkaan ylläpitämästä sivustosta. Toimittajat voivat rekisteröityä antamalla perustiedot, kuten toimittajan nimen, perustelut ja organisaatiotunnuksen sekä yhteyshenkilön nimen ja sähköpostiosoitteen. Pyynnöt tuodaan tiedonhallintaliittymään kautta.
2. **Mahdollisen toimittajan rekisteröintipyyntö -luettelosivu** – Hankinta-asiantuntija päättää mahdollisen toimittajan rekisteröintipyynnössä annettujen tietojen perusteella aktivoidaanko toimittaja. Hankinta-ammattilainen tarkastelee saapuvaa pyyntöä Finance and Operationsin **Mahdollisen toimittajan rekisteröintipyynnöt** -luettelosivulla.
3. **Käyttäjien varaustyönkulku** – Kun hankinta-ammattilainen on tarkistanut saapuvan pyynnön tiedot ja päättänyt jatkaa aktivointiprosessia, käyttäjäpyynnön työnkulku valmistelee uuden käyttäjän ja lähettää sähköpostikutsun, jonka avulla yhteyshenkilö voidaan hyväksyä Microsoft Dynamics 365:n todennetuksi käyttäjäksi.
4. **Ohjattu toimittajan rekisteröintitoiminto** – Toimittajan yhteyshenkilö kirjautuu Finance and Operationsiin uudella käyttäjätilillä. Yhteyshenkilö suorittaa ohjatun toimittajan rekisteröintitoiminnon loppuun ja antaa esimerkiksi seuraavat tiedot: osoitteet, liiketoimintatiedot, hankintaluokat ja kyselylomakkeen vastaukset.
5. **Hyväksyntätyönkulku** – Rekisteröintitiedot sisältävä toimittajapyyntö luodaan. Toimittajapyyntö lähetetään työnkulkuun, jossa se reititetään tarkistettavaksi ja hyväksyttäväksi.
6. **Toimittajan päätietojen luonti ja käyttäjäroolin muokkaus** – Hyväksytylle toimittajapyynnölle luodaan toimittajatietue. Toimittajan yhteyshenkilön käyttäjätilille joko myönnetään käyttöoikeus toimittajayhteistyötä varten tai tili poistetaan käytöstä.

Seuraavassa taulukossa on prosessiin liittyvät vaiheet ja roolit.

| Rooli ja prosessi       | OData-tietojenhallinta – yksikön tuonti | Mahdollisen toimittajan rekisteröintipyyntö -luettelosivu | Käyttäjien varaustyönkulku | Ohjattu toimittajan rekisteröintitoiminto | Hyväksyntätyönkulku | Toimittajan päätietojen luonti ja käyttäjäroolin muokkaus |
|--------------------------|---|---|---|---|---|---|
| System                   | Uutta toimittajaa koskeva pyyntö tuodaan. | | | | | Toimittajatietue luodaan, kun toimittajapyyntö on hyväksytty. |
| Hankinta-asiantuntija | | Aloita aktivointiprosessi. | | | Tarkista toimittajapyyntö ja joko hyväksy tai hylkää se. | |
| Järjestelmänvalvoja            | | | Luo käyttäjä Finance and Operationsissa ja Microsoft Azuressa. | | | |
| Toimittajan yhteyshenkilö    | | | Lähetä sähköposti yhteyshenkilölle. | Rekisteröi toimittajan tiedot. | | |

Toimittajan aktivointiprosessi esitellään nopeasti tässä lyhyessä YouTube-videossa: 
> [!Video https://www.youtube.com/embed/0KUc3AGaTKk]

## <a name="importing-the-prospective-vendor-registration-request"></a>Mahdollisen toimittajan rekisteröintipyynnön tuominen

Mahdollisen toimittajan rekisteröintipyyntö on Finance and Operationsin yksikkö. Voit määrittää järjestelmän tuomaan tietoja tämän yksikön kautta. 

Seuraavassa, tuotavassa taulukossa on tähän yksikköön sisältyvät tiedot.

| Kenttä                        | kuvaus |
|------------------------------|-------------|
| Toimittajan nimi                  | Toimittajan nimi. |
| Liiketoimintaperuste       | Toimittajapyynnön syyt. |
| Organisaatiotunnus          | Virallinen, tunnistettu rekisteröintinumero. |
| Toimiala             | Toimittajan toimiala. |
| Yhteyshenkilön etunimi  | Sen henkilön etunimi, joka kutsutaan rekisteröimään toimittajan tiedot. |
| Yhteyshenkilön toinen nimi. | Sen henkilön toinen nimi, joka kutsutaan rekisteröimään toimittajan tiedot. |
| Yhteyshenkilön sukunimi   | Sen henkilön sukunimi, joka kutsutaan rekisteröimään toimittajan tiedot. |
| Yhteyshenkilön sähköpostiosoite       | Sähköpostiosoite, jolla uusi käyttäjä luodaan Finance and Operationsissa ja joka rekisteröidään vuokraajan Azure Active Directory (Azure AD) -tilillä. |
| Lähetyspäivämäärä               | Päivämäärä, jolloin tarjouspyyntö luotiin ulkoisessa järjestelmässä. |
| Oikeushenkilö                 | Yritys, jonka toimittajaksi toimittaja haluaa tulla. Tämän arvon on oltava Finance and Operationsiin rekisteröity yrityksen koodi. Jos arvoa ei saada tuontiprosessin kautta, käytetään hankintaparametreista saatavaa arvoa. |
| Toimittajan tyyppi                  | Toimittaja voi olla organisaatio tai henkilö. Toimittaja tyyppi määrittää, miten toimittaja luodaan lopuksi. |

Kun mahdollisen toimittajan rekisteröintipyyntö on tuotu, se näkyy **Mahdollisen toimittajan rekisteröintipyyntö** -luettelosivulla. Hankinta-asiantuntija voi kutsua käyttäjän tältä luettelosivulta. Käyttäjän valmisteluun liittyvä käyttäjäpyyntö lähetetään työnkulkuun.

## <a name="submitting-a-prospective-vendor-user-request"></a>Mahdollisen toimittajan käyttäjäpyynnön lähettäminen

Mahdollisen toimittajan käyttäjäpyynnön tarkoitus on valmistella alkuperäisen pyynnön lähettänyt käyttäjä siten, että kyseinen käyttäjä voi kirjautua Finance and Operationsiin mahdollisen toimittajan rekisteröintipyynnössä ilmoitetulla sähköpostitilillä.

Käyttäjäpyynnön työnkulku käsittelee mahdollisen toimittajan käyttäjäpyynnön. Tämä työnkulku siirtää tietoja Azure AD B2B -yhteiskäytön avulla. Se luo Finance and Operationsiin käyttäjän, jolla on soveltuvat käyttöoikeudet.

Uusille käyttäjille määritetään seuraavat käyttöoikeusroolit:

- Järjestelmän ulkoinen käyttäjä
- Mahdollinen toimittaja (ulkoinen)

Uusi käyttäjä vastaanottaa sähköpostiviestin, jonka käyttäjäpyynnön työnkulku on luonut. Tämä sähköposti pyytää käyttäjää kirjautumaan järjestelmään.

Lisätietoja sähköpostin määrityksistä ja yleisesti työnkulusta on käyttöpyynnön työnkulkua käsittelevässä kohdassa aiheessa [Toimittajayhteistyön määrittäminen ja hallinta](set-up-maintain-vendor-collaboration.md).

## <a name="vendor-registration"></a>Toimittajan rekisteröinti

Mahdollisen toimittajan Finance and Operationsin kirjautuva käyttäjä näkee ohjatun toimittajan rekisteröintitoiminnon ensimmäisen sivun, jossa käyttäjä voi antaa toimittajan tiedot.

Ohjattu toiminto vastaa toimittajapyynnön määritystä. Maa tai alue, jossa toimittaja harjoittaa liiketoimintaa, määrittää, mitä tietoja ohjatussa toiminnossa kysytään ja mitkä tiedot ovat pakollisia.

Lisätietoja toimittajapyynnön määrityksestä on aiheessa [Toimittajayhteistyön määritys ja ylläpito](set-up-maintain-vendor-collaboration.md). Seuraavassa taulukossa on yhteenveto ohjatun toiminnon sivuista ja kunkin sivun tarkoituksesta.

| Sivu                       | kuvaus |
|----------------------------|-------------|
| Maa/alue             | Maa tai alue määrittää myöhemmillä ohjatun toiminnon sivuilla käytettävät toimittajapyynnön määritykset. Se määrittää myös **Veron tila** haun arvot. |
| Ehdot       | Toimittajapyynnön määritykset määrittävät, onko tämä sivu käytettävissä. Jos se on käytössä, käyttäjän on hyväksyttävä ehdot ennen jatkamista. |
| Toimittajatiedot         | Tällä sivulla on toimittajan nimi, joka lisätään automaattisesti alkuperäisestä mahdollisen toimittajan rekisteröintipyynnöstä. Siinä on myös organisaatiotunnus, toimittajan puhelinnumero, faksinumero ja sähköpostiosoite sekä toimittajan osoitteita eri tarkoituksia varten. |
| Yhteyshenkilön tiedot | Tällä sivulla on yhteyshenkilön nimi, joka lisätään automaattisesti alkuperäisestä mahdollisen toimittajan rekisteröintipyynnöstä. Siinä on myös yhteyshenkilön puhelinnumero ja sähköpostiosoite sekä yhteyshenkilön osoitteita eri tarkoituksia varten. |
| Liiketoimintatiedot       | Tällä sivulla verorekisteröintinumeroita (eri maita ja alueita varten) ja työntekijöiden määrä. Siinä ilmoitetaan myös, onko yritys vähemmistöön kuuluvan henkilön omistuksessa. |
| Hankintaluokat     | Tällä sivulla on tietoja hankintaluokista, joiden hyväksyntää toimittaja pyytää. Käyttäjä voi valita hankintaluokkahierarkian luokkia. Voit määrittää näytettävien hierarkiatasojen määrän valitsemalla **Hankintaparametrit** &gt; **Toimittajayhteistyö** kohdassa **Hankinta** &gt; **Asetukset**. |
| Kyselylomakkeet             | Ohjatussa toiminnossa voi olla toimittajalle suunnattuja kyselylomakkeita. Ohjatussa toiminnossa näkyvät kyselylomakkeet on määritetty joko toimittajapyynnössä tai hankintaluokittain. Jos kyselylomake on määritetty hankintaluokittain, hankintaluokat, joiden hyväksymistä toimittaja pyytää, määrittävät ohjatussa toiminnossa näkyvät kyselylomakkeet. Voit lisätä **Hankintaluokat**-sivulla kyselylomakkeen sopivaan luokkaan ja määrittää tehtävätyypiksi **Toimittajan aktivointi**. |

Toimittajapyyntö luodaan, kun mahdollisen toimittajan käyttäjä on suorittanut ohjatun toimittajan rekisteröintitoiminnon.

## <a name="manually-or-automatically-submit-a-vendor-request"></a>Toimittajapyynnön lähettäminen manuaalisesti tai automaattisesti

Toimittajapyyntö voidaan luoda luonnoksena ja lähettää manuaalisesti työnkulkuun. Toimittajapyyntö voidaan vaihtoehtoisesti lähettää automaattisesti työnkulkuun, kun ohjattu toimittajan rekisteröintitoiminto on suoritettu loppuun. Pyyntö voidaan lähettää manuaalisesti, jos hankinta-asiantuntija haluaa esimerkiksi arvioida, onko pyyntö reititettävä hyväksyntäprosessin kautta ennen työnkulkuun lähettämistä.

- Valitse ensin **Hankintaparametrit** &gt; **Toimittajayhteistyö** ja sitten **Lähetä mahdollisen toimittajan rekisteröinti työnkulkuun automaattisesti**, jos haluat määrittää toimittajapyynnön, joka lähetetään automaattisesti työnkulkuun, kun ohjattu toimittajan rekisteröintitoiminto on suoritettu.

## <a name="vendor-requests"></a>Toimittajapyynnöt

Toimittajapyyntöjä voi käyttää **Toimittajayhteistyön käyttäjäpyynnöt** -sivulla.

Toimittajapyyntö sisältää mahdollisen toimittajakäyttäjän ohjatussa toimittajan rekisteröintitoiminnossa antamat tiedot.

Pyynnön ansiosta voit tarkastella toimittajan tietoja ja päättää, tuleeko toimittajassa rekisteröity toimittaja Finance and Operationsissa.

Toimittajapyyntö on lähetettävä työnkulkuun ja se on reititettävä soveltuville tarkistajille ja hyväksyjille. Perustietoja työnkulkujen määrittämisestä on kohdassa [Hankinnan työnkulut](procurement-sourcing-workflows.md).

Seuraavassa taulukossa on tilat, joita toimittajapyynnöillä voi olla.

| Tila                     | kuvaus |
|----------------------------|-------------|
| Luonnos                      | Toimittajapyyntöä ei ole vielä lähetetty. |
| Pyyntö lähetetty          | Toimittajapyyntö on lähetetty ja työnkulun ensimmäinen vaihe on käsitelty. |
| Odottava tarkistus             | Jos työnkulkutehtävällä on useita tarkistajia, tarkistaja voi hyväksyä toimittajapyynnön tarkistustehtävän ja suorittaa tarkistuksen. Jos tarkistajia on vain yksi, osallistuja voi suorittaa tarkistuksen valitsemalla työnkulkutoiminnossa **Valmis**. Kyseisen henkilön ei tarvitse hyväksyä työnimikettä ensin. |
| Pyyntö odottaa hyväksyntää   | Toimittajapyyntö on reititetty osallistujille hyväksyttäväksi. Käytössä on myös mahdollisuus pyytää lisätietoja. Lisätietojen pyytäminen voi aiheuttaa työnimikkeen reitittämisen takaisin lähettäjälle. Toimittajapyyntö voidaan myös hyväksyä tai hylätä tässä tilassa. |
| Hakemuksen muutospyyntö | Hyväksyjä on pyytänyt lisätietoja ja toimittajapyyntö on reititetty toimittajapyynnön lähettäneelle henkilölle. Lähettäjä voi lisätä tarvittavat tiedot ja lähettää sitten toimittajapyynnön uudelleen. Jos toimittajapyyntö on lähetetty uudelleen, sen tilaksi palautetaan **Pyyntö odottaa hyväksyntää**. |
| Pyyntö hyväksytty           | Tämä tila on lopullinen tila. |
| Pyyntö hylätty           | Tämä tila on lopullinen tila. |

## <a name="approving-a-vendor-request"></a>Toimittajapyynnön hyväksyminen

Toimittajapyynnön hyväksymisen jälkeen luodaan toimittajatili. Alkuperäisen mahdollisen toimittajan rekisteröintipyynnön ja toimittajapyynnön tilana on **Hyväksytty**.

Valitse toimittajaryhmä ennen toimittajapyynnön hyväksymistä valitsemalla **Uusi toimittaja** -sivun **Yleiset**-pikavälilehdessä **Toimittajaryhmä**.

Jos mahdollisella toimittajakäyttäjällä on oltava Finance and Operationsin käyttöoikeus toimittajaa edustavana toimittajayhteistyökäyttäjänä, määritä toimittajayhteistyön käyttöoikeudeksi **Kyllä**. Jos haluat poistaa käytöstä käyttäjätilin, jolla mahdollinen toimittaja rekisteröityi, määritä käyttöoikeusasetukseksi **Ei**.

Jos toimittajayhteistyön käyttöoikeudeksi on määritetty **Kyllä** toimittajapyyntöä hyväksyttäessä, lähetetään pyyntö käyttäjän roolien muokkaamisesta vastaamaan **Ulkoiset roolit** -kohdan **Toimittaja**-tyypille määritettyjä rooleja. Jos käyttöoikeudeksi on valittu tässä kohdassa **Ei**, käyttäjän poistamista käytöstä pyydetään, kun toimittajapyyntö hyväksytään. Siinä tapauksessa on määritettävä käyttäjän käytöstäpoistamisen työnkulku.

Jotta toimittajatili voitaisiin luoda toimittajapyynnön hyväksymisen yhteydessä, toimittajapyynnöistä luotavien toimittajien numerojärjestyksen asetukseksi on määritettävä **Automaattinen**.

Yhteenveto toimittajayhteistyökäyttäjän käyttöoikeuksista on kohdassa [Toimittajayhteistyön määrittäminen ja hallinta](set-up-maintain-vendor-collaboration.md).

## <a name="rejecting-a-vendor-request"></a>Toimittajapyynnön hylkääminen

Jos toimittajapyyntö on hylätty, hylkäyksen syy on valittava toimittajapyynnössä.

Kun toimittajapyyntö hylätään, pyyntö lähetetään, jotta käyttäjä voidaan poistaa käytöstä. Siinä tapauksessa on määritettävä käyttäjän käytöstäpoistamisen työnkulku. Lisätietoja on kohdassa [Toimittajayhteistyön määrittäminen ja hallinta](set-up-maintain-vendor-collaboration.md).

Toimittajapyynnön hylkäämisen alkuperäisen mahdollisen toimittajan rekisteröintipyynnön ja toimittajapyynnön tilana on **Hylätty**.

## <a name="deleting-a-prospective-vendor-registration-request-in-various-statuses"></a>Eri tiloissa olevan mahdollisen toimittajan rekisteröintipyynnön poistaminen

Mahdollisen toimittajan rekisteröintipyynnön eri tilat luovat yleiskuvan pyynnön etenemisestä.

**Poista**-toiminnon käyttö mahdollisen toimittajan rekisteröintipyynnössä puhdistaa ja poistaa luodun tietueketjun. Voit myös poistaa käyttäjätilin käytöstä. **Poista**-toiminnon seuraukset vaihtelevat mahdollisen toimittajan rekisteröintipyynnön mukaan seuraavan taulukon mukaisesti.


|          Tila          |                                                                                     Tilan kuvaus                                                                                      |                                                                                                                                                            Poista-toiminnon tulos                                                                                                                                                             |
|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|           Uusi            |                                                                         Pyynnössä ei ole tehty mitään toimintoja.                                                                          |                                                                                                                                              Mahdollisen toimittajan rekisteröintipyyntö on poistettu.                                                                                                                                               |
|      Käyttäjän pyytämä      | Kun valitset <strong>Kutsu käyttäjä</strong>, tilaksi tulee <strong>Käyttäjän pyytämä</strong>. Lisäksi luodaan mahdollisen toimittajan käyttäjäpyyntö, ja se lähetetään käyttäjäpyynnön työnkulkuun. |                                                                                                          Jos tämä on mahdollisen toimittajan rekisteröintipyynnön tila, sitä ei voi poistaa, koska käyttäjäpyynnön työnkulku ei ole päättynyt.                                                                                                          |
|       Käyttäjä kutsuttu       |                                                               Käyttäjäpyynnön työnkulku on hyväksytään ja käyttäjä luodaan.                                                               |                                                                                                                      Käyttäjän käytöstäpoistopyyntö luodaan ja mahdollisen toimittajan rekisteröintipyyntö poistetaan.                                                                                                                      |
| Rekisteröinti on käynnissä |                                                         Uusi käyttäjä on kirjautunut sisään ja käynnistänyt ohjatun toimittajan rekisteröintitoiminnon.                                                          |                                                                                     Käyttäjän käytöstäpoistopyyntö luodaan sekä mahdollisen toimittajan rekisteröintipyyntö ja ohjatussa toimittajan rekisteröintitoiminnossa annetut tiedot poistetaan.                                                                                      |
|  Toimittajapyyntö luotu  |                                                                     Ohjattu toimittajan rekisteröintitoiminto on suoritettu.                                                                      | Käyttäjän käytöstäpoistopyyntö luodaan sekä mahdollisen toimittajan rekisteröintipyyntö, ohjatussa toimittajan rekisteröintitoiminnossa annetut tiedot ja toimittajapyyntö poistetaan.<blockquote>[!NOTE]<br><strong>Poista</strong>-toimintoa ei voi käyttää, kun toimittajapyyntö on työnkulun tarkistusvaiheessa.</blockquote> |
|         Hyväksytty         |                                                                               Toimittajapyyntö hyväksytään.                                                                               |                                                                                                   Mahdollisen toimittajan rekisteröintipyyntö, ohjatussa toimittajan rekisteröintitoiminnossa annetut tiedot ja toimittajapyyntö poistetaan.                                                                                                    |
|         Hylätty         |                                                                               Toimittajapyyntö hylätään.                                                                               |                                                                                                   Mahdollisen toimittajan rekisteröintipyyntö, ohjatussa toimittajan rekisteröintitoiminnossa annetut tiedot ja toimittajapyyntö poistetaan.                                                                                                    |


