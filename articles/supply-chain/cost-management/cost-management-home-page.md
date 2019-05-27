---
title: Kustannushintojen hallinnan aloitussivu
description: Kustannushintojen hallinnan avulla voit käsitellä raaka-aineiden, puolivalmiiden tuotteiden, valmiiden tuotteiden ja keskeneräisten resurssien arvostusta ja kirjanpitoa.
author: AndersGirke
manager: AnnBe
ms.date: 04/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fd94ae4c5ea855139fd1c41060de7db455ffab06
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1557636"
---
# <a name="cost-management-home-page"></a>Kustannushintojen hallinnan aloitussivu

[!include [banner](../includes/banner.md)]

[Kustannushintojen hallinnan (video)](https://www.youtube.com/watch?v=vXzlC-mOBcg&feature=youtu.be) avulla voit käsitellä raaka-aineiden, puolivalmiiden tuotteiden, valmiiden tuotteiden ja keskeneräisten resurssien arvostusta ja kirjanpitoa. Tässä prosessissa [varastokirjanpito](cost-object.md) ja [valmistuksen kirjanpito](bom-calculations.md) määritetään. Lisäksi niitä hallitaan ja niistä raportoidaan.

Voit määrittää kustannuskäytännöt seuraavilla alueilla: 
-  [Ennalta määritetty kustannus](costing-versions.md)
-  [Varastokirjanpito](cost-object.md)
-  [Valmistuksen kirjanpito](bom-calculations.md)
-  [Välillisten kustannusten laskenta](costing-sheets.md)
-  [Kirjanpidon integrointi](production-order-cost-analysis.md)

Voit esimerkiksi määrittää, mitä varastonarvostusmenetelmiä, kuten [FIFO](fifo-physical-value-marking.md), [Painotettu keskiarvo](weighted-average-physical-value-marking.md), [Standardikustannus](prerequisites-standard-costs.md) tai [Liukuva keskiarvo](moving-average.md), haluat käyttää tuotteisiin varastokirjanpidon [nimikemalliryhmässä](../inventory/reserve-inventory-quantities.md).

Voit käyttää varastokirjanpitoa ja valmistuksen kirjanpitoa **Kustannuslaskenta**- ja **Kustannusanalyysi**-työtiloissa. Näissä työtiloissa saa kattavan käsityksen tämän hetkisestä tilanteesta, tunnusluvuista ja mahdollisista poikkeamista. 

Valmistuksen kirjanpidossa voit käsitellä [työtilausten kustannuslaskentaa](production-order-cost-analysis.md) tuotanto- ja erätilauksissa sekä [jälkikustannuslaskentaan](backflush-costing.md) Lean-valmistuksessa.

[Kustannustenhallinnan Power BI -sisältö](../../dev-itpro/analytics/cost-management-content-pack.md) tarjoaa johdolle näkymän varastoon ja keskeneräisten töiden (KET) varastoon sekä niiden läpi kulkeviin kustannuksiin luokittain pitkällä aikavälillä. Näitä tietoja voidaan käyttää myös raportin yksityiskohtaisena täydennyksenä.

### <a name="additional-resources"></a>Lisäresurssit

#### <a name="whats-new-and-in-development"></a>Uudet ja kehitteillä olevat toiminnot

[Microsoft Dynamics 365 Tiekartta](https://roadmap.dynamics.com/) -sivustossa on lisätietoja julkaistuista ja kehitteillä olevista uusista toiminnoista. 

#### <a name="white-paper"></a>Tekninen raportti
[Tuoterakenteen laskenta kustannuslaskentalomakkeen avulla](https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/white-papers/365operationsbomcalsheet) on ohje, jossa selvitetään, miten materiaalin ja valmistuksen sisältävät kustannuslaskentalomakkeet määritetään ja miten määritys vaikuttaa tuorerakennelaskennan tuloksiin. Näitä ohjeaiheita selventämässä on konkreettisia skenaarioita ja tietoja, jotka osoittavat, mitä vaikutuksia eri asetuksilla ja määrityksillä on. Ei ole todennäköistä, että käytät näitä kaikkia skenaarioita, koska tässä asiakirjassa ei ole riittävästi ohjeita, niiden määrittämiseen. Jos sinulla kuitenkin on perustiedot, voit kokeilla alla olevien tehtäväoppaiden toistamista niiden esiintymisjärjestyksessä. Voit analysoida tuoterakennelaskennan tämän asiakirjan tietojen perusteella. 

-  [Valmiin tuotteen luominen](tasks/create-finished-product-2016-02.md)
-  [Puolivalmiin tuotteen luominen](tasks/create-semi-finished-product-2016-02.md)
-  [Raaka-aineiden luominen](tasks/create-raw-materials-2016-02.md)
-  [Tuoterakenteiden luominen](tasks/create-boms-2016-02.md)
-  [Luo reittejä](tasks/create-routes-2016-02.md)
-  [Tuoterakenteen laskeminen käyttämällä yhtä tasorakennetta](tasks/calculate-bom-single-level-structure-2016-02.md)
-  [Tuoterakenteen laskeminen käyttämällä monitasoista rakennetta](tasks/calculate-bom-multilevel-structure-2016-02.md)


#### <a name="blogs"></a>Blogit
Kustannushintojen hallintaa koskevia mielipiteitä, uutisia ja muita tietoja on [Dynamics AX:n valmistuksen tutkimus- ja kehitysryhmän blogissa](https://blogs.msdn.microsoft.com/axmfg) ja [Dynamics AX:n toimitusketjun hallinnan tutkimus- ja kehitysryhmän blogissa](https://blogs.msdn.microsoft.com/dynamicsaxscm). Vaikka monet kirjoitukset koskevat kustannushintojen hallinnan edellistä versiota, samoja käsitteitä käytetään edelleen ja menettelyt ovat samanlaisia myös nykyisessä versiossa.

#### <a name="task-guides"></a>Tehtäväoppaat
Finance and Operationsin tehtäväoppaissa on lisäohjeita. Voit avata tehtäväoppaan napsauttamalla Ohje-painiketta millä tahansa sivulla.

