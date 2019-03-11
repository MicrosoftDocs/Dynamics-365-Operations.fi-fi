---
title: Rekisteröintitunnukset
description: Tässä ohjeaiheessa on tietoja rekisteröintitunnuksien määrittämisestä ja käyttämisestä.
author: ShylaThompson
manager: AnnBe
ms.date: 11/08/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DirPartTaxRegistrationSearch, LogisticsPostalAddress, TaxRegistrationLegislationTypes, TaxRegistrationType
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 264824
ms.search.region: Global
ms.author: vlru
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 7b663b9a72afdd3c2e2dcf503152f02e0b7861fd
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "350501"
---
# <a name="registration-ids"></a>Rekisteröintitunnukset

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa on tietoja rekisteröintitunnuksien määrittämisestä ja käyttämisestä.

Monilla mailla ja alueilla on eri säädökset ja vaatimukset rekisteröintinumeroiden tai -tunnusten tallentamiseen. Tässä aiheessa on yleiskatsaus tuettujen rekisteröintityyppien tarvittavista asetuksista ja käsittelystä, kun osapuolet ovat eri Euroopan maissa/alueilla. Kaikilla mailla/alueilla on omat vaatimukset tuesta erilaisille maakohtaisille toiminnoille, jotka liittyvät eri valtion virastojen antamiin rekisterinumeroihin. Esimerkkejä rekisterinumeroista ovat verovelvollisen tunnistenumero (TIN), henkilötunnus (SSN) ja Euroopan ALV-tunnus (EU VAT ID). Tämä toiminto tarjoaa yhtenäisen kehyksen kaikille maille kaikilla alueilla ottaen huomioon maakohtaiset vaatimukset joissakin Euroopan maissa. Seuraavissa osissa kuvataan rekisteröintitunnusten määrittämisessä ja käsittelyssä käytettävää yleistä tiedonkulkua.

## <a name="registration-type-creation"></a>Rekisteröintityypin luominen
Ennen rekisteröintitunnuksen määrittämistä on määritettävä tyypit erilaisille osapuoleen liittyville rekisteröintinumeroille. Siirry **Organisaation hallinta** &gt; **Yleinen osoitekirja** &gt; **Rekisteröintityypit** &gt; **Rekisteröintityypit** -sivun luodaksesi ja hallitaksesi rekisteröintityyppejä toimittajille, asiakkaille, työntekijöille ja yrityksille eri maissa/alueilla.

|Kenttä                 |kuvaus      |
|------------------------------|----------------------------|                                                                           
| Nimi                | Rekisteröintityypin nimi. |                                                                           
| kuvaus         | Rekisteröintityypin kuvaus. |
| Maa/alue      | Maan/alueen yksilöivä tunnus.|
| Veroviranomainen       | Veroviranomainen, joka liittyy rekisteröinnin tyyppiin.|
| Rajoitettu:       | Rajoitus, joka koskee verorekisteröinnin tyyppejä Ei mitään, Henkilö ja Organisaatio.|
| Muoto              | Rekisteröintityypin vahvistusmuoto.|
| Voidaan päivittää      | Määrittää, voiko rekisteröintityypin rekisteröintinumeron päivittää syöttämisen jälkeen.|
| Yksilöivä              | Määrittää, onko rekisteröintityypin rekisterinumero on yksilöllinen. |
| Ensisijainen maalle | Jos osapuoleen on liitetty yksi tai useita osoitteita tietyssä maassa ja rekisteröintitunnus kelpaa kaikkiin näihin osoitteisiin, tälle maalle on nimettävä yksi osoite ensisijaiseksi. Voit rekisteröidä vain yhden tunnuksen ensisijaiseksi. Määrittää, voiko rekisteröintinumeron syöttää vain ensisijaiselle maan osoitteelle. |

## <a name="assign-a-registration-type-to-a-registration-category"></a>Määritä rekisteröintityyppi rekisteröintiluokkaan
Rekisteröintiluokka on maan/alueen rekisteröintitunnus, joka on hyväksytty tietyssä maassa vero-, tulli- ja muita tarkoituksia varten. Tämä luokka määrittää kelpoisuussääntöjä tietylle rekisteröintitunnukselle (mukaan lukien tarkistusnumerot jne.) ja rekisteritunnuksen sisällyttämisen erilaisiin raportteihin. Sivulla **Organisaation hallinta** &gt; **Yleinen osoitekirja** &gt; **Rekisteröintityypit** &gt; **Rekisteröintiluokat** voit määrittää tietyn maan rekisteröintityypin tuettuun rekisteröintiluokkaan.

| Kenttä            | kuvaus|
|-----------------------|----------------|
| Rekisteröintityyppi     | Rekisteröintityyppi tietyssä maassa/alueessa.|
| Rajoitettu:         | Rajoitus, joka koskee verorekisteröinnin tyyppejä Ei mitään, Henkilö ja Organisaatio.|
| Rekisteröintiluokka | Yksilöllinen rekisteröintitunnus, joka on hyväksytty käyttöön kyseisessä maassa. Alla on täydellinen luettelo Microsoft Dynamics 365 for Finance and Operationsin luokista. |

## <a name="enter-registration-ids-for-global-address-book-records"></a>Kirjoita yleisen osoitekirjan tietueiden rekisteröintitunnukset

Microsoft Dynamics 365 for Finance and Operationsin yleinen osoitekirja sisältää konsolidoidut osoitetiedot asiakkaille, toimittajille, yhteyshenkilöille, liikesuhteille ja yrityksille. Lisätietoja saat ohjeaiheesta [Yleisen osoitekirjan yleiskatsaus](../../fin-and-ops/organization-administration/overview-global-address-book.md). Osapuolen tietueet, jotka on tallennettu yleiseen osoitekirjaan, voivat sisältää yhden tai useampia osoitetietueita. Näitä osoitteita käytetään eri tarkoituksiin, esimerkiksi laskutukseen tai toimitukseen. Voit määrittää rekisteröintitunnukset asiakkaiden, toimittajien, työntekijöiden ja oikeussubjektien osoitetiedoille. Etsi osapuolen (oikeushenkilö, toimittaja, asiakas, työntekijä) tietue, jolle haluat syöttää rekisteritunnuksen ja valitse sitten **Rekisteröintitunnukset** oikeushenkilöön, toimittajaan, asiakkaaseen tai työntekijään liittyvässä lomakkeessa avataksesi **Osoitteiden hallinta** -sivun. Valitse **Verorekisteröinti**-välilehdessä **Lisää** ja kirjoita seuraavat tiedot rekisteröintitunnuksesta.


|Kenttä                |kuvaus                                                |
|---------------------|-----------------------------------------------------------|
| Rekisteröintityyppi   | Rekisteröintityyppi valitussa maassa/alueessa.     |
| Rekisteröintinumero | Osapuolen rekisteröintitunnus.                                |
| kuvaus         | Rekisteröintinumeron kuvaus.               |
| Osa             | Lisätietoja rekisteröintinumerosta. |
| Myöntäjätaho      | Rekisteröintinumeron myöntävä veroviranomainen.        |
| Luontipäivämäärä         | Rekisteröintinumeron luontipäivä.              |
| Voimassa           | Rekisteröintinumeron voimaantulopäivä.           |
| Vanhentuminen          | Rekisteröintinumeron vanhentumispäivä.          |

> [!NOTE]
> Yrityksen, toimittajan tai asiakkaan verovapautusnumero voidaan valita ALV-tunnukseen liittyvistä rekisteröintitunnuksista ja määrittää osapuolelle.

## <a name="search-for-records-by-registration-id"></a>Hae tietueita rekisteröintitunnuksella
Etsi osapuolen tietueita perustuen osapuolen, yrityksen, toimittajan, asiakkaan tai työntekijän lomakkeiden rekisteröintitunnukseen. Valitse **Rekisteröintitunnuksen haku** avataksesi **Rekisteröintitunnuksen hakuehdot** -sivun. Määritä hakuehdot ja valitse **Etsi**. Järjestelmä näyttää valitut tietueet yleisestä osoitekirjasta sekä osapuolitietueiden liittyvät tyypit.

## <a name="supported-registration-categories"></a>Tuetut rekisteröintiluokat
Seuraavassa taulukossa on lueteltu Finance and Operationsissa tuetut rekisteröintityypit. Jos osaat käyttää Microsoft Dynamics AX 2012:n kenttiä rekisteröintitunnusten kenttiä, myös tässä taulukossa nämä kentät yhdistetään Finance and Operationsin rekisteröintiluokkiin.

| Finance and Operationsin rekisteröintiluokka         |Maa/alue  | Dynamics AX 2012:n termi/kenttä|
|---------------------------------------------------------------|---------------------|---------------------------------|
| ALV-tunnus                                                        | Kaikki Euroopan unionin (EU) maat|  Verovapautusnumero (AX 2012 R3:n lainsäädännöllinen tyyppi TAX ID)|
| Yrityksen tunnus (COID)                                          | Belgia Tsekki Viro Unkari Latvia Liettua Puola Sveitsi | Yrityksen numero (EnterpriseNumber) Rekisteröintinumero (RegNum\_W) Rekisteröintinumero (RegNum\_W) Rekisteröintinumero (RegNum\_W) Rekisteröintinumero (RegNum\_W) Yrityksen koodi (EnterpriseCode) Rekisteröintinumero (RegNum\_W) UID-tunnus (AX 2012 R3:n lainsäädännöllinen tyyppi UID) |
| Sivuliikkeen tunnus                                                     | Belgia            | Sivuliikkeen numero (BranchNumber)|
| Spisová-značka (rekisterinumero, myöntävä toimisto, osasto) | Tšekin tasavalta     | Lisänumero (CommercialRegisterInsetNumber) Pidetään kaupparekisterissä (CommercialRegister) Kaupparekisterin alue (CommercialRegisterSection)|
| Tullin asiakastunnus                                           | Suomi | Tullin asiakasnumero (CustomsCustomerNumber\_FI)|
| INN                                                           | Venäjän federaatio| INN (AX 2012 R3:n lainsäädännöllinen tyyppi INN)|
| RRC                                                           | Venäjän federaatio| RRC (AX 2012 R3:n lainsäädännöllinen tyyppi RRC)|
| OKDP                                                          | Venäjän federaatio| OKDP (AX 2012 R3:n lainsäädännöllinen tyyppi OKDP)|
| OKPO                                                          | Venäjän federaatio| OKPO (AX 2012 R3:n lainsäädännöllinen tyyppi OKPO)|
| RCOAD                                                         | Venäjän federaatio| RCOAD (AX 2012 R3:n lainsäädännöllinen tyyppi RCOAD)|
| OGRN                                                          | Venäjän federaatio| OGRN (AX 2012 R3:n lainsäädännöllinen tyyppi OGRN) |
| SNILS                                                         | Venäjän federaatio| SNILS (AX 2012 R3:n lainsäädännöllinen tyyppi SNILS)|
| CIFTS                                                         | Venäjän federaatio| CIFTS (AX 2012 R3:n lainsäädännöllinen tyyppi CIFTS)|
| Passi                                                      | Espanja             | Passi|
| Virallinen tunnistusasiakirja                              | Espanja             | Virallinen tunnistusasiakirja|
| Asuinpaikkatodistus                                         | Espanja             | Asuinpaikkatodistus|
| Muu tunnistusasiakirja                                 | Espanja             | Muu tunnistusasiakirja|
| Ei laskettu                                                  | Espanja             | Ei käytettävissä AX 2012 R3 -versiossa|


Lisätietoja rekisteröintitunnusten käsittelystä mukaan lukien vaaditut edellytykset löydät seuraavista Lifecycle Services (LCS) -palvelusta ALV-tunnuksen tehtävätallenteista:

-   Aseta ALV-tunnus
-   Toimittajan ALV-tunnuksen rekisteröinti
-    Osaouolen haku ALV-tunnuksen avulla




