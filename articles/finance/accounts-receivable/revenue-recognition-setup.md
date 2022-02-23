---
title: Tuottokirjauksen määritys
description: Tässä aiheessa kuvataan tuottokirjauksen määritysasetukset ja niiden vaikutukset.
author: kweekley
manager: aolson
ms.date: 08/24/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 73acfc92777b8fe07b89bea782e13213d38000cd
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4458917"
---
# <a name="revenue-recognition-setup"></a>Tuottokirjauksen määritys
[!include [banner](../includes/banner.md)]

Uusi **Tuottokirjauksen** moduuli on lisätty, Se sisältää valikkovaihtoehtoja kaikille tarvittaville määrityksille. Tässä aiheessa kuvataan määritysasetukset ja niiden vaikutukset.

> [!NOTE]
> Tuoton kirjaustoimintoa ei voi ottaa käyttöön ominaisuuksien hallinnan avulla. Tällä hetkellä se on otettava käyttöön konfigurointiavainten avulla.

**Tuottokirjauksen** moduulilla on seuraavat määritysvaihtoehdot:

- Tuottokirjauskansiot
- Tuottokirjauksen parametrit
- Tuottoaikataulut 
- Varaston määritys

    - Nimikeryhmät ja vapautetut tuotteet
    - Tuottoaikataulun määritys
    - Tuottohinnan määritys

        - Kirjausprofiilit
        - Niput

    - Nippukomponentit
    - Nippunimike

- Projektimääritykset

## <a name="revenue-recognition-journals"></a>Tuottokirjauskansiot

Tuottokirjaukseen on lisätty uusi kirjauskansiotyyppi. Kirjauskansio on pakollinen ja sitä käytetään kahdessa skenaariossa.

Ensimmäinen skenaario toteutuu sopimusvelvoitteiden täyttämisen jälkeen, kun siirretty tuotto kirjataan luomalla tuottokirjauksen kirjauskansio, joka perustuu tuottoaikataulun tietoihin. Kirjauskansio sisältää kirjanpitomerkinnän, joka siirtää saldon siirretyn tuoton kirjanpitotililtä tuoton kirjanpitotilille.

Toinen skenaario toteutuu, kun kirjauskansio luodaan uudelleenkohdistuksen jälkeen. Uudelleenkohdistus tapahtuu, kun myyntitilausrivi lisätään aiemmin laskutettuun myyntitilaukseen tai kun luodaan uusi myyntitilaus, joka sisältää alkuperäiseen sopimukseen kuuluvan rivin. Jos lasku on kirjattu ennen uuden myyntitilausrivin lisäämistä, kirjatulle myyntilaskulle on luotava korjaava kirjanpitomerkintä.

Kirjauskansio määritetään **Kirjauskansioiden nimet** -sivulla (**Tuottokirjaus \> Määritys \> Kirjauskansioiden nimi**). Kirjauskansion tyypiksi on asetettava **Tuottokirjaus**. Tuottokirjauskansiossa voidaan valita kirjanpitotaso, jolle se kirjataan.

## <a name="parameters-for-revenue-recognition"></a>Tuottokirjauksen parametrit

Tuottokirjauksen asetukset määritetään **Kirjanpitoparametrit** -sivun **Tuottokirjaus** välilehdellä (**Tuottokirjaus \> Määritys \> Kirjanpitoparametrit**). Seuraavat asetukset ovat käytettävissä:

- **Tuottokirjauskansion nimi** – Valitse kirjauskansio, joka luotiin tuottokirjausta varten. Kirjauskansio vaaditaan, kun tuotto kirjataan tuottoaikataulusta tai kun suoritetaan uudelleenkohdistus myyntitilauksessa, joka on jo laskutettu.
- **Ota alennuksen kohdistus -menetelmä käyttöön** – Määritä tämä asetus arvoon **Kyllä**, jotta tuottohinta määritetään kohdistamalla käyvä markkina-arvo, joka määritetään kunkin vapautetun tuotteen tuottohinnassa. Tämä kohdistus sisältää nimikkeiden mahdollisten rivialennusten kohdistuksen. Jos asetuksen arvoksi määritetään **EI**, järjestelmä käyttää mediaanihintaa, joka on määritetty kunkin vapautetun tuotteen tuottohinnassa. Jos tämän asetuksen arvoksi asetetaan **Ei**, mutta vapautetuille tuotteille ei ole määritetty mediaanihintaa, tuottohintaa ei kohdisteta.
- **Sisällytä ylätunnistealennukset** – Jos tämän asetuksen arvoksi määritetään **Kyllä**, tuottohinta määritetään kohdistamalla tuotteisiin ylätunnistealennuksia. Jos tämän asetuksen arvoksi määritetään **Ei**, ylätunnistealennusta ei oteta huomioon tuottohinnan kohdistuksessa.
- **Poista sopimusehdot käytöstä** – Määritä tämän asetuksen arvoksi **Kyllä**, jos tuotteet, joilla on tuottotyyppi **Sopimuksenjälkeinen tuki**, voidaan vapauttaa, vaikka niille ei ole määritetty sopimuksen alkamis- ja päättymispäivämääriä. Yleensä **Sopimuksenjälkeinen tuki** -tuottotyypin nimikkeille vaaditaan sopimuksen alkamis- ja päättymispäivämäärät. Kun sopimuksen alkamis- ja päättymispäivämääriä ei ole määritetty, kirjauksen tuottoaikataulun tiedot lasketaan käyttämällä esiintymien määrää ja laskun päiväys.
- **Kirjaa laskujen korjaukset uudelleenkohdistuksen yhteydessä myyntireskontraan** – Kun suoritat uudelleenkohdistuksia laskuissa, jotka on jo kirjattu, niiden kirjanpitomerkintä on korjattava. Tällä asetuksella määritetään, miten korjaus suoritetaan.

    - Kun tämän asetuksen arvona on **Ei**, korjaavan tapahtuman kirjaaminen rajoitetaan kirjanpitoon. Kun tämän asetuksen arvona on **Ei**, myyntireskontrassa ei luoda lisäasiakirjoja sisäisen kirjanpidon korjausta varten. Kun lasku maksetaan, tilitysprosessissa käytetään vanhaa kirjanpitomerkintää mahdollisten käteisalennusten, toteutuneen voiton tai toteutuneen tappion kirjaukseen.
    - Kun tämän asetuksen arvo on **Kyllä**, myyntireskontrassa luodaan automaattisesti takaisinkirjausasiakirja ja uusi lasku korjaavaa tapahtumaa varten. Koska tämä korjaus on sisäisen kirjanpidon korjaus, uusia asiankirjoja ei lähetetä tai ilmoiteta asiakkaalle. Takaisinkirjausasiakirja tilitetään alkuperäiselle laskulle ja asiakas maksaa uuden korjatun laskun. Huomaa, että kaikki kolme asiakirjaa näkyvät raporteissa, kuten asiakkaan tiliotteessa.

[![Määritystiedot](./media/revenue-recognition-setup-info.png)](./media/revenue-recognition-setup-info.png)

## <a name="revenue-schedules"></a>Tuottoaikataulut

Kullekin esiintymälle, jossa tuottoa voidaan siirtää, on luotava tuottoaikataulu. Jos organisaatiosi esimerkiksi tarjoaa tukea 6, 12, 18 tai 24 kuukaudeksi, tuottoaikataulu on luotava kullekin näistä kestoista. Tuottoaikataulun määritykset määrittävät, miten tuottohinta kohdistetaan valitsemillesi kestoille. Se määrittää myös oletuspäivämäärät, jotka annetaan laskun kirjaamisen yhteydessä luotavalle tuottoaikataululle.

Jos tuotto kirjataan välitavoitteiden mukaan, suosittelemme tuottokirjausaikataulun luomista kaikille välitavoitteille kirjausten päivämääristä riippumatta. Kun aikataulut on luotu, niitä voidaan muokata, jotta ne vastaavat odotettuja välitavoitteiden päivämääriä. Nämä tietueet voidaan laittaa pitoon siihen asti, että saat ilmoituksen välitavoitteen täyttymisestä ja siitä, että tuotto voidaan kirjata.

Tuottoaikataulut luodaan **Tuottoaikataulut** -sivulla (**Tuottokirjaus \> Määritys \> Tuottoaikataulut**).

[![Tuottoaikataulut](./media/revenue-recognition-revenue-schedules.png)](./media/revenue-recognition-revenue-schedules.png)

Syötä kuvaavia arvoja kenttiin **Tuottoaikataulu** ja **Kuvaus**. Seuraavia lisäasetuksia käytetään tuottoaikataulun luomiseen, kun lasku kirjataan.

- **Esiintymät** – Syötä kuukausi- tai esiintymämäärä tuoton siirtämiselle.
- **Automaattinen pito** – Tämä valintaruutu valitaan, jos kaikki tuottoaikataulun rivit on tarkoitus asettaa automaattisesti pitoon, kun lasku kirjataan. Pito on poistettava manuaalisesti kultakin aikataulun riviltä, ennen kuin rivin siirretty tuotto voidaan kirjata.
- **Automaattiset sopimusehdot** – Tämä valintaruutu valitaan, jos sopimuksen alkamis- ja päättymispäivät on tarkoitus asettaa automaattisesti. Nämä päivämäärät asetetaan automaattisesti vain tuottotyypin **Sopimuksenjälkeinen tuki** vapautetuille tuotteille. Sopimuksen alkamispäiväksi asetetaan automaattisesti myyntitilausrivin pyydetty lähetyspäivämäärä ja sopimuksen päättymispäivä asetetaan automaattisesti lisäämällä tuottoaikataulun määrityksessä annettujen kuukausien tai esiintymien määrä alkamispäivämäärään. Myyntitilauksen tuote voi olla esimerkiksi vuoden takuu. Tuottoaikataulun oletusarvo on **12M** (12 kuukautta) ja **Automaattiset sopimusehdot** -valintaruutu on valittuna tälle tuottoaikataululle. Jos myyntitilauksen pyydetty lähetyspäivämäärä on 16.12.2019, sopimuksen oletusarvoinen alkamispäivä on 16.12.2019 ja oletusarvoinen päättymispäivä on 15.12.2020.
- **Kirjausperusteet** – Kirjausperuste määrittää, miten tuottohinta kohdistetaan esiintymiin.

    - **Kuukausittain päivämäärien mukaan** – Summa kohdistetaan kunkin kuukauden todellisten päivien perusteella.
    - **Kuukausittain** – Summa jaetaan tasan esiintymissä määritetyn kuukausimäärän kesken.
    - **Esiintymät** – Summa jaetaan tasan esiintymien kesken, mutta se voi sisältää lisäajan, jos **Todellinen alkamispäivä** valitaan kirjausmenetelmäksi.

- **Kirjausmenetelmä** – Kirjausmenetelmällä määritetään oletuspäivämäärät, jotka asetetaan laskun tuottoaikataululle.

    - **Todellinen alkamispäivä** – Aikataulu luodaan käyttämällä joko sopimuksen alkamispäivää (sopimuksenjälkeisen tuen \[PCS\] nimikkeille) tai laskun päiväystä (oleellisille ja muille kuin oleellisille nimikkeille).
    - **Kuun 1. päivä** – Ensimmäisen aikataulurivin päivämäärä on sopimuksen alkamispäivä (tai laskun päiväys). Kaikki seuraavat aikataulurivit kuitenkin luodaan kuukauden ensimmäiselle päivälle.
    - **Jako keskellä kuukautta** – Ensimmäisen aikataulurivin päivämäärä määräytyy laskun päiväyksen mukaan. Jos lasku kirjataan kuun 1.–15. päivän välisenä aikana, tuottoaikataulu luodaan käyttämällä kuukauden ensimmäistä päivää. Jos lasku kuun 15. päivän jälkeen, tuottoaikataulu luodaan käyttämällä seuraavan kuukauden ensimmäistä päivää.
    - **Seuraavan kuun 1. päivä** – Aikataulun päivämääränä on seuraavan kuukauden ensimmäinen päivä.

Valitse **Tuottoaikataulun tiedot** -painike tarkastellaksesi yleisiä kausia ja prosenttiosuuksia, jotka kirjataan kunkin kauden aikana. Oletusarvoisesti **Kirjausprosentti** -arvo jaetaan tasan kausimäärän kesken. Jos kirjausperusteen arvoksi on asetettu joko **Kuukausittain** tai **Esiintymät**, kirjausprosenttia voidaan muuttaa. Kun muutat kirjausprosenttia, saat varoitusviestin siitä, että kokonaismäärä ei ole 100 prosenttia. Jos saat viestin, voit jatkaa rivien muokkaamista. Kokonaismäärän on kuitenkin oltava 100 prosenttia ennen sivun sulkemista.

[![Tuottoaikataulun tiedot](./media/revenue-recognition-revenue-schedule-details.png)](./media/revenue-recognition-revenue-schedule-details.png)

## <a name="inventory-setup"></a>Varaston määritys

Vapautettujen tuotteiden tuotto voidaan kirjata myyntitilauksiin, mutta ei myyntitilausten myyntiluokkiin tai vapaatekstilaskuihin, jos asiakirjassa ei ole nimikkeitä. Vapautettujen tuotteiden määrittämisessä tehtävät valinnat määrittävät, miten nimikkeen tuotto kirjataan. Valinnat määrittävät esimerkiksi, kohdistetaanko tuottohinta ja siirretäänkö tuottoa tuottoaikataulua käyttäen.

Määritys voidaan aloittaa **Nimikeryhmä** -sivun **Tuottokirjaus**-pikavälilehdellä (**Tuottokirjaus \> Määritys \> Varaston ja tuotteen määritys \> Nimikeryhmä**). Kyseinen sivu sisältää useita määrityskenttiä. Niitä voidaan käyttää oletusarvojen asettamiseen ainoastaan järjestelmässä luoduille uusille vapautetuille tuotteille. Kun uusia tuotteita luodaan, tässä asetettuja arvoja käytetään nimikeryhmän oletusarvoina. Vapautettujen tuotteiden oletusarvot voidaan ohittaa **Vapautetut tuotteet** -sivulla (**Tuottokirjaus \> Määritys \> Varaston ja tuotteen määritys \> Vapautetut tuotteet**). Vapautetuille tuotteille asetetut oletusarvot siirretään sitten myyntitilaukseen.

## <a name="item-groups-and-released-products"></a>Nimikeryhmät ja vapautetut tuotteet

### <a name="define-the-revenue-schedule"></a>Tuottoaikataulun määritys

Myyntitilausrivin tuottoa siirretään, jos vapautetulle tuotteelle on määritetty tuottoaikataulu, jota käytetään oletusarvoisesti myyntitilausrivillä. Jos asetusta on tarkoitus käyttää tuotteessa oletusarvoisesti, tuottoaikataulu voidaan määrittää **Nimikeryhmä**-sivun **Tuottokirjaus** -pikavälilehdessä (**Tuottokirjaus \> Määritys \> Varaston ja tuotteen määritys \> Nimikeryhmä**). Vapautetun tuotteen asetus voidaan määrittää myös **Vapautetut tuotteet** -sivun **Tuottokirjaus** -pikavälilehdessä (**Tuottokirjaus \> Määritys \> Varaston ja tuotteen määritys \> Vapautetut tuotteet**).

Valitse **Tuottokirjaus**-kentässä tuottoaikataulu, joka vastaa vaadittua tuoton siirtoaikaa. Tuottoaikataulu täytetään automaattisesti myyntitilausriville ja aikataulun tiedot luodaan, kun myyntitilauksen lasku kirjataan.

### <a name="define-the-revenue-price"></a>Tuottohinnan määritys

Nimikeryhmiä ja vapautettuja tuotteita voidaan määrittää käyttäen joko mediaanihintamenetelmää tai alennuksenkohdistusmenetelmää. Molemmat menetelmät edellyttävät useita asetuksia **Vapautetut tuotteet** -sivulla:

- **Onko tuoton kohdistus käytössä** – Jos tämän asetuksen arvoksi asetetaan **Kyllä** vapautettu tuote otetaan huomioon tuoton kohdistuksen laskennassa. Jos asetuksen arvoksi määritetään **EI**, vapautetussa tuotteessa käytetään mediaanihintamenetelmää, jos mediaanihinta on määritetty. Jos mediaanihintaa ei ole määritetty, tuoton tai siirretyn tuoton kirjauksessa käytetään myyntitilausrivin yksikköhintaa.
- **Tuottotyyppi** – Valitse tuottotyyppi, joka vastaa vapautettua tuotetta:

    - **Olennainen** – Nimike on ensisijainen organisaation tuottolähde. Tämä arvo on oletusarvo.
    - **Muu kuin olennainen** – Nimike ei ole ensisijainen organisaation tuottolähde. Kun mediaanihinnan asetuksia käytetään, hinnasta muodostetaan mediaanihinta, joka sitten kohdistetaan. Olennaisella nimikkeellä voi esimerkiksi olla kiinteä hinta, joka on kirjattava tuottona. Jos käytössä on alennus, se voidaan vähentää olennaisen nimikkeen tuotosta, mutta **vain** kiinteän hinnan suuruuteen asti. Muu osa alennuksesta vähennetään muiden kuin olennaisten nimikkeiden tuotosta. Vaihtoehtoisesti alennusta ei vähennetä olennaisen nimikkeen tuotosta.
    - **Sopimuksenjälkeinen tuki** – Nimike tukee muita elementtejä, jotka sisältyvät asiakkaan ostoon. Tuottohinta jaetaan myyntiin kuuluvien olennaisten ja muiden kuin olennaisten tuotteiden kesken. Määrityksestä riippuen sopimuksenjälkeisen tuen nimikkeet eivät välttämättä edellytä sopimuksen alkamis- ja päättymispäivien määrittämistä myyntitilausrivillä.

- **Jätä pois vähennyksestä** – Tämän asetuksen arvoksi määritetään **Kyllä**, jos nimikkeen mediaanihintaa ei voi asettaa määritetyn vähimmäisprosenttiosuuden alapuolelle tai enimmäisprosenttiosuuden yläpuolelle. Tuottohinta johdetaan tällöin muun myyntitilaukseen sisältyvän vapautetun tuotteen tuottohinnasta. Jos tämän asetuksen arvoksi on määritetty **Ei**, nimikkeen mediaanihintaa voidaan muuttaa tai se voidaan vähentää. Huomaa, että useaa sellaista tuotetta myytäessä, jolla mediaanihinta on käytössä, vähintään yhdessä tuotteessa **Jätä pois vähennyksestä** -asetuksen arvoksi on oltava määritettynä **Ei**. Tällöin erot tuottohinnassa voidaan kohdistaa vähintään yhdelle nimikkeelle.
- **Mediaanihinta** – Tämän asetuksen arvoksi määritetään **Kyllä**, jos nimikkeen tuottohinta on tarkoitus muuttaa vastaamaan mediaanihintaa sen alittaessa määritetyn enimmäistoleranssin tai ylittäessä enimmäistoleranssin ja vähennysmäärä on tarkoitus kohdistaa sellaisille riveille, joilla on tuotteitta, joissa **Jätä pois vähennyksestä** -asetuksen arvona on **Ei**.

    - **Enimmäistoleranssi** – Määritä sallittu mediaanihinnan ylittävä prosenttiosuus.
    - **Vähimmäistoleranssi** – Määritä sallittu mediaanihinnan alittava prosenttiosuus.

Kun vapautetun tuotteen asetukset on määritetty, tuottohinta on määritettävä manuaalisesti antamalla käyvä hinta tai mediaanihinta (jos käytetään mediaanihintamenetelmää) **Tuottohinnat**-sivulla (siirry kohtaan **Tuottokirjaus \> Määritys \> Varaston määritys \> Vapautetut tuotteet** ja valitse sitten **Tuottohinnat** **Tuottokirjaus** -ryhmän **Myy**-välilehden toimintoruudussa).

[![Tuottohinnat](./media/revenue-recognition-revenue-prices.png)](./media/revenue-recognition-revenue-prices.png)

Tällä sivulla manuaalisesti määritettyä tuottohintaa käytetään tuottohintakohdistuksen määrittämiseen kussakin myyntitilauksessa määritettyjen ehtojen perusteella. Kukin ehto yhdistetään myyntitilaukseen sen tuottohinnan määrittämiseksi, jota käytetään kohdistusprosessissa.

- **Nimikekoodi** ja **Nimikkeen suhde** – Tuottohinta voidaan määrittää yksittäiselle tuotteelle tai tuoteryhmälle. Jos **Nimikekoodi**-kentässä valitaan **Taulukko**, **Nimikkeen suhde** -kentässä valitaan vapautettu tuote. Jos **Nimikekoodi**-kentässä valitaan **Ryhmä**, **Nimikkeen suhde** -kentässä valitaan nimikeryhmä.
- **Tilikoodi** ja **Tilin/ryhmän numero** – Tuottohinta voidaan määrittää kaikille asiakkaille, yksittäiselle asiakkaalle tai asiakasryhmälle. Jos **Tilikoodi**-kentässä valitaan **Kaikki**, hintaa sovelletaan kaikkiin asiakkaisiin. Jos **Tilikoodi**-kentässä valitaan **Taulukko**, asiakas on valittava **Tilin/ryhmän numero** -kentässä. Jos **Tilikoodi**-kentässä valitaan **Ryhmä**, asiakasryhmä on valittava **Tilin/ryhmän numero** -kentässä.
- **Valuutta** – Jokaiselle myyntitilauksissa käytetylle valuutalle on määritettävä erillinen tuottohinta. Jos myynti esimerkiksi tapahtuu Yhdysvaltojen dollareissa, Kanadan dollareissa ja euroissa, kaikille näille valuutoille on määritettävä tuottohinta. Tuottohintaa ei muuteta yhdestä valuutasta, kuten kirjanpitovaluutasta, muiksi käytettäviksi tapahtumavaluutoiksi.
- **Summa vai prosenttiosuus luettelosta** – Määritä, esitetäänkö tuottohinta summana vai prosenttiosuutena luettelohinnasta. Jos valitset **Prosenttiosuus luettelosta**, käyttäjät voivat antaa mediaanihinnan prosenttiosuutena luettelohinnasta summan sijaan. **Prosenttiosuus luettelosta** -arvoa käytetään vain vapautetuissa tuotteista, jotka on määritetty sopimuksenjälkeisen tuen nimikkeiksi.
- **Tuoton kohdistushinta** – **Summa vai prosenttiosuus luettelosta** -kentässä valitun arvon mukaan tähän syötetään joko summa tai prosenttiosuus, joka edustaa tuoton kohdistuksessa myyntitilauksen elementeille käytettyä tuottohintaa.
- **Alkamispäivä** ja **Päättymispäivä** – Määritä päivämääräväli, jossa tuottohinta on käytössä. Nämä kentät ovat valinnaisia.

Jos **Kirjanpitoparametrit**-sivun asetuksen **Ota alennuksenkohdistusmenetelmä käyttöön** arvoksi on asetettu **Kyllä** ja jos vapautetun tuotteen **Tuottotyyppi**-kentän arvona on **Sopimuksenjälkeinen tuki**, on määritettävä myös vapautetun tuotteen tukemat nimikkeet. Tämä määritetään **Määritysperuste**-sivulla (siirry kohtaan **Tuottokirjaus \> Määritys \> Varaston määritys \> Vapautetut tuotteet** ja valitse sitten **Määritysperuste** **Tuottokirjaus**-ryhmän **Myy**-välilehdellä).

Lisää **Määritysperuste** -sivulla tietue kullekin nimekkeen tukemalla nimikeryhmälle. Kun tuoton kohdistus toteutuu, tuottohinta jaetaan sopimuksenjälkeisen tuen nimekkeen olennaisten ja muiden kuin olennaisten osien kesken.

### <a name="posting-profiles"></a>Kirjausprofiilit

Kolme muuta kirjaustyyppiä tukee mahdollisuutta siirtää tuottoa. Nämä kirjaustyypit määritetään **Kirjaus**-sivun **Myyntitilaus**-välilehdellä (**Tuottokirjaus \> Määritys \> Varaston ja tuotteen määritys \> Kirjaus**).

- **siirretty tuotto** – Anna siirrettyyn tuottoon (tuoton sijaan) kirjattavan tuottohinnan päätili. Tuottohinta siirretään, jos myyntitilausrivillä on tuottoaikataulu.
- **Myytyjen tuotteiden siirretyt kustannukset** – Anna myytyjen tuotteiden sen kustannussumman päätili, joka kirjataan myytyjen tuotteiden siirrettyihin kustannuksiin, jos myös tuottoa siirretään.
- **Osittainen laskutetun tuoton selvitys** – Anna joko myyntitilauksen osittaisen laskutuksen tai uudelleenkohdistuksen yhteydessä käytetyn selvitystilin päätili. Tämän tilin saldo palaa nollaan, kun myyntitilaukset on laskutettu täysimääräisesti.

### <a name="bundles"></a>Niput

Nippunimikkeet ovat ainutkertaisia vapautettuja tuotteita, jotka on määritetty sisältämään komponentteja. Tämä määritys suoritetaan käyttämällä tuoterakennenimiketoimintoa. Kun nippunimike lisätään myyntitilaukseen, yksittäisiä komponentteja käytetään tuottohintojen ja tuottoaikataulujen määritykseen. Nippunimike kuitenkin näkyy asiakkaalle tulostettavissa asiakirjoissa, kuten myyntitilauksessa ja laskussa.

#### <a name="bundle-components"></a>Nippukomponentit

Nippuun sisältyvät komponentit on määritettävä **Vapautetut tuotteet** -sivulla (**Tuottokirjaus \> Määritys \> Varaston ja tuotteen määritys \> Vapautetut tuotteet**). Nämä komponentit ovat vapautettuja tuotteita ja ne on määritettävä samalla tavalla kuin tuoterakennenimikkeeseen sisältyvät tuotteet. Vapautettu tuote voi esimerkiksi olla joko **Esine**-tyypin tai **Palvelu**-tyypin nimike, mutta se on yhdistettävä nimikemalliryhmään, jossa **Varastotuote**-asetuksen arvoksi on määritetty **Kyllä**. Lisätietoja esitetään tuoterakenteen nimikkeiden määritysasiakirjoissa.

Komponentit on määritettävä myös tuottokirjausta varten aivan kuin myyntitilauksessa yksittäin myytävät tuotteet. On esimerkiksi varmistettava, että kullekin komponentille on määritetty oikea tuottohinta ja että sopimuksenjälkeisen tuen nimikkeille on määritetty hintaperuste.

#### <a name="bundle-items"></a>Nippunimikkeet

Nippunimikettä määritettäessä on määritettävä kaksi **Vapautetut tuotteet** -sivun (**Tuottokirjaus \> Määritys \> Varaston ja tuotteen määritys \> Vapautetut tuotteet**):

- Nimike on määritettävä tuoterakenteen nimikkeeksi **Tuotantotyyppi**-kentän **Kehittäjä**-pikavälilehdessä.
- **Nippu**-kentän **Yleistä**-pikavälilehdessä nimike on merkittävä nippunimikkeeksi.

Sen jälkeen komponentit on kohdistettava nipun/tuoterakenteen päänimikkeelle **Tuoterakenteen versiot**-sivulla (siirry kohtaan **Tuottokirjaus \> Määritys \> Varaston ja tuotteen määritys \> Vapautetut tuotteet** ja valitse sitten **Tuoterakenteen versiot** **Tuoterakenne**-ryhmän **Kehittäjä**-välilehden toimintoruudussa). Lisätietoja esitetään tuoterakenteen nimikkeiden määritysasiakirjoissa.

[![Vapautetut tuotteet, tuoterakenteen aikataulut](./media/revenue-recognition-bom-scheduleds.jpg)](./media/revenue-recognition-bom-scheduleds.jpg)

Jos nipun päänimikkeet ja nipun komponentit on asetettu kohdistukselle, nipun tuottohinta jaetaan komponenteille niiden tuottoprosenttiosuuksien perusteella.

## <a name="project-setup"></a>Projektimääritykset

Tuottokirjausta voidaan käyttää myös myyntitilauksissa, jotka luodaan aika- ja materiaaliprojektilla. Projekteihin perustuvien myyntitilausten osalta on vain määritettävä päätilit niissä projektinkirjausprofiileissa, joita käytetään projektilaskujen kirjaukseen. Päätilit määritetään **Kirjanpidon kirjausten määritys** -sivulla (**Tuottokirjaus \> Määritys \> Projektin määritys \> Kirjanpidon kirjausten määritys**).

- **siirretty laskutettu tuotto** (kohdassa **Tuottotilit**) – Lisää siirrettyyn tuottoon (tuoton sijaan) kirjattavan tuottohinnan päätili. Tuottohinta siirretään, jos myyntitilausrivillä on tuottoaikataulu.
- **Siirretyt kustannukset** (kohdassa **Kustannustilit**) – Anna myytyjen tuotteiden sen kustannussumman päätili, joka kirjataan myytyjen tuotteiden siirrettyihin kustannuksiin, jos myös tuottoa siirretään.
