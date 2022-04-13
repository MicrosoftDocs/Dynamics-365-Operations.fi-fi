---
title: Laskutusaikataulujen luominen
description: Tässä aiheessa kerrotaan, miten laskutusaikatauluja luodaan, poistetaan ja muokataan.
author: JodiChristiansen
ms.date: 02/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 2c4e3c0edadd00fd3a3f2ae9968248a226147996
ms.sourcegitcommit: c0f7ee7f8837fec881e97b2a3f12e7f63cf96882
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/22/2022
ms.locfileid: "8462584"
---
# <a name="create-billing-schedules"></a>Laskutusaikataulujen luominen

[!include [banner](../includes/banner.md)]

**Laskutustaikataulu**-sivulla voit luoda, poistaa ja muokata laskutusaikatauluja. Voit myös tarkastella laskutusaikataulujen luetteloa. Kun luot laskutusaikataulun, sen oletusarvot määrittää siihen liittyvä laskutusryhmä. Lisätietoja määritetään **Toistuvan sopimuslaskutuksen parametrit** -sivulla.

## <a name="create-a-billing-schedule"></a>Laskutusaikataulun luominen

Voit luoda laskutusaikataulun seuraavien ohjeiden avulla.

1. Valitse **Laskutusaikataulu**-sivulla **Uusi**.
2. Valitse **Luo laskutusaikataulu**-valintaruudun **Laskutusaikatauluryhmä**-kentässä laskutusaikatauluryhmä.
3. Valitse **Asiakastili**-kentässä asiakastili.
4. Valitse **Aloituspäivämäärä**-kentässä aloituspäivämäärä ja syötä sitten **Kausien määrä** -kenttään kausien määrä. **Päättymispäivämäärä**-kenttä päivitetään syötetyn kausimäärän perusteella. Jos päivität **Laskutuksen päättymispäivä** -kenttää **Kausien määrä** -kentän arvoksi päivittyy **0** (nolla).
5. Valitse **OK**.
6. Syötä **Laskutusaikataulu**-sivun **Yleistä**-välilehden **Kuvaus**-kenttään laskutusaikataulun kuvaus.
7. Valitse **Tavoitemalli**-kentässä tavoite **Tavoitteisiin perustuvalle laskutukselle**.

**Laskutustili**- ja **Valuuttakoodi**-kenttien kaltaiset kentät päivitetään asiakkaalta saaduilla tiedoilla.

Kentät **Laskutustiheys** ja **Laskutusväli** määrittyvät automaattisesti valitun laskutusaikatauluryhmän perusteella.

8. Voit luoda erillisiä laskuja määrittämällä **Laskuta erikseen** -asetuksen arvoksi **Kyllä**.
9. Jos haluat uusia laskutusaikataulun automaattisesti viimeisen laskutuskauden jälkeen, määritä **Uusi automaattisesti** -asetuksen arvoksi **Kyllä** ja määritä sitten **Uusimista kohden lisättävät rivit** -kenttä.

**Parametrit**-kentät määrittyvät automaattisesti **Toistuvan sopimuslaskutuksen parametrit** -sivun arvojen perusteella.

10. Voit laskea laskutusaikataulun summan suhteellisesti määrittämällä **Laske osittaiset kaudet suhteellisesti** -asetuksen arvoksi **Kyllä**.
11. Jos haluat tasata laskutusaikataulun tietorivit kuukauden lopussa, määritä **Tasaa kuukauteen** -asetuksen arvoksi **Kyllä**.
12. Syötä sopimuksen alkamis- ja päättymispäivät kenttiin **Sopimuksen alkamispäivämäärä** ja **Sopimuksen päättymispäivämäärä**. Nämä päivämäärät ovat vain tiedoksi.

**Maksu**-kentässä näkyy asiakkaalta peräisin olevat asiakkaan maksutiedot. Kun rivinimike on pidossa tai lopetetaan, maksutietoja ei voi muuttaa.

> [!NOTE]
> Kun konsolidoit laskuja nimikkeen mukaan, kenttien **Maksuehdot**, **Menetelmä** ja **Laskutusaikataulu** on täsmättävä. Muuten laskuja ei voi konsolidoida.

13. **Osoite**-välilehdessä voit tarkastella ja päivittää kenttiä **Toimitusosoite** ja **Laskutusosoite**.
14. **Yhteystiedot**-välilehdellä voit yhdistää loppukäyttäjätilin laskutusaikatauluun.
15. **Yhteystiedot**-kenttiin voit syöttää yhteyshenkilön, sähköpostiosoitteen ja verkko-osoitteen.
16. kumppaniprovisiotietoja voit seurata määrittämällä kentät **Kumppanitili** ja **kumppaniprovisioprosentti**. Nämä kentät ovat vain tiedoksi.
17. **Yhteensä**-välilehdessä voit tarkastella eri summia, jotka on laskettu laskutusaikataululle.
18. **Pito**-välilehdessä voit tarkastella auditointitietoja siitä, milloin laskutusaikataulu on asetettu pitoon ja milloin se on otettu siitä pois.
19. **Päättyminen**-välilehdessä voit tarkastella lopetuksia, joita sovellettiin laskutusaikatauluun tai poistetiin siitä.
20. Valitse **Tallenna**.
21. Valitse **Laskutusaikataulurivit**-pikavälilehdessä **Lisää rivi**.
22. Valitse **Nimiketunnus**-kentässä nimikkeen numero. Jos lisättävä nimike on tuottojaon päänimike, rivit päivitetään automaattisesti alinimikkeillä. Voit muokata vain tuottojaon päänimikettä. Kaikki alikohteet päivitetään sen mukaisesti.
23. Valitse **Nimiketyyppi**-kentässä nimikkeen tyyppi.
24. Päivitä alkamis- ja päättymispäivät.
25. Ennen laskujen luomista voit muuttaa laskutustiheyttä päivittämällä **Laskutustiheys**-kentän. Kun laskutusaikataulun ensimmäinen lasku on luotu, laskutustiheyttä ei voi muuttaa.
26. Valitse nimikkeen määrän mittayksikkö **Yksikkö**-kentästä.
27. Valitse nimikkeen **Hinnoittelutapa**-kentässä nimikkeen hinnoittelutapa.

**Yksikköhinta** määräytyy automaattisesti varaston perusteella. Voit kuitenkin päivittää sen, jos muutat hinnoittelutavaksi **Kiinteä**.

## <a name="remove-a-line-item"></a>Rivinimikkeen poistaminen

Voit poistaa nimikkeen laskutusaikataulusta seuraavien ohjeiden avulla.

1. Valitse **Laskutusaikataulu**-sivun **Aikataulunumero** -kentässä muokattavan laskutusaikataulun numero.
2. Valitse **Laskutusaikataulun rivit** -pikavälilehdestä poistettavat rivit ja valitse sitten **Poista**.
3. Valitse **Tallenna**.

Tämän aiheen loppuosassa kuvat toiminnot ja tiedot, jotka ovat käytettävissä **Laskutusaikataulurivit**-pikavälilehdessä.

## <a name="billing-schedule-line-actions"></a>Laskutusaikataulun rivitoiminnot

**Laskutusaikataulurivit**-pikavälilehden painikkeiden avulla voit kohdistaa toimintoja yksittäisille riveille.

| Painike | Kuvaus |
|--------|-------------|
| Lisää rivi | Lisää rivi laskutusaikatauluun. |
| Lisää nimikeluettelosta | Lisää useita rivejä laskutusaikatauluun valitsemalla ne luettelosta. |
| Poista | <p>Poista valittu rivi laskutusaikataulusta.</p><p>Tuottojakoon kuuluvissa nimikkeissä voit poistaa vain päänimikkeen. Kaikki siihen liittyvät alinimikkeet poistetaan silloin automaattisesti.</p> |
| Näytä laskutustiedot | Näytä laskutustiedot. |
| Lopeta | <p>Päätä valitut rivit. Tämä painike on käytettävissä vain, kun valittujen rivien tilana on **Aktiivinen**.</p><p>Tuottojakoon kuuluvissa nimikkeissä voit lopettaa vain päänimikkeen.</p> |
| Poista irtisanominen | <p>Poista lopetus valituilta riveiltä. Tämä painike on käytettävissä vain, kun valittujen rivien tilana on **Päätetty**.</p><p>Tuottojakoon kuuluvissa nimikkeissä voit poistaa lopetuksen vain päänimikkeeltä.</p> |
| Paikanvaraaja | <p>Valitse tiedot valitun rivin pitoon asettamista varten.</p><p>Tuottojakoon kuuluvissa nimikkeissä voit asettaa pitoon vain päänimikkeen.</p> |
| Poista pito | <p>Poista pito valitulta riviltä.</p><p>Tuottojakoon kuuluvissa nimikkeissä voit poistaa pidon vain päänimikkeeltä.</p> |
| Eskalointi ja alennus | Tämä painike ei ole käytettävissä tuottojakoon kuuluvissa nimikkeissä lukuun ottamatta päänimikkeitä, joissa jaossa käytetään **Nollamäärä**-kohdistusmenetelmää. |
| Lykkäykset | <p>Syötä valitun rivin lykkäysasetukset.</p><p>Tämä painike ei ole käytettävissä tuottojaon päänimikkeiden osalta.</p> |
| Välitavoitteen kohdistus | <p>Tarkista ja päivitä valitun rivin tavoitteenkohdistustiedot.</p><p>Tämä painike on käytettävissä vain, kun laskutusaikataulun rivinimike on tavoitenimike.</p> |
| Tuki ja uusiminen | <p>Tarkista ja päivitä valitun rivin tuki- ja uusimistiedot.</p><p>Tämä painike on käytettävissä vain, kun laskutusaikataulun rivinimike on tuki- tai uusimisnimike.</p> |
| Näytä dimensiot | Näytä tai piilota dimensiosarakkeet, jotka tulevat näkyviin **Laskutusaikataulurivit**-ruudukossa. |
| Laske yksikköhinta | <p>Laske nimikkeen yksikköhinta, jotta asiakas voi maksaa sopimussumman erissä (esimerkiksi päivittäin, kuukausittain, neljännesvuosittain, puolivuosittain tai vuosittain). Voit valita sopimushinnan ja hintatiheyden.</p><p>Voit tarkastella muutosten kirjausketjua: vanhaa sopimushintaa ja -taajuutta, uutta sopimushintaa ja -taajuutta, muutoksen tehnyttä käyttäjää sekä muutoksen päivämäärää ja kellonaikaa.</p> |
| Tasauspäivä | <p>Määritä uusimisnimikkeiden kohdistuspäivämäärä.</p><p>Jos valitset **Nimikeryhmä**-kentästä nimikeryhmän, kaikissa nimikkeissä käytetään ensimmäisen nimikkeen kohdistuspäivää laskutusaikataulun nimikeryhmässä. Jos **Nimikeryhmä**-kenttä on tyhjä, voit määrittää kaikissa nimikkeissä käytettävän kohdistuspäivän.</p><p>Tämä painike on käytettävissä vain, jos **Laskutustiheys**-kentän arvoksi on valittu **Vuosittain**.</p> |
| Laskuttamaton tuotto | <p>Määritä nimike käyttämään laskuttamattoman tuoton toimintoa. Tämän jälkeen voit määrittää nimikkeen laskuttamattoman tuoton ja laskuttamattoman alennuksen tilit.</p><p>Tämä painike on käytettävissä vain nimikkeissä, joissa **Nimiketyyppi**-kentän arvo on **Vakio**. Se ei ole käytettävissä olemassa oleville laskutusaikatauluille tai laskutusaikatauluriveille, joiden osalta lasku on jo luotu.</p> |
| Lisää tuoton jaon alituotto | <p>Valitse myyntitilaukseen lisättävä alinimike.</p><p>Tämä painike on käytettävissä vain tuottojaon päänimikkeiden osalta.</p> |
| Erityishinnoittelun asetukset | Muokkaa nimikkeen hinnoitteluasetuksia. |

## <a name="billing-schedule-line-details"></a>Laskutusaikataulun rivitiedot

Kun valitset rivin **Laskutusaikataulurivit**-pikavälilehdestä, voit tarkastella kyseisen rivin yksityiskohtia. Nämä tiedot on jaettu eri välilehdille.

### <a name="general-tab"></a>Yleinen-välilehti

**Yleistä** -välilehdessä on seuraavat tiedot.

| Kenttä tai osa | Kuvaus |
|------------------|-------------|
| Käyttö | <p>Tässä osassa annetaan tietoja kulutusnimikkeistä. Se sisältää seuraavat kentät:</p><ul><li>**Kulutustunniste** – Mittarin tai kulutusnimikkeen tunnus.</li><li>**Lukuvaihtoehto** – Kulutuksenlukuasetus: **Lukema** tai **Kulutus**.</li><li>**Arvioitu kulutus** – Määritä sellaisen kulutusnimikkeen arvioitu kulutus, jolla on kausia, joille laskua ei ole luotu. **Laskutustiedot**-sivulla voit tarkastella arvioidun kulutuksen laskutusrivitietoja.</li></ul> |
| Ulkoiset viittaukset\* | Tämä osa sisältää kentät **Ulkoinen** ja **Rivinumero**, joilla voit määrittää ulkoisia viitetietoja. |
| Tavoite | <p>Tässä osassa annetaan tietoja tavoitenimikkeistä. Se sisältää **Arvioitu valmistumispäivä**, jossa näkyy nimikkeen valmistumispäivä.</li></ul> |
| Teksti | Riviin liittyvä kommentti. Teksti käännetään asiakkaan tai yrityksen oletuskielelle. |
| Nimikeryhmä | Rivinimikkeen nimikeryhmä. |
| Tasauspäivä | Laskutusaikataulun kohdistuspäivämäärä. |

\* Kun konsolidoit laskuja nimikkeen perusteella **Luo lasku** -sivulla **Ulkoinen viite** -kenttien on täsmättävä. Jos niissä on yhdenkin merkin ero, nimikkeitä ei konsolidoida laskussa. **Ulkoinen viite** -osan kummassakaan kentässä ei suoriteta vahvistustarkastusta, ja **Rivinumero**-kentän arvon on oltava positiivinen kokonaisluku.

### <a name="address-tab"></a>Osoitevälilehti

**Osoite**-välilehdessä on seuraavat tiedot.

| Kenttä | Kuvaus |
|-------|-------------|
| Toimitusosoite | <p>Valitse rivinimikkeen toimitusosoite. Oletusarvoinen toimitusosoite on **Osoite**-pikavälilehden ensisijainen toimitusosoite.</p><p>Kun muutat osoitetta, voit valita seuraavat osoiteasetukset:</p><ul><li>**Osoitteet** – Valitse osoite nykyiselle asiakkaalle.</li><li>**Käytössä** – Valitse osoite, jota tällä hetkellä käytetään nykyisen asiakkaan osalta.</li><li>**Muu osoite** – Valitse osoite mille tahansa asiakastietueelle.</li></ul><p>Nimikkeissä, joissa käytetään tuottojakoa, voidaan muokata vain päänimikkeen osoitetta. Alinimikkeiden osoite vastaa päänimikkeen osoitetta, eikä sitä voi muuttaa erikseen.</p> |
| Laskutusosoite | <p>Valitse rivinimikkeen laskutusosoite. Oletusarvoinen toimitusosoite on **Osoite**-pikavälilehden ensisijainen toimitusosoite. Voit muuttaa osoitetta tarpeen mukaan käytettävissä olevien ositteiden tarkoituksen mukaan:</p><ul><li>Jos yhdelläkään osoitteista ei ole tarkoitusta **Lasku**, oletusarvoinen laskutusosoite on tarkoituksesta riippumatta asiakkaan ensisijainen osoite.</li><li>Jos vähintään yhdellä osoitteella on tarkoitus **Lasku**, oletusarvoinen laskutusosoite on viimeksi syötetty osoite.</li><li>Jos vähintään yhdellä osoitteella on tarkoitus **Lasku** ja yksi laskutusosoitteista on määritetty ensisijaiseksi osoitteeksi, oletusarvoinen laskutusosoite on se osoite, jolla on tarkoitus **Lasku** ja joka on määritetty ensisijaiseksi osoitteeksi.</li><li>Nimikkeissä, joissa käytetään tuottojakoa, voidaan muokata vain päänimikkeen osoitetta. Alinimikkeiden osoite vastaa päänimikkeen osoitetta, eikä sitä voi muuttaa erikseen.</li></ul> |

### <a name="product-tab"></a>Tuotevälilehti

**Tuote**-välilehdessä on seuraavat tiedot.

| Kenttä tai osa | Kuvaus |
|------------------|-------------|
| Varastodimensiot | <p>Tässä osassa näkyvät nimikkeen varastotiedot. Se sisältää **Sarjanumero**-kentän, jossa näkyy nimikkeen sarjanumero.</p><p>Sarjanumero kopioidaan alkuperäisestä myyntitilauksesta tuki- ja uusimisprosessin aikana. Nimikkeissä, joissa käytetään tuottojakoa, päänimikkeen sarjanumero kopioidaan kaikkiin alinimikkeisiin. Sarjanumero kopioidaan, kun **Kopioi sarjanumero** -asetuksen arvona on **Kyllä** **Toistuvan sopimuslaskutuksen parametrit** -sivulla.</li></ul> |
| Tuotedimensiot | Nimikkeen tuotetiedot ja arvot päivitetään automaattisesti laskutusaikatauluriville valitun **Varianttinumero**-arvon perusteella. |

### <a name="account-tab"></a>Tilivälilehti

**Tili**-välilehdessä on seuraavat tiedot.

| Kenttä | Kuvaus |
|-------|-------------|
| Päätili | Myyntirivillä luotu päätili. Oletusarvo on peräisin myyntitilauksesta. Tämä kenttä voi olla tyhjä. |
| Nimikkeen taloushallinnon dimensiot | <p>Oletusarvioiset taloushallinnon dimension arvot asiakkaan ja nimiketietueen perusteella.</p><p>Tuottojakoa käyttävien nimikkeiden osalta alinimikkeet käyttävät asiakas- ja nimiketietueiden talousdimensioarvoja edellä kuvatulla tavalla. Jos sinun on päivitettävä alinimikkeiden taloushallinnon dimension arvoja, voit tuoda tietoyksikön.</p> |

### <a name="renewals-tab"></a>Uusimisvälilehti

**Uusimiset**-välilehdessä on seuraavat tiedot.

| Kenttä | Kuvaus |
|-------|-------------|
| Uusi automaattisesti | <p>Arvo, joka ilmaisee, uusitaanko laskutusaikataulun rivi automaattisesti seuraavalle laskutuskaudelle:</p><ul><li>**Kyllä** – Laskutusaikataulurivi uusitaan automaattisesti seuraavalle laskutuskaudelle, kun luot laskun.</li><li>**Ei** – Laskutusaikataulun riviä ei uusita automaattisesti. Sinun on uusittava laskutusaikataulu manuaalisesti.</li></ul> |
| Uusintaa kohti lisättävät rivit | Laskutusaikataulun uusimiseen lisättävä rivimäärä. |

**Uusimiset**-välilehdessä ovat lisäksi käytettävissä seuraavat painikkeet.

| Painike | Kuvaus |
|--------|-------------|
| Laskuttamattoman tuoton kirjauskansioviennin tarkistus | Voit tarkastella kaikkia sellaisten nimikkeiden muutoksia, joissa käytetään laskuttamattoman tuoton toimintoa. |
| Lisää uusimiskausi | Lisää nimikkeelle uusimiskausi. Uuden uusimiskauden alkamispäivämäärä on edellisen kauden päättymispäivää seuraava päivä. Kentät **Uusimisen päättymispäivä**, **Lykkäyksen alkamispäivä**, **Lykkäyksen päättymispäivä**, **Nimikemäärä** ja **Yksikköhinta** voidaan päivittää. |
| Muokkaa uusimiskautta | <p>Muokkaa uusimisaikaa. Alustavan kauden osalta voit muuttaa lykkäyksen alkamis- ja päättymispäivää, ennen kuin alustava kirjauskansioviesti luodaan. Seuraavien kausien osalta alkamispäivää ei voi muuttaa. Se on aina edellisen kauden päättymistä seuraava päivä.</p><p>Jos muutettavan kauden jälkeen on olemassa uusimiskausi, kauden päivämääriä ei voi muuttaa. Tällöin vain uusimisnimikkeen kenttiä **Määrä** ja **Yksikköhinta** voidaan päivittää.</p><p>Otetaan esimerkiksi tilanne, jossa on olemassa kolme kautta. <ul><li>Ensimmäistä kautta ei voi muuttaa, koska se on jo alkanut.</li><li>Toisen kauden osalta voidaan muuttaa vain määrää ja yksikköhintaa.</li><li>Kolmannen kauden osalta voidaan muuttaa kaikkia arvoja alkamispäivämäärää lukuun ottamatta. Lisäksi voit **Aikataulu mallin perusteella** -valinnan avulla luoda lykkäysaikataulun, joka perustuu laskuttamattoman tuoton nimikkeen malliin. Kun tämä asetuksen arvona on **Kyllä**, valitse **Malli**-kentän lykkäysmalli ja muuta lykkäyksen alkamis- ja päättymispäiviä tarpeen mukaan. Myöhemmissä uusimiskausissa käytetään samaa lykkäysmallia. Lykkäysmallia voi kuitenkin muuttaa.</p></li></ul> |

### <a name="termination-tab"></a>Lopetusvälilehti

**Lopetus**-välilehdessä on seuraavat tiedot.

| Kenttä | Kuvaus |
|-------|-------------|
| Työsuhteen loppumispäivämäärä | Päivämäärä, jona laskutusaikataulurivi lopetetaan. Oletusarvo perustuu otsikon **Lopetuspäivämäärä**-kenttään. Voit muuttaa arvoa tarpeen mukaan. |
| Irtisanomisen tyyppi | Lopetuksen tyyppi. Oletusarvo perustuu otsikon **Lopetuksen tyyppi**-kenttään. |

### <a name="hold-tab"></a>Pitovälilehti

Jos käytetään tuottojen ja kulujen lykkäyksiä **Pito**-välilehdessä näkyy lykkäyspäivämäärä.

### <a name="escalation-and-discount-tab"></a>Eskalointi- ja alennusvälilehti

**Eskalointi- ja alennus** -välilehdessä on seuraavat tiedot.

| Kenttä | Kuvaus |
|-------|-------------|
| Eskalointi | <p>Valitse sallitaanko eskaloinnit laskutusaikataulurivin osalta. Mitä tahansa otsikon eskalointiriviä sovelletaan, kun laskutusaikataulurivi luodaan.</p><ul><li>**Kyllä** – Riviin voi soveltaa eskalointeja. Kun tämä asetus on valittuna, voit määrittää eskalointeja laskutusaikatauluriveille **Eskalointi ja alennus** -sivulla.</li><li>**Ei** – Riviin ei voi soveltaa eskalointeja.</li></ul><p>Oletusasetus perustuu valittuun **Laskutusaikatauluryhmään**.</p> |

### <a name="price-changes-tab"></a>Hintamuutosten välilehti

Sellaisten rivien osalta, joissa hinnan arvo on muutettu muodosta **Vakio** muotoon **Kiinteä**, **Hintamuutokset**-välilehden ruudukko sisältää seuraavat sarakkeet:

- Muuta päivämäärä
- Käyttäjän muuttama
- Vakiohinta
- Kiinteä hinta
- Hinnanpäivitys
