---
title: "Prospektista käteiseksi"
description: "Tässä ohjeaiheessa on yleiskuvaus Microsoft Dynamics 365 for Finance and Operationsin ja Microsoft Dynamics 365 for Salesin välisestä prospektista käteiseksi -ratkaisusta."
author: ChristianRytt
manager: AnnBe
ms.date: 04/03/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustTable, SalesTable, EcoResProductListPage
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: bc0fa8fe3e20ae4be3e572932f99ccc54e3b746b
ms.contentlocale: fi-fi
ms.lasthandoff: 04/13/2018

---

# <a name="prospect-to-cash"></a>Prospektista käteiseksi

[!INCLUDE [banner](../includes/banner.md)]

Prospektista käteiseksi -ratkaisu mahdollistaa suoran synkronoinnin Dynamics 365 for Finance and Operationsin ja Dynamics 365 for Salesin välillä. Tietojen integrointitoiminnon prospektista käteiseksi -mallit mahdollistavat tilien, yhteyshenkilöiden, tuotteiden, myyntitarjousten, myyntitilausten ja myyntilaskujen tietojen kulun Finance and Operationsin ja Salesin välillä. Kun tieto kulkee Finance and Operationsin ja Salesin välillä, voit suorittaa myynti- ja markkinointitehtäviä Salesissa sekä käsitellä tilauksen täyttämistä Finance and Operationsin inventoinnin- ja varastonhallinnalla. 

Saat lisätietoja Prospektista käteiseksi -integraatiosta katsomalla lyhyen YouTube-videon:

> [!Video https://www.youtube.com/embed/AVV9x5x-XCg]

Nykyisessä versiossa prospektista käteiseksi -ratkaisu mahdollistaa seuraavat suoran synkronoinnin tyypit:

- [Tilien ylläpito Salesissa ja tilien synkronointi suoraan Salesista Finance and Operationsiin](accounts-template-mapping-direct.md)
- [Tuotteiden ylläpito Finance and Operationsissa ja synkronointi suoraan Salesiin](products-template-mapping-direct.md)
- [Salesin yhteyshenkilöiden ylläpito ja synkronointi suoraan Finance and Operationsin yhteyshenkilöihin tai asiakkaisiin](contacts-template-mapping-direct.md)
- [Myyntitarjouksien synkronointi suoraan Salesista Finance and Operationsiin](sales-quotation-template-mapping-sales-fin.md)
- [Myyntitilausten synkronointi suoraan Salesin ja Finance and Operationsin välillä](sales-order-template-mapping-direct-two-ways.md)
- [Myyntilaskun synkronointi suoraan Finance and Operationsista Salesiin](sales-invoice-template-mapping-direct.md)

## <a name="system-requirements-for-finance-and-operations"></a>Finance and Operations -sovelluksen järjestelmävaatimukset
Prospektista käteiseksi -integraatio tuetaan seuraavissa versioissa:

### <a name="microsoft-dynamics-365-for-finance-and-operations-enterprise-edition-73-december-2017"></a>Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 (joulukuu 2017)

- Dynamics 365 for Finance and Operations, Enterprise edition (joulukuu 2017) – sovellusversio 7.3.11971.56116 ja ympäristöversio 12 (7.0.4709.41129)

### <a name="dynamics-365-for-finance-and-operations-enterprise-edition-july-2017"></a>Dynamics 365 for Finance and Operations, Enterprise edition (heinäkuu 2017)

- Dynamics 365 for Finance and Operations, Enterprise edition (heinäkuu 2017) – sekä ympäristöpäivitys 8 (sovellusversio 7.2.11792.56024 ja ympäristöversio 7.0.4565.16212).
- Seuraavat hotfix-korjaukset ovat pakollisia:

  - **[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** – tämän korjaus mahdollistaa myyntitilauksen synkronoinnin Salesista Finance and Operationsiin tietojen integrointitoiminnolla. Se sisältää myös useita parannuksia.
  - **[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – tämän korjaus mahdollistaa myyntitilausrivin synkronoinnin Finance and Operationsista Salesiin tietojen integrointitoiminnolla.
  - **[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – tämän korjaus mahdollistaa myyntitilauksen synkronoinnin Finance and Operationsista Salesiin tietojen integrointitoiminnolla.

    > [!NOTE]
    > Ainoastaan KB4045570 on asennettava, sillä sen asennus sisältää muiden hotfix-korjausten muutokset. 

### <a name="dynamics-365-for-finance-and-operations-version-1611-november-2016"></a>Dynamics 365 for Finance and Operations -versio 1611 (marraskuu 2016)

- Dynamics 365 for Finance and Operations -versio 1611 (marraskuu 2016) ja vähintään ympäristöpäivitys 8

- Seuraavat hotfix-korjaukset ovat pakollisia:

  - **[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** - Mahdollistaa myyntitilauksen synkronoinnin Finance and Operationsista Salesiin tietojen integrointiohjelman avulla. 
  - **[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** - Mahdollistaa myyntitilauksen otsikon ja rivin synkronoinnin Finance and Operationsista Salesiin tietojen integrointiohjelman avulla.
  - **[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** - Prospektista käteiseksi -integrointia tietoyksiköiden kautta on tuettava.
    
    > [!NOTE]
    > Kun hotfix-korjaukset on asennettu, seuraava **SalesPopulateProspectToCash**-lomakkeen erätyö on käynnistettävä. Tämä lomake on piilotettu, koska sitä tarvitaan vain kerran. Voit käyttää lomaketta kirjautumalla ympäristöön ja lisäämällä seuraavan URL-osoitteeseen selaimen osoitekentässä. Esimerkki: `https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash`. Kun lomake avautuu, valitse OK. **SalesLine**-, **SalesQuotationLine**- ja **CustInvoiceTrans**-taulukkojenn uuteen **LineCreationSequnceNumber**-kenttiin täytetään yksilöivät arvot, jolloin tuoteluettelo päivittyy. Tämä on välttämätöntä, jotta Prospektista käteiseksi -integrointi toimisi.


## <a name="system-requirements-for-sales"></a>Sales-sovelluksen järjestelmävaatimukset

Seuraavat komponentit on asennettava, jotta prospektista käteiseksi -ratkaisua voi käyttää:

- Dynamics 365 for Sales -versio 1612 (8.2.1.207) (DB 8.2.1.207) online tai uudempi versio
- Dynamics 365 for Salesin prospektista käteiseksi -ratkaisu, versio 1.15.0.0 tai uudempi versio. Ratkaisun voi ladata AppSourcesta. [Lataa Dynamics 365, Prospektista käteiseksi](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).

