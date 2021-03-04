---
title: Puhelinkeskuksen luettelot
description: Tässä ohjeaiheessa käsitellään Dynamics 365 Commercein luetteloiden puhelinkeskusta koskevia toimintoja.
author: josaw1
manager: AnnBe
ms.date: 05/15/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailMCRChannelDetailPage, RetailCatalogDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16231
ms.assetid: f28a827c-3a50-4d5e-83eb-e5a768db70a1
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 9abe493746719d2e229ef09c2eb5f436b91b2171
ms.sourcegitcommit: 4c6d31f3ebd88212d3d1497a4bba9c64c5300444
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/24/2020
ms.locfileid: "4412118"
---
# <a name="call-center-catalogs"></a>Puhelinpalvelukeskuksen luettelot

[!include [banner](includes/banner.md)]

Tässä artikkelissa käsitellään Dynamics 365 Commercein puhelinkeskusta koskevat, luettelotoimintoihin linkittyvät toiminnot.

Commercen luettelo-ominaisuuksia voidaan käyttää useita tarkoituksia varten. Alunperin luettelo-ominaisuudet luotiin tukemaan sähköisen kaupankäynnin kolmannen osapuolen integrointeja. Luettelon asetukset sallivat yritysten luoda tuotteiden ja määritteiden ryhmittelyjä, jotka voitiin julkaista ulkoisesti sähköisen kaupankäynnin kolmannen osapuolen ratkaisun käyttöön.

Kun puhelinkeskuskanavan tuki lisättiin, luettelo-ominaisuus laajennettiin lisäämään ominaisuuksia, jotka tukevat perinteisen suoraan asiakkaille suunnattujen markkinointiluetteloiden ominaisuuksia ja hallintaa. Suoraan asiakkaille -yritys usein tuottaa tulostettuja luetteloita, jotka sitten lähetetään yhdelle tai useammalle asiakassegmentille. Nämä luettelot sisältävät yleensä tiettyjä kampanjoita tai tarjouksia, jotka voi käyttää vain, jos asiakas antaa luettelon tunnuskoodin tilauksen yhteydessä.

Suoraan asiakkaille -markkinointiyritykset ovat hyvin keskittyneitä seuraamaan reaktioita näihin luetteloihin sen varmistamiseksi, että kustannukset luetteloiden tuottamiseen ja postitukseen ovat hyväksyttävät. Vastauksen seuraamiseksi koodi perinteisesti tulostetaan luettelon takaosaan ja tätä koodia on pyydetty ja käytetty, kun luettelon vastaanottaja soittaa tilatakseen puhelimitse (tai nykyään perinteisesti koodi voidaan kirjoittaa, kun asiakas tekee tilauksen verkkokaupassa). Vaikka eri toimialoilla tätä luettelon seurantakoodia kutsutaan eri nimillä (mukaan lukien avainkoodi, tarjouskoodi, luettelokoodi, lähdekoodi), kutsumme koodia Commercessa nimellä **Lähdekoodin tunnus**.

## <a name="basic-catalog-setup"></a>Luettelon perusasetukset

Määritä luettelo valitsemalla **Retail ja Commerce** \> **Luettelot ja valikoimat** \> **Kaikki luettelot**.

Kun uusi luettelo luodaan, luettelo on linkitettävä vähintään yhteen kanavaan. Tämä tehdään **Commerce-kanavat**-pikavälilehdessä **Luettelon asetukset** -lomakkeessa. Valitse **Lisää** ja valitse vähintään yksi kanava. Vain sellaisia nimikkeitä voi käyttää luetteloa luodessa, jotka on linkitetty valitun kanavan [valikoimiin](https://docs.microsoft.com/dynamics365/unified-operations/retail/assortments).

Lisää luetteloon tuotteita. Ensin on valittava siirtymishierarkia. Siirtymishierarkia tukee luettelon luokitusrakennetta. Valitse yksi kanaviin linkitetty siirtymishierarkia, joka on valittu **Commerce-kanavat**-pikavälilehdessä **Luettelo**-sivulla. Jos siirtymiskanavaa ei ole linkitetty kanavaan aiemmin, valitse **Retail ja Commerce** \> **Kanavan asetukset** \> **Kanavaluokat ja tuotemääritteet** ja linkitä oletussiirtymishierarkia kuhunkin kanavaan.

Valitse **Luettelot**-valikkovälilehdessä **Luettelon asetukset** -sivulla **Lisää tuotteita** määrittääksesi tuotteita lisätäksesi luetteloon tai valitse solmu siirtymishierarkiassa (valitsemalla solmun muuttuu näytön esitys ja sallii lisätä tuotteita suoraan luettelon luokkaan).

Valitse luettelohierarkian ylin solmu palataksesi pääluettelon otsikkonäkymään. Määritä voimassaolo- ja vanhentumispäivämäärät tarpeen mukaan **Yleiset**-pikavälilehdessä.

Ennen kuin luettelo on käytettävissä, se on julkaistava. Valitsemalla **Vahvista luettelo** **Luettelot**-valikossa voit käsitellä oikeellisuustarkistuksen. Tämä on pakollinen toimenpide ja se tarkistaa, että pakolliset määritykset ovat tarkkoja. Näet tarkistuksen tulokset valitsemalla **Näytä tulokset**. Jos tiedoista löytyy virheitä, korjaa tiedot ja suorita oikeellisuustarkistus uudelleen kunnes oikeellisuustarkistus on läpäisty.

Kun oikeellisuustarkistus on vahvistettu, valitsemalla **Työnkulku** valikosta aloitat hyväksyntätyönkulun. Valitse **Lähetä** **Työnkulku**-valikossa suorittaaksesi prosessin. Määritä työnkulun valtuutetut käyttäjät ja vaiheet kohdassa **Retail ja Commerce** \> **Pääkonttorin asetukset** \> **Commercen työnkulut**. Työnkulku määrittää vaiheet, jotka tarvitaan saamaan luettelo tilaan **Hyväksytty**. Luettelon ollessa **Hyväksytty**-tilassa voit valita **Julkaise**-toiminnon **Luettelot**-valikossa suorittaaksesi prosessin loppuun. Kun luettelo on **Julkaistu**-tilassa, sitä voidaan käyttää puhelinkeskuksen tilaustenkäsittelyn ja luettelon lähettämisen prosesseissa.

## <a name="use-catalogs-to-drive-sales-order-pricing-and-promotions"></a>Luetteloiden avulla voit parantaa myyntitilausten hinnoittelua ja tarjouksia

Tärkein syy luettelon määrittämiseen puhelinkeskuksen käytettäväksion mahdollisuus määritellä kyseisen luettelon omat hinnat ja tarjoukset. Tästä luettelosta tilaavat asiakkaat saavat nämä hinnat ja alennukset puhelinkeskuksen tilaustenkäsittelyn yhteydessä, jos luettelon **Lähdekoodin tunnus** kohdistetaan tilauksen otsikkoon tai riveille.

Voit määrittää luettelokohtaiset hinnat valitsemalla **Hintaryhmät**-vaihtoehdon **Luettelot**-välilehdessä linkittääksesi yhden tai useamman hintaryhmän luetteloon. Kaikki kauppasopimukset, hinnanoikaisun kirjauskansiot ja lisäalennukset (raja, määrä, yhdistelmäalennus), jotka on linkitetty samaan hintaryhmään otetaan käyttöön, kun asiakkaat tilaavat tästä luettelosta.

Valitse **Lähdekoodit**-pikavälilehdessä **Lisää** lisätäksesi vähintään yhden **Lähdekoodin tunnus** -tunnuksen tähän luetteloon. Tämä on koodi, jota käytetään puhelinkeskuksen tilaustenkäsittelyn aikana myyntitilauksen otsikkoon (ja riveihin). Tätä koodia käytetään linkittämään myyntitilaus luetteloon ja lopuksi hintaryhmiin ja kaikkiin erityisiin hintoihin ja tarjouksiin, jotka on määritetty.

## <a name="use-the-source-id-to-track-costs-and-response-rates"></a>Lähteen tunnuksen avulla voit seurata kustannuksia ja vastausprosentteja

Määrittäessäsi **Lähdekoodin tunnus** -tunnusta voit linkittää vaihtoehtoisesti tämän tunnuksen **Kohdemarkkinan tunnus** -tunnukseen. **Kohdemarkkinan tunnus** voidaan määrittää kohdassa **Retail ja Commerce** \> **Asiakkaat** \> **Kohdemarkkina**. Kohdemarkkina on luettelo asiakkaista ja/tai prospekteista, jotka kuuluvat käyttäjän määrittämään segmenttiin. Asiakkaan tai prospektin tietojen linkittäminen lähdekoodin tunnukseen sallii paremman näkyvyyden luettelon vastaanottajiin. Jos asiakas on linkitetty kohdemarkkinaan ja kohdemarkkina on linkitetty aktiiviseen lähdekoodin tunnukseen tai luetteloon, puhelinkeskuksen käyttäjät voivat nähdä, mitä luetteloita asiakas on saanut valitsemalla **Lähdekoodit**-vaihtoehdon **Asiakkaat**-valikkovälilehdessä **Asiakaspalvelu**-sivulla. Tilausta syötettäessä puhelinkeskuksen käyttäjät näkevät myös ne luettelot, jotka asiakkaalle lähetetettiin avattavasta **Lähde**-luettelosta myyntitilauksen otsikossa. Suodattimen muuttaminen arvosta **Kaikki** arvoon **Tavoiteltu** sallii käyttäjän näkevän tietyt aktiiviset luettelot, jotka lähetettiin asiakkaalle. Tästä on hyötyä tilanteissa, joissa asiakas on unohtanut luettelon tai ei löydä tai voi lulea luettelon koodia, kun ne soittavat luodakseen myyntitilauksen.

On mahdollista linkittää useita lähdekoodin tunnuksia luetteloon. Tätä usein tarvitaan, kun yritys haluaa seurata vastausprosentteja eri segmenttien mukaan. Yritys antaa luettelon yksilöllisen koodin eri asiakassegmenteille, jonka avulla voidaan seurata vastausprosenttia segmentin tasolla tietyn luettelon tapahtuman sisällä.

Valitsemalla jonkin tietyn **Lähdekoodin tunnus** -tietueen ja valitsemalla **Tiedot**-asetuksen **Lähdekoodit**-pikavälilehdessä näyttää lisäkentät, joissa myyntiennusteet lähetyskustannukset ja postituksen päivämäärät voidaan rekisteröidä. Nämä tiedot ovat hyödyllisiä luettelon tehokkuutta analysoitaessa. Käyttäjät voivat palata tälle sivulle myöhemmin ja käyttää **Lähdekoodin analyysi**- ja **Vertaile kampanjoita** -painikkeita käynnistääkseen analyyttiset raportit, jotka perustuvat nykyisiin myyntitietoihin ja verratakseen kustannuksia ja budjettia toteutuneisiin kuluihin.

## <a name="configure-catalog-specific-order-and-item-scripts"></a>Määritä luettelokohtaisten tilausten ja nimikkeiden komentosarjat

Kun puhelukeskuksen käyttäjä luo myyntitilauksen, hän voi käyttää näytön komentosarjoja. Nämä tekstipohjaiset komentosarjat voivat toimittaa lisätiedot, jotka käyttäjän on sanottava asiakkaalle tai ne voivat olla sisäisiä huomautuksia tai muistutuksia, jotka käyttäjien tulee tarkistaa ja ottaa huomioon myyntitilausta luoetaessa.

On usein hyödyllistä käyttää erilaisia komentosarjoja eri luetteloihin. **Komentosarjat**-pikavälilehdessä ennalta määritetyt komentosarjat voidaan linkittää luetteloon. **Ajoitus**-kentän avulla voit määrittää, jos komentosarja näkyy tilauksen alussa (kun lähdekoodin tunnus määritetään tilausotsikkoon) tai tilauksen lopussa (myyntitilauksen yhteenvetolomakkeessa).

Valittaessa luettelohierarkian solua ja käsiteltäessä **Tuotteet**-pikavälilehden tietoja käyttäjät voivat myös linkittää komentosarjoja, jotka ovat luettelo- tai nimikekohtaisia **Komentosarjat**-toiminnon avulla.

## <a name="configure-catalog-specific-up-sell-and-cross-sell-items"></a>Määritä luettelokohtaisia lisämyynti- ja liittyviä nimikkeitä

Lisämyynnin ja liittyvien tuotteiden ehdotuksien linkittäminen voidaan tehdä tuotteiden asetuksissa, mutta joissakin tapauksissa yrityksen saattaa haluta tarjota tiettyjä lisämyynnin tai liittyviä tuotteita asiakkaille, jotka tilaavat tiettyä tuotetta tietystä luettelosta. Valitse **Tuotteet**-pikavälilehdessä nimike ja valitse **Nimikkeiden lisämyynti / liittyvien tuotteiden myynti** määrittääksesi tuotteita lisämyyntiin tai liittyvien tuotteiden myyntiin asiakkaille, jotka ostavat luettelosta valitun nimikkeen. Puhelukeskuksen tilausta tallennettaessa luettelokohtaiset lisämyynnin tai liittyvien tuotteiden myynnin nimikkeet näkyvät ruudulla niiden vakionimikkeiden sijaan, joita on määritetty kyseiselle nimikkeelle tavallisen tuotemäärityksen kautta.

Lisämyynnin tai liittyvien tuotteiden myynnin nimikkeet voivat myös hyödyntää komentosarjaominaisuuksia näyttämään tiettyjä viestejä, jotka käyttäjä näkee näytettäessä isämyynnin tai liittyvien tuotteiden myynnin nimikettä tilauskäsittelyn aikana. Lisämyynnin tai liittyvien tuotteiden myynnin nimikkeisiin sidotut komentosarjat, jotka on määritetty erityisesti luettelotuotteeseen, näkyvät vain kun kyseisen luettelon lähdekoodia käytetään puhelukeskuksen tilaustenkäsittelyssä.

## <a name="catalog-page-analysis"></a>Luettelosivujen analyysi

**Luettelot**-välilehdessä on mahdollisuus määrittää **Luettelosivut**. Tämän toiminnon avulla voit määrittää tulostetun luettelon ja siihen liittyvät kustannukset tietyille sivuille ja sivutyypeille.

Määritettäessä tuotteita luettelossa käytä **Tuotesivun asettelu** -toimenpide määrittääksesi nimikkeelle tietyt sivut, sivun prosenttiosuus ja sivun tietojen sijainti. Näiden tietojen määrittämisen avulla käyttäjät voivat käyttää **Luetteloalueen analyysiraportti** -raporttia. Tämä raportti löytyy valitsemalla **Retail ja Commerce** \> **Puhelinkeskuksen raportit** \> **Luetteloalueen analyysiraportti**. Tämä raportti analysoi luetteloon liityvän myynnin (myyntitilaukset, missä luettelon lähteen tunnus on sidottu tilauksen otsikkoon tai riviin) ja siihen liittyvän sivun prosenttiosuuden ja kustannukset, jotta saadaan perinteiselle suoralle markkinoinnille **Neliötuuma-analyysi** -raportti.

## <a name="catalog-requests"></a>Luettelopyynnöt

Kun luettelot määritetään ja julkaistaan Commercessa, **Lähetä luettelo** -toimintoa voidaan käyttää. Tämä toiminto on käytössä **Asiakashaku**- ja **Asiakaspalvelu**-sivuilla. Valittuasi asiakastietueen kautta **Asiakashaku**-sivulla tai tarkastellessasi valitun asiakkaan tiliä **Asiakaspalvelu**-sivulla, käyttäjät voivat valita **Lähetä luettelo** -vaihtoehdon, joka avautuu valintaikkunassa, jossa käyttäjä voi valita kaikkien julkaistujen ja aktiivisten luetteloiden listasta. Käyttäjä voi valita luettelon ja määrän ja tietyn lähetettävän lähdekoodin tunnuksen. Kun napsautetaan **Lähetä**-painiketta, pyyntö on tallennettu, jonka jälkeen sitä voidaan hallita tulostamalla **Luettelopyynnöt**-raportti. Tämä raportti löytyy valitsemalla **Retail ja Commerce** \> **Puhelinkeskuksen raportit** \> **Luettelopyyntöjen raportti**. Se sisältää kaikki luettelopyynnöt, kuten asiakkaan nimen ja osoitteen tiedot luetteloa pyytäneeltä asiakkaalta. Tätä raporttia voidaan käyttää sisäisesti tai tiedot voidaan lähettää kolmannelle osapuolelle, joka tukee ulkoisia prosesseja luettelon lähettämiseksi fyysisesti asiakkaalle.

## <a name="additional-features"></a>Lisätoiminnot

**Luettelot**-välilehdessä voidaan määrittää myös **Maksusuunnitelma** ja **Vapaita tuotteita**. Jos luetteloon linkitettyä lähdekoodin tunnusta käytetään puhelinkeskuksen tilaustenkäsittelyn aikana, asiakas on oikeutettu ilmaisiin tuotteisiin tai tiettyihin luetteloon määritettyihin maksusuunnitelmiin. Tarvittaessa voit rajoittaa asiakkaan valitsemaan vain luetteloon linkitetyistä maksusuunnitelmista eikä kaikista järjestelmän maksusuunnitelmistaa valitsemalla **Salli vain luettelosuunnitelmat** -valintaruudun yhdelle tai useammalle lähdekoodin tunnukselle määrittääksesi kyseisen rajoituksen.

## <a name="additional-notes"></a>Lisähuomautukset

Tällä hetkellä, kun lähdekoodin tunnusta käytetään puhelinkeskuksen myyntitilaukseen, sitä käytetään luettelokohtaisten hintojen, alennusten, komentosarjojen ja ylös- ja ristiinmyynnin edistämiseen. Järjestelmä ei kiellä tai estä tilaamasta myyntitilauksella tuotetta, joka ei ole luettelossa. Jos on tilattu luetteloon kuulumaton nimike, järjestelmä käyttää ensin **Hintaryhmä**-määritystä, joka määritetään puhelinkeskuksen kanavassa (**Retail ja Commerce** \> **Kanavat** \> **Puhelinkeskukset** \> **Kaikki puhelinkeskukset**) nimikkeen hinnalle tai tarjouksille. Jos tiettyä kanavan hintaa ei löydy, käytetään nimikkeen perusmyyntihintaa.


[!INCLUDE[footer-include](../includes/footer-banner.md)]