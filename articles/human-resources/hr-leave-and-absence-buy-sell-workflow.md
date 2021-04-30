---
title: Loman rahaksi tai lomapalkan vapaaksi vaihtamisen työnkulkujen luominen
description: Luo loman rahaksi tai lomapalkan vapaaksi vaihtamisen työnkulku, jonka avulla voit hallita loman rahaksi tai lomapalkan vapaaksi vaihtamista johdonmukaisesti Dynamics 365 Human Resourcesissa.
author: andreabichsel
ms.date: 08/20/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 15cedc16fbdbb5d25daa262f094a56bb8fe2f5cc
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/13/2021
ms.locfileid: "5892702"
---
# <a name="create-a-buy-and-sell-leave-request-workflow"></a>Loman rahaksi tai lomapalkan vapaaksi vaihtamisen työnkulkujen luominen

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Voit luoda Dynamics 365 Human Resourcesissa työnkulun, jolla voi hallita loman rahaksi tai lomapalkan vapaaksi vaihtamispyyntöjä johdonmukaisesti. **Loman rahaksi tai lomapalkan vapaaksi vaihtaminen** -työnkulun avulla voi tehdä seuraavat:

- Määrittää tehtäviä
- Määrittää, kenen tehtävät on suoritettava
- Määrittää, ketkä voivat hyväksyä tai hylätä pyyntöjä

## <a name="create-a-buy-and-sell-leave-request-workflow"></a>Loman rahaksi tai lomapalkan vapaaksi vaihtamisen työnkulkujen luominen

1. Valitse **Lomat ja poissaolot** -sivulla **Linkit**-välilehti.

2. Valitse **Määritys**-kohdasta **Henkilöstöhallinnon työnkulut**.

3. Valitse **Uusi** ja valitse sitten **Loman rahaksi tai lomapalkan vapaaksi vaihtamispyyntö**. 

4. Kun **Avaa tämä tiedosto?** -sanomaruutu tulee näkyviin, valitse **Avaa** ja kirjaudu sisään yrityksen tunnistetiedoilla.

5. Työnkulkueditorin avulla voit luoda työnkulun lomapyyntöihin. Lisätietoja työnkulkujen käyttämisestä on kohdassa [Luo työnkulkujen yhteenveto](../fin-ops-core/fin-ops/organization-administration/create-workflow.md?toc=%2fdynamics365%2fcommerce%2ftoc.json.)

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

- Käytä automaattisia **Henkilöstöhallinnon toimittama**- ja **Esimiehen lähettämä** -toimintoja, jotka hyväksyvät automaattisesti Loman rahaksi tai lomapalkan vapaaksi vaihtamispyynnöt, jotka nämä roolit lähettävät työntekijöiden puolesta. Lisätietoja automaattisista toiminnoista on kohdassa [Määritä hyväksyntäprosessit työnkulussa](../fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow.md).

- Käytä **lomatyyppiä** ehtolauseessa tai automaattisessa toiminnossa, kun haluat hallita sitä, miten työnkulkureititykset on pyydetty tietyillä lomatyypeillä.

## <a name="see-also"></a>Lisätietoja

[Lomien ja poissaolojen yhteenveto](hr-leave-and-absence-overview.md)<br>
[Käytäntöjen hallinta loman vaihtamisessa rahaksi ja lomapalkan vaihtamisessa vapaaksi](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]