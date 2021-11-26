---
title: Osapuolen ja yleinen osoitekirja
description: Tässä aiheessa kuvataan kaksoiskirjoituksen osapuolen ja yleinen osoitekirja.
author: RamaKrishnamoorthy
ms.date: 08/11/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-02-22
ms.openlocfilehash: 127b4092ad3c5e8737aff43f503e0a8f36ff1ec8
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/10/2021
ms.locfileid: "7781341"
---
# <a name="party-and-global-address-book"></a>Osapuolen ja yleinen osoitekirja

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

*Osapuoli* ja *yleinen osoitekirja* ovat käsitteitä Finance and Operations -sovelluksissa. Osapuoli voi olla henkilö tai organisaatio. On kätevää tallentaa ja hallita osapuolen ominaisuuksia, kuten nimeä, kieltä, yhteyshenkilöitä ja osoitteita. Sitten kun ominaisuuden arvo muuttuu yhdessä paikassa, muutos heijastuu kaikkiin paikkoihin, joissa osapuoli näkyy.

## <a name="party"></a>Osapuoli

Osapuoli on henkilö tai organisaatio, joka osallistuu liiketoimintaan. Käyttämällä osapuolen käsitettä henkilöllä tai organisaatiolla voi olla useita rooleja (työntekijä, asiakas, toimittaja tai yhteyshenkilö) liiketoiminnassa. Rooli perustuu kontekstiin ja tarkoitukseen. Seuraavassa on esimerkkejä rooleista kahdessa fiktiivisessä yrityksessä: Contosossa ja Fabrikamissa:

+ **Työntekijä** – työntekijä. Esimerkkinä on Contoson työntekijä.
+ **Toimittaja** – Toimittajaorganisaatio tai elinkeinonharjoittaja, joka toimittaa tavaroita tai palveluja yritykselle. Jos Fabrikam esimerkiksi myy Contosolle toimituksia, Fabrikam on Contoson toimittaja.
+ **Yhteyshenkilö** – yhteyshenkilö. Jos Contoso esimerkiksi ostaa toimituksia Fabrikamista, Contoson työntekijät ottavat yhteyttä Fabrikamin yhteyshenkilöön.
+ **Asiakas** – asiakas on henkilö tai yritys, joka ostaa tavaroita yritykseltä. Jos Contoso esimerkiksi ostaa toimituksia Fabrikamista, Contoso on Fabrikamin asiakas.

Osapuolimallia käytetään usein keskitasoisten ja monimutkaisten organisaatioiden ja ihmisten välisten suhteiden kuvaamiseen erityisesti silloin, kun osapuolilla on enemmän kuin yksi rooli. Joitakin yleisiä esimerkkejä:

+ Osapuoli voi olla sekä asiakas että toimittaja. Esimerkiksi Pohjois-Amerikassa Fabrikam myy sähköjohtoja Contosolle ja ostaa Contosolta koottuja kaiuttimia. Euroopassa Fabrikam myy varaosia Contosolle mutta ei osta mitään Contosolta.
+ Osapuoli voi olla sekä työntekijä että asiakas. Contoson työntekijä esimerkiksi ostaa Contosolta elektroniikkaa omaan käyttöön.
+ Henkilön ja organisaation välillä voi olla monta-moneen-suhteita (N:N). Esimerkiksi Fabrikam toimittaa huoltoasiantuntijoita, ja sen palveluksessa on sijoittelun koordinaattori. Sijoittelun koordinaattori löytää huoltoasiantuntijoita Fabrikamin useiden asiakkaiden työpyyntöihin. Contoso on yksi Fabrikamin asiakkaista. Kun Contoso tarvitsee palveluasiantuntijan, se ottaa yhteyttä sijoittelun koordinaattoriin, joka tämän jälkeen edistää pyyntöä. Koska sijoittelun koordinaattori käsittelee kaikkien asiakkaiden pyyntöjä, tähän liittyy N:N-suhde.

Seuraavassa kuvassa näkyy osapuolen tietomalli:

![Osapuolen tietomalli.](media/party-gab-image1.png)

> [!TIP]
> Kun yrität luoda uutta tilitietuetta, voit etsiä tietuetta nimen perusteella **Osapuoli**-kentän avulla. Jos tietue löytyy tällä tavalla, se on vain valittava. Järjestelmä täyttää automaattisesti kaikki tiedot osapuolen tiedoilla. Kaikkia pakollisia kenttiä ei tarvitse täyttää manuaalisesti. Tämä toiminta löytyy käyttövalmiista **Tili**-, **Yhteyshenkilö**- ja **Toimittaja**-sivuilta.

Kaksoiskirjoitus ei tue kaikkia Finance and Operations -sovellusten osapuolen rooleja. Täydellinen luettelo osapuolen rooleista on [yleisen osoitekirjan yleiskatsauksessa](../../../fin-ops/organization-administration/overview-global-address-book.md).

### <a name="global-address-book"></a>Yleinen osoitekirja

Yleinen osoitekirja on liiketoimintaan osallistuvien organisaatioiden ja henkilöiden postiosoitteiden ja sähköisten osoitteiden hakemisto.

Yleinen osoitekirja tallentaa ja käsittelee tarvittavan monta postiosoitetta ja sähköistä osoitetta. Esimerkiksi Fabrikamilla on polttoaineasemia 50 sijainnissa. Kullakin sijainnilla on eri postiosoite, sähköpostiosoite ja puhelinnumero. Kaikki yritysostot laskutetaan pääasemalta, mutta ostot toimitetaan suoraan tiettyyn ostoa pyytäneeseen polttoaineasemaan. Yleinen osoitekirja tallentaa pääaseman Fabrikamin laskutusosoitteena ja tallentaa kunkin polttoaineaseman toimitusosoitteena. Osoitteet voi tallentaa kerran ja noutaa tarvittaessa tarjouksia ja tilauksia varten.

Liiketoimintakontekstin mukaan henkilöllä tai organisaatiolla voi olla useita rooleja, ja kaikissa rooleissa voidaan käyttää samaa postiosoitetta ja sähköistä osoitetta. Tällöin osoitteen muuttaminen yhdessä roolissa pitäisi näkyä kaikissa muissa rooleissa. Yleisen osoitekirjan tallentaa ja käsittelee osoitteet koko globaalisti.

Seuraavassa kuvassa on yleisen osoitekirjan tietomalli.

![Yleisen osoitekirjan tietomalli.](media/party-gab-image2.png)

## <a name="contact"></a>Kontakti

Asiakasvuorovaikutussovelluksissa Yhteyshenkilö on henkilö. **Yhteyshenkilö**-taulu on kuitenkin ylikuormitettu edustamaan henkilöä, portaalin käyttäjää, B2C-asiakasta tai toimittajaa. Esitys on epäsuora, eikä eroa voi selvittää selvittämättä niihin liittyviä tapahtumia. **Yhteyshenkilö**-taulun suhde **Tili**-tauluun on rajoitettu 1:1-suhteeksi. Osana osapuolen ja yleisen osoitekirjan mallia kaksoiskirjoitus ottaa käyttöön luokitusta varten täsmällisiä ominaisuuksia, ja kaksoiskirjoitus sallii N:N-suhteet yhteyshenkilön ja organisaation (**Tili**-yksikkö tai **Toimittaja**-yksikkö) välillä.

**Yhteyshenkilö**-rivejä on kahta eri tyyppiä:

+ **Merkitty yhteyshenkilö** – **Yhteyshenkilörivi**, jossa **Yritys**-kentällä on pakollinen arvo.
+ **Merkitsemätön yhteyshenkilö** – **Yhteyshenkilörivi**, jossa **Yritys**-kenttä on tyhjä.

**Yhteyshenkilö**-tauluun voi tallentaa seuraavan tyyppisiä rivejä.

| Rivityyppi | kuvaus |
|----------|-------------|
| Henkilö, joka on asiakas (esimerkiksi myyntikelpoinen yhteyshenkilö tai B2C-asiakas) | Merkitty yhteyshenkilötietue, jossa **Yritys**-kenttä ei ole tyhjä ja **On asiakas** -kentän arvo on **Kyllä**. |
| Henkilö, joka on toimittaja (esimerkiksi elinkeinonharjoittaja kuten toimittaja) | Merkitty yhteyshenkilötietue, jossa **Yritys**-kenttä ei ole tyhjä ja **On toimittaja** -kentän arvo on **Kyllä**. |
| Henkilö, joka on sekä asiakas että toimittaja | Merkitty yhteyshenkilötietue, jossa **Yritys**-kenttä ei ole tyhjä ja **On asiakas** -kentän arvo on **Kyllä** ja **On toimittaja** -kentän arvo on **Kyllä**. Henkilö voi olla sekä yhden tuotteen valmistaja että toisen tuotteen kuluttaja. Sekä Finance and Operations -sovellukset että kaksoiskirjoitus tukevat tätä suhdetta. |
| Henkilö, joka on organisaation yhteyshenkilö mutta ei ole asiakas tai toimittaja | Merkitsemätön yhteyshenkilötietue, jossa **Yritys**-kenttä on tyhjä ja **On asiakas** -kentän arvo on **Ei** ja **On toimittaja** -kentän arvo on **Ei**. |

## <a name="contact-for-party-table"></a>Osapuolen yhteyshenkilö -taulukko

**Osapuolen yhteyshenkilö** -taulukko tallentaa ja käsittelee **Tili**-rivien ja **Yhteyshenkilö**-rivien väliset N:N-suhteet. Se voi suodattaa pois merkityt **Yhteyshenkilö**-rivit merkitsemättömistä riveistä ja liittää vain merkitsemättömät **Yhteyshenkilö**-rivit **Tili**- tai **Toimittaja**-riveille.

Esimerkiksi Natasha Jones ja Miguel Reyes ovat eläinlääkäreitä, jotka tarjoavat hoitoa omien alueidensa maatiloille. Natasha palvelee Seattlen alueella ja Miguel Kentin alueella. Asiakasvuorovaikutussovelluksessa maatiloja edustavat asiakkaat ja eläinlääkäreitä yhteyshenkilöt. Natashan yksi **yhteyshenkilö**-tietue liittyy kaikkiin maatiloihin, joissa Natasha työskentelee. Samoin yksi Miguelin **yhteyshenkilö**-tietue liittyy kaikkiin maatiloihin, joissa Miguel työskentelee.

Nämä suhteet tallennetaan **Osapuolen yhteyshenkilö** -tauluun. Nämä tiedot löytyvät käyttövalmiista **Tili**-, **Yhteyshenkilö**- ja **Toimittaja**-sivuilta:

+ **Tili**-sivulla voit käyttää **Liitetyt yhteyshenkilöt** -välilehteä yhden tai usean yhteyshenkilön liittämiseksi **Tili**-riviin. Tällä tavalla voit määrittää organisaation yhteyshenkilöitä. Tämän jälkeen voit valita yhden yhteyshenkilön tilin ensisijaiseksi yhteyshenkilöksi. Jos käytät **Pikaluonti**-sivua, voit valita vain yhteyshenkilön. Toiminta on sama, kun käytät **Toimittaja**-sivua ja tietuetyyppinä on **Organisaatio**.
+ Kun rivi on **Yhteyshenkilö**-sivulla asiakas, toimittaja tai molemmat (merkitty yhteyshenkilö), voit liittää yhteyshenkilöitä **Liitetyt yhteyshenkilöt** -välilehdessä. Tällä tavalla määritetään yhteyshenkilöt B2C-asiakkaalle tai toimittajalle. Tämän jälkeen voit valita yhden yhteyshenkilön ensisijaiseksi yhteyshenkilöksi. Jos käytät **Pikaluonti**-sivua, voit valita vain yhteyshenkilön.
+ Kun rivi on **Yhteyshenkilö**-sivulla yhteyshenkilö (merkitsemätön yhteyshenkilö), voit liittää asiakkaita tai toimittajia **Liitetyt organisaatiot** -välilehdessä. Tällä tavalla määritetään asiakkaita tai toimittajia taustalla olevaan yhteyshenkilöön. Asiakas tai toimittaja voi olla organisaatio, henkilö tai molemmat. Voit valita arvon vain yhdestä neljästä kentästä kerrallaan:

    + Jos valitset tunnuksen **Osapuolen tunnus** -kentässä, pohjana oleva yhteyshenkilö liitetään kaikkiin valitun osapuolen rooleihin.
    + Jos valitset arvon **Liitetty yhteyshenkilö**, valitset **henkilö**-tyyppiä olevan merkityn yhteyshenkilön.
    + Jos valitset arvon **Liitetty tili**- tai **Liitetty toimittaja** -kentässä, valitset organisaation.

    ![Liitetyt organisaatiot -välilehti yhteyshenkilösivulla.](media/party-gab-image3.png)

    Riippumatta valinnastasi liitos luodaan osapuolen tasolla, se koskee kaikkia osapuolen rooleja ja tallennetaan **Osapuolen yhteyshenkilö** -entiteettiin.

> [!NOTE]
> Asiakasvuorovaikutussovelluksissa **Osapuolen yhteyshenkilö** -taulun näyttönimi on **Asiakkaan/toimittajan yhteyshenkilö**.

Kun avaat **Yhteyshenkilö**-rivin, jolla sekä **On asiakas**- että **On myyjä** -kentän asetuksena on **Ei**, **Liitetyt organisaatiot** -välilehti näytetään. Tämän välilehden avulla voit liittää yhteyshenkilöön yhden tai useampia asiakas- tai toimittajaorganisaatioita.

Kun avaat **Yhteyshenkilö**-rivin, jolla joko **On asiakas**- tai **On myyjä** -kentän asetuksena on **Kyllä**, **Liitetyt yhteyshenkilöt** -välilehti näytetään. Tämän välilehden avulla voit liittää yhteyshenkilöitä.

## <a name="postal-addresses"></a>Postiosoitteet

**Tili**-, **Yhteyshenkilö**- ja **Toimittaja**-sivuilla on uusi välilehti nimeltä **Osoitteet**. Tämä välilehti tukee useita postinumeroita ruudukon avulla seuraavan kuvan mukaisesti.

![Postiosoitteiden ruudukko.](media/party-gab-image4.png)

Ruudukko sisältää seuraavat sarakkeet:

+ **Postiosoitteen roolit** – Postiosoitteen tarkoitus.
+ **On ensisijainen** – Arvo, joka ilmaisee, onko osoite ensisijainen osoite.
+ **Osoitenumero** – Osoitteen järjestys.

Voit luoda niin monta postiosoitetta kuin haluat ruudukon yläpuolella olevalla **Uusi osoite** -painikkeella.

**Tili**-sivun **Yhteenveto**-välilehden **Osoite 1**- ja **Osoite 2**-kentät vastaavat **toimitus**- ja **laskutusosoitteita**.

![Postiosoitteiden Yhteenveto-välilehti.](media/party-gab-image5.png)

**Yhteyshenkilö**-sivun **Yhteenveto**-välilehden **Osoite 1**-, **Osoite 2**- ja **Osoite 3** -kentät vastaavat **yritys**-, **toimitus**- ja **laskutusosoitteita**.

## <a name="electronic-addresses"></a>Sähköiset osoitteet

**Tili**-, **Yhteyshenkilö**- ja **Toimittaja**-sivuilla on uusi välilehti nimeltä **Sähköiset osoitteet**. Tämä välilehti tukee useita sähköisiä osoitteita ruudukon avulla seuraavan kuvan mukaisesti.

![Sähköisten osoitteiden ruudukko.](media/party-gab-image6.png)

Ruudukko sisältää seuraavat sarakkeet:

+ **Tyyppi** – Sähköisen osoitteen tyyppi.
+ **On ensisijainen** – Arvo, joka ilmaisee, onko osoite ensisijainen osoite.
+ **Tarkoitus** – Sähköisen osoitteen tarkoitus.

Voit luoda niin monta postiosoitetta kuin haluat ruudukon yläpuolella olevalla **Uusi sähköinen osoite** -painikkeella.

Sähköiset osoitteet ovat käytettävissä vain tässä ruudukossa. Tulevissa versioissa kaikki postiosoitteen ja sähköisenosoitteen kentät poistetaan muista välilehdistä, kuten **Yhteenveto**- ja **Tiedot**-välilehdistä. **Tiedot**-välilehdessä näkyvät yhteystiedot ovat vain luku -muotoisia kopioita ensisijaisesta sähköisestä osoitteesta, kuten ensisijainen puhelinnumero, ensisijainen sähköposti, ensisijainen faksinumero ja ensisijainen Twitter-tunnus. Liidin hyväksyntäprosessin aikana voidaan antaa sekä työnumero että matkapuhelimenumero. Työnumero katsotaan ensisijaiseksi puhelinnumeroksi, jos **IsMobile=No**, ja matkapuhelinnumero katsotaan toissijaiseksi puhelinnumeroksi, jos **IsMobile=Yes**.

> [!TIP]
> Postiosoitetta ja sähköistä osoitetta hallitaan käyttämällä **Tili**- ja **Yhteyshenkilö**-lomakkeiden **Osoitteet**- ja **Sähköiset osoitteet** -välilehtiä. Näin varmistetaan, että osoitetiedot synkronoidaan Finance and Operations -sovelluksiin.

## <a name="setup"></a>Luo perustiedot

1. Avaa asiakasvuorovaikutussovelluksen ympäristö.

2. Asenna uusin versio (2.2.2.60 tai uudempi): [Kaksoiskirjoituksen sovellusorkestrointiratkaisu](https://aka.ms/dual-write-app).

3. Asenna [Kaksoiskirjoituksen osapuoli ja yleisiä osoitekirjaratkaisuja](https://aka.ms/dual-write-gab).

4. Avaa Finance and Operations -sovellus. Siirry tietojen hallintamoduuliin ja valitse Kaksoiskirjoitus-välilehti. Kaksoiskirjoitus-hallintasivu avautuu.

5. Käytä molempia vaiheissa 2 ja 3 asennettuja ratkaisuja käyttäen [Käytä ratkaisua](link-your-environment.md) -toimintoa.

6. Pysäytä seuraavat yhdistämiset, koska niitä ei tarvita enää. Sen sijaan voit suorittaa `Contacts V2 (msdyn_contactforparties)`-kartan.

    + CDS-yhteyshenkilöt V2 ja yhteyshenkilöt (viittaa asiakkaan yhteyshenkilöihin)
    + CDS-yhteyshenkilöt V2 ja yhteyshenkilöt (viittaa toimittajan yhteyshenkilöihin)

7. Osapuolitoimintojen seuraavat yksiköiden yhdistämismääritykset päivitetään, joten uusin versio on otettava käyttöön näissä yhdistämismäärityksissä.

    Yhdistämismääritys | Päivitä tähän versioon | Muutokset
    ---|---|---
    `CDS Parties (msdyn_parties)`| 1.0.0.0 | Tämä on uusi määritys, joka on lisätty osana tätä julkaisua.
    `Contacts V2 (msdyn_contactforparties)`| 1.0.0.5 | Tämä on uusi määritys, joka on lisätty osana tätä julkaisua.
    `Customers V3 (accounts)` | 1.0.0.5 |Poistaa `PartyNumber`-kentän ja muut osapuoleen liittyvät kentät, kuten nimen, henkilökohtaiset tiedot, postiosoitekentät ja sähköisen osoitteen kentät.
    `Customer V3 (contacts)` | 1.0.0.5 | Poistaa `PartyNumber`-kentän ja muut osapuoleen liittyvät kentät, kuten nimen, henkilökohtaiset tiedot, postiosoitekentät ja sähköisen osoitteen kentät.
    `Vendors V2 (msdyn_vendors)` | 1.0.0.6 | Poistaa `PartyNumber`-kentän ja muut osapuoleen liittyvät kentät, kuten nimen, henkilökohtaiset tiedot, postiosoitekentät ja sähköisen osoitteen kentät.
    `CDS Sales quotation headers (quotes)` | 1.0.0.7 | Korvasi yhteyshenkilön `ContactforParty`-viitteellä.
    `Sales invoice headers V2 (invoices)` | 1.0.0.4 | Korvasi yhteyshenkilön `ContactforParty`-viitteellä.
    `CDS Sales order headers (salesorders)` | 1.0.0.5 | Korvasi yhteyshenkilön `ContactforParty`-viitteellä.
    `CDS Party postal address locations (msdyn_partypostaladdresses)` | 1.0.0.1  | Tämä on uusi määritys, joka on lisätty osana tätä julkaisua.
    `CDS postal address history V2 (msdyn_postaladdresses)` | 1.0.0.1 | Tämä on uusi määritys, joka on lisätty osana tätä julkaisua.
    `CDS postal address locations (msdyn_postaladdresscollections)` | 1.0.0.0 | Tämä on uusi määritys, joka on lisätty osana tätä julkaisua.
    `Party Contacts V3 (msdyn_partyelectronicaddresses)` | 1.0.0.0 | Tämä on uusi määritys, joka on lisätty osana tätä julkaisua.
    `Complimentary Closings ( msdyn_compliemntaryclosings)` | 1.0.0.0 | Tämä on uusi määritys, joka on lisätty osana tätä julkaisua.
    `Decision making roles (msdyn_decisionmakingroles)` | 1.0.0.0 | Tämä on uusi määritys, joka on lisätty osana tätä julkaisua.
    `Loyalty levels (msdyn_loyaltylevels)` | 1.0.0.0 | Tämä on uusi määritys, joka on lisätty osana tätä julkaisua.
    `Contact person titles (msdyn_salescontactpersontitles)` | 1.0.0.0 | Tämä on uusi määritys, joka on lisätty osana tätä julkaisua.
    `Personal character types (msdyn_personalcharactertypes)` | 1.0.0.0 | Tämä on uusi määritys, joka on lisätty osana tätä julkaisua.
    `Salutations (msdyn_salutations)` | 1.0.0.0 | Tämä on uusi määritys, joka on lisätty osana tätä julkaisua.
    `Employment job functions (msdyn_employmentjobfunctions)` | 1.0.0.0 | Tämä on uusi määritys, joka on lisätty osana tätä julkaisua.

8. Ennen kuin voit käyttää yllä olevia karttoja, integrointiavaimet on päivitettävä manuaalisesti seuraavien ohjeiden mukaisesti. Valitse sitten **Tallenna**.

    | Yhdistämismääritys | Avaimet |
    |-----|------|
    | Tili |  accountnumber [Tilinumero]<br>msdyn_company.cdm_companycode [Yritys (Yrityksen koodi)] |
    | Kontakti | msdyn_contactpersonid [Tilinumero/Yhteyshenkilön tunnus]<br>msdyn_company.cdm_companycode [Yritys (Yrityksen koodi)] |
    | Asiakkaan/toimittajan yhteyshenkilö | msdyn_contactforpartynumber [Osapuolen numeron yhteyshenkilö]<br>msdyn_associatedcompanyid.cdm_companycode [Liittyvä yritys (Yrityksen koodi)] |
    | Toimittaja | msdyn_vendoraccountnumber [Toimittajan tilinumero]<br>msdyn_company.cdm_companycode [Yritys (Yrityksen koodi)]|

9. Dataversessa kaksoiskappaleiden tunnistussääntöjen merkkiraja on kasvanut 450 merkistä 700 merkkiin. Tämä raja mahdollistaa yhden tai usean avaimen lisäämisen kaksoiskappaleiden tunnistussääntöihin. Laajenna kaksoiskappaleiden tunnistussäännöt **Tilit**-taulukolle määrittämällä seuraavat kentät.

    | Kenttä | Arvo |
    |-------|-------|
    | Nimi | Tilit, joilla on sama tilinimi. |
    | kuvaus | Havaitsee tilitietueet, joissa on sama arvo Tilin nimi -määritteessä. |
    | Perustietuetyyppi | Tili |
    | Vastaava tietuetyyppi | Tili |
    | Tilin nimi (kenttä) | Tarkka vastaavuus |
    | Yritys (kenttä) | Tarkka vastaavuus |
    | Suhdetyyppi (kenttä) | Tarkka vastaavuus |
    | Osapuolen tunnus (kenttä) | Tarkka vastaavuus |
    | Valitse (kenttä) | (tyhjä) |

    ![Tilien kaksoiskappaleiden sääntö.](media/duplicate-rule-1.PNG)

10. Laajenna kaksoiskappaleiden tunnistussäännöt **Yhteystiedot**-taulukolle määrittämällä seuraavat kentät.

    | Kenttä | Arvo |
    |-------|-------|
    | Nimi | Yhteyshenkilöt, joilla on sama etunimi ja sukunimi. |
    | kuvaus | Havaitsee yhteyshenkilötietueet, joissa on samat arvot Etunimi- ja Sukunimi-kentissä. |
    | Perustietuetyyppi | Kontakti |
    | Vastaava tietuetyyppi | Kontakti |
    | Etunimi (kenttä) | Tarkka vastaavuus |
    | Sukunimi (kenttä) | Tarkka vastaavuus |
    | Yritys (kenttä) | Tarkka vastaavuus |
    | Osapuolen tunnus (kenttä) | Tarkka vastaavuus |
    | Valitse (kenttä) | (tyhjä) |

    ![Yhteyshenkilöiden kaksoiskappaleiden sääntö.](media/duplicate-rule-2.PNG)

11. Jos käytät kaksoiskirjoitusta tällä hetkellä, noudata ohjeita kohdassa [Päivitä osapuolen osoitekirja ja yleinen osoitekirja](upgrade-party-gab.md) ja päivitä tiedot.

12. Suorita kartat seuraavassa järjestyksessä. Jos näyttöön tulee virheilmoitus, jonka mukaan "Projektin vahvistus epäonnistui. Puuttuva kohdekenttä...", avaa kartta ja valitse **Päivitä taulut**. Suorita sitten kartta.

    Finance and Operations -sovellus | Asiakkaiden aktivointisovellus  
    ----------------------------|------------------------
    [CDS-osapuolet](mapping-reference.md#220) | msdyn_parties
    [CDS-postiosoitteiden sijainnit](mapping-reference.md#234) | msdyn_postaladdresscollections
    [CDS-osapuolen postiosoitteen historia V2](mapping-reference.md#235) | msdyn_postaladdresses
    [CDS-osapuolen postiosoitteiden sijainnit](mapping-reference.md#233) | msdyn_partypostaladdresses
    [Osapuolen yhteyshenkilöt V3](mapping-reference.md#236) | msdyn_partyelectronicaddresses
    [Asiakkaat V3](mapping-reference.md#101) | tilit
    [Asiakkaat V3](mapping-reference.md#116) | yhteyshenkilöt
    [Toimittajat V2](mapping-reference.md#202) | msdyn_vendors
    [Yhteyshenkilöiden arvonimet](mapping-reference.md#223) | msdyn_salescontactpersontitles
    [Loppusanat](mapping-reference.md#222) | msdyn_complimentaryclosings
    [Tervehdykset](mapping-reference.md#228) | msdyn_salutations
    [Päätöksentekoroolit](mapping-reference.md#224) | msdyn_decisionmakingroles
    [Työsuhteen työtehtävät](mapping-reference.md#225) | msdyn_employmentjobfunctions
    [Kanta-asiakastasot](mapping-reference.md#226) | msdyn_loyaltylevels
    [Henkilökohtaisten luonteenpiirteiden tyypit](mapping-reference.md#227) | msdyn_personalcharactertypes
    [Yhteyshenkilöt V2](mapping-reference.md#221) | msdyn_contactforparties
    [CDS-myyntitarjouksen otsikko](mapping-reference.md#215) | tarjoukset
    [CDS-myyntitilauksien otsikot](mapping-reference.md#217) | salesorders
    [Myyntilaskun otsikot V2](mapping-reference.md#118) | laskut

> [!NOTE]
> `CDS Contacts V2 (contacts)`-kartta on kartta, jonka olet keskeyttänyt vaiheessa 1. Kun yrität suorittaa muita karttoja, nämä 2 karttaa saattavat näkyä riippuvaisten luettelossa. Älä suorita näitä karttoja.
>
> Jos osapuolen ja yleisen osoitekirjan ratkaisu on asennettu, sinun on poistettava käytöstä laajennus `Microsoft.Dynamics.SCMExtended.Plugins.Plugins.LeadPrimaryContactPostCreate: QualifyLead of lead`. Jos poistat osapuolen ja yleisen osoitekirjan ratkaisun asennuksen, laajennus on otettava uudelleen käyttöön.
>
> `msdyn_*partynumber`-kenttää (yksirivinen tekstikenttä), joka sisältyy **Tili**-, **Yhteyshenkilö**- ja **Toimittaja**-taulukoihin, ei pitäisi käyttää jatkossa. Etiketin nimessä on etuliite **(Vanhentunut)** selkeyden vuoksi. Käytä sen sijaan **msdyn_partyid**-kenttää. Kenttä on haku **msdyn_party**-taulukkoon.

> Taulun nimi | Vanha kenttä | Uusi kenttä
> --------|-------|--------
> Tili | `msdyn_partynumber` | `msdyn_partyid`
> Kontakti | `msdyn_partynumber` | `msdyn_partyid`
> msdyn_vendor | `msdyn_vendorpartynumber` | `msdyn_partyid`

## <a name="templates"></a>Mallit

Taulujen yhdistämisten kokoelma toimii yhdessä osapuolen ja yleisen osoitekirjan vuorovaikutusta seuraavan taulukon mukaisesti.

| Finance and Operations -sovellus | Asiakkaiden aktivointisovellus | kuvaus |
|----------------------------|-------------------------|-------------|
| [Yhteyshenkilöiden arvonimet](mapping-reference.md#223) | msdyn\_salescontactpersontitles |
| [Asiakkaat V3](mapping-reference.md#101) | tilit |
| [Asiakkaat V3](mapping-reference.md#116) | yhteyshenkilöt |
| [CDS-osapuolet](mapping-reference.md#220) | msdyn\_parties |
| [CDS-osapuolen postiosoitteiden sijainnit](mapping-reference.md#233) | msdyn\_partypostaladdresses |
| [CDS-osapuolen postiosoitteen historia V2](mapping-reference.md#235) | msdyn\_postaladdresses |
| [CDS-postiosoitteiden sijainnit](mapping-reference.md#234) | msdyn\_postaladdresscollections |
| [CDS-myyntitarjouksen otsikko](mapping-reference.md#215) | tarjoukset |
| [CDS-myyntitilauksien otsikot](mapping-reference.md#217) | salesorders |
| [Loppusanat](mapping-reference.md#222) | msdyn\_complimentaryclosings |
| [Yhteyshenkilöt V2](mapping-reference.md#221) | msdyn\_contactforparties |
| [Päätöksentekoroolit](mapping-reference.md#224) | msdyn\_decisionmakingroles |
| [Työsuhteen työtehtävät](mapping-reference.md#225) | msdyn\_employmentjobfunctions |
| [Kanta-asiakastasot](mapping-reference.md#226) | msdyn\_loyaltylevels |
| [Osapuolen yhteyshenkilöt V3](mapping-reference.md#236) | msdyn\_partyelectronicaddresses |
| [Henkilökohtaisten luonteenpiirteiden tyypit](mapping-reference.md#227) | msdyn\_personalcharactertypes |
| [Myyntilaskun otsikot V2](mapping-reference.md#118) | laskut |
| [Tervehdykset](mapping-reference.md#228) | msdyn\_salutations |
| [Toimittajat V2](mapping-reference.md#202) | msdyn\_vendors |

Lisätietoja on [kaksoiskirjoituksen yhdistämismäärityksen viitteessä](mapping-reference.md).

## <a name="known-issues-and-limitations"></a>Tunnetut ongelmat ja rajoitukset

+ Kun luot asiakkaan ja osoitteen ja tallennat sen Finance and Operations -sovelluksissa, osoite ei välttämättä synkronoidu **Osoite**-taulukkoon. Tämä johtuu kaksoiskirjoitusalustan järjestysongelmasta. Voit ratkaista ongelman luomalla ensin asiakkaan ja tallentamalla sen. Lisää sitten osoite.
+ Finance and Operations -sovelluksissa kun asiakastietueessa on ensisijainen osoite ja luot asiakkaalle uuden yhteyshenkilön, yhteyshenkilötietue perii ensisijaisen osoitteen liitetystä asiakastietueesta. Näin tapahtuu myös toimittajan yhteyshenkilölle. Dataverse ei tue tällä hetkellä tätä toimintatapaa. Jos kaksoiskirjoitus on käytössä, ensisijaisella osoitteella perityt asiakkaan yhteyshenkilöt Finance and Operations -sovelluksesta synkronoidaan Dataversen kanssa osoitteineen.
+ **Tili**-, **Yhteyshenkilö**- ja **Toimittaja**-lomakkeiden sähköisten osoitteiden välilehdessä määritetyt sähköiset osoitteet tulevat `msdyn_partyelectronicaddress`-taulukosta. Nämä tiedot eivät siirry liittyviin tapahtumiin, kuten myyntitilaukseen, tarjoukseen ja ostotilaukseen. Tämä ongelma aiotaan korjata asteittaisessa julkaisussa. Tili- ja yhteyshenkilötietueiden sähköisten osoitekenttien olemassa olevat tiedot toimivat edelleen myyntitilausten, tarjousten ja ostotilausten kaltaisissa tapahtumissa.
+ Finance and Operations -sovelluksissa voit luoda yhteyshenkilötietueen **Lisää yhteyshenkilö** -lomakkeesta. Kun yrität luoda uuden yhteyshenkilön **Näytä yhteyshenkilö** -lomakkeesta, toimenpide epäonnistuu. Tämä on tiedossa oleva ongelma.

    ![Tunnettu Lisää yhteyshenkilö -ongelma.](media/party-gab-contact-issue.png)

+ **Alkuperäinen synkronointi** ei tue **Käytettävissä alkaen**- ja **Käytettävissä saakka** -aikakenttiä kohdassa **ContactForParty**, koska DIXF muuntaa arvon merkkijonoksi kokonaisluvun sijaan. Muunto aiheuttaa virheen `Cannot convert the literal '<say 08:00:00>’ to the expected type edm.int32`.
+ Kun postiosoitetta käytetään useampaan kuin yhteen syyhyn, esimerkiksi yrityksen yhteysosoitteena ja laskutusosoitteena, pitäisi näkyä muodossa `Business;Invoice` seuraavan kuvan mukaisesti. Jos lisäät arvojen väliin välin, saat virheilmoituksen.

    ![Tiedossa oleva osoiteongelma.](media/party-gab-address-issue.png)

+ Et voi syöttää postiosoitetta, jonka päivämäärä on tulevaisuudessa käyttämällä Finance and Operations -sovellusta kaksoiskirjoituksella, koska Dataverse ei tue päivämäärän voimassaoloa. Jos kirjoitat postiosoitteen, jonka päivämäärä on tulevaisuudessa, Finance and Operations -sovelluksella, se synkronoi Dataversen kanssa kokonaan ja näet osoitteen käyttöliittymässä välittömästi. Tämän tietueen päivitykset johtavat virheeseen, koska sen päivämäärä on tulevaisuudessa eikä nykyinen Finance and Operations -sovelluksessa.
