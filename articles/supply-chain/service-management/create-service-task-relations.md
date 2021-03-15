---
title: Huoltotehtävän suhteiden luominen
description: Voi liittää huoltotehtäviä huoltosopimuksiin tai huoltotilauksiin kuvataksesi sopimuksen tai tilauksen huoltotehtävää.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 9e5fd978c1e9db7e7ce3c06bbeb45b59854f1582
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974657"
---
# <a name="create-service-task-relations"></a>Huoltotehtävän suhteiden luominen    

[!include [banner](../includes/banner.md)]

Voi liittää huoltotehtäviä huoltosopimuksiin tai huoltotilauksiin kuvataksesi sopimuksen tai tilauksen huoltotehtävää. Sekä teknikot että asiakkaat näkevät nämä tiedot.

## <a name="create-a-relation-with-a-service-agreement"></a>Suhteen luominen huoltosopimukseen

1.  Valitse **Palvelunhallinta** \> **Yleinen** \> **Palvelusopimukset** \> **Palvelusopimukset**.

2.  Valitse nykyinen huoltosopimus tai luo uusi huoltosopimus.

3.  Valitse toimintoruudussa **Huoltotehtävät**-painike.

4.  Paina **Huoltotehtävät**-lomakkeessa CTRL + N luodaksesi uuden rivin, ja valitse sitten huoltosopimukseen liitettävä huoltotehtävä **Huoltotehtävä**-luettelosta.

5.  Lisää **Kuvaus** -välilehden vapaatekstikenttiin mahdolliset sisäisten tai ulkoisten huomautusten kuvaukset.

6.  Tallenna tietue sulkemalla lomake.

Toista tämä toimenpide, kunnes olet luonut huoltosopimuksen kaikki tarvittavat huoltotehtäväsuhteet. Voit nyt määrittää nämä huoltotehtävät liittyville huoltoriveille.

Huoltosopimukselle luotavat huoltotehtäväsuhteet ovat käytettävissä kaikissa huoltotilauksissa, jotka liittyvät huoltosopimukseen.

## <a name="create-a-relation-with-a-service-order"></a>Suhteen luominen huoltotilaukseen

1.  Valitse **Huoltohallinta** \> **Yleinen** \> **Huoltotilaukset** \> **Huoltotilaukset**.

2.  Valitse nykyinen huoltotilaus tai luo uusi huoltotilaus.

3.  Valitse toimintoruudussa **Huoltotehtävät**-painike.

4.  Paina **Huoltotehtävät**-lomakkeessa CTRL + N luodaksesi uuden rivin, ja valitse sitten huoltotilaukseen liitettävät huoltotehtävät **Huoltotehtävä**-luettelosta.

5.  Lisää **Kuvaus** -välilehden vapaatekstikenttiin mahdolliset sisäisten tai ulkoisten huomautusten kuvaukset.

6.  Tallenna tietue sulkemalla lomake.

Toista tämä toimenpide, kunnes olet luonut huoltotilauksen kaikki tarvittavat huoltotehtäväsuhteet. Kun luot huoltotilausrivejä, voit valita huoltotehtävän, jolle suhde luotiin.

Huoltotilaukselle luotavat huoltotehtäväsuhteet ovat käytettävissä kyseisessä huoltotilauksessa.

## <a name="see-also"></a>Lisätietoja

[Huoltotehtävien yleiskatsaus](service-tasks.md)


  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]