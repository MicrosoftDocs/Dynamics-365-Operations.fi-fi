---
title: Loman rahaksi tai lomapalkan vapaaksi vaihtaminen
description: Tässä artikkelissa kuvataan vapaiden ostamista ja myymistä koskevien pyyntöjen lähettämistä Dynamics 365 Human Resourcesissa.
author: twheeloc
ms.date: 08/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ESSLeaveBuyRequestEntry, EssWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-06-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a6d38a69a73ce14f099beb6b6b560bf6c5686b0c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875710"
---
# <a name="buy-and-sell-leave"></a>Loman rahaksi tai lomapalkan vapaaksi vaihtaminen


>[!Important]
>Tässä artikkelissa mainittu toiminto on tällä hetkellä Dynamics 365 Human Resourcesin erillistä versiota käyttävien asiakkaiden käytettävissä. Osa toiminnoista tai kaikki toiminnot ovat saatavana osana Finance-infrastruktuurin tulevaa versiota, Finance-julkaisun 10.0.26 jälkeen.

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Voit lähettää Dynamics 365 Human Resourcesissa loman rahaksi tai lomapalkan vapaaksi vaihtamispyyntöjä yrityksen määrittämien loman rahaksi tai lomapalkan vapaaksi vaihtamiskäytäntöjen perusteella.  

## <a name="request-to-buy-leave"></a>Pyyntö ostaa loma

1. Valitse **työntekijän itsepalvelu** -työtilassa **Loman ostopyyntö** **Vapaasaldot**-ruudusta. 

2. Lisää **Lomatyyppi** ja kirjoita **Määrä**, jonka verran lomaa haluat ostaa. 

3. Valitse **Lähetä**, kun olet valmis lähettämään pyyntösi. 

Saldo päivitetään joko automaattisesti tai se siirtyy hyväksyntäprosessiin ennen päivittämistä. Toimintatapa määräytyy loman rahaksi vaihtamiskäytännön määrityksen mukaan.

## <a name="request-to-sell-leave"></a>Lomapalkan vapaaksi vaihtamispyyntö

1. Valitse **Työntekijän itsepalvelu** -työtilassa **Lomapalkan vapaaksi vaihtamispyyntö** **Vapaasaldot**-ruudussa. 

2. Lisää **Lomatyyppi** ja kirjoita vapaaksi vaihdettavan lomapalkan **Määrä**. 

3. Valitse **Lähetä**, kun olet valmis lähettämään pyyntösi.

Saldo päivitetään joko automaattisesti tai se siirtyy hyväksyntäprosessiin ennen päivittämistä. Toimintatapa määräytyy loman rahaksi vaihtamiskäytännön määrityksen mukaan.


## <a name="troubleshooting"></a>Vianmääritys 

Jos osto- tai myyntipyyntötyönkulku epäonnistuu, käyttäjät, joilla on **EssLeaveBuySellRequestApprover**-oikeudet, voivat tarkistaa kaikkien osto- ja myyntipyyntöjen sanomalokin. Voit tehdä tämän menemällä kohtaan **Loma ja poissaolo > Linkit > Osto- ja myyntipyynnöt > Sanomaloki** (vasemmalla yläkulmassa). **Sanomaloki** näyttää käyttäjille, kuinka tapahtumat on käsitelty, sekä niihin liittyvät työnkulkuhistoriat.


## <a name="see-also"></a>Lisätietoja

[Lomien ja poissaolojen yhteenveto](hr-leave-and-absence-overview.md)</br>
[Käytäntöjen hallinta loman vaihtamisessa rahaksi ja lomapalkan vaihtamisessa vapaaksi](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
