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
ms.openlocfilehash: 47551f52f35fec5ae49d696e3f4027b7d2eb2e19
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023216"
---
# <a name="set-up-payment-schedules-with-tds-allocation"></a>Määritä maksusuunnitelmia, joissa on TDS-kohdistus

[!include [banner](../includes/banner.md)]

Tässä aiheessa kuvataan, miten maksusuunnitelmat määritetään Vero vähennettynä lähteissä (TDS) -kohdistuksella.

1. Siirry kohtaan **Ostoreskontra \> Maksun asetukset \> Maksusuunnitelmat**.

    [![Maksusuunnitelmat-sivu](./media/apac-ind-TDS-27.png)](./media/apac-ind-TDS-27.png)

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
