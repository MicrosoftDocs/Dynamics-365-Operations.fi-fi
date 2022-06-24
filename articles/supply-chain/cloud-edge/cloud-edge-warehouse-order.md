---
title: Varastotilausten pilvi- ja reunapalvelujen scale unitit
description: Tässä artikkelissa käsitellään varastotilausominaisuutta, jota käytetään varaston scale unitin työkuorman osana.
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
ms.openlocfilehash: db254216e6c34b81f83c87a8fda454d0aeb1cece
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8893523"
---
# <a name="warehouse-orders-for-cloud-and-edge-scale-units"></a>Varastotilausten pilvi- ja reunapalvelujen scale unitit

[!include [banner](../includes/banner.md)]

> [!WARNING]
> Kaikkia liiketoimintatoimintoja ei tueta kokonaisuudessaan julkisessa esiversiossa, kun scale unitin kuormituksia käytetään. Jos scale unitit ovat käytössä, on varmistettava, että vain niitä prosesseja käytetään, joiden tuesta nimenomaisesti ilmoitetaan tässä artikkelissa.

## <a name="what-are-warehouse-orders"></a>Mitä varastotilaukset ovat?

*Varastotilaukset* ovat tilaustyyppi, jota käytetään tukemaan keskusta ja scale unitia hyödyntäviä varaston käyttöönottoja. Niiden avulla voidaan vastaanottaa ja lähettää varastoa, kun varastotyökuorma suoritetaan scale unitissa.

Varastotilauksia käytetään sekä saapuvien että lähtevien varastonhallintakäsittelyjen osana. Ne luodaan osana *Varastoon vapautus* -prosessia, joka käynnistetään keskuksessa.
Saapuvan käsittelyn osalta Warehouse Mobile Appia käytetään fyysisen käytettävissä olevan varaston rekisteröintiin saapuvien tilausten käsittelyssä. Tämä on käytettävissä osto- ja tuotantotilauksissa, joissa eritellään scale unit -varasto ja nimikkeet, joiden osalta voi käyttää varastonhallintaprosesseja.
Lähteviä varastotilauksia käytetään osana lähetyksen aaltoprosessia siirto- ja ostotilausten osalta.

> [!IMPORTANT]
> Varastotilaukset ovat käytettävissä vain käyttöönotoissa, joissa käytetään [varastonhallinnan kuormitusten pilvi- ja reunapalvelujen scale uniteja](cloud-edge-workload-warehousing.md).

## <a name="create-an-inbound-warehouse-order"></a>Saapuvan varastotilauksen luominen

Voit luoda saapuvan varastotilauksen ostotilausprosessia varten noudattamalla seuraavia ohjeita.

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
