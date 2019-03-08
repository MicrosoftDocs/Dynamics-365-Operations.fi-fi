---
title: Project Service Automation
description: Tässä ohjeaiheessa on tietoja Project Service Automation to Finance and Operationsin integraatioratkaisuista. Tämä integraatioratkaisu synkronoi tietojen integrointitoiminnolla tietoja Microsoft Dynamics 365 for Finance and Operationsin ja Microsoft Dynamics 365 for Project Service Automationin esiintymien välillä Common Data Servicen kautta.
author: KimANelson
manager: AnnBe
ms.date: 06/29/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4b1d2ae69899a2937d47f6547ee4ba72b2d1ece4
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "335689"
---
# <a name="project-service-automation"></a>Project Service Automation

[!include[banner](../includes/banner.md)]

Project Service Automationin ja Finance and Operationsin välinen integrointiratkaisu synkronoi tietojen integrointitoiminnolla tietoja Microsoft Dynamics 365 for Finance and Operationsin ja Microsoft Dynamics 365 for Project Service Automationin esiintymien välillä Common Data Servicen kautta. Tietojen integrointiominaisuuteen sisältyvät integrointimallit mahdollistavat projekteja, projektisopimuksia, projektisopimuksen rivejä, projektisopimuksen rivien välitavoitteita, projektitehtäviä, kulutapahtumaluokkia, tuntiarvioita ja kuluarvioita koskevien tietojen siirtymisen Project Service Automationista Finance and Operationsiin.

> [!NOTE]
> - Jos käytössä on Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0 ja KB 4132657 ja KB 4132660 on asennettu, voit integroida projektitehtäviä, kulutapahtumaluokkia, tuntiarvioita, kuluarvioita ja todellisia tietoja sekä määrittää toimintojen lukituksen. Jos kirjanpidollinen jako on palautettava alkuperäisasetuksiin, myös KB 4131710 kannattaa asentaa.
> - Jos käytät Finance and Operations 7.3.0 -versiota, sinun on asennettava KB 4074835. Sen avulla voi integroida kiinteähintaisia projekteja.
> - Jos käytät Finance and Operations 7.3.0:aa ja tuot maksutapahtumia Project Service Automationista, sinun on asennettava KB 4345320, jotta maksut sisällytetään projektin laskuun.
> - Jos käytössä on Microsoft Dynamics 365 for Finance and Operationsin versio 8.0, voit käyttää projektitehtävien integrointia, kulutapahtumaluokkia, tuntiarvioita, kuluarvioita ja toiminnon lukitsemista.
> - Jos käytössä on Microsoft Dynamics 365 for Finance and Operationsin versio 8.0.1 tai uudempi, voit synkronoida todelliset tiedot.

Project Service Automationin integrointiparametrit on määritettävä ennen Project Service Automationin ja Finance and Operationsin integrointia. Lisätietoja on kohdassa [Project Service Automationin integrointiparametrit](PSA-parameters.md).

Integrointiratkaisu mahdollistaa suoran synkronoinnin seuraavissa skenaarioissa:

- Projektisopimusten ylläpito Project Service Automationissa ja niiden synkronointi suoraan Project Service Automationista Finance and Operationsiin.
- Projektien luonti Project Service Automationissa ja niiden synkronointi suoraan Project Service Automationista Finance and Operationsiin.
- Projektisopimuksen rivien ylläpito Project Service Automationissa ja niiden synkronointi suoraan Project Service Automationista Finance and Operationsiin.
- Projektisopimuksen rivien välitavoitteiden ylläpito Project Service Automationissa ja niiden synkronointi suoraan Project Service Automationista Finance and Operationsiin.
- Projektitehtävien ylläpito Project Service Automationissa ja niiden synkronointi suoraan Project Service Automationista Finance and Operationsiin.
- Kulutapahtumaluokkien ylläpito Finance and Operationsissa ja niiden synkronointi suoraan Finance and Operationsista Project Service Automationiin.
- Projektin tuntiarvioiden luonti Project Service Automationissa ja niiden synkronointi suoraan Project Service Automationista Finance and Operationsiin.
- Projektin kuluarvioiden luonti Project Service Automationissa ja niiden synkronointi suoraan Project Service Automationista Finance and Operationsiin.
- Luo projektin aika, kulut ja todelliset maksut Project Service Automationissa ja luo projektitapahtumat Project Service Automationin integraatiokirjauskansiossa siten, että ne voidaan kirjataan Finance and Operationsiin.

## <a name="data-synchronization"></a>Tietojen synkronointi

Seuraava kuva ilmaisee, miten tiedot synkronoidaan osana Project Service Automationin ja Finance and Operationsin välistä integrointia.

> [!NOTE]
> Tällä hetkellä yhtään mallia ei ole käytettävissä. Mallit julkaistaan, kun ne valmistuvat.

[![Project Service Automationin ja Finance and Operationsin integrointi](./media/PSA-integration.png)](./media/PSA-integration.png)

## <a name="system-requirements-for-finance-and-operations"></a>Finance and Operations -sovelluksen järjestelmävaatimukset

Project Service Automationin ja Finance and Operationsin välisen integrointiratkaisua varten on asennettava Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3, jossa on vähintään ympäristöpäivitys 12.

## <a name="system-requirements-for-project-service-automation"></a>Project Service Automationin järjestelmävaatimukset

Project Service Automationin ja Finance and Operationsin välisen integrointiratkaisun käyttöä varten on asennettava seuraavat osat:

- Microsoft Dynamics 365 for Project Service Automation versio 9.0.0.0 tai uudempi
- Microsoft Dynamics 365 for Salesin prospektista käteiseksi -ratkaisu, versio 1.14.0.0 (14) tai uudempi
- Microsoft Dynamics 365 for Project Service Automationin version 1.0.0.0 tai uudemman ratkaisu Project Service Automationista Finance and Operationsiin

## <a name="install-the-project-service-automation-to-finance-and-operations-integration-solution-in-your-project-service-automation-instance"></a>Asenna Project Service Automationin ja Finance and Operationsin välinen integrointiratkaisu Project Service Automationin esiintymään.

Lataa Project Service Automation to Finance and Operationsin integrointiratkaisu [Microsoft Download Center](https://www.microsoft.com/en-us/download/details.aspx?id=57016) -sivulta, ja seuraa ratkaisun mukana olevia ohjeita.
