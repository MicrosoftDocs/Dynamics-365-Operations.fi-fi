---
title: "Rekisteröintitunnukset"
description: "Tässä ohjeaiheessa on tietoja rekisteröintitunnuksien määrittämisestä ja käyttämisestä."
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
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 712eb9ec22f4eea4a969a7bd23b7d3728b35772e
ms.contentlocale: fi-fi
ms.lasthandoff: 04/25/2017


---

# <a name="registration-ids"></a>Rekisteröintitunnukset

[!include[banner](../includes/banner.md)]


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
| Rekisteröintiluokka | Yksilöllinen rekisteröintitunnus, joka on hyväksytty käyttöön kyseisessä maassa. Alla on täydellinen luettelo AX7.1-luokista. |

## <a name="enter-registration-ids-for-global-address-book-records"></a>Kirjoita yleisen osoitekirjan tietueiden rekisteröintitunnukset
Microsoft Dynamics 365 for Operationsin yleinen osoitekirja sisältää konsolidoidut osoitetiedot asiakkaille, toimittajille, yhteyshenkilöille, liikesuhteille ja yrityksille. Lisätietoja saat ohjeaiheesta [Yleisen osoitekirjan yleiskatsaus](/dynamics365/operations/organization-administration/overview-global-address-book). Osapuolen tietueet, jotka on tallennettu yleiseen osoitekirjaan, voivat sisältää yhden tai useampia osoitetietueita. Näitä osoitteita käytetään eri tarkoituksiin, esimerkiksi laskutukseen tai toimitukseen. Voit määrittää rekisteröintitunnukset asiakkaiden, toimittajien, työntekijöiden ja oikeussubjektien osoitetiedoille. Etsi osapuolen (oikeushenkilö, toimittaja, asiakas, työntekijä) tietue, jolle haluat syöttää rekisteritunnuksen ja valitse sitten **Rekisteröintitunnukset** oikeushenkilöön, toimittajaan, asiakkaaseen tai työntekijään liittyvässä lomakkeessa avataksesi **Osoitteiden hallinta** -sivun. Valitse **Verorekisteröinti**-välilehdessä **Lisää** ja kirjoita seuraavat tiedot rekisteröintitunnuksesta.

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
Seuraavassa taulukossa on lueteltu Dynamics 365 for Operationsissa tuetut rekisteröintityypit. Jos osaat käyttää Microsoft Dynamics AX 2012 -kenttiä rekisteröintitunnuksille, tässä taulukossa myös yhdistetään nämä kentät myös Dynamics 365 for Operationsin rekisteröintiluokkiin.

| Dynamics 365 for Operations -rekisteröintiluokka         |Maa/alue  | Dynamics AX 2012:n termi/kenttä|
|---------------------------------------------------------------|---------------------|---------------------------------|
| ALV-tunnus                                                        | Kaikki Euroopan unionin (EU) maat|  Verovapautusnumero (Lainopillinen tyyppi TAX ID kohteessa AX2012 R3)|
| Yrityksen tunnus (COID)                                          | Belgia Tsekki Viro Unkari Latvia Liettua Puola Sveitsi | Enterprise number (EnterpriseNumber) Registration number (RegNum\_W) Registration number (RegNum\_W) Registration number (RegNum\_W) Registration number (RegNum\_W) Enterprise code (EnterpriseCode) Registration number (RegNum\_W) UID (Legislative type UID in AX2012 R3) |
| Sivuliikkeen tunnus                                                     | Belgia            | Sivuliikkeen numero (BranchNumber)|
| Spisová-značka (rekisterinumero, myöntävä toimisto, osasto) | Tšekin tasavalta     | Lisänumero (CommercialRegisterInsetNumber) Pidetään kaupparekisterissä (CommercialRegister) Kaupparekisterin alue (CommercialRegisterSection)|
| Tullin asiakastunnus                                           | Suomi | Tullin asiakasnumero (CustomsCustomerNumber\_FI)|
| INN                                                           | Venäjän federaatio| INN (Lainopillinen tyyppi INN kohteessa AX2012 R3)|
| RRC                                                           | Venäjän federaatio| RRC (Lainopillinen tyyppi RRC kohteessa AX2012 R3)|
| OKDP                                                          | Venäjän federaatio| OKDP (Lainopillinen tyyppi OKDP kohteessa AX2012 R3)|
| OKPO                                                          | Venäjän federaatio| OKPO (Lainopillinen tyyppi OKPO kohteessa AX2012 R3)|
| RCOAD                                                         | Venäjän federaatio| RCOAD (Lainopillinen tyyppi RCOAD kohteessa AX2012 R3)|
| OGRN                                                          | Venäjän federaatio| OGRN (Lainopillinen tyyppi OGRN kohteessa AX2012 R3) |
| SNILS                                                         | Venäjän federaatio| SNILS (Lainopillinen tyyppi SNILS kohteessa AX2012 R3)|
| CIFTS                                                         | Venäjän federaatio| CIFTS (Lainopillinen tyyppi CIFTS kohteessa AX2012 R3)|

Lisätietoja rekisteröintitunnusten käsittelystä mukaan lukien vaaditut edellytykset löydät seuraavista Lifecycle Services (LCS) -palvelusta ALV-tunnuksen tehtävätallenteista:

-   Aseta ALV-tunnus
-   Toimittajan ALV-tunnuksen rekisteröinti
-    Osaouolen haku ALV-tunnuksen avulla





