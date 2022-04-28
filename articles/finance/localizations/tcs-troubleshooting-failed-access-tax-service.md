---
title: Veropalvelun käyttö epäonnistui
description: Tässä aiheessa kuvataan, miten Veron laskenta -palvelun käytön virhettä voidaan korjata.
author: hangwan
ms.date: 03/04/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxIntegrationTaxServiceParameters
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: hangwan
ms.search.validFrom: 02/16/2022
ms.dyn365.ops.version: Version 10.0.21
ms.openlocfilehash: f4682b83405071b4ad7647958122ab2b4e082133
ms.sourcegitcommit: 2977e92a76211875421e608555311c363cfbdc25
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/16/2022
ms.locfileid: "8612313"
---
# <a name="failed-to-access-tax-service"></a>Veropalvelun käyttö epäonnistui

[!include [banner](../includes/banner.md)]


Tässä aiheessa kerrotaan, miten verolaskentapalvelun "Ei voi käyttää veropalvelua" -virhe korjataan.

## <a name="symptoms"></a>Oireet

Siirry Microsoft Dynamics 365 Financessa kohtaan **Vero** \> **Määritys** \> **Veromääritys** \> **Veropalvelun parametrit**. Ota käyttöön **Ota käyttöön veron laskenta** -vaihtoehto **Yleiset**-välilehdessä. Jos yrität valita arvon **Ominaisuuden asetusten nimi** -kentässä, tapahtuu virhe. Virhesanomassa näkyy seuraava sanoma: "Veropalvelua ei voi käyttää."

## <a name="cause"></a>Syy

Tämä virhe ilmenee, koska Finance ei voi käyttää Veron laskenta -palvelua.

## <a name="resolution"></a>Ratkaisu 

1. Kirjaudu Microsoft Dynamics Lifecycle Servicesiin (LCS).
2. Etsi **Ympäristö-sivun** **Ympäristön lisäosat**-välilehdessä **Veron laskenta** -kohde ja tarkista sen tila. Tilan tulee olla **Asennetaan** tai **Asennettu**. Jos veron laskentapalvelun lisäosaa ei ole asennettu, näyttöön tulee virheilmoitus.

## <a name="mitigation"></a>Lievennys

1. Valitse LCS:n **Finance**-sivun **Power Platform - integrointi** -osasta **Asenna uusi lisäosa**.
2. Siirry sivun alareunaan ja asenna lisäosa valitsemalla **Veron laskenta**.
3. Palaa Finance-ympäristöön ja yritä käyttää Veron laskenta -palvelua.

> [!NOTE]
> Tarkista [veron laskentapalvelun edellytykset](global-get-started-with-tax-calculation-service.md#prerequisites) ennen veron laskentapalvelun asentamista.
> 
> Jos et voi asentaa lisäosaa, koska **Power Platform -integrointi** ei ole käytettävissä, katso [Lisäosien yleiskatsaus](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md). Jos kohtaat virheen edelleen sen jälkeen, kun olet asentanut lisäosan, ota yhteys järjestelmänvalvojaan.
