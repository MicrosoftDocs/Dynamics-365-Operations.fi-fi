---
title: QR-koodin tai viivakoodin lisääminen tapahtuma- ja kuittisähköposteihin
description: Tässä aiheessa kerrotaan, miten QR-koodeja ja viivakoodeja, jotka kuvaavat tilaustunnuksia, lisätään Microsoft Dynamics 365 Commercessa tapahtuma- ja kuittisähköposteihin.
author: bicyclingfool
manager: annbe
ms.date: 03/04/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Commerce, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2021-02-16
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 3cc4fcb1237f8409a89b3d4818c132c60c57b5a0
ms.sourcegitcommit: 88babb2fffe97e93bbde543633fc492120f2a4fc
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/06/2021
ms.locfileid: "5555419"
---
# <a name="add-a-qr-code-or-bar-code-to-transactional-and-receipt-emails"></a>QR-koodin tai viivakoodin lisääminen tapahtuma- ja kuittisähköposteihin

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Tässä aiheessa kerrotaan, miten QR-koodeja ja viivakoodeja, jotka kuvaavat tilaustunnuksia, lisätään Microsoft Dynamics 365 Commercessa tapahtuma- ja kuittisähköposteihin.

Tapahtumasähköposteihin voidaan helposti sisällyttää QR-koodeja ja viivakoodeja, jotka nopeuttavat tilausten hakuprosessia vähittäismyyntiympäristössä. Jos haluat lisätä sähköpostiviesteihin QR-koodeja ja viivakoodeja, käytät HTML:n **\<img\>**-tunnisteita, jotka pyytävät luomis- ja muodostamispalvelusta QR-koodin tai viivakoodin kuvan. Microsoft ei toimita tätä palvelua. On kuitenkin monia maksuttomia tai edullisia palveluita, jotka voivat tuottaa QR-koodeja ja viivakoodeja,, jotka luodaan dynaamisesti kyselymerkkijonossa välitetyn arvon perusteella.

## <a name="add-a-qr-code-or-bar-code-to-a-transactional-email"></a>QR-koodin tai viivakoodin lisääminen tapahtumasähköpostiin

Jos haluat lisätä QR-koodeja ja viivakoodeja tapahtumasähköpostiviestiin, joka lähetetään osana sähköistä ostoa, noudata seuraavia ohjeita.

1. Avaa tapahtumasähköpostimallin lähde-HTML-koodi ja lisää **\<img\>**-HTML-tunniste, joka osoittaa QR-koodien tai viivakoodien palveluun. Esimerkki:

    ```HTML
    <img src="https://YOUR_QR_CODE_BAR_CODE_SERVICE?data=%salesid%&param1=value1&param2=value2" alt="%salesid%" />
    ```

    Seuraavassa on selitetty edellinen esimerkki:

    - **YOUR\_QR\_CODE\_BAR\_CODE\_SERVICE** edustaa QR-koodien ja viivakoodien palvelun toimialuetta.
    - **data** edustaa parametria, jonka QR-koodi- tai viivakoodipalvelu vastaanottaa sisällöt, jotka tulee antaa QR-koodina tai viivakoodina.

        Arvo **%salesid%** on määritettävä tähän parametriin. Huomaa tässä esimerkissä, että arvoa käytetään myös kuvan alt-tekstinä.

    - **param1** ja **param2** edustavat valinnaisia lisäparametreja.

1. Siirry kohtaan **Retail ja Commerce \> Pääkonttorin asetukset \> Parametrit \> Organisaation sähköpostimallit** ja lataa päivitetty HTML palvelimeen oikeaan tapahtumasähköpostin malliin.

> [!NOTE]
> Parametrit voivat vaihdella eri QR-koodi- ja viivakoodipalveluiden välillä. Varmista siksi, että otat yhteyttä palveluntarjoajaan ja vahvistat parametrit, jotka on määritettävä.

## <a name="add-a-qr-code-or-bar-code-to-a-receipt-email"></a>QR-koodin tai viivakoodin lisääminen kuittisähköpostiin 

Kun haluat lisätä oston jälkeen myyntipisteestä lähetettävään kuittisähköpostiviestiin QR-koodin tai viivakoodin, noudata seuraavia ohjeita.

1. Avaa kuittisähköpostimallin lähde-HTML-koodi ja lisää **\<img\>**-HTML-tunniste, joka osoittaa QR-koodien tai viivakoodien palveluun. Alla on esimerkki.

    ```HTML
    <img src="https://YOUR_QR_CODE_BAR_CODE_SERVICE?data=%receiptid%&param1=value1&param2=value2" alt="%receiptid%" />
    ```

    Seuraavassa on selitetty edellinen esimerkki:

    - **YOUR\_QR\_CODE\_BAR\_CODE\_SERVICE** edustaa QR-koodien ja viivakoodien palvelun toimialuetta.
    - **data** edustaa parametria, jonka QR-koodi- tai viivakoodipalvelu vastaanottaa sisällöt, jotka tulee antaa QR-koodina tai viivakoodina.

        Arvo **%receiptid%** on määritettävä tähän parametriin. Huomaa tässä esimerkissä, että arvoa käytetään myös kuvan alt-tekstinä.

    - **param1** ja **param2** edustavat valinnaisia lisäparametreja.

1. Siirry kohtaan **Retail ja Commerce \> Pääkonttorin asetukset \> Parametrit \> Organisaation sähköpostimallit** ja lataa päivitetty HTML palvelimeen sähköpostimalliin, jolla on sähköpostitunnus **emailrecpt**.

> [!NOTE]
> Parametrit voivat vaihdella eri QR-koodi- ja viivakoodipalveluiden välillä. Varmista siksi, että otat yhteyttä palveluntarjoajaan ja vahvistat parametrit, jotka on määritettävä.

## <a name="additional-resources"></a>Lisäresurssit

[Sähköpostikuittien lähettäminen Modern POS:stä (MPOS)](email-receipts.md)

[Tapahtuman tapahtumien sähköpostimallien luominen](email-templates-transactions.md)