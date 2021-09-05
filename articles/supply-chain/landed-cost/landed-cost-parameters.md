---
title: Aiheutuneen kustannuksen parametrien määritys
description: Tässä aiheessa käsitellään niiden yleisten tietojen ja määritysasetusten määrittämistä, joita käytetään Aiheutunut kustannus -moduulissa kirjaamiseen, tilapäivityksiin, numerosarjoihin ja toimintoihin.
author: sherry-zheng
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 3b6678b2579db00a9f8884786fdaacd027fab744
ms.sourcegitcommit: 7aa7d756e1e98a53da62e03c608a9597ef9893ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/20/2021
ms.locfileid: "7403973"
---
# <a name="landed-cost-parameters-setup"></a>Aiheutuneen kustannuksen parametrien määritys

[!include [banner](../../includes/banner.md)]

**Aiheutuneen kustannuksen parametrit** -sivulla määritetään yleiset tiedot ja konfiguraatioasetukset, joita käytetään koko **Aiheutunut kustannust** -moduulissa kirjaamiseen, tilapäivityksiin, numerosarjoihin ja toimintoihin. Parametrien asetukset ovat yhteisiä yrityksille, ja järjestelmänvalvoja voi muokata sitä.

## <a name="open-the-landed-cost-parameters-page"></a>Avaa Aiheutuneen kustannuksen parametrit -sivu

Voit käyttää parametreja kohdassa **Aiheutunut kustannus \> Määritys \> Aiheutuneen kustannuksen parametrit** ja määrittää sitten kentät seuraavissa aliosissa kuvatulla tavalla.

![Aiheutuneen kustannuksen parametrit -sivu.](media/landed-cost-parameters.png "Aiheutuneen kustannuksen parametrit -sivu")

## <a name="general-tab"></a>Yleinen-välilehti

### <a name="general-fasttab"></a>Yleinen-pikavälilehti

Seuraavassa taulukossa käsitellään kenttiä, jotka ovat käytettävissä **Yleiset**-välilehden **Yleiset**-pikavälilehdessä **Aiheutuneen kustannuksen parametrit** -sivulla.

| Asetus | kuvaus |
|---|---|
| Käytä lähetyshintaa | Lähetyshinta määritetään määritetylle ajanjaksolle, ja sitä käytetään useita valuuttoja käyttävien tuotteiden arvioiduissa kustannuksissa. Määritä tämä vaihtoehto arvoon *Kyllä*, jos haluat käyttää lähetyshintaa. |
| Vaihtokurssin tyyppi | Vaihtokurssien oletuskokoelma, jota käytetään monivaluutan laskentoja varten merikuljetuksen ja merikuljetuksen kustannusten osalta. |
| Päivitä ostotilauksen määrä | Valitse, mitä tapahtuu, jos käyttäjä muuttaa ostotilausrivin määrän:<ul><li>**Hyväksy** – Merikuljetuksen määrää säädetään automaattisesti.</li><li>**Varoitus** – Jos rivi on liitetty merikuljetukseen, tulee varoitus näyttöön, mutta merikuljetuksen määrä päivitetään.</li><li>**Virhe** – Jos rivi on liitetty merikuljetukseen, näyttöön tulee virhesanoma eikä ostotilausta voi päivittää. Sen vuoksi tilausrivi on ensin poistettava merikuljetuksesta.</li></ul> |
| Päivitä laatikoiden määrä automaattisesti | Kun tämän vaihtoehdon arvoksi määritetään *Kyllä*, kaikki pakkaukset lisätään yhteen ja ne näkyvät merikuljetus- ja konttitasoilla. Kun sen arvoksi on asetettu *Ei*, pakkausten määräksi asetetaan aluksi 0 (nolla) ja sitä voi tarvittaessa muokata manuaalisesti. |

### <a name="costing-fasttab"></a>Kustannuslaskenta-pikavälilehti

Seuraavassa taulukossa käsitellään kenttiä, jotka ovat käytettävissä **Yleiset**-välilehden **Kustannuslaskenta**-pikavälilehdessä **Aiheutuneen kustannuksen parametrit** -sivulla.

| Asetus | kuvaus |
|---|---|
| Kirjauserittely | Valitse arvon oikaisu kirjanpidossa:<ul><li>**Yhteensä** – Kirjanpitoon kirjataan kokonaissumma.</li><li>**Nimikeryhmä** – Oikaisu määritetään nimikeryhmittäin.</li><li>**Nimiketunnus** – Oikaisu määritetään nimikkeittäin. Tämä arvo sisältää yksityiskohtaisimmat tiedot.</li></ul> |
| Salli nollakustannukset | Aseta vaihtoehdoksi *Ei*, jos haluat näyttää virheen, jos käyttäjä yrittää kirjata kustannusarvion merikuljetuksen laskulle tai ostotilaukselle, joka ei sisällä odotettua merikuljetuksen kustannusta. Virhesanomassa osoitetaan, että nollakustannusta ei voi kohdistaa ja laskun kirjaus epäonnistuu. Tässä tapauksessa käyttäjä voi päivittää arvion manuaalisesti (tai määrittää automaattisen kustannuksen uudelleen) ja joko hakea päivitetyn arvon tai poistaa kustannuksen, jos se ei ole voimassa.<p>Aseta vaihtoehdoksi *Kyllä*, jos haluat sallia, että merimatkan kustannus on tyhjä. Tällöin kustannusalueen mukaan kohdistetaan nollahinta. Toimittajan kustannuslaskun voi tämän jälkeen käsitellä nollahintaista kustannusta vastaan merikuljetusta vastaanotettaessa.</p><p>Suosittelemme, että määrität arvion automaattisessa kustannustietueessa, jotta nollahintainen kustannus ei näkyisi. Vaikka tämä arvio ei ole täysin tarkka, sen pitäisi olla tarkempi kuin oletettu nollakustannus.</p> |
| Oikaisun kirjauspäivä | Kun kirjaat ostoreskontran merikuljetuksen kustannuslaskun, myös selvitystaulukko (varasto-oikaisut) päivitetään. Valitse oletusarvon mukaan asetettu päivämäärä **Valitse merikuljetuksen kustannukset** -sivulla, kun olet laskukirjauskansiossa:<ul><li>**Tapahtumapäivä** – Käytä kirjauskansion päivämäärää (kirjauspäivämäärä).</li><li>**Ostotilauksen laskun päivämäärä** – Käytä varaston (ostotilauksen) laskun taloushallinnon kirjauspäivämäärää.</li><li>**Valittu päivämäärä** – Käyttäjä voi määrittää kirjauspäivämäärän. Vaikka päivämäärä voidaankin jättää tyhjäksi, jos se on silti tyhjä kustannuslaskun kirjaamispäivänä, näyttöön tulee virheilmoitus.</li></ul> |
| Käytä ostolaskutositetta | Kun tämän asetuksen arvoksi määritetään *Kyllä*, kustannusten jaksotustapahtumissa käytetään samaa tositenumeroa, jota ostolaskussa käytetään. Kun arvoksi on määritetty *Ei*, järjestelmä käyttää seuraavaa käytettävissä olevaa **Kustannusten jaksotustositteen** numerosarjan numeroa, joka on määritetty **Aiheutuneen kustannuksen parametrit** -sivun **Numerosarjat**-välilehdessä.<p>Tämä vaihtoehto on käytössä vain, kun **Kirjaa kirjanpidon veloitustilille** -asetuksen arvona on *Kyllä* **Ostoreskontran parametrit** -sivun **Lasku**-välilehdessä.</p> |
| Estä manuaalinen kirjaaminen selvitystilille | Määritä tämän vaihtoehdon arvoksi *Kyllä*, jos haluat estää kirjaamisen selvitystileihin, joissa tapahtumaa ei ole linkitetty merikuljetukseen, valitsemalla toimittajan laskukirjauskansion toimintoruudusta **Toiminnot \> Valitse merikuljetuksen kustannukset**. Suosittelemme, että määrität tämän asetuksen arvoksi *Kyllä*, jotta merikuljetus ja selvitystili voidaan selvittää oikein. |
| Käytä kustannustyypin veloituksen jaksotustiliä | Kun tämän vaihtoehdon arvoksi määritetään *Kyllä*, veloituksen jaksotustiliä, joka on määritetty asianmukaista kustannustyyppikoodia varten **Kustannustyyppien koodit** -sivulla, käytetään kustannusten jaksottamiseen kuluna.<p>Tämä vaihtoehto on käytössä vain, kun **Kirjaa kirjanpidon veloitustilille** -asetuksen arvona on *Kyllä* **Ostoreskontran parametrit** -sivun **Lasku**-välilehdessä. |
| Kirjaa oikaisut varianssina | Kun tämän asetuksen arvo on *Kyllä*, se ohittaa vakiotoiminnon ja pakottaa varasto-oikaisutapahtumat, jotka liittyvät arvioitujen kustannusten ja todellisten kustannusten varianssitapahtumiin, jotka kirjataan varianssitilille.<p>Kun tämän vaihtoehdon arvoksi määritetään *Ei*, variansseihin liittyviä varaston oikaisutapahtumia käsitellään kustannuslaskentamenetelmän ja kustannustyyppikoodin konfiguroinnin perusteella. Standardikustannusten varianssit kirjataan edelleen varianssitilille. Painotettua keskiarvoa (WMA) siirrettäessä varianssit kirjataan joko varianssitilille tai varastoon.</p><p>Tämä vaihtoehto on käytössä vain, kun **Kirjaa kirjanpidon veloitustilille** -asetuksen arvona on *Kyllä* **Ostoreskontran parametrit** -sivun **Lasku**-välilehdessä.</p> |

### <a name="validation-fasttab"></a>Vahvistus-pikavälilehti

Seuraavassa taulukossa käsitellään kenttiä, jotka ovat käytettävissä **Yleiset**-välilehden **Vahvistus**-pikavälilehdessä **Aiheutuneen kustannuksen parametrit** -sivulla.

| Asetus | kuvaus |
|---|---|
| Usean kustannuksen laskut | Valitse, mitä tapahtuu, jos useita laskuja käsitellään merikuljetusta, pakkausta tai konttia vastaan samana muuna kuluna.<ul><li>**Hyväksy** – Järjestelmän tulisi sallia useita kustannuslaskuja.</li><li>**Varoitus** – Näytetään varoitus.</li><li>**Virhe** - Näyttöön tulee virhesanoma.</li></ul> |
| Useita toimittajia laskua kohden | Valitse, mitä tapahtuu, jos useamman kuin yhden toimittajan ostotilaukset lisätään pakkaukseen.<ul><li>**Hyväksy** – Järjestelmän pitää sallia toimenpide.</li><li>**Varoitus** – Näytetään varoitus, mutta toimenpide voidaan silti suorittaa.</li><li>**Virhe** – Näyttöön tulee virhesanoma, ja toimenpide estetään.</li></ul><p>Tulliasioitsija tai paikallinen laki saattaa valtuuttaa tälle kentälle tietyn arvon.</p> |
| Usean toimitustavan toleranssi | Valitse, mitä tapahtuu, jos tuotteet ostotilauksesta, joka käyttää eri toimitustapoja kuin merikuljetus, lisätään merikuljetukseen.<ul><li>**Hyväksy** – Järjestelmän pitää sallia toimenpide.</li><li>**Varoitus** – Näytetään varoitus, mutta toimenpide voidaan silti suorittaa.</li><li>**Virhe** – Näyttöön tulee virhesanoma, ja toimenpide estetään.</li></ul> |
| Usean varaston toleranssi | Valitse, mitä tapahtuu, jos merikuljetus sisältää useita tilausrivejä, jotka on toimitettava eri varastoihin. Nämä tilausrivit voidaan jakaa yhden tai usean ostotilauksen välillä.<ul><li>**Hyväksy** – Järjestelmän pitää sallia toimenpide.</li><li>**Varoitus** – Näytetään varoitus.</li><li>**Virhe** - Näyttöön tulee virhesanoma.</li></ul> |
| Tilavuus puuttuu | Valitse, mitä tapahtuu, jos käyttäjä lisää merikuljetukseen nimikkeen ilman tilavuutta.<ul><li>**Hyväksy** – Järjestelmän pitäisi hyväksyä nimike.</li><li>**Varoitus** – Näytetään varoitus.</li><li>**Virhe** - Näyttöön tulee virhesanoma.</li></ul><p>Jos tilavuuksien avulla lasketaan ja jaetaan kustannuksia, on suositeltavaa valita joko *Varoitus* tai *Virhe*.</p> |
| Palvelujen tarjoaja ilman matkakustannuksia | Valitse, mitä tapahtuu, jos käyttäjä yrittää käsitellä sellaisen palveluntarjoajan laskua, jota ei ole linkitetty merikuljetukseen. <ul><li>**Hyväksy** – Järjestelmän pitää sallia toimenpide.</li><li>**Varoitus** – Näytetään varoitus.</li><li>**Virhe** - Näyttöön tulee virhesanoma.</li></ul><p>On suositeltavaa valita *Varoitus*.</p> |

### <a name="defaults-fasttab"></a>Oletusarvot-pikavälilehti

Seuraavassa taulukossa käsitellään kenttiä, jotka ovat käytettävissä **Yleiset**-välilehden **Oletusarvot**-pikavälilehdessä **Aiheutuneen kustannuksen parametrit** -sivulla.

| Asetus | kuvaus |
|---|---|
| Kirjauskansion nimi | Valitse oletuskirjauskansio, jota *Luo saapumisten kirjauskansio* -toiminnon tulee käyttää. |
| Matkan tila | Valitse tila, joka merikuljetuksella on oltava, ennen kuin käyttäjät voivat määrittää sitä varten vuokrakontin järjestelmään. Tämä toimenpide tapahtuu yleensä, kun tavarat ovat kuljetettavana tai laiturilla. |
| Matkamalli | Valitse oletusmatkamalli, jota käytetään uusien vuokrakonttien kohdalla. Tavallisesti valitset matkamallin, joka sisältää vuokrakustannukset. |
| Siirto | Jos toimituksen liiallinen tai liian vähäinen määrä on määritetyssä toleranssissa, siirtokirjauskansio käsitellään automaattisesti. Valitse oletusarvoinen käytettävä siirtokirjauskansio. Valitun siirtokirjauskansion nimen **Vastatili**-kentällä on oltava arvo. |
| Tapahtumien siirto | Kun alitoimitus käsitellään, lyhytvastaanottomäärä siirretään alitoimitusvarastoon. Valitse oletusarvoinen käytettävä siirron kirjauskansio. |
| Poista käytöstä muut kuin matkojen ostotilaukset | Poista Aiheutuneen kustannuksen yli-/alitoimitustoiminto käytöstä ostotilauksissa, jotka eivät ole liitettyjä merikuljetukseen. |
| Poista käytöstä muiden kuin matkalla olevien tavaroiden ostotilaukset | Poista Aiheutuneen kustannuksen yli-/alitoimitustoiminto käytöstä ostotilauksissa, jotka eivät käytä kuljetettavien tuotteiden toimintoa. |
| Matkalla olevien tavaroiden ylivastaanotto lisäajan aikana | Määritä, kuinka monta päivää kuljetuskontin ensimmäisestä vastaanotosta kyseisen kuljetuskontin kohdalla voidaan vielä suorittaa ylimääräisiä ylikuittauksia. |

## <a name="status-updates-tab"></a>Tilapäivitykset-välilehti

Järjestelmä käyttää tila-arvoja kunkin merikuljetuksen tilan ilmaisemiseksi. Merikuljetuksen tila-arvoja voidaan automaattisesti soveltaa merikuljetuksiin merikuljetuksen jäljityksen tai kausittaisten erätöiden kautta. Vaihtoehtoisesti voit ottaa ne käyttöön manuaalisesti avaamalla merikuljetuksen ja valitsemalla sen jälkeen tilan toimintoruudun **Merikuljetuksen päivitys** -ryhmässä **Hallinta**-välilehdessä. 

Voit luoda tarvittavan määrän merikuljetuksen tila-arvoja. Neljä niistä on kuitenkin määritettävä erityistarkoituksessa käytettäväksi **Tilapäivitykset**-välilehdessä **Aiheutuneen kustannuksen parametrit** -sivulla. Seuraavassa taulukossa näkyvät siellä valittavina olevat kentät.

| Asetus | kuvaus |
|---|---|
| Kustannuslaskenta suoritettu | Valitse merikuljetuksen tila, joka ilmaisee, että merikuljetus on viimeistelty. |
| Kuljetuksessa | Valitse merikuljetuksen tila, joka ilmaisee, että merikuljetus on kuljetuksessa. |
| Valmis kustannuslaskentaan | Valitse merikuljetuksen tila, joka ilmaisee, että merikuljetus on valmiina kustannuslaskentaan. Tätä tilaa käytetään, kun kaikki varasto-ostolaskut ja merikuljetuksen kustannuslaskut, joiden **Merikuljetuksen kustannuksen saldo** -kentän arvona on *Toimittaja*, on käsitelty merikuljetusta varten. Jos merikuljetuksen kustannuslaskentaprosessi epäonnistuu, sen tilaksi tulee *Valmiina kustannuslaskentaan*.|
| Kustannukset esilaskettu | Valitse merikuljetuksen tila, joka ilmaisee, että merikuljetusta valmistellaan kustannuslaskentaa varten. Tätä tilaa käytetään, kun uusi kustannustapahtuma lisätään merikuljetukseen sen jälkeen, kun kustannuslaskenta on suoritettu. Uusia kustannustapahtumia voidaan lisätä aiemmin kustannuslaskettuun merikuljetukseen, kun vastaanotetaan toinen rahtilasku tai odottamaton seisokkiveloitus. Tämä tila otetaan automaattisesti käyttöön, kun kustannuslaskettuun merikuljetukseen lisätään uusi merikuljetuksen kustannus. |

## <a name="voyage-creator-tab"></a>Merikuljetuksen luoja -välilehti

Seuraavassa taulukossa kuvaillaan **Aiheutuneen kustannuksen parametrit** -sivun **Merikuljetuksen luoja** -välilehden osiot.

| Osa | kuvaus |
|---|---|
| Liikkumarajat | **Tilavuustoleranssin ulkopuolella**- ja **Painotoleranssin ulkopuolella** -kentät määrittävät raja-arvot, joiden yläpuolella olevia tuotteita pidetään liian suurina tilavuudeltaan ja painoltaan. Jos käyttäjä lisää tuotteita **Matkaeditori**-sivulle, järjestelmä näyttää varoituksen, jos tilavuus tai paino ylittää tässä määrittämäsi arvon. Kunkin kentän arvo ilmaistaan asianmukaiselle kuljetuskonttityypille määritettynä enimmäistilavuuden tai -painon prosenttiosuutena. On suositeltavaa, että arvo on 5–10 prosenttia enimmäistilavuudesta tai -painosta. |
| Laskun luonnin asetukset | Järjestelmä voi luoda useita eri pakkauksia merikuljetuksen luontiprosessin aikana. Tämän osion avulla voit määrittää, milloin luodaan uusi pakkaus. Järjestelmä tarkistaa jokaisen tämän osan rivin kohdalla määritetyn taulukon ja kentän ja luo jokaiselle yksilöivälle kentän arvolle pakkauksen. |

## <a name="cost-estimates-tab"></a>Kustannusarviot-välilehti

**Kustannusarviot**-välilehdessä **Aiheutuneen kustannuksen parametrit** -sivulla on vain yksi kenttä: **Oletuskustannuslaskennan versio**. Tätä kenttää käytetään vain, jos kustannuslaskentamenetelmä on *Vakiokustannuslaskelma*. Valitse oletuskustannuslaskelman versio, joka käytetään kausittaiselle *Nimikkeen kustannushinnan päivitys* -tehtävälle. Tätä asetusta on ehkä muutettava aina, kun uusi tilikausi alkaa.

## <a name="inventory-dimensions-tab"></a>Varastodimensiot-välilehti

**Aiheutuneen kustannuksen parametrit** -sivun **Varastodimensiot**-välilehdessä voit määrittää, mitkä käytettävissä olevat varastodimensiot näytetään oletusarvon mukaan kullakin Aiheutunut kustannus -sivulla, joilla dimensioita käytetään.

Valitse dimensio ja määritä sen jälkeen **Merikuljetuksen rivit**-, **Kuljetettavat tuotteet**- ja/tai **Kustannusarviot**-kohtien arvoksi *Kyllä* kullakin sivulla, jolla dimensio pitäisi näyttää oletusarvoisesti. Toista tämä vaihe tarvittaessa muille dimensioille.

Tämän välilehden asetukset määrittävät kunkin yrityksille määritetyn sivun oletusdimensiot. Määritetyllä sivulla työskentelevät käyttäjät voivat kuitenkin ohittaa oletusdimensiot valitsemalla toimintoruudusta **Varasto \> Näytä dimensiot**.

## <a name="number-sequences-tab"></a>Numerosarjat-välilehti

**Aiheutuneen kustannuksen parametrit** -sivun **Numerosarjat**-välilehdessä näkyvät kaikki viitenumerosarjatyypit, joita aiheutunut kustannus edellyttää, mutta joita ei jaeta yrityksille. Valitse kullekin luettelon viitteelle numerosarjan koodi.

> [!NOTE]
> Moniyrityskonfiguraatiossa kullekin yritykselle on luotava eri numerosarjat.

## <a name="shared-number-sequences-tab"></a>Jaetut numerosarjat -välilehti

**Aiheutuneen kustannuksen parametrit** -sivun **Jaetut numerosarjat**-välilehdessä näkyvät kaikki viitenumerosarjatyypit, jotka on jaettu yrityksille aiheutuneen kustannuksen kohdalla. Luettelossa on tällä hetkellä vain yksi numerosarja. Tätä numerosarjaa käytetään merikuljetuksen tunnuksessa.

**Kaikki merikuljetukset** -sivulla käyttäjät voivat tarkastella kaikkia merikuljetuksia kaikissa yrityksissä. Käyttäjien on kuitenkin oltava valitun tietueen yrityksessä, jotta he voivat muokata ja käsitellä merikuljetusta.

## <a name="feature-visibility-tab"></a>Ominaisuuden näkyvyys -välilehti

Aiheutunut kustannus lisää ominaisuuksia (kenttiä ja toimintoja) useisiin usein käytettyihin Microsoft Dynamics 365 Supply Chain Managementin sivuihin. Nämä sivut sisältävät toimittajan päätietoihin, vapautettuihin tuotteisiin, ostotilauksiin, siirtotilauksiin ja varaston asetuksiin liittyviä sivuja. Jos käytät aiheutunutta kustannusta, nämä toiminnot on laitettava näkyville kaikkialla, ennen kuin niistä voi olla hyötyä. Jos et käytä aiheutunutta kustannusta, voit piilottaa ominaisuudet ja näin pitää ne poissa tieltä.

Määritä **Aiheutuneen kustannuksen parametrit** -sivun **Ominaisuuden näkyvyys** -välilehdessä **Aktivoi**-asetuksen arvoksi *Kyllä*, jos haluat, että aiheutuneen kustannuksen ominaisuudet ovat näkyvissä aina, kun ne ovat käytettävissä. Määritä arvoksi *Ei*, jos haluat piilottaa ominaisuuden yhteisillä sivuilla aiheutuneen kustannuksen ulkopuolella. Kuitenkin vaikka asetuksena olisi *Ei*, itse moduuli, mukaan lukien **Aiheutuneen kustannuksen parametrit** -sivu, on kuitenkin niiden käyttäjien käytettävissä, joilla on tarvittavat käyttöoikeudet.
