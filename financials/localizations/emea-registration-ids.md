---
title: "Rekisteröintitunnukset"
description: "Tässä ohjeaiheessa on tietoja määrittämisestä ja käyttämisestä rekisteröinti tunnukset."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: DirPartTaxRegistrationSearch, LogisticsPostalAddress, TaxRegistrationLegislationTypes, TaxRegistrationType
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 264824
ms.assetid: e86f0a35-be58-4ef5-b5ab-bcfc495eaa13
ms.search.region: Global
ms.author: vlru
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 32cd09975861083b8940368ed53ae16e89bcd748
ms.lasthandoff: 03/31/2017


---

# <a name="registration-ids"></a>Rekisteröintitunnukset

Tässä ohjeaiheessa on tietoja määrittämisestä ja käyttämisestä rekisteröinti tunnukset.

Monet maat ja alueet ovat erilaiset säännökset ja vaatimukset rekisterinumerot tai tunnukset. Tässä aiheessa tarvittavat asetukset ja tuetut Rekisteröintityypit käsittelyn yhteenveto osapuolten eri Euroopan maissa ja alueilla. Kaikkia maita/alueita on niiden tukemalla erilaisia maakohtaisia toimintoja rekisterinumerot tarjoaman eri valtion virastojen liittyviä vaatimuksia. Esimerkkejä rekisterinumerot ovat verovelvollisen tunnistenumero (TIN), henkilötunnus (SSN) ja Euroopan ALV-tunnus (EU: N ALV-tunnus). Tämä toiminto tarjoaa yhtenäisen kehyksen kaikissa maissa, kaikilla alueilla ottaen huomioon Maakohtaiset vaatimukset joissakin Euroopan maissa. Seuraavissa osissa on tietoja, joita käytetään ja käsitellään rekisteröinti tunnukset yleistä kulkua.

## <a name="registration-type-creation"></a>Rekisteröinnin tyyppi luominen
Ennen kuin voit syöttää Tunnuksella, rekisterinumerot, jotka kumpikin osapuoli on erilaisia tyyppejä rekisteröinti on määritettävä. Siirry **organisaation hallinta**&gt;**yleisen osoitekirjan**&gt;**Rekisteröintityypit**&gt;**Rekisteröintityypit** sivun voi luoda ja hallita tyyppien rekisteröinti toimittajille, asiakkaille, työntekijöille ja oikeussubjektien eri maissa ja alueilla.

|Kenttä                 |kuvaus      |
|------------------------------|----------------------------|                                                                           
| Nimi                | Rekisteröintityypin nimi. |                                                                           
| kuvaus         | Rekisteröintityypin kuvaus. |
| Maa/alue      | Maan/alueen yksilöivä tunnus.|
| Veroviranomainen       | Veroviranomainen, joka liittyy rekisteröinnin tyyppi.|
| Rajoitettu:       | Rajoitus, joka koskee ALV-rekisteröinnin tyyppi laji: ei mitään, henkilö, organisaatio.|
| Muoto              | Rekisteröintityypin vahvistus muoto.|
| Voidaan päivittää      | Määritetään Rekisteröintityypin rekisterinumero voi päivittää sen jälkeen, kun se on kirjoitettu.|
| Yksilöivä              | Määritetään Rekisteröintityypin rekisterinumero on yksilöllinen. |
| Ensisijainen maalle | Osapuoli on liitetty yksi tai useita osoitteita erityisesti maan ja rekisteröinti tunnus kelpaa kaikki osoitteet, jos ensisijainen maan on nimettävä yksi osoite. Ensisijainen voi rekisteröidä vain yhden tunnuksen. Määritetään rekisteröintinumero voi syöttää vain ensisijaisen osoitteen maa. |

## <a name="assign-a-registration-type-to-a-registration-category"></a>Määritä rekisteröinti luokkaan rekisteröinti
Rekisteröinti luokka on hyväksytty avulla erityisesti maan vero-, tulli- ja muita tarkoituksia varten maa rekisteröinti tunnus. Tämän luokan määrittää kelpoisuussääntöjä erityisesti rekisteröinti tunnus (mukaan lukien tarkistusnumeroa jne.) ja osallisuuden Tunnuksella erilaisia raportteja. Sivulla **organisaation hallinta**&gt;**yleisen osoitekirjan**&gt;**Rekisteröintityypit**&gt;**rekisteröinti luokkiin** määrittäminen tietyn maan Rekisteröintityypin tuettu rekisteröinti luokkaan.

| Kenttä            | kuvaus|
|-----------------------|----------------|
| Rekisteröintityyppi     | Erityisesti rekisteröinnin Kirjoita maa tai alue.|
| Rajoitettu:         | Verorekisteröintityyppiä koskee, millaisia rajoituksia: ei mitään, henkilö, organisaatio.|
| Rekisteröintiluokka | Yksilöllisten rekisteröintien tunnus käyttämällä maassa hyväksytty. Täydellinen luettelo luokkien on tuettu-AX7.1 alla. |

## <a name="enter-registration-ids-for-global-address-book-records"></a>Kirjoita yleisen osoitekirjan tietueiden rekisteröinti tunnukset
Microsoft Dynamics-365 työvaiheiden yleisen osoitteiston (yleiseen OSOITEKIRJAAN) sisältää konsolidoidun asiakkaiden, toimittajien, yhteystiedot, liikesuhteet ja oikeussubjektien osoitetietoja. Lisätietoja saat [yleisen osoitekirjan yleistä](/dynamics365/operations/organization-administration/overview-global-address-book). Osapuolitietueet, jotka on tallennettu yleisessä osoitekirjassa voi sisältää osoitteen yksi tai useita tietueita. Näitä osoitteita käytetään eri tarkoituksiin, esimerkiksi laskutukseen tai toimitukseen. Voit määrittää asiakkaat, toimittajat, työntekijät ja oikeussubjektien osoitetietoja rekisteröinti tunnukset. Tallentaa (oikeushenkilö, toimittaja, asiakas, työntekijä) osapuoli, jolle haluat syöttää tunnus ja valitse sitten Etsi **rekisteröinti tunnukset** liittyvien osapuolten, oikeushenkilö, toimittaja, asiakas, työntekijä Avaa lomakkeen **osoitteiden hallinta** sivulla. - **ALV-rekisteröinnin** -välilehdessä **Lisää**, ja kirjoita seuraavat tiedot tietoja rekisteröinti on.

|Kenttä                |kuvaus                                                |
|---------------------|-----------------------------------------------------------|
| Rekisteröintityyppi   | Rekisteröintityypin valitun maan/alueen.     |
| Rekisteröintinumero | Osapuoli on rekisteröinti.                                |
| kuvaus         | Kuvaus rekisterinumero.               |
| Osa             | Lisätietoja rekisterinumero. |
| Myöntäjätaho      | Viranomainen, jolle on annettu rekisteröintinumero.        |
| Luontipäivämäärä         | Rekisterinumero annettu päivämäärä.              |
| Voimassa           | Rekisterinumero voimaantulopäivä.           |
| Vanhentuminen          | Rekisterinumero vanhentumispäivämäärä.          |

> [!NOTE]
> Y-tunnuksen oikeushenkilö, toimittaja, asiakas voi valita rekisteröintiä vero ALV-tunnukseen liittyvää ja osapuolen menettelyyn.

## <a name="search-for-records-by-registration-id"></a>Hae tietueita-Tunnuksella
Rekisteröinti-tunnuksen perusteella osapuolten tietueiden etsiminen on käytettävissä osapuoli, oikeushenkilö, toimittaja, asiakas ja työntekijä liittyvissä lomakkeissa. Valitse **Tunnuksella haku** avaamiseen **Tunnuksella hakuehdot** sivun. Määritä hakuehdot ja valitse **Etsi**. Järjestelmä näyttää valitut tietueet yleisen osoitekirjan ja osapuolitietueen liittyvät tyypit.

## <a name="supported-registration-categories"></a>Tuetut rekisteröinti luokkiin
Seuraavassa taulukossa on lueteltu Dynamics 365 toimintojen tuetut rekisteröinti tiedostotyypeistä. Jos osaat käyttää Microsoft Dynamics AX 2012-kenttien tunnusten rekisteröintiä, tässä taulukossa yhdistää nämä kentät myös toimintojen rekisteröinti luokkiin Dynamics-365.

| Toimintojen rekisteröinti luokkaan Dynamics 365         |Maa/alue  | Dynamics AX 2012: n termi/kenttä|
|---------------------------------------------------------------|---------------------|---------------------------------|
| ALV-tunnus                                                        | Kaikki maat, Euroopan unionin (EU)|  ALV-numero (lainsäädännölliset Verotunnus AX2012 R3-tyyppi)|
| Yrityksen tunnus (COID)                                          | Belgia, tsekki Viro Unkari Latvia Liettuan Puolan Sveitsi | Yrityksen numero (EnterpriseNumber)-rekisteröintinumero (RegNum\_W) rekisterinumero (RegNum\_W) rekisterinumero (RegNum\_W) rekisterinumero (RegNum\_W) yrityksen koodi (EnterpriseCode)-rekisteröintinumero (RegNum\_W) UID (lainsäädännölliset UID AX2012 R3-tyyppi) |
| Sivuliikkeen tunnus                                                     | Belgia            | Sivuliikkeen numeron (BranchNumber)|
| Spisová-značka (rekisterinumero, myöntävä toimisto-osa) | Tšekin tasavalta     | Lisäkuva numero (CommercialRegisterInsetNumber) pidettäville osoitteessa kaupalliset rekisteröidä kaupparekisteriin (CommercialRegisterSection) (CommercialRegister)-osassa|
| Tullin asiakastunnus                                           | Suomi | Tullin asiakasnumero (CustomsCustomerNumber\_FI)|
| INN                                                           | Venäjän federaatio| INN (lainsäädännölliset INN AX2012 R3-tyyppi)|
| RRC                                                           | Venäjän federaatio| RRC (lainsäädännölliset RRC AX2012 R3-tyyppi)|
| OKDP                                                          | Venäjän federaatio| OKDP (tyyppi lainsäädännölliset AX2012 R3-OKDP)|
| OKPO                                                          | Venäjän federaatio| OKPO (tyyppi lainsäädännölliset AX2012 R3-OKPO)|
| RCOAD                                                         | Venäjän federaatio| RCOAD (tyyppi lainsäädännölliset AX2012 R3-RCOAD)|
| OGRN                                                          | Venäjän federaatio| OGRN (tyyppi lainsäädännölliset AX2012 R3-OGRN) |
| SNILS                                                         | Venäjän federaatio| SNILS (tyyppi lainsäädännölliset AX2012 R3-SNILS)|
| CIFTS                                                         | Venäjän federaatio| CIFTS (tyyppi lainsäädännölliset AX2012 R3-CIFTS)|

Lisätietoja käsittelyssä tarvittavat edellytykset, mukaan lukien rekisteröinti tunnukset on tehtävä seuraavat tallenteet ALV-tunnuksen Lifecycle Services (LCS):

-   Aseta ALV-tunnus
-   Toimittajan ALV-tunnuksen rekisteröinti
-    Osaouolen haku ALV-tunnuksen avulla



