---
title: Dayforceen integroinnin määritys
description: Microsoft Dynamics 365 Human Resourcesin ja Ceridian Dayforcen välinen integrointi käyttää useita konfiguraation vaiheita, jotka on kuvattu tässä artikkelissa. Sekä Human Resourcesin että Dayforcen integrointi on määritettävä ennen kuin voit käsitellä palkka-ajoa.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: PersonnelIntegrationConfiguration
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 044a2d2f632b2c98ce94b6d61c2582a861640b68
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/03/2021
ms.locfileid: "5112364"
---
# <a name="configure-integration-with-dayforce"></a>Dayforceen integroinnin määritys

Microsoft Dynamics 365 Human Resourcesin ja Ceridian Dayforcen välinen integrointi käyttää useita konfiguraation vaiheita, jotka on kuvattu tässä artikkelissa. Sekä Human Resourcesin että Dayforcen integrointi on määritettävä ennen kuin voit käsitellä palkka-ajoa.

Käytettäessä jotakin palvelua, kuten Dayforcea palkka-ajojen suorittamiseen, on otettava käyttöön integrointi Human Resourcesissa. Integrointi edellyttää tiettyjä tietoja Human Resourcesista. Sinun on varmistettava, että Dayforceen yhdistetyt tiedot on konfiguroitu Human Resourcesissa siten, että ne tukevat integrointia. Integraatio käyttää seuraavanlaisia laajoja tietoryhmiä:

- Henkilöstöhallintotiedot
- Kompensaatiotiedot
- Palkanlaskentatietoja, kuten maksujaksot, maksukaudet ja ansiokoodit
- Työntekijän tiedot

Tässä artikkelissa kuvataan vaiheita, joita sinun on noudatettava ottaaksesi integroinnin käyttöön. Lisäksi kerrotaan minkä tyyppisiä tietoja ja konfigurointitietoja integrointi edellyttää.

## <a name="enable-the-integration"></a>Ota integraatio käyttöön

Ota integraatio käyttöön Human Resourcesissa ja lisää konfiguraatiotiedot muodostaaksesi yhteyden Dayforceen. Mikäli haluat kirjanpitotapahtuman, joka valmistetaan ja tuodaan Microsoft Dynamics 365 Financeen, sinun on määritettävä myös Microsoft Azure -tallennustili ja kirjoitettava Azure-tallennuksen yhteyden muodostuskomento Financeen.

Ota integrointi käyttöön Human Resourcesissa seuraavien vaiheiden mukaan.

1. Valitse **Järjestelmänvalvoja**-sivulla **konfiguroinnin integrointi**.
2. Lisää File Transfer Protocol (FTP) -päätepiste ja suojattu FTP-kansiopolku.
3. Kirjoita sen käyttäjän käyttäjänimi ja salasana, joka voi käyttää suojattua FTP-päätepistettä ja kansiopolkua.
4. Testaa yhteys kuten vaadittu ja määritä **Ota käyttöön palkanmaksun integrointi** -asetukseksi **Kyllä**.

Kun integrointi otetaan käyttöön, tietojen viennin paketti ja tiedostot luodaan ja taajuus määritetään. Voit muuttaa tätä taajuutta tarpeen mukaan.

Lisätietoja Azure-tallennustilien ja Azure-tallennusyhteyden yhteysmerkkijonoista seuraavissa Azure-artikkeleissa:

- [Lisätietoja Azure-tallennustileistä](https://docs.microsoft.com/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [Määritä Azure-tallennustilan yhteysmerkkijonot](https://docs.microsoft.com/azure/storage/common/storage-configure-connection-string)

### <a name="technical-details-when-payroll-integration-is-enabled"></a>Tekniset tiedot, kun palkanlaskennan integrointi on otettu käyttöön

Palkanlaskennan integroinnin käytöstäpoistamisella on kaksi pääasiallista vaikutusta:

- Palkanlaskennan integroinnin vienti -niminen tietojen vientiprojekti luodaan. Tämä projekti sisältää palkanhallinnan integrointiin tarvittavat yksiköt ja kentät. Voit tutustua projektiin valitsemalla ensin **Järjestelmän hallinta**, sitten **Tietojen hallinta** -ruudun ja avaamalla lopuksi tietoprojektin projektiluettelosta.
- Tämä erätyö suorittaa tietojen vientiprojektin, salaa tuloksena olevan tietopaketin ja siirtää tietopakettitiedoston SFTP-päätepisteeseen, joka on määritetty **Integroinnin määritys** -näytössä.

> [!NOTE]
> SFTP-päätepisteeseen siirretty tietopaketti salataan paketin yksilöllisellä avaimella. Avain on Azure Key Vaultissa, jota vain Ceridian voi käyttää. Tietopaketin sisällön salausta ei voi purkaa eikä sisältöä tutkia. Jos tietopaketin sisältöä on tarkasteltava, Palkanlaskennan integroinnin vienti -tietoprojekti on vietävä manuaalisesti, jonka jälkeen on ladattava ja avattava. Manuaalisessa viennissä ei käytetä salausta eikä pakettia siirretä.

## <a name="configure-your-data"></a>Määritä tietosi 

Voidaksesi käsitellä palkanlaskentaa, sinun on määritettävä henkilöstöhallinnon tiedot Human Resourcesissa. On määritettävä organisaation tiedot, kuten työt ja toimet sekä edut ja kompensaatiotiedot. Nämä tiedot sisältävät työllisyys-, palkka- ja vähennystiedot, jotka vaaditaan, jotta voidaan luoda työntekijän palkka.

### <a name="human-resource-data"></a>Henkilöstöhallintotiedot

#### <a name="benefits"></a>Edut 

Henkilöstöhallinto sisältää työkaluja, joiden avulla organisaation tarjoamia tai työntekijöitä varten käsittelemiä etuja, vähennyksiä ja työntekijöiden kompensaatiosuunnitelmia voi määrittää ja ylläpitää.

Luodessasi etuja, pidä mielessä seuraavat tiedot ja konfiguraatiot, joita käytetään Dayforcessa.

##### <a name="benefit-plans"></a>Etusuunnitelmat

- Suunnitelma (pakollinen)
- Tyyppi (pakollinen)
- Palkanlaskennan vaikutus (pakollinen)
- Palauta velvoitteet
- Vähennysmenetelmä
- Vähennyksen prioriteetti
- Rajaa kausi
- Rajasumma

##### <a name="benefits"></a>Edut

- Suunnitelma (pakollinen)
- Tyyppi (pakollinen)
- Vaihtoehto (pakollinen)
- Edun tunnus (pakollinen)
- Tiheys
- Peruste
- Summa tai hinta
- Ansiokoodi

##### <a name="supported-frequencies"></a>Tuetut maksutiheydet 

- Viikoittain
- Kahden viikon välein
- Joka toinen kuukausi
- Kuukausittain

##### <a name="supported-bases"></a>Tuetut pohjat 

- Kiinteä summa
- Ansioiden prosenttiosuus
- Tuottavat tunnit

Dayforce luo seuraavat vähennykset, jotka perustuvat palkanlaskennan vaikutukseen, joka on määritelty etusuunnitelmassa.

| Valinta Human Resourcesissa        | Tulos Dayforcessa                            |
|----------------------------|-----------------------------------------------|
| Ei ole                       | Vähennyksiä ei luoda.                      |
| Vain vähennys             | Työntekijävähennys on luotu.             |
| Vain osuus          | Työnantajavähennys on luotu.             |
| Vähennys ja osuus | Työntekijän ja työnantajan vähennykset luodaan. |

Lisätietoja etuohjelman määrittämisestä ja hallitsemisesta seuraavissa artikkeleissa:

- [Työsuhde-etuusohjelman toteuttaminen](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [Luo uusi etu](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [Määritä edun oikeutussäännöt ja -käytännöt](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [Rekisteröi etuja työntekijöille ja poista niitä](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a>Kompensaatio 

Kompensaationhallinnan avulla ohjataan peruspalkan ja palkkioiden maksamista. Työntekijän kiinteän peruspalkan ja bonusten korotuksia hallitaan kiinteän kompensaatiosuunnitelmien avulla. Bonusmaksujen, suorituskykypalkkioiden, optioiden, lahjoitusten sekä muiden kannusteiden maksamista hallitaan muuttuvan kompensaation suunnitelmien avulla.

Dayforce käyttää kompensaatiotietoja laskeakseen työntekijän tunti- tai vuosihinnan. Kiinteät kompensaatiosuunnitelmat ja palkkojen muunnokset vaaditaan. Työntekijöiden täytyy olla liitettynä kiinteään kompensaatiosuunnitelmaan.

Katso lisätietoja kompensaatiosuunnitelmista seuraavista artikkeleista:

- [Kiinteiden kompensaatiosuunnitelmien luominen](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [Muuttuvien kompensaatiosuunnitelmien luominen](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [Palkka- ja kompensaatiorakenteen ja -suunnitelmien kehittäminen](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [Kompensaation käsittely](https://docs.microsoft.com/dynamics365/unified-operations/talent/process-compensation)
- [Kompensaatioprosessin määrittäminen ja tulosten laskeminen](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [Työntekijän rekisteröiminen kiinteän kompensaation suunnitelmaan](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [Työntekijän rekisteröiminen muuttuvan kompensaation suunnitelmaan](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a>Työt 

Työ sisältää tehtäviä ja vastuita, joita työn suorittajalta edellytetään. Lisätietoja on seuraavissa artikkeleissa:

- [Työn komponenttien määrittäminen](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-job)
- [Uusien töiden määrittäminen](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a>Toimet

Toimi on työn yksittäinen esiintymä. Esimerkiksi toimi Myyntipäällikkö (Itä) on yksi Myyntipäällikkö-työhön liittyvistä toimista. Osastolla on toimi. Vain yksi työntekijä voidaan liittää yhteen toimeen.

Muista seuraavat tiedot ja määritykset, kun määrität toimia:

- Toimi (pakollinen)
- Kuvaus (pakollinen)
- Työ (pakollinen)
- Osasto (pakollinen)
- Toimen tyyppi (pakollinen)
- Kokopäiväinen (FTE)
- Vuosittaiset vakiotunnit (pakollinen)
- Yrityksen maksama (pakollinen)
- Maksujakson (pakollinen)
- Oletusarvo taloushallinnon dimensio – kustannuspaikka (pakollinen)
- Työntekijän määritys – työntekijä, tehtävän alkamisaika, tehtävän lopetusaika, syykoodi

Mikäli useita toimia samalla osastolla liittyy samaan työhön, ne yhdistetään yhteen toimeen Dayforcessa.

Lisätietoja on seuraavissa artikkeleissa:

- [Työvoiman järjestäminen osastojen, töiden ja toimien avulla](https://docs.microsoft.com/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [Toimien määritys](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a>Osastot

Osasto on toimintayksikkö, joka vastaa organisaation luokkaa tai liiketoiminta-aluetta. Osasto on vastuussa määrätystä organisaation alueesta, kuten myynnistä, kirjanpidosta tai henkilöstöhallinnosta. Voit käyttää osastoja toiminnallisia alueita koskevaan raportointiin. Osastot voivat olla tulosvastuullisia.

Lisätietoja on seuraavissa artikkeleissa:

- [Osaston luominen ja liittäminen osastohierarkiaan](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [Määritä uudet osastot](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a>Maksujaksot ja maksukaudet

Palkkajakso määrittää kuinka usein palkkalistoja käytetään, ja minä tiettyinä päivinä työntekijöille maksetaan. Esimerkiksi palkkajakso voi olla kuukausittainen ja työntekijöille voidaan maksaa kuukauden viimeisenä päivänä. Vaihtoehtoisesti palkkajakso voi olla viikoittainen ja työntekijöille voidaan maksaa tiistaina palkkajakson päätyttyä. Palkkajaksot on osoitettu toimiin, jotta voidaan valvoa milloin näissä tehtävissä oleville työntekijöille maksetaan.

Luotuasi palkkajaksoja, voit luoda maksukausia kullekin jaksolle. Jokaisella palkkakaudella on maksun oletuspäivämäärä, joka perustuu antamiisi tietoihin. Voit kuitenkin muokata maksun oletuspäivämäärää salliaksesi poikkeuksia, kuten kun maksupäivämäärä osuu vapaapäivälle.

Dayforcessa käytetään seuraavia tietoja:

- Maksujakson (pakollinen)
- Maksujakson tiheys (pakollinen)
- Kauden alkamispäivä (ensimmäinen palkkakausi vaaditaan)
- Oletusmaksupäivä (ensimmäinen palkkakausi vaaditaan)

Nämä tiedot on integroitu Dayforce-palkkaryhmien kanssa ja eriteltynä eriteltyinä maittain tai alueittain kullekin maksujaksolle. Ennen integraatiota on luotava vähintään yksi palkkakausi. Dayforce luo maksuryhmäkalentereita ja maksupäiviä, jotka perustuvat ensimmäisen palkkakauden alkamispäivämäärään ja määritetty oletusmaksupäivä on asetettu Human Resourcesissa.

#### <a name="earning-codes"></a>Ansiokoodit

Ansiokoodit tunnistavat yksilöllisesti kaikentyyppiset ansiot, joita työntekijät saavat. Tunnuksissa on erilaisia parametreja, jotka liittyvät tuloihin, kuten kirjanpitosäännöt, verolait, raportointivaatimukset ja ylöspäin bruttotehokkuus.

Dayforcessa käytetään seuraavia tietoja:

- Ansiokoodi (pakollinen)
- kuvaus
- Mittayksikkö
- Tuottava

### <a name="worker-data"></a>Työntekijän tiedot

Tietueet eri työntekijöille, joita sinulla on ovat tärkeitä henkilöstöhallinnossa ja palkanlaskentajärjestelmissä. Tietueisiin lisättäviä tietoja käytetään työntekijöiden ja henkilökohtaisten tietojen seurannassa.

Voit ylläpitää työntekijöille seuraavia tietoja:

- **Perustiedot** – Ylläpidä työntekijän perustietoja, kuten yhteystiedot, demografiatiedot, tunnistetiedot, perheen tiedot, asevelvollisuuden tila, ekspatriaatin tiedot ja omat yhteyshenkilöt ja hätäyhteyshenkilöt.
- **Työsuhde** – Ylläpidä tietoja työntekijän työsuhteesta, kuten yrityksen tai organisaation kytköksistä, toimen määrityksestä, aloitus- ja päättymispäivämääristä, työkelpoisuudesta, työehdoista, eläkkestä, lomista ja uudelleensijoittumisesta.
- **Lomat ja poissaolot** –Ylläpidä tietoa työntekijän poissaoloista, kuten työaikakalentereista, poissaolotapahtumista ja poissaoloasetuksista.
- **Kompensaatio ja palkanlaskenta** – Ylläpidä työntekijän kompensaatiosuunnitelmien tietoja ja palkanlaskentatietoja, kuten suunnitelmien toteutuminen, palkkiot, suorituskyky, provisio, verotiedot, eläkkeelle jääminen ja palkan vähennykset.

Kirjoittaessasi työntekijätietoja, pidä mielessä seuraavat tiedot ja konfiguraatiot, joita käytetään Dayforcessa.

#### <a name="general-information"></a>Yleistiedot

- Henkilönumero (pakollinen)
- Etunimi (pakollinen)
- Sukunimi (pakollinen)
- Toinen nimi
- Ikälisäpäivä
- Tunnetaan nimellä

#### <a name="personal-information"></a>Henkilökohtaiset tiedot

- Siviilisääty (pakollinen)
- Syntymäpäivä (pakollinen)
- Sukupuoli (pakollinen)
- Henkilö on invalidi
- Kansalaisuus, maa, alue (vain Meksikossa)

#### <a name="address-information"></a>Osoitetiedot

- Ensisijainen (pakollinen)
- Maa/alue (pakollinen)
- Postinumero (pakollinen)
- Kadunnumero (pakollinen) (vain Meksikossa)
- Rakennusta koskeva lisätieto (vain Meksikossa)
- Kaupunki (pakollinen)
- Alue (pakollinen)
- Lääni (pakollinen)

#### <a name="contact-information"></a>Yhteystiedot 

- Ensisijainen (pakollinen)
- Yhteystiedon numero (pakollinen)
- Alanumero

#### <a name="payroll-information-and-earning-codes"></a>Palkanlaskentatiedot ja ansiokoodit

Työntekijöille voidaan antaa erityisiä tuloja tietyllä maksutaajuudella ja toivotulla maksutavalla. Seuraavia kenttiä käytetään Dayforcessa sen varmistamiseksi, että näitä määrityksiä ja asetuksia käytetään.

##### <a name="earning-codes"></a>Ansiokoodit

- Toimi (pakollinen)
- Ansiokoodi (pakollinen)
- Taajuus (pakollinen)
- Summa (pakollinen)

##### <a name="payroll-information"></a>Palkanlaskentatiedot

- Maksutapa
- Talousalue (pakollinen)
- Työsuhde-etujen tunnus
- Kansallinen/alueellinen tunnusnumero (pakollinen)
- Sotilaspalveluksen numero
- Vuoron tunnus (pakollinen)
- Veronumero (pakollinen)
- Ammattijärjestön tunnus (pakollinen)
- Työpäivän tunnus (pakollinen)
- Työluvan numero

> [!NOTE]
> Maksutavoista Meksiko tukee seuraavia: **Käteinen**, **shekki** (yrityksen fyysinen shekki) ja **sähköinen maksu**. Mikäli maksutapaa ei ole määritetty, **shekki** on oletusarvo.

#### <a name="employment-details"></a>Työsuhteen tiedot

Työntekijöiden yksityiskohtaista historiaa käytetään keskeisenä informaationa, jolla saadaan työntekijän palkkaus, irtisanominen ja rekrytointitilastot Dayforcesta. Dayforce tukee kerrallaan vain yhtä aktiivisen työntekijän tietuetta.

- Työsuhteen alkamispäivä (pakollinen)
- Työsuhteen päättymispäivämäärä
- Aloituspäivämäärä
- Muutettu aloituspäivämäärä
- Työsuhteen päättymispäivä (pakollinen päättyessä)
- Työsuhteen päättymissyy (pakollinen päättyessä)

Seuraavien tietojen avulla lasketaan työntekijän tärkeimmät päivämäärät.

| Henkilöstö                | Dayforce                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| Viimeisimmän työhönoton päivämäärä | Työntekijän työsuhteen alku voimassa olevassa työhistoriatietueessa                                 |
| Työsuhteen loppumispäivämäärä      | Työntekijän työsuhteen loppu voimassa olevassa työhistoriatietueessa                                 |
| Aloituspäivämäärä            | Muutettu alkamispäivämäärä, alkamispäivämäärä tai työsuhteen alku ei-aktiivisessa työsuhteen historiatietueessa |
| Alkuperäinen työsuhteen alkamispäivämäärä    | Varhaisin työhistoriatietueen työsuhteen alku                                               |

#### <a name="compensation"></a>Kompensaatio

Kiinteän kompensaatiosuunnitelmaan tulee liittää jokaisen työntekijän ensisijainen toimi koko työsuhteen ajalla. Ajanjakso alkaa siitä päivämäärästä, jona työntekijä palkattiin (tai työsuhteen alkamispäivämäärä) ja jatkuu, kunnes työsuhde loppuu.

- Voimaantulopäivä (pakollinen)
- Vanhentumispäivä
- Palkkio (pakollinen)
- Palkkion muunnokset (pakollinen)
- Vuosittainen arvo (pakollinen)
- Tunnittainen arvo (pakollinen)

Mikäli tuntityöntekijällä on useita toimia, ensisijaisen toimen kiinteä kompensaation tuodaan Dayforceen työntekijätason hinta-/peruspalkkana. Ei-ensisijaisten toimien tuntihinta tallennetaan Dayforcen vastaavaan sijaintiin.

Mikäli palkallisella työntekijällä on useita toimia, kumulatiivinen tuntihinta ja vuosittainen palkka kaikista aktiivisista toimista johdetaan ja käytetään työntekijätason hinta-/peruspalkkana.

#### <a name="identification-numbers"></a>Tunnusnumerot

##### <a name="social-security-identifier"></a>Sosiaaliturvan tunniste 

Jokaisella työntekijä on oltava yksi ensisijainen tunnus. Tunnuksen on oltava **SSN**-tunnus. Dayforcessa se johdetaan automaattisesti työntekijän sosiaaliturvatunnuksesta, jota tarvitaan työsuhdetta solmittaessa.

- Ensisijainen (pakollinen)
- Tunnuksen tyyppi = "Henkilötunnus"
- Myöntämispäivämäärä
- Vanhentumispäivä

Työntekijät voi määrittää useita tunnistenumeroita **SSN**-tunnuksesta (henkilötunnus). Tietue, joka on merkitty **Ensisijainen** on integroitu Dayforceen, riippumatta siitä, onko numero aktiivinen tai vanhentunut.

#### <a name="bank-accounts-and-disbursements"></a>Pankkitilit ja suoritukset

Voimassa olevat pankkitilitiedot on kirjattava kaikille työntekijöille, jotka haluavat, että hänelle maksetaan pankkisiirtona.

| Henkilöstö                         | Dayforce                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| Pankkitilin numero (pakollinen) |                                                                                                             |
| SWIFT-koodi (pakollinen)          | **Pankkitunnus**-kenttä, jota käytetään, kun käsitellään palkkalistoja Meksikossa.                                                             |
| Sivuliikkeen numero (pakollinen)       |                                                                                                             |
| Pankkitilin tyyppi (pakollinen)   | **Tilityyppi**-kenttä, jota käytetään, kun käsitellään palkkalistoja Meksikossa. Tuetut arvot sisältävät kohdat **Tarkistus** ja **Palkanlaskenta**. |

> [!NOTE]
> Työntekijät, jotka haluavat, että heille maksetaan pankkisiirtona, on toimitettava linkki jäännöstilille, joka kuuluu oikeushenkilölle, jolla on ensisijainen osoite Meksikossa ja jolla on voimassa oleva tili meksikolaisessa pankissa. Kaikki muut jäljellä olevat tilit jätetään huomiotta.

#### <a name="address-information"></a>Osoitetiedot

Jokaisella työntekijällä on oltava yksi ensisijainen toimipaikka. Dayforcessa tätä sijaintia käytetään määrittämään työntekijän ensisijainen oleskelulupa verotusta varten.

- Ensisijainen (pakollinen)
- Maa/alue (pakollinen)
- Postinumero (pakollinen)
- Katuosoite (pakollinen)
- Kadunnumero (pakollinen)
- Rakennusta koskeva lisätieto
- Kaupunki (pakollinen)
- Alue (pakollinen)
- Lääni (pakollinen)

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a>Määritä tiedot luodaksesi palkkalistoja Yhdysvalloissa ja Kanadassa

Jos luot maksuja työntekijöille, jotka ovat Yhdysvalloissa ja Kanadassa, seuraavat seikat on määritettävä:

- Toimia varten vaaditaan osastot.
- Kustannuspaikat on määritettävä taloushallinnon dimensioina ja niiden pitää olla ensimmäisenä osana merkkijonoa oletusarvoisessa taloushallinnon dimensiossa.

> [!NOTE] 
> Voit määrittää Human Resourcesin edellyttämään, että toimet määrittävät osaston. Tehdäksesi tämän valitse **Henkilöstöhallinnon jaetut toimet > Toimet > Edellytä osastoja toimissa**. Suosittelemme, että tämä asetus otetaan käyttöön integrointia varten.

### <a name="job-types"></a>Työtyypit

Työtyyppien avulla voi luokitella samankaltaisia töitä. Työlajit ovat pakollisia palkanlaskennan käsittelemiseksi Yhdysvalloissa ja Kanadassa. Työtyypit ovat: kokopäiväinen ja osa-aikainen sekä kuukausipalkka tai tuntipalkka. Työlajit on yhdistetty Dayforceen maksulajeina, jotka ilmaisevat, onko työntekijällä tuntipalkka vai kuukausipalkka.

Tarvitaan seuraavat työlajit ja kuvaukset.

| Työlaji   | kuvaus |
|------------|-------------|
| Tunneittain     | Tunneittain      |
| Kuukausipalkka   | Kuukausipalkka    |

### <a name="position-types"></a>Toimityypit 

Voit käyttää toimityyppejä kuvaamaan, onko toimi kokoaikainen, osa-aikainen vai jokin muu. Toimityypit on yhdistetty Dayforceen maksuluokkina, jotka ilmaisevat, onko työntekijä koko- vai osa-aikainen.

Tarvitaan seuraavat toimityypit ja kuvaukset.

| Toimityyppi   | kuvaus        |
|-----------------|--------------------|
| Kokoaikainen       | Kokopäiväinen työntekijä |
| Osa-aikainen       | Osapäiväinen työntekijä |

### <a name="reason-codes"></a>Syykoodit

Syykoodit antavat tietoja työntekijän tilasta Syykoodit määritetään Dayforceen tilan syinä, jotka ilmaisevat muutokset työntekijän toimessa tai työsuhteessa.

Tarvitaan seuraavat syykoodit ja kuvaukset.

| Syykoodi    | kuvaus      | Soveltuvat skenaariot |
|----------------|------------------|----------------------|
| EROAMINEN    | Eroaminen      | Irtisano työntekijä     |
| IRTISANOMINEN    | Irtisanominen      | Irtisano työntekijä     |
| ELÄKKEELLE SIIRTYMINEN     | Eläkkeelle siirtyminen       | Irtisano työntekijä     |
| MUU          | Muut syyt    | Irtisano työntekijä     |
| KUOLEMA          | Kuolema            | Irtisano työntekijä     |
| LEAVEOFABSENCE | Virkavapaa | Irtisano työntekijä     |
| CONTRACTEND    | Sopimuksen päättyminen  | Irtisano työntekijä     |
| SALARYCHANGE   | Palkan muutos | Kompensaatio         |

### <a name="marital-status"></a>Siviilisääty

Siviilisääty on liitetty Dayforceen ja käännetty tarvittaessa integraatiolle hyväksyttyihin arvoihin.

Seuraavassa taulukossa kuvataan, miten siviilisääty liitetään Dayforceen.

| Henkilöstö                 | Dayforce             |
|------------------------|----------------------|
| Naimisissa                | Naimisissa              |
| Yksi                 | Yksi               |
| Leski                | Leski              |
| Eronnut               | Eronnut             |
| Rekisteröity suhde | Kotimainen kumppanuus |
| None                   | None                 |
| Avoliitossa             | Avoliitossa           |

### <a name="gender"></a>Sukupuoli

Sukupuolinimitykset on liitetty Dayforceen ja käännetty tarvittaessa integraatiolle hyväksyttyihin arvoihin.

Seuraavassa taulukossa kuvataan, miten sukupuolinimitykset liitetään Dayforceen.

| Henkilöstö       | Dayforce        |
|--------------|-----------------|
| Mies         | Mies            |
| Nainen       | Nainen          |
| Yksilöimätön | *Ei tueta* |

### <a name="earning-codes"></a>Ansiokoodit

Ansiokoodit tunnistavat yksilöllisesti kaikentyyppiset ansiot, joita työntekijät saavat. Tunnukset kattavat erilaisia parametreja, jotka liittyvät tuloihin, kuten kirjanpitosäännöt, verolait, raportointivaatimukset ja ylöspäin bruttotehokkuus. Mikäli käytetään ei-tuettua taajuutta **Jokainen palkka** -taajuutta käytetään oletusarvon mukaan laskelmissa.

#### <a name="supported-frequencies"></a>Tuetut maksutaajuudet

- Kaikki
- EVERYPAY
- EACHPAYPERIOD
- EVRYOTHRPAYODD
- EVRYOTHRPAYEVN
- 1OFMTH
- LASTOFMTH
- 2OFMTH
- 3OFMTH
- 4OFMTH
- 5OFMTH
- 1N2OFMTH
- 3N4OFMTH
- 1N3OFMTH
- 1N4OFMTH
- 2N3OFMTH
- 2N4OFMTH
- 1N2N3OFMTH
- 1N2N4OFMTH
- 1N3N4OFMTH
- 2N3N4OFMTH
- 1N2N3N4OFMTH - 1N2N3N4OFMTH
- 2N3N4N5OFMth - 2N3N4N5OFMth
- 1OFQTR - 1OFQTR
- LASTOFQTR – LASTOFQTR
- LASTMTHOFQTR – LASTMTHOFQTR
- 1OFYEAR - 1OFYEAR
- LASTOFYEAR – LASTOFYEAR
- NOVNDECOFYEAR - NOVNDECOFYEAR

### <a name="addresses"></a>Osoitteet

Määriteltyjen maiden tai alueiden, valtioiden ja läänin (kuntien) koodien tunnistaminen edellyttää tiettyjä muotoja, joita Dayforce ja maassa tai alueella olevat toimijat pystyvät tunnistamaan. Vaikka kaupunkien muoto on joustava, jokainen paikkakunta täytyy liittää osavaltioon.

| Henkilöstö          | Dayforce              |
|-----------------|-----------------------|
| Maa/alue  | Maakoodi          |
| Postinumero | Postinumero           |
| Alue           | Aluekoodi            |
| Paikkakunta            | Paikkakunta                  |
| Piirikunta          | Lääni (kunta) |
| Katu          | Osoiterivi 1        |

### <a name="tax-regions"></a>Verotusalueet

Verotusalueita käytetään palkanlaskennan muodostamisessa käytettävän veron määrittämiseen. ALV-alueet yhdistetään Dayforceen toimipaikan osoitteina. Oletusarvoinen verotusalue on liitettävä työntekijän aktiiviseen toimeen. 

- Verotusalue (pakollinen)
- Maa/alue (pakollinen)
- Alue (pakollinen)
- Piirikunta 
- Kaupunki (pakollinen)

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a>Määritä tietosi tuottaaksesi palkkalistoja Meksikossa

Jos luot maksuja työntekijöille, jotka ovat Meksikossa, seuraavat seikat on määritettävä:

- Toimia varten vaaditaan osastot.
- Kustannuspaikat on määritettävä taloushallinnon dimensioina ja niiden pitää olla ensimmäisenä osana merkkijonoa oletusarvoisessa taloushallinnon dimensiossa.

### <a name="job-types"></a>Työtyypit

Työtyyppien avulla voi luokitella samankaltaisia töitä. Työlajit ovat pakollisia palkkalistojen käsittelemiseen Meksikossa. Työtyypit ovat: kokopäiväinen ja osa-aikainen sekä kuukausipalkka tai tuntipalkka. Työlajit on yhdistetty Dayforceen maksulajeina, jotka ilmaisevat, onko työntekijällä tuntipalkka vai kuukausipalkka.

Tarvitaan seuraavat työlajit ja kuvaukset.

| Työlaji   | kuvaus |
|------------|-------------|
| Tunneittain     | MX tunneittain   |
| Kuukausipalkka   | MX kuukausipalkka |

### <a name="position-types"></a>Toimityypit 

Voit käyttää toimityyppejä kuvaamaan, onko toimi kokoaikainen, osa-aikainen vai jokin muu. Toimityypit on yhdistetty Dayforceen maksuluokkina, jotka ilmaisevat, onko työntekijä koko- vai osa-aikainen.

Tarvitaan seuraavat toimityypit ja kuvaukset.

| Toimityyppi   | kuvaus        |
|-----------------|--------------------|
| Kokoaikainen       | Kokopäiväinen työntekijä |
| Osa-aikainen       | Osapäiväinen työntekijä |

### <a name="reason-codes"></a>Syykoodit

Syykoodit antavat tietoja työntekijän tilasta Syykoodit määritetään Dayforceen tilan syinä, jotka ilmaisevat muutokset työntekijän toimessa tai työsuhteessa.

Tarvitaan seuraavat syykoodit ja kuvaukset.

| Syykoodi            | kuvaus                    | Soveltuvat skenaariot |
|------------------------|--------------------------------|----------------------|
| DEPARTUREBEFOREPAYMENT | Lähtö ennen ensimmäistä palkanlaskentaa | Irtisano työntekijä     |
| EROAMINEN            | Eroaminen                    | Irtisano työntekijä     |
| ELÄKE                | Eläke                        | Irtisano työntekijä     |
| IRTISANOMINEN            | Irtisanominen                    | Irtisano työntekijä     |
| ELÄKKEELLE SIIRTYMINEN             | Eläkkeelle siirtyminen                     | Irtisano työntekijä     |
| ABSENTEE               | Absentee                       | Irtisano työntekijä     |
| MUU                  | Muut syyt                  | Irtisano työntekijä     |
| SULKEMINEN                | Liiketoiminnan sulkeminen               | Irtisano työntekijä     |
| KUOLEMA                  | Kuolema                          | Irtisano työntekijä     |
| LEAVEOFABSENCE         | Virkavapaa               | Irtisano työntekijä     |
| CONTRACTEND            | Sopimuksen päättyminen                | Irtisano työntekijä     |
| SALARYCHANGE           | Palkan muutos               | Kompensaatio         |

### <a name="terms-of-employment"></a>Työehdot

Työehtoja voidaan käyttää, kun luodaan työehtoluokkia. Ehdot määritetään Dayforceen työsuhteen mittarin arvoina.

Seuraavat työsuhteen ja kuvaukset termit ovat pakollisia.

| Työehdot   | kuvaus |
|-----------------------|-------------|
| Säännöllinen               | Säännöllinen     |
| Suora                | Suora      |
| Harjoittelujakso            | Harjoittelujakso  |
| Pysyvä             | Pysyvä   |

### <a name="marital-status"></a>Siviilisääty

Siviilisääty on liitetty Dayforceen ja käännetty tarvittaessa integraatiolle hyväksyttyihin arvoihin.

Seuraavassa taulukossa kuvataan, miten siviilisääty liitetään Dayforceen.

| Henkilöstö                 | Dayforce                  |
|------------------------|---------------------------|
| Naimisissa                | Naimisissa                   |
| Yksi                 | Yksi                    |
| Leski                | Leski                   |
| Eronnut               | Eronnut                  |
| Rekisteröity suhde | Kotimainen kumppanuus      |
| None                   | *Meksiko ei tue tyyppiä* |
| Avoliitossa             | *Meksiko ei tue tyyppiä* |

### <a name="gender"></a>Sukupuoli

Sukupuolinimitykset on liitetty Dayforceen ja käännetty tarvittaessa integraatiolle hyväksyttyihin arvoihin.

Seuraavassa taulukossa kuvataan, miten sukupuolinimitykset liitetään Dayforceen.

| Henkilöstö       | Dayforce                  |
|--------------|---------------------------|
| Mies         | Mies                      |
| Nainen       | Nainen                    |
| Yksilöimätön | *Meksiko ei tue tyyppiä* |

### <a name="payment-method"></a>Maksutapa

Maksutavat antavat työntekijälle ja yritykselle keinon kuvata, miten työntekijöille maksetaan. Maksutavat on liitetty Dayforceen ja käännetty tarvittaessa integraatiolle hyväksyttyihin arvoihin.

Seuraavassa taulukossa kuvataan, miten maksutavat liitetään Dayforceen.

| Henkilöstö             | Dayforce                  |
|--------------------|---------------------------|
| Maksu               | Maksu                      |
| Sähköinen maksu | Tapahtumien siirto                  |
| Tarkistus              | Sekki                    |
| Pankkivekseli         | *Meksiko ei tue tyyppiä* |
| Muu              | *Meksiko ei tue tyyppiä* |

### <a name="bank-account-type"></a>Pankkitilin tyyppi

Pankkitilin tyyppejä käytetään sähköisissä maksuissa työntekijöille. Pankin tilityypit yhdistetään Dayforceen tilinsiirtämisen tietoina. Pankkitilin tyypit ovat tarvittaessa käännettyjä ja hyväksytty arvoiksi sen jälkeen.

| Henkilöstö            | Dayforce                  |
|-------------------|---------------------------|
| Käyttötili  | CheckingAccount           |
| Palkanlaskennan tili   | PayrollAccount            |
| Säästötili   | *Meksiko ei tue tyyppiä* |
| BankGirot-tili | *Meksiko ei tue tyyppiä* |
| PlusGirot-tili | *Meksiko ei tue tyyppiä* |

### <a name="earning-codes"></a>Ansiokoodit

Ansiokoodit tunnistavat yksilöllisesti kaikentyyppiset ansiot, joita työntekijät saavat. Tunnukset kattavat erilaisia parametreja, jotka liittyvät tuloihin, kuten kirjanpitosäännöt, verolait, raportointivaatimukset ja ylöspäin bruttotehokkuus. Mikäli käytetään ei-tuettua taajuutta **Jokainen palkka** -taajuutta käytetään oletusarvon mukaan laskelmissa.

#### <a name="supported-frequencies"></a>Tuetut maksutaajuudet

- Kaikki
- EVERYPAY
- EACHPAYPERIOD
- EVRYOTHRPAYODD
- EVRYOTHRPAYEVN
- 1OFMTH
- LASTOFMTH
- 2OFMTH
- 3OFMTH
- 4OFMTH
- 5OFMTH
- 1N2OFMTH
- 3N4OFMTH
- 1N3OFMTH
- 1N4OFMTH
- 2N3OFMTH
- 2N4OFMTH
- 1N2N3OFMTH
- 1N2N4OFMTH
- 1N3N4OFMTH
- 2N3N4OFMTH
- 1N2N3N4OFMTH - 1N2N3N4OFMTH
- 2N3N4N5OFMth - 2N3N4N5OFMth
- 1OFQTR - 1OFQTR
- LASTOFQTR – LASTOFQTR
- LASTMTHOFQTR – LASTMTHOFQTR
- 1OFYEAR - 1OFYEAR
- LASTOFYEAR – LASTOFYEAR
- NOVNDECOFYEAR - NOVNDECOFYEAR

### <a name="addresses"></a>Osoitteet

Määriteltyjen maiden tai alueiden, valtioiden ja läänin (kuntien) koodien tunnistaminen edellyttää tiettyjä muotoja, joita Dayforce ja maassa tai alueella olevat toimijat pystyvät tunnistamaan. Vaikka kaupunkien muoto on joustava, jokainen paikkakunta täytyy liittää osavaltioon.

| Henkilöstö              | Dayforce              |
|---------------------|-----------------------|
| Maa/alue      | Maakoodi          |
| Postinumero     | Postinumero           |
| Alue               | Aluekoodi            |
| Paikkakunta                | Paikkakunta                  |
| Piirikunta              | Lääni (kunta) |
| Katu              | Osoiterivi 1        |
| Kadunnumero       | Osoiterivi 2        |
| Rakennusta koskeva lisätieto | Osoiterivi 5        |

### <a name="passport-number"></a>Passin numero

Työntekijät voivat ilmoittaa passin tiedot. Tämä tietoa on **Passi**-tunnustyyppiä ja se on integroitu Dayforceen osaksi työntekijän Meksikon liittyvää tietoa.

- Tunnustyyppi = "Passi"
- Myöntämispäivämäärä
- Vanhentumispäivä

Työntekijät voi määrittää useita tunnistenumeroita **Passi**-tunnuksesta. Vain nykyiset aktiiviset passitapahtumat integroidaan Dayforceen. Mikäli kaikki passitapahtumat ovat vanhentuneet, passi, joka on viimeksi myönnetty on integroitu Dayforceen.

