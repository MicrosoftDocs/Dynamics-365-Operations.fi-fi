---
title: Finance and Operations- ja Common Data Service -sovellusten ja ohjelmien alkusynkronoinnin suoritusjärjestys
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
ms.openlocfilehash: befe4e12a10f4a39b90bcb4faba6431a063a40e2
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019760"
---
# <a name="execution-order-for-initial-synchronization-of-finance-and-operations-apps-and-common-data-service"></a>Finance and Operations- ja Common Data Service -sovellusten ja ohjelmien alkusynkronoinnin suoritusjärjestys

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

Ennen kuin käytät tietojen integrointia, sinun on luotava asiakkaille, toimittajille ja yhteyshenkilöille tarvittavat alkuperäiset tiedot. Haluat esimerkiksi luoda uuden **Toimittajaryhmä**-nimikkeen ja määrittää sen **Maksuehdot**-arvoksi **Net30**. Varmista tässä tapauksessa ennen **Toimittajaryhmä**-nimikkeen luomisen yrittämistä, että **Net30** on sekä sovelluksessa että Common Data Servicessä. (Microsoft julkaisee tulevaisuudessa kaksoiskirjoitusalustan toiminnallisuuden nimeltä Alkusynkronointi. Tämä toiminto synkronoi tiedot kerran sovelluksen ja Common Data Servicen välillä osana kaksoiskirjoituksen määritystä.)

> [!TIP]
> Microsoft julkaisee kaksoiskirjoituksen yhdistämismääritykset kaikille viitetiedoille, mukaan lukien **Maksuehdot** (maksuehdot). Jos sinulla on jo alkuperäiset tiedot yhdessä järjestelmässä, tietueen pieni päivitystoiminto voi laukaista kaksoiskirjoitustoiminnon kyseiseen tietueeseen.

Sinun on noudatettava seuraavaa järjestystä ja varmistettava, että alkuperäiset tiedot ovat käytettävissä sekä sovelluksessa että Common Data Servicessä.

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
