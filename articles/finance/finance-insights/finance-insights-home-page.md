---
title: Finance Insights -kotisivu
description: Finance Insights sisältää määritettävät ja laajennettavat mallit, joiden avulla yrityksen kassavirta voidaan ennustaa tarkasti ja älykkäästi silloin, kun selvittämättömien saatavien maksu vastaanotetaan. Se auttaa myös budjetointiprosessia nopeuttavan budjettiesityksen luomisessa. Kaikki nämä ominaisuudet perustuvat älykkäisiin koneoppimismalleihin.
author: ShivamPandey-msft
ms.date: 11/15/2021
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
ms.search.validFrom: 2020-07-20
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: dfc4d9cb5be4d8d287122fd33bf09b0570498169
ms.sourcegitcommit: a46f0bf9f58f559bbb2fa3d713ad86875770ed59
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/15/2021
ms.locfileid: "7813744"
---
# <a name="finance-insights-home-page"></a>Finance Insightsin aloitussivu

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Finance Insights sisältää määritettävät ja laajennettavat ratkaisut, joiden avulla yrityksen kassavirta voidaan ennustaa ja älykkäästi silloin, kun selvittämättömien saatavien maksu vastaanotetaan. Se auttaa myös budjetointiprosessia nopeuttavan budjettiesityksen luomisessa. Näissä ominaisuuksissa käytetään koneoppimisen mallipohjia mallien luomiseen tietojasi käyttäen (mukaan lukien tiedot kolmannelta osapuolelta, kuten toimiston kulutusraportit). Nämä älykkäät toiminnot antavat tietoja päätöksentekoon ja auttavat sinua vastaamaan tehokkaasti nykyisiin ja odotettuihin liiketoimintaominaisuuksiin. Olet vastuussa kaikista Finance Insightsissa käytetyistä tiedoista ja sen tuottamista tiedoista.

> [!NOTE]
> Finance Insightsin esiversio on saatavilla käyttöön otettavaksi Yhdysvalloissa, Kanadassa, Yhdistyneessä kuningaskunnassa, Euroopassa, Aasian ja Tyynenmeren alueella, Japanissa, Australiassa ja Uudessa-Seelannissa. Microsoft lisää tukea jatkuvasti myös muilla alueilla.

## <a name="prerequisites"></a>Edellytykset

Tässä ohjeaiheessa luetellaan Finance Insightsin käyttövaatimukset. Lisätietolinkit ovat käytettävissä aina, kun se on mahdollista.

### <a name="legal-requirements"></a>Lakisääteiset vaatimukset

Voit hakea esiversio-ohjelman käyttäjäksi täyttämällä [Finance Insightsin esiversio Dynamics 365 Financea varten -sopimuksen](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUM1c0Uzc1RFpaU1RVTEwxVTNWUERPRThUSy4u).

### <a name="system-requirements"></a>Järjestelmävaatimukset

Finance Insightsin esikatselu edellyttää Taso 2 -ympäristön (useita paketteja) käyttämistä. Ympäristöjen taustatietoja on kohdassa [Ympäristön suunnittelu](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).

### <a name="version-requirements"></a>Version vaatimukset

Tämä aihe koskee Microsoft Dynamics 365 Financen versiota 10.0.21 ja sitä uudempia versioita.

### <a name="historical-data-requirements"></a>Aiemmat tietovaatimukset

Asiakkaan maksuennusteet -toiminnossa käytettävän koneoppimismallin onnistunut kouluttaminen edellyttää myyntilaskuja vähintään vuoden ajalta. Kassavirtaennusteita varten suositellaan kolmen vuoden historiatietoja. Älykkäisiin budjettiehdotuksiin suositellaan kolmen vuoden historiallisia ja/tai toteutuneita budjetteja.

## <a name="configure-finance-insights"></a>Finance Insightsin määrittäminen

Määritysvaiheet on suoritettava ennen Finance Insightsin käyttämistä. Lisätietoja Finance Insightsin määrittämisestä on kohdassa [Finance Insightsin määrittäminen](configure-for-fin-insites.md).

## <a name="create-a-data-integrator-project"></a>Tietojen integrointiprojektin luominen

Luo tietojen integrointiprojekti, jotta koneoppimismallin luomat tiedot voidaan siirtää Dynamics 365 Financeen. Projektin luontivaiheet ovat kohdassa [Tietojen integrointiprojektin luominen](create-data-integrate-project.md).

## <a name="enable-finance-insights-capabilities"></a>Finance Insightsin ominaisuuksien käyttöönotto

Kun olet tehnyt määritysvaiheet ja määrittänyt esittelytiedot, ota kaikki seuraavat käyttöön tulevat ominaisuudet käyttöön ja määritä ne: asiakkaan maksuennusteet, kassavirran ennustaminen ja budjettiesitykset.

### <a name="enable-customer-payment-predictions"></a>Asiakkaan maksuennusteiden ottaminen käyttöön
Jos käytät esittelytietoja asiakkaan maksuennusteiden testaamisessa, tuo lisää esittelytietoja. Tämän jälkeen tekoälymallin luominen onnistuu. 

Jos haluat ottaa käyttöön asiakkaan maksuennusteet, tee sen koneoppimismallin luontivaiheet valmiiksi, joka käyttää organisaation tietoja luodessaan ennusteita siitä, milloin asiakkaat aikovat maksaa maksamattomat laskut ja milloin tietyt laskut todennäköisesti maksetaan. Lisätiedot ja tietyt suoritettavat vaiheet ovat kohdassa [Asiakkaan maksuennusteiden käyttöönotto](enable-cust-paymnt-prediction.md). 

### <a name="enable-cash-flow-forecasting"></a>Kassavirtaennusteiden ottaminen käyttöön
Jos haluat ottaa käyttöön kassavirtaennusteet, tee sen koneoppimismallin luontivaiheet valmiiksi, joka käyttää organisaation tietoja luodessaan kassavirtaennusteita. Lisätiedot ja tietyt suoritettavat vaiheet ovat kohdassa [Kassavirtaennusteiden käyttöönotto](enable-cash-flow-forecasting.md).

### <a name="enable-budget-proposals"></a>Budjettiehdotusten käyttöönotto

Budjettiehdotukset-ominaisuus käyttää koneoppimismallia ja organisaation historiallisia tietoja budjettiehdotuksen luomisessa. Luodun ehdotuksen avulla voit aloittaa budjetointiprosessin, joka on tehokkaampi kuin manuaalinen prosessi. Lisätietoja tämän ominaisuuden käyttöönotosta on kohdassa [Budjettiehdotusten käyttöönotto](enable-budget-proposal.md). 

## <a name="using-finance-insights-features"></a>Finance Insights -ominaisuuksien käyttäminen

### <a name="using-customer-payment-predictions"></a>Asiakkaan maksuennusteiden käyttäminen

- Lisätietoja asiakkaan maksuennusteista saatavista tiedoista, joita tarvitaan perintätehtävien ennakoivaa aloittamista varten, on kohdassa [Asiakkaan maksuennusteiden käyttäminen](use-customer-payment-predictions.md).
- Lisätietoja ennustemallin tehokkuuden arvioimisesta ominaisuuden käyttöönoton jälkeen on kohdassa [Alkuperäisen asiakkaan maksuennustemallin arvioiminen](evaluate-payment-prediction.md).
- Lisätietoja ennusteen luomisessa käytettyjen tietojen muokkaamisesta ja ennusteen tehokkuuden parantamisesta on kohdassa [Ennustemallin parantaminen](improve-model.md).
- Lisätietoja tekoälyennustemallien tuloksista on kohdassa [Koneoppimismallien tulokset](confusion-matrix.md).

### <a name="using-cash-flow-forecasts"></a>Kassavirtaennusteiden käyttäminen

Kassavirtaennusteominaisuus voi auttaa kassatilanteen tarkemmassa arvioimisessa. Älykäs kassavirtaennuste on luotu Dynamics 365 Financen olemassa olevan kassavirtaennustetoiminnon pohjalta. Lisätietoja olemassa olevan ominaisuuden tarkastelemisesta on kohdassa [Kassavirtaennusteet](../cash-bank-management/cash-flow-forecasting.md).

- Lisätietoja kassavirtaennusteiden uusista ominaisuuksista on kohdassa [Kassavirtaennuste](cash-flow-forecast-intro.md).
- Lisätietoja ulkoisten tietojen tuomisesta kassavirtaennusteeseen on kohdassa [Ulkoisten tietojen käyttäminen kassavirtaennusteissa](external-data-in-cash-flow.md). 
- Lisätietoja tekoälymallin käyttämisessä lähitulevaisuuden kassavirran ennustamisessa on kohdassa [Kassatilanne](cash-position.md).
- Lisätietoja kassavirtatilanteiden ja kassavirtaennusteiden tallentamisesta tilannevedoksina ja tilannevedosten vertaamisesta todelliseen tilanteeseen on kohdassa [Tilannevedosten yleiskatsaus](payment-snapshots.md).

### <a name="using-budget-proposal"></a>Budjettiehdotuksen käyttäminen

Lisätietoja budjetin luomisen nopeuttamisesta on kohdassa [Budjettiehdotukset](budget-proposals.md). 

## <a name="feedback-and-support"></a>Palaute ja tuki

Lähetä sähköpostia [Finance Insightsiin](mailto:fiap@microsoft.com), jos haluat antaa palautetta tai tarvitset tukea.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
