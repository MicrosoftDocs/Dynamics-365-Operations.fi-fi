---
title: Piilota verojen keskeytystiedot tilausyhteenvedoissa
description: Tässä artikkelissa kuvataan, miten veroerittelyn tiedot piilotetaan tilausyhteenvedoissa ostoskorissa, kassavaiheessa, tilausvahvistuksessa ja tilausten erittelysivuilla Microsoft Dynamics 365 Commercessa.
author: gvrmohanreddy
ms.date: 05/17/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-03-28
ms.openlocfilehash: fe1f6c5875444f4f91ee1dfb01b3fdaa527c52e5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8881787"
---
# <a name="hide-tax-breakup-information-in-order-summaries"></a>Piilota verojen keskeytystiedot tilausyhteenvedoissa

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Tässä artikkelissa kuvataan, miten veroerittelyn tiedot piilotetaan tilausyhteenvedoissa ostoskorissa, kassavaiheessa, tilausvahvistuksessa ja tilausten erittelysivuilla Microsoft Dynamics 365 Commercessa.

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

> [!NOTE]
> Jos olet mukauttanut tilausyhteenvetomoduuleita etkä halua periä "piilota veroerittelyn tiedot tilausyhteenvedoissa" -toimintoa Commerce-versiossa 10.0.27 tai sitä myöhemmässä versiossa, katso lisätietoja kohdasta [Tilausyhteenvedon välisumma ei sisällä veroja kuluista, kun käytetään mukautettuja tilausyhteenvetomoduuleita](troubleshoot/summary-taxes-custom-modules-10.0.27.md#resolution).

## <a name="additional-resources"></a>Lisäresurssit

[Arvonlisäveron yleiskatsaus](/finance/general-ledger/indirect-taxes-overview)

[Arvonlisäveron laskeminen online-tilauksille](sales-tax-config.md)

[Vianetsintä: Online-tilausten verot on laskettu väärin](troubleshoot/tax-miscalculated-online-order.md)
