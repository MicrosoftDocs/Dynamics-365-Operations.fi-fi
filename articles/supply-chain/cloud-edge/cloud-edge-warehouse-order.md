---
title: Varastotilausten pilvi- ja reunapalvelujen scale unitit
description: Tässä aiheessa käsitellään varastotilausominaisuutta, jota käytetään varaston scale unitin työkuorman osana.
author: perlynne
ms.date: 04/22/2021
ms.topic: article
ms.search.form: WHSWarehouseOrderLine, WHSWarehouseReceiptEntry, PurchTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-04-13
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 4a77b157e9dd5ee1f551cbb59abbc89aaa28d325cc74a77e6624f25902c5b19e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6731886"
---
# <a name="warehouse-orders-for-cloud-and-edge-scale-units"></a>Varastotilausten pilvi- ja reunapalvelujen scale unitit

[!include [banner](../includes/banner.md)]

> [!WARNING]
> Kaikkia liiketoimintatoimintoja ei tueta kokonaisuudessaan julkisessa esiversiossa, kun scale unitin kuormituksia käytetään. Jos scale unitit ovat käytössä, on varmistettava, että vain niitä prosesseja käytetään, joiden tuesta nimenomaisesti ilmoitetaan tässä aiheessa.

## <a name="what-are-warehouse-orders"></a>Mitä varastotilaukset ovat?

*Varastotilaukset* ovat tilaustyyppi, joka luotiin tukemaan keskusta ja scale unitia hyödyntäviä varaston käyttöönottoja. Niiden avulla voidaan vastaanottaa varastoa, kun varastotyökuorma suoritetaan scale unitissa. Niitä käytetään tällä hetkellä vain ostotilausten yhteydessä.

Varastotilauksia käytetään varastonhallintaprosessien osana esimerkiksi silloin, kun varastonhallinnan mobiilisovelluksella kirjataan fyysinen käytettävissä oleva varasto saapuvan ostotilauksen käsittelyn aikana. Varastotilaukset luodaan *Vapauta varastoon* -prosessin osana. Tätä prosessia voi käyttää ostotilauksissa, jotka määrittävät scale unit -varaston, ja nimikkeissä, joissa varastonhallintaprosessien käyttö on otettu käyttöön.

> [!IMPORTANT]
> Varastotilaukset ovat käytettävissä vain käyttöönotoissa, joissa käytetään [varastonhallinnan kuormitusten pilvi- ja reunapalvelujen scale uniteja](cloud-edge-workload-warehousing.md).

## <a name="create-a-warehouse-order"></a>Varastotilauksen luominen

Varastotilaus luodaan seuraavasti:

1. Kirjaudu Microsoftin Dynamics 365 Supply Chain Managementn esiintymään, joka suoritetaan keskuksessa. (*Vapauta varastoon* -prosessi on käynnistettävä keskukseen kirjautuneena.)
1. Siirry kohtaan **Hankinta ja alihankinta \> Ostotilaukset \> Kaikki ostotilaukset**.
1. Valitse toimintoruudussa **Varasto**-välilehden **Toiminnot**-ryhmässä **Vapauta varastoon**.
1. Liittyviä varastotilauksia rivejä voi tarkastella avaamalla liittyvän ostotilauksen, valitsemalla rivin **Ostotilausrivit**-osassa ja valitsemalla sitten työkalurivillä **Varasto \> Varastotilausrivit**. Kaikki rivit voidaan näyttää valitsemalla **Varastonhallinta \> Kyselyt ja raportit \> Varastotilausrivit**.

Voit käynnistää *Vapauta varastoon* -prosessin myös erätyöstä valitsemalla **Varastonhallinta > Vapauta varastoon > Ostotilausten automaattinen vapautus**. Kun määrität erätyötä, voit valita tietyt ostotilausrivit kyselyn perusteella. Tyypillinen tilanne on määrittää toistuva erätyö, joka vapauttaa kaikki vahvistetut ostotilausrivit, joiden odotetaan saapuvan seuraavana päivänä.

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

**Varastotilausrivit**-näkymässä voi seurata saapuvan vastaanoton etenemistä tarkastelemalla **Jäljellä oleva vastaanotettava määrä** -sarakkeen arvoja. Varastonhallinnan mobiilisovelluksella tehtävään työhön liittyviä tietoja voi tarkastella jollakin seuraavista tavoista:

- Valitse **Varastonhallinta \> Kyselyt ja raportit \> Varastotilausrivit** ja etsi rivit suodattimen avulla.
- Valitse **Hankinta \> Ostotilaukset \> Kaikki ostotilaukset** ja avaa kyseinen ostotilaus. Valitse **Ostotilausrivit**-osassa vähintään yksi rivi ja valitse sitten työkalurivillä **Varasto \> Varaston vastaanottoviennit**.

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
