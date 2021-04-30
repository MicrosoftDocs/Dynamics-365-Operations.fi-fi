---
title: Asiakkaan maksuennusteiden käyttäminen (esiversio)
description: Tässä ohjeaiheessa kerrotaan edellytyksistä ja vaiheista, jotka Finance Insightsin kokeiluversion käyttäminen edellyttää.
author: ShivamPandey-msft
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-11-16
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: 21c5236b6d7e7ce7bd968f1511723a3646fe7a29
ms.sourcegitcommit: 7d0cfb359a4abc7392ddb3f0b3e9539c40b7204d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/14/2021
ms.locfileid: "5897789"
---
# <a name="use-customer-payment-predictions-preview"></a>Asiakkaan maksuennusteiden käyttäminen (esiversio)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Tässä ohjeaiheessa kerrotaan, miten asiakkaan maksuennusteita käytetään. Ennen kuin käytät tätä toimintoa, varmista, että olet tehnyt sen määritysvaiheet. Lisätietoja on ohjeaiheessa [Asiakkaan maksuennusteiden käyttöönotto](enable-cust-paymnt-prediction.md).

Voit tarkastella asiakkaan maksuennusteita **Asiakkaan luotonvalvonnan hallinta** -työtilassa ja kahdella uudella luettelosivulla, joiden nimet ovat **Maksuennusteet tapahtuman mukaan** ja **Maksuennusteet asiakkaan mukaan**.

### <a name="manage-customer-credit-and-collections-workspace"></a>Asiakkaan luotonvalvonnan hallinta -työtila

**Asiakkaan luotonvalvonnan hallinta** -työtila sisältää kaksi uutta ruutua, joiden nimet ovat **Maksuennuste tapahtuman mukaan** ja **Asiakkaat ja ennustetut myöhässä olevat saldot**.

- **Maksuennuste tapahtuman mukaan** -ruudussa on niiden avointen asiakastapahtumien määrä, joiden maksun todennäköisyys on alle 50 prosenttia **Ajoissa**-säilössä. Voit valita tämän ruudun, jos haluat avata **Maksuennusteet tapahtuman mukaan** -luettelosivun.
- **Asiakkaat ja ennustetut myöhässä olevat saldot** -ruudussa on niiden asiakkaiden määrä, joiden kokonaissaldosta yli puolet (50 prosenttia) ennustetaan maksettavan myöhässä ja/tai erittäin paljon myöhässä. Valitse tämä ruutu, jos haluat avata **Maksuennuste asiakkaan mukaan** -luettelosivun.

[![Asiakkaan luotonvalvonnan hallinta -työtila](./media/manage-customer-credit-collections.png)](./media/manage-customer-credit-collections.png)

### <a name="payment-predictions-per-transaction-list-page"></a>Maksuennusteet tapahtuman mukaan -luettelosivu

**Maksuennusteet tapahtuman mukaan** -luettelosivulla ovat näkyvissä avointen tapahtumien todennäköisyys **Ajoissa**-, **Myöhässä**- ja **Erittäin paljon myöhässä** -säilöissä. **Ajoissa-todennäköisyys**-sarakkeessa on kunkin ruudukon tapahtuman todennäköisyys sille, että lasku maksetaan ajoissa tai ennen eräpäivää. Jos todennäköisyys ajoissa tehdylle maksulle on alle 50 prosenttia, **Ajoissa-todennäköisyys**-sarakkeen prosenttiosuuden vieressä on punainen ympyrä. Se osoittaa myöhässä tehtävän maksun riskin.

[![Maksuennuste tapahtuman mukaan -sivu](./media/payment-predictions-per-transaction.png)](./media/payment-predictions-per-transaction.png)

Sivun oikealla puolella oleva **Liittyvät tiedot** -paneeli sisältää seuraavat ennusteen lisätiedot:

- Ruudukossa valitun tapahtuman **Maksuennuste**-pikavälilehdessä näkyvät maksuennusteiden tiedot **Ajoissa**-, **Myöhässä**- ja **Erittäin paljon myöhässä** -säilöissä. **Tärkeimmät tekijät** -osassa näkyvät ennusteisiin vaikuttaneet tärkeimmät tekijät. Tärkeimmät tekijät ovat valitun tapahtuman määritteet ja/tai kyseisen tapahtuman asiakas.
- **Customer Insights** -pikavälilehti sisältää nykyisen laskun, maksun ja perinnän tilastotiedot valitun tapahtuman asiakasta varten.
- **Asiakashistoria**-pikavälilehdessä on asiakkaan maksuhistoria **Ajoissa**-, **Myöhässä**- ja **Erittäin paljon myöhässä** -säilöissä.

**Tärkeimmät tekijät** -osan sekä **Customer Insights**- ja **Asiakashistoria**-pikavälilehtien tiedot auttavat maksuennusteiden ymmärtämisessä. Ne tuovat luottamusta ennusteiden tehokkuuteen.

[![Liittyvät tiedot -ruudun maksuennusteiden graafiset ilmaisimet](./media/payment-prediction-gauges.png)](./media/payment-prediction-gauges.png)

### <a name="payment-prediction-per-customer-list-page"></a>Maksuennuste asiakkaan mukaan -luettelosivu

**Maksuennuste asiakkaan mukaan** -luettelosivu sisältää avoimen kokonaissaldo ja summan, joka ennustetaan maksettavaksi **Ajoissa**-, **Myöhässä**- ja **Erittäin paljon myöhässä** -säilöissä.

[![Maksuennusteet asiakkaan mukaan -sivu](./media/payment-predictions-per-transaction-02.png)](./media/payment-predictions-per-transaction-02.png)

Kunkin säilön maksusumma lasketaan tapahtuman saldon painotetun keskiarvon summana. Tämä summa lasketaan kunkin säilön maksun todennäköisyyksien perusteella.

Ajatellaan, että asiakkaalla on esimerkiksi kolme avointa tapahtumaa. Niillä on seuraavat maksun todennäköisyydet kussakin säilössä.

| Tapahtuma | Määrä | Ajoissa olevan maksun todennäköisyys | Myöhässä olevan maksun todennäköisyys | Erittäin paljon myöhässä olevan maksun todennäköisyys |
|-------------|--------|-----------------------------|--------------------------|-------------------------------|
| T1          | 100    | 10 prosenttia                  | 50 prosenttia               | 40 prosenttia                    |
| T2          | 1 000  | 50 prosenttia                  | 30 prosenttia               | 20 prosenttia                    |
| T3          | 10,000 | 1 prosenttia                   | 4 prosenttia                | 95 prosenttia                    |

Tässä tapauksessa maksut ennustetaan jokaiselle säilölle seuraavasti.

| Säilöt   | Tapahtuma T1      | Tapahtuma T2         | Tapahtuma T3            | Yhteensä |
|-----------|---------------------|------------------------|---------------------------|-------|
| Ajallaan   | 100 × 10 ÷ 100 = 10 | 1 000 × 50 ÷ 100 = 500 | 10 000 × 1 ÷ 100 = 100    | 610   |
| Myöhässä      | 100 × 50 ÷ 100 = 50 | 1 000 × 30 ÷ 100 = 300 | 10 000 × 4 ÷ 100 = 400    | 750   |
| Hyvin myöhässä | 100 × 40 ÷ 100 = 40 | 1 000 × 20 ÷ 100 = 200 | 10 000 × 95 ÷ 100 = 9 500 | 9,740 |

Sivun oikealla puolella oleva **Liittyvät tiedot** -osa sisältää seuraavat ennusteen lisätiedot:

- Ruudukossa valitun tapahtuman **Maksuennusteet**-pikavälilehdessä näkyvät maksuennusteiden tiedot **Ajoissa**-, **Myöhässä**- ja **Erittäin paljon myöhässä** -säilöissä. **Tärkeimmät tekijät** -osassa näkyvät maksuihin vaikuttaneet tärkeimmät tekijät. Tärkeimmät tekijät ovat valitun tapahtuman määritteet ja/tai kyseisen tapahtuman asiakas.
- **Customer Insights** -pikavälilehti sisältää nykyisen laskun, maksun ja perinnän tilastotiedot valitun tapahtuman asiakasta varten.
- **Asiakashistoria**-pikavälilehdessä on asiakkaan maksuhistoria **Ajoissa**-, **Myöhässä**- ja **Erittäin paljon myöhässä** -säilöissä.

**Tärkeimmät tekijät** -osan sekä **Customer Insights**- ja **Asiakashistoria**-pikavälilehtien tiedot auttavat maksuennusteiden ymmärtämisessä. Ne tuovat luottamusta ennusteiden tehokkuuteen.

## <a name="improving-the-accuracy-of-payment-predictions"></a>Maksuennusteiden tarkkuuden parantaminen

Voit tarkastella maksuennusteiden tarkkuutta siirtymällä kohtaan **Luotonvalvonta \> Asetukset \> Finance Insights \> Finance Insights -parametrit**. **Asiakasmaksun tiedot** -välilehden **Ennustemalli**-osassa on ennustemallin tarkkuus prosenttiosuutena.

[![Maksuennusteiden tarkkuus](./media/finance-insights-parameters-accuracy-2nd.png)](./media/finance-insights-parameters-accuracy-2nd.png)

Jos et ole tyytyväinen tarkkuuteen, avaa AI Builder -laajennuskokemus valitsemalla **Paranna mallint arkkuutta** -linkki. AI Builder -laajennuskokemuksen avulla voit valita kenttiä tai peruuttaa niiden valinnan ja näin valita kentät, jotka ovat tärkeimmät maksun todennäköisyyksien tarkassa ennustamisessa. Kun olet valmis, voit helposti kouluttaa ennustemallin ja julkaista muutokset. Juuri koulutettu ennustemalli valitaan automaattisesti Dynamics 365 Financen ennusteita varten.

[![AI Builder -laajennuskokemus](./media/ai-builder.png)](./media/ai-builder.png)

## <a name="release-details"></a>Julkaisun tiedot

Finance Insightsin julkinen esiversio on saatavilla käyttöönotoissa kokeilua varten Yhdysvalloissa, Euroopassa ja Yhdistyneessä kuningaskunnassa. Microsoft lisää tukea jatkuvasti myös muilla alueilla.

Julkisen esiversion ominaisuudet voidaan ottaa käyttöön vain Taso 2 -eristysympäristöissä. Eristysympäristössä luotuja määrityksiä ja tekoälymalleja ei voi siirtää tuotantoympäristöön. Lisätietoja on kohdassa [Microsoft Dynamics 365 -esiversioiden lisäkäyttöehdot](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md).

## <a name="privacy-notice"></a>Tietosuojatiedot

Esiversiot (1) voivat käyttää vähemmän tietosuojaa ja suojaustoimenpiteitä kuin Dynamics 365 Finance and Operations -palvelu, (2) eivät sisälly tämän huoltotilauksen palvelutasosopimukseen, (3) niitä ei ole tarkoitettu henkilötietojen tai muiden sellaisten tietojen käsittelemiseen, joihin liittyy lainsäädännön tai määräysten vaatimustenmukaisuusvaatimuksia ja (4) niillä on rajoitettu tuki.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]