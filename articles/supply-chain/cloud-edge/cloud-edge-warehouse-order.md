---
title: Varastotilausten pilvi- ja reunapalvelujen scale unitit
description: Tässä aiheessa käsitellään varastotilausominaisuutta, jota käytetään varaston scale unitin työkuorman osana.
author: perlynne
manager: tfeyr
ms.date: 01/14/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWarehouseOrderLine, WHSWarehouseReceiptEntry, PurchTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2021-01-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: c04127b9fe621d962be2d7fe06358b3bd1b78916
ms.sourcegitcommit: 289e9183d908825f4c8dcf85d9affd4119238d0c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/02/2021
ms.locfileid: "5105704"
---
# <a name="warehouse-orders-for-cloud-and-edge-scale-units"></a>Varastotilausten pilvi- ja reunapalvelujen scale unitit

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!WARNING]
> Kaikkia liiketoimintatoimintoja ei tueta kokonaisuudessaan julkisessa esiversiossa, kun scale unitin kuormituksia käytetään. Jos scale unitit ovat käytössä, on varmistettava, että vain niitä prosesseja käytetään, joiden tuesta nimenomaisesti ilmoitetaan tässä aiheessa.

## <a name="what-are-warehouse-orders"></a>Mitä varastotilaukset ovat?

*Varastotilaukset* ovat tilaustyyppi, joka luotiin tukemaan keskusta ja scale unitia hyödyntäviä varaston käyttöönottoja. Niiden avulla voidaan vastaanottaa varastoa, kun varastotyökuorma suoritetaan scale unitissa. Niitä käytetään tällä hetkellä vain ostotilausten yhteydessä.

Varastotilauksia käytetään varastonhallintaprosessien osana esimerkiksi silloin, kun varastosovelluksella kirjataan fyysinen käytettävissä oleva varasto saapuvan ostotilauksen käsittelyn aikana. Varastotilaukset luodaan *Vapauta varastoon* -prosessin osana. Tätä prosessia voi käyttää ostotilauksissa, jotka määrittävät scale unit -varaston, ja nimikkeissä, joissa varastonhallintaprosessien käyttö on otettu käyttöön.

> [!IMPORTANT]
> Varastotilaukset ovat käytettävissä vain käyttöönotoissa, joissa käytetään [varastonhallinnan kuormitusten pilvi- ja reunapalvelujen scale uniteja](cloud-edge-workload-warehousing.md).

## <a name="create-a-warehouse-order"></a>Varastotilauksen luominen

Varastotilaus luodaan seuraavasti:

1. Kirjaudu Microsoftin Dynamics 365 Supply Chain Managementn esiintymään, joka suoritetaan keskuksessa. (*Vapauta varastoon* -prosessi on käynnistettävä keskukseen kirjautuneena.)
1. Siirry kohtaan **Hankinta ja alihankinta \> Ostotilaukset \> Kaikki ostotilaukset**.
1. Valitse toimintoruudussa **Varasto**-välilehden **Toiminnot**-ryhmässä **Vapauta varastoon**.
1. Liittyviä varastotilauksia rivejä voi tarkastella avaamalla liittyvän ostotilauksen, valitsemalla rivin **Ostotilausrivit**-osassa ja valitsemalla sitten työkalurivillä **Varasto \> Varastotilausrivit**. Kaikki rivit voidaan näyttää valitsemalla **Varastonhallinta \> Kyselyt ja raportit \> Varastotilausrivit**.

## <a name="cancel-a-warehouse-order"></a>Varastotilauksen peruuttaminen

*Vapauta varastoon* -prosessin osana keskus linkittää ostotilauksen varastotapahtumat varastotilauksiin ja lukitsee niiden päivittämisen. Jos vapautus varastoon on tehty vahingossa tai jos varastotilausrivien luonti halutaan peruuttaa jostain muusta syystä, varastotilausrivien peruuttamista voidaan pyytää.

Varastotilausrivit peruutetaan seuraavasti:

1. Kirjaudu Supply Chain Managementin esiintymään, joka suoritetaan keskuksessa.
1. Valitse **Varastonhallinta \> Kyselyt ja raportit \> Varastotilausrivit**.
1. Valitse rivi.
1. Valitse toimintoruudussa **Peruuta varastotilausrivit**.

> [!NOTE]
> Sellaisten rivien peruuttamispyyntö hylätään, jotka jo odottavat peruuttamista tai joita käsitellään aktiivisesti työkuorman scale unitissa suorittavassa varastossa.

## <a name="monitor-a-warehouse-order"></a>Varastotilauksen seuraaminen

**Varastotilausrivit**-näkymässä voi seurata saapuvan vastaanoton etenemistä tarkastelemalla **Jäljellä oleva vastaanotettava määrä** -sarakkeen arvoja. Varastosovelluksella tehtävään työhön liittyviä tietoja voi tarkastella jollakin seuraavista tavoista:

- Valitse **Varastonhallinta \> Kyselyt ja raportit \> Varastotilausrivit** ja etsi rivit suodattimen avulla.
- Valitse **Hankinta \> Ostotilaukset \> Kaikki ostotilaukset** ja avaa kyseinen ostotilaus. Valitse **Ostotilausrivit**-osassa vähintään yksi rivi ja valitse sitten työkalurivillä **Varasto \> Varaston vastaanottoviennit**.
