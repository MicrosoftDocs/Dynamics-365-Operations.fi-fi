---
title: Luo lomapyyntötyönkulku
description: Luo loma- ja poissaolopyyntöjen työnkulku, jonka avulla voit hallita lomapyyntöjä johdonmukaisesti Dynamics 365 Human Resources -ohjelmassa.
author: andreabichsel
ms.date: 05/08/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5580b4b07b2d335ad9444a064c726bc4aca1db6a
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/18/2021
ms.locfileid: "6056537"
---
# <a name="create-a-leave-request-workflow"></a>Luo lomapyyntötyönkulku

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