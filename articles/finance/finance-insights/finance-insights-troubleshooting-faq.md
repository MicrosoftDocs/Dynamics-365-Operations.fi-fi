---
title: Finance Insightsin määritysongelmien vianmääritys
description: Tässä on aiheessa on luettelo ongelmista, joita voi esiintyä käytettäessä Finance Insights -ominaisuuksia Aiheessa käsitellään myös kyseisten ongelmien korjaamista.
author: panolte
ms.date: 11/03/2021
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
ms.openlocfilehash: 68115d484abcdc3c37357ae441e9f9ccb5212659
ms.sourcegitcommit: 6a9f068b59b62c95a507d1cc18b23f9fd80a859b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/20/2021
ms.locfileid: "7827050"
---
# <a name="troubleshoot-finance-insights-setup-issues"></a>Finance Insightsin määritysongelmien vianmääritys

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

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

## <a name="symptom-when-i-try-to-open-ai-builder-by-using-the-links-on-the-customer-payment-predictions-setup-page-why-do-i-receive-the-following-error-message-sorry-theres-been-a-disconnect"></a>Oire: Kun yritän avata AI Builderin Asiakkaan maksuennusteiden asetus -sivun linkkien avulla, miksi seuraava virhesanoma avautuu: Yhteys on valitettavasti katkaistu?

### <a name="resolution"></a>Ratkaisu

Dynamics 365 Finance -käyttäjillä on oltava ympäristön Microsoft Power Apps -käyttäjätili ja kyseisellä käyttäjätilillä on oltava järjestelmän mukauttajan rooli. Microsoft Power Appsin järjestelmänvalvoja voi luoda käyttäjätilin ja määrittää roolin. Voit sitten siirtyä sivustoon <https://make.preview.powerapps.com/>, kirjautua sisään käyttämällä kyseistä käyttäjätiliä ja kokeilemalla linkkejä uudelleen.

## <a name="symptom-why-doesnt-the-cash-forecast-tab-in-the-cash-flow-forecast-workspace-show-any-data"></a>Oire: miksi Kassavirtaennuste-työtilan Kassavirtaennuste-välilehdessä ei ole tietoja?

### <a name="resolution"></a>Ratkaisu

Kassavirtaennustetoiminto on oltava otettuna käyttöön maksuliikenteen hallinnassa ja Finance Insights Kassavirtaennusteen -ominaisuus on määritettävä ja otettava käyttöön, jotta tiedot näkyvät oikein **Kassavirtaennuste**-työtilassa.

Ensimmäiseksi määritetään ja otetaan käyttöön kassavirtaennuste- ja maksuvalmiustilit. Lisätietoja on kohdassa [Kassavirtaennusteet](../cash-bank-management/cash-flow-forecasting.md). Jos nämä määrityksen on suoritettu mutta tulokset eivät vastaa odotuksia, lisätietoja on kohdassa [Kassavirtaennusteiden asetusten vianmääritys](../cash-bank-management/cash-flow-forecasting-tsg.md).

Seuraavaksi vahvistetaan, että Finance Insightsin Kassavirtaennusteet ominaisuus (**Maksuliikenteen hallinta \> Asetukset \> Finance Insights \> Kassavirtaennusteet**) on otettu käyttöön ja että tekoälymallin koulutus on suoritettu loppuun. Jos koulutus ei ole valmis, aloita mallin koulutusprosessi valitsemalla **Ennusta nyt**.

## <a name="symptom-why-isnt-the-install-a-new-add-in-button-visible-in-microsoft-dynamics-lifecycle-services"></a>Oire: Miksi Microsoft Dynamics Lifecycle Services -palveluissa ei näy Asenna uusi lisäosa -painiketta?

### <a name="resolution"></a>Ratkaisu

Tarkista ensin, että **ympäristön esimiehen** tai **projektin omistajan** rooli on määritetty kirjautuneelle käyttäjälle Microsoft Dynamics Lifecycle Servicesin (LCS) **Projektin suojausrooli** -kentässä. Uusien lisäosien asennus edellyttää jonkin näistä projektin käyttöoikeusrooleista.

Jos sinulle on määritetty oikea projektin käyttöoikeusrooli, sinun on ehkä päivitettävä selaimen ikkuna, niin näkyviin tulee **Asenna uusi lisäosa** -painike.

## <a name="symptom-the-finance-insights-add-in-doesnt-seem-to-be-installing-why-is-that"></a>Oire: Finance Insights -lisäosa ei näytä asentuvan. Miksi?

### <a name="resolution"></a>Ratkaisu

Seuraavat vaiheet on suoritettava.

- Tarkista, että sinulla on **järjestelmänvalvojan** ja **järjestelmän mukauttajan** käyttöoikeus Power Portal -hallintakeskuksessa.
- Tarkista, että lisäosan asentavalla käyttäjällä on Dynamics 365 Finance -lisenssi tai vastaava lisenssi.
- Tarkista, että seuraava Azure AD -sovellus on rekisteröity Azure AD:ssä: 

  | Hakemus                  | Sovelluksen tunnus           |
  | ---------------------------- | ---------------- |
  | Microsoft Dynamics ERP Microservices CDS | 703e2651-d3fc-48f5-942c-74274233dba8 | 
  
