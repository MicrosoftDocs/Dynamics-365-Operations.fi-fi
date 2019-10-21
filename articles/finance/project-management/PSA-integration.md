---
title: Project Service Automationin yleiskatsaus
description: Tässä ohjeaiheessa on tietoja Dynamics 365 Project Service Automationin ja Dynamics 365 Financen integrointiratkaisusta.
author: KimANelson
manager: AnnBe
ms.date: 07/25/2019
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
ms.openlocfilehash: 31d72591041f8d8cc327aa7c6578c15731ba13c5
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250550"
---
# <a name="project-service-automation-overview"></a>Project Service Automationin yleiskatsaus

[!include[banner](../includes/banner.md)]

Project Service Automationin ja Financen välinen integrointiratkaisu synkronoi tietojen integrointitoiminnolla tietoja Dynamics 365 Financen ja Dynamics 365 Project Service Automationin esiintymien välillä Common Data Servicen kautta. Tietojen integrointiominaisuuteen sisältyvät integrointimallit mahdollistavat projekteja, projektisopimuksia, projektisopimuksen rivejä, projektisopimuksen rivien välitavoitteita, projektitehtäviä, kulutapahtumaluokkia, tuntiarvioita ja kuluarvioita koskevien tietojen siirtymisen Project Service Automationista Financeen.

> [!NOTE]
> - Jos käytät versiota 7.3.0, sinun on asennettava KB 4074835. Sen avulla voi integroida kiinteähintaisia projekteja.
> - Jos käytät versiota 7.3.0 ja tuot maksutapahtumia Project Service Automationista, sinun on asennettava KB 4345320, jotta maksut sisällytetään projektin laskuun.
> - Jos käytä versiota 8.0, voit käyttää projektitehtävien integrointia, kulutapahtumaluokkia, tuntiarvioita, kuluarvioita ja toiminnon lukitsemista.
> - Jos käytät versiota 8.0.1 tai uudempaa, voit synkronoida todelliset tiedot.

Project Service Automationin integrointiparametrit on määritettävä ennen Project Service Automationin ja Financen integrointia. Lisätietoja on kohdassa [Project Service Automationin integrointiparametrit](PSA-parameters.md).

Integrointiratkaisu mahdollistaa suoran synkronoinnin seuraavissa skenaarioissa:

- Projektisopimusten ylläpito Project Service Automationissa ja niiden synkronointi suoraan Project Service Automationista Financeen.
- Projektien luonti Project Service Automationissa ja niiden synkronointi suoraan Project Service Automationista Financeen.
- Projektisopimusten rivien ylläpito Project Service Automationissa ja niiden synkronointi suoraan Project Service Automationista Financeen.
- Projektisopimusten rivien välitavoitteiden ylläpito Project Service Automationissa ja niiden synkronointi suoraan Project Service Automationista Financeen.
- Projektitehtävien ylläpito Project Service Automationissa ja niiden synkronointi suoraan Project Service Automationista Financeen.
- Kulutapahtumaluokkien ylläpito Financessa ja niiden synkronointi suoraan Financesta Project Service Automationiin.
- Projektin tuntiarvioiden luonti Project Service Automationissa ja niiden synkronointi suoraan Project Service Automationista Financeen.
- Projektin kuluarvioiden luonti Project Service Automationissa ja niiden synkronointi suoraan Project Service Automationista Financeen.
- Luo projektin aika, kulut ja todelliset maksut Project Service Automationissa ja luo projektitapahtumat Project Service Automationin integraatiokirjauskansiossa siten, että ne voidaan kirjataan Financeen.

## <a name="data-synchronization"></a>Tietojen synkronointi

Seuraava kuva ilmaisee, miten tiedot synkronoidaan osana Project Service Automationin ja Financen välistä integrointia.

> [!NOTE]
> Tällä hetkellä yhtään mallia ei ole käytettävissä. Mallit julkaistaan, kun ne valmistuvat.

[![Project Service Automationin ja Financen integrointi](./media/PSA-integration.png)](./media/PSA-integration.png)

## <a name="system-requirements-for-finance"></a>Financen järjestelmävaatimukset

Project Service Automationin ja Financen välisen integrointiratkaisua varten on asennettava Enterprise edition 7.3, jossa on ympäristöpäivitys 12 tai uudempi.

## <a name="system-requirements-for-project-service-automation"></a>Project Service Automationin järjestelmävaatimukset

Project Service Automationin ja Financen välisen integrointiratkaisun käyttöä varten on asennettava seuraavat osat:

- Dynamics 365 Project Service Automation versio 9.0.0.0 tai uudempi
- Dynamics 365 Salesin Prospektista käteiseksi -ratkaisu, versio 1.14.0.0 (v14) tai uudempi
- Project Service Automationista Financeen -ratkaisu Dynamics 365 Project Service Automation -versiolle 1.0.0.0 tai uudemmalle

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a>Asenna Project Service Automationin ja Financen välinen integrointiratkaisu Project Service Automationin esiintymään

Lataa Project Service Automationin ja Financen välinen integrointiratkaisu [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=57016) -sivulta ja noudata ratkaisun mukana olevia ohjeita.
