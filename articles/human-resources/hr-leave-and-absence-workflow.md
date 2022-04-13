---
title: Luo lomapyyntötyönkulku
description: Luo loma- ja poissaolopyyntöjen työnkulku, jonka avulla voit hallita lomapyyntöjä johdonmukaisesti Dynamics 365 Human Resources -ohjelmassa.
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b23dbf6a1923030abfadc6d82d57d5ea226b1e42
ms.sourcegitcommit: 67c4ed957e43d4d60bb609d93921a0be9619e675
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2022
ms.locfileid: "8509244"
---
# <a name="create-a-leave-request-workflow"></a>Luo lomapyyntötyönkulku

> [!Important]
> Tässä ohjeaiheessa mainittu toiminto on tällä hetkellä Dynamics 365 Human Resourcesin erillistä versiota käyttävien asiakkaiden käytettävissä. Osa toiminnoista tai kaikki toiminnot ovat saatavana osana Finance-infrastruktuurin tulevaa versiota, Finance-julkaisun 10.0.26 jälkeen.

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Voit luoda loma- ja poissaolopyyntöjen työnkulun, jonka avulla voit hallita lomapyyntöjä johdonmukaisesti Dynamics 365 Human Resources -ohjelmassa. **Loma ja poissaolo** -työnkulun avulla voit:

- Määrittää tehtäviä
- Määrittää, kenen tehtävät on suoritettava
- Määrittää, ketkä voivat hyväksyä tai hylätä pyyntöjä

## <a name="create-a-leave-and-absence-request-workflow"></a>Luoda loma- tai poissaolopyyntötyönkulun

1. Valitse **Lomat ja poissaolot** -sivulla **Linkit**-välilehti.

2. Valitse **Määritys**-kohdasta **Henkilöstöhallinnon työnkulut**.

3. Valitse **Uusi** ja valitse sitten **Loma- ja poissaolopyyntö**. 

4. Kun **Avaa tämä tiedosto?** -sanomaruutu tulee näkyviin, valitse **Avaa** ja kirjaudu sisään yrityksen tunnistetiedoilla.

5. Työnkulkueditorin avulla voit luoda työnkulun lomapyyntöihin. Lisätietoja työnkulkujen käyttämisestä on kohdassa [Luo työnkulkujen yhteenveto](../fin-ops-core/fin-ops/organization-administration/create-workflow.md?toc=%2fdynamics365%2fcommerce%2ftoc.json.)

## <a name="leave-and-absence-request-workflow-data-elements"></a>Loma- tai poissaolopyyntötyönkulun tietoelementit

Seuraavien tietoelementtien avulla voit luoda ehdollisia tai automaattisia hyväksyntöjä loma- ja poissaolopyyntöjen työnkuluissa:

- **summa**
- **Kommentti**
- **Yritys**
- **Luonut**
- **Luonnin päivämäärä ja aika**
- **Päättymispäivämäärä**
- **Lomatyyppi**
- **Muokkaaja**
- **Muokkauksen päivämäärä ja aika**
- **Syykoodi**
- **Pyynnön tunnus**
- **Aloituspäivämäärä**
- **Tila** 
- **Lähetyspäivämäärä**
- **Lähettäjä**
- **Henkilöstöhallinnon lähettämä**
- **Esimiehen lähettämä**
- **Lähetetty puolesta**
- **Työntekijä**
- **Työntekijätyyppi**

Nämä esimerkit osoittavat, miten voit luoda erityyppisiä työnkulkuehtoja käyttämällä näitä tietoelementtejä:

- Voit käyttää ehtolausekkeen **syykoodia** reitittämään sairauslomapyyntöjä, joiden syykoodi on **leikkaus** HR:n hyväksyttäväksi, ja reitittää kaikki muut syykoodit esimiehelle. Lisätietoja ehdollisesta lausekkeista on kohdassa [ehdollisen päätöksenteon määrittäminen työnkulussa](../fin-ops-core/fin-ops/organization-administration/configure-conditional-decision-workflow.md). 

- Käytä automaattisia **Henkilöstöhallinnon toimittama**- ja **Esimiehen lähettämä** -toimintoja, jotka hyväksyvät automaattisesti lomapyynnöt, jotka nämä roolit lähettävät työntekijöiden puolesta. Lisätietoja automaattisista toiminnoista on kohdassa [Määritä hyväksyntäprosessit työnkulussa](../fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow.md).

- Käytä **lomatyyppiä** ehtolauseessa tai automaattisessa toiminnossa, kun haluat hallita sitä, miten työnkulkureititykset on pyydetty tietyillä lomatyypeillä.

## <a name="see-also"></a>Lisätietoja

- [Lomien ja poissaolojen yhteenveto](hr-leave-and-absence-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
