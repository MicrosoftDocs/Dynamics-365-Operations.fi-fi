---
title: Finance Insightsin määritysongelmien vianmääritys
description: Tässä on aiheessa on luettelo ongelmista, joita voi esiintyä käytettäessä Finance Insights -ominaisuuksia Aiheessa käsitellään myös kyseisten ongelmien korjaamista.
author: panolte
ms.date: 08/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom:
- "14151"
- intro-internal
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2021-08-20
ms.dyn365.ops.version: AX 10.0.20
ms.openlocfilehash: 7ff42ffc334147c1a4c6b6349c86580df7f1955b
ms.sourcegitcommit: 47a3ad71210c7ac84d0c25e913c440b5ba205282
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/23/2021
ms.locfileid: "7512887"
---
# <a name="troubleshoot-finance-insights-setup-issues"></a>Finance Insightsin määritysongelmien vianmääritys

[!include [banner](../includes/banner.md)]

Tässä on aiheessa on luettelo ongelmista, joita voi esiintyä käytettäessä Finance Insights -ominaisuuksia Aiheessa käsitellään myös kyseisten ongelmien korjaamista.

## <a name="symptom-why-cant-i-map-the-customer-payment-insights-data-integration-template-destination-column"></a>Oire: Miksi asiakasmaksujen tietojen tietojen integrointimallin kohdesarakkeen yhdistämismääritys ei onnistu?

### <a name="resolution"></a>Ratkaisu

On mahdollista, että käytössä on aiemman version malli. Julkaisuversiota 10.0.17 edeltävät esiversion asiakkaat määrittivät tietojen integrointimallin **Asiakasmaksujen tietojen tulokset (CDS:stä Fin and Opsiin)** **Maksuennusteen tulos (esiversio)** -yksikön avulla Versioon 10.0.17 ja sitä myöhempään versioon tehdyn päivityksen jälkeen on yhdistämismääritykseen on käytettävä tietojen integrointimallia **Asiakasmaksujen tietojen tulokset (CDS:stä Fin and Opsiin sekä uudemmat)**. Tietojen integrointimallin kohdesarakkeen yhdistämismääritys ei ehkä ole mahdollista, ennen kuin tiedonhallinnan yksikköluettelo on päivitetty sisältämään **Maksuennusteen tulos** -yksikkö. Yksikköluettelon päivittämistä ja maksuennusten tuloksen näyttämistä varten on suoritettava ohjeiden mukaiset vaiheet Microsoft Dynamics 365 Financessa ja Dataversessa (jota kutsuttiin aiemmin Common Data Service \[CDS\] -hallintaportaaliksi).

### <a name="in-finance"></a>Finance

Suorita seuraavat vaiheet Financessa päivityksen jälkeen:

1. Valitse **Järjestelmänhallinta \> Työtilat \> Tietojen hallinta**.
2. Valitse **Tiedonhallinta**-työtilassa **Kehikkoparametrit**-ruutu.
3. Valitse **Tietojen tuonti- ja vientiympäristön parametrit** -sivulla **Yksikön asetukset** ja valitse sitten **Päivitä yksikköluettelo**.
4. Sulje **Tietojen tuonti- ja vientiympäristön parametrit** -sivu.
5. Valitse **Tiedonhallinta**-työtilassa **Tietoyksiköt**-ruutu.
6. Tee haku hakusanalla Maksuennusten tulos. Tarkista, että **Maksuennusten tulos** -yksikkö ei ole esiversio. Esiversion nimen lopussa on (esiversio). Jos vain yksikön esiversio on näkyvissä, ota yhteys Microsoftin tukeen.

### <a name="in-dataverse"></a>Dataverse -palvelussa

Päivitä tietojen integrointiprojektit seuraavien ohjeiden mukaisesti [Power Platform -hallintakeskuksessa](https://admin.powerplatform.microsoft.com/environments).

1. Jos käytössä on Finance Insights -esiversio, poista se tietojen integrointiprojekti, joka on liitetty **Asiakasmaksujen tietojen tulokset (CDS:stä Fin and Opsiin)** -malliin.
2. Toimi kohdassa [Tietojen integrointiprojektin luominen](create-data-integrate-project.md) annettujen ohjeiden mukaisesti. Käytä **Asiakasmaksujen tietojen tulokset (CDS:stä Fin and Opsiin versioon 10.0.17 ja sitä uudempiin versioihin)** -mallia.

## <a name="symptom-why-doesnt-the-cash-forecast-tab-in-the-cash-flow-forecast-workspace-show-any-data"></a>Oire: miksi Kassavirtaennuste-työtilan Kassavirtaennuste-välilehdessä ei ole tietoja?

### <a name="resolution"></a>Ratkaisu

Kassavirtaennustetoiminto on oltava otettuna käyttöön maksuliikenteen hallinnassa ja Finance Insights Kassavirtaennusteen -ominaisuus on määritettävä ja otettava käyttöön, jotta tiedot näkyvät oikein **Kassavirtaennuste**-työtilassa.

Ensimmäiseksi määritetään ja otetaan käyttöön kassavirtaennuste- ja maksuvalmiustilit. Lisätietoja on kohdassa [Kassavirtaennusteet](../cash-bank-management/cash-flow-forecasting.md). Jos nämä määrityksen on suoritettu mutta tulokset eivät vastaa odotuksia, lisätietoja on kohdassa [Kassavirtaennusteiden asetusten vianmääritys](../cash-bank-management/cash-flow-forecasting-tsg.md).

Seuraavaksi vahvistetaan, että Finance Insightsin Kassavirtaennusteet ominaisuus (**Maksuliikenteen hallinta \> Asetukset \> Finance Insights \> Kassavirtaennusteet**) on otettu käyttöön ja että tekoälymallin koulutus on suoritettu loppuun. Jos koulutus ei ole valmis, aloita mallin koulutusprosessi valitsemalla **Ennusta nyt**.
