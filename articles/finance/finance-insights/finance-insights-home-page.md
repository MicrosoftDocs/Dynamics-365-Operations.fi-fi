---
title: Finance Insightsin aloitussivu (esiversio)
description: Finance Insights sisältää määritettävät ja laajennettavat mallit, joiden avulla yrityksen kassavirta voidaan ennustaa tarkasti ja älykkäästi silloin, kun selvittämättömien saatavien maksu vastaanotetaan. Se auttaa myös budjetointiprosessia nopeuttavan budjettiesityksen luomisessa. Kaikki nämä ominaisuudet perustuvat älykkäisiin koneoppimismalleihin.
author: ShivamPandey-msft
ms.date: 07/16/2021
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
ms.openlocfilehash: 2086a33285d9a529480c5f34fb048105e65c2046
ms.sourcegitcommit: e42c7dd495829b0853cebdf827b86a7cf655cf86
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/17/2021
ms.locfileid: "6638511"
---
# <a name="finance-insights-home-page-preview"></a>Finance Insightsin aloitussivu (esiversio)

[!include [banner](../includes/banner.md)]

Finance Insights sisältää määritettävät ja laajennettavat mallit, joiden avulla yrityksen kassavirta voidaan ennustaa tarkasti ja älykkäästi silloin, kun selvittämättömien saatavien maksu vastaanotetaan. Se auttaa myös budjetointiprosessia nopeuttavan budjettiesityksen luomisessa. Kaikki nämä ominaisuudet perustuvat älykkäisiin koneoppimismalleihin. Kun nämä uudet ominaisuudet yhdistetään automaation kanssa toimittajan maksuissa ja perinnöissä, saadaan aikaan monipuolinen ja älykäs talousjärjestelmä. Se auttaa päätöstenteossa ja nykyisten ja odotettavissa olevien liiketoimintahaasteiden tehokkaassa käsittelemisessä.

> [!NOTE]
> Finance Insightsin esiversio on saatavilla käyttöön otettavaksi Yhdysvalloissa, Kanadassa, Yhdistyneessä kuningaskunnassa, Euroopassa, Aasian ja Tyynenmeren alueella, Australiassa ja Uudessa-Seelannissa. Microsoft lisää tukea jatkuvasti myös muilla alueilla. Jos haluat ottaa Finance Insightsin käyttöön tuotantoympäristöissä, [Vie Data Lakeen](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md) -ominaisuudet tulee ottaa ensin käyttöön tuotantoympäristössä.

> [!NOTE]
> Tätä toimintoa tarjotaan esikatselutoimintojen joukkona. Esiversiotoimintoa ei tule käyttää tuloksena syntyneissä koneoppimismalleissa, jotka edistävät tai vaikuttavat liiketoimintapäätöksiin tai budjetointiehdotuksiin. Tämän ominaisuuden käyttö määräytyy [Täydentävien käyttöehtojen](https://go.microsoft.com/fwlink/?linkid=2105274) mukaan.

## <a name="prerequisites"></a>Edellytykset

Tässä ohjeaiheessa luetellaan Finance Insightsin käyttövaatimukset. Lisätietolinkit ovat käytettävissä aina, kun se on mahdollista.

### <a name="legal-requirements"></a>Lakisääteiset vaatimukset

Voit hakea esiversio-ohjelman käyttäjäksi täyttämällä [Finance Insightsin esiversio Dynamics 365 Financea varten -sopimuksen](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUM1c0Uzc1RFpaU1RVTEwxVTNWUERPRThUSy4u).

### <a name="system-requirements"></a>Järjestelmävaatimukset

Finance Insightsin esikatselu edellyttää Taso 2 -ympäristön (useita paketteja) käyttämistä. Ympäristöjen taustatietoja on kohdassa [Ympäristön suunnittelu](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).

### <a name="version-requirements"></a>Version vaatimukset

Tämä asiakirja koskee Finance and Operations -sovellusten (Platform update 35) versiota 10.0.11 ja uudempia versioita.

### <a name="historical-data-requirements"></a>Aiemmat tietovaatimukset

Asiakkaan maksuennusteet -toiminnossa käytettävän koneoppimismallin onnistunut kouluttaminen edellyttää myyntilaskuja vähintään vuoden ajalta.

### <a name="role-and-permission-requirements"></a>Rooli- ja käyttöoikeusvaatimukset

Microsoft Dynamics 365 Financeen, Microsoft Dynamics Lifecycle Servicesiin (LCS), Power Appsiin ja Azureen tehdään muutoksia. Näissä ympäristöissä tarvitaan oikeat käyttöoikeudet. Tässä on joitakin esimerkkejä tulevista muutoksista:

- Microsoft Power Platformiin luodaan uusi ympäristö.
- Azuressa luodaan tallennustili, avainsäilö ja sovellus.
- Active Directoryn vuokraajan järjestelmänvalvojan on annettava AI Builder -sovellukselle Data Laken käyttöoikeus.
- Toiminto otetaan käyttöön Dynamics 365:ssä.

Azuren, Microsoft Dataversen ja LCS:n resurssien luonti- ja hallintakokemus auttaa tässä prosessissa.

## <a name="configure-finance-insights"></a>Taloushallinnon tietojen määrittäminen

Sinun on suoritettava joitakin määritysvaiheita, ennen kuin voit käyttää Finance Insightsia. Lisätietoja Finance Insightsin määrittämisestä:
  - Versioille 10.0.19 asti: [Finance Insightsin (esiversio) määritys versioon 10.0.19 asti](configure-for-fin-insites.md).
  - Versioille 10.0.20 ja sitä uudemmat versiot: [Finance Insightsin (esiversio) määritys versiolle 10.0.20 ja siitä eteenpäin](configure-for-fin-insites-PubPrvw.md).

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

Älykäs kassavirtaennuste on luotu Dynamics 365 Financen olemassa olevan kassavirtaennusteen avulla. Lisätietoja olemassa olevan ominaisuuden tarkastelemisesta on kohdassa [Kassavirtaennusteet](../cash-bank-management/cash-flow-forecasting.md).

- Lisätietoja siitä, miten asiakkaan maksuennusteista saadaan tietoja perintätehtäviä varten, on kohdassa [Asiakkaan maksuennusteiden käyttäminen](use-customer-payment-predictions.md).
- Lisätietoja ennustemallin tehokkuuden arvioimisesta ominaisuuden käyttöönoton jälkeen on kohdassa [Alkuperäisen asiakkaan maksuennustemallin arvioiminen](evaluate-payment-prediction.md).
- Lisätietoja ennusteen luomisessa käytettyjen tietojen muokkaamisesta ja ennusteen tehokkuuden parantamisesta on kohdassa [Ennustemallin parantaminen](improve-model.md).

Lisätietoja tekoälyennustemallien tuloksista on kohdassa [Koneoppimismallien tulokset](confusion-matrix.md).

### <a name="using-cash-flow-forecasts"></a>Kassavirtaennusteiden käyttäminen

Kassavirtaennusteominaisuus voi auttaa kassatilanteen tarkemmassa arvioimisessa. 

- Lisätietoja kassavirtaennusteiden uusista ominaisuuksista on kohdassa [Kassavirtaennuste](cash-flow-forecast-intro.md).
- Lisätietoja ulkoisten tietojen tuomisesta kassavirtaennusteeseen on kohdassa [Ulkoisten tietojen käyttäminen kassavirtaennusteissa](external-data-in-cash-flow.md). 
- Lisätietoja tekoälymallin käyttämisessä lähitulevaisuuden kassavirran ennustamisessa on kohdassa [Kassatilanne](cash-position.md).
- Lisätietoja kassavirtatilanteiden ja kassavirtaennusteiden tallentamisesta tilannevedoksina ja tilannevedosten vertaamisesta todelliseen tilanteeseen on kohdassa [Tilannevedosten yleiskatsaus](payment-snapshots.md).

### <a name="using-budget-proposal"></a>Budjettiehdotuksen käyttäminen

Lisätietoja budjetin luomisen nopeuttamisesta on kohdassa [Budjettiehdotukset](budget-proposals.md). 

## <a name="feedback-and-support"></a>Palaute ja tuki

Lähetä sähköpostiviesti [Asiakasmaksujen tiedot (esiversio) -kohteeseen](mailto:fiap@microsoft.com), jos haluat antaa palautetta tai tarvitset tukea.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
