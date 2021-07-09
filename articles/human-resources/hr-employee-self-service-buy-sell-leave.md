---
title: Osta ja myy lomaa
description: Voit lähettää Dynamics 365 Human Resourcesissa loman rahaksi tai lomapalkan vapaaksi vaihtamispyyntöjä yrityksen määrittämien loman rahaksi tai lomapalkan vapaaksi vaihtamiskäytäntöjen perusteella.
author: andreabichsel
ms.date: 08/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ESSLeaveBuyRequestEntry, EssWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-06-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6d32abacc1539cb930ad6f1ebcfe6fa9af4befcf
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271479"
---
# <a name="buy-and-sell-leave"></a>Osta ja myy lomaa

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

Jos osto- tai myyntipyyntötyönkulku epäonnistuu, käyttäjät, joilla on **EssLeaveBuySellRequestApprover**-oikeudet, voivat tarkistaa kaikkien osto- ja myyntipyyntöjen sanomalokin. Voit tehdä tämän menemällä kohtaan **Loma ja poissaolo > Linkki > Osto- ja myyntipyynnöt > sanomaloki** (vasemmalla yläkulmassa). **Sanomaloki** näyttää käyttäjille, kuinka tapahtumat on käsitelty, sekä niihin liittyvät työnkulkuhistoriat.


## <a name="see-also"></a>Lisätietoja

[Lomien ja poissaolojen yhteenveto](hr-leave-and-absence-overview.md)</br>
[Käytäntöjen hallinta loman vaihtamisessa rahaksi ja lomapalkan vaihtamisessa vapaaksi](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
