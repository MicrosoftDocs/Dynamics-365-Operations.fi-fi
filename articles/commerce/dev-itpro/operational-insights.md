---
title: Käyttöön perustuvien näkemysten määrittäminen
description: Tässä artikkelissa käsitellään Käyttöön perustuvat näkemykset -ominaisuuden määrittämistä Microsoft Dynamics 365 Commercessa.
author: ashishMSFT
ms.date: 12/07/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: ca0d31e403275d6131fa6d53f0a7b46a7ddb651d
ms.sourcegitcommit: 0c927fcb3afd34d870391f05b5393a4673d916e5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/08/2022
ms.locfileid: "9832120"
---
# <a name="set-up-operational-insights"></a>Käyttöön perustuvien näkemysten määrittäminen

[!include [banner](../includes/banner.md)]

Tässä artikkelissa käsitellään Käyttöön perustuvat näkemykset -ominaisuuden määrittämistä Microsoft Dynamics 365 Commercessa.

Käyttöön perustuvat näkemykset on Dynamics 365 Commerce -ominaisuus, joka on suunniteltu parantamaan asiakkaiden näkyvyyttä palvelun kuntoon ja liiketoiminnan toimintoihin. Tämä onnistuu lähettämällä telemetriatietoja suodaan asiakkaan omistamalle Application Insights -tilille.

Kun ympäristöjen Käyttöön perustuvat näkemykset -ominaisuus on otettu käyttöön Commerce headquartersissa, valikoituun tapahtumaluetteloon voidaan kerätä tapahtumia Commerce Scale Unitista (CSU) ja myyntipisteen laitteista. Nämä tapahtumat auttavat hahmottamaan entistä paremmin, mikä on järjestelmien suorituskykyä. Niiden avulla voi myös seurata keskeisiä teknisiä ja liiketoiminnan mittareita.

Vaikka näitä telemetriatietoja ei kerättäisi koko ajan, kokoelman nopeasta käyttöönottamisesta tai käytöstäpoistamisesta tietyissä ympäristöissä on hyötyä. Telemetriasta on tällä tavoin apua vianmäärityksessä tai virheenkorjauksessa kehitystyön aikana tai tuotantoympäristössä.

## <a name="access-logs-in-application-insights"></a>Application Insightsin lokien käyttäminen

Commerce CSU- ja myyntipistekomponenttien diagnostiikkatapahtumien lokeja voi käyttää Application Insightsin kautta suorittamalla tämän osan toimenpiteet.

### <a name="minimum-version-requirements-for-csu"></a>CSU-version vähimmäisvaatimukset

CSU-version vähimmäisvaatimukset ovat seuraavat:

- 10.0.23 (Retail Server -versio 9.33.22062.15 ja uudempi)
- 10.0.24 (Retail Server -versio 9.34.22062.14 ja uudempi)
- 10.0.25 (Retail Server -versio 9.35.22062.13 ja uudempi)
- 10.0.26 ja uudempi (kaikki versiot)

### <a name="enable-diagnostic-events-in-application-insights"></a>Diagnostiikkatapahtumien ottaminen käyttöön Application Insightsissa

> [!IMPORTANT]
> Jos aiemmin oli käytössä Käyttöön perustuvat näkemykset -esiversio, Käyttöön perustuvat näkemykset -ominaisuus on otettava käyttöön seuraavien ohjeiden mukaisesti. Näin voidaan varmistaa, että tapahtumia voi jatkossakin käyttää luotettavasti ja turvallisesti.

Commerce-komponentin diagnostiikkatapahtumien käyttöönottamiseen tarvitaan Application Insights -tili. Se voi olla aiemmin luotu tili tai [tili voidaan luoda uutena](/azure/azure-monitor/app/create-workspace-resource#create-workspace-based-resource). Tietosuojan vuoksi on suositeltavaa käyttää erillisiä Application Insights -tilejä tuotanto-, eristys- ja kehitysympäristöjä varten. Tilin luonnin jälkeen **Käyttöön perustuvat näkemykset** -ominaisuus on otettava käyttöön Headquartersissa.

Diagnostiikkatapahtumat otetaan käyttöön Application Insightsissa seuraavasti.

1. Avaa Headquartersissa **Ominaisuuksien hallinta** -työtila ja ota **Käyttöön perustuvat näkemykset** -ominaisuus käyttöön.
1. Valitse **Järjestelmänvalvonta \> Asetukset \> Käyttöön perustuvat näkemykset**.
1. Määritä **Määritykset**-välilehden **Commerce-kanavan tapahtumat** -asetukseksi **Kyllä**.
1. Syötä **Ympäristöt**-välilehdessä **LCS-ympäristön tunnus**- ja **Ympäristön tila** -arvot jokaiselle ympäristölle, jossa Application Insightsia on tarkoitus käyttää. Kunkin ympäristön ympäristötunnus löytyy kyseisen ympäristön **Ympäristöön tiedot** -sivulta Microsoft Dynamics Lifecycle Servicesissä. Tämä vaihe on pakollinen, sillä se estää diagnostiikkatapahtumien lähettämisen vahingossa väärään ympäristöön, kun tietokannan kopiointitoimintoja suoritetaan.
1. Määritä **Application Insights -rekisteri** -välilehdessä Application Insightsin **Instrumentointiavain**-arvo ja sen ympäristön vastaava **Ympäristön tila** -arvo, jossa kutakin Application Insights -tiliä on tarkoitus käyttää.
1. Kun edellä olevat määritykset on tehty, **CDX-työ 1110** on suoritettava. Työ voidaan jättää suoritettavaksi sen aikataulun mukaisesti, tai se voidaan suorittaa manuaalisesti.
1. Valitse Lifecycle Servicesissä **Ympäristön tiedot \> Commerce \> Hallinta**, valitse CSU-esiintymä ja valitse lopuksi **Käynnistä uudelleen**. Toista tämä vaihe kunkin CSU:n osalta.
1. Toista edellä olevat vaiheet kussakin ympäristössä, jossa Application Insightsia on tarkoitus käyttää.

> [!NOTE]
> - Käyttöön perustuvat näkemykset -ominaisuuden telemetriatapahtuvat voivat muuttua. Käyttöön perustuvat näkemykset -tapahtumia on suositeltavaa käyttää itse tehtävään alustavaan analyysiin ja vianmääritykseen mutta ei koontinäyttöjen tai hälytysten määrittämiseen. Jos tapahtumia käytetään muutoin kuin omatoimiseen vianmääritykseen, kyselyt kannattaa tarkistaa ja päivittää kunkin CSU- tai myyntipistejulkaisun jälkeen:
> - Commercen versiosta 10.0.29 alkaen tässä osassa käsitellyt menettelyt mahdollistavat myös myyntipisteen Käyttöön perustuvat näkemykset -tapahtumien suoratoiston Application Insights -tilille. Lisätietoja on kohdassa [Myyntipisteen Käyttöön perustuvat näkemykset -ominaisuus – tapahtumat ja kyselyt](https://download.microsoft.com/download/9/2/b/92be35b0-0e24-4a4d-940d-6f4db29791c0/Operational-Insights-Commerce-POS-events-queries.pdf).

#### <a name="use-the-dllhostexeconfig-file-to-control-pos-operational-insights-events"></a>Myyntipisteen Käyttöön perustuvat näkemykset -tapahtumien hallinta DLLHost.exe.config-tiedoston avulla

Myyntipisteen Käyttöön perustuvat näkemykset -tapahtumien voi hallinta DLLHost.exe.config-tiedoston avulla seuraavasti.

1. Avaa **DLLHost.exe.config**-tiedosto tekstieditorissa kansiossa **C:\\Program Files (x86)\\Microsoft Dynamics 365\\70\\Retail Modern POS\\ClientBroker**.
1. Poista **diagnosticsSection**-osassa sink XML -elementti, jonka luokkanimi on **Microsoft.Dynamics.Retail.Diagnostics.OperationalInsights.OperationalInsightsLogger**.
1. Tallenna tiedosto.

### <a name="disable-diagnostic-events-in-application-insights"></a>Diagnostiikkatapahtumien poistaminen käytöstä Application Insightsissa

> [!IMPORTANT]
> Jos diagnostiikkatapahtumat halutaan poistaa käytöstä eikä niitä enää lähetetä Application Insightsiin, on toimittava seuraavasti. Ominaisuutta ei voi vain poistaa käytöstä ominaisuuksien hallinnassa.

Diagnostiikkatapahtumat poistetaan käytöstä Application Insightsissa seuraavasti.

1. Valitse Headquartersissa **Järjestelmänvalvonta \> Käyttöön perustuvat näkemykset**.
1. Määritä **Määritykset**-välilehden **Commerce-kanavan tapahtumat** -asetukseksi **Ei**.
1. Kun edellä olevat määritykset on tehty, **CDX-työ 1110** on suoritettava. Työ voidaan jättää suoritettavaksi sen aikataulun mukaisesti, tai se voidaan suorittaa manuaalisesti.
1. Valitse Lifecycle Servicesissä **Ympäristön tiedot \> Commerce \> Hallinta**, valitse CSU-esiintymä ja valitse lopuksi **Käynnistä uudelleen**. Toista tämä vaihe kunkin CSU:n osalta.
1. Toista edellä olevat vaiheet kussakin ympäristössä, jossa Application Insights on tarkoitus poistaa käytöstä.

Diagnostiikkatapahtumat voidaan poistaa käytöstä yhdessä ympäristössä poistamalla instrumentointiavain **Käyttöön perustuvat näkemykset** -sivun **Application Insights -rekisteri** -välilehdessä. Sen jälkeen suoritetaan edellisen menettelyn vaiheet 3 ja 4.

> [!NOTE]
> Commercen versiossa 10.0.29 ja sitä uudemmissa versioissa tässä osassa käsitellyt vaiheet poistavat käytöstä myös myyntipisteen Käyttöön perustuvat näkemykset -tapahtumien suoratoiston Application Insights -tilille. 
