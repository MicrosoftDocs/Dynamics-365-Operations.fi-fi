---
title: Kassavirtaennusteiden asetusten vianmääritys
description: Tässä aiheessa on vastauksia kysymyksiin, joita sinulla saattaa olla, kun määrität kassavirtaennusteita. Se käsittelee usein kysyttyjä kysymyksiä kassavirran asetuksista, kassavirran päivityksistä ja kassavirran Power BI -ominaisuuksista.
author: panolte
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerCovParameters
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2020-12-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: e2b5a8df84ff5159a85526251a6367857afa1808
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/07/2022
ms.locfileid: "8724567"
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

Tarkista, että yksikkösäilön mitat "Kassavirran mitta V2" ja "LedgerCovLiquidityMeasurement" on konfiguroitu. Lisätietoja yksikkösäilön tietojen ksäittelystä on kohdassa [Power BI:n ja yksikkösäilön integrointi](../../fin-ops-core/dev-itpro/analytics/power-bi-integration-entity-store.md). Varmista, että kaikki Power BI -sisällön tarkastelemiseen tarvittavat vaiheet on suoritettu. Lisätietoja on kohdassa [Kassayhteenvedon Power BI -sisältö](Cash-Overview-Power-BI-content.md).

## <a name="have-the-entity-store-entities-been-refreshed"></a>Onko yksikkösäilön entiteetit päivitetty?

Entiteetit on päivitettävä säännöllisesti, jotta tiedot ovat ajan tasalla ja oikein. Jos haluat päivittää tietyn yksikön manuaalisesti, siirry kohtaan **Järjestelmänvalvonta \> Määritys \> Yksikkösäilö** valitse yksikkö ja sitten **Päivitä**. Tiedot voidaan myös päivittää automaattisesti. Määritä **Yksikkösäilö**-sivulla **Automaattinen päivitys käytössä** -asetuksen arvoksi **Kyllä**.

## <a name="which-calculation-method-should-be-used-when-calculating-cash-flow-forecasts"></a>Mitä laskentamenetelmää tulisi käyttää kassavirtaennusteita laskettaessa?

Kassavirtaennusteen laskentamenetelmässä on kaksi tärkeää valintavaihtoehtoa. **Uusi**-vaihtoehto laskee kassavirtaennusteet uusille asiakirjoille ja asiakirjoille, jotka ovat muuttuneet edellisen eräajon jälkeen. Tämä asetus suoritetaan yleensä nopeammin, koska se käsittelee pienemmän asiakirjajoukon. **Yhteensä**-vaihtoehto laskee uudelleen kassavirtaennusteet järjestelmän jokaiselle asiakirjalle. Tämä vaihtoehto vie enemmän aikaa, koska sillä on enemmän työtä suoritettavana.

### <a name="how-do-i-improve-the-performance-of-the-cash-flow-forecasting-recurring-batch-job"></a>Miten parannan kassavirtaennusteen toistuva eräajon suorituskykyä?

Suosittelemme, että kassavirtaennuste suoritetaan kerran päivässä ruuhka-aikojen ulkopuolella **Uusi**-laskentamenetelmällä. Suosittelemme käyttämään tätä lähestymistapaa 6 päivänä viikossa. Suorita sitten kassavirtaennuste kerran viikossa käyttämällä **Yhteensä**-laskentamenetelmää päivänä, jolloin on vähiten aktiviteettia.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

