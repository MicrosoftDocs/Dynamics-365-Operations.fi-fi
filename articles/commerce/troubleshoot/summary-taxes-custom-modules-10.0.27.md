---
title: Tilausyhteenvedon välisumma ei sisällä kulujen veroja, kun käytetään mukautettuja tilausyhteenvetomoduuleita
description: Tämä artikkeli antaa vianmäärityksen ohjeita, jotka auttavat mukautettujen tilausyhteenvetomoduulien käytössä sekä tilanteissa, joissa tilausyhteenvedon välisumma ei sisällä veroja kuluista "hinta sisältää arvonlisäveron" -skenaariossa.
author: gvrmohanreddy
ms.date: 05/17/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-04-22
ms.openlocfilehash: 260dcb6bc1585615195e32adfcd1da6bfbca294e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8848834"
---
# <a name="order-summary-subtotal-doesnt-include-taxes-on-charges-when-using-customized-order-summary-modules"></a>Tilausyhteenvedon välisumma ei sisällä kulujen veroja, kun käytetään mukautettuja tilausyhteenvetomoduuleita

Tämä artikkeli antaa vianmäärityksen ohjeita, jotka auttavat mukautettujen tilausyhteenvetomoduulien käytössä sekä tilanteissa, joissa tilausyhteenvedon välisumma ei sisällä veroja kuluista "hinta sisältää arvonlisäveron" -skenaariossa.

## <a name="description"></a>Kuvaus

Alkaen Microsoft Dynamics 365 Commerce -versiosta 10.0.27, seuraavat muutokset on tehty "Hinta sisältää arvonlisäveron" -skenaarioon, jotta kokemus olisi yhdenmukainen verkkokaupan sivujen tilausyhteenvetomoduuleissa.

- On lisätty kaksi uutta kenttää: **TaxOnShippingCharge** ja **TaxOnNonShippingCharges**.
- **GetSalesOrderBySalesId**- ja **GetSalesOrderByTransactionId**-ohjelmointirajapinnoilla on tarkat arvot seuraavia kenttiä varten "Hinta sisältää arvonlisäveron" -skenaariossa:

    - SubtotalSalesAmount
    - SubtotalAmountWithoutTax
    - SubtotalAmount
    - ShippingChargeAmount
    - OtherChargeAmount

Jos kuitenkin käytät mukautettuja tilausyhteenvetomoduuleja, nämä muutokset voivat vaikuttaa tilausten yhteenvedon välisummien arvoihin niin, että kuluihin ei sisällytetä veroja.

## <a name="resolution"></a>Ratkaisu

Jos käytät mukautettuja tilausyhteenvetomoduuleita etkä halua periä muutoksia, jotka on tehty "Hinta sisältää arvonlisäveron" -skenaarioon Commerce-versiossa 10.0.27 ja sitä myöhemmissä versioissa, noudata tämän osan ohjeita.

Palauttamalla aiemman (ennen versiota 10.0.27) tilausyhteenvetotoiminnon kentät **salesTransaction.SubtotalAmount** ja **salesTransaction.SubtotalAmountWithoutTax** voit palauttaa kokonaisveromäärän sisällyttämisen (**TaxOnShippingCharge** ja **TaxOnNonShippingCharges**) välisummiin (**SubtotalAmount** ja **SubtotalAmountWithoutTax**).

Voit palauttaa aiemman tilausyhteenvetotoiminnon noudattamalla seuraavia vaiheita.

1. Avaa Commerce headquarters -sovelluksessa Commerce-parametrit-sivu (**Retail ja Commerce \> Pääkonttorin asetukset \> Parametrit \> Commerce-parametrit**).
1. Valitse vasemmassa siirtymisruudussa **Määritysparametrit**.
1. Lisää seuraavat määritysparametrit ja määritä kaikkien arvoksi **tosi**:

    - IsLegacyTaxOnChargeInSubtotalAmountIncludedInTaxIncusiveEnabled
    - IsLegacyOrderSummaryHydrationEnabled

> [!NOTE]
> Jos olet käyttänyt aikaisemmin **IsUpdatedPriceIncludesTaxSubtotalCalculationEnabled**-määritysparametria ja haluat pitää **order.NetAmountWithoutTax**-ominaisuuden saman toiminnan, sinun tulisi lisätä myös **IsLegacyPriceIncludesTaxNetAmountWithoutTaxCalculationEnabled**-määritysparametri ja asettaa sen arvoksi **tosi**.

## <a name="additional-resources"></a>Lisäresurssit

[Piilota verojen keskeytystiedot tilausyhteenvedoissa](../hide-taxes-breakup.md)
