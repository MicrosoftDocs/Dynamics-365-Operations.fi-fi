---
title: Määritä TDS-parametrit
description: Tässä aiheessa kuvataan, kuinka määritetään parametrit, jotka aktivoivat Vero vähennettynä lähteissä (TDS) -toiminnon määritetyissä tapahtumissa. Tämä on tarpeellinen vaihe, kun haluat käyttää Vero vähennettynä lähteissä (TDS) -toimintoa.
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
ms.openlocfilehash: b74a1ab6d0f17367fc16f795e1b28ff5d0c5508e
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/06/2021
ms.locfileid: "6358239"
---
# <a name="set-the-tds-parameters"></a>Määritä TDS-parametrit

[!include [banner](../includes/banner.md)]

Tässä aiheessa kuvataan, kuinka määritetään parametrit, jotka aktivoivat Vero vähennettynä lähteissä (TDS) -toiminnon määritetyissä tapahtumissa. Tämä on tarpeellinen vaihe, kun haluat käyttää Vero vähennettynä lähteissä (TDS) -toimintoa.

1. Siirry kohtaan **Kirjanpito \> Kirjanpidon asetukset \> Kirjanpitoparametrit**.
2. Määritä **Suorat verot** -välilehden **Vero vähennettynä lähteissä** -osiossa **Aktivoi TDS** -asetuksen arvoksi **Kyllä** aktivoidaksesi TDS-toiminnon sekä siihen käytettävät sivut ja kentät.
3. Valitse **Lasku**-asetuksen arvoksi **Kyllä**, jos haluat ottaa käyttöön kentät, joita käytetään TDS:n laskentaan ja vähennykseen laskutasolla.
4. Valitse **Maksu**-asetuksen arvoksi **Kyllä**, jos haluat ottaa käyttöön kentät, joita käytetään TDS:n laskentaan ja vähennykseen maksutasolla.

    [![Suorat verot -välilehti.](./media/apac-ind-TDS-1.png)](./media/apac-ind-TDS-1.png)

5. Etsi **Numerosarjat**-välilehdestä rivi, jonka **Viite**-kentän arvoksi on määritetty **Ennakonpidätysmaksu**. Valitse numerosarjan koodi rivin **Numerosarjan koodi** -kentässä. Numerosarjan koodin avulla luodaan tositenumerot kausittaista TDS-tilitysprosessia varten.

    > [!NOTE]
    > Voit suorittaa kausittaisen TDS-tilitysprosessin valitsemalla **Vero \> Ilmoitukset \> Ennakonpidätys \> Ennakonpidätysmaksu**.

    [![Numerosarjat-välilehti.](./media/apac-ind-TDS-2.png)](./media/apac-ind-TDS-2.png)

6. Sulje sivu.
