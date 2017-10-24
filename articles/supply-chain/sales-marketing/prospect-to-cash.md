---
title: "Prospektista käteiseksi"
description: "Tässä ohjeaiheessa on yleiskatsaus prospektista käteiseksi ratkaisusta Dynamics 365 for Salesin ja Dynamics 365 for Finance and Operations, Enterprise editionin välillä."
author: ChristianRytt
manager: AnnBe
ms.date: 08/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 47e70cb1291e390b42b7feff844b2aca141f09b7
ms.openlocfilehash: a5f1ecd5f8b46287839439a963e571531ae161a7
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

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

## <a name="system-requirements-for-dynamics-365-for-finance-and-operations-enterprise-edition"></a>Dynamics 365 for Finance and Operations, Enterprise Editionin järjestelmävaatimukset

Jotta voit käyttää prospektista käteiseksi -ratkaisua, sinun on asennettava seuraavat:

- Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (heinäkuu 2017) ja ympäristöpäivitys 8 (Sovellusversio 7.2.11792.56024 + ympäristö 7.0.4565.16212)

- Kaksi hotfix-korjausta Microsoft Dynamics 365 for Finance and Operations, Enterprise Editioniin (heinäkuu 2017).

    -  [KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) - tämän korjaus mahdollistaa myyntitilauksen rivin synkronoinnin Finance and Operationsista Salesiin tietojen integrointitoiminnolla.
        
    -  [KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) - tämän korjaus mahdollistaa myyntitilauksen synkronoinnin Finance and Operationsista Salesiin tietojen integrointitoiminnolla.
    
**Huomautus**: ainoastaan KB4036524 on asennettava; sen asennus sisältää KB4036461-päivityksen korjaukset.
 
## <a name="system-requirements-for-dynamics-365-for-sales"></a>Dynamics 365 for Salesin järjestelmävaatimukset

Jotta voit käyttää prospektista käteiseksi -ratkaisua, sinun on asennettava seuraavat:

- Dynamics 365 for Sales -versio 1612 (8.2.1.207) (DB 8.2.1.207) online tai uudempi.
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

