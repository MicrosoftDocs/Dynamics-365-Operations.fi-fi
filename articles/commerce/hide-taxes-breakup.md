---
title: Piilota verojen erittelytiedot tilausyhteenvedoissa
description: Tässä aiheessa kuvataan, miten veroerittelyn tiedot piilotetaan tilausyhteenvedoissa ostoskorissa, kassavaiheessa, tilausvahvistuksessa ja tilausten erittelysivuilla Microsoft Dynamics 365 Commercessa.
author: gvrmohanreddy
ms.date: 04/21/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-03-28
ms.openlocfilehash: 9890b5cd92f8c07e6feabb26f4fdd076cb7a02bc
ms.sourcegitcommit: d715e44b92b84b1703f5915d15d403ccf17c6606
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/27/2022
ms.locfileid: "8645216"
---
# <a name="hide-tax-breakup-information-in-order-summaries"></a>Piilota verojen erittelytiedot tilausyhteenvedoissa

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Tässä aiheessa kuvataan, miten veroerittelyn tiedot piilotetaan tilausyhteenvedoissa ostoskorissa, kassavaiheessa, tilausvahvistuksessa ja tilausten erittelysivuilla Microsoft Dynamics 365 Commercessa.

Oletusarvoisesti Dynamics 365 Commerce näyttää veroerittelyn tiedot tilausyhteenvedoissa ostoskorissa, kassavaiheessa, tilausvahvistuksessa ja tilausten erittelysivuilla. Commercen sivustonmuodostin sisältää Commerce versiosta 10.0.27 eteenpäin vaihtoehdon, jonka avulla voit piilottaa verojen erittelytiedot tilausyhteenvedoissa.

Seuraavassa kuvassa on esimerkki kahdesta tilausyhteenvedosta. Ensimmäisessä näkyvät verojen erittelytiedot, ja toinen piilottaa tiedot.

![Esimerkkejä ostoskärryistä, joissa näytetään ja piilotetaan veron erittelytietoja.](media/prices-include-sales-tax-e-Commerce.png)

> [!NOTE]
> - Verojen erittelytietojen piilottamisen vaihtoehto tilausyhteenvedoissa on käytettävissä vain, kun sähköisen kauppakanavan **Hinnat sisältävät arvonlisäveron** -asetuksen arvoksi on määritetty **Kyllä** Commerce headquartersissa kohdassa **Retail ja Commerce \> Kanavat \> Myymälät \> Kaikki myymälät**. 
> - Oletusarvon mukaan **Näytä verojen erittely tilausyhteenvedossa** -valinta on käytössä sivuston luontityökalussa.

## <a name="hide-tax-breakup-information-in-order-summaries"></a>Piilota verojen erittelytiedot tilausyhteenvedoissa

Voit piilottaa verojen erittelytiedot tilausyhteenvedoissa seuraavasti.

1. Siirry Commercen sivustonmuodostimessa sivustoon, jonka haluat päivittää.
1. Siirry kohtaan **Sivuston asetukset \> Laajennukset**.
1. Poista **Näytä verojen erittely tilausyhteenvedossa** -valintaruudun valinta.

Jos haluat näyttää tilausyhteenvedoissa verojen erittelytiedot, valitse **Näytä verojen erittely tilausyhteenvedossa** -valintaruutu.  

Seuraavassa kuvassa näkyy **Näytä verojen erittely tilausyhteenvedossa** -valintaruutu, joka on korostettu ja valittu sivuston luontityökalussa.

![Näytä verojen erittely tilausyhteenvedossa -vaihtoehto sivustonmuodostimessa.](media/prices-include-sales-tax-e-Commerce-site-settings.png)

## <a name="additional-resources"></a>Lisäresurssit

[Arvonlisäveron yleiskatsaus](/finance/general-ledger/indirect-taxes-overview)

[Arvonlisäveron laskeminen online-tilauksille](sales-tax-config.md)

[Vianetsintä: Online-tilausten verot on laskettu väärin](troubleshoot/tax-miscalculated-online-order.md)
