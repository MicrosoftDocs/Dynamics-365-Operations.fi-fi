---
title: Prosessin automaation aktivoiminen laatutilausten luontia varten
description: Tämä aihe tarjoaa resursseja Power Automaten käyttämiseen liiketoimintaprosessien automatisointiin laatutilausten esimerkin avulla.
author: cabeln
ms.date: 05/28/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: cabeln
ms.search.validFrom: 2021-05-28
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: f35adab3075ba810964a41899ba95ae40c115e83
ms.sourcegitcommit: 588f8343aaa654309d2ff735fd437dba6acd9d46
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/28/2021
ms.locfileid: "6115180"
---
# <a name="invoke-process-automation-flows-to-create-quality-orders"></a>Prosessin automaation aktivoiminen laatutilausten luontia varten

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Organisaatioiden tarve standardiprosessien automatisoinnissa, henkilökunnan kätevämpi vuorovaikutus sekä erilaisten tietojen käyttö ja liiketoimintaprosessien automaattinen ajaminen edellyttävät organisaatioiden välistä tiedonsiirtoa. Ohjelmistorobotiikan (RPA) ja Microsoft Power Automaten avulla yritykset voivat käyttää koodittomia kokemuksia toistuvien prosessien automatisoimiseksi, mikä parantaa tehokkuutta ja tarkkuutta.

Supply Chain Managementin ladattavan automaatioratkaisun mallissa näytetään esimerkiksi, miten Power Automatea voidaan käyttää liiketoimintaprosessien automatisointiin laatutilausten avulla.

Voit ladata automaatioratkaisun mallin [tästä](https://aka.ms/D365SCMQualityOrderRPASolution).

Yleisiä tietoja tästä ominaisuudesta ja sen ominaisuuksista on seuraavassa videossa: [RPA:n käyttäminen laatutilausten luomiseen Dynamics 365 Supply Chain Managementissa](https://www.youtube.com/watch?v=LFbzJ6-H89w)

![Automaatioasetukset ja RPA](media/rpa-automation-options.png "Automaatioasetukset ja RPA")

Power Automate -ratkaisumalli sisältää pilvipalvelutyönkulun ja työpöytätyönkulun automaation, joka automatisoi laatutilausten luonnin Supply Chain Managementissa.

Automaation voi aloittaa vastauksena moniin tapahtumiin ja signaaleihin, mukaan lukien käyttäjän syötön tai konesignaalit (kuten esineiden Internet (IoT)). *Q-Order* Power Application -esimerkki sisältyy ratkaisumalliin. Sen avulla käyttäjä voi skannata nimikkeen QR-koodin, lisätä määrän ja liittää kuvia käyttämällä kameraa.

Mukana on ratkaisuparametreja, jotka määrittävät automaation tiettyä käyttötapausta varten tuotantolaitoksessa.

![Luo laatutilaus](media/rpa-create-quality-roder.png "Luo laatutilaus")

Täydellinen vaiheittainen opas siitä, kuinka ladataan, asennetaan ja käytetään malliratkaisua tilausten laadun automatisointiin, on kohdassa [Automaattisen laatutilauksen luominen Dynamics 365 Supply Chain Managementissa ohjelmistorobotiikan avulla käyttäen Power Automate Desktopia](/power-automate/desktop-flows/dynamics365-scm-rpa).

