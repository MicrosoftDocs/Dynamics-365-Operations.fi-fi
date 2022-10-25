---
title: Kustannusseurannan työtila
description: Tässä artikkelissa on tietoja kustannusseurannan työtilasta. Esimiehet voivat avata työtilassa keskitetysti vastuullaan olevia yhden tai kaikkien dimensioiden kustannusobjekteja tai kustannusobjektijoukkoja koskevia raportteja.
author: AndersGirke
ms.date: 06/16/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CAMCostControlWorkspaceConfiguration, CAMCostControlWorkspace, CAMCostControlWorkspaceConfigurationPerUser
audience: Application User
ms.reviewer: twheeloc
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: twheeloc
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 8d5ded4b08d562fff9ec5fd9a3de591f944e3ee0
ms.sourcegitcommit: dca54dd3afc7c94795d89c63050b105df2c48e3f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/15/2022
ms.locfileid: "9682895"
---
# <a name="cost-control-workspace"></a>Kustannusseurannan työtila 

[!include [banner](../includes/banner.md)]

Esimiehet voivat avata **Kustannusseuranta**-työtilassa keskitetysti vastuullaan olevia yhden tai kaikkien dimensioiden (kuten kustannuspaikkojen ja tuoteryhmien) kustannusobjekteja tai kustannusobjektijoukkoja koskevia raportteja. Työtilan raportit ovat täysin kustannuslaskijoiden hallinnassa, joten raportoinnissa käytettävä asettelu ja tiedot ovat yhtenäiset koko organisaatiossa.

## <a name="cost-control-workspace-configuration"></a>Kustannusseurannan työtilan konfiguraatio

Kustannuslaskijat voivat määrittää tarvitsemansa määrän raporttimäärityksiä haluamallaan tietojen kokoonpanolla tai asettelulla. Raportin määritys koostuu kuudesta osasta, joista jokainen vaikuttaa joko kohdennettujen tietojen kokoonpanon tai asettelun valintaan.

Määritä kustannusseurannan työtila valitsemalla **Kustannusseuranta** \> **Asetukset** \> **Kustannusseurannan työtilan konfiguraatio**.

### <a name="general"></a>Yleiset

Voit luoda yksilöllisen raporttiasettelun **Yleiset**-pikavälilehdessä. Raportin nimi on yksilöllinen tunniste, jonka käyttäjät tunnistavat **Kustannusseuranta**-työtilassa. Voit määrittää, jaetaanko raportti vai onko se tarkoitettu vain kustannuslaskijoiden sisäiseen käyttöön.

| Kenttä       | kuvaus |
|-------------|-------------|
| Nimi        | Anna asettelulle yksilöllinen nimi. |
| kuvaus | Kirjoita tarkka kuvaus. |
| Julkaistu   | Jos valitset tässä kentässä **Kyllä**, käyttäjä, jolle on määritetty jokin seuraavista rooleista, näkee raportin **Kustannuslaskenta**-työtilassa:<ul><li>Kustannuslaskennan hallinta</li><li>Kustannuslaskija</li><li>Kustannuslaskijan apulainen</li><li>Kustannusobjektin vastuuhenkilö</li></ul>Jos valitset tässä kentässä **Ei**, vain käyttäjät, joille on määritetty jokin seuraavista rooleista, näkee raportin **Kustannuslaskenta**-työtilassa:<ul><li>Kustannuslaskennan hallinta</li><li>Kustannuslaskija</li><li>Kustannuslaskijan apulainen</li></ul> |

### <a name="data-filtering"></a>Tietojen suodatus

Määritä raportin tietoperusta **Tietojen suodatus** -pikavälilehdessä. Tämän raportin käyttäjät näkevät arvot raportissa sen jälkeen, kun lähdetiedot on käsitelty.

| Kenttä                                                             | kuvaus |
|-------------------------------------------------------------------|-------------|
| Kustannuslaskennan kirjanpito                                            | **Kustannuslaskennan kirjanpito**, johon raportti perustuu. Arvo on peräisin **Kustannusseurantayksikkö**-kentästä. |
| Kustannusseurantayksikkö                                                 | Valitsemasi arvo määrittää kustannuslaskennan kirjanpidon ja kustannusobjektit, joihin tämä raportti perustuu. |
| Tilastodimension hierarkia, kustannustason dimensiohierarkia | **Kustannusseuranta**-työtilan määritystietue voi ilmoitta joko ei-rahallisen tai rahallisen arvon, mutta molempia ei voi käyttää samassa asettelussa. Raportoi rahalliset arvot valitsemalla arvo **Kustannustason dimensiohierarkia** -kentässä. Raportoi ei-rahalliset arvot valitsemalla arvo **Tilastodimension hierarkia** -kentässä. Valitsemasi dimensiohierarkian tietue määrittää raportointi- ja koostetasojen rakenteen.<blockquote>**HUOMAUTUS:**<br>Voit tarkastella ei-rahallisia ja rahallisia arvoja rinnakkain viemällä tiedot Microsoft Excelin Microsoft Power BI -sisältöön.</blockquote> |
| Kustannusobjektin dimensiohierarkia      | Valitse määrittämäsi raportoinnin tarkoitusta vastaava kustannusobjektin dimensiohierarkia. |
| Budjetin alkuperäinen versio                                           | Valitse budjetin versiotunnus, joka on tämän raportin alkuperäinen budjetti. |
| Budjetin uusi versio                                            | Valitse budjetin versiotunnus, joka on tämän raportin muutettu budjetti. |

### <a name="assign-calculation-records"></a>Määritä laskentatietueet

Yleiskustannuslaskenta suorittaa lähdetiedoissa useita laskentatoimintoja, kustannustoiminnan luokittelu, kustannusten jakelu tai kustannusten kohdistus. Samalle tilikaudelle voidaan tehdä useita yleiskustannuslaskentoja, jos havaitaan puuttuvia tietolähteitä tai sääntöjä on päivitettävä. Jokainen yleiskustannuslaskenta tallennetaan yksilöllisellä tunnuksella. Kustannuslaskija voi valita tietyn yleiskustannuslaskennan tunnuksen. Raportin käyttäjät, kuten esimiehet, näkevät yleiskustannuslaskennan tulokset **Kustannusseuranta**-työtilassa.

| Kenttä                  | kuvaus |
|------------------------|-------------|
| Kirjanpidon vuosikalenterin kausi | Valitse kirjanpidon vuosikalenterin jakso, johon yleiskustannuslaskennan tunnus määritetään.<blockquote>**HUOMAUTUS:**<br>Kentässä mainitut tilikaudet ovat peräisin kustannuslaskennan kirjanpitoon liitetystä kirjanpidon vuosikalenterista.</blockquote> |
| Todellinen versio         | Valitse sopiva yleiskustannuslaskennan tunnus. |
| Budjettiversio         | Valitse sopiva yleiskustannuslaskennan tunnus. |
| Uusi budjettiversio | Valitse sopiva yleiskustannuslaskennan tunnus. |

### <a name="fiscal-periods-per-column"></a>Tilikausia sarakkeessa

Kustannuslaskija päättää **Tilikausia sarakkeessa** -pikavälilehdessä, mitä tilikausi näytetään raporttiasettelussa.

Valittujen sarakkeiden arvoit kerrotaan **Tilikausia sarakkeessa** -pikavälilehdessä valituilla arvoilla.

| Kenttä                | kuvaus |
|----------------------|-------------|
| Kuluva kausi       | Nykyisen tilikauden saldo näytetään.<blockquote>**HUOMAUTUS:**<br>Nykyinen tilikausi määritetään oletusarvoisesti istunnon päivämäärän mukaan. **Kustannusseuranta**-työtilassa voi valita tietyn tilikauden. Valittu arvo edustaa sitten nykyistä kautta.</blockquote> |
| Edellinen jakso      | Edellisen tilikauden saldo näytetään. Seuraavaa kaavaa käytetään:<br>Nykyinen tilikausi – 1<blockquote>**HUOMAUTUS:**<br>Edellinen tilikausi johdetaan oletusarvoisesti istunnon päivämäärästä. Tietty tilikausi voidaan valita **Kustannusseuranta**-työtilassa nykyiseksi kaudeksi. **Edellinen kausi** lasketaan sitten siitä uudelleen.</blockquote> |
| Vuoden alusta         | Vuoden alusta on näkyvissä. Seuraavaa kaavaa käytetään:<br>YearToDate (nykyinen tilikausi)<blockquote>**HUOMAUTUS:**<br>Nykyinen tilikausi määritetään oletusarvoisesti istunnon päivämäärän mukaan. **Kustannusseuranta**-työtilassa voi valita tietyn tilikauden. Valittu arvo vastaa sitten nykyistä kautta ja **Vuoden alusta** -arvo päivitetään vastaavasti.</blockquote> |
| Keskiarvo vuoden alusta | Keskiarvo vuoden alusta on näkyvissä. Seuraavaa kaavaa käytetään:<br>(YearToDate [nykyinen tilikausi]) ÷ (Count [nykyinen tilikausi])<p><strong>Esimerkki</strong></p><ul><li>**Tilastodimension jäsen:** kokoaikaiset työntekijät</li><li>**Kuluva päivämäärä:** 21.3.2017</li><li>**Kausi:** tilikausi 1, tilikausi 2, tilikausi 3</li><li>**Suuruus:** 10, 10, 12</li></ul>Tässä tapauksessa **Keskiarvo vuoden alusta** = (10 + 10 + 12) ÷ 3 = 10,67<p>**Keskiarvo vuoden alusta** -arvo voidaan laskea kustannustason dimension jäsenille ja tilastodimension jäsenille.</p><blockquote>**HUOMAUTUS:**<br>Nykyinen tilikausi määritetään oletusarvoisesti istunnon päivämäärän mukaan. **Kustannusseuranta**-työtilassa voi valita tietyn tilikauden. Valittu arvo vastaa sitten nykyistä kautta. Lisäksi **Vuoden alusta**- ja **Keskiarvo vuoden alusta** -arvot päivitetään vastaavasti.</blockquote> |

### <a name="columns-to-display-for-costs"></a>Kustannusten näytettävät sarakkeet

Kustannuslaskija päättää **Kustannusten näytettävät sarakkeet** -pikavälilehdessä, mitä sarakkeita raportin asettelussa käytetään. Käytössä on kolme luokkaa: kiinteä kustannus, muuttuva kulu ja luokittelemattomat kulut.

| Kenttä                 | kuvaus |
|-----------------------|-------------|
| Kiinteä kustannus            | Tämä saraketyyppi näyttää kiinteän kustannuksen valitun yleiskustannuslaskennan tunnuksen perusteella.<blockquote>**HUOMAUTUS:**<br>Tämä saraketyyppi näyttää saldon vain silloin, kun tilikaudelle on valittu yleiskustannuslaskennan tunnus.</blockquote> |
| Muuttuva kulu         | Tämä saraketyyppi näyttää muuttuvan kulun valitun yleiskustannuslaskennan tunnuksen perusteella.<blockquote>**HUOMAUTUS:**<br>Tämä saraketyyppi näyttää saldon vain silloin, kun tilikaudelle on valittu yleiskustannuslaskennan tunnus.</blockquote> |
| Kiinteä + muuttuva kustannus | Tämä saraketyyppi näyttää kiinteän kustannuksen ja muuttuvan kulun valitun yleiskustannuslaskennan tunnuksen perusteella.<blockquote>**HUOMAUTUS:**<br>Tämä saraketyyppi näyttää saldon vain silloin, kun tilikaudelle on valittu yleiskustannuslaskennan tunnus.</blockquote> |
| Kokonaiskustannukset            | Tässä saraketyyppi näyttää kokonaiskustannukset (luokittelemattomat kulut, kiinteän kustannuksen ja muuttuvan kulun).<blockquote>**HUOMAUTUS:**<br>Saraketyyppi näyttää saldon koko ajan.</blockquote> |
| Luokittelematon kustannus     | Tämä saraketyyppi näyttää luokittelemattomat kulut.<blockquote>**HUOMAUTUS:**<br>Tällä sarakkeella voidaan tarkistaa, onko kaikki kustannukset luokiteltu oikein yleiskustannuslaskennassa tai onko kustannustoiminnan sääntöjä muutettava.</blockquote> |

### <a name="columns-to-display-for-budgeted-costs"></a>Budjetoitujen kustannusten näytettävät sarakkeet

Kustannuslaskija päättää **Budjetoitujen kustannusten näytettävät sarakkeet** -pikavälilehdessä, mitkä valittujen budjettiversioiden sarakkeet näytetään. Alkuperäinen ja muutettu budjetti voidaan valita erikseen.

> [!NOTE]
> Koska seuraavat kentät toimivat samalla tavoin alkuperäisessä ja muutetussa budjetissa, ne selitetään vain kerran.

| Kenttä                     | kuvaus |
|---------------------------|-------------|
| Budjetti                    | Budjettisaldot näytetään valittujen sarakkeiden perusteella.<blockquote>**HUOMAUTUS:**<br>Saldot perustuvat **Tietojen suodatus** -pikavälilehdessä valittuihin budjettiversioihin.</blockquote> |
| Budjetin varianssi           | Laske ja näytä budjetin ja toteutuneen välinen ero. Seuraavaa kaavaa käytetään:<br>Budjettisaldo – toteutunut saldo |
| Budjetin varianssi prosenttiosuutena      | Laske ja näytä budjetin ja toteutuneen välinen ero prosentteina. Seuraavaa kaavaa käytetään:<br>(Budjettisaldo – toteutunut saldo) ÷ budjettisaldo |
| Varianssikauden raja-arvo | Määritä nykyisen kauden rahasumman varianssin raja-arvo. Jos raja-arvo ylittyy, rivi korostetaan punaisella **Kustannusseuranta**-työtilassa.<blockquote>**HUOMAUTUS:**<br>Tämä kenttä koskee vain menoja ilmaisevia kustannustasoja.</blockquote> |
| Varianssin vuoden raja-arvo   | Määritä vuoden rahasumman varianssin raja-arvo. Jos raja-arvo ylittyy, rivi korostetaan punaisella **Kustannusseuranta**-työtilassa. |
| Varianssin raja-arvoprosentti      | Määritä varianssin raja-arvo prosentteina. Jos raja-arvo ylittyy, rivi korostetaan punaisella **Kustannusseuranta**-työtilassa.<blockquote>**HUOMAUTUS:**<br>Sama prosenttiraja-arvo koskee nykyistä kautta ja vuotta.</blockquote> |

## <a name="cost-control-workspace"></a>Kustannusseurannan työtila

**Kustannusseuranta**-työtila on suunniteltu verkkoraportiksi. Niinpä kaikille kustannusobjektista vastaaville esimiehille voidaan myöntää käyttöoikeus. Käyttöoikeuden myöntäminen käsitellään ohjeaiheessa [Kustannusobjektin vastuuhenkilöiden käyttöoikeuksien määrittäminen](access-rights-cost-object-controller.md).

Käyttäjien, kuten esimiesten, käytettävissä olevien raporttien luetteloa hallitaan valitsemalla **Kustannusseurannan työtilan konfiguraatiot** -sivulla **Julkaistu**-vaihtoehto.

![Raportti, jonka käyttäjät näkevät Kustannusseuranta-työtilassa.](./media/report-cost-control.png)

Esimies voi valita tarkasteltavan kirjanpidon vuosikalenterin. Istunnon päivämäärä määrittää oletusarvoisen nykyisen kauden.

Kirjanpidon vuosikalenterin kauden arvot määritetään raportin nimen ja sen kirjanpidon vuosikalenterin mukaan, joka on valittu **Kustannusseurannan työtilan konfiguraatiot** -sivulla raportin nimeen liitetylle kustannusseurannan kirjanpidolle.

Käyttäjät voivat valita kustannusobjektin dimensiohierarkiassa koostetason, jolla saldot näytetään. Ottamalla käyttöön käyttöoikeustason suojauksen voit hallita käyttöoikeuksia siten, että käyttäjät voivat valita vain ne hierarkiatasot, joihin heille on myönnetty käyttöoikeus. Niinpä he näkevät vain ne koostesaldot, joiden käyttöoikeudet heille on myönnetty.

### <a name="add-or-remove-columns"></a>Lisää tai poista sarakkeita

Käyttäjät voivat mukauttaa raportin sarakkeet omia tarpeitaan vastaaviksi.

### <a name="view-details"></a>Näytä tiedot

Käyttäjät voivat porautua työtilassa näkyvien saldojen taustoihin. Jos käyttäjät valitsevat kustannustason dimensiohierarkian solmun ja valitsevat sitten **Näytä tiedot**, solmun tarkat tiedot näkyvät **Kustannustason tiedot** -valintaikkunassa.

Ruudukossa näkyy kukin kustannustason dimensiohierarkian solmuun liitetty kustannustaso ja sen arvot. Ruudukossa näkyvät sarakkeet vastaavat työtilan asetuksia.

Kahdessa kaaviossa on yhteenveto toteutuneen ja budjetoidun vertailusta sekä budjetin varianssista kauden mukaan.

![Kaavioissa näkyy yhteenveto toteutuneen ja budjetoidun vertailusta sekä budjetin varianssista kauden mukaan.](./media/cost-element-details-operations.png)

Käyttäjät voivat porautua tarvittaessa merkinnän tietoihin valitsemalla **Kustannusmerkinnät**.

![Kustannusmerkinnät.](./media/cost-entries.png)

Esimerkiksi vuokra on meno, joka jaetaan kustannuspaikoille. Käyttäjän, joka haluaa tiedostaa oman kustannuspaikan vuokrakustannuksen, on porauduttava alas tarkistamaan, miten vuokra on laskettu.

Jos käyttäjät valitsevat **Kohdistusperuste** **Kustannusmerkinnät**-sivulla, valintaikkuna avautuu. Käyttäjät voivat sitten määrittää kohdistusperusteen sääntöön ja tarkastella kaudelle rekisteröityjä vastaavia tilastomittauksia.

Seuraavassa esimerkissä kohdistusperusteen tyyppi on **Kaavan kohdistusperuste** ja kaava näytetään. Kaavan määrittämät kertoimet ovat luettelossa. Ruudukossa näkyy myös kustannusobjektikohteisesti tehdyt laskelmat.

![Kustannusobjektikohtaiset laskelmat.](./media/cost-entries-allocation-base.png)

Lisäresurssit 

[Kustannusobjektin vastuuhenkilöiden käyttöoikeuksien määrittäminen](access-rights-cost-object-controller.md)




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
