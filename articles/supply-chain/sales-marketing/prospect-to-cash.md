---
title: "Prospektista käteiseksi"
description: "Tässä ohjeaiheessa on yleiskatsaus prospektista käteiseksi ratkaisusta Dynamics 365 for Salesin ja Dynamics 365 for Finance and Operations, Enterprise editionin välillä."
author: ChristianRytt
manager: AnnBe
ms.date: 10/26/2017
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
ms.sourcegitcommit: 674d2e1f2c5cdbccf43618a9083ca01abed0735a
ms.openlocfilehash: 2accf77c5241adff7ad1648737dde451153fde46
ms.contentlocale: fi-fi
ms.lasthandoff: 11/14/2017

---

# <a name="prospect-to-cash"></a>Prospektista käteiseksi  

[!include[banner](../includes/banner.md)]

Prospektista käteiseksi ratkaisu synkronoi [tietojen integrointitoiminnolla](/common-data-service/entity-reference/dynamics-365-integration) tietoja Microsoft Dynamics 365 Financen ja Operations, Enterprise editionin ja Dynamics 365 for Salesin esiintymien välillä Common Data Servicen kautta. Tietojen integrointitoiminnon prospektista käteiseksi -mallit mahdollistavat tilien, yhteyshenkilöiden, tuotteiden, myyntitarjousten, myyntitilausten ja myyntilaskujen tietojen kulun Finance and Operationsin ja Salesin välillä. Kun tieto kulkee Finance and Operationsin ja Salesin välillä, voit suorittaa myynti- ja markkinointitehtäviä Salesissa sekä käsitellä tilauksen täyttämistä Finance and Operationsin inventoinnin- ja varastonhallinnalla. 

Ratkaisu integroi seuraavat alueet: 

-   [Ylläpidä tilejä Salesissa ja synkronoi ne Finance and Operationsiin.](accounts-template-mapping.md)
-   [Ylläpidä yhteyshenkilöitä Salesissa ja synkronoi ne Finance and Operationsiin.](contacts-template-mapping.md)
-   [Ylläpidä tuotteita Finance and Operationsissa ja synkronoi ne Salesiin](products-template-mapping.md)
-   [Luo myyntitarjouksia Salesissa ja synkronoi ne Finance and Operationsiin](sales-quotation-template-mapping.md)
-   [Luo myyntitilauksia Finance and Operationsissa ja synkronoi ne Salesiin](sales-order-template-mapping.md)
-   [Luo myyntilaskuja Finance and Operationsissa ja synkronoi ne Salesiin](sales-invoice-template-mapping.md)

Tämä ratkaisu mahdollistaa suoran synkronoinnin seuraavilla alueilla:

-   [Tilien ylläpito Salesissa ja tilien synkronointi suoraan Salesista Finance and Operationsiin](accounts-template-mapping-direct.md)
-   [Tuotteiden ylläpito Finance and Operationsissa ja synkronointi suoraan Salesiin](products-template-mapping-direct.md)
-   [Salesin yhteyshenkilöiden ylläpito ja synkronointi suoraan Finance and Operationsin yhteyshenkilöihin tai asiakkaisiin](contacts-template-mapping-direct.md)
-   [Myyntitarjouksien otsikoiden ja rivien synkronointi suoraan Salesista Finance and Operationsiin](sales-quotation-template-mapping-sales-fin.md)
-   [Myyntitilausten luominen Finance and Operationsissa ja synkronointi suoraan Salesiin](sales-order-template-mapping-direct.md)
-  [Myyntitilauksien otsikoiden ja rivien synkronointi suoraan Salesin ja Finance and Operationsin välillä](sales-order-template-mapping-between-sales-fin.md)
-   [Myyntitilausten synkronointi suoraan Salesin ja Finance and Operationsin välillä](sales-order-template-mapping-direct-two-ways.md)
-   [Myyntilaskujen luominen Finance and Operationsissa ja synkronointi suoraan Salesiin](sales-invoice-template-mapping-direct.md)


## <a name="system-requirements-for-dynamics-365-for-finance-and-operations-enterprise-edition"></a>Dynamics 365 for Finance and Operations, Enterprise Editionin järjestelmävaatimukset

Jotta voit käyttää prospektista käteiseksi -ratkaisua, sinun on asennettava seuraavat:

- Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (heinäkuu 2017) ja ympäristöpäivitys 8 (Sovellusversio 7.2.11792.56024 + ympäristö 7.0.4565.16212)

- Hotfix-korjaukset Microsoft Dynamics 365 for Finance and Operations, Enterprise Editioniin (heinäkuu 2017).
        
    -  [KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160) - Tämä hotfix-korjaus mahdollistaa tietojen integrointitoiminnon tuen myyntitilausten synkronoinnissa Salesista Finance and Operationsiin. Hotfix-korjaus sisältää myös muita parannuksia.

    -  [KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) - tämän korjaus mahdollistaa myyntitilauksen rivin synkronoinnin Finance and Operationsista Salesiin tietojen integrointitoiminnolla.
        
    -  [KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) - tämän korjaus mahdollistaa myyntitilauksen synkronoinnin Finance and Operationsista Salesiin tietojen integrointitoiminnolla.

**Huomautus**: ainoastaan KB4045570 on asennettava; sen asennus sisältää muiden KB-päivityksen korjaukset.
 
## <a name="system-requirements-for-dynamics-365-for-sales"></a>Dynamics 365 for Salesin järjestelmävaatimukset

Jotta voit käyttää prospektista käteiseksi -ratkaisua, sinun on asennettava seuraavat:

- Dynamics 365 for Sales -versio 1612 (8.2.1.207) (DB 8.2.1.207) online.
- Dynamics 365 for Salesin prospektista käteiseksi -ratkaisu, versio 1.14.0.0 (v14) tai uudempi.

### <a name="install-the-prospect-to-cash-solution-for-sales"></a>Asenna Salesin prospektista käteiseksi -ratkaisu

- Lataa [Dynamics 365 for Salesin prospektista käteiseksi -ratkaisun zip-pakettitiedosto](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) CustomerSourcesta.

- Varmista, että zip-tiedostoa ei ole estetty, jotta et saa virheviestiä "Tuontipakkauksia ei löytynyt", kun asennat ratkaisupaketin. Voit poistaa eston seuraavasti:

    -  Napsauta zip-tiedostoa hiiren kakkospainikkeella.
    -  Valitse **Ominaisuudet** ja valitse sitten **Kumoa esto**. 

- Pura ja suorita PackageDeployer.exe.

- Asenna prospektista käteiseksi -ratkaisu Sales-esiintymään.

    - Valitse **Office 365** -käyttöönottotyyppi.
    - Valitse **Näytä laajennettu**
    - Pika-asennuksen voit aloittaa valitsemalla **alueen**. Jos valitset **En tiedä**, järjestelmä etsii kaikki alueet, ja asennus kestää kauemmin.
    - Määritä **käyttäjänimi** ja **salasana** hallinnon käyttäjälle, jolla on käyttöoikeudet asentamiseen.

