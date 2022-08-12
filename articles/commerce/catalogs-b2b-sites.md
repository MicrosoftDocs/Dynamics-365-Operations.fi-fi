---
title: Commerce-luetteloiden luominen yritysten välisille sivustoille
description: Tässä artikkelissa kuvataan, kuinka luodaan Commerce-luetteloita Microsoft Dynamics 365 Commercen B2B-sivustoille.
author: ashishmsft
ms.date: 07/11/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2022-02-28
ms.openlocfilehash: 7d4ed3e2a76924c2c3c0ba55e21ba648e8da7b76
ms.sourcegitcommit: d1491362421bf2fcf72a81dc2dc2d13d3b98122b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/11/2022
ms.locfileid: "9136823"
---
# <a name="create-commerce-catalogs-for-b2b-sites"></a>Commerce-luetteloiden luominen yritysten välisille sivustoille

[!include [banner](includes/banner.md)]

Tässä artikkelissa kuvataan, kuinka luodaan Commerce-tuoteluetteloita Microsoft Dynamics 365 Commercen B2B-sivustoille. Vastaukset usein kysytyihin kysymyksiin B2B-sivustojen Commerce-luetteloista on kohdassa [Usein kysytyt kysymykset B2B-sivustojen Commerce-luetteloista](catalogs-b2b-sites-FAQ.md).

> [!NOTE]
> Tämä artikkeli koskee Dynamics 365 Commercen versiota 10.0.27 ja sitä uudempia versioita.

Voit käyttää Commerce-esitteitä tunnistaaksesi tuotteet, joita haluat tarjota B2B-verkkokaupoissasi. Kun luot luettelon, määrität online-myymälät, joissa tuotteita tarjotaan, lisäät sisällytettävät tuotteet ja parannat tuotetarjoomaa lisäämällä myynninedistämistietoja. Kullekin yritystenväliselle verkkokaupalle voi luoda useita luetteloita kuten seuraavassa kuvassa.

![Commerce-tuoteluetteloiden esikatselu](./media/Commerce_Catalogs.png)

Commerce-tuoteluetteloiden avulla voit määrittää seuraavat tiedot:

- **Luettelotyyppi** – Määritä arvoksi **Yritystenvälinen**. Yritystenvälisen luetteloon voidaan määrittää ominaisuuksia, kuten siirtymishierarkian, asiakashierarkian ja luettelon määritteen metatiedot. 
- **Luettelokohtainen siirtymishierarkia** – Organisaatiot voivat luoda erillisen luokkarakenteen omaa luetteloaan varten.
- **Luettelokohtaiset määritemetatiedot** – Määritteet sisältävät tietoja tuotteesta. Kun liität määritteitä siirtymishierarkian luokkaan, voit määrittää määritteiden arvot tähän luokkaan liitettyjen tuotteiden tasolla. Organisaatiot voivat sitten suorittaa seuraavat tehtävät:

    - Määrittää luettelokohtaiset määritearvot.
    - Hallita määritteiden näkyvyyttä luettelotasolla.
    - Valita yksittäiseen luetteloon liittyvät tarkentajat.

- **Kanavat** – Organisaatiot voivat liittää luetteloon useita B2B-verkkokanavia. Luetteloiden alusta loppuun -tuki on tällä hetkellä käytettävissä vain B2B-verkkokaupoissa.
- **Asiakashierarkiat** – Kun tietty B2B-kanava on käytössä, organisaatiot voivat määrittää tietyn luettelon valittujen B2B-yhteistyökumppanien käyttöön liittämällä asiakashierarkiat luetteloon.
- **Hintaryhmät** – Voit määrittää tiettyyn luetteloon liittyvät hinnat ja kampanjat. Tämä ominaisuus on olennaista sille, että luettelo määritetään B2B-kanavaa varten. Luetteloiden hintaryhmien avulla organisaatiot voivat antaa tuotteita tiettyjen B2B-organisaatioiden käyttöön ja käyttää ensisijaista hinnoitteluaan ja alennuksiaan. B2B-asiakkaat, jotka tilaavat konfiguroidusta luettelosta, voivat saada erityishintoja ja tarjouksia, kun he kirjautuvat Commerce B2B -sivustoon. Voit määrittää luettelokohtaiset hinnat valitsemalla **Hintaryhmät**-asetuksen **Luettelot**-välilehdessä linkittääksesi yhden tai useamman hintaryhmän luetteloon. Kaikki kauppasopimukset, hinnanoikaisun kirjauskansiot ja lisäalennukset, jotka on linkitetty samaan hintaryhmään otetaan käyttöön, kun asiakkaat tilaavat kyseisestä luettelosta. (Lisäalennuksiin kuuluvat raja- ja määräalennukset sekä yhdistelmäalennukset.) Lisätietoja hintaryhmistä on kohdassa [Hintaryhmät](price-management.md#price-groups).

> [!NOTE]
> Tämä ominaisuus on saatavana Dynamics 365 Commercen versiosta 10.0.27 alkaen. Luettelokohtaiset määritykset, kuten siirtymishierarkia ja asiakashierarkia, voidaan määrittää siirtymällä Commerce headquartersissa **Ominaisuudenhallinta** -työtilaan (**Järjestelmän hallinta \>Työtilat \> Ominaisuuksien hallinta**), ottamalla käyttöön **Ota käyttöön usean luettelon käyttö vähittäismyyntikanavissa** -ominaisuuden ja suorittamalla sitten **1110 CDX** -työn. Kun tämä ominaisuus otetaan käyttöön, kaikkiin aiemmin luotuihin luetteloihin, joita käytetään myymälöiden myyntipisteissä tai puhelinkeskuksissa, lisätään **Luettelot**-sivulla merkintä **Luettelotyyppi = Yritystenvälinen**. Vain ne aiemmin luodut tai uudet luettelot, joissa on merkintä **Luettelotyyppi = Yritystenvälinen**, ovat käytettävissä myymälöiden myyntipisteissä ja puhelinkeskuksessa. 

## <a name="b2b-catalog-process-flow"></a>Yritystenvälisen luettelon prosessityönkulku

Luettelon luonti- ja käsittelyprosessi sisältää neljä yleistä vaihetta. Jokainen vaihe on selitetty seuraavassa osassa yksityiskohtaisemmin.

> [!NOTE]
> Ennen jatkamista on varmistettava, että luettelossa on merkintä **Luettelotyyppi = Yritystenvälinen**.

1. **[Konfiguraatio](#configure-the-catalog)**

    - Liitä siirtymishierarkia.
    - Määritä voimassaolo- ja vanhentumispäivämäärät, jos niitä käytetään.
    - Lisää ja luokittele tuotteet.
    - Liitä hintaryhmät.
    - Liitä B2B-organisaatioillesi erityinen asiakashierarkia. 
    - Liitä oletusdimensiomääritteen ryhmä tarkentajille, kuten koko, tyyli ja väri.
    - Määritä määritteen metatiedot.

1. **[Tarkistus](#validate-the-catalog)** – Tässä vaiheessa suoritetaan oikeellisuustarkistussäännöt, jotka valvovat tiettyä toimintatapaa. Seuraavassa on muutamia esimerkkejä:

    - Varmista, ettei luokittelemattomia tuotteita ole.
    - Varmista, että kaikki kuhunkin kanavaan liitetyt nimikkeet on liitetty luetteloon.

1. **[Hyväksyminen](#approve-the-catalog)**
1. **[Julkaistaan](#publish-the-catalog)**

## <a name="set-up-the-catalog"></a>Luettelon määrittäminen

Tämän osan tietojen avulla voit määrittää luettelon.

### <a name="configure-the-catalog"></a>Luettelon määrittäminen

Siirry Commerce headquarters -sovelluksessa kohtaan **Retail ja Commerce \> Luettelot ja valikoimat \> Kaikki luettelot** määrittääksesi luettelon.

Kun uusi luettelo luodaan, luettelo on liitettävä vähintään yhteen kanavaan. Vain sellaisia nimikkeitä voi käyttää luetteloa luodessa, jotka on linkitetty valitun kanavan [valikoimiin](/dynamics365/unified-operations/retail/assortments). Voit liittää luettelon yhteen tai useaan kanaviaan valitsemalla **Luettelon asetukset** -sivun **Commerce-kanavat**-pikavälilehdessä **Lisää**. Varmista, että luettelossa on merkintä **Luettelotyyppi = Yritystenvälinen**.

#### <a name="associate-the-navigation-hierarchy"></a>Liitä siirtymishierarkia

Lisää luetteloon tuotteita valitsemalla ensin siirtymishierarkia. Siirtymishierarkia tukee luettelon luokitusrakennetta. Valitse yksi siirtymishierarkia, joka on liitetty **Commerce-kanavat**-pikavälilehdessä **Luettelon asetukset**-sivulla valittuihin kanaviin. Jos haluat liittää kuhunkin kanavaan oletussiirtymishierarkian, siirry kohtaan **Retail ja Commerce \> Kanavan asetukset \> Kanavaluokat ja tuotemääritteet**.

#### <a name="specify-time-effective-and-expiration-dates"></a>Määritä voimaantulo- ja vanhentumispäivämäärät

Voit määrittää luettelon voimassaolo- ja vanhentumispäivämäärät valitsemalla luettelon hierarkian ylimmän solmun palataksesi pääluettelon otsikkonäkymään. Määritä voimassaolo- ja vanhentumispäivämäärät tarpeen mukaan **Yleiset**-pikavälilehdessä.

#### <a name="add-and-categorize-products"></a>Lisää ja luokittele tuotteet

Siirry Commerce headquarters -sovelluksessa kohtaan **Retail ja Commerce \> Luettelot ja valikoimat \> Kaikki luettelot** määrittääksesi luetteloon lisättävät tuotteet. Valitse sitten **Luettelot**-välilehdessä **Lisää tuotteet**.

Vaihtoehtoisesti voit valita solmun siirtymishierarkiasta. Tämän jälkeen voit lisätä tuotteita suoraan luettelon luokkaan.

#### <a name="associate-price-groups"></a>Liitä hintaryhmät

Siirry Commerce headquarters -sovelluksessa kohtaan **Retail ja Commerce \> Luettelot ja valikoimat \> Kaikki luettelot** määrittääksesi luetteloon lisättävät tuotteet. Valitse sitten **Luettelot**-välilehdessä **Lisää tuotteet**. 

Tuotteet, jotka lisättiin luetteloon siirtymishierarkian juurisolmusta valitsemalla toimintoruudussa **Lisää tuotteita**, perivät luokat, jos myös lähteen siirtymishierarkia on liitetty luetteloon. Lähteen siirtymishierarkian luokkiin tehdyt muutokset siirtyvät heti luetteloihin. Kanavat päivitetään julkaisemalla luettelot uudelleen.

Vaihtoehtoisesti siirtymishierarkiassa voidaan valita solmu ja lisätä tuotteet suoraan valittuun luettelon luokkaan. 

Kun tuotteita lisätään **Sisällytä kaikki variantit automaattisesti vain, kun päätuote on valittuna** -vaihtoehto on käytettävissä. Kaikkien varianttien sisällyttäminen voidaan estää valitsemalla ainakin yksi päätuotteen variantti. 

> [!NOTE]
> Jos valitaan kaikkien varianttien automaattinen sisällyttäminen suuressa päätuotevalikoimassa, käsittelyaika voi pidentyä. Suurissa valinnoissa on suositeltavaa valita luettelosivun toimintoruudussa **Sisällytä kaikki variantit** ja suorittaa toiminto erätilassa. Jos sisällytetään vain luettelon päätuote eikä yhtään varianttia, varianttivalitsin ei ehkä ole käytettävissä tuotetietosivulle siirryttäessä. 

Jotta luettelokohtaiset hinnat voidaan konfiguroida, vähintään yksi hintaryhmä on linkitettävä luetteloon. Siirry Commerce headquarters -sovelluksessa kohtaan **Retail ja Commerce \> Luettelot ja valikoimat \> Kaikki luettelot** liittääksesi hintaryhmät luetteloon. Valitse sitten **Hintaryhmät** **Luettelot**-välilehden **Hinnoittelu**-kohdasta. Kaikki kauppasopimukset, hinnanoikaisun kirjauskansiot ja lisäalennukset (raja- ja määräalennus sekä yhdistelmäalennus), jotka on linkitetty samaan hintaryhmään otetaan käyttöön, kun asiakkaat tilaavat kyseisestä luettelosta.

Lisätietoa hintaryhmistä on kohdassa [Hintaryhmät](price-management.md#price-groups).

> [!NOTE]
> Et voi luoda uutta hintaryhmää **Kaikki luettelot** -sivulla. Se on sen sijaan luotava **Kaikki hintaryhmät** -sivulla. Se on sitten liitettävä luetteloon **Kaikki luettelot** -sivulla.

#### <a name="associate-a-customer-hierarchy"></a>Liitä asiakashierarkia

Siirry Commerce headquarters -sovelluksessa kohtaan **Retail ja Commerce \> Luettelot ja valikoimat \> Kaikki luettelot** liittääksesi asiakashierarkiat. Tämän jälkeen voit linkittää yhden tai useita asiakashierarkioita luetteloon valitsemalla **Luettelot**-välilehden **Asiakashierarkia**-kohdasta **Liitä hierarkiat**.

> [!NOTE]
> Et voi luoda uutta asiakashierarkiaa **Kaikki luettelot** -sivulla. Se on sen sijaan luotava **Asiakashierarkiat** -sivulla. Se on sitten liitettävä luetteloon **Kaikki luettelot** -sivulla.

#### <a name="associate-default-dimension-attribute-group-for-refiners-such-as-size-style-and-color"></a>Liitä oletusdimensiomääritteen ryhmä tarkentajille, kuten koko, tyyli ja väri

Voit liittää dimension oletusmääritteen ryhmän tarkentajiin, kuten koko-, tyyli- ja väriominaisuuksiin, siirtymällä Commerce Headquarters -sovelluksessa kohtaan **Retail ja Commerce \> Luettelot ja valikoimat \> Kaikki luettelot**. Valitse sitten **Määriteryhmät** **Luettelot**-välilehden **Määritteet**-kohdasta.

#### <a name="set-attribute-metadata"></a>Määritä määritteen metatiedot

Siirry Commerce headquarters -sovelluksessa kohtaan **Retail ja Commerce \> Luettelot ja valikoimat \> Kaikki luettelot** määrittääksesi määritteiden metatiedot. Valitse sitten **Määritä määritteen metatiedot** **Luettelot**-välilehden **Määritteet**-kohdasta. Voit valita määritteet, joita voidaan tarkastella ja tarkentaa valitsemalla luokan liittyvästä luettelokohtaista siirtymishierarkiasta ja valitsemalla sitten määritteen **Luettelon tuotemääritteet** -kohdasta. Valitse sitten **Näytä määrite kanavassa**. Oletusarvon mukaan myös kaikkia näytettäviä määritteitä voi myös hakea. Voit halutessasi määrittää määritteet tarkennettaviksi valitsemalla **Voidaan tarkentaa**.

### <a name="validate-the-catalog"></a>Luettelon vahvistaminen

Ennen kuin uusi luettelo on käytettävissä, se on vahvistettava ja julkaistava.

Vahvista luettelo seuraavien ohjeiden avulla.

1. Suorita oikeellisuustarkistus valitsemalla **Vahvista luettelo** **Kaikki luettelot** -sivun **Luettelot**-välilehden **Vahvista**-kohdasta. Tämä vaihe on pakollinen. Se tarkistaa, että pakolliset määritykset ovat tarkkoja.
1. Näet tarkistuksen tulokset valitsemalla **Näytä tulokset**. Jos löytyy virheitä, korjaa tiedot ja suorita oikeellisuustarkistus uudelleen kunnes oikeellisuustarkistus on läpäisty.

> [!NOTE]
> Jos kyseessä **Luettelotyyppi = Yritystenvälinen**, tarkistus epäonnistuu, myymälöiden myyntipisteet tai puhelinkeskus lisättiin luetteloon. Yritystenvälisiin luetteloihin on oltava liitettyinä vain yritystenvälisiä verkkokanavia. Tarkistus epäonnistuu myös silloin, jos yritystenväliseen luetteloon ei ole liitetty yhtään asiakashierarkiaa. 

### <a name="approve-the-catalog"></a>Hyväksy luettelo

Kun luettelo on vahvistettu, se pitää hyväksyä.

Aloita luettelon hyväksyntätyönkulku näiden ohjeiden avulla.

1. Valitse **Kaikki luettelot** -sivun toimintoruudussa **Työnkulku \> Lähetä**.
1. Määritä työnkulun valtuutetut käyttäjät ja vaiheet kohdassa **Retail ja Commerce \> Pääkonttorin asetukset \> Commercen työnkulut**. Työnkulku määrittää vaiheet, jotka tarvitaan saamaan luettelo tilaan **Hyväksytty**.

### <a name="publish-the-catalog"></a>Julkaise luettelo

Kun luettelon tila on **Hyväksytty**, voit julkaista sen valitsemalla **Luettelot**-valikosta **Julkaise**. Kun luettelo on **Julkaistu**-tilassa, sitä voidaan käyttää puhelinkeskuksen tilaustenkäsittelyn ja luettelon lähettämisen prosesseissa. Voit julkaista luettelon manuaalisesti tai käyttämällä eräkäsittelyä. Luettelolle määrittämäsi voimaantulopäivä määrittää, milloin tuotteet ovat saatavilla online-myymälässä. Määrittämäsi vanhenemispäivämäärä määrää, milloin tuotteet poistetaan online-myymälästä.

> [!NOTE]
> Voit julkaista luettelon, joka sisältää varoituksia sisältävät tuotteet. Kyseiset tuotteet eivät kuitenkaan näy online-myymälässä.

## <a name="additional-resources"></a>Lisäresurssit

[Commerce-luetteloiden laajennettavuusvaikutus B2B-mukautuksia varten](catalogs-b2b-sites-dev.md)

[Usein kysytyt kysymykset B2B-sivustojen Commerce-luetteloista](catalogs-b2b-sites-FAQ.md)

[Luettelon valitsinmoduuli](catalog-picker.md)
