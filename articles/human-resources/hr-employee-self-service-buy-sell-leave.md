---
title: Loman rahaksi tai lomapalkan vapaaksi vaihtaminen
description: Tässä aiheessa kuvataan vapaiden ostamista ja myymistä koskevien pyyntöjen lähettämistä Dynamics 365 Human Resourcesissa.
author: twheeloc
ms.date: 08/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ESSLeaveBuyRequestEntry, EssWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-06-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 716afdc4e52c3e4a0432b987cb82077012d4d0c2
ms.sourcegitcommit: a8ac6d9b63eb67d14dd17a086ef4f1eccd7f9fc1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/27/2021
ms.locfileid: "7431507"
---
# <a name="buy-and-sell-leave"></a>Loman rahaksi tai lomapalkan vapaaksi vaihtaminen

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
