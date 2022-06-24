---
title: Päivitä siirrettävä budjetti ostotilausten ja laskujen vähennysten jälkeen
description: Tässä artikkelissa kuvataan, miten hallitaan, mitä siirrettävälle budjetille tapahtuu, kun ostotilaukset peruutetaan tai vähennetään ja laskuja vähennetään.
author: TaylorVH
ms.date: 02/11/2022
ms.topic: article
ms.search.form: LedgerFund
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-savanh
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2022-02-01
ms.openlocfilehash: 7f0ef0ffdf697609e811f754b4378b1f7a81c494
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8897955"
---
# <a name="update-the-carry-forward-budget-after-reductions-in-purchase-orders-and-invoices"></a>Päivitä siirrettävä budjetti ostotilausten ja laskujen vähennysten jälkeen

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Tässä artikkelissa kuvataan, miten hallitaan, mitä siirrettävälle budjetille tapahtuu, kun ostotilaukset peruutetaan tai vähennetään ja laskuja vähennetään.

Tietoja ostotilausten käsittelemiseen vuoden lopussa on kohdassa [Ostotilausten käsitteleminen vuoden lopussa](/dynamicsax-2012/appuser-itpro/process-purchase-orders-at-year-end).

## <a name="turn-carry-forward-budget-reductions-for-invoice-variances-on-or-off"></a>Ota siirrettävän budjetin vähennykset käyttöön laskuvaihtelulle tai poista ne käytöstä

Järjestelmä voi aina päivittää siirrettävän budjetin, kun ostotilaus peruutetaan tai vähennetään. Jos kuitenkin haluat päivittää siirrettävän budjetin laskun vähentämisen yhteydessä, ota käyttöön *Pienennä siirrettävää budjettia, kun varianssi pienentää ostotilauksen laskua* -ominaisuus. Järjestelmänvalvojat voivat ottaa tämän ominaisuuden käyttöön tai pois käytöstä hakemalla toimintoa **[Toimintojen hallinta](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** -työtilassa.

## <a name="purchase-order-reductions-and-cancellations"></a>Ostotilausten vähennykset ja peruutukset

Riippumatta siitä, onko *Pienennä siirrettävää budjettia, kun varianssi pienentää ostotilauksen laskua* -ominaisuus käytössä, siirrettävä budjetti päivitetään, kun hyväksytty ostotilaus peruutetaan tai vähennetään. Voit määrittää kunkin kirjanpitorahaston vastaamaan seuraavilla tavoilla:

- Säilytä siirrettävä budjetti sellaisena kuin se luotiin.
- Poista peruutettu tai vähennetty summa oikaisemalla automaattisesti siirrettävää budjettia.

Vain ostotilausrivit, joissa on jakeluita, jotka sisältävät rahastoja, ovat käytettävissä automaattista budjetin oikaisua varten. Automaattinen budjetin oikaisu tapahtuu, kun ostotilaus viimeistellään tai ostotilausvähennys vahvistetaan.

## <a name="invoice-reductions"></a>Laskun vähennykset

Kun *Pienennä siirrettävää budjettia, kun varianssi pienentää ostotilauksen laskua* -ominaisuus on käytössä, voit määrittää pitääkö kunkin rahaston vähentää siirrettävää budjettia, kun lasku vähennetään sen lisäksi että ostotilaus peruutetaan tai vähennetään. Laskun on oltava ostotilausta varten, jolla on siirrettävä budjetti. Vähennyksiä ovat hinnan varianssit, veloitusvarianssit ja verovarianssit. Kun siirrettävä ostotilaus vähennetään laskutuksen aikana, luodaan varianssi. Kun lasku kirjataan, ostotilauksen varauksesta vähennetään varianssin summa. Toiminto luo myös automaattisen budjettioikaisun varianssin summalle.

Kun *Pienennä siirrettävää budjettia, kun varianssi pienentää ostotilauksen laskua* -ominaisuus ei ole käytössä, siirrettävää budjettia ei vähennetä tässä skenaariossa. Tästä syystä jäljellä oleva siirrettävä budjetti varianssin summalle jää jälkeen.

## <a name="configure-the-carry-forward-budget-options-for-each-fund"></a>Kunkin rahaston siirrettävä budjetin asetusten konfiguroiminen

Noudata näitä ohjeita jokaisessa kirjanpitorahastossa, jonka tulisi pystyä pienentämään siirrettävää budjettia, kun ostotilaus tai lasku vähennetään.

1. Valitse **Kirjanpito \> Tilikartta \> Varat \> Varat**.
1. Valitse rahasto, jonka haluat määrittää.
1. Varmista **Ostotilauksen vuoden lopun prosessi** -kohdassa , että **Ohita valittu vuoden lopun asetus** - asetuksena on *Kyllä*.
1. Määritä **Siirrettävän budjetin tila** -kohdassa **Palauta budjetti, kun siirrettävä ostotilaus peruutetaan tai pienennetään** -kenttä tarpeen mukaan. Asetuksilla on hieman erilaisia vaikutuksia sen mukaan, onko *Pienennä siirrettävää budjettia, kun varianssi pienentää ostotilauksen laskua* -ominaisuus käytössä järjestelmässä.

    - Kun toiminto on poistettu käytöstä, järjestelmä reagoi vain peruutettuihin tai vähennettyihin ostotilauksiin. Vaihtoehtojen asetukset toimivat seuraavasti:

        - *Ei* – Järjestelmä luo budjettirekisteritapahtuman peruutettujen tai vähennetyiden ostotilausten jäljellä olevalle saldolle.
        - *Kyllä* – Järjestelmä sallii ostotilausten peruutuksen tai vähennyksen, mutta ei luo budjettirekisteritapahtumaa. Siirrettävä budjetti pysyy muiden asiakirjojen käytettävissä.

    - Kun toiminto on on otettu käyttöön, järjestelmä reagoi sekä laskuvaihteluihin että peruutettuihin tai vähennettyihin ostotilauksiin. Vaihtoehtojen asetukset toimivat seuraavasti:

        - *Ei* – Laskuvariansseille järjestelmä luo varianssivähennyssummalle budjettirekisteritapahtuman ostotilauksen suhteen. Peruutetuissa tai vähennetyissä ostotilauksissa tällä asetuksella on sama vaikutus, joka sillä on, kun toiminto on poistettu käytöstä.
        - *Kyllä* – Laskuvariansseille järjestelmä sallii laskun vähennyksen, mutta ei luo budjettirekisteritapahtumaa. Siirrettävä budjetti pysyy muiden asiakirjojen käytettävissä. Peruutetuissa tai vähennetyissä ostotilauksissa tällä asetuksella on sama vaikutus, joka sillä on, kun toiminto on poistettu käytöstä.

## <a name="additional-resources"></a>Lisäresurssit

- [Ostotilausten tilinpäätösprosessi](/dynamicsax-2012/appuser-itpro/process-purchase-orders-at-year-end)
- [Ylläpidä yleisiä budjettivarauksia](general-budget-reservation-tasks.md)
- [Julkisen sektorin varat](funds-public-sector.md)
- [Julkisen sektorin rahoituksen määrittäminen](tasks/set-up-fund-public-sector.md)
