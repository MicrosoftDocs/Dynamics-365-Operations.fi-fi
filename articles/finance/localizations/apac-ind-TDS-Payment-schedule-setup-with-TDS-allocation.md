---
title: Määritä maksusuunnitelmia, joissa on TDS-kohdistus
description: Tässä aiheessa kuvataan, miten maksusuunnitelmat määritetään Vero vähennettynä lähteissä (TDS) -kohdistuksella.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 31ecf2e6fa4d3d37c3d5332dc1d5592bf1a99bad
ms.sourcegitcommit: 6dc2b877cf8ea9185a07964ec05c5ddb7a78471b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/12/2022
ms.locfileid: "8408087"
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
