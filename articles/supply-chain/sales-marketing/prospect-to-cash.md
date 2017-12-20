---
title: "Prospektista käteiseksi"
description: "Tässä ohjeaiheessa on yleiskuvaus Microsoft Dynamics 365 for Finance and Operations, Enterprise editionin ja Microsoft Dynamics 365 for Sales -sovelluksen välisestä prospektista käteiseksi -ratkaisusta."
author: ChristianRytt
manager: AnnBe
ms.date: 11/17/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 788e64476094e84eb4d438890776306c05b20582
ms.openlocfilehash: 762699cf68ec8a9df5db20d7dd33bc9248f0a36e
ms.contentlocale: fi-fi
ms.lasthandoff: 12/11/2017

---

# <a name="prospect-to-cash"></a>Prospektista käteiseksi

[!include[banner](../includes/banner.md)]

Prospektista käteiseksi -ratkaisu mahdollistaa suoran synkronoinnin Microsoft Dynamics 365 for Finance and Operations, Enterprise editionin ja Microsoft Dynamics 365 for Sales -sovelluksen välillä. Tietojen integrointitoiminnon prospektista käteiseksi -mallit mahdollistavat tilien, yhteyshenkilöiden, tuotteiden, myyntitarjousten, myyntitilausten ja myyntilaskujen tietojen kulun Finance and Operationsin ja Salesin välillä. Kun tieto kulkee Finance and Operationsin ja Salesin välillä, voit suorittaa myynti- ja markkinointitehtäviä Salesissa sekä käsitellä tilauksen täyttämistä Finance and Operationsin inventoinnin- ja varastonhallinnalla.

Nykyisessä versiossa prospektista käteiseksi -ratkaisu mahdollistaa seuraavat suoran synkronoinnin tyypit:

- [Tilien ylläpito Salesissa ja tilien synkronointi suoraan Salesista Finance and Operationsiin](accounts-template-mapping-direct.md)
- [Tuotteiden ylläpito Finance and Operationsissa ja synkronointi suoraan Salesiin](products-template-mapping-direct.md)
- [Salesin yhteyshenkilöiden ylläpito ja synkronointi suoraan Finance and Operationsin yhteyshenkilöihin tai asiakkaisiin](contacts-template-mapping-direct.md)
- [Myyntitarjouksien synkronointi suoraan Salesista Finance and Operationsiin](sales-quotation-template-mapping-sales-fin.md)
- [Myyntitilausten synkronointi suoraan Finance and Operationsista Salesiin](sales-order-template-mapping-direct.md)
- [Myyntitilausten synkronointi suoraan Salesin ja Finance and Operationsin välillä](sales-order-template-mapping-direct-two-ways.md)
- [Myyntilaskun synkronointi suoraan Finance and Operationsista Salesiin](sales-invoice-template-mapping-direct.md)

Aiemmissa versiossa prospektista käteiseksi -ratkaisu mahdollistaa seuraavat epäsuoran synkronoinnin tyypit:

- [Ylläpidä tilejä Salesissa ja synkronoi ne Finance and Operationsiin.](accounts-template-mapping.md)
- [Ylläpidä yhteyshenkilöitä Salesissa ja synkronoi ne Finance and Operationsiin.](contacts-template-mapping.md)
- [Ylläpidä tuotteita Finance and Operationsissa ja synkronoi ne Salesiin](products-template-mapping.md)
- [Luo myyntitarjouksia Salesissa ja synkronoi ne Finance and Operationsiin](sales-quotation-template-mapping.md)
- [Luo myyntitilauksia Finance and Operationsissa ja synkronoi ne Salesiin](sales-order-template-mapping.md)
- [Luo myyntilaskuja Finance and Operationsissa ja synkronoi ne Salesiin](sales-invoice-template-mapping.md)

## <a name="system-requirements-for-finance-and-operations"></a>Finance and Operations -sovelluksen järjestelmävaatimukset

Seuraavat komponentit on asennettava, jotta prospektista käteiseksi -ratkaisua voi käyttää:

### <a name="july-2017"></a>Heinäkuu 2017 

- Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (heinäkuu 2017) ja ympäristöpäivitys 8 (sovelluksen versio 7.2.11792.56024 + ympäristö 7.0.4565.16212)
- Finance and Operations -sovelluksen hotfix-korjaukset:

    - **[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** – tämän korjaus mahdollistaa myyntitilauksen synkronoinnin Salesista Finance and Operationsiin tietojen integrointitoiminnolla. Se sisältää myös useita parannuksia.
    - **[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – tämän korjaus mahdollistaa myyntitilausrivin synkronoinnin Finance and Operationsista Salesiin tietojen integrointitoiminnolla.
    - **[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – tämän korjaus mahdollistaa myyntitilauksen synkronoinnin Finance and Operationsista Salesiin tietojen integrointitoiminnolla.

    > [!NOTE]
    > Ainoastaan KB4045570 on asennettava, koska sen asennus sisältää muiden Microsoft Knowledge Base -tietokannan artikkeleiden muutokset.

### <a name="november-2016-version-1611"></a>Marraskuun 2016 (versio 1611)

- Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (marraskuu 2016) ja ympäristöpäivitys 8 tai uudempi

- Finance and Operations -sovelluksen hotfix-korjaukset:

    - **[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** - Mahdollistaa myyntitilauksen synkronoinnin Microsoft Dynamics 365 for Finance and Operationsista Salesiin tietojen integrointiohjelman avulla 
    - **[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** - Mahdollistaa myyntitilausotsikon ja -rivin synkronoinnin Microsoft Dynamics 365 for Finance and Operationsista Salesiin tietojen integrointiohjelman avulla
    - **[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** - Prospektista käteiseksi -integrointi tietoyksiköiden kautta vaatii tuen
    
    > [!NOTE]
    > Kun hotfix-korjaukset on asennettu, seuraava SalesPopulateProspectToCash-lomakkeen erätyö on käynnistettävä. Tämä lomake on piilotettu, koska sitä tarvitaan vain kerran. Löydät sen lisäämällä seuraavan osoitteen selaimen osoitekenttään, kun olet kirjautunut sisään ympäristöön: &mi=action:SalesPopulateProspectToCash, esimerkiksi https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash Valitse avautuvassa lomakkeessa OK.
    SalesLine-, SalesQuotationLine- ja CustInvoiceTrans-taulukon uuteen LineCreationSequnceNumber-kenttiin täytetään yksilöivät arvot ja tuoteluettelo päivitetään. Tämä on pakollista, jotta P2C-integrointi toimii versiossa 7.1


## <a name="system-requirements-for-sales"></a>Sales-sovelluksen järjestelmävaatimukset

Seuraavat komponentit on asennettava, jotta prospektista käteiseksi -ratkaisua voi käyttää:

- Microsoft Dynamics 365 for Sales -versio 1612 (8.2.1.207) (DB 8.2.1.207) online
- Microsoft Dynamics 365 for Salesin prospektista käteiseksi -ratkaisu, versio 1.15.0.0 (v15) 

   > [!NOTE]
   >
   > Malleja, joiden versio on 1.0.0.0 tai 1.0.0.1, tuetaan prospektista käteiseksi -ratkaisussa Microsoft Dynamics 365 for Sales -sovelluksen versiossa 1.14.1.0
   >
   > Malleja, joiden versio on 2.0.0.0 tai 2.1.0.0, ei tueta prospektista käteiseksi -ratkaisussa Microsoft Dynamics 365 for Sales -sovelluksen versiossa 1.15.0.0

### <a name="install-the-prospect-to-cash-solution-for-sales"></a>Asenna Salesin prospektista käteiseksi -ratkaisu

1. Lataa [Dynamics 365 for Salesin prospektista käteiseksi -ratkaisun zip-pakettitiedosto](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) CustomerSourcesta.
2. Varmista, että zip-tiedoston esto on poistettu. Muussa tapauksessa saat seuraavan virhesanoman, kun yrität asentaa ratkaisupakettia: Tuontipaketteja ei löytynyt. Voit poistaa zip-tiedoston eston napsauttamalla sitä hiiren kakkospainikkeella ja valitsemalla **Ominaisuudet**-kohdan. Valitse sitten **Poista esto**.
3. Pura ja suorita **PackageDeployer.exe**.
4. Asenna prospektista käteiseksi -ratkaisu Sales-esiintymään:

    1. Valitse käyttöönottotyypiksi **Office 365**.
    2. Valitse **Näytä laajennettu**
    3. Aloita pika-asennus valitsemalla alue. Jos valitset **En tiedä**, järjestelmä etsii kaikki alueet, ja asennus kestää kauemmin.
    4. Anna asennusoikeudet omaavan järjestelmänvalvojan käyttäjänimi ja salasana.

