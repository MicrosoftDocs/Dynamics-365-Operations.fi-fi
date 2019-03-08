---
title: Kaksoisvaluutta
description: Tässä ohjeaiheessa käsitellään kaksoisvaluuttaa eli tilannetta, jossa raportointivaluuttaa käytetään Microsoft Dynamics 365 for Finance and Operationsin toisena kirjanpitovaluuttana.
author: kweekley
manager: AnnBe
ms.date: 10/10/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, Ledger, AssetTransReportingCurrencyAmountsWizard,BankAccountTransReportingCurrencyAmountsWizard, LedgerTrialBalanceListPage
audience: Application User
ms.reviewer: shylaw
ms.search.scope: ''
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-10
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 8de178ec80f7408d657e746b633703f386c8e02d
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "330307"
---
# <a name="dual-currency"></a>Kaksoisvaluutta

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 for Finance and Operationsin versiossa 8.1 (lokakuu 2018) käyttöönotetulla toiminnolla raportointivaluutan käyttötarkoitusta voidaan muuttaa ja sitä voidaan käyttää toisena kirjanpitovaluuttana. Tätä toimintoa kutsutaan *kaksoisvaluutaksi*. Kaksoisvaluuttamuutoksia ei voi poistaa käytöstä määritysavaimella tai parametrilla. Koska raportointivaluuttaa käytetään toisena kirjanpitovaluuttana, raportointivaluutan laskentatapa kirjauslogiikassa on muuttunut.

Lisäksi useita moduuleja on täydennetty niin, että voivat seurata, raportoida ja käyttää raportointivaluuttaa erilaisissa prosesseissa. Näitä moduuleja ovat esimerkiksi seuraavat: **Kirjanpito**, **Taloushallinnan raportointi**, **Ostoreskontra**, **Myyntireskontra**, **Maksuliikenteen hallinta** ja **Käyttöomaisuuserät**. Päivityksen jälkeen Maksuliikenteen hallinta- ja Käyttöomaisuuserät-moduuleissa on suoritettava tietyt vaiheet. Lue sen vuoksi asiaan liittyvät osat huolellisesti tässä ohjeaiheessa.

## <a name="posting-process"></a>Kirjausprosessi

Kaikkien kirjanpitotapahtuman kirjanpitoon luovien tapahtumien kirjauslogiikkaa on muutettu. Raportointivaluutta laskettiin aiemmin seuraavasti:

Tapahtuman valuuttasumma \> Kirjanpitovaluutan summa \> Raportointivaluuttasumma

Esimerkki: Tapahtuma kirjataan Kanadan dollarina (CAD). CAD-summa muunnetaan kirjanpitovaluutaksi, joka on Yhdysvaltain dollari (USD). USD-summa muunnetaan sitten raportointivaluutaksi, joka on euro (EUR). Tämän vuoksi tarvitaan sekä CAD:n ja USD:n että USD:n ja EUR:n välinen vaihtokurssi.

Uusi laskenta on seuraavanlainen:

Tapahtuman valuuttasumma \> Kirjanpitovaluutan summa

Tapahtuman valuuttasumma \> Raportointivaluuttasumma

Tämän muutoksen vuoksi nyt tarvitaan sekä CAD:n ja USD:n että CAD:n ja EUR:n välinen vaihtokurssi.

## <a name="reports-and-inquiries"></a>Raportit ja kyselyt

Monenlaisissa raporteissa ja kyselyissä näkyy nyt sekä raportointivaluutan että kirjanpitovaluutan summat. Kaikkia raportteja ja kyselyjä ei ole päivitetty. Esimerkiksi raportteja, joissa summat näkyvät vain tapahtuman valuuttana, ei ole muutettu.

Muutoksia on kahdenlaisia:

- Jos raportissa tai kyselyssä on riittävästi tilaa sekä kirjanpito- että raportointivaluutan näyttämiseen, raportointivaluutan summat lisättiin.
- Jos raportissa tai kyselyssä ei ole riittävästi tilaa summien näyttämiseen kummassakin valuutassa, käyttäjät voivat valita lisätyn asetuksen avulla, kumpi valuutta näytetään.

Lisäksi moniin raportteihin ja kyselyihin lisättiin logiikka, jolla voidaan piilottaa raportointivaluutan summat, jos raportointivaluutta on sama kuin kirjanpitovaluutta tai jos raportointivaluuttaa ei ole määritetty yrityksen kirjanpidossa.

## <a name="financial-journals"></a>Talouskirjauskansiot

Talouskirjauskansiot, kuten yleinen kirjauskansio ja toimittajan laskukirjauskansio, on päivitetty siten, että niihin sisältyy lisätietoja raportointivaluutasta. Tositteen ja kirjauskansion kokonaissummat näytetään nyt raportointivaluutassa. Raportointivaluutan vaihtokurssin lisätiedot näkyvät nyt kirjauskansion rivien **Yleiset**-välilehdessä. Niinpä voitkin ohittaa raportointivaluutan vaihtokurssin tapahtumia kirjatessa.

## <a name="module-changes"></a>Moduulimuutokset

Seuraavat moduulit käyttävät raportointivaluuttaa toisena kirjanpitovaluuttana:

- [Kirjanpito](#general-ledger)
- [Talousraportointi](#financial-reporting)
- [Ostoreskontra](#accounts-payable-and-accounts-receivable)
- [Myyntireskontra](#accounts-payable-and-accounts-receivable)
- [Maksuliikenteen hallinta](#cash-and-bank-management)
- [Käyttöomaisuuserät](#fixed-assets)

### <a name="general-ledger"></a>Kirjanpito

Jos raportointivaluutta määritettiin kirjanpidossa, kirjanpito seurasi jo jokaisen kirjanpitomerkinnän raportointivaluutan summia. Nyt nämä summat kuitenkin muunnetaan tapahtumavaluutan summista.

**Kirjanpito**-moduuliin tehtiin lisäksi seuraavat muutokset:

- Raportointivaluutalle voidaan määrittää kirjanpidossa erillinen vaihtokurssityyppi. Jos organisaatio ei halua käyttää eri vaihtokurssityyppiä, voit jättää raportointivaluutan vaihtokurssityypin kentän tyhjäksi. Vaihtoehtoisesti voit valita sen vaihtokurssityypin, jota käytetään kirjanpitovaluutassa. Jos jätät kentän tyhjäksi, järjestelmä käyttää kirjanpitovaluutan vaihtokurssityyppiä.
- Uusi raportointivaluutan muutosten kirjauskansio ottaa käyttöön oikaisut, jotka kirjataan kirjanpitotileille vain raportointivaluuttana. Tämän kirjauskansion avulla kirjaukset voidaan tehdä vain kirjanpitotileille. Se ei tue konsernin sisäistä kirjausta, ja valuutan on oltava sama kuin sen yrityksen raportointivaluutta, jossa kirjauskansio kirjataan. Kun kirjauskansio kirjataan, tapahtumavaluutan ja kirjanpitovaluutan summa on 0 (nolla). Lisäksi raportointivaluutan summaksi kirjataan summa, joka on viety tapahtumaan. Koska raportointivaluutan käyttötapa on muuttunut **Ostoreskontra**-, **Myyntireskontra**- ja **Käyttöomaisuuserät**-moduuleissa, tätä kirjauskansioita voi käyttää oikaisuissa päivityksen jälkeen. Esimerkkejä kirjauskansion käytöstä on kyseisiä moduuleja käsittelevissä osissa.
- Kaudenkohdistusprosessia on päivitetty siten, että summat kohdistetaan tapahtuma-, kirjanpito- ja raportointivaluutoissa. Aiemmin summa kohdistettiin tapahtuma- ja kirjanpitovaluutoissa, jonka jälkeen kirjanpitovaluutan summa muunnettiin raportointivaluutaksi. Tämän vuoksi kirjanpitotilin saldo saattoi jäädä raportointivaluutaksi. Nyt kun summat lasketaan ja niitä käytetään kirjanpitomerkinnässä, muutoksia ei tarvitse tehdä.
- Ulkomaanvaluutan uudelleenarvostusprosessi on jo tehnyt summien uudelleenarvostuksen raportointivaluutassa. Raportointivaluutan summa lasketaan kuitenkin nyt tapahtumavaluutan summan kautta. Tämä menettely selitettiin aiemmin tämän ohjeaiheen kohdassa [Kirjausprosessi](#posting-process).
- Monet kirjanpidon raportit ja kyselyt sisälsivät jo raportointivaluutan, mutta muutamissa sitä ei ollut. Tällainen on esimerkiksi **Pääkirja**-luettelosivu. Luettelosivulla on nyt kirjanpitovaluutan että raportointivaluutan sarakkeet. Huomaa, että raportointivaluutan sarakkeet on piilotettu, jos kirjanpito- ja raportointivaluutta on sama tai jos raportointivaluuttaa ei ole määritetty kirjanpidossa.

### <a name="financial-reporting"></a>Taloushallinnon raportointi

**Taloushallinnan raportointi** -moduulin laajennuksen avulla voit sisällyttää raportointivaluutan summat raporttiin kahdella tavalla. Voit raportoida sarakemäärityksessä suoraan ne raportointivaluuttasummat, jotka on kirjattu kirjanpitoon (uusi toiminto). Vaihtoehtoisesti voit jatkaa summien muuttamista kirjanpitovaluutasta raportointivaluutaksi (nykyinen toiminto).

Muutoksen voi ottaa käyttöön sarakemäärityksen **Valuutan näyttö** -asetuksella. Jos valitset **Raportointivaluutta kirjanpidosta**, sarakkeen summia ei muunneta. Sen sijaan ne raportoidaan suoraan kirjanpidosta. Jos haluat, että muunnetut summat näkyvät sarakkeessa. valitse **Muunna valuutaksi** -asetus, jossa *XXXX* sarakkeessa näkyvä raportointivaluutta. Tässä tapauksessa kirjanpitovaluutan summat muunnetaan valittuun valuuttaan nykyisellä muuntotoiminnolla.

### <a name="accounts-payable-and-accounts-receivable"></a>Ostoreskontra ja myyntireskontra

**Ostoreskontra**- ja **Myyntireskontra**-moduulit seurasivat jo raportointivaluuttasummia. Summia ei kuitenkaan näytetty tai niitä ei käytetty eri prosesseissa. Seuraavat muutokset on tehty:

- Raportointivaluuttasummat näytetään nyt sekä asiakkaiden että toimittajien tapahtumille. Raportointivaluuttasummat näytetään myös kunkin tapahtuman alkusaldolle.
- Erääntymisprosessia on päivitetty siten, että organisaatio voi tarkastella erääntymisjakaumia joko kirjanpito- tai raportointivaluutassa.
- Erilaisia kyselyjä ja raportteja päivitettiin siten, että näyttävät raportointivaluuttasummat. Tällaisia raportteja ovat esimerkiksi **Asiakas kirjanpidon täsmäytykseen** ja **Toimittaja kirjanpidon täsmäytykseen**.
- Ulkomaanvaluutan uudelleenarvostusprosessi on jo tehnyt summien uudelleenarvostuksen raportointivaluutassa. Raportointivaluutan summa lasketaan kuitenkin nyt tapahtumavaluutan summan kautta. Tämä menettely on selitetty kohdassa [Kirjausprosessi](#posting-process).
- **Päivityksessä huomioon otettavia seikkoja:** Ennen päivitystä asiakirjojen (kuten laskujen ja maksujen) raportointivaluuttasummat lasketaan kirjanpitovaluutan avulla. Esimerkki: Lasku kirjataan, ennen kuin organisaatio tekee päivityksen, eikä laskua ole maksettu. Päivityksen aikana laskun kirjanpitomerkintä ei muutu. Päivityksen jälkeen kaksoisvaluuttaa koskevat muutokset ovat kuitenkin käytössä. Niinpä laskua maksettaessa maksun raportointivaluuttasumma lasketaankin tapahtumavaluutan summan avulla. Kun maksu ja lasku selvitetään, toteutuneessa voitto/tappio-summassa voi olla pieni laskennallinen ero, koska raportointivaluuttasummat on laskettu eri tavalla. Jos laskennallinen ero on merkittävä, uuden raportointivaluutan oikaisukirjauskansion avulla voidaan oikaista vain raportointivaluuttana toteutuneen voiton/tappion sekä osto- ja myyntireskontran kirjanpitotilien saldo.

### <a name="cash-and-bank-management"></a>Maksuliikenteen hallinta

**Maksuliikenteen hallinta** -moduuli ei aiemmin seurannut mitään kullekin pankkitilille kirjattua tapahtumien raportointivaluuttasummia. Päivityksen jälkeen uusien kirjattujen tapahtumien raportointivaluuttasummia seurataan. Raportointivaluuttasummat on kuitenkin lisättävä aiemmin kirjattuihin tapahtumiin alareskontrassa.

- **Päivityksessä huomioon otettavia seikkoja:** Koska pankkitilitapahtumat eivät aiemmin seuranneet raportointivaluuttasummia alareskontrassa, lisätty ohjattu toiminto auttaa lisäämään raportointivaluuttasummat pankkitilitapahtumiin. Ohjattu toiminto **ei** kirjaa uudelleen kirjanpitoon. Sen sijaan se ottaa raportointivaluuttasummat kirjanpidosta ja päivittää ne alareskontratauluissa.

    - Voit aloittaa ohjatun toiminnon käytön valitsemalla **Maksuliikenteen hallinta** \> **Asetukset** \> **Lisää raportointivaluuttasummat pankkitilitapahtumiin**.
    - Ohjattu toiminto näyttää kaikki ne valitun yrityksen pankkitilien tapahtumat, joiden raportointivaluutan summa on 0 (nolla). Vain ennen päivitystä kirjatut tapahtumat sisältyvät tähän.
    - Ohjattu toiminto etsii kutakin pankkitilitapahtumaa vastaavat kirjanpitomerkinnät kirjanpidossa ja kirjaa oletusraportointivaluutan summan. Vaikka summia voi muokata, niiden muokkaaminen **ei** ole suositeltavaa. Tämä johtuu siitä, pankkitilien saldoja ei ehkä pystytä täsmäyttämään kirjanpitoon. Summaa on syytä muokata vain siinä tapauksessa, että raportointivaluuttasummaa ei löydy kirjanpidosta. Ohjattu toiminto näyttää siinä tapauksessa raportointivaluutan summaksi nollan (0).
    - Jos valitset ohjatussa toiminnossa **Peruuta**, pankkitilitapahtumat ja raportointivaluuttasummiin tehdyt muutokset tallennetaan odottamaan ohjatun toiminnon suorittamista seuraavan kerran. Pankkitilitapahtumien raportointivaluuttasummia ei kuitenkaan päivitetä. Tämä päivitys tapahtuu vasta sitten, kun valitset ohjatussa toiminnossa **Valmis**. Voit suorittaa ohjatun toiminnon useita kertoja. Niinpä voitkin korjata mahdolliset virheelliset raportointivaluuttasummat.

- Maksuliikenteen hallinnan prosesseja ei ole muutettu, mutta erilaiset raportit ja kyselyt päivitettiin näyttämään raportointivaluuttasummat. Kassavirtaennusteiden raportit ovat kuitenkin poikkeuksia. Niitä ei ole päivitetty sisältämään raportointivaluuttasummia.

### <a name="fixed-assets"></a>Käyttöomaisuuserät

**Käyttöomaisuuserät** -moduuli ei aiemmin seurannut mitään kuhunkin käyttöomaisuuskirjanpitoon kirjattuja tapahtumien raportointivaluuttasummia. Päivityksen jälkeen uusien kirjattujen tapahtumien raportointivaluuttasummia seurataan. Raportointivaluuttasummat on kuitenkin lisättävä aiemmin kirjattuihin tapahtumiin alareskontrassa.

Myös poistoprosessiin on tehty merkittäviä muutoksia. Nämä muutokset edellyttävät käyttäjän toimia päivityksen jälkeen. Seuraaviin muutoksiin on ehdottomasti tutustuttava, vaikket vielä käyttäisikään Käyttöomaisuuserät-moduulia.

- Tapaa, jolla poistoprosessi määrittää raportointivaluuttasumman, on muutettu. Seuraavassa skenaariossa verrataan tapaa, jolla poisto määritti aiemmin raportointivaluuttasumman, tapaan, jolla se määritetään nyt.

    **Poistoskenaario**

    Käyttöomaisuuserä on hankittu ja sille kirjattu seuraavat summat. Huomaa, että vaikka raportointivaluuttasumma on kirjattu kirjanpitoon, sitä ei ole tallennettu käyttöomaisuuden alareskontran tauluihin.

    | Tapahtumalaji | Tapahtuman summa | Vaihtokurssi | Kirjanpitovaluutan summa | Vaihtokurssi | Raportointivaluuttasumma |
    |------------------|--------------------|---------------|----------------------------|---------------|---------------------------|
    | Hankinta      | 1 000 000 DKK      | 2,0           | 500 000 USD                | 2,5           | 200 000 EUR               |

    **Raportointivaluutan aiempi poisto**

    Poistoehdotus suoritetaan vuoden lopussa, ja se laskee seuraavat summat.

    | Tapahtumalaji | Tapahtuman summa | Vaihtokurssi | Kirjanpitovaluutan summa | Vaihtokurssi | Raportointivaluuttasumma |
    |------------------|--------------------|---------------|----------------------------|---------------|---------------------------|
    | Poisto     | 50 000 USD         | 1.0           | 50 000 USD                 | 2,6           | 19 230,77 EUR             |

    Kun poistoehdotus suoritetaan, se laskee kirjanpitovaluutan summan käyttämällä poistomenetelmää. Se muuntaa sitten kyseisen summan raportointivaluutaksi käyttämällä voimassa olevaa USD:n ja EUR:n välistä vaihtokurssia. Tämä muunto aiheuttaa ongelmia, koska käyttöomaisuutta ei ole poistettu kokonaan raportointivaluutassa spot-kurssia käytettäessä.

    **Raportointivaluutan uusi poisto**

    Poistoprosessia on muutettu siten, että myös raportointivaluuttasumma on laskettu poistomenetelmää käyttämällä. Kun poistoa tehdään käyttöominaisuuserässä, saadaan seuraavat tulokset.

    | Tapahtumalaji | Tapahtuman summa | Vaihtokurssi | Kirjanpitovaluutan summa | Vaihtokurssi                                                       | Raportointivaluuttasumma |
    |------------------|--------------------|---------------|----------------------------|---------------------------------------------------------------------|---------------------------|
    | Poisto     | 50 000 USD         | 1.0           | 50 000 USD                 | 2,5<blockquote>[!NOTE] Vaikka vaihtokurssi on näkyvissä, sitä ei käytetä raportointivaluuttamuuntoon.</blockquote> | 20 000 EUR                |

    Kun poistoehdotus suoritetaan, se laskee sekä kirjanpitovaluutan että raportointivaluutan summan poistomenetelmää käyttämällä. Summia käytetään sitten kirjanpitoon tehdyssä kirjanpitomerkinnässä. Raportointivaluuttasumman määrittämiseen ei käytetä muuntoa.

- **Päivityksessä huomioon otettavia seikkoja:** Koska käyttöomaisuuskirjanpidon tapahtumat eivät aiemmin seuranneet raportointivaluuttaa, lisätty ohjattu toiminto auttaa lisäämään raportointivaluuttasummat käyttöomaisuuskirjanpidon tapahtumiin. Ohjattu toiminto **ei** kirjaa uudelleen kirjanpitoon. Koska poistoehdotuksen tapa laskea raportointivaluuttasummat on muuttunut, ohjattua toimintoa **on käytettävä** ja se on suoritettava loppuun jokaisessa yrityksessä, ennen kuin organisaatio voi kirjata poistotapahtumia.

    - Aloita ohjatun toiminnon käyttö valitsemalla **Käyttöomaisuuserät** \> **Asetukset** \> **Lisää raportointivaluuttasummat käyttöomaisuuskirjoihin**.
    - Ohjattu toiminto näyttää kaikki ne valitun yrityksen käyttöomaisuuskirjojen tapahtumat, joiden raportointivaluutan summa on 0 (nolla). Vain ennen päivitystä kirjatut tapahtumat sisältyvät tähän.
    - Ohjattu toiminto **ei** hae raportointivaluuttasummia kirjanpidosta. Kuten edellisessä skenaariossa selitettiin, kirjanpitoon alun perin kirjatut raportointivaluuttasummat käyttivät virheellisesti spot-kurssia. Näiden summien ei pitäisi näkyä käyttöomaisuuden alareskontrassa, koska seuraava poistolaskenta käyttää virheellisiä summia. Ohjattu toiminto etsii sen sijaan ensimmäisen hankintapäivän vaihtokurssin. Sen jälkeen se suosittelee alareskontraan kirjattavaksi tähän vaihtokurssiin perustuvaa raportointivaluuttasummaa. Ohjatussa toiminnossa voi olla näkyvissä edellisen skenaarion perusteella seuraavat tiedot.

        | Käyttöomaisuus | Kirja      | Tapahtumalaji | Tapahtuman päivämäärä | Valuutta | Summa tapahtuman valuuttana | Määrä  | Vaihtokurssi | Raportointivaluuttasumma |
        |-------------|-----------|------------------|------------------|----------|--------------------------------|---------|-----------|---------------------------|
        | BUIL-00001  | 200\_SLLT | Hankinta      | 6/3/2016         | DKK      | 1 000 000                      | 500,000 | 2,5       | 250,000                   |
        | BUIL-00001  | 200\_SLLT | Poisto     | 6/3/2016         | DKK      | 50 000                         | 50 000  | 2,5       | 250,000                   |
        | BUIL-00001  | 200\_SLLT | Poisto     | 6/3/2016         | DKK      | 50 000                         | 50 000  | 2,5       | 250,000                   |
        | BUIL-00001  | 200\_SLLT | Poisto     | 6/3/2016         | DKK      | 50 000                         | 50 000  | 2,5       | 250,000                   |

    - Monet asiakkaat seuraavat käyttöomaisuustapahtuman tietoja laskentataulukoissa. Näitä tietoja ovat esimerkiksi vaihtokurssit ja summat. Jos nämä tiedot ovat laskentataulukossa, voit luoda mukautetun valuuttakurssin tyypin ja päivittää sen laskentataulukon vaihtokursseilla. Tämän vaihtokurssin tyypin avulla kirjataan sitten hankintapäivän oletusvaihtokurssi ja lasketaan raportointivaluuttasumma. Jos vaihtokurssin tyyppiä ei ole valittu, ohjattu toiminto käyttää kirjanpidossa määritettyä vaihtokurssin tyyppiä.
    - Vaihtokurssia ja raportointivaluutan summia voi muuttaa. Jos vaihtokurssia muutetaan, raportointivaluutan summa lasketaan uudelleen uuden kurssin perusteella.
    - Jos valitset ohjatussa toiminnossa **Peruuta**, käyttöomaisuuskirjan tapahtumat ja vaihtokurssiin tai raportointivaluuttasummiin tehdyt muutokset tallennetaan odottamaan ohjatun toiminnon suorittamista seuraavan kerran. Käyttöomaisuuskirjan tapahtumien raportointivaluuttasummia ei kuitenkaan päivitetä. Tämä päivitys tapahtuu vasta sitten, kun valitset ohjatussa toiminnossa **Valmis**. Voit suorittaa ohjatun toiminnon useita kertoja. Niinpä voitkin korjata mahdolliset virheelliset raportointivaluuttasummat.
    - Kun raportointivaluuttasummien päivitys alareskontrassa on valmis, **Oletko päivittänyt kaikki raportointivaluuttasummat käyttöomaisuuskirjan tapahtumiin?** -asetukseksi on **ehdottomasti** valittava **Kyllä**. Valitse lopuksi **Valmis**. Poistolaskelmia ei voi suorittaa loppuun, ennen kuin **Oletko päivittänyt kaikki raportointivaluuttasummat käyttöomaisuuskirjan tapahtumiin?** -asetukseksi on valittu **Kyllä**. Kun tässä asetuksessa on valittu **Kyllä**, ohjattu toiminto ei ole enää käytettävissä.
    - Kun alareskontran käyttöomaisuustapahtumat on päivitetty raportointivaluuttasummilla, kyseiset summat eivät vastaa kirjanpitoon alun perin kirjattuja summia. Raportointivaluutan muutosten kirjauskansion avulla voidaan kuitenkin päivittää kirjanpidon poistokirjanpitotilin saldot siten, että ne vastaavat alun perin kirjattuja summia.
    - Uudella **Tietojen hallinta** -työtilaan lisätyllä **Omaisuustapahtumien summat raportointivaluutassa** -yksiköllä voidaan viedä tietoja ohjatusta toiminnosta. Voit sitten määrittää poistotapahtumien saldon käyttöomaisuuden alareskontrassa näiden tietojen avulla. Kyseistä saldon avulla voidaan sitten määrittää raportointivaluutan muutoksen summa kirjanpidossa.

- **Päivityksessä huomioon otettavia seikkoja:** Käyttöomaisuuseriin on lisätty uusia asetuskenttiä, joilla voidaan laskea poistoja. Nämä kentät on ehkä päivitettävä ennen seuraavaa poistolaskentaa.

    - Käyttöomaisuuskirjan (**Käyttöomaisuuserät** \> **Kirjat**) **Yleiset**-pikavälilehdessä on uusi **Hankintahinta raportointivaluutassa** -kenttä.
    - Käyttöomaisuuskirjan (**Käyttöomaisuuserät** \> **Kirjat**) **Poisto**-pikavälilehdessä on uusi **Odotettu romuarvo raportointivaluutassa** -kenttä.
    - Käyttöomaisuusparametrien (**Käyttöomaisuuserät** \> **Asetukset** \> **Käyttöomaisuusparametrit**) **Yleiset**-pikavälilehdessä on uusi **Vähimmäispoiston summa raportointivaluutassa** -kenttä.
    - Kirjojen (**Käyttöomaisuuserät** \> **Asetukset** \> **Kirjat**) **Yleiset**-pikavälilehdessä on kaksi uutta kenttää: **Pyöristä poisto raportointivaluutassa** ja **Jätä nettokirjanpitoarvo raportointivaluutan muotoon**.

- Koska poistoehdotus laskee nyt summat sekä kirjanpito- että raportointivaluutassa, käyttöomaisuuserän kirjauskansio on päivitetty näyttämään poistosummat raportointivaluuttana. Poistotapahtumien tapahtumavaluutta on aina kirjanpitovaluutta. Niinpä nämä summat näkyvät edelleen **Debet**- ja **Kredit**-sarakkeissa. Ruudukkoon on lisätty kaksi uutta saraketta: **Debet raportointivaluutassa** ja **Kredit raportointivaluutassa**.

    - Uudet kentät ovat käytettävissä vain, jos tapahtumatyyppi on jokin neljästä poistotyypistä: **Poisto**, **Poistojen oikaisu**, **Erikoispoisto** tai **Erityinen poistovähennys**.
    - Jos poistotapahtuman tyyppi on kirjattu käyttöomaisuuserän kirjauskansioon, raportointivaluuttasummat näkyvät uusissa sarakkeissa. Näitä summia voi muuttaa.
    - Jos kirjanpidon kirjanpito- ja raportointivaluutta ovat samat, summat pysyvät synkronoituina. Jos muutat **Kredit**-summaa, **Kredit raportointivaluutassa** -summa muutetaan automaattisesti sitä vastaavaksi.
    - Jos käyttöomaisuuserän kirjauskansioon on kirjattu jokin muu tapahtuman tyyppi, **Debet raportointivaluutassa**- ja **Kredit raportointivaluutassa** -summia ei näytetä koskaan ennen kirjausta eikä myöskään kirjauksen jälkeen. Kirjanpito- ja raportointivaluuttasummat on edelleen käytettävissä kirjanpitoon kirjattavassa tositteessa.
