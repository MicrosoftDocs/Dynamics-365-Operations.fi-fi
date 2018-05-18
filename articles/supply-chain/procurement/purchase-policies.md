---
title: "Ostokäytännöt"
description: "Tässä artikkelissa on tietoja ostokäytännöistä. Ostokäytäntö on kokoelma sääntöjä, jolla hallitaan ostoehdotusprosessia. Ostokäytännöt auttavat ostotapahtumien hallinnoijia toteuttamaan hankintastrategiaa luomalla käytäntörakenteen, joka on linjassa organisaation strategisten ostotarpeiden kanssa."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchReqSourcingPolicyRule, SysPolicy, SysPolicyListPage
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 11614
ms.assetid: 729a304d-0f3f-4ccb-bd5b-46ee0976c57f
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 675a7a8b0da228e789ee37ca8fe1d0c0ea01c283
ms.contentlocale: fi-fi
ms.lasthandoff: 11/03/2017

---

# <a name="purchasing-policies"></a>Ostokäytännöt

[!include [banner](../includes/banner.md)]

Tässä artikkelissa on tietoja ostokäytännöistä. Ostokäytäntö on kokoelma sääntöjä, jolla hallitaan ostoehdotusprosessia. Ostokäytännöt auttavat ostotapahtumien hallinnoijia toteuttamaan hankintastrategiaa luomalla käytäntörakenteen, joka on linjassa organisaation strategisten ostotarpeiden kanssa.

Ostokäytäntö koostuu joukosta käytäntösääntöjä. Kun määrität käytäntösäännön, sinun on ensin valittava sääntötyyppi. Voit sitten luoda sääntötyypille säännön määrittämällä sen asetukset, alkamis- ja päättymispäivämäärän.  

Esimerkiksi, järjestelmänvalvoja luo käytännön, valitsee säännön tyypiksi **Luettelokäytännön** ja lisää luettelokäytännön säännön käytäntöön. Tämän luettelon käytäntösääntö määrittää, että sisäisessä hankinnassa on käytettävä Adventure-luetteloa. Kun ostokäytäntö on liitetty tiettyyn organisaatioon, kyseisen organisaation työntekijät näkevät Adventure-luettelon luodessaan varasto-ottoehdotuksia.

## <a name="assigning-policies-to-organizations"></a>Käytäntöjen liittäminen organisaatioihin
Ennen kuin käytäntövoi astua voimaan, se on liitettävä organisaatioon. Ostokäytännöt on liitettävä **Hankinnan sisäinen tarkistus** -hierarkian tarkoitukseen. Sen vuoksi ostokäytännöt koskevat ainoastaan organisaatioita, joille on määritetty **Hankinnan sisäinen tarkistus** -hierarkian tarkoitus. Voit valita myös organisaatiot jäsentämättömästä oikeushenkilöiden luettelosta CompanyInfo-taulukossa. Nämä oikeushenkilöt on määritetty käytäntökehikossa "Yrityksiksi".

## <a name="determining-which-rule-to-apply"></a>Käytettävän säännön valitseminen
Riippuen siitä, miten ostokäytäntösi on määritetty, organisaation käyttäjiä voi koskea useampia sääntöjä. Seuraavissa esimerkeissä esitellään erilaisia tapoja, joilla voi määrittää sekä ostokäytännöt että miten niitä käytetään kun tapahtumia tapahtuu.

### <a name="example-1-simple-purchasing-policy-configuration"></a>Esimerkki 1: Yksinkertaisen ostokäytännön määrittäminen

Pienemmät, vähemmän monimutkaiset organisaatiot voivat määrittää ostokäytännöt oikeushenkilöittäin ja käyttää ainoastaan Yritykset-organisaatiohierarkiaa.  

Fabrikam on pieni yritys, jonka ostovaatimukset eivät juuri vaihtele organisaation sisällä. Ostosäännöt vaihtelevat vain organisaation oikeushenkilöiden välillä. Esimerkiksi Fabrikamin Kanadan ja Yhdysvaltojen työntekijät ostavat tavarat ja palvelut eri luetteloista ja eri toimittajilta. Fabrikam määrittää siis ostokäytäntönsä oikeushenkilötasolla.  

Fabrikam luo kaksi ostokäytäntöä. Käytäntö A koskee sen Yhdysvaltain yritystä 1111. Käytäntö B koskee sen Kanadan yritystä 2222. Kun yrityksen 1111 työntekijä ostoehdotuksen, käytäntösäännöt johdetaan käytännöstä A. Esimerkiksi tuoteluettelo, jonka työntekijä näkee määritetään käytännön A luettelon käytäntösäännössä.  

Kun yrityksen 2222 työntekijä luo ostoehdotuksen, käytäntösäännöt perustuvat käytäntöön B.  

**Huomautus:** Jos yrityksen 1111 työntekijä ostaa nimikkeen yrityksen 2222 työntekijän puolesta, käytetään yritykselle 2222 määritettyjä käytäntösääntöjä (toisin sanoen käytännön B sääntöjä).

### <a name="example-2-complex-purchasing-policy-configuration"></a>Esimerkki 2: Monitasoisen ostokäytännön määrittäminen

Edellisessä esimerkissä kaikki ostosäännöt oli määritetty yhdelle organisaatiohierarkialle, Yritykset. Monitasoinen organisaatio voi kuitenkin määrittää käytäntöjä useille organisaatiohierarkioille.  


Contoso on suuri yritys, joka edellyttää monitasoisia ostosääntöjä hallitsemaan ehdotusprosessia. Contoso on määrittänyt säännöt kahdelle erilliselle organisaatiohierarkialle: Osasto ja Yleinen ostojenhallinta.  

Käytäntö 123 on määritetty Osasto-organisaatiohierarkialle Ison-Britannian myynti – Myyntiosastolle. Käytännössä 123 ostoehdotuksen hallintasäännössä määritetään, että vähimmäistilausmäärillä on käytettävä rajoituksia. Tässä säännössä **Pakota vähimmäistilausmäärän rajoitukset** -asetus on valittuna.  

Käytäntö 456 on määritetty Yleinen ostojenhallinta -organisaatiohierarkiassa Myynti ja markkinointi -osastolle. Käytännössä 456 ostoehdotuksen hallintasäännössä ei määritetä, että vähimmäistilausmäärillä on käytettävä rajoituksia. Tässä säännössä **Pakota vähimmäistilausmäärän rajoitukset** -asetus ei ole valittuna.  

Sam työskentelee Ison-Britannian myyntiosastolla Contoson Ison-Britannian toimipisteessä. Sekä Osasto-, että Yleinen ostojenhallinta -organisaatiohierarkiat koskevat hänen osastoaan. Kun Sam luo ostoehdotuksen, järjestelmän on määritettävä, kumpaa käytäntöä sovelletaan. Järjestelmänvalvoja on määrittänyt ostokäytäntöjen parametrit siten, että ostokäytäntöjä sovelletaan seuraavassa tärkeysjärjestyksessä:

1.  Yleinen ostojenhallinta
2.  Osasto
3.  Yritykset

Samin luomaan ostoehdotukseen sovelletaan siis käytäntöä 456, eikä ostoehdotukselta vaadita vähimmäistilausmäärää.

## <a name="policy-rules"></a>Käytännön säännöt
### <a name="catalog-policy-rule"></a>Luettelon käytäntösääntö

Luettelon käytäntösääntö määrittää tuotteiden hankintaluettelon, jonka käyttäjät näkevät luodessaan ostoehdotuksia. Jos käyttäjälle on myönnetty oikeudet tilata tuotteita toisen käyttäjän puolesta, ehdotus käyttää pyynnön lähettäjän oikeushenkilölle ja toimintayksikölle määritettyä luettelon käytäntösääntöä määrittääkseen, mikä luettelo hankintasivustolla näytetään. Ennen luettelon käytäntösäännön määrittämistä sinun on luotava tuotteiden hankintaluettelo ja julkaistava se.

### <a name="category-access-policy-rule"></a>Luokan käyttöoikeuskäytäntösääntö

Luokan käyttöoikeuskäytäntösääntö määrittää, mihin luokkiin käyttäjillä on käyttöoikeus luodessaan ostoehdotuksia. Jos mitään sääntöä ei ole määritetty, kaikki hankintaluokat on mahdollista lisätä ostoehdotukseen.

1.  Käytä pääorganisaation luokan käyttöoikeuden käytäntösääntöä luokkaan valitsemalla **Sisällytä pääsääntö** -valintaruutu.
2.  Valitse **Käytettävissä olevat luokat** -ruudusta luokat, joihin sääntö vaikuttaa. Kun valitset luokan, myös kaikki hierarkiassa ylempänä olevat luokat lisätään **Valitut luokat** -luetteloon.
3.  Valitse **Sisällytä aliluokat** -asetus, jos haluat käyttää sääntöä kaikkiin valitun luokan alaluokkiin.

### <a name="category-policy-rule"></a>Luokan käytäntösääntö

Luokan käytäntösääntö määrittää, miten käyttäjä voi valita toimittajia kuhunkin luokkaan. Se määrittää myös vastaanotto- ja laskutusprosessien vaatimukset.

### <a name="re-approval-rule-for-purchase-orders"></a>Ostotilausten uudelleenhyväksymissääntö

Uudelleenhyväksymissääntö on valinnainen sääntö, joka määrittää ehdot muutetun ostotilauksen uudelleenhyväksynnälle. Valitut kentät arvioidaan ostotilauksen työnkulussa, kun "Edellyttää ostotilauksen uudelleenhyväksymistä" -ehto on määritetty työnkululle.

> [!NOTE]
> Kirjanpidollinen jako nollataan aina, kun muutetaan hyväksyttyä ostotilausta, jossa on käytössä muutostenhallinta. Ota huomioon, että jos haluat välttää ostotilauksen uudelleenhyväksynnän tiettyjen kenttien muuttamisen yhteydessä, Muutettu kirjanpidollinen jako -kenttää ei tule valita uudelleenhyväksyttäväksi kentäksi. 

### <a name="purchase-requisition-rfq-rule"></a>Ostoehdotuksen tarjouspyyntösääntö

Ostoehdotuksen tarjouspyyntösääntö määrittää ostoehdotusriville ehdot tarjouspyynnön pyytämiseksi. Jos rivi täyttää ehdot, tilausriville lisätään joko "epävirallinen tarjouspyyntö"- tai "virallinen tarjouspyyntö" -leima.

### <a name="purchase-requisition-control-rule"></a>Ostoehdotuksen ohjaussääntö

Ostoehdotuksen hallintasääntö on valinnainen sääntö. Tämänkaltaisia sääntöjä luodessa voit määrittää asetuksia useilla välilehdillä:

-   **Työnkulun lähetys** -välilehdessä voit määrittää kentät, jotka on täytettävä hyväksyttäväksi lähetettävän ehdotuksen riveille silloin, kun ehdotuksen tarkoitus on **Kulutus**.
-   **Tilausmäärät**-välilehdessä voit määrittää kentät, jotka ovat pakollisia ostoehdotuksessa tiettyjen ehtojen täyttyessä. Voit myös pakottaa tietyn tilausmäärän.
-   **Päivämäärät**-välilehdessä voit määrittää onko kirjauspäivä sama, kuin pyydetty päivä
-   **Osoite**-välilehdessä voit määrittää käyttäjän oikeuden luoda uusia osoitteita järjestelmään, jotka koskevat ostoehdotusta.

### <a name="requisition-purpose-rule"></a>Ehdotuksen tarkoitussääntö

Ostoehdotuksen tarkoitussääntö on valinnainen sääntö, joka määrittää tietylle yritykselle sallitut ehdotuksen tarkoitustyypit. Jos tässä säännössä ei ole määritetty toista tarkoitusta, luotujen ostoehdotuksien tarkoitus on automaattisesti **Kulutus**.

### <a name="replenishment-category-access-policy-rule"></a>Täydennysluokan käyttöoikeuskäytäntöjen sääntö

Täydennysluokan käyttöoikeussääntö on valinnainen sääntö, joka määrittää tietyn yrityksen ehdotuksen vaatimukset täyttävät, käytettävissä olevat tuotteet silloin, kun ostoehdotuksen tarkoitus on **Täydennys**.

### <a name="replenishment-control-rule"></a>Täydennyksen hallintasääntö

Täydennyksen hallintasääntö on valinnainen sääntö, joka määrittää kentät, jotka on täytettävä hyväksyttäväksi lähetettävän ehdotuksen riville silloin, kun ehdotuksen tarkoitus on **Täydennys**.

### <a name="purchase-order-creation-and-demand-consolidation-rule"></a>Ostotilauksen luonnin ja kysynnän konsolidoinnin sääntö

Ostotilauksen luonnin ja kysynnän konsolidoinnin sääntö määrittää käytäntösäännöt, joita käytetään, kun ostotilaus luodaan hyväksytystä ostoehdotuksesta. Tämänkaltaisia sääntöjä luodessa voit määrittää asetuksia useilla välilehdillä:

-   **Ostotilauksen jako** -välilehdessä voit määrittää ehdot ostoehdotusrivien jakamiselle erillisiin ostotilauksiin.
-   **Hinnan/alennuksen siirto** -välilehdessä voit määrittää, milloin hintasopimus lasketaan uudelleen ostotilausta luotaessa:
    -   **Vain, jos kauppasopimusta ei ole** – hinnat ja alennukset siirretään ostoehdotuksesta vain, jos sovellettavaa kauppasopimusta tai perushintaa ei ole olemassa. Jos nimikkeelle tai toimittajalle on olemassa perushinta, hinnat ja alennukset lasketaan uudelleen kauppasopimuksen tai perushinnan perusteella ja niitä sovelletaan ostotilaukseen. Jollei toisin määritetä, tämä on oletusasetus.
    -   **Aina** – hinnat ja alennukset siirretään aina ostoehdotuksesta.

    Voit myös sallia, että pyynnön lähettäjä saa muuttaa yksittäisten ostoehdotusrivien hinnan ja alennuksen siirtotapaa määritetystä hinnan tai alennuksen siirtosäännöstä riippumatta. Valitse **Salli manuaalinen ohitus ostoehdotuksen rivin osalta**-asetus, ottaaksesi tämän ominaisuuden käyttöön.
-   **Nimikkeen kuvauksen siirto** -välilehdellä voit siirtää nimikkeen kuvauksen ehdotuksesta silloin, kun ehdotuksen lähde on tarjouspyyntö.
-   **Hintatoleranssi**-välilehdellä voit määrittää hintatoleranssin säännöt, joiden avulla hyväksytyt ostoehdotukset reititetään takaisin tarkastusprosessiin, kun tuotteiden hankintaluettelon nimikkeen hinta kasvaa. Aseta enimmäissumma, jonka ostoehdotuksen rivinimikkeen nettosumma voi kasvaa ostoehdotuksen hyväksynnän ja ostotilauksen luonnin välillä. Nettosumma lasketaan seuraavalla kaavalla: (\[Määrä × (Yksikköhinta - Alennus) ÷ Hintayksikkö\] + Muut ostokulut) × (100 - Alennusprosentti) ÷ 100 Ostoehdotusrivit, jotka ylittävät asettamasi hintatoleranssin asetetaan pitoon ja siirretään manuaaliseen käsittelyyn. Säännöt, jotka voit määrittää **Virheiden käsittely** -välilehdellä määrittävät kuinka ostoehdotusrivit käsitellään.
-   **Virheiden käsittely** -välilehdellä voit määrittää ostoehdotukseen sovellettavan käsittelysäännön, jos sen vahvistaminen epäonnistuu ostotilauksen luonnin yhteydessä toimittajan virheen tai hintatoleranssivirheen vuoksi. Valitse jompikumpi seuraavista vaihtoehdoista:
    -   **Ei toimintoa** – Ostoehdotusrivit jätetään **Vapauta hyväksytyt ostoehdotukset** -sivulle. Ostoehdotusrivien tilana säilyy **Hyväksytty**. Virheet on kuitenkin korjattava ennen ostotilauksen luomista ostoehdotusriveille.
    -   **Peruuta ostoehdotusrivi** – Ostoehdotusrivit peruutetaan. Pyynnön lähettäjä voi luoda peruutetuille riveille uuden ostoehdotuksen, jos hän haluaa edelleen pyytää rivinimikkeitä.
    -   **Luo uusi ostoehdotusrivi** – Ostoehdotusrivit peruutetaan. Järjestelmä luo uudet ostoehdotusrivit, jotka sisältävät vain ne ostoehdotusrivit, joiden hyväksyntä epäonnistui. Uusien ostoehdotuksien tila on **Luonnos**. Nämä ostoehdotukset voidaan lähettää uudelleen tarkistettaviksi, kun kelpoisuustarkistusvirheet on ratkaistu. Ostoehdotusrivien valmistelijalle ilmoitetaan, että rivit peruutettiin, ja että epäonnistuneille ostoehdotusriveille luotiin uudet ostoehdotukset.
-   **Manuaalinen ostotilauksen luonti** -välilehdellä voit määrittää parametrit, jotka määrittävät, onko ostoehdotus käsiteltävä manuaalisesti vai voidaanko se muuntaa ostotilaukseksi automaattisesti. Parametreja voidaan soveltaa sisäisiin luettelonimikkeisiin, ulkoisiin luettelonimikkeisiin tai luettelon ulkopuolisiin nimikkeisiin. Valitse jompikumpi seuraavista vaihtoehdoista:
    -   **Luo ostotilaukset manuaalisesti** – Kaikille ostoehdotuksille luodaan ostotilaukset manuaalisesti.
    -   **Luo ostotilaukset automaattisesti** – Kaikille hyväksytyille ostoehdotuksille luodaan ostotilaukset automaattisesti. Ostoehdotuksia ei ole pidossa manuaalista ostotilauksen luomista varten.
    -   **Luo ostotilaukset automaattisesti muulloin kuin näiden ehtojen täyttyessä** – Määritellyt ehdot täyttäville ostoehdotuksille luodaan ostotilaukset manuaalisesti. Kaikki muut hyväksytyt ostoehdotukset muunnetaan automaattisesti ostotilauksiksi. Jos valitset **Luo ostotilaukset automaattisesti muulloin kuin näiden ehtojen täyttyessä** -asetuksen, voit lisätä hankintaluokat ja toimittajat, jotka määrittävät mitkä hyväksytyt ostoehdotusrivit asetetaan pitoon manuaalista käsittelyä varten. Tätä asetusta voidaan soveltaa sisäisiin luettelonimikkeisiin, ulkoisiin luettelonimikkeisiin ja luettelon ulkopuolisiin nimikkeisiin. Kun valitset hankintaluokan, myös kaikki tämän hankintaluokan alaluokat valitaan. Kun valitset **Kaikki** -vaihtoehdon, tietty ostoehdotusrivin tyyppi pidättää kaikki tämän rivityypin rivit manuaalista käsittelyä varten.

    Jos haluat, että ostotilaukset luodaan automaattisesti hyväksytyistä ostoehdotuksista ostotilausten luonnin eräajon suorituksen yhteydessä, valitse **Suorita automaattinen ostotilauksen luonti erätyönä** -valintaruutu. Tämän asetus koskee vain niitä ostoehdotuksia, jotka eivät edellytä manuaalista käsittelyä. Kun automaattinen ostotilausten luonti suoritetaan erätyönä, tehtävä voidaan suorittaa ajankohtana, jolloin resursseja on käytössä enemmän. Valitse **Kun ehdotukselle on määritetty ennakkomaksu** -asetus, jos haluat asettaa hyväksytyt ostoehdotukset pitoon manuaalista käsittelyä varten, kun ostoehdotuksen riveillä on valittu **Vaaditaan ennakkomaksua** -asetus. Manuaalista käsittelyä varten pidätettyjä ostoehdotuksia voidaan suodattaa, jotta näet vain ne ostoehdotusrivit, jotka edellyttävät ennakkomaksun.
-   **Kysynnän konsolidointi** -välilehdellä voit asettaa parametrit, jotka määrittävät, voidaanko manuaalisesti käsiteltäviä ostoehdotuksia harkita ostoehdotuksen konsolidointia varten. Parametreja voidaan soveltaa sisäisiin luettelonimikkeisiin, ulkoisiin luettelonimikkeisiin tai luettelon ulkopuolisiin nimikkeisiin. Valitse jompikumpi seuraavista vaihtoehdoista:
    -   **Älä salli tarpeiden yhdistämistä** – Mitään hyväksyttyjä ostoehdotusrivien tarpeita ei yhdistetä. Tämä asetus on oletusarvon mukaan valittuna ja koskee vain niitä ostoehdotusrivejä, jotka edellyttävät manuaalista ostotilauksen luontia.
    -   **Salli aina tarpeiden yhdistäminen** – Kaikki hyväksyttyjen ostoehdotusrivien tarpeet voidaan yhdistää. **Huomautus:** Jos valitset **Salli aina tarpeiden yhdistäminen** -asetuksen **Kysynnän konsolidointi** -välilehdeltä, mutta valitset **Luo ostotilaukset automaattisesti** -asetuksen **Manuaalinen ostotilausten luonti** -välilehdellä, järjestelmä asettaa kaikki ostoehdotukset manuaaliseen käsittelyyn.
    -   **Salli tarpeiden yhdistäminen näiden ehtojen täyttyessä** – Määritä ehdot, joiden perusteella hyväksyttyjen ostoehdotusrivien tarpeet voidaan yhdistää. Voit määrittää kullekin ostoehdotusrivin tyypille ehdot hankintaluokan ja toimittajan mukaan. Jos valitset **Salli tarpeiden yhdistäminen näiden ehtojen täyttyessä**, voit määrittää kullekin ostoehdotusrivin tyypille ehdon hankintaluokan ja toimittajan mukaan. Kun valitset hankintaluokan, myös kaikki tämän hankintaluokan alaluokat valitaan. Jos valitset **Kaikki**-vaihtoehdon tietylle rivityypille, kaikki tämän rivityypin ostoehdotusrivit ovat oikeutettuja kysynnän konsolidointiin.





