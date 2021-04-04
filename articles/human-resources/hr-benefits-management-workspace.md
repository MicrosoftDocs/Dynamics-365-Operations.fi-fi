---
title: Etujen hallinnan työtila
description: Tässä aiheessa kuvataan Dynamics 365 Human Resources -sovellukseen sisältyvä etujen hallinnan työtila.
author: andreabichsel
manager: tfehr
ms.date: 02/24/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-24
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8f17685dab8159522ec88af0fa6ca9c99c346b7b
ms.sourcegitcommit: 105f65468b45799761c26e5d0ad9df4ff162c38d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/04/2021
ms.locfileid: "5488195"
---
# <a name="benefits-management-workspace"></a>Etujen hallinnan työtila

[!include [applies to](../includes/applies-to-hr.md)]

[!include [preview feature](./includes/preview-feature.md)]

Tässä aiheessa kuvataan Dynamics 365 Human Resources -sovellukseen sisältyvä **etujen hallinnan työtila**.

> [!NOTE]
> Jos haluat nähdä **etujen hallinnan työtilan**, sinun täytyy ottaa **(Esikatselu) Etujen hallinnan työtila** -ominaisuus käyttöön ominaisuuksien hallinnasta. Lisätietoja esiversiotoimintojen käyttöönotosta on kohdassa [Ominaisuuksien hallinta](../hr-admin-manage-features.md).<br><br>![Etujen hallinnan työtilan käyttöönotto](./media/hr-benefits-management-workspace-enable.png)

**Etujen hallinnan työtilan** avulla voit katsastaa nopeasti etujen nimikkeet, jotka vaativat huomiotasi. Tällä sivulla näytetään seuraavat tiedot:

- Toimintoa odottavien nimikkeiden kokonaismäärät
- Työntekijät, joilla on vahvistamattomia valintoja
- Työntekijät, jotka rekisteröityvät etuihin äskettäin
- Työntekijät, joilla on tulevia elinkaaritapahtumia
- Uudet työntekijät, jotka eivät ole rekisteröityneet
- Työntekijät, joilla on aktiivisia elinkaaritapahtumia
- Työntekijät, joilla on avoimia rekisteröitymisiä, jotka eivät ole valinneet yhtään suunnitelmaa

![Etujen hallinnan työtila](./media/hr-benefits-management-workspace.png)

## <a name="view-action-items"></a>Toimintonimikkeiden tarkasteleminen

Voit tarkastella toimintonimikkeitä valitsemalla ruudun tai välilehden. Jos valitset välilehden, voit tarkastella ja valita työntekijöitä suoraan työtilan sivulta.

![Toimintonimikkeet](./media/hr-benefits-management-workspace-action-items.png)

Jos valitset ruudun, siirryt kyseiselle sivulle. Esimerkiksi seuraavien ruutujen valitseminen näyttää **Työntekijän etuussuunnitelmat** -sivun, joka on suodatettu näyttämään toimenpiteitä vaativat työntekijät:

- **Vahvistamattomat valinnat**
- **Avoimet rekisteröinnit, joilla ei ole uloskuitattuja suunnitelmia**
- **Rekisteröity etuihin**
- **Uutta työntekijää ei ole rekisteröity**

![Työntekijän etusuunnitelmat](./media/hr-benefits-management-workspace-plans.png)

**Aktiiviset elinkaaritapahtumat**- tai **Tulevat elinkaaritapahtumat** -ruutujen valitseminen sinut aktiivisten tai tulevien elinkaaritapahtumien luetteloon.

![Elinkaaritapahtumat](./media/hr-benefits-management-workspace-life-events.png)

## <a name="processing"></a>Käsittely

Jos haluat käsitellä rekisteröintikelpoisuutta, elinkaaritapahtumia tai hintamuutosten päivityksiä, valitse asiaankuuluva nimike siirtymispalkista.

![Käsittely](./media/hr-benefits-management-workspace-processing.png)

Voit tarkastaa prosessin tulokset valitsemalla **Prosessin tulokset** -sivun.

![Prosessin tulokset](./media/hr-benefits-management-workspace-process-results.png)

Lisätietoja etujen käsittelystä on kohdissa:

- [Rekisteröitymiskelpoisuuksien käsittely](hr-benefits-process-enrollment-eligibility.md)
- [Elämäntapahtumien muutosten käsittely](hr-benefits-process-life-event-changes.md)
- [Elämäntapahtumien oikeutusten käsittely](hr-benefits-process-life-event-eligibility.md)
- [Elämäntapahtumien käsittely](hr-benefits-process-life-events.md)
- [Hintamuutosten käsittely](hr-benefits-process-rate-changes.md)

## <a name="change-period"></a>Ajanjakson muuttaminen

Jos haluat tarkastella etuja toiselta ajanjaksolta, valitse se **Kausi**-pudotusvalikosta.

![Ajanjakson muuttaminen](./media/hr-benefits-management-workspace-period.png)

## <a name="view-more-options"></a>Lisävaihtoehtojen tarkasteleminen

Jos haluat nähdä lisätietoja ja muita tehtäviä toimenpiteitä, valitse **Linkit**.

![Linkit](./media/hr-benefits-management-workspace-links.png)

## <a name="see-also"></a>Lisätietoja

[Etujen hallinnan yleiskatsaus](hr-benefits-management-overview.md)