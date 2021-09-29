---
title: Sinetöidyt tarjoukset tarjouspyyntöihin
description: Tässä aiheessa kuvaillaan, miten määritetään eriävät lausekkeet, jotta toimittajien tarjousvastaukset voidaan säilyttää, kunnes ostohenkilöstö ei hallitse niitä.
author: yanansong
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 02cbe9d6a6d157208d73ed756efae24df2a082de
ms.sourcegitcommit: ecd4c148287892dcd45656f273401315adb2805e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/18/2021
ms.locfileid: "7500631"
---
# <a name="sealed-bidding-for-rfqs"></a>Sinetöidyt tarjoukset tarjouspyyntöihin

[!include [banner](../includes/banner.md)]

Eriävät lausekkeet säilyttävät toimittajien tarjousvastaukset, kunnes ostohenkilöstö ei hallitse niitä. Kaikki tarjouspyyntöön (RFQ) liittyvät tarjoukset ovat ensin avattavissa tarjouksen vanhentumisen yhteydessä. Ennen kuin tarjousta ei voi tehdä, vain käyttäjät, joilla on erityisiä käyttäjärooleja ja jotka kuvaavat toimittajaa, voivat käyttää tarjousta.

> [!IMPORTANT]
> Lomakkeiden muokkaaminen tai laajentaminen tai uusien lomakkeiden tai liiketoimintalogiikan luominen voi poistaa Microsoftin suljetulle tarjoamiselle luoman suojauksen. Sinulla on vastuu muokkausten, laajentamisten, uusien lomakkeiden ja uuden liiketoimintalogiikan käytöstä tai siitä, ettet voi käyttää suljetun tarjoamisen ominaisuutta tällaisten muokkausten, laajentamisten, uusien lomakkeiden ja uuden liiketoimintalogiikan käytön takia.  Microsoft ei ole vastuussa vahingoista, jotka aiheutuvat lomakkeiden muokkauksista tai laajentamisista tai liiketoimintalogiikan uusista muodoista, jotka luot tai jotka jokin kolmas osapuoli luo puolestasi. Microsoft ei tarjoa teknistä tai muuta tukea millekään muokkauksille, laajennuksille, uusille lomakkeille tai liiketoimintalogiikalle, jonka olet tehnyt itse tai jonka jokin kolmas osapuoli on tehnyt puolestasi. Olet yksinomaisesti vastuussa kaikkien suljettua tarjoamista koskevien soveltuvien lakien ja säännösten noudattamisesta.

## <a name="how-bids-are-kept-secure"></a>Tarjousten suojaaminen

Sähköpostiviestit, jotka käyttävät epäsymmetristä salausta, salaavat tarjousten salauksen avaimen (KEK) ja salauksen, joka salaa varsinaisen tarjouksen. Järjestelmä integroituu Microsoft Azure Key Vaultin kanssa muodostaakseen ja hallitakseen salausavaimia, joita käytetään salattujen tarjousten salauksessa. Jokaiseen tarjoukseen on oma salausavain. Salaus pitää turvassa avaimen organisaation omistamassa avainsäilössä, joka suorittaa Dynamics 365 Supply Chain Managementia. Järjestelmä käyttää avainta tarpeen mukaan aina, kun salausta ja salauksen purkua vaaditaan.

## <a name="setup-and-configuration"></a>Asetukset ja määrittäminen

Tässä osassa kuvataan edellytykset, jotka on oltava käytössä, ennen kuin voi lähettää tarjouspyynnön, joka edellyttää epäsäännöllistä salausta.

### <a name="step-1-set-up-user-access-to-sealed-bidding"></a>Vaihe 1: Määritä, että käyttäjällä on pääsy epäsäännölliseen salaukseen

Kun käytät vanhentumista, vain toimittajan yhteyshenkilöksi määritettävät käyttäjät voivat tarkastella, muokata ja lähettää tarjoukset toimittajalle, kunnes vanhentumisaika päättyy. Käyttäjillä on oltava **toimittajarooli (ulkoinen)**, ja heidät on määritettävä toimittajatilin yhteyshenkilöksi. Yhteyshenkilöllä on oltava myös toimittajien yhteistyöoikeus, joka on kuvattu kohdassa [Toimittajien yhteistyön määrittäminen ja ylläpito](set-up-maintain-vendor-collaboration.md).

Koska käyttäjät, joilla on asianmukaiset käyttöoikeudet ja jotka on määritetty toimittajan yhteyshenkilöiksi, voivat käyttää toimittajan suljettuja hintatarjouksia, on tärkeää seurata, keitä käyttäjät ovat. Järjestelmänvalvoja, joka määrittää käyttäjät ja käyttöoikeusroolit, on vastuussa siitä, että tarjousten käyttöoikeudet rajataan käyttäjille, jotka todella saavat tarkastella niitä.

### <a name="step-2-enable-the-sealed-bidding-feature"></a>Vaihe 2: Ota suljettu hinnoittelutoiminto käyttöön

Varmista ennen toiminnon määrittämistä tai käyttämistä, että se on saatavana järjestelmässä. Järjestelmänvalvojat voivat tarkistaa **[Ominaisuuksien hallinta](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** -työtilassa toiminnon tilan ja ottaa sen käyttöön. **Ominaisuuksien hallinta** -työtilassa ominaisuus on luetteloitu seuraavalla tavalla:

- **Moduuli:** *Hankinnan tehtävät*
- **Ominaisuuden nimi:** *Tarjouspyynnön suljettu hinnoittelutoiminto*

### <a name="step-3-set-up-azure-key-vault"></a>Vaihe 3: Azure Key Vaultin määrittäminen

Supply Chain Managementissa käytetään salausavaimia, jotka suojaavat kaikkia tarjouksia ja pitävät tarjoukset salassa, kunnes aika on sopiva. Se hyödyntää Key Vaultin ominaisuuksia tarvittavien avainten luomiseen ja hallintaan. Siksi sinun on määritettävä yhteys Supply Chain Managementista avainsäilöön, jotta järjestelmää olisi mahdollista käyttää.

> [!IMPORTANT]
> Avainsäilö on luotava Azure-tilauksessa, jonka omistaa organisaatiosi (ei tilaus, jossa käytät Supply Chain Managementia).

Jokainen tarjous hakee oman salaisen avaimensa. Tätä avainta käytetään aina, kun käyttäjä avaa tarjouksen, päivittää tai poistaa sen käytöstä.

Key Vault luo avaimen, jota käytetään toimittajalle, kun toimittaja valitsee **Tarjous**-avaimen toimittajan yhteiskäyttöliittymässä. Avain vanhenee sitten tietyn hankintapäällikön asettaman ajan kuluttua **Hankinta ja hankintaparametrit** -sivulla Supply Chain Managementissa. Kun avain vanhenee, kukaan voi tarkastella, muokata tai poistaa tarjousta. Siksi on tärkeää määrittää avaimen vanheneminen niin, että vanhentumisprosessi kestää kauan aikaa.

Seuraavissa kolmessa vaiheessa määrität yhteyden Key Vaultiin. Määritä ensin avainvarasto käytettäväksi suljetun hintatarjouksen kanssa. Seuraavaksi määrität Supply Chain Managementin kommunikoimaan avainsäilön kanssa. Lopuksi määrität avaimen vanhenemisajan.

### <a name="step-4-set-up-a-key-vault-to-use-with-sealed-bidding"></a>Vaihe 4: Määritä ensin avainvarasto käytettäväksi suljetun hintatarjouksen kanssa

Määritä avainsäilösi noudattamalla seuraavia ohjeita. Vaiheiden järjestys on erittäin tärkeä.

1. Jos et ole vielä määrittänyt Azure-tilausta, joka on erillinen sopimus siitä, jossa Supply Chain Management on käynnissä, määritä se.
1. Voit määrittää avaimen, joka sijaitsee eri Azure-tallennustilassa. Lisätietoja: [Azure Key Vault -tallennustilan ylläpito](https://support.microsoft.com/help/4040294/maintaining-azure-key-vault-storage).
1. Määritä Supply Chain Management -sovelluksesi toimimaan avainsäilösi asiakkaana. Lisätietoja: [Azure Key Vault -asiakasohjelman määrittäminen](https://support.microsoft.com/help/4040305/setting-up-azure-key-vault-client).

### <a name="step-5-configure-key-vault-parameters-in-supply-chain-management"></a>Vaihe 5: Key Vault -parametrien konfiguroiminen Supply Chain Managementissa

Noudattamalla näitä vaiheita voit määrittää Supply Chain Managementin kommunikoimaan avainsäilön kanssa suljetun tarjouksen aikana.

1. Kirjaudu sisään Supply Chain Managementiin ja siirry kohtaan **Järjestelmän hallinta \> Asetusa \> Key Vault -parametrit**.
1. Luo tietue valitsemalla **Uusi** ja määritä tietueelle seuraavat kentät:

    - **Nimi** – Syötä nimi.
    - **Kuvaus** – Syötä kuvaus.
    - **Key Vault URL-osoite** – Kirjoita avainsäilön URL-osoite.
    - **Key Vault -asiakasohjelma** - Syötä avainsäilöön liittyvän Active Directory -sovelluksen vuorovaikutteinen asiakastunnus todennusta varten.
    - **Key Vault -salainen avain** – Syötä salainen varmenne todistusta varten.
    - **Käytössä vain salatussa tarjouksessa** – Määritä tämän asetuksen arvoksi *Kyllä*.

![Key Vaultin parametrisivu](media/sealed-bidding-key-vault-param.png "Key Vaultin parametrisivu")

> [!NOTE]
> Voit ottaa käyttöön kerrallaan vain yhden avainsäilökonfiguraation yhtä suljettua tarjousta varten. Ennen kuin poistat olemassa olevan avainsäilökonfiguraation käytöstä, sinun on varmistettava, että kaikki sitä käyttävät suljetut tarjoukset on suljettu. Tarkista jokainen *suljettu* RFQ -tapaus ja varmista, että kaikki siihen liittyvät vastaukset on suljettu.

### <a name="step-6-set-the-key-expiration-time"></a>Vaihe 6: Avaimen vanhenemisajan määrittäminen

Seuraavia ohjeita noudattamalla voit määrittää jokaiselle uudelle tarjoukselle luodulle avaimelle määritettävän vanhentumisajan.

1. Siirry kohtaan **Hankkimisen ja hankinnan parametrit \> Asetukset \> Hankkiminen ja hankinta -parametrit**.
1. Kirjoita **Tarjouspyyntö**-välilehden **Päivien vastakirjaus** -kenttään, kuinka monta päivää tarjouspyyntökauden tulee kestää. Kun tarjouspyyntö luodaan, tähän syötetyt päivät lisätään järjestelmän päivämäärään, jolloin tarjouspyynnön oletusvanhenemispäivämäärä määritetään.
1. Määritä **Salauksen avaimen vanhentumispäivän vastakirjaus** -kenttään, kuinka monta päivää jokaisen salausavaimen on oltava voimassa sen antamisen jälkeen. Kun salausavain vanhenee, kukaan voi tarkastella, muokata tai poistaa suljettua tarjousta, joka käyttää sitä.

> [!TIP]
> **Salauksen avaimen vanhenemispäivän vastatilin** kentän arvon ei saa olla pienempi kuin **Päivien vastakirjaus** -kentän arvo.

### <a name="step-7-set-the-default-bid-type"></a><a name="set-default-bid-type"></a>Vaihe 7: Oletustarjoustyypin määritäminen

Jokaisella tarjouspyyntötapauksella on tarjoustyyppi. Tarjoustyyppi määrittää, tarjoaako tarjouspyyntötapaus avointa vai suljettua tarjousta.

#### <a name="rfq-cases-that-dont-have-a-solicitation-type"></a>Tarjouspyyntötapauksissa, joissa ei ole pyyntöjen tyyppiä

Noudattamalla näitä ohjeita voit määrittää uusille tarjouspyynnön palvelupyynnöille määritetyn oletustarjoustyypin, jota ei ole määritetty pyyntöjen luomisen yhteydessä.

1. Siirry kohtaan **Hankkimisen ja hankinnan parametrit \> Asetukset \> Hankkiminen ja hankinta -parametrit**.
1. Määritä **Tarjouspyyntö**-välilehdessä **Tarjoustyyppi**-kentän arvoksi *Suljettu*.

#### <a name="rfq-cases-that-have-a-solicitation-type"></a>Tarjouspyyntötapauksissa, joissa on pyyntöjen tyyppi

Noudattamalla näitä ohjeita voit määrittää uusille tarjouspyynnön palvelupyynnöille määritetyn oletustarjoustyypin, joka on määritetty pyyntöjen luomisen yhteydessä.

1. Siirry kohtaan **Hankinta \> Asetukset \> Tarjouspyyntö \> Pyyntötyyppi**.
1. Luo uusi pyyntötyyppi tai valitse aiemmin luotu pyyntötyyppi, jos haluat käyttää *Suljettua* tarjoustyyppiä.
1. Valitse **Pyyntötyyppi**-kentän arvoksi *Suljettu*.
1. Toista nämä vaiheet jokaiselle lisäpyyntötyypille, jossa haluat käyttää suljettua hintatarjousta.

> [!TIP]
> Pyyntötyyppiä ei tarvitse määrittää, kun uusi tarjouspyyntö luodaan. Jos pyynnölle on määritetty tarjouspyyntötyyppi, tarjouspyynnön oletustarjoustyyppi voi noutaa sen. Muussa tapauksessa voit käyttää hankinnan parametreissa määritettyä oletuksena käytettävää pyyntötyyppiä.

## <a name="the-sealed-bidding-process"></a>Suljettu tarjousprosessi

Suljettu tarjous noudattaa lähes samaa prosessia, joka on kuvattu kohdassa [Tarjouspyyntöjen (RQF) yhteenveto](request-quotations.md). Suurin ero on se, että tarjoustiedot ja niiden liitteet pidetään salattuina, kunnes tarjous on avattu.

> [!IMPORTANT]
> [Kyselyitä](/dynamicsax-2012/appuser-itpro/view-and-respond-to-questionnaires) ei salata, eikä niitä pitäisi käyttää luottamuksellisten tietojen keräämiseen

Tässä on hahmotelma prosessista:

1. Luot ja lähetät tarjouspyynnön vähintään yhdelle toimittajalle.
1. Toimittajat vastaavat lähettämällä salatun tarjouksen.
1. Poistat tarjousten sulkemisen tarjouksen jättämisen päättymisajan jälkeen.
1. Tarjoukset tulevat näkyviin, ja niitä voi arvioida ja verrata.
1. Kun tarjous on hyväksytty, luot ostotilauksen, luot ostosopimuksen tai päivität ostoehdotuksen.

### <a name="create-an-rfq-case-that-uses-sealed-bidding"></a>Luo tarjouspyyntötapaus, jossa käytetään suljettua tarjousta

Prosessi, jossa luodaan tarjouspyyntö, on miltei samanlainen kuin se prosessi, jossa tarjous ei ole suljettu. Lisätietoja molempien tyyppisten tarjouspyyntöjen luomisesta on ohjeaiheessa [Tarjouspyynnön luominen](tasks/create-request-quotation.md). Tässä osassa korostetaan muutamia tärkeitä näkökohtia, kun luot tarjouspyynnön suljetulle tarjoukselle.

Suljetuissa tarjouspyyntötapauksissa **tarjouspyynnön** arvon tulee olla *Suljettu*. Tämän arvon voi liittää tarjouspyyntöpyyntöön kolmella tavalla:

- Määritä arvo suoraan tarjouspyyntöpyyntöön sen jälkeen, kun olet luonut sen.
- Määritä suljettu hintatarjous oletustarjoustyypiksi kaikille tarjouspyyntötapauksille osto- ja hankintaparametreissa. (Lisätietoja on [Määritä oletustarjoustyyppi](#set-default-bid-type) -osassa aiemmin tässä aiheessa.)
- Kun luot uuden tarjouspyyntötapauksen, valitse pyyntötyypiksi se, joka sisältää suljetun tarjouksen. (Lisätietoja on kohdassa [Määritä oletustarjoustyyppi](#set-default-bid-type).)

Suljetussa tarjouksessa tarjouspyyntötapauksen **viimeinen voimassaolopäivä ja -aika** määrittää, milloin lähetetyt tarjoukset voidaan purkaa. Kunkin rivin **vanhenemispäivämäärä ja -aika** vastaavat otsikon arvoa.

Tarjoustyyppiä ei voi muuttaa sen jälkeen, kun tarjouspyyntöpyyntö on lähetetty.

### <a name="vendors-respond-to-an-rfq"></a>Toimittajat vastaavat tarjouspyyntöön

Toimittajat, jotka vastaavat suljettuun tarjoukseen, käyttävät samaa menettelyä kuin silloin, kun he vastaavat avoimiin tarjouksiin, kuten on kuvattu kohdassa [Tarjouspyyntöjen käsittely toimittajan tarjoustyötilassa](vendor-collaboration-work-customers-dynamics-365-operations.md#working-with-rfqs-in-the-vendor-bidding-workspace). Yksityiskohtaiset ohjeet sekä avointen tarjousten että tarjouspyyntöjen vertailusta on kohdassa [Tarjouspyyntöjen ja palkkiosopimusten syöttäminen ja vertaaminen](tasks/enter-compare-rfq-bids-award-contracts.md). Ainoa suljettujen tarjousten ja avointen tarjousten käsittelyn välinen ero on se, että hankinta-asiantuntijat eivät voi avata toimittajan suljettua tarjousta, ennen kuin se on vanhentunut. Vain toimittajan yhteyshenkilö voi avata toimittajan tarjouspyynnön.

> [!IMPORTANT]
> Suljetussa hinnoittelussa myyjät voivat lähettää liitteitä vain PDF-muodossa. Muita muotoja ei hyväksytä.

Kun rekisteröitynyt toimittajan käyttäjä on valinnut **tarjouksen** suljetun tarjouksen tarjouspyynnössä, hän voi syöttää hintatarjoustietonsa ja nämä tiedot pidetään turvassa. Toimittajat voivat tallentaa työnsä valmistellessaan tarjousta, palata siihen niin usein kuin tarvitaan ja lähettää sen sitten, kun se on valmis. Myös toimittajat voivat tarkastella tarjoustaan sen lähettämisen jälkeen. Jos toimittajien on muutettava tarjoustaan sen lähettämisen jälkeen, he voivat kutsua sen takaisin, päivittää sen ja lähettää sen uudelleen milloin tahansa, kunnes vanhentumisaika päättyy.

Seuraavien ehtojen on täytyttävä suljetun tarjouksen aikana:

- Järjestelmä luo *tarjouspyynnön* kirjauskansion suljetun tarjouksen aikana.
- Kun toimittaja lähettää tarjouspyynnön, luodaan tarjouspyynnön rivittömät kirjauskansiot, joissa on suljettu hinta.
- Kun tapausta avataan, luodaan tarjouspyynnön kirjauskansiot, joissa on hinta ja summa. Voit käyttää tätä kirjauskansiota valitsemalla **Tarjouspyyntökirjauskansion** **Kaikki tarjouspyynnöt** -sivulla.
- Järjestelmä tallentaa lokin kustakin toimesta, jonka käyttäjät tekevät suljetulle tarjoukselle. Tällaisia toimenpiteitä ovat tarjouksen tarkasteleminen, muokkaaminen ja tallentaminen. Tämä loki näkyy sekä toimittajalle että hankinta-asiantuntijoille, joilla on tarjouksen käyttöoikeus.
- Tarjousten edetessä hankinta-asiantuntijat voivat tarkastella tarjouksen tilaa. Tila on joko *Toimittaja päivittää* tai *Toimittaja on lähettänyt*.
- Tarjouksen rivien tila on *lähetetty*, kunnes tarjous avataan.
- Jos toimittaja päättää hylätä tarjouksen, tarjouksen **vastauksen edistymisen tilaksi** tulee *Toimittajan hylkäämä*. Hankintahenkilöt voivat nähdä tämän tilan.
- Kyselylomakkeiden vastauksia **ei** tallenneta tietokantaan salatussa muodossa. Siksi niitä ei sulkea. Ne eivät kuitenkaan näy tarjouspyynnön käyttöliittymässä, ennen kuin tapaus on avattu.

### <a name="all-sealed-bid-activities-are-logged"></a>Kaikki muokkaustoimet kirjataan lokiin

Yksityiskohtainen loki tallentaa kaikki käyttäjätoiminnot ja tarjouksen toimenpiteet. Tehtävälokin avulla organisaatiot voivat määrittää, kuka päivitti tarjouksen sen elinkaaren aikana ja mitä päivitykset olivat. Sen avulla organisaatiot voivat myös vahvistaa, että vain valtuutettu henkilö voi käyttää tarjousta. Tehtäväloki on käytettävissä jokaisen tarjouksen **tehtävä**-sivulla.

### <a name="review-rfq-activity"></a>Tarjouspyynnön tehtävien tarkasteleminen

Jokainen tarjouksen kanssa toimiminen kirjataan lokiin, ja sitä voi tarkastella **Tehtävä**-sivulla. Seuraavassa kuvassa on esimerkki.

![Esimerkki tehtäväsivusta](media/sealed-bidding-rfq-activity.png "Esimerkki tehtäväsivusta")

Toimittajat voivat käyttää **tehtävä**-sivua valitsemalla **Toimi** **tarjouspyyntö suljetusta tarjouksesta** -sivulla. Hankintahenkilöt voivat käyttää sitä valitsemalla **Tehtävän** **Tarjouspyyntö**-sivulla. Tehtävälokista saa täyden näkyvyyden toimittajille ja hankintahenkilöstölle, jotka ovat täyttäneet tarjouksen. Näin ollen se voi paljastaa luvattoman käytön.

### <a name="unseal-sealed-bids"></a>Suljettujen tarjousten avaaminen

Kun **erääntymispäivä ja -aika** -arvo, joka on määritetty tarjouspyynnön vanhentumispäiväksi, on ohitettu, **Avaa**-painike on käytettävissä. Valitse **Avaa**, jos haluat poistaa kaikkien valitun tarjouspyyntötapauksen tarjousten salauksen. Kaikki tarjoustiedot ja liitteet tulevat sitten näkyviin, jotta tapauksen vastauksia voidaan hallita. Lisäksi luodaan kirjauskansiot, jotka sisältävät lähetetyt tarjoustiedot.

Avaustapahtuma kirjataan lokiin, ja sitä voi tarkastella **Tehtävä**-sivulla.

### <a name="process-accepted-bids"></a>Hyväksyttyjen tarjousten käsitteleminen

Aiemmin avoimia tarjousten vertailua ja hyväksymistä käsitellään samalla tavalla kuin avointen tarjousten prosessissa. Lisätietoja tarjouspyyntöjen tekemisistä, vertaamisesta, hylkäämisestä ja hyväksymisestä on kohdassa [Tarjouspyyntöjen ja palkkiosopimusten syöttäminen ja vertaaminen](tasks/enter-compare-rfq-bids-award-contracts.md).

## <a name="the-rfq-activity-log-can-never-be-deleted"></a>Tarjouspyynnön tehtävälokia ei voi koskaan poistaa

Edes järjestelmänvalvojat tai Microsoftin tuki eivät voi muokata tarjouspyyntötehtävän lokia tai poistaa niitä. Tämä rajoitus auttaa varmistamaan suljetun tarjousprosessin oikeudenmukaisuuden. Sen avulla voidaan myös varmistaa, että kirjausketju säilyy tarkasti.
