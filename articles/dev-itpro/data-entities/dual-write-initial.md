---
title: Finance and Operationsin ja Common Data Servicen alkuperäisen sykronoinnin toteuttamisjärjestys
description: Tässä ohjeaiheessa määritetään synkronoinnin järjestys, jota on noudatettava alkuperäisten tietojen luomiseen.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 1473c3bad55734d5f83ee3e4c1654921b872f3bb
ms.sourcegitcommit: 3f05ede8b8acdf0550240a83a013e093b4ad043d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/13/2019
ms.locfileid: "1873125"
---
# <a name="execution-order-for-initial-synchronization-of-finance-and-operations-and-common-data-service"></a>Finance and Operationsin ja Common Data Servicen alkuperäisen sykronoinnin toteuttamisjärjestys

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

Ennen kuin käytät tietojen integrointia, sinun on luotava asiakkaille, toimittajille ja yhteyshenkilöille tarvittavat alkuperäiset tiedot. Haluat esimerkiksi luoda uuden **Toimittajaryhmä**-nimikkeen ja määrittää sen **Maksuehdot**-arvoksi **Net30**. Tässä tapauksessa, ennen kuin yrität luoda **Toimittajaryhmä**-nimikkeen, varmista, että **Net30** on sekä Microsoft Dynamics 365 for Finance and Operationsissa että Common Data Servicessä. (Tulevaisuudessa Microsoft julkaisee kaksoiskirjoitusalustan toiminnallisuuden nimeltä Alkusynronointi. Tämä ominaisuus tekee tietojen kertasynkronoinnin Finance and Operationsin ja Common Data Servicen välillä osana kaksoiskirjoituksen määritystä.)

> [!TIP]
> Microsoft julkaisee kaksoiskirjoituksen yhdistämismääritykset kaikille viitetiedoille, mukaan lukien **Maksuehdot** (maksuehdot). Jos sinulla on jo alkuperäiset tiedot yhdessä järjestelmässä, tietueen pieni päivitystoiminto voi laukaista kaksoiskirjoitustoiminnon kyseiseen tietueeseen.

Sinun on noudatettava seuraavaa järjestystä ja varmistettava, että alkuperäiset tiedot ovat käytettävissä sekä Finance and Operationsissa että Common Data Servicessa.

## <a name="vendor"></a>Toimittaja

Tässä on **Toimittaja**-kohteen suoritusjärjestys:

1. Toimittajaryhmä

    1. Maksuehto

        1. Maksupäivä ja -rivit
        2. Maksusuunnitelma

2. Toimittajan maksutapa

## <a name="customer-organization"></a>Asiakas (organisaatio)

Tässä on **Asiakas**-kohteen suoritusjärjestys:

1. Asiakasryhmä

    1. Maksuehto

        1. Maksupäivä ja -rivit
        2. Maksu 

2. Asiakkaan maksutapa

## <a name="contact-person"></a>Yhteyshenkilö (henkilö)

Tässä on **Yhteyshenkilö**-kohteen suoritusjärjestys:

1. Asiakas
2. Toimittaja
