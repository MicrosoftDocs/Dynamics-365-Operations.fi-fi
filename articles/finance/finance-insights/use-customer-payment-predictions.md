---
title: Asiakkaan maksuennusteiden käyttäminen
description: Tässä ohjeaiheessa kerrotaan edellytyksistä ja vaiheista, jotka Finance Insightsin kokeiluversion käyttäminen edellyttää.
author: ShivamPandey-msft
ms.date: 11/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-11-16
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: ecc864485dfc106df22b48e92a85f2c73d58e0e8
ms.sourcegitcommit: d70f66a98eff0a2836e3033351b482466bd9c290
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2022
ms.locfileid: "8740621"
---
# <a name="use-customer-payment-predictions"></a>Asiakkaan maksuennusteiden käyttäminen

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, miten asiakkaan maksuennusteita käytetään. Ennen kuin käytät tätä toimintoa, varmista, että olet tehnyt sen määritysvaiheet. Lisätietoja on ohjeaiheessa [Asiakkaan maksuennusteiden käyttöönotto](enable-cust-paymnt-prediction.md).

Voit tarkastella asiakkaan maksuennusteita **Hallitse asiakkaan luotonvalvontaa** -työtilassa ja kahdella uudella luettelosivulla: **Tapahtuman maksuennusteet** ja **Asiakkaan maksuennusteet**.

### <a name="manage-customer-credit-and-collections-workspace"></a>Asiakkaan luotonvalvonnan hallinta -työtila

**Hallitse asiakkaan luotonvalvontaa** -työtila sisältää kaksi uutta ruutua: **Tapahtuman maksuennusteet** ja **Asiakkaan maksuennusteet**.

### <a name="transaction-payment-predictions-list-page"></a>Tapahtuman maksuennusteet -luettelosivu

**Tapahtuman maksuennusteet** -luettelosivulla näkyy maksamisen todennäköisyys avoimien tapahtumien **Ajoissa**-, **Myöhässä**- ja **Erittäin paljon myöhässä** -säilöissä. **Ajoissa-todennäköisyys**-sarakkeessa on kunkin ruudukon tapahtuman todennäköisyys sille, että lasku maksetaan ajoissa tai ennen eräpäivää. Jos todennäköisyys ajoissa tehdylle maksulle on alle 50 prosenttia, **Ajoissa-todennäköisyys**-sarakkeen prosenttiosuuden vieressä on punainen ympyrä. Se osoittaa myöhässä tehtävän maksun riskin.

[![Maksuennuste tapahtuman mukaan -sivu.](./media/payment-predictions-per-transaction.png)](./media/payment-predictions-per-transaction.png)

Sivun oikealla puolella oleva **Liittyvät tiedot** -paneeli sisältää seuraavat ennusteen lisätiedot:

- Ruudukossa valitun tapahtuman **Maksuennuste**-pikavälilehdessä näkyvät maksuennusteiden tiedot **Ajoissa**-, **Myöhässä**- ja **Erittäin paljon myöhässä** -säilöissä. **Tärkeimmät tekijät** -osassa näkyvät ennusteisiin vaikuttaneet tärkeimmät tekijät. Tärkeimmät tekijät ovat valitun tapahtuman määritteet ja/tai kyseisen tapahtuman asiakas.
- **Customer Insights** -pikavälilehti sisältää nykyisen laskun, maksun ja perinnän tilastotiedot valitun tapahtuman asiakasta varten.
- **Asiakashistoria**-pikavälilehdessä on asiakkaan maksuhistoria **Ajoissa**-, **Myöhässä**- ja **Erittäin paljon myöhässä** -säilöissä.

**Tärkeimmät tekijät** -osan sekä **Customer Insights**- ja **Asiakashistoria**-pikavälilehtien tiedot auttavat maksuennusteiden ymmärtämisessä. Ne tuovat luottamusta ennusteiden tehokkuuteen.

[![Liittyvät tiedot -ruudun maksuennusteiden graafiset ilmaisimet.](./media/payment-prediction-gauges.png)](./media/payment-prediction-gauges.png)

### <a name="customer-payment-predictions-list-page"></a>Asiakkaan maksuennusteet -luettelosivu

**Asiakkaan maksuennusteet** -luettelosivu sisältää avoimen kokonaissaldo ja summan, joka ennustetaan maksettavan **Ajoissa**-, **Myöhässä**- ja **Erittäin paljon myöhässä** -säilöissä.

[![Maksuennusteet asiakkaan mukaan -sivu.](./media/payment-predictions-per-transaction-02.png)](./media/payment-predictions-per-transaction-02.png)

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

- Ruudukossa valitun tapahtuman **Maksuennusteet**-pikavälilehdessä näkyvät maksuennusteiden tiedot **Ajoissa**-, **Myöhässä**- ja **Erittäin paljon myöhässä** -säilöissä.
- **Customer Insights** -pikavälilehti sisältää nykyisen laskun, maksun ja perinnän tilastotiedot valitun tapahtuman asiakasta varten.
- **Asiakashistoria**-pikavälilehdessä on asiakkaan maksuhistoria **Ajoissa**-, **Myöhässä**- ja **Erittäin paljon myöhässä** -säilöissä.

**Asiakkaan merkitykselliset tiedot**- ja **Asiakashistoria**-pikavälilehtien tiedot auttavat hahmottamaan maksuennusteita. Ne tuovat luottamusta ennusteiden tehokkuuteen.

## <a name="improving-the-accuracy-of-payment-predictions"></a>Maksuennusteiden tarkkuuden parantaminen

Voit tarkastella maksuennusteiden tarkkuutta siirtymällä kohtaan **Luotonvalvonta \> Asetukset \> Finance Insights \> Finance Insights -parametrit**. **Asiakasmaksun tiedot** -välilehden **Ennustemalli**-osassa on ennustemallin tarkkuus prosenttiosuutena.

Jos et ole tyytyväinen tarkkuuteen, avaa AI Builder -laajennuskokemus valitsemalla **Paranna mallin tarkkuutta** -linkki. AI Builder -laajennuskokemuksen avulla voit valita kenttiä tai peruuttaa niiden valinnan ja näin valita kentät, jotka ovat tärkeimmät maksun todennäköisyyksien tarkassa ennustamisessa. Kun olet valmis, voit helposti kouluttaa ennustemallin ja julkaista muutokset. Juuri koulutettu ennustemalli valitaan automaattisesti Dynamics 365 Financen ennusteita varten.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
