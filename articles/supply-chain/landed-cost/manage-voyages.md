---
title: Hallitse matkoja
description: Tässä aiheessa kuvataan, miten matkoja käsitellään. Matka edustaa yleensä alusta. Käytäntöjen ja menettelyiden mukaan se voi kuitenkin edustaa toimittajaa, ostotilausta tai muuta organisaation kannalta järkevää asiaa.
author: Weijiesa
ms.date: 12/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMTableListPage, ITMTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 7d85ef86351f5d6ac662bb72c88d464fba82f561
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/04/2022
ms.locfileid: "8696163"
---
# <a name="manage-voyages"></a>Hallitse matkoja

[!include [banner](../../includes/banner.md)]

Matka edustaa yleensä alusta. Käytäntöjen ja menettelyiden mukaan se voi kuitenkin edustaa toimittajaa, ostotilausta tai muuta organisaation kannalta järkevää asiaa.

**Kaikki matkat** -sivu sisältää matkan yksityiskohdat, toimitus- ja kustannuslaskentatiedot sekä tietoja nimikkeistä, ostotilauksista ja siirtotilauksista. Voit avata **Kaikki matkat** -sivun siirtymällä kohtaan **Aiheutunut kustannus \> Matkat \> Kaikki matkat**. Tällä sivulla on luettelo kaikista nykyisistä matkoista. Toimintoruudun painikkeiden avulla voit luoda, poistaa ja käsitellä matkoja. Katso minkä tahansa luettelon matkan tiedot valitsemalla se.

> [!NOTE]
> Kuljetuskontit ja pakkaukset on linkitetty matkaan. Ostorivit on linkitetty kuljetuskonttiin. Jos kuljetuskontit ja pakkaukset on poistettu käytöstä, ne voidaan linkittää myös suoraan matkaan. Lisäksi tähän syötetyt kustannukset jaetaan kaikkien liitettyjen ostorivien kesken.

## <a name="action-pane"></a>Toimintoruutu

**Matkat**-sivun toimintoruudussa on painikkeita, joilla valittua matkaa voi käsitellä. Kullakin painikkeella suoritetaan yksittäinen toiminto. Toimintoruudussa on myös välilehtiä, joista kukin puolestaan sisältää joukon asiaan liittyviä painikkeita. Jos toisin ei mainita, kaikki painikkeet ja välilehdet ovat käytettävissä sekä **Kaikki matkat**-sivun luettelonäkymässä että yksittäisen valitun matkan tietonäkymässä.

### <a name="buttons-that-appear-directly-on-the-action-pane"></a>Suoraan toimintoruudussa näkyvät painikkeet

Seuraavassa taulukossa kuvataan painikkeet, jotka ovat käytettävissä suoraan toimintoruudussa.

| Painike | kuvaus |
|---|---|
| Luo uusi | Luo matka. <!-- KFM: Link to scenario --> |
| Delete-näppäin | Poista nykyinen matka. Vain ne matkat, joiden tila on *Vahvistettu*, voi poistaa. Kun matka on lähtenyt satamasta ja käsittelee kuljetettavana olevia tuotteita, sitä ei enää voi poistaa. |
| Matkan muokkaustoiminto | Avaa **Matkaeditori**-sivu, jolla voit lisätä tai poistaa ostorivejä, luoda uusia kontteja ja muokata itse matkan tietoja. |
| Matkan kustannukset | Avaa **Matkan kustannukset** -sivu, jolla voit tarkastella ja lisätä matkan kustannuksia kaikkiin sen sisältämiin tuotteisiin. Kun matkaan lisätään manuaalisesti kustannuksia, ne lisätään automaattisesti **Kustannustiedustelu**-sivulle ja jaetaan kullekin tuotteelle **Matkan kustannukset** sivulla määritetyn menetelmän mukaisesti. |

### <a name="buttons-on-the-voyage-tab"></a>Matkat-välilehden painikkeet

Seuraavassa taulukossa kuvataan painikkeet, jotka ovat käytettävissä toimintoruudun **Matkat**-välilehdessä. Tämä välilehti on käytettävissä vain, kun käsittelet **Kaikki matkat** -sivun luettelonäkymää.

| Painike | kuvaus |
|---|---|
| Lähetyskontti | Avaa sivu, jossa näkyvät kaikki valittuun matkaan liittyvät kuljetuskontit. Kontteja voi olla yksi tai useita. |
| Lasku | Avaa sivu, jossa näkyvät kaikki valittuun matkaan liittyvät pakkaukset. Pakkauksia voi olla yksi tai useita. |

### <a name="buttons-on-the-manage-tab"></a>Hallitse-välilehden painikkeet

Seuraavassa taulukossa kuvataan toiminnot, jotka ovat käytettävissä toimintoruudun **Hallitse**-välilehdessä.

| Painike | kuvaus |
|---|---|
| Asiakirjat vastaanotettu | Päivitä matkaa siten, että **Asiakirjat vastaanotettu** -asetuksen arvona on *Kyllä*. Tämän painikkeen avulla voit lukita nimikkeen ja/tai ostorivin, jotta riviä ei voida enää päivittää. |
| Kuljetuksessa | Päivitä **Matkan tila** kuljetustilaksi, joka on **[Aiheutuneen kustannuksen parametrit](landed-cost-parameters.md)** -sivulla. Tätä prosessia ei ole enempää logiikkaa. Matka voidaan päivittää kuljetustilaan myös automaattisesti [Jäljityksen hallintakeskuksen](delivery-information-setup.md) asetusten perusteella.
| Valmis kustannuslaskentaan | Päivitä **Matkan tila** kustannuslaskentaan valmiiksi tilaksi, joka on **[Aiheutuneen kustannuksen parametrit](landed-cost-parameters.md)** -sivulla. Matkan kustannuslaskenta voidaan suorittaa, kun kaikki laskut on käsitelty (sekä varastolaskut että matkan kustannuslaskut) ja tuotteet on vastaanotettu. Jos matkaan liittyvät arvioitujen kustannusten osalta ei ole suoritettu kustannuslaskentaa, tapahtuu virhe, kun matkan kustannuslaskentaa yritetään suorittaa. |
| Kustannuslaskenta suoritettu | Korjaa kustannuslaskennan virheet, kun kaikille ostotilauksille ja matkakustannuksille on omat laskunsa. Kun valitset tämän painikkeen, **Matkan päivitys – kustannukset laskettu** -valintaikkuna avautuu. Siinä voit valita kirjauksen oletusrahoituspäivämäärälle tai määrittää kirjauspäivämäärän ja sitten suorittaa toiminnon. Voit suorittaa toiminnon uudelleen haluamasi määrän kertoja. Voit myös käyttää **Matkan päivitys – kustannukset laskettu** -valintaruutua määrittääksesi aikataulun toiminnon säännölliselle suorittamiselle (erätyö). On suositeltavaa suorittaa toiminto säännöllisesti määrittämällä se erätyöksi. |
| Kirjaa vastaanottoluettelo | Kirjaa vastaanottoluettelo kaikille matkan ostotilausriveille.  |
| Kirjaa tuotteen vastaanotto | Kirjaa tuotteen vastaanotto kaikille matkan tilausriveille. Tuotteen vastaanottoprosessia matkaan liittyvien ostotilausrivien osalta käytetään vain, jos tuotteet **eivät** käy läpi kuljetettavien tuotteiden käsittelyä. Jos tuotteet käyvät läpi kuljetettavien tuotteiden käsittelyn, saat virheilmoituksen, kun yrität kirjata ostotilausrivin tuotteen vastaanoton.  |
| Kirjaa lasku | Kirjaa lasku kaikille matkan tilausriveille. Jos matkan tuotteet käyvät läpi kuljetettavien tuotteiden käsittelyn, ostotilausrivit laskutetaan, ennen kuin vastaanottoprosessi on valmis. Kun alkuperäinen ostotilaus laskutetaan, luodaan alkuperäisiin ostotilausriveihin liittyvät kuljetettavien tuotteiden tilaukset. Tämän jälkeen varasto voi vastaanottaa tilaukset.  |
| Lähetyksen siirtotilaus | Kirjaa siirtotilausmatka kaikille matkan kuljetustilausriveille. Kun tämä painike on valittuna, vain siirtotilauksia voidaan päivittää. |
| Vastaanota siirtotilaus | Kirjaa siirtotilauksen vastaanotto kaikille matkan kuljetustilausriveille. |
| Vastaanota matkalla olevat tavarat | Vastaanota kaikki tilausrivit, jotka ovat kuljetettavana matkassa. Tämä painike on yksi kolmesta vaihtoehdosta, joita voi käyttää matkan kuljetettavien tuotteiden vastaanottoon. (Kaksi muuta vaihtoehtoa ovat **Luo saapumisten kirjauskansio** -painike, joka kuvataan myöhemmin tässä taulukossa, sekä varastonhallinnan mobiilisovellus.) Tämä vaihtoehto on yksinkertaisin vaihtoehto, jossa kuljetettavana olevat tuotteet käsitellään kuljetettavien tuotteiden varastosta lopulliseen kohdevarastoon. Jos haluat hallita prosessia tarkemmin, käytä tuotteiden vastaanoton käsittelyyn saapumisten kirjauskansiota tai mobiililaitetta. |
| Hae automaattiset kustannukset | Etsi asianomaiset matkakustannukset. Jos nämä kustannukset on jo löydetty tai päivitetty, näyttöön tulee viesti "Laskuttamattomia kustannusrivejä löytyi. Haluatko korvata ne?" Kaikki kustannukset, joita ei ollut liitetty matkaan sen luontihetkellä, haetaan. Matkakustannuksia, jotka on liitetty matkoihin ja laskutettu, ei korvata. |
| Luo saapumisen kirjauskansio | <p>Avaa **Luo saapumisten kirjauskansio** -valintaikkuna, jossa voit luoda sijainnin erittelevän saapumisten kirjauskansion. Valintaikkunassa sisältää seuraavat vaihtoehdot:</p><ul><li>**Luo kuljetettavista tuotteista** tai **Luo siirtotilauksesta** – Tämän vaihtoehdon otsikko muuttuu sen mukaan, käytätkö kuljetettavien tuotteiden prosessia. Valitse *Kyllä*, jos haluat avata saapumisten kirjauskansiosivun, jonka avulla voit käsitellä matkaan liittyvien kuljetettavien tuotteiden vakiomallista saapumisten kirjauskansiota. Jos nimike on jo vastaanotettu lopulliseen kohdevarastoon, sitä ei lisätä saapumisten kirjauskansion riveille.</li><li>**Alusta määrä** – Voit alustaa vastaanotettavan määrän matkan rivillä määritetyn tuotemäärän perusteella valitsemalla tämän vaihtoehdon arvoksi *Kyllä*. Jos matkarivi on vastaanotettu osittain, tämä määrä on jäljellä oleva määrä. On suositeltavaa asettaa tämän asetuksen arvoksi *Kyllä*.</li><li>**Luo tilausriveiltä** – Määritä tämän asetuksen arvoksi *Kyllä*, jos haluat käyttää tilausrivien arvoa.</li></ul><p>Tämä painike on yksi kolmesta vaihtoehdosta, joita voi käyttää matkan tuotteiden vastaanottoon. (Muut vaihtoehdot ovat **Vastaanota kuljetettavat tuotteet** -painike, joka kuvattiin aiemmin tässä taulukossa, sekä varastonhallinnan mobiilisovellus.)</p> |
| Jaksota kustannukset | Kustannukset voi jaksottaa, jos kustannuslajin veloitukselle on määritetty kirjanpitotili. Tätä painiketta käytetään yleensä, kun varasto on kuljetettava tai kun tuotteet on vastaanotettu ja laskutettu. |
| Koosta kustannukset | Siirrä kustannuksia kuljetuskontin tasolta matkatasolle. Voit käyttää tätä painiketta yhteisten palvelujen/kuljetusten tilanteessa, joissa useat yksiköt käyttävät samaa kuljetuskonttia tai pakkaustilaa. Käytetään esimerkkinä matkaa, jossa on 12 metrin ja 6 metrin kuljetuskontit ja jako tapahtuu tilavuuden perusteella. Tässä tapauksessa tuotteille/yksiköille, jotka jakavat tai käyttävät 6-metrisen kuljetuskontin tilaa, voi koitua haittaa. Kustannusten oikeudenmukaista jakamista varten joidenkin organisaatioiden kannattaa siirtää matkan kustannukset ja jakaa ne matkatason jakomenetelmän perusteella. |
| Muuta matkamallia | Näyttöön tulee valintaikkuna, jossa voit muokata matkamallia. Kun olet vaihtanut mallin, kaikki matkan kustannukset poistetaan. Siksi voi olla tarpeen valita **Hae automaattiset kustannukset** (katso kuvaus ylempänä tässä taulukossa) tai lisätä kustannukset jälleen manuaalisesti. |

### <a name="buttons-on-the-general-tab"></a>Yleistä-välilehden painikkeet

Seuraavassa taulukossa kuvataan painikkeet, jotka ovat käytettävissä toimintoruudun **Yleistä**-välilehdessä.

| Painike | kuvaus |
|---|---|
| Saapumisluettelo | Avaa tuotteiden vastaanottojen luettelo kaikkien matkan ostotilausrivien osalta.  Jos tuotteiden vastaanottoluetteloja ei ole käsitelty, tämä painike ei ole käytettävissä. |
| Tuotteen vastaanotto | Avaa matkaan liitettyjen ostotilausrivien tuotteiden vastaanottotietue, jos kyseistä tietuetta käytetään. Jos tuotteiden vastaanottoja ei ole kirjattu, tämä painike ei ole käytettävissä. Tuotteen vastaanottoprosessia ei käytetä, jos käytät kuljetettavien tuotteiden käsittelyä. |
| Nimikkeen saapuminen | Avaa nimikkeen saapumisten kirjauskansio, jos sitä käytetään. |
| Seuranta | Avaa **Saapuvien jäljitys** -sivu, jolla voit päivittää kuljetuskontissa olevien tuotteiden ja matkan odotettua saapumispäivää sekä sen jälkeen päivittää ostotilausrivien odotettuja toimituspäivämääriä. |
| Kustannuskysely | <p>Avaa **Kustannustiedustelu**-sivu, jolla näkyvät kaikki matkan kustannukset.</p><p>Muokkaa näkymää valitsemalla toimintoruudusta **Näkymä**. Voit tarkastella mitä tahansa tasoa sekä nimike- kustannuslajikoodia.</p><p>**Kustannustiedustelu**-sivulla näkyvät vain kustannuslajikoodit, jotka liittyvät suoraan varastotapahtumiin. Poistamalla kustannuslajikoodeja voit muokata sivua ryhmittäen kustannuksia yhteen. Tämä ominaisuus voi olla hyödyllinen, kun käytät kokoja ja värejä.</p><p>**Kustannustiedustelu**-sivulla näkyvät vain kustannuslajikoodit, joissa **Veloitus**-kentän arvona on *Nimike*.</p> |
| Matkalla olevien tavaroiden tilaukset | Avaa **Kuljetettavien tuotteiden tilaukset** -sivu, jolla näkyvät vain valitun matkan kuljetettavien tuotteiden tietueet. |

## <a name="lines-view"></a>Rivinäkymä

Voit avata **Rivit**-näkymän avaamalla matkan ja valitsemalla sitten **Rivit**-välilehden matkan otsikon oikealta puolelta.

### <a name="information-on-the-voyage-header-fasttab"></a>Matkan otsikon pikavälilehden tiedot

**Matkan otsikko**-pikavälilehti matkan **Rivit**-näkymässä sisältää matkaa kuvaavia perustietoja. Monet tällä pikavälilehdellä näkyvistä kentistä näkyvät myös **Otsikko**-näkymässä tässä ohjeaiheessa myöhemmin kuvatulla tavalla.

### <a name="information-on-the-voyage-lines-fasttab"></a>Matkan rivien pikavälilehden tiedot

Matkan **Matkan rivit** -pikavälilehti sen **Rivit**-näkymässä liittyy matkan tietoihin sekä kustannuslaskentatietoihin, joita sovelletaan matkan tasolla. Täällä voit tarkastella matkaan liitettyjä kuljetuskontteja, pakkauksia ja nimikkeitä. Näkyvissä ovat myös matkassa olevien nimikkeiden hinta ja määrä. Voit tarkastella mitä tahansa luettelossa olevaa kuljetuskonttia tai pakkausta valitsemalla sen linkin.

### <a name="information-on-the-line-details-fasttab"></a>Tietoa Rivin tiedot -pikapalkista

Matkan **Rivit**-näkymän **Rivin tiedot** -näkymässä on lisätietoja **Matkan rivit** -pikavälilehdessä valittuna olevasta rivistä. Huomaa, että tämä pikavälilehti sisältää tietoja kunkin rivin paikasta kontista ja ilmoitetusta määrästä.

## <a name="header-view"></a>Otsikkonäkymä

Voit avata **Otsikko**-näkymän avaamalla matkan ja valitsemalla sitten **Otsikko**-välilehden matkan otsikon oikealta puolelta.

### <a name="settings-on-the-general-fasttab"></a>Yleinen-pikavälilehden asetukset

Seuraavassa taulukossa kuvataan kentät, jotka ovat käytettävissä matkan **Otsikko**-näkymän **Yleistä**-pikavälilehdessä.

| Kenttä | kuvaus |
|---|---|
| Matka | Syötä matkan tai lennon numero. |
| Varausviite | Jos lähettäjä tai lähetyskeskus antaa viitenumeron, jonka avulla matka voidaan tunnistaa (eli lähettäjän tai lähettäjän sisäisen viitteen), syötä se tähän. |
| Alus | Syötä tai valitse alus. Jos alus ei ole arvoluettelossa, voit syöttää aluksen tunnuksen vapaana tekstinä. Tällöin päätaulukkoa ei päivitetä, jolloin aluksen tunnus voidaan valita tässä kentässä myöhemmin. |
| Ulkoisen matkan tunnus | Syötä matkan julkisesti saatavilla oleva tunnus (kuten lennon numero). |
| Päälentorahtikirja/rahtikirja | Syötä päälentorahtikirjan tai rahtikirjan numero. Voit määrittää tämän arvon, kun kuljetus tapahtuu ilmateitse. |
| Alalentorahtikirja/rahtikirja | Syötä kuljetuskontin sisäinen lentorahtikirja tai rahtikirja. |
| Vuokra | Valitse tämä valintaruutu, kun haluat ilmaista, että kontti on vuokrakontti, joka on palautettava. |
| kuvaus | Kirjoita matkalle kuvaus, jotta se on helpompi tunnistaa. |
| Matkan tila | Matkan tila. Arvoja ovat *Luotu*, *Kuljetettavana*, *Asiakirjat vastaanotettu* ja *Kustannuslaskenta suoritettu*. Tätä kenttää ei lasketa logiikan perusteella. Se päivitetään ainoastaan kirjaustoiminnon kautta. *Kustannuslaskenta suoritettu* -arvo ilmaisee, että varastosta ja kaikista matkakustannuksista on vastaanotettu lasku. Jos laskua ei ole vastaanotettu, matka ei voi siirtyä tilaan *Kustannukset laskettu*. |
| Ostotilauksen tila | Edistynein tila, joka on saavutettu kaikissa matkaan liittyvissä ostotilauksissa. |
| Asiakirjat vastaanotettu | Arvo, joka ilmaisee, onko yritys vastaanottanut kaikki matkaan liittyvät asiakirjat. Tätä arvoa voi muuttaa valitsemalla toimintoruudun **Hallitse**-välilehden **Matkan päivitys** -ryhmässä **Asiakirjat vastaanotettu**. |
| Kuljetusyritys | Valitse tämän matkan rahdinkuljettaja. Tätä kenttää voidaan käyttää automaattisten kustannusten määrittämiseen. |
| Nimi | **Rahdinkuljettaja**-kentässä valitun yrityksen nimi. |
| Mittaus | Tämän kentän avulla automaattiselle kustannukselle voi määrittää mitan. Mittoja käyttävät usein organisaatiot, jotka eivät tiedä tuotteiden yksilöllisiä tilavuuksia tai painoja mutta tarvitsevat tarkemman jakoperusteen kuin määrän tai summan. Huolitsija ilmoittaa painon tai kuutiomitan, jonka voi syöttää joko nimikkeen tai ostotilauksen tasolle. Se voidaan päivittää automaattisesti, jos parametri on valittu, tai sen voi syöttää manuaalisesti. |
| Mittayksikkö | Mittayksikkö, jota käytetään **Mitta**-kentässä. |
| Kuormalavojen määrä | Määritä matkarivin kuormalavojen määrä. Tämä kenttä päivitetään automaattisesti, jos **Aiheutuneiden kustannusten parametrit** -sivun **Yleistä**-välilehden **Päivitä pakkaus automaattisesti** -asetuksen arvona on *Kyllä*. |

### <a name="settings-on-the-delivery-fasttab"></a>Toimitus-pikavälilehden asetukset

Seuraavassa taulukossa kuvataan kentät, jotka ovat käytettävissä merikuljetuksen **Otsikko**-näkymän **Toimitus**-pikavälilehdessä.

| Kenttä | kuvaus |
|---|---|
| Luonnin päivämäärä ja aika | Päivämäärä ja aika, jona matkatietue on luotu. |
| Lähettäjältä noutamisen päivämäärä | Tämä kenttä valitsee aikaisimman vapaasti tehtaalla -päivämäärän matkaan liittyvien ostotilausten joukosta. Vapaasti tehtaalla -päivämäärä on käytettävissä ostotilauksen otsikossa, ja se päivitetään käyttämällä jäljityksenhallintaominaisuutta. |
| Lähetyspäivä | Arvioitu päivämäärä, jona lentokone tai alus lähtee lähtöpisteestä. |
| Lähtöpäivämäärä | Lähtöpäivämäärä on yleensä päivämäärä, jona lentokone tai alus todella lähtee ulkomailla olevasta lähtöpaikastaan. Lähetyspäivämäärien ja lähtöpäivämäärien ei tarvitse vastata toisiaan. **Lähtöpäivämäärä**-kenttä on tarkoitettu vain tiedoksi. Sitä ei käytetä odotetun toimituspäivän arvioinnissa. Jäljityksenhallintatoiminnon avulla arvioidaan odotettu toimituspäivä. Tämän kentän voi määrittää siten, että jäljityksenhallintatoiminto täyttää sen automaattisesti. |
| Myymälään tulon päivämäärä | Tämä kenttä valitsee aikaisimman päivämäärän, jona matkaan liittyvien ostotilausten tuotteet ovat myytävissä. |
| Arvioitu toimituspäivämäärä | Arvioitu toimituspäivä on yleensä päivämäärä, jona tuotteiden on määrä saapua varastoon. Tämä kenttä on tarkoitettu vain tiedoksi. Sitä ei käytetä tuotteiden pääsuunnitteluun. Ostotilausrivin odotettua toimituspäivää käytetään matkan tuotteiden pääsuunnitteluun, ja se päivitetään jäljityksenhallintatoiminnon avulla. Tämän kentän voi määrittää niin, että jäljityksenhallintatoiminto täyttää sen. |
| Todellinen toimituspäivämäärä | Varhaisin toimituspäivä matkaan liittyvien tuotteiden perusteella. |
| Arvioitu saapumisaika lähetyssatamaan | Syötä päivämäärä, jona odotat matkan saapuvan lähetyspaikkaan, huolitsijan antamien tietojen perusteella. |
| Alkuperäiset asiakirjat vastaanotettu | Syötä päivämäärä, jona alkuperäiset asiakirjat on otettu vastaan. |
| Välittäjä neuvoi | Syötä päivämäärä, jona välittäjälle on ilmoitettu. |
| Alkuperäinen rahtikirja lähetetty | Syötä päivämäärä, jona alkuperäinen rahtikirja on lähetetty. |
| Vapautetut tavarat | Syötä päivämäärä, jona tuotteet on vapautettu tullista. |
| Asiakastapaaminen | Syötä asiakastapaamisen päivämäärä eli päivämäärä, jona odotat asiakkaan ottavan tuotteet omistukseensa. |
| Toimitettu varastoon | Syötä päivämäärä, jona tuotteet on toimitettu varastoon. |
| Tarkistuspäivämäärä | Syötä kirjauspäivämäärä. |
| Toimitusohjeet | Syötä päivämäärä, jona toimitusohjeet on otettu vastaan. |
| Toimitustapa | Tässä kentässä on tietoja menetelmästä, jota käytetään matkan ja kulloiseenkin toimitustapaan liittyvien automaattisten kustannusten kustannusvalinnan toimittamiseen. |
| Lähtösatama | Lähtösatama, josta matka alkaa. |
| Satamaan | Satama, johon matka saapuu. Kuljetuskonteilla voi olla eri satamia, koska laiva saattaa pysähtyä useissa satamissa. Tarkistamalla kohdesataman kuljetuskonttitasolla annat tarkat satamatiedot jokaisesta matkaan kuuluneesta kuljetuskontista. Rahtiin liittyvä automaattinen kustannus määräytyy kuljetuskontin tyypin, kohdesataman ja lähtösataman perusteella. |
| Paikallinen huolitsija | Tämä kenttä on tarkoitettu vain tiedoksi. Paikallisen huolitsijan pitäisi olla valittavissa toimittajaluettelosta. |
| Paikallisen kuljetuksen päivämäärä | Päivämäärä, jolle paikallinen kuljetus on varattu. Tämä kenttä voi auttaa varastoa suunnittelussa. |
| Paikallisen kuljetuksen aika | Aikaväli, jolle paikallinen kuljetus on varattu. Tämä kenttä voi auttaa varastoa suunnittelussa. |
| Matkamalli | Matkalle määritetty matkamalli. Matkamallia käytetään kuljetuskontin ja matkan lähtö- ja kohdesataman syöttämiseen. Nämä arvot puolestaan auttavat tunnistamaan matkaan liittyvät automaattiset kustannukset. |

### <a name="settings-on-the-other-fasttab"></a>Muuta-pikavälilehden asetukset

Seuraavassa taulukossa kuvataan kentät, jotka ovat käytettävissä merikuljetuksen **Otsikko**-näkymän **Muut**-pikavälilehdessä.

| Kenttä | kuvaus |
|---|---|
| Huomautukset | Määritä matkaan liittyvät lisätiedot. |
| Arvostuspäivämäärä | Valitse aikaisin vapaasti tehtaalla -päivämäärän matkaan liittyvien ostotilausten joukosta. |
| Odottava matka | Voit käyttää tätä ilmaisemaan, onko lähetys tai matka jo lähtenyt. Se on tarkoitettu vain tiedoksi.  |
| Kuljetuskonttien nimen muuttaminen | Useita kontteja sisältävissä matkoissa niiden konttien määrä, joita ei vielä ole vastaanotettu. |

## <a name="voyage-update-periodic-tasks"></a>Säännölliset matkanpäivitystehtävät

**Aiheutunut kustannus** -moduuli sisältää useita matkaan liittyviä säännöllisiä tehtäviä, jotka voivat joukkopäivittää useita matkojen tietoja. Voit suorittaa tai ajoittaa nämä säännölliset tehtävät siirtymällä kohtaan **Aiheutunut kustannus \> Säännölliset tehtävät \> Matkan päivitykset** ja valitsemalla sitten jokin seuraavista tehtävätyypeistä:

- **Asiakirjat vastaanotettu** – Tämän tehtävän avulla voit määrittää samanaikaisesti useiden matkojen kohdan **Asiakirjat vastaanotettu** arvoksi *Kyllä*. **Suodatin**-asetusten avulla voit määrittää, minkä matkajoukon haluat päivittää.
- **Kuljetettavana** – Tämän tehtävän avulla voit määrittää samanaikaisesti useiden matkojen kentän **Matkan tila** kentän arvoksi kuljetustilan, joka on määritetty **[Aiheutuneen kustannuksen parametrit](landed-cost-parameters.md)**-sivulla. **Suodatin**-asetusten avulla voit määrittää, minkä matkajoukon haluat päivittää.
- **Valmiina kustannuslaskentaan** – Tämän tehtävän avulla voit määrittää samanaikaisesti useiden matkojen kentän **Matkan tila** arvoksi kustannuslaskentavalmiin tilan, joka on määritetty **[Aiheutuneen kustannuksen parametrit](landed-cost-parameters.md)**-sivulla. Tämä tehtävä määritetään useimmiten suoritettavaksi säännöllisellä aikataululla.
- **Kustannukset laskettu** – Tämän tehtävän avulla voit määrittää samanaikaisesti useiden matkojen kentän **Matkan tila** arvoksi laskettujen kustannusten tilan, joka on määritetty **[Aiheutuneen kustannuksen parametrit](landed-cost-parameters.md)** -sivulla, jos kustannukset on laskettu, mutta niitä ei ole vielä päivitetty matkaan. Tämä tehtävä määritetään useimmiten suoritettavaksi säännöllisellä aikataululla.
