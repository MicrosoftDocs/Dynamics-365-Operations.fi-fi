---
title: Työntekijät, joilla ei työsuhdetta
description: Työntekijät, joilla ei ole organisaatiossasi tulevia, aktiivisia tai historiallisia työtehtäviä, näkyvät Työntekijät, joilla ei ole työsuhdetta -sivulla.
author: twheeloc
ms.date: 11/03/2021
ms.topic: ''
ms.prod: ''
ms.technology: ''
ms.search.form: HcmWorkerV2, HRMMassHireProject, HRMMassHireLine, HcmPersonnelManagementWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-04-06
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d282c0fac00d6bc410717dd156aef9ffce352c6d
ms.sourcegitcommit: 7e0e2a266d9a9473df72e207554d9bd150e17ce3
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/05/2021
ms.locfileid: "7771287"
---
# <a name="workers-without-employment"></a>Työntekijät, joilla ei työsuhdetta

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Työntekijät, joilla ei ole organisaatiossasi tulevia, aktiivisia tai historiallisia työtehtäviä, näkyvät **Työntekijät, joilla ei ole työsuhdetta** -sivulla. Tämän tyyppiset työntekijät voivat näkyä, kun tuot työntekijöitä, joilla ei ole työntekijän tietuetta, tai kun poistat työntekijän työsuhteen kohdassa **Työntekijät \> Työhistoria**.

Oletusarvoisesti **Työntekijät, joilla ei ole työsuhdetta** -sivu on seuraavien roolien käytettävissä:

- Henkilöstöapulainen
- Henkilöstöpäällikkö
- Työhönottaja
- Kompensaatioiden ja etujen päällikkö
- Palkanlaskentakoordinaattori
- Palkanlaskentapäällikkö
- Koulutuspäällikkö

Voit poistaa **Työntekijät, joilla ei ole työsuhdetta** -luettelossa olevat henkilöt. Oletusarvon mukaan tämä oikeus annetaan henkilöstöapulaisen roolille. Voit antaa oikeuden muille rooleille seuraavasti:

1. Valitse **Järjestelmän hallinta** ja valitse sitten **Suojauskonfiguraatio**-välilehti.

2. Suodata **Oikeudet**-välilehdessä **Oikeudet**-luettelo ja **Ylläpidä työntekijöitä**.

   [![Suodata Oikeudet-luettelo.](./media/hr-personnel-workers-without-employment-filter.png)](./media/hr-personnel-workers-without-employment-filter.png)

3. Valitse **viitteet**-sarakkeesta **Näytä valikon vaihtoehdot**.

4. Valitse **Näytä valikon vaihtoehdot**-sarakkeesta **HcmWorkersWithoutEmployment**.

   [![Valitse lomake.](./media/hr-personnel-workers-without-employment-select.png)](./media/hr-personnel-workers-without-employment-select.png)

5. Määritä **Poisto**-oikeudeksi **Myönnä**.

6. Valitse **Julkaisemattomat objektit** -välilehti.

7. Valitse **Julkaise kaikki**.

   [![Julkaise muutokset.](./media/hr-personnel-workers-without-employment-publish.png)](./media/hr-personnel-workers-without-employment-publish.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
