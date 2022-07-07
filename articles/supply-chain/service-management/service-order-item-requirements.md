---
title: Huoltotilauksen nimiketarpeet
description: Tässä artikkelissa käsitellään huoltotilauksen nimiketarpeita.
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjSalesItemReq
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 376cda6bbe1800611e6f24c347b9035469a30a14
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/15/2022
ms.locfileid: "9015169"
---
# <a name="service-order-item-requirements"></a>Huoltotilauksen nimiketarpeet

[!include [banner](../includes/banner.md)]

Voit luoda huoltotilauksen seurataksesi ja hallitaksesi palveluita, joita tarjoat asiakkaillesi. Jos sinun pitää varata tiettyjä nimiketarpeita huoltotilaukselle, voit luoda sille varastonimikevaatimuksia. Nimiketarve voidaan kuluttaa suoraan varastosta tai se voi käynnistää nimikkeen tuotantotilauksen.

Kun käytät nimiketarvetta nimiketapahtuman sijaan, voit suunnitella toimituksen niin, että se tapahtuu juuri ennen nimikkeen käyttöä, luoda ostotilauksen, sisällyttää nimikkeen kauppasopimukseen ja sisällyttää nimiketarpeen tuotannonsuunnitteluun.

Palvelutilausten nimikevaatimukset käsitellään projektin kautta. Jos huoltotilaukselle luodaan nimiketarve, huoltotilauksen pitää olla liitetty projektiin.

Nimiketarvetta voi katsella heti, kun se on luotu huoltotilaukseen, yksittäisen huoltotilauksen **Projekti**-kohdassa tai **Myyntitilaus**-lomakkeen avulla.

## <a name="view-an-item-requirement-from-a-service-order"></a>Nimiketarpeen tarkasteleminen huoltotilauksesta

1. Siirry kohtaan **Palveluiden hallinta** \> **Huoltotilaukset** \> **Huoltotilaukset**.
1. Valitse **Lähetys** ja avaa sitten **Nimiketarpeet**-lomake valitsemalla **Nimiketarve**.
1. Valitse **Projekti**-välilehti ja tarkista **Huoltotilaus**-kentässä nimiketarpeen palvelutilaukset.

## <a name="delete-service-orders-with-item-requirements"></a>Nimiketarpeita sisältävien huoltotilausten poistaminen

Jos huoltotilaukselle luodaan nimiketarve, et voi poistaa huoltotilausta. Sinun on poistettava nimiketarve ennen kuin voit poistaa huoltotilauksen.

1. Siirry kohtaan **Palveluiden hallinta** \> **Huoltotilaukset** \> **Huoltotilaukset**.
1. Valitse **Lähetys** ja avaa sitten **Nimiketarpeet**-lomake valitsemalla **Nimiketarve**. Tässä lomakkeessa näkyvät kaikki huoltotilaukseen luodut nimiketarpeet.
1. Valitse poistettava nimiketarve ja valitse sitten **Poista**.

–TAI–

1. Valitse **Projektinhallinta ja kirjanpito** \> **Projektit** \> **Kaikki projektit**.
1. Avaa projekti, joka sisältää palvelutilauksen, jossa nimiketarve on luotu.
1. Valitse **Projektit**-lomakkeen oikeassa ruudussa **Nimiketarpeet**. **Nimiketarpeet**-lomake avautuu, ja siinä näkyvät valittuun projektiin liittyvät nimiketarpeet.
1. Valitse poistettava nimiketarve ja valitse sitten **Poista**.

## <a name="see-also"></a>Lisätietoja

[Nimiketarpeet (lomake)](https://technet.microsoft.com/library/aa552021\(v=ax.60\))



[!INCLUDE[footer-include](../../includes/footer-banner.md)]