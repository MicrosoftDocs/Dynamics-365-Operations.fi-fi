---
title: Finance Insightsin määritysongelmien vianmääritys
description: Tässä artikkelissa on luettelo ongelmista, joita voi esiintyä käytettäessä Finance Insights -ominaisuuksia Aiheessa käsitellään myös kyseisten ongelmien korjaamista.
author: panolte
ms.date: 02/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom:
- "14151"
- intro-internal
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2021-08-20
ms.dyn365.ops.version: AX 10.0.20
ms.openlocfilehash: 1ee354a1c3d9b45eb12eeb3a6a29f2a6d5e4c34c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8846912"
---
# <a name="troubleshoot-finance-insights-setup-issues"></a>Finance Insightsin määritysongelmien vianmääritys

[!include [banner](../includes/banner.md)]

Tässä artikkelissa on luettelo ongelmista, joita voi esiintyä käytettäessä Finance Insights -ominaisuuksia Aiheessa käsitellään myös kyseisten ongelmien korjaamista.

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
  
## <a name="symptom-error-we-didnt-find-any-data-for-the-selected-filter-range-please-select-a-different-filter-range-and-try-again"></a>Oire: Virhe: "Ei löytynyt tietoja valitusta suodatinalueesta. Valitse toinen suodatusalue ja yritä uudelleen." 

### <a name="resolution"></a>Ratkaisu

Tarkista tietojen integroijan asetukset ja vahvista, että se toimii odotetulla tavalla, ja lisää (upsert) tiedot AI Builderista takaisin Financeen.  
Lisätietoja on kohdassa [Tietojen integrointiprojektin luominen](../finance-insights/create-data-integrate-project.md).

## <a name="symptom-customer-payment-prediction-training-failed-and-the-ai-builder-error-states-prediction-should-have-only-2-distinct-outcome-values-to-train-the-model-map-to-two-outcomes-and-retrain-training-report-issue-isnotminrequireddistinctnonnullvalues"></a>Oire: Asiakkaan maksujen ennusteen koulutus epäonnistui; AI Builder -virhe: "Ennusteilla tulisi olla vain kaksi erillistä tulosarvoa mallin kouluttamiseen. Määritä kaksi tulosta ja kouluta uudelleen", "Koulutusraportin ongelma: IsNotMinRequiredDistinctNonNullValues".

### <a name="resolution"></a>Ratkaisu

Tämä virhe ilmaisee, että viime vuonna ei ole tarpeeksi historiatapahtumia, jotka kuvaavat jokaista **Ajoissa**-, **Myöhässä**- ja **Erittäin myöhässä** -luokissa kuvattua luokkaa. Voit ratkaista virheen oikaisemalla **Erittäin myöhässä** -tapahtumakauden. Jos **Erittäin myöhässä** -tapahtumakauden oikaiseminen ei korjaa virhettä, **Asiakkaan maksuennusteet** eivät ole paras ratkaisu, koska ne tarvitsevat tietoja kussakin luokassa koulutustarkoituksiin.

Lisätietoja **Ajoissa**-, **Myöhässä**- ja **Erittäin myöhässä** -luokkien oikaisemisesta on kohdassa [Asiakkaan maksuennusteiden ottaminen käyttöön](../finance-insights/enable-cust-paymnt-prediction.md).

## <a name="symptom-model-training-failed"></a>Oire: Mallin koulutus epäonnistui

### <a name="resolution"></a>Ratkaisu

**Kassavirtaennuste**-mallin koulutus vaatii tietoja, jotka kattavat yli vuoden ja sisältävät vähintään 100 tapahtumaa. On suositeltavaa, että käytettävissä on vähintään kahden vuoden edestä tietoja ja yli 1 000 tapahtumaa.

**Asiakkaan maksuennusteet**-toiminto edellyttää yli 100 tapahtumaa 6–9 edellisen kuukauden ajalta. Tapahtumia voivat olla esimerkiksi vapaatekstilaskut, myyntitilauksia ja asiakasmaksut. Tietojen on oltava jaettuna **Määritys**-sivulla määritettyjen asetusten **Ajoissa**, **Myöhässä** ja **Paljon myöhässä** kesken.    

**Budjettiehdotus**-toiminto edellyttää vähintään kolmen vuoden budjetti- tai toteutuneita tietoja. Tämän ratkaisun ennusteissa käytetään 3–10 vuoden edestä tietoja. Tulokset ovat parempia, jos tietoja on yli kolmen vuoden ajalta. Tiedot itse toimivat parhaiten, kun arvoissa on vaihtelua. Jos tiedot sisältävät vain vakiomallisia tietoja, kuten vuokrakuluja, opetus voi epäonnistua, koska vaihtelun puute ei edellytä, että tekoäly ennustaisi määriä.

## <a name="symptom-error-message-states-that-the-table-with-name-msdyn_paypredpredictionresultentities-does-not-exist-the-remote-server-returned-an-error-404-not-found"></a>Oire: Virhesanoma "Taulukkoa nimellä msdyn_paypredpredictionresultentities ei ole olemassa. Etäpalvelin palautti virheen: (404) Ei löydetty..."

### <a name="resolution"></a>Ratkaisu

Ympäristö on saavuttanut Data Lake -palvelujen taulukoiden enimmäismäärän rajan. Lisätietoja: **Ota käyttöön lähes reaaliaikaiset tietomuutokset** -osa artikkelissa [Azure Data Lakeen viemisen yleiskuvaus](../../fin-ops-core/dev-itpro/data-entities/Azure-Data-Lake-GA-version-overview.md).
