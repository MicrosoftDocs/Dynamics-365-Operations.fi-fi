---
title: Ensisijaisen teknikon määrittäminen
description: Voit valita minkä tahansa työntekijän ensisijaiseksi teknikoksi huoltosopimukseen tai huoltotilaukseen.
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAAgreementTable, SMADispatchBoard
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4c9495bbc8e5f7cb603c027a125887feba1f0e2d
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/15/2022
ms.locfileid: "9017200"
---
# <a name="set-up-a-preferred-technician"></a>Ensisijaisen teknikon määrittäminen 

[!include [banner](../includes/banner.md)]


Voit valita minkä tahansa työntekijän ensisijaiseksi teknikoksi huoltosopimukseen tai huoltotilaukseen. On kuitenkin hyvä ajatus lisätä työntekijä asianmukaiseen resursointiryhmään siten, että työntekijä on mukana **Resursointitaulussa**.

## <a name="assign-employee-to-a-dispatch-team"></a>Työntekijän määrittäminen resursointiryhmään

1.  Valitse **Henkilöstöhallinto** \> **Työntekijät** \> **Työntekijät**. Kaksoisnapsauta työntekijää avataksesi työntekijän tiedot -sivun. Valitse **toimintoruudussa** **Asetukset** \>**Resursointiryhmä** avataksesi **Resursoi työntekijöitä** -lomakkeen.

2.  Valitse **Resursointiryhmä**-kentässä työntekijään liitettävä ryhmä.

## <a name="assign-a-preferred-technician-to-a-service-agreement"></a>Ensisijaisen teknikon määrittäminen huoltosopimukseen

1.  Valitse **Palvelujen hallinta** \> **Huoltosopimukset** \> **Huoltosopimukset**. Avaa tietolomake kaksoisnapsauttamalla huoltosopimusta.

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
  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]