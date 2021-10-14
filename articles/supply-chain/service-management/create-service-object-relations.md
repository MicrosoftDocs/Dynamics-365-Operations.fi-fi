---
title: Huoltokohteen suhteiden luominen
description: Tässä ohjeaiheessa kuvataan, kuinka huoltosopimukselle ja huoltotilaukselle voidaan luoda huoltokohteiden suhteita.
author: kamaybac
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0a558d513ba97d7df72ee785704b84dd38a5929b
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/29/2021
ms.locfileid: "7569116"
---
# <a name="create-service-object-relations"></a>Huoltokohteen suhteiden luominen 

[!include [banner](../includes/banner.md)]


Tässä ohjeaiheessa kuvataan, kuinka huoltosopimukselle ja huoltotilaukselle voidaan luoda huoltokohteiden suhteita. Kun luot huolto-objektin suhteen, liität huoltokohteen huoltosopimukseen tai huoltotilaukseen. Asiakkaan pyytäessä huoltoa nimikkeelle, joka on huoltokohde, voit valita huoltokohteen huoltokohteen suhdeluettelosta.

## <a name="create-a-service-object-relation-for-a-service-agreement"></a>Luo huoltokohteen suhde huoltosopimukselle

Luo uusi huoltokohteen suhde huoltosopimukselle seuraavien ohjeiden avulla:

1.  Valitse **Palvelunhallinta** \> **Yleinen** \> **Palvelusopimukset** \> **Palvelusopimukset**.

2.  Valitse **Huoltosopimukset**-luettelosta aiemmin luotu huoltosopimus tai valitse **Uusi** luodaksesi uuden huoltosopimuksen.

3.  Napsauta **Huoltosopimukset**-lomakkeen **toimintoruudussa** **Huoltosopimus**-välilehden **Suhteet**-ryhmässä **Huoltokohteet**

4.  Valitse **Huoltokohteet**-lomakkeesta **Uusi** ja valitse sitten huoltokohde tälle palvelusopimukselle.

5.  Voit määrittää mallituoterakenteen (BOM) huoltosopimukseen napsauttamalla **Toiminnot** ja valitsemalla sitten **Liitä mallituoterakenne**. Valitse malli **Valitse mallituoterakenne**-lomakkeen **Mallituoterakenne**-kentässä. 

## <a name="create-a-service-object-relation-for-a-service-order"></a>Luo huoltokohteen suhde huoltotilaukselle

Luo uusi huoltokohteen suhde huoltotilaukselle seuraavien ohjeiden avulla:

1.  Valitse **Huoltohallinta** \> **Yleinen** \> **Huoltotilaukset** \> **Huoltotilaukset**.

2.  **Huoltotilaukset**-luettelosta valitse nykyinen huoltotilaus tai luo uusi huoltotilaus.

3.  Napsauta **Huoltotilaukset**-lomakkeen **toimintoruudussa** **Huoltotilaus**-välilehden **Suhteet**-ryhmässä **Huoltokohteet**

4.  Valitse **Huoltokohteet**-lomakkeesta **Uusi** ja valitse sitten huoltokohde tälle huoltotilaukselle.

5.  Voit määrittää mallituoterakenteen (BOM) huoltosopimukseen napsauttamalla **Toiminnot** ja valitsemalla sitten **Liitä mallituoterakenne**. Valitse malli **Valitse mallituoterakenne**-lomakkeen **Mallituoterakenne**-kentässä. 


## <a name="see-also"></a>Lisätietoja

[Huoltokohteiden yleiskatsaus](service-objects.md)

[Huoltokohteen suhteet](service-object-relations.md)

[Mallituoterakenteet](template-boms.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]