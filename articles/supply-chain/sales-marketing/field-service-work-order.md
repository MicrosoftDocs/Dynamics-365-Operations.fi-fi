---
title: Field Servicen työtilausten synkronointi Supply Chain Managementin myyntitilauksiin
description: Tässä ohjeaiheessa käsitellään malleja ja taustalla olevia tehtäviä, joilla Field Servicen työtilaukset synkronoidaan Supply Chain Managementin myyntitilauksiin.
author: Henrikan
ms.date: 04/09/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: henrikan
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: b7b311701aff12d58392fc036d0f1174678b7dc3
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/31/2022
ms.locfileid: "8061306"
---
# <a name="synchronize-work-orders-in-field-service-to-sales-orders-in-supply-chain-management"></a>Field Servicen työtilausten synkronointi Supply Chain Managementin myyntitilauksiin

[!include[banner](../includes/banner.md)]



Tässä ohjeaiheessa käsitellään malleja ja taustalla olevia tehtäviä, joilla Dynamics 365 Field Servicen työtilaukset synkronoidaan Dynamics 365 Supply Chain Managementin myyntitilauksiin.

[![Liiketoimintaprosessien synkronointi Supply Chain Managementin ja Field Servicen välillä.](./media/field-service-integration.png)](./media/field-service-integration.png)


## <a name="templates-and-tasks"></a>Mallit ja tehtävät

Field Servicen työtilaukset synkronoidaan Supply Chain Managementin myyntitilauksiin seuraavien mallien ja taustalla olevien tehtävien avulla.

### <a name="names-of-the-templates-in-data-integration"></a>Mallien nimet tietojen integroinnissa

Synkronointi tehdään **Työtilauksista myyntitilauksiin (Field Servicestä Supply Chain Managementiin)** -mallin avulla.

### <a name="names-of-the-tasks-in-the-data-integration-project"></a>Tietojen integrointiprojektin tehtävien nimet

- WorkOrderHeader
- WorkOrderServiceLineEstimate
- WorkOrderServiceLineUsed
- WorkOrderProductLineEstimate
- WorkOrderProductLineUsed

Seuraavat synkronointitehtävät tarvitaan, ennen kuin myyntitilausten otsikot ja rivit voidaan synkronoida:

- Field Service -tuotteet (Supply Chain Managementista Field Serviceen)
- Asiakkaat (Salesista Supply Chain Managementiin) - suora

## <a name="entity-set"></a>Yksikköjoukko

| **Field Service** | **Toimitusketjun hallinta** |
|-------------------------|-------------------------|
| msdyn_workorders        | Dataversen myyntitilauksen otsikot |
| msdyn_workorderservices | Dataversen myyntitilausrivit   |
| msdyn_workorderproducts | Dataversen myyntitilausrivit   |

## <a name="entity-flow"></a>Yksikön työnkulku

Työtilaukset luodaan Field Servicessä. Jos työtilaukset sisältävät vain ulkoisesti ylläpidettäviä tuotteita ja jos **Työtilauksen tila** -arvo on jokin muu kuin **Avoin - ajoittamaton** ja **Suljettu - peruutettu**, työtilaukset voidaan synkronoida Supply Chain Managementiin Microsoft Dataverse -tietojen integrointiprojektin kautta. Työtilausten päivitykset synkronoidaan myyntitilauksina Supply Chain Managementissa. Nämä päivitykset sisältävät tietoja alkuperän tyypistä ja tilasta.

## <a name="estimated-versus-used"></a>Ennakkolasketun ja käytetyn vertailu

Field Servicessä työtilausten tuotteiden ja huoltojen määrillä ja summilla on sekä **Ennakkolaskettu**- että **Käytetty**-arvot. Supply Chain Managementin myyntitilauksissa ei kuitenkaan ole vastaavia **Ennakkolaskettu**- ja **Käytetty**-arvoja. Jotta Supply Chain Managementin myyntitilauksen odotettua määrää käyttävää tuotekohdistusta voitaisiin käyttää samalla, kun kulutettavan ja laskutettavan määrän käyttö olisi mahdollista, työtilauksen tuotteiden ja huoltojen synkronointiin käytetään kahta tehtäväjoukkoa. Yksi tehtäväjoukko käsittelee **Ennakkolaskettu**-arvoja ja toinen **Käytetty**-arvoja.

Tämän toiminnan ansiosta voidaan käyttää skenaarioita, joissa kohdistamiseen tai varaamiseen Supply Chain Managementissa käytetään ennakkolaskettuja arvoja, kun taas käytettyjä arvoja käytetään kulutukseen ja laskutukseen.

### <a name="estimated"></a>Ennakkolaskettu

Tuoterivien synkronoinnissa käytetään **Ennakkolaskettu**-arvoja, kun **Rivin tila** -arvo on **Ennakkolaskettu**, **Kohdistettu**-asetukseksi on valittu **Kyllä** ja **Järjestelmän tila** -arvo ei ole **Suljettu - kirjattu**.

Huoltorivien synkronoinnissa käytetään **Ennakkolaskettu**-arvoja, kun **Rivin tila** -arvo on **Ennakkolaskettu** ja **Järjestelmän tila** -arvo ei ole **Suljettu - kirjattu**.

### <a name="used"></a>Käytetty

**Käytetty**-arvoja käytetään kulutuksessa ja laskutuksessa. Näissä tapauksissa **Käytetty**-arvot synkronoidaan.

Seuraavassa taulukossa on yhteenveto erilaisten tuoterivien yhdistelmistä.

| Järjestelmän tila <br>(Field Service) | Rivin tila <br>(Field Service) | Kohdistettu <br>(Field Service) |Synkronoitu arvo <br>(Supply Chain Management) |
|--------------------|-------------|-----------|---------------------------------|
| Avoin - ajoitettu   | Ennakkolaskettu   | Kyllä       | Ennakkolaskettu                       |
| Avoin - ajoitettu   | Ennakkolaskettu   | Ei        | Käytetty                            |
| Avoin - ajoitettu   | Käytetty        | Kyllä       | Käytetty                            |
| Avoin - ajoitettu   | Käytetty        | Ei        | Käytetty                            |
| Avoin - käsittelyssä | Ennakkolaskettu   | Kyllä       | Ennakkolaskettu                       |
| Avoin - käsittelyssä | Ennakkolaskettu   | Ei        | Käytetty                            |
| Avoin - käsittelyssä | Käytetty        | Kyllä       | Käytetty                            |
| Avoin - käsittelyssä | Käytetty        | Ei        | Käytetty                            |
| Avoin - valmis   | Ennakkolaskettu   | Kyllä       | Ennakkolaskettu                       |
| Avoin - valmis   | Ennakkolaskettu   | Ei        | Käytetty                            |
| Avoin - valmis   | Käytetty        | Kyllä       | Käytetty                            |
| Avoin - valmis   | Käytetty        | Ei        | Käytetty                            |
| Suljettu - kirjattu    | Ennakkolaskettu   | Kyllä       | Käytetty                            |
| Suljettu - kirjattu    | Ennakkolaskettu   | Ei        | Käytetty                            |
| Suljettu - kirjattu    | Käytetty        | Kyllä       | Käytetty                            |
| Suljettu - kirjattu    | Käytetty        | Ei        | Käytetty                            |

Seuraavassa taulukossa on yhteenveto erilaisten huoltorivien yhdistelmistä.

| Järjestelmän tila <br>(Field Service) | Rivin tila <br>(Field Service) | Synkronoitu arvo <br>(Supply Chain Management) |
|--------------------|-------------|-----------|
| Avoin - ajoitettu   | Ennakkolaskettu   | Ennakkolaskettu |
| Avoin - ajoitettu   | Käytetty        | Käytetty      |
| Avoin - käsittelyssä | Ennakkolaskettu   | Ennakkolaskettu |
| Avoin - käsittelyssä | Käytetty        | Käytetty      |
| Avoin - valmis   | Ennakkolaskettu   | Ennakkolaskettu |
| Avoin - valmis   | Käytetty        | Käytetty      |
| Suljettu - kirjattu    | Ennakkolaskettu   | Käytetty      |
| Suljettu - kirjattu    | Käytetty        | Käytetty      |

Tuote- ja huoltorivien **Ennakkolaskettu**- ja **Käytetty**-arvojen synkronointia hallitaan kahdella tehtäväjoukolla. Ennalta määritetyt suodattimet käynnistävät oikean tehtävän ja taustalla tehtävä yhdistämismääritys varmistaa, että oikeat **Odotettu**- ja **Käytetty**-arvot synkronoidaan.

### <a name="example"></a>Esimerkki

1. Työtilaus luodaan ja ajoitetaan Field Servicessä.

    **Järjestelmän tila** -arvo on **Avoin - ajoitettu**.

    - **Tuoterivi:** Ennakkolaskettu määrä = 5 kpl, Käytetty määrä = 0 kpl, Rivin tila = ennakkolaskettu, Kohdistettu = ei
    - **Huoltorivi:** Ennakkolaskettu määrä = 2 h, Käytetty määrä = 0 h, Rivin tila = ennakkolaskettu

    Tässä esimerkissä tuotteen **Käytetty määrä** -arvo **0** (nolla) ja huollon **Ennakkolaskettu määrä** **2 h** synkronoidaan Supply Chain Managementiin.

2. Tuotteet kohdistetaan Field Servicessä.

    **Järjestelmän tila** -arvo on **Avoin - ajoitettu**.

    - **Tuoterivi:** Ennakkolaskettu määrä = 5 kpl, Käytetty määrä = 0 kpl, Rivin tila = ennakkolaskettu, Kohdistettu = kyllä
    - **Huoltorivi:** Ennakkolaskettu määrä = 2 h, Käytetty määrä = 0 h, Rivin tila = ennakkolaskettu

    Tässä esimerkissä tuotteen **Ennakkolaskettu määrä** -arvo **5ea** ja huollon **Ennakkolaskettu määrä** **2 h** synkronoidaan Supply Chain Managementiin.

3. Huoltoteknikko aloittaa työtilauksen käsittelyn ja rekisteröi materiaalikäytöksi 6.

    **Järjestelmän tila** -arvo on **Avoin - käsittelyssä**.

    - **Tuoterivi:** Ennakkolaskettu määrä = 5 kpl, Käytetty määrä = 6 kpl, Rivin tila = käytetty, Kohdistettu = kyllä
    - **Huoltorivi:** Ennakkolaskettu määrä = 2 h, Käytetty määrä = 0 h, Rivin tila = ennakkolaskettu

    Tässä esimerkissä tuotteen **Käytetty määrä** -arvo **6** ja huollon **Ennakkolaskettu määrä** **2 h** synkronoidaan Supply Chain Managementiin.

4. Huoltoteknikko suorittaa työtilauksen loppuun ja rekisteröi käytetyksi ajaksi 1,5 tuntia.

    **Järjestelmän tila** -arvo on **Avoin - valmis**.

    - **Tuoterivi:** Ennakkolaskettu määrä = 5 kpl, Käytetty määrä = 6 kpl, Rivin tila = käytetty, Kohdistettu = kyllä
    - **Huoltorivi:** Ennakkolaskettu määrä = 2 h, Käytetty määrä = 1,5 h , Rivin tila = käytetty

    Tässä esimerkissä tuotteen **Käytetty määrä** -arvo **6** ja palvelun **Käytetty määrä** **1,5 h** synkronoidaan Supply Chain Managementiin.

## <a name="sales-order-origin-and-status"></a>Myyntitilauksen alkuperä ja tila

### <a name="sales-origin"></a>Myynnin alkuperä

Voit seurata Supply Chain Managementissa työtilauksista peräisin olevia myyntitilauksia luomalla myynnin alkuperän, jossa **Alkuperän tyypin määritys** -asetukseksi on valittu **Kyllä** ja **Myynnin alkuperän tyyppi** -kentässä on valittu **Työtilauksen integrointi**.

Yhdistämismääritys valitsee myynnin alkuperäksi oletusarvoisesti **Työtilauksen integrointi** -asetuksen myynnin alkuperän tyypin kaikille työtilauksille luoduille myyntitilauksille. Tämä on kätevää, jos käsittelet myyntitilauksia Supply Chain Managementissa. Muista varmistaa, että työtilauksista peräisin olevia myyntitilauksia ei synkronoida takaisin Field Serviceen työtilauksina.

Lisätietoja oikean myynnin alkuperän luomisesta Supply Chain Managementissa on tämän ohjeaiheen kohdassa Edellytykset ja yhdistämismääritykset.

### <a name="status"></a>Tila

Kun myyntitilaus on peräisin työtilauksesta, myyntitilauksen ylätunnisteen **Asetukset**-välilehdessä näkyy **Ulkoisen työtilauksen tila** -kenttä. Tässä kentässä näkyy työtilauksen tila Field Servicessä, mikä auttaa seuraamaan myyntitilausten synkronoitujen työtilausten tilaa Supply Chain Managementissa. Lisäksi käyttäjä voi määrittää tämän kentän avulla, milloin myyntitilaus on toimitettava tai laskutettava.

**Ulkoisen työtilauksen tila** -kentän arvo voi olla jokin seuraavista:

- Avoin - ajoitettu
- Avoin - käsittelyssä
- Avoin - valmis
- Suljettu - kirjattu

## <a name="field-service-crm-solution"></a>Field Service CRM -ratkaisu

Field Servicen ja Supply Chain Managementin integraation tukemiseen tarvitaan Field Service CRM -ratkaisun lisätoiminto. Ratkaisu sisältää seuraavat muutokset.

### <a name="work-order-entity"></a>Työtilaus-yksikkö

**Tarjous sisältää vain ulkoisesti ylläpidettyjä tuotteita** -kenttä on lisätty **Työtilaus**-yksikköön ja näkyy sivulla. Sen avulla voi seurata, että työtilaus koostuu pelkästään ulkoisesti ylläpidetyistä tuotteista. Työtilauksessa on vain ulkoisesti ylläpidettyjä tuotteita, kun kaikkia liittyviä tuotteita ylläpidetään Supply Chain Managementissa. Tämä kenttä auttaa varmistamaan, että käyttäjät eivät yritä synkronoida sellaisia työtilauksia, joissa on tuntemattomia tuotteita.

### <a name="work-order-product-entity"></a>Työtilauksen tuote -yksikkö

- **Tilaus sisältää vain ulkoisesti ylläpidettyjä tuotteita** -kenttä on lisätty **Työtilauksen tuote** -yksikköön ja näkyy sivulla. Sen avulla voidaan seurata, ylläpidetäänkö työtilauksen tuotetta yhdenmukaisesti Supply Chain Managementissa. Tämä kenttä auttaa varmistamaan, että käyttäjät eivät yritä synkronoida sellaisia työtilauksen tuotteita, joissa on tuotteita, joita Supply Chain Management ei tunne.
- **Ylätunnisteen järjestelmän tila** -kenttä on lisätty **Työtilauksen tuote** -yksikköön ja näkyy sivulla. Sen avulla voidaan seurata työtilauksen järjestelmän tilaa yhdenmukaisesti ja varmistaa oikea suodatus, kun työtilauksen tuotteet synkronoidaan Supply Chain Managementiin. Kun integraatiotehtävien suodattimet määritettään, **Ylätunnisteen järjestelmän tila** -tietojen avulla määritetään myös, synkronoidaanko ennakkolasketut vai käytetyt arvot.
- **Laskutettu yksikkösumma** -kentässä on summa, joka on laskutettu käytetyn todellisen yksikön mukaan. Arvo lasketaan jakamalla **Loppusumma**-arvo **Toteutunut määrä** -arvolla. Kenttää käytetään integroimaan järjestelmät, jotka eivät tue eri arvoja käytetylle ja laskutetulle määrälle. Tämä kenttä ei näy käyttöliittymässä. 
- **Laskutettu alennussumma** -kenttä lasketaan **Alennussumma**-arvona, johon lisätään laskettu **Laskutettu yksikkösumma** -arvo pyöristettynä. Kenttää käytetään integraatioon eikä se näy käyttöliittymässä.
- **Desimaalien määrä** -kenttään tallennetaan **Määrä**-kentän arvo desimaalilukuna. Kenttää käytetään integraatioon eikä se näy käyttöliittymässä. 
- **Käytetty**-kenttien arvoksi palautetaan **0** (nolla), jos työtilauksen tuotteen **Rivin tila** -arvo **Käytetty** muutetaan arvoksi **Ennakkolaskettu**. Tämä muutos auttaa estämään tilanteet, jossa vahingossa annettua käytettyä määrää käytetään synkronoitaessa, kun **Rivin tila** -arvo on **Ennakkolaskettu** ja **Kohdistettu**-asetukseksi on valittu **Ei**.

### <a name="work-order-service-entity"></a>Työtilauksen huolto -yksikkö

- **Tilaus sisältää vain ulkoisesti ylläpidettyjä tuotteita** -kenttä on lisätty **Työtilauksen huolto** -yksikköön ja näkyy sivulla. Sen avulla voidaan seurata, ylläpidetäänkö työtilauksen palvelua yhdenmukaisesti Supply Chain Managementissa. Tämä kenttä auttaa varmistamaan, että käyttäjät eivät yritä synkronoida sellaisia työtilauksen palveluita, joita Supply Chain Management ei tunne.
- **Ylätunnisteen järjestelmän tila** -kenttä on lisätty **Työtilauksen huolto** -yksikköön ja näkyy sivulla. Sen avulla voidaan seurata työtilauksen järjestelmän tilaa yhdenmukaisesti ja varmistaa oikea suodatus, kun työtilauksen palvelut synkronoidaan Supply Chain Managementiin. Kun integraatiotehtävien suodattimet määritettään, **Ylätunnisteen järjestelmän tila** -tietojen avulla määritetään myös, synkronoidaanko ennakkolasketut vai käytetyt arvot.
- **Kesto tunteina** -kenttään tallennetaan **Kesto**-kentän arvo sen jälkeen, kun arvo on muutettu minuuteista tunneiksi. Kenttää käytetään integraatioon eikä se näy käyttöliittymässä.
- **Arvioitu kesto tunteina** -kenttään tallennetaan **Arvioitu kesto** -kentän arvo sen jälkeen, kun arvo on muutettu minuuteista tunneiksi. Kenttää käytetään integraatioon eikä se näy käyttöliittymässä.
- **Laskutettu yksikkösumma** -kenttään on tallennettu summa, joka on laskutettu käytetyn todellisen yksikön mukaan. Arvo lasketaan jakamalla **Loppusumma**-arvo **Toteutunut määrä** -arvolla. Tätä kenttää käytetään integroimaan järjestelmät, jotka eivät tue eri arvoja käytetylle ja laskutetulle määrälle. Kenttä ei näy käyttöliittymässä.
- **Laskutettu alennussumma** -kenttä lasketaan **Alennussumma**-arvona, johon lisätään laskettu **Laskutettu yksikkösumma** -arvo pyöristettynä. Kenttää käytetään integraatioon eikä se näy käyttöliittymässä.
- **Ulkoinen rivitilaus** -kenttä on laskettu negatiivinen rivitilausnumero, jota käytetään sellaisissa ulkoisissa järjestelmissä, joissa työtilauksen tuote- ja huoltorivit yhdistetään. Tämän kentän ansiosta lisätyillä työtilauksen tuotteilla voi olla positiiviset rivinumerot ja työtilauksen huolloilla voi olla negatiiviset rivinumerot. Tämä kentän arvo lasketaan kertomalla **Rivitilaus**-arvo luvulla -1. Tämä kenttä ei näy käyttöliittymässä.
- **Käytetty**-kenttien arvoksi palautetaan **0** (nolla), jos työtilauksen huollon **Rivin tila** -arvo **Käytetty** muutetaan jostain syystä arvoksi **Ennakkolaskettu**. Tämä muutos auttaa estämään tilanteet, jossa vahingossa annettua käytettyä määrää käytetään synkronoitaessa, kun **Rivin tila** -arvo on **Ennakkolaskettu** ja **Ylätunnisteen järjestelmän tila**-arvo on **Suljettu - kirjattu**.

## <a name="preconditions-and-mapping-setup"></a>Edellytykset ja yhdistämismääritykset

Seuraavat asetukset on päivitettävä järjestelmissä ennen työtilausten synkronointia.

### <a name="setup-in-field-service"></a>Field Servicen asetukset

- Varmista, että Field Servicen työtilauksissa käytettävä numerosarja ei ole päällekkäinen Supply Chain Managementin myyntitilauksessa käytettävän numerosarjan kanssa. Jos näin on, aiemmin luodut myyntitilaukset voivat päivittyä virheellisesti Field Servicessä tai Supply Chain Managementissa.
- **Työtilauksen laskun luonti** -kentän asetuksena on oltava **Ei koskaan**, koska laskutus tehdään Supply Chain Managementissa. Valitse **Field Service** \> **Asetukset** \> **Hallinto** \> **Field Servicen asetukset** ja varmista, että **Työtilauksen laskun luonti** -kentässä on valittu **Ei koskaan**.

### <a name="setup-in-supply-chain-management"></a>Määritys Supply Chain Managementissa

Työtilauksen integraatio edellyttää, että myynnin alkuperä määritetään. Myynnin alkuperän avulla Field Servicen työtilauksista luodut myyntitilaukset voidaan erottaa Supply Chain Managementissa. Kun myyntitilauksen myynnin alkuperätyyppi on **Työtilauksen integrointi**, myyntitilauksen ylätunnisteessa on **Ulkoisen työtilauksen tila** -kenttä. Myynnin alkuperä auttaa varmistamaan, että Field Servicen työtilauksista luodut myyntitilaukset suodatetaan pois synkronoitaessa myyntitilausta Supply Chain Managementista Field Serviceen.

1. Valitse **Myynti ja markkinointi** \> **Asetukset** \> **Myyntitilaukset** \> **Myynnin alkuperä**.
2. Luo uusi myynnin alkuperä valitsemalla **Uusi**.
3. Anna **Myynnin alkuperä** -kentässä myynnin alkuperän nimi, kuten **Työtilaus**.
4. Kirjoita **Kuvaus**-kenttään kuvaus, kuten **Field Servicen työtilaus**.
5. Valitse **Alkuperän tyypin määritys** -valintaruutu.
6. Valitse **Myynnin alkuperän tyyppi** -kentässä **Työtilauksen integrointi**.
7. Valitse **Tallenna**.


### <a name="setup-in-data-integration"></a>Määritys tietojen integroinnissa

Varmista, että **Integrointiavain** on olemassa kohteelle **msdyn_workorders**
1. Siirry tietojen integrointiin
2. Valitse **Yhteysjoukko**-välilehti
3. Valitse yhteysjoukko, jota käytetään työtilauksen synkronointiin
4. Valitse **Integrointiavain**-välilehti
5. Etsi msdyn_workorders ja tarkista, että avain **msdyn_name (työtilauksen numero)** on lisätty. Jos avainta ei näy, lisää se napsauttamalla **Lisää avain** ja **Tallenna** sivun yläosassa

## <a name="template-mapping-in-data-integration"></a>Mallin yhdistäminen tietojen integroinnin yhteydessä

Seuraavissa kuvissa on esimerkki mallin yhdistämisestä tietojen integroinnin yhteydessä.

### <a name="work-orders-to-sales-orders-field-service-to-supply-chain-management-workorderheader"></a>Työtilauksista myyntitilauksiksi (Field Servicesta Supply Chain Managementiin): WorkOrderHeader

Suodata: (msdyn_systemstatus ne 690970005) ja (msdyn_systemstatus ne 690970000) ja (msdynce_hasexternallymaintainedproductsonly eq true)

[![Työtilauksista myyntilaukseen integroitavien tietojen mallin yhdistämismääritys (Field Servicesta Supply Chain Managementiin): WorkOrderHeader.](./media/FSWorkOrder1.png )](./media/FSWorkOrder1.png)

### <a name="work-orders-to-sales-orders-field-service-to-supply-chain-management-workorderservicelineestimate"></a>Työtilauksista myyntitilauksiksi (Field Servicesta Supply Chain Managementiin): WorkOrderServiceLineEstimate

Suodata: (msdynce_headersystemstatus ne 690970005) ja (msdynce_headersystemstatus ne 690970000) ja (msdynce_orderhasexternalmaintainedproductsonly eq true) ja (msdyn_linestatus eq 690970000) ja (msdynce_headersystemstatus ne 690970004)

[![Työtilauksista myyntilaukseen integroitavien tietojen mallin yhdistämismääritys (Field Servicesta Supply Chain Managementiin): WorkOrderServiceLineEstimate.](./media/FSWorkOrder2.png )](./media/FSWorkOrder2.png)

### <a name="work-orders-to-sales-orders-field-service-to-supply-chain-management-workorderservicelineused"></a>Työtilauksista myyntitilauksiksi (Field Servicesta Supply Chain Managementiin): WorkOrderServiceLineUsed

Suodata: (msdynce_headersystemstatus ne 690970005) ja (msdynce_headersystemstatus ne 690970000) ja (msdynce_orderhasexternalmaintainedproductsonly eq true) ja ((msdyn_linestatus eq 690970001) tai (msdynce_headersystemstatus eq 690970004))

[![Työtilauksista myyntilaukseen integroitavien tietojen mallin yhdistämismääritys (Field Servicesta Supply Chain Managementiin): WorkOrderServiceLineUsed.](./media/FSWorkOrder3.png )](./media/FSWorkOrder3.png)

### <a name="work-orders-to-sales-orders-field-service-to-supply-chain-management-workorderproductlineestimate"></a>Työtilauksista myyntitilauksiksi (Field Servicesta Supply Chain Managementiin): WorkOrderProductLineEstimate

Suodata: (msdynce_headersystemstatus ne 690970005) ja (msdynce_headersystemstatus ne 690970000) ja (msdynce_orderhasexternalmaintainedproductsonly eq true) ja (msdyn_linestatus eq 690970000) ja (msdynce_headersystemstatus ne 690970004) ja (msdyn_allocated eq true)

[![Työtilauksista myyntilaukseen integroitavien tietojen mallin yhdistämismääritys (Field Servicesta Supply Chain Managementiin): WorkOrderProductLineEstimate.](./media/FSWorkOrder4.png )](./media/FSWorkOrder4.png)

### <a name="work-orders-to-sales-orders-field-service-to-supply-chain-management-workorderproductlineused"></a>Työtilauksista myyntitilauksiksi (Field Servicesta Supply Chain Managementiin): WorkOrderProductLineUsed

Suodata: (msdynce_headersystemstatus ne 690970005) ja (msdynce_headersystemstatus ne 690970000) ja (msdynce_orderhasexternalmaintainedproductsonly eq true) ja ((msdyn_linestatus eq 690970001) tai (msdynce_headersystemstatus eq 690970004) tai (msdyn_allocated ne true))

[![Työtilauksista myyntilaukseen integroitavien tietojen mallin yhdistämismääritys (Field Servicesta Supply Chain Managementiin): WorkOrderProductLineUsed.](./media/FSWorkOrder5.png )](./media/FSWorkOrder5.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]