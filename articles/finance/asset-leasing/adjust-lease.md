---
title: Vuokrasopimusten muuttaminen
description: Ohjeaiheessa kerrotaan, miten vuokrasopimusta muutetaan. Oikaisu voi olla tarpeen, jos vuokra-aikoja muutetaan, vuokrasopimusta pidennetään tai muita ehtoja muutetaan.
author: moaamer
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 89ec876c9bd967107635eb2955209a4dcb95cde5
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/05/2022
ms.locfileid: "8712171"
---
# <a name="adjust-leases"></a>Vuokrasopimusten muuttaminen

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Ohjeaiheessa kerrotaan, miten vuokrasopimusta muutetaan. Oikaisu voi olla tarpeen, jos vuokra-aikoja muutetaan, vuokrasopimusta pidennetään tai muita ehtoja muutetaan. Resurssin vuokraus noudattaa ASC 842:n ja IFRS 16:n ohjeita vuokrasopimuksen muokkauksesta. ASC 842-20-15-1 määrittää vuokrasopimuksen muokkauksen miksi tahansa sopimuksen ehtojen muutokseksi, jos se muuttaa vuokrasopimuksen laajuutta tai kohdetta. IFRS 16:n kappale 39 määrittää, että vuokralle ottajan on uudelleenarvostettava vuokrasopimusvelka niin, että se vastaa vuokrien muutoksia.

ASC 842- ja IFRS 16 -säädöksiä noudattavissa organisaatioissa vuokrasopimus arvioidaan uudelleen niin, että se vastaa tulevan vähimmäisvuokran nykyisen arvon muutosta. Jos tämä arvo kasvaa, luotu kirjauskansiovienti veloitetaan käyttöoikeusomaisuuserän tililtä ja hyvitetään vuokrasopimusvelan tilille uuden ja edellisen arvon välisenä erona. Jos arvo pienenee, kirjauskansiovienti veloitetaan vuokrasopimusvelan tililtä ja ero hyvitetään käyttöoikeusomaisuuserän tilille.

Js oikaisu vähentää käyttöoikeusomaisuuserän alle arvon 0 (nolla), jäljellä oleva osa hyvitetään vuokrasopimuksen muokkauksen kirjaustilin voittoon. Se on määritetty **Vuokrasopimuksen kirjaustilit** -sivulla. Järjestelmä ottaa huomioon nämä tapahtumat ja muut oikaisuviennit, kuten vuokrasopimuksen muokkauksen aiheuttamat luokittelun muutokset, alkuvaiheen välittömät menot, vuokrasopimukseen liittyvät kannustimet, ennakkomaksut ja purkamiskustannukset.

Lisäohjeita vuokrasopimuksen oikaisutapahtumia varten on IFRS 16- ja ASC 842 -ohjeissa.

## <a name="lease-adjustment-wizard"></a>Vuokrausoikaisun ohjattu toiminto

Oikaise vuokrasopimus seuraavien ohjeiden mukaan. Muokatut tiedot päivittävät vuokra-aaikataulut sen jälkeen, kun olet kirjannaut ohjatusta **Vuokrausoikaisu**-toiminnosta. Voit tallentaa työsi ja sulkea ohjatun toiminnon milloin tahansa ja palata sitten myöhemmin takaisin työsi jatkamista varten.

Voit avata ohjatun **Vuokraoikaisu**-toiminnon vuokrayhteenvedosta noudattamalla seuraavia ohjeita.

1. Siirry kohtaan **Resurssin leasing \> Vuokrasopimukset \> Vuokrasopimusyhteenveto**. 
2. Valitse oikaistavat vuokrat ja valitse sitten **ohjattu oikaisutoiminto**.
3. Tee tarvittavat muutokset noudattamalla ohjatun toiminnon kehotteita.

Voit avata ohjatun **Vuokraoikaisu**-toiminnon **Vuokraoikaisut**-sivulla jo käynnissä ollutta oikaisua varten noudattamalla seuraavia vaiheita.

1.  Siirry kohtaan **Vuokra \> Vuokrat \> Vuokraoikaisut**.
2.  Valitse vuokra, jonka oikaisutilana on **kesken** ja valitse sitten **ohjattu oikaisutoiminto**.
3.  Syötä **Muokkauksen alkamispäivä **- ja** Kirjauspäivä**-kenttiin haluamasi päivämäärät.
4.  Valitse **Seuraava**.

    Vuokra lisätään nyt **Vuokraoikaisut**-sivulle, jonne voit syöttää sille uudet tiedot.

    Kun vuokra on oikaistu, siihen sovelletaan käyttöoikeusehtojen kenttää. Jos muokattuun vuokrasopimukseen ei liity alkuperäisiä suoria kustannuksia, vuokrasopimukseen liittyviä kannustimia, ennakkomaksuja tai purkamiskustannuksia, jätä vastaavat kentät tyhjiksi. Alkuperäiset summat eivät koske päivitettyä vuokrasopimusta. 

    Esimerkiksi vuokralle antaja antaa 1 000 dollarin kannustimen, jotta vuokrasopimus hyväksytään. Kun tässä tapauksessa vuokrasopimusta muutetaan niin, että se ottaa laajennuksen huomioon, syötä **1 000** **Oikaisusta johtuvat vuokrasopimuksen kannustimet** -kenttään.

    Maksusuunnitelman rivit näyttävät nyt kaikki kuukauden ja myöhempien kuukausien maksut **Muokkauksen alkamispäivä**-kentässä. Koska muutokset ovat prospektiivisia, maksusuunnitelmarivit eivät voi alkaa ennen muutoksen alkamista. Voit tarkastella maksusuunnitelman rivejä ennen muokkauksen alkamispäivämäärää **Vuokran versiohistoria** -sivulla.

8.  Valitse **Seuraava**.

    Seuraava sivu sisältää odotettua vuokraoikaisua koskevat tärkeimmät tiedot, kuten vuokravelkaan liittyvät kirjanpitoarvot ennen muutosta ja uuden odotettavissa olevan vuokravelan muutoksen jälkeen. Sivulla voit myös esikatsella odotetun vuokraoikaisun kirjauskansiokirjauskirjausta.

9.  Valitse **Lähetä työnkulkuun**, jos haluat lähettää vuokraoikaisun työnkulkujärjestelmään, jos vuokraoikaisun työnkulku on aktiivinen eikä oikaisua ole vielä hyväksytty. Lisätietoja vuokraoikaisun työnkulun käyttämisestä on kohdassa [Vuokraoikeisun työnkulkujen käyttäminen](use-create-lease-wrkflw.md).

    > [!NOTE]
    > Tässä vaiheessa järjestelmä laskee oikaisun muuttujat uudelleen varmistaakseen, ettei tapahtumia ole kirjattu vuokraan oikaisun yhteenvedon ja oikaisukirjauskansion kirjauksen ensimmäisen laskennan jälkeen. Jos jokin arvo muuttuu, oikaisujen yhteenvetoruudukko päivitetään ja voit tarkistaa tiedot, ennen kuin lähetät vuokraoikaisut uudelleen työnkulkujärjestelmään.

10. Jos työnkulku ei ole aktiivinen tai vuokraoikaisu on hyväksytty, käsittele muutokset ja kirjaa oikaisukirjauskansion merkintä valitsemalla **Valmis**.

    > [!NOTE] 
    > Tässä vaiheessa järjestelmä laskee oikaisun muuttujat uudelleen varmistaakseen, ettei tapahtumia ole kirjattu vuokraan oikaisun yhteenvedon ja oikaisukirjauskansion kirjauksen ensimmäisen laskennan jälkeen. Jos jokin arvo muuttuu, oikaisujen yhteenvetoruudukko päivitetään ja voit tarkistaa muutokset ennen kuin valitset **Valmis**. Jos työnkulku on aktiivinen ja vuokraoikaisu on hyväksytty, oikaisun yhteenvedon muutokset aiheuttavat hyväksynnän tilan määrittämisen takaisin **Ei lähetetty** -tilaan. Tässä tapauksessa vuokraoikaisu on lähetettävä uudelleen työnkulkujärjestelmään.

    **Vuokraoikaisut**-sivulla oikaisun tilaksi tulee nyt **Valmis**.

    **Vuokraoikaisut**-sivulla voit silti tarkastella **Oikaisun yhteenveto**- ja **Oikaisumerkinnän esikatselu** -pikavälilehtiä. Vuokra- ja päivämäärätiedot näkyvät vuokran versiohistoriassa.

    Uusi vuokraversio ja uusi aikataulujoukko luodaan nyt muokattujen tietojen avulla. 

13. Voit tarkastella uusia aikatauluja siirtymällä vuokraan ja valitsemalla sitten **Kirjat**.
14. Voit tarkastella uutta luotua maksusuunnitelmaa valitsemalla **Maksusuunnitelma**.
15. Voit tarkastella uutta vuokrasopimusvelan kuoletusaikataulua, joka luotiin uusista tiedoista, sulkemalla **Maksuaikataulu**-sivun ja avaamalla **Velan kuoletusaikataulu** -sivun.
16. Voit tarkastella juuri luotua resurssin poistoaikataulua avaamalla **Resurssin poistoaikataulu** -sivun **Kirjan tiedot** -sivulla.
17. Voit tarkastella oikaisun kirjauskansiovientiä valitsemalla **Kirjauskansiot \> Resurssin leasingkirjauskansio**.

## <a name="cancel-a-lease-adjustment"></a>Vuokraoikaisun peruuttaminen

Jos haluat poistaa käynnissä olevan vuokraoikaisun, noudata seuraavia ohjeita.

1.  Siirry kohtaan **Vuokra \> Vuokrat \> Vuokraoikaisut**.
2.  Valitse kesken oleva ja peruutettava vuokraoikaisu.
3.  Valitse **Peruuta oikaisu**. 
4.  Valitse **OK**.

    > [!NOTE] 
    > Jos valitset ohjatussa **Vuokraoikaisu**-toiminnossa **Peruuta**, peruutat ohjatun toiminnon viimeisimpään muutokseen, mutta et poista käynnissä ollutta oikaisua.

## <a name="use-the-lease-adjustment-workflow"></a>Vuokraoikaisun työnkulun käyttäminen

Tässä osassa on tietoja vuokraoikaisutyönkulun käytöstä. Vuokraoikaisun työnkulku auttaa hallitsemaan vuokraoikaisuja yhdenmukaisesti antamalla hyväksyntävaiheet ja määrittämällä ne tietyille käyttäjille, jotka hyväksyvät vuokraoikaisun ennen sen lopullista muuttamista. Kun vuokraoikaisu on hyväksytty työnkulussa, voit viimeistellä vuokraoikaisun ohjatun **Vuokraoikaisu**-toiminnon avulla.

1.  Jos haluat lähettää vuokraoikaisun hyväksyttäväksi, siirry kohtaan **Vuokra \> Vuokrat \> Vuokraoikaisut**.
2.  Valitse vuokraoikaisun tunnus ja valitse sitten **ohjattu oikaisutoiminto**.
3.  Valitse ohjatun toiminnon viimeisellä sivulla **Lähetä hyväksyttäväksi**.
4.  Kirjoita oikaisua koskeva huomautus ja valitse sitten **OK**.

    Työnkulun tilaksi muutetaan **Odottaa hyväksyntää**, ja kaikki ohjatun toiminnon kentät on lukittu muokkauksen suhteen.

5.  Jos haluat hyväksyä vuokraoikaisun, siirry kohtaan **Vuokra \> Vuokrat \> Vuokraoikaisut**.
6.  Valitse vuokraoikaisun vuokratunnus ja tarkista **Oikaisun yhteenveto**- ja **Oikaisumerkinnän esikatselu** -pikavälilehdet.
7.  Valitse **Työnkulku \> Hyväksytty**.

    **Vuokraoikaisut**-sivulla työnkulun tilaksi tulee nyt **Hyväksytty**. Tässä vaiheessa vuokraoikaisu voidaan kirjata oikaisukirjauskansiomerkinnän kautta.

8.  Voit jatkaa vuokraoikaisun käsittelyä ja kirjata oikaisumerkinnän siirtymällä kohtaan **Vuokra \> Vuokra \> Vuokraoikaisut**.
9.  Valitse vuokraoikaisun tunnus ja valitse sitten **ohjattu oikaisutoiminto**.
10. Valitse **Seuraava**, kunnes pääset ohjatun toiminnon viimeiselle sivulle, ja valitse sitten **Valmis**.

Järjestelmä laskee vuokran kirjanpitoarvot uudelleen varmistaakseen, että hyväksytyt oikaisumuuttujat ovat ajan tasalla. Jos muutoksia on, hyväksynnän tilaksi tulee **Luonnos** ja sinun on lähetettävä vuokraoikaisu uudelleen työnkulkujärjestelmään.

## <a name="view-lease-versions"></a>Vuokrasopimusversioiden tarkasteleminen

Jos vuokrasopimusta on oikaistu, voit tarkastella sen eri versioita. Voit myös tarkastella aiempia aikatauluja ja aiempien vuokrasopimusten tietoja.

1. Valitse **Vuokrasopimusyhteenveto**-sivu ja valitse sitten toimintoruudussa **Vuokrasopimuksen versiohistoria**.

    Jos valittu vuokrasopimus on oikaistu, **Vuokrasopimuksen versiohistoria** -sivulla näkyvät sen eri versiot. Alkuperäisen vuokrasopimuksen otsikko on **1**. Seuraavien versioiden numerot ovat suurempia.

    Voit tarkastella valitun vuokrasopimusversion taloushallinnon dimensioita, sopimustietoja, sijaintia ja maksuaikataulurivejä.

2. Jos haluat tarkastella aiempia aikatauluja, avaa muokattu vuokrasopimus **Vuokrasopimusyhteenveto**-sivulla, valitse haluttu kirja ja valitse sitten toimintoruudussa **Kirjan versiohistoria**.
3. Valitse **Kirjan versio** -sivulla versio ja aikataulu tarkastelemista varten.

## <a name="adjust-a-lease-book"></a>Vuokrakirjan muokkaaminen

Voit muuttaa vain vuokrakirjaa noudattamalla seuraavia vaiheita.

1. Siirry kohtaan **Resurssin leasing** \> **Vuokrasopimukset** \> **Vuokrasopimusyhteenveto**.
2. Valitse ja avaa vuokra.
3. Valitse **Vuokrauksen tiedot** -sivulla **Kirjat**.
4. Valitse **Kirjan tiedot** -sivun toimintoruudun **Ylläpidä** -ryhmässä **Oikaise kirja**. 
5. Poista maksuaikataulurivit.
6. Syötä muokkauspäivämäärä **Vuokran muokkauspvm**-kenttään. Harkitse sitten kaikkien ylimääräisien käyttöomaisuus- ja velkatietojen (alkuperäinen suorakustannus, vuokrakannuste, vuokran ennakkomaksu, kustannusten purkaminen ja jäännösarvon takuu) poistamista, jos niitä on. 
7. Voit estää vuokraoikaisun virheelliset laskelmat lisäämällä uusia maksusuunnitelman rivejä uusille maksupäivämäärille, jotka vastaavat muokkauspäivää. 

> [!NOTE] 
> On suositeltavaa käyttää ohjattua **Vuokraoikaisu**-toimintoa vuokran oikaisemiseen. Ohjattu toiminto vähentää manuaalisten vaiheiden määrää, voit esikatsella saldoja oikaisun jälkeen ja mahdollistaa summien muutoksen ennen kirjaamista.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
