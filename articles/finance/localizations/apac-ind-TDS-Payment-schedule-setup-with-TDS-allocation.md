---
title: Määritä maksusuunnitelmia, joissa on TDS-kohdistus
description: Tässä aiheessa kuvataan, miten maksusuunnitelmat määritetään Vero vähennettynä lähteissä (TDS) -kohdistuksella.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 55bfdfb97c418ec9fd856a151da46c1bcf94aa2cb4df85185b47f722d8526ef2
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6769719"
---
# <a name="set-up-payment-schedules-with-tds-allocation"></a>Määritä maksusuunnitelmia, joissa on TDS-kohdistus

[!include [banner](../includes/banner.md)]

Tässä aiheessa kuvataan, miten maksusuunnitelmat määritetään Vero vähennettynä lähteissä (TDS) -kohdistuksella.

1. Siirry kohtaan **Ostoreskontra \> Maksun asetukset \> Maksusuunnitelmat**.

    [![Maksusuunnitelmat-sivu.](./media/apac-ind-TDS-27.png)](./media/apac-ind-TDS-27.png)

2. Valitse toimintoruudusta **Uusi**, jos haluat luoda maksusuunnitelman, ja syötä tarvittavat tiedot.
3. Valitse **Kohdistus**-kentässä maksutapa, jota käytetään maksusuunnitelman maksun kohdistuksena:

    - Yhteensä
    - Kiinteä summa
    - Kiinteä määrä
    - Määritetty

    **Ennakonpidätyksen kohdistus** -kenttä näyttää maksusuunnitelman TDS-kohdistusmenetelmän. Jos valitset **Yhteensä** **Kohdistus**-kentässä, **Ennakonpidätyksen kohdistus** -kentän arvoksi tulee automaattisesti **Yhteensä**. Jos valitset **Kohdistus**-kentässä **Kiinteä summa**, **Kiinteä määrä** tai **Määritetty**, **Ennakonpidätyksen kohdistus** -kentän arvoksi määritetään automaattisesti **Suhteellinen**.

    > [!NOTE]
    > Jos **Ennakonpidätyksen kohdistus** -kentän arvoksi määritetään **Kokonaissumma**, maksun maksuerät lasketaan bruttosumman perusteella, joka sisältää TDS-summan. Jos **Ennakonpidätyksen kohdistus** -kentän arvoksi määritetään **Suhteellinen**, maksun maksuerät lasketaan nettolaskusumman perusteella TDS-summan vähentämisen jälkeen.

4. Lisää muut pakolliset yksityiskohdat ja sulje sitten sivu.
