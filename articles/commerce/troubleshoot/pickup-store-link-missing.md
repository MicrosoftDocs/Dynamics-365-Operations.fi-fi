---
title: Nouda tämä -vaihtoehtoa ei ole näkyvissä ostoskori- tai tuotetietosivuilla
description: Tämä artikkeli antaa vianmääritysohjeet, jotka voivat auttaa siinä, että myymälästä noudon vaihtoehto ei näy ostoskorisivulla tai tuotteen tietosivuilla.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 88367e13b4d079edb0816e301901828b65c437ae
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8900305"
---
# <a name="pick-this-up-option-doesnt-appear-on-cart-or-product-details-pages"></a>Nouda tämä -vaihtoehtoa ei ole näkyvissä ostoskori- tai tuotetietosivuilla

[!include [banner](../../includes/banner.md)]

Tämä artikkeli antaa vianmääritysohjeet, jotka voivat auttaa siinä, että myymälästä noudon vaihtoehto ei näy ostoskorisivulla tai tuotteen tietosivuilla.

## <a name="description"></a>kuvaus

**Nouda tämä** -vaihtoehtoa ei ole näkyvissä ostoskorisivulla tai tuotetietosivuilla.

Seuraavassa kuvassa on esimerkki sivusta, joka sisältää **Nouda tämä** -painikkeen.

![Nouda tämä -painike.](media/pickup-button-missing.jpg)

## <a name="resolution"></a>Ratkaisu

### <a name="enable-the-bopis-extension-in-commerce-site-builder"></a>Ota BOPIS-laajennus käyttöön Commerce sivustonmuodostimessa

Ota "Osta verkosta, nouda myymälästä" (BOPIS) -laajennus käyttöön Commerce sivustonmuodostimessa noudattamalla seuraavia ohjeita.

1. Valitse sivusto.
1. Valitse **Sivuston asetukset** ja valitse sitten **Laajennukset**.
1. Varmista, että **Poista BOPIS** -valinta on tyhjä.

### <a name="configure-modes-of-delivery-in-commerce-headquarters"></a>Toimitustapojen konfiguroiminen Commerce headquarters -sovelluksessa

Voit määrittää toimitustavat Commerce headquarters -sovelluksessa seuraavasti.

1. Siirry kohtaan **Hankinta \> Asetukset \> Toimitustavat**.
1. Varmista, että **Asiakkaan nouto** -toimitustapa on luotu ja että siihen on liitetty tuotteet ja osoitteet.
1. Valitse **Vähittäismyynti ja kauppa \> Pääkonttorin asetukset \> Parametrit**.
1. Valitse vasemmassa siirtymisruudussa **Asiakastilaukset**.
1. Varmista, että **Noutotoimitustapa** on määritetty oikein.

### <a name="configure-customer-orders-payments"></a>Asiakastilausmaksujen konfiguroiminen

Voit konfiguroida asiakastilausten maksut Commerce headquarters -sovelluksessa seuraavasti.

1. Valitse **Vähittäismyynti ja kauppa \> Pääkonttorin asetukset \> Parametrit**.
1. Valitse vasemmassa siirtymisruudussa **Asiakastilaukset**.
1. Varmista **Maksut**-pikavälilehdellä, että **Maksuehdot**- ja **Maksutapa**-kentät on määritetty oikein.

## <a name="additional-resources"></a>Lisäresurssit

[Määritä BOPIS](../cpe-bopis.md)

[Useiden noutotoimitustapojen ottaminen käyttöön asiakastilauksille](../multiple-pickup-modes.md)

[Monikanavaisten Commerce-tilausten maksut](../dev-itpro/commerce-payments.md)

[Myymälän valitsinmoduuli](../store-selector.md)
