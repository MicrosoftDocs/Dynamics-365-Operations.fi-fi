---
title: Osapuolen ja yleinen osoitekirja
description: Tässä aiheessa kuvataan kaksoiskirjoituksen osapuolen ja yleinen osoitekirja.
author: RamaKrishnamoorthy
ms.date: 02/22/2021
ms.topic: article
ms.service: dynamics-ax-applications
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-02-22
ms.openlocfilehash: e7bec58f8094a1448017822e7d8840368cc482b8
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750785"
---
# <a name="party-and-global-address-book"></a>Osapuolen ja yleinen osoitekirja

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Osapuolen ja yleinen osoitekirja ovat käsitteitä Finance and Operations -sovelluksissa. Osapuoli voi olla henkilö tai organisaatio. On kätevää tallentaa ja hallita **osapuolen** ominaisuuksia, kuten nimeä, kieltä, yhteyshenkilöitä ja osoitteita. Kun ominaisuuden arvo muuttuu yhdessä paikassa, se heijastuu kaikkiin paikkoihin, joissa **osapuoli** näkyy.

## <a name="party"></a>Osapuoli

*Osapuoli* on henkilö tai organisaatio, joka osallistuu liiketoimintaan. Käyttämällä osapuolen käsitettä henkilöllä tai organisaatiolla voi olla useita rooleja (työntekijä, asiakas, toimittaja tai yhteyshenkilö) liiketoiminnassa. Rooli perustuu kontekstiin ja tarkoitukseen. Seuraavassa on esimerkkejä kahdesta fiktiivestä yrityksestä, Contososta ja Fabrikamista.

+ **Työntekijä**: työntekijä. Esimerkiksi Contoson työntekijä.
+ **Toimittaja**: Toimittajaorganisaatio tai elinkeinonharjoittaja, joka toimittaa tavaroita tai palveluja yritykselle. Jos Fabrikam esimerkiksi myy toimituksia Contosolle, Fabrikam toimii toimittajan roolissa.
+ **Yhteyshenkilö**: yhteyshenkilö. Jos Contoso esimerkiksi ostaa toimituksia Fabrikamista, Contoso-yrityksen työntekijä ottaa yhteyttä Fabrikamin yhteyshenkilöön.
+ **Asiakas**: asiakas on henkilö tai yritys, joka ostaa tavaroita yritykseltä. Jos Contoso esimerkiksi ostaa toimituksia Fabrikamista, Contoso on Fabrikamin asiakas.

Osapuolimallia käytetään usein keskitasoisten ja monimutkaisten organisaatioiden ja ihmisten välisten suhteiden kuvaamiseen erityisesti silloin, kun osapuolilla on enemmän kuin yksi rooli. Joitakin yleisiä esimerkkejä:

+ Osapuoli voi olla sekä asiakas että toimittaja. Esimerkiksi Pohjois-Amerikassa Fabrikam myy sähköjohtoja Contosolle ja ostaa Contosolta koottuja kaiuttimia. Euroopassa Fabrikam myy varaosia Contosolle, mutta ei osta mitään Contosolta.
+ Osapuoli voi olla sekä työntekijä että asiakas. Contoson työntekijä esimerkiksi ostaa Contosolta elektroniikkaa omaan käyttöön.
+ Henkilön ja organisaation välillä voi olla monta-moneen-suhteita. Esimerkiksi Fabrikam toimittaa huoltoasiantuntijoita, ja sen palveluksessa on sijoittelun koordinaattori. Koordinaattori löytää huoltoasiantuntijoita Fabrikamin useiden asiakkaiden työpyyntöihin. Contoso on yksi asiakastileistä. Kun Contoso tarvitsee asiantuntijan, Contoso ottaa yhteyttä koordinaattoriin, joka tämän jälkeen edistää pyyntöä. Koordinaattori käsittelee kaikkia asiakkaita koskevat pyynnöt, mikä luo monta-moneen-suhteen.

Seuraavassa kuvassa näkyy osapuolen tietomalli:

![Osapuolen tietomalli](media/party-gab-image1.png)

> [!Tip]
> Kun yrität luoda uutta tilitietuetta, voit etsiä tietuetta nimen perusteella Osapuoli-kentän avulla. Jos tietue löytyy, sinun on vain valittava tietue. Järjestelmä täyttää automaattisesti kaikki tiedot osapuolen tiedoilla. Kaikkia pakollisia kenttiä ei tarvitse täyttää manuaalisesti. Tämä toiminta löytyy käyttövalmiista Tili-, Yhteyshenkilö- ja Toimittaja-lomakkeista.

Kaksoiskirjoitus ei tue kaikkia Finance and Operations -sovellusten osapuolen rooleja. Täydellinen luettelo osapuolen rooleista on [yleisen osoitekirjan yleiskatsauksessa](../../../fin-ops/organization-administration/overview-global-address-book.md).

### <a name="global-address-book"></a>Yleinen osoitekirja

Yleinen osoitekirja on liiketoimintaan osallistuvien organisaatioiden ja henkilöiden postiosoitteiden ja sähköisten osoitteiden hakemisto.

Yleinen osoitekirja tallentaa ja käsittelee tarvittavan monta postiosoitetta ja sähköistä osoitetta. Oletetaan esimerkiksi, että Fabrikamilla on polttoaineasemia 50 sijainnissa. Kullakin sijainnilla on eri postiosoite, sähköposti ja puhelinnumero. Kaikki yritysostot laskutetaan pääasemalta, mutta ostot toimitetaan suoraan tiettyyn ostoa pyytäneeseen polttoaineasemaan. Yleinen osoitekirja tallentaa pääaseman laskutusosoitteena ja kunkin polttoaineaseman toimitusosoitteena Fabrikamille. Osoitteet voi tallentaa kerran ja noutaa tarvittaessa tarjouksia ja tilauksia varten.

Henkilöllä tai organisaatiolla voi olla useita rooleja liiketoimintakontekstin perusteella. Kun näin on, roolien postiosoitteet ja sähköiset osoitteet voivat olla samat. Tällöin osoitteen muuttaminen yhdessä roolissa näkyy toisella roolilla ja päinvastoin. Yleisen osoitekirjan tallentaa ja käsittelee osoitteet koko globaalisti.

![Yleisen osoitekirjan tietomalli](media/party-gab-image2.png)

## <a name="contacts"></a>Yhteyshenkilöt

Asiakasvuorovaikutussovelluksissa *Yhteyshenkilö* on henkilö. **Yhteyshenkilö**-taulu on kuitenkin ylikuormitettu edustamaan henkilöä, portaalin käyttäjää, B2C-asiakasta tai toimittajaa. Esitys on epäsuora, eikä eroa voi selvittää selvittämättä niihin liittyviä tapahtumia. **Yhteyshenkilö**-taulun suhde **Tili**-tauluun on rajoitettu 1:1-suhteeksi. Osana osapuolen ja yleisen osoitekirjan mallia kaksoiskirjoitus ottaa käyttöön luokitusta varten täsmällisiä ominaisuuksia, ja kaksoiskirjoitus sallii N:N-suhteet **yhteyshenkilön** ja organisaation (Tili-yksikkö tai Toimittaja-yksikkö) välillä.

**Yhteyshenkilö**-rivejä on kahta eri tyyppiä:

+ Merkitty yhteyshenkilö – Yhteyshenkilörivi, jolla on pakollinen arvo **Yritys**-kentässä.
+ Merkitsemätön yhteyshenkilö – Yhteyshenkilörivi, jossa on tyhjä **Yritys**-kenttä.

**Yhteyshenkilö**-tauluun voi tallentaa tämäntyyppisiä rivejä:

Rivityyppi | kuvaus
---|---
Henkilö, joka on asiakas, esimerkiksi myyntikelpoinen yhteyshenkilö tai B2C-asiakas. | Merkitty yhteyshenkilötietue, jossa **Yritys**-kenttä ei ole tyhjä ja **On asiakas** -kentän arvo on **Kyllä**.
Henkilö, joka on toimittaja, esimerkiksi elinkeinonharjoittaja kuten toimittaja. | Merkitty yhteyshenkilötietue, jossa **Yritys**-kenttä ei ole tyhjä ja **On toimittaja** -kentän arvo on **Kyllä**.
Henkilö, joka on sekä asiakas että toimittaja. | Merkitty yhteyshenkilötietue, jossa **Yritys**-kenttä ei ole tyhjä ja **On asiakas** -kentän arvo on **Kyllä** ja **On toimittaja** -kentän arvo on **Kyllä**. Henkilö voi olla sekä yhden tuotteen valmistaja että toisen tuotteen kuluttaja. Sekä Finance and Operations -sovellukset että kaksoiskirjoitus tukevat tätä suhdetta.
Henkilö, joka on organisaation yhteyshenkilö mutta ei ole asiakas tai toimittaja. | Merkitsemätön yhteyshenkilötietue, jossa **Yritys**-kenttä on tyhjä ja **On asiakas** -kentän arvo on **Ei** ja **On toimittaja** -kentän arvo on **Ei**.

## <a name="contact-for-party"></a>Osapuolen yhteyshenkilö

**Osapuolen yhteyshenkilö** tallentaa ja käsittelee **Tili**-rivien ja **Yhteyshenkilö**-rivien väliset N:N-suhteet. Se voi suodattaa pois merkityt **Yhteyshenkilö**-rivit merkitsemättömistä riveistä ja liittää vain merkitsemättömät **Yhteyshenkilö**-rivit **Tili**- tai **Toimittaja**-riveille.

Esimerkiksi Natasha Jones ja Miguel Reyes ovat eläinlääkäreitä, jotka tarjoavat hoitoa omien alueidensa maatiloille. Natasha palvelee Seattlen alueella ja Miguel Kentin alueella. Asiakasvuorovaikutussovelluksessa maatiloja edustavat asiakkaat ja eläinlääkäreitä yhteyshenkilöt. Natashan yksi **yhteyshenkilö**-tietue liittyy kaikkiin maatiloihin, joissa Natasha työskentelee. Samoin yksi Miguelin **yhteyshenkilö**-tietue liittyy kaikkiin maatiloihin, joissa Miguel työskentelee.

Nämä suhteet tallennetaan **Osapuolen yhteyshenkilö** -tauluun. Tiedot löytyvät käyttövalmiista lomakkeista:

+ Kun olet **Tili**-lomakkeessa, siinä on välilehti nimeltä **Liitetyt yhteyshenkilöt**. Tämän välilehden avulla voit liittää **Tili**-riviin yhteyshenkilöitä. Tässä lomakkeessa määritetään organisaation yhteyshenkilö. Kun olet määrittänyt yhteyshenkilöt, voit valita yhden yhteyshenkilön kyseisen tilin ensisijaiseksi yhteyshenkilöksi. **Pikaluontilomakkeen** avulla voit valita vain yhteyshenkilön. Toiminta on sama, kun käytät **Toimittaja**-lomaketta ja tietuetyyppinä on **Organisaatio**.
+ Kun olet **Yhteyshenkilö**-lomakkeessa ja rivi on asiakas tai toimittaja tai molemmat (merkitty yhteyshenkilö), on olemassa **Liitetyt yhteyshenkilöt** -välilehti. Tämän välilehden avulla voit liittää yhteyshenkilöitä. Tässä lomakkeessa määritetään yhteyshenkilö B2C-asiakkaalle ta toimittajalle. Kun olet määrittänyt yhteyshenkilöt, voit valita yhden yhteyshenkilön ensisijaiseksi yhteyshenkilöksi. **Pikaluontilomakkeen** avulla voit valita vain yhteyshenkilön.
+ Kun olet **Yhteyshenkilö**-lomakkeessa ja rivi on yhteyshenkilö (merkitsemätön yhteyshenkilö), on olemassa **Liitetyt organisaatiot** -välilehti. Tämän välilehden avulla voit liittää asiakkaita tai toimittajia. Tässä lomakkeessa määritetään asiakas tai toimittaja taustalla olevaan yhteyshenkilöön. Asiakas tai toimittaja voi olla organisaatio, henkilö tai molemmat. Voit valita neljästä kentästä vain yhden arvon kerrallaan.

    ![Liitetyt organisaatiot -välilehti](media/party-gab-image3.png)

    + Jos valitset **Osapuolen tunnus**, pohjana oleva yhteyshenkilö liitetään kaikkiin valitun osapuolen rooleihin.
    + Jos valitset **Liitetty yhteyshenkilö**, valitset henkilö-tyyppiä olevan merkityn yhteyshenkilön.
    + Jos valitset **Liitetty tili** tai **Toimittaja**, valitset organisaation.

    Riippumatta valinnastasi liitos luodaan osapuolen tasolla, ja se koskee kaikkia osapuolen rooleja ja tallennetaan Osapuolen yhteyshenkilö -entiteettiin.

> [!Note]
> Asiakasvuorovaikutussovellukessa **Osapuolen yhteyshenkilö** -taulun näyttönimi on **Asiakkaan/toimittajan yhteyshenkilö**.

Kun avaat **yhteyshenkilö**-rivin, jossa on **On asiakas** on **Ei** ja **On toimittaja** on **Ei**, näet **Liitetyt organisaatiot** -välilehden. Tämän välilehden avulla voit liittää yhteyshenkilöön yhden tai useampia asiakas- tai toimittajaorganisaatioita.

Kun avaat **yhteyshenkilö**-rivin, jossa on **On asiakas** on **Kyllä** tai **On toimittaja** on **Kyllä**, näet **Liitetyt yhteyshenkilöt** -välilehden. Tämän välilehden avulla voit liittää yhden tai useampia yhteyshenkilöitä.

## <a name="postal-address"></a>Postiosoite

**Tili**-, **Yhteyshenkilö**- ja **Toimittaja**-lomakkeissa on uusi välilehti nimeltä **Osoitteet**. Tässä kuvassa näkyy **Osoitteet**-kohdan tukemien N osoitteiden ruudukko:

![Postiosoitteen ruudukko](media/party-gab-image4.png)

+ **Postiosoitteen roolit** -sarakkeessa luetellaan osoitteen tarkoitus.
+ Ensisijainen osoite näkyy **On ensisijainen** -sarakkeessa.
+ **Osoitenumero**-sarake sisältää osoitteiden järjestyksen.
+ **+Uusi osoite** -painikkeella voit luoda uuden osoitteen. Voit luoda tarvittavan määrän osoitteita.

**Tili**-lomakkeen **Yhteenveto**-välilehden **Osoite 1**- ja **Osoite 2**-kentät vastaavat **toimitus**- ja **laskutusosoitteita**.

![Postiosoitteen Yhteenveto-välilehti](media/party-gab-image5.png)

**Yhteyshnekilö**-lomakkeen **Yhteenveto**-välilehden **Osoite 1**-, **Osoite 2**- ja **Osoite 3** -kentät vastaavat **yritys**-, **toimitus**- ja **laskutusosoitteita**.

## <a name="electronic-address"></a>Sähköinen osoite

**Tili**-, **Yhteyshenkilö**- ja **Toimittaja**-lomakkeissa on uusi välilehti nimeltä **Sähköiset osoitteet**. Tässä kuvassa näkyy **Osoitteet**-kohdan tukemien N osoitteiden ruudukko:

![Sähköisen osoitteen ruudukko](media/party-gab-image6.png)

+ **Tyyppi**-sarakkeessa näkyy osoitteen tyyppi.
+ Ensisijainen osoite näkyy **On ensisijainen** -sarakkeessa.
+ **Tarkoitus** -sarakkeessa luetellaan sähköisen osoitteen tarkoitus.
+ **+Uusi sähköinen osoite** -painikkeella voit luoda uuden osoitteen. Voit luoda tarvittavan määrän osoitteita.

Sähköiset osoitteet ovat käytettävissä vain tässä ruudukossa. Tulevissa versioissa kaikki sähköisen osoitteen ja postiosoitteen kentät poistetaan muista välilehdistä, esimerkiksi **Yhteenveto**- ja **Tiedot**-välilehdistä.

## <a name="setup-instructions"></a>Määritysohjeet

Jos olet jo kaksoiskirjoituksen asiakas, seuraavat määritysohjeet ovat pakollisia. Muussa tapauksessa voit ohittaa tämän osion.

1. Pysäytä seuraavat yhdistämiset, koska niitä ei tarvita enää. Suorita sen sijaan Yhteyshenkilöt V2 (msdyn_contactforparties) -yhdistämismääritys.

    + CDS-yhteyshenkilöt V2 ja yhteyshenkilöt (viittaa asiakkaan yhteyshenkilöihin)
    + CDS-yhteyshenkilöt V2 ja yhteyshenkilöt (viittaa toimittajan yhteyshenkilöihin)

2. Osapuolitoimintojen seuraavat yksiköiden yhdistämismääritykset päivitetään, joten uusin versio on otettava käyttöön näissä yhdistämismäärityksissä.

Yhdistämismääritys | Päivitä tähän versioon | Muutokset
---|---|---
Asiakkaat V3 (accounts) | 1.0.0.5 |Poistaa PartyNumber-kentän ja muut osapuoleen liittyvät kentät, kuten nimen, henkilökohtaiset tiedot, postiosoitekentät ja sähköisen osoitteen kentät jne.
Asiakas V3 (contacts) | 1.0.0.5 | Poistaa PartyNumber-kentän ja muut osapuoleen liittyvät kentät, kuten nimen, henkilökohtaiset tiedot, postiosoitekentät ja sähköisen osoitteen kentät jne.
Toimittajat V2 (msdyn_vendors) | 1.0.0.6 | Poistaa PartyNumber-kentän ja muut osapuoleen liittyvät kentät, kuten nimen, henkilökohtaiset tiedot, postiosoitekentät ja sähköisen osoitteen kentät jne.
CDS-myyntitarjouksen otsikot (quotes) | 1.0.0.6 | Korvasi yhteyshenkilön ContactforParty-viitteellä.
Myyntilaskun otsikot V2 (invoices) | 1.0.0.4 | Korvasi yhteyshenkilön ContactforParty-viitteellä.
CDS-myyntitilauksen otsikot (salesorders) | 1.0.0.5 | Korvasi yhteyshenkilön ContactforParty-viitteellä.
Yhteyshenkilöt V2 (msdyn_contactforparties) | 1.0.0.2 | Tämä on uusi yhdistämismääritys. Jos sinulla on osapuoliratkaisun edellinen versio, muista päivittää tämä yhdistämismääritys uusimpaan versioon.
CDS-osapuolen postiosoitesijainnit (msdyn_partypostaladdresses) | 1.0.0.1  | Tämä on uusi määritys, joka on lisätty osana edellisen osapuolen esiversiojulkaisua.
CDS-postiosoitehistoria V2 (msdyn_postaladdresses) | | Tämä on uusi määritys, joka on lisätty osana edellisen osapuolen esiversiojulkaisua.
CDS-postiosoitesijainnit (msdyn_postaladdresscollections) | | Tämä on uusi määritys, joka on lisätty osana edellisen osapuolen esiversiojulkaisua.
Osapuolen yhteyshenkilöt V3 (msdyn_partyelectronicaddresses) | | Tämä on uusi määritys, joka on lisätty osana tätä julkaisua.

## <a name="templates"></a>Mallit

Taulujen yhdistämisten kokoelma toimii yhdessä osapuolen ja yleisen osoitekirjan vuorovaikutusta seuraavan taulukon mukaisesti.

Finance and Operations -sovellus | Asiakkaiden aktivointisovellus     | kuvaus
----------------------------|-----------------------------|------------
[Yhteyshenkilöiden arvonimet](mapping-reference.md#223) | msdyn_salescontactpersontitles |
[Asiakkaat V3](mapping-reference.md#101) | tilit |
[Asiakkaat V3](mapping-reference.md#116) | yhteyshenkilöt |
[CDS-osapuolet](mapping-reference.md#220) | msdyn_parties |
[CDS-osapuolen postiosoitteiden sijainnit](mapping-reference.md#233) | msdyn_partypostaladdresses |
[CDS-osapuolen postiosoitteen historia V2](mapping-reference.md#235) | msdyn_postaladdresses |
[CDS-postiosoitteiden sijainnit](mapping-reference.md#234) | msdyn_postaladdresscollections |
[CDS-myyntitarjouksen otsikko](mapping-reference.md#215) | tarjoukset |
[CDS-myyntitilauksien otsikot](mapping-reference.md#217) | salesorders |
[Loppusanat](mapping-reference.md#222) | msdyn_complimentaryclosings |
[Yhteyshenkilöt V2](mapping-reference.md#221) | msdyn_contactforparties |
[Päätöksentekoroolit](mapping-reference.md#224) | msdyn_decisionmakingroles |
[Työsuhteen työtehtävät](mapping-reference.md#225) | msdyn_employmentjobfunctions |
[Kanta-asiakastasot](mapping-reference.md#226) | msdyn_loyaltylevels |
[Osapuolen yhteyshenkilöt V3](mapping-reference.md#236) | msdyn_partyelectronicaddresses |
[Henkilökohtaisten luonteenpiirteiden tyypit](mapping-reference.md#227) | msdyn_personalcharactertypes |
[Myyntilaskun otsikot V2](mapping-reference.md#118) | laskut |
[Tervehdykset](mapping-reference.md#228) | msdyn_salutations |
[Toimittajat V2](mapping-reference.md#202) | msdyn_vendors |

Lisätietoja on [kaksoiskirjoituksen yhdistämismäärityksen viitteessä](mapping-reference.md).
