---
title: Loman rahaksi tai lomapalkan vapaaksi vaihtamisen työnkulkujen luominen
description: Luo loman rahaksi tai lomapalkan vapaaksi vaihtamisen työnkulku, jonka avulla voit hallita loman rahaksi tai lomapalkan vapaaksi vaihtamista johdonmukaisesti Dynamics 365 Human Resourcesissa.
author: andreabichsel
manager: AnnBe
ms.date: 08/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-08-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d490e0c36ea0e854c5d7afc5b3bf75f6b65e542c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4418383"
---
# <a name="create-a-buy-and-sell-leave-request-workflow"></a>Loman rahaksi tai lomapalkan vapaaksi vaihtamisen työnkulkujen luominen

Voit luoda Dynamics 365 Human Resourcesissa työnkulun, jolla voi hallita loman rahaksi tai lomapalkan vapaaksi vaihtamispyyntöjä johdonmukaisesti. **Loman rahaksi tai lomapalkan vapaaksi vaihtaminen** -työnkulun avulla voi tehdä seuraavat:

- Määrittää tehtäviä
- Määrittää, kenen tehtävät on suoritettava
- Määrittää, ketkä voivat hyväksyä tai hylätä pyyntöjä

## <a name="create-a-buy-and-sell-leave-request-workflow"></a>Loman rahaksi tai lomapalkan vapaaksi vaihtamisen työnkulkujen luominen

1. Valitse **Lomat ja poissaolot** -sivulla **Linkit**-välilehti.

2. Valitse **Määritys**-kohdasta **Henkilöstöhallinnon työnkulut**.

3. Valitse **Uusi** ja valitse sitten **Loman rahaksi tai lomapalkan vapaaksi vaihtamispyyntö**. 

4. Kun **Avaa tämä tiedosto?** -sanomaruutu tulee näkyviin, valitse **Avaa** ja kirjaudu sisään yrityksen tunnistetiedoilla.

5. Työnkulkueditorin avulla voit luoda työnkulun lomapyyntöihin. Lisätietoja työnkulkujen käyttämisestä on kohdassa [Luo työnkulkujen yhteenveto](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/create-workflow?toc=/dynamics365/commerce/toc.json.)

## <a name="leave-and-absence-request-workflow-data-elements"></a>Loma- tai poissaolopyyntötyönkulun tietoelementit

Seuraavien tietoelementtien avulla voit luoda ehdollisia tai automaattisia hyväksyntöjä Loman rahaksi tai lomapalkan vapaaksi vaihtamispyyntöjen työnkulkuja:

- **summa**
- **Lomien osto- ja myyntikäytäntö**
- **Yritys**
- **Luonut**
- **Luonnin päivämäärä ja aika**
- **Päättymispäivämäärä**
- **Lomatyyppi**
- **Muokannut**
- **Muokkauksen päivämäärä ja aika**
- **Pyynnön tunnus**
- **Aloituspäivä**
- **Tila** 
- **Lähetyspäivämäärä**
- **Lähettäjä**
- **Henkilöstöhallinnon lähettämä**
- **Esimiehen lähettämä**
- **Lähetetty puolesta**
- **Työntekijä**

## <a name="workflow-examples"></a>Työnkulkuesimerkit

Nämä esimerkit osoittavat, miten voit luoda erityyppisiä työnkulkuehtoja käyttämällä näitä tietoelementtejä:

- Käytä automaattisia **Henkilöstöhallinnon toimittama**- ja **Esimiehen lähettämä** -toimintoja, jotka hyväksyvät automaattisesti Loman rahaksi tai lomapalkan vapaaksi vaihtamispyynnöt, jotka nämä roolit lähettävät työntekijöiden puolesta. Lisätietoja automaattisista toiminnoista on kohdassa [Määritä hyväksyntäprosessit työnkulussa](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow).

- Käytä **lomatyyppiä** ehtolauseessa tai automaattisessa toiminnossa, kun haluat hallita sitä, miten työnkulkureititykset on pyydetty tietyillä lomatyypeillä.

## <a name="see-also"></a>Lisätietoja

[Lomien ja poissaolojen yhteenveto](hr-leave-and-absence-overview.md)<br>
[Käytäntöjen hallinta loman vaihtamisessa rahaksi ja lomapalkan vaihtamisessa vapaaksi](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]