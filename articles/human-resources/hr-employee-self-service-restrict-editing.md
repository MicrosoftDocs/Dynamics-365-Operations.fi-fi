---
title: Henkilökohtaisten tietojen muokkaamisen rajoittaminen
description: Estä työntekijöitä muokkaamasta yhteystietoja Dynamics 365 Human Resources -sovelluksessa.
author: twheeloc
ms.date: 08/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EssWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c82114f6600345ee5e2eb9c1c0629ae6c8f0b9a7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8877682"
---
# <a name="restrict-editing-of-personal-information"></a>Henkilökohtaisten tietojen muokkaamisen rajoittaminen


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [applies to](../includes/applies-to-hr.md)]
[!include [preview feature](./includes/preview-feature.md)]

Tässä artikkelissa kuvataan, kuinka työntekijöitä voi estää muokkaamasta yhteystietoja Dynamics 365 Human Resources -sovelluksessa. Saatat haluta estää työntekijöitä muokkaamasta tiettyjä yhteystietoja, kuten yrityksen sijaintia tai sähköpostiosoitetta.

> [!NOTE]
> Ennen kuin voit käyttää tätä ominaisuutta, sinun täytyy ottaa käyttöön **(Esikatselu) Estä työntekijöitä lisäämästä tai muokkaamasta osoite- ja yhteystietoja tiettyihin tarkoituksiin** -ominaisuus käyttöön ominaisuuksien hallinnasta. Lisätietoja esiversiotoimintojen käyttöönotosta on kohdassa [Ominaisuuksien hallinta](hr-admin-manage-features.md).<br><br>![Ota esikatselutoiminto käyttöön.](./media/hr-employee-self-service-restrict-enable.png)

## <a name="choose-the-information-an-employee-can-add-or-edit"></a>Valitse tiedot, jotka työntekijä voi lisätä tai muokata

1. Valitse Human Resourcesissa ensin **Henkilöstön hallinta**, sitten **Linkit** ja lopuksi **Henkilöstöhallintoparametrit**.

   ![Valitse Henkilöstöhallintoparametrit.](./media/hr-employee-self-service-human-resources-parameters.png)

2. Valitse **Henkilöstöhallintoparametrit** -sivulta **Työntekijän itsepalvelu** -välilehti.

   ![Valitse Työntekijän itsepalvelu.](./media/hr-employee-self-service-tab.png)

3. Poista **Työntekijän itsepalvelu** -välilehden **Osoite- ja yhteystiedot** -osiosta kaikkien niiden tietojen valinta, joita et halua työntekijöiden lisäävän tai muokkaavan. Tässä esimerkissä olemme poistaneet **yrityksen** yhteystietojen valinnan.

   ![Yrityksen yhteystietojen muokkaamisen rajoittaminen.](./media/hr-employee-self-service-restrict-business.png)

4. Valitse **Tallenna**.

   ![Tallenna muutokset.](./media/hr-employee-self-service-restrict-save.png)

## <a name="employee-experience"></a>Työntekijäkokemus

Kun olet estänyt työntekijöitä lisäämästä tai muokkaamasta yhteystietoja, he näkevät kyseiset tiedot, mutta eivät voi muuttaa niitä.

Tässä esimerkissä työntekijöitä on estetty muokkaamasta **yrityksen** yhteystietoja, mutta he voivat silti nähdä **työntekijän itsepalvelun** tiedot:

![Yrityksen yhteystietojen tarkasteleminen.](./media/hr-employee-self-service-restrict-view.png)

Kun työntekijät valitsevat yrityksen yhteystiedot, he näkevät **Muokkaa osoitetta** -ruudun Vain luku -tilassa eivätkä he voi muuttaa kenttiä.

![Yrityksen yhteystiedot näytetään Vain luku -muodossa.](./media/hr-employee-self-service-restrict-read-only.png)

Jos he lisäävät uuden osoitteen valitsemalla **Lisää**, he eivät voi valita **Yritys**-vaihtoehtoa **Tarkoitus**-pudotusvalikosta.

![Työntekijä ei voi lisätä yrityksen osoitetta.](./media/hr-employee-self-service-restrict-add.png)

Työntekijöillä on sama kokemus, kun he valitsevat **Henkilökohtaiset tiedot** -sivulta **Yhteystiedot** ja lisäävät uuden osoitteen. **Tarkoitus**-pudotusvalikossa näytetään vain sentyyppiset tiedot, joita he voivat lisätä. 

![Työntekijä ei voi valita Yritys-vaihtoehtoa Tarkoitus-pudotusvalikosta.](./media/hr-employee-self-service-restrict-purpose.png)

**Tarkoitus** näytetään nyt **Yhteystiedot**-ruudukossa.

![Tarkoitus näytetään Yhteystiedot-ruudukossa.](./media/hr-employee-self-service-restrict-purpose-grid.png)

## <a name="see-also"></a>Lisätietoja

[Työntekijän ja esimiehen itsepalvelun yleiskatsaus](hr-employee-manager-self-service-overview.md)<br>
[Määritä Human Resourcesin parametrit](hr-setup-parameters.md)<br>
[Muokkaa henkilökohtaisia tietoja](hr-employee-manager-self-service-edit-personal-information.md)
