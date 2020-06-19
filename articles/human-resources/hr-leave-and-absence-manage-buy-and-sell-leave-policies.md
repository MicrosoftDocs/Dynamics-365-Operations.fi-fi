---
title: Käytäntöjen hallinta loman vaihtamisessa rahaksi ja lomapalkan vaihtamisessa vapaaksi
description: Voit antaa työntekijöille oikeuden ostaa ja myydä lomaa Dynamics 365 Human Resourcesissa.
author: andreabichsel
manager: AnnBe
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeaveBuySellPolicy, LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-06-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 859445f2b6e980b5960e512e69129f6a8fc6df2b
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/04/2020
ms.locfileid: "3429010"
---
# <a name="manage-buy-and-sell-leave-policies"></a>Käytäntöjen hallinta loman vaihtamisessa rahaksi ja lomapalkan vaihtamisessa vapaaksi

[!include [banner](includes/preview-feature.md)]

Voit antaa työntekijöille oikeuden ostaa lomaa luomalla ostolomakäytännön.  

## <a name="enable-employees-to-buy-and-sell-leave"></a>Anna työntekijöille mahdollisuus ostaa ja myydä lomaa

1. Valitse **Loma- ja poissaoloparametrit** -sivulla **Kyllä**, jotta **Työntekijät voivat ostaa loman**. 

## <a name="create-a-buy-leave-policy"></a>Luo loman ostokäytäntö

1. Valitse **Lomat ja poissaolot** -sivulla **Linkit**-välilehti. 

2. Valitse **Loman vaihtaminen rahaksi ja lomapalkan vaihtaminen vapaaksi -käytäntö**.

3. Valitse **Uusi**.

4. Kirjoita **Osta ja myy lomaa** -käytännön mukaisen käytännön **Nimi** ja **Kuvaus**. 

5. Valitse **Käytäntötyyppi**. 

   Käytettävissä olevat käytäntötyypit ovat **Määrä** ja **Tuntia viikossa**. Valitse **Määrä**, jos haluat syöttää **Kiinteän määrän** maksimi määriin, joita työntekijät voivat ostaa ja myydä. Jos valitset **Tunteja viikossa** -käytännön, enimmäismäärä määritetään käyttämällä työntekijän määritettyä työaikaa työaikakalenterissa. 

6. Valitse käytännön **Alkamispäivämäärä** ja **Päättymispäivämäärä**. Osto- tai myyntipyynnöt ovat käytettävissä vain tämän aikajakson aikana. 

7. Valitse **Ostokäytäntö**-kohdasta **Koko ajan vastaavuus** (FTE), jos haluat määrittää enimmäisarvon työntekijän toimessa määritetyn FTE-arvon perusteella. Jos käytäntötyyppi on **Määrä**, määritä **Enimmäismäärä**. 

8. Valitse **Lisää**, kun haluat lisätä lomatyypit työntekijöille, jotka ostavat lomaa. Voit lisätä käytäntöön useita lomatyyppejä. 

9. Syötä lomatyypin **palvelukuukaudet**, jotta eri kuukaudet voivat määrittää työntekijän ostaman enimmäishinnan. 

10. Kirjoita lomatyypin **enimmäismäärä**. 

11. Kirjoita **taksa**, jolla työntekijä ostaa loman. 

12. Vaihtoehtoisesti voit antaa **ansaintakoodin**, jota käytetään loman ostamiseen. 

13. Voit myös määrittää, käytetäänkö FTE-tyyppiä, kun haluat määrittää lomatyypin enimmäismäärän. 

## <a name="add-the-buy-and-sell-leave-policy-to-a-leave-and-absence-plan"></a>Loman osto- ja myyntikäytännön lisääminen loma- ja poissaolosuunnitelmaan

1. Valitse **loma ja poissaolo** -sivulla loma- ja poissaolosuunnitelma.

2. Valitse **Säännöt**-kohdasta **Loman vaihtaminen rahaksi ja lomapalkan vaihtaminen vapaaksi** -käytäntö.

## <a name="see-also"></a>Lisätietoja

[Lomien ja poissaolojen yhteenveto](hr-leave-and-absence-overview.md)</br>
[Loma- ja poissaolotyyppien määrittäminen](hr-leave-and-absence-types.md)</br>
[Jaksota loma- ja poissaolosuunnitelmat](hr-leave-and-absence-accrue.md)</br>
[Osta ja myy lomaa](hr-employee-self-service-buy-sell-leave.md)

