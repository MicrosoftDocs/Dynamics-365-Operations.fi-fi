---
title: Kassavirtaennusteiden asetusten vianmääritys
description: Tässä aiheessa on vastauksia kysymyksiin, joita sinulla saattaa olla, kun määrität kassavirtaennusteita. Se käsittelee usein kysyttyjä kysymyksiä kassavirran asetuksista, kassavirran päivityksistä ja kassavirran Power BI -ominaisuuksista.
author: panolte
manager: AnnBe
ms.date: 12/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerCovParameters
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2020-12-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 89eb2f1bcfc73a6a7171a275532b2356e858e87c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985284"
---
# <a name="troubleshoot-cash-flow-forecasting-setup"></a>Kassavirtaennusteiden asetusten vianmääritys

[!include [banner](../includes/banner.md)]

Tässä aiheessa on vastauksia kysymyksiin, joita sinulla saattaa olla, kun määrität kassavirtaennusteita. Se käsittelee usein kysyttyjä kysymyksiä kassavirran asetuksista, kassavirran päivityksistä ja kassavirran Power BI -ominaisuuksista.

## <a name="why-is-cash-flow-shown-for-only-one-legal-entity"></a>Miksi kassavirta näkyy vain yhdessä yrityksessä?

Kassavirtaennusteet konfiguroitaan ja lasketaan yrityskohtaisesti. Power BI -raportit ja kassavirtaennusteiden ominaisuus taloushallinnon tiedoissa osoittavat tulokset.

Kassavirtaennusteet on määritettävä kullekin yritykselle, jota varten haluat nähdä ennusteen. Tarkista kaikkien yritysten kassavirtaennusteiden konfiguraatio. Vaihtoehtoisesti voit tarkistaa kaikkien yritysten kassavirtaennusteiden konfiguraatiot ja varmistaa, että ne on määritetty suunnitellulla tavalla.

## <a name="why-doesnt-power-bi-show-all-the-cash-flow-data"></a>Miksi Power BI ei näytä kaikkia kassavirtatietoja?

Useita vaiheita on suoritettava, ennen kuin kassavirtaennusteet voivat näkyä Power BI -näkymissä. Tarkista seuraava tarkistusluettelo ja varmista, että kaikki vaiheet on suoritettu loppuun:

- Määritä kunkin yrityksen kassavirta.
- Määritä kirjanpitoparametreissa järjestelmän valuutta ja järjestelmän vaihtokurssityyppi.
- Määritä kirjanpidon valuutta ja vaihtokurssityyppi.
- Anna tapahtumavaluutan ja kirjanpitovaluutan väliset valuutan vaihtokurssit.
- Anna kirjanpitovaluutan ja järjestelmävaluutan väliset valuutan vaihtokurssit.
- Anna kirjanpitovaluutan ja kunkin pankin valuutan väliset valuutan vaihtokurssit.

## <a name="why-did-cash-flow-power-bi-work-in-previous-versions-but-is-now-blank"></a>Miksi kassavirran Power BI toimi aiemmissa versioissa, mutta on nyt tyhjä?

Tarkista, että yksikkösäilön mitat "Kassavirran mitta V2" ja "LedgerCovLiquidityMeasurement" on konfiguroitu. Lisätietoja yksikkösäilön tietojen tarkastelemista varten on ohjeessa [Power BI:n integrointi yksikkösäilön kanssa](../../fin-ops-core/dev-itpro/analytics/power-bi-integration-entity-store.md). Varmista, että kaikki Power BI -sisällön tarkastelemisen edellyttämät vaiheet on suoritettu. Lisätietoja on kohdassa [Kassayhteenvedon Power BI -sisältö](Cash-Overview-Power-BI-content.md).

## <a name="have-the-entity-store-entities-been-refreshed"></a>Onko yksikkösäilön entiteetit päivitetty?

Entiteetit on päivitettävä säännöllisesti, jotta tiedot ovat ajan tasalla ja oikein. Jos haluat päivittää tietyn yksikön manuaalisesti, siirry kohtaan **Järjestelmänvalvonta \> Määritys \> Yksikkösäilö** valitse yksikkö ja sitten **Päivitä**. Tiedot voidaan myös päivittää automaattisesti. Määritä **Yksikkösäilö**-sivulla **Automaattinen päivitys käytössä** -asetuksen arvoksi **Kyllä**.
