---
title: Ensisijaisen teknikon määrittäminen
description: Voit valita minkä tahansa työntekijän ensisijaiseksi teknikoksi huoltosopimukseen tai huoltotilaukseen.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAAgreementTable, SMADispatchBoard
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 80ea0265eb27fb5cf32f5f921caa7ac2e44a0116
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2020
ms.locfileid: "3217284"
---
# <a name="set-up-a-preferred-technician"></a>Ensisijaisen teknikon määrittäminen 

[!include [banner](../includes/banner.md)]


Voit valita minkä tahansa työntekijän ensisijaiseksi teknikoksi huoltosopimukseen tai huoltotilaukseen. On kuitenkin hyvä ajatus lisätä työntekijä asianmukaiseen resursointiryhmään siten, että työntekijä on mukana **Resursointitaulussa**.

## <a name="assign-employee-to-a-dispatch-team"></a>Työntekijän määrittäminen resursointiryhmään

1.  Valitse **Henkilöstöhallinto** \> **Yleinen** \> **Työntekijät** \> **Työntekijät**. Kaksoisnapsauta työntekijää avataksesi työntekijän tiedot -sivun. Valitse **toimintoruudussa** **Asetukset** \>**Resursointiryhmä** avataksesi **Resursoi työntekijöitä** -lomakkeen.

2.  Valitse **Resursointiryhmä**-kentässä työntekijään liitettävä ryhmä.

## <a name="assign-a-preferred-technician-to-a-service-agreement"></a>Ensisijaisen teknikon määrittäminen huoltosopimukseen

1.  Valitse **Palvelunhallinta** \> **Yleinen** \> **Palvelusopimukset** \> **Palvelusopimukset**. Avaa tietolomake kaksoisnapsauttamalla huoltosopimusta.

2.  Valitse **Yleinen**-välilehdellä **Ensisijainen teknikko** -kenttä ja valitse sitten sopivan resursointiryhmän jäsen huoltosopimuksen ensisijaiseksi teknikoksi.

## <a name="assign-a-preferred-technician-to-a-service-order"></a>Ensisijaisen teknikon määrittäminen huoltotilaukseen

1.  Valitse **Huollon hallinta** \> **Kausittainen** \> **Resursointitaulu**.
    

    > [!NOTE]
    > <P>Määritä <STRONG>Resursointitaulu</STRONG>-lomakkeessa tarkasteltavien resursointitehtävien päivämääräväli. Voit myös määrittää, haluatko näyttää suljettuja tehtäviä ja haluatko rajoittaa resursointitehtävien käytön ryhmille, joihin kuulut tai joille on annettu valintaoikeudet. Avaa <STRONG>Resursointitaulu</STRONG> valitsemalla <STRONG>OK</STRONG>.</P>



2.  Valitse muokattavan huoltotoiminnan rivi.

3.  Valitse **Liittyvä**-välilehti ja määritä **Työntekijä**-luettelosta asianmukaisen resursointiryhmän jäsen huoltokäynnin ensisijaiseksi teknikoksi.

## <a name="see-also"></a>Lisätietoja

[Huoltosopimusten laatiminen ja luominen – yleiskatsaus](service-agreements.md)

[Huoltotilausten luominen manuaalisesti](create-service-orders-manually.md)

[Palvelusopimukset (lomake)](https://technet.microsoft.com/library/aa617823\(v=ax.60\))
  


