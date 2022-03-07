---
title: Käytäntöjen hallinta loman vaihtamisessa rahaksi ja lomapalkan vaihtamisessa vapaaksi
description: Voit antaa työntekijöille oikeuden ostaa ja myydä lomaa Dynamics 365 Human Resourcesissa.
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeaveBuySellPolicy, LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-06-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1fe7ce7eafdec175e3395a6ac37b33cb2bb8dbda
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/31/2022
ms.locfileid: "8066672"
---
# <a name="manage-buy-and-sell-leave-policies"></a>Käytäntöjen hallinta loman vaihtamisessa rahaksi ja lomapalkan vaihtamisessa vapaaksi


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Voit antaa työntekijöille oikeuden ostaa ja myydä lomia luomalla lomien osto- ja myyntikäytännön. Voit määrittää nämä käytännöt käyttämään hyväksyntätyökulkua, määrittää enimmäismäärät ja -hinnat sekä määrittää osto- ja myyntihinnat. 

## <a name="enable-employees-to-buy-and-sell-leave"></a>Anna työntekijöille mahdollisuus ostaa ja myydä lomaa

1. Valitse **Loma- ja poissaoloparametrit** -sivun **Työntekijät voivat ostaa lomaa**- ja **Salli työntekijöiden myydä lomaa** -vaihtoehdoissa **Kyllä**.

## <a name="create-a-buy-and-sell-leave-policy"></a>Loman rahaksi tai lomapalkan vapaaksi vaihtamiskäytäntöjen luominen

1. Valitse **Lomat ja poissaolot** -sivulla **Linkit**-välilehti. 

2. Valitse **Loman vaihtaminen rahaksi ja lomapalkan vaihtaminen vapaaksi -käytäntö**.

3. Valitse **Uusi**.

4. Kirjoita **Osta ja myy lomaa** -käytännön mukaisen käytännön **Nimi** ja **Kuvaus**. 

5. Valitse **Käytäntötyyppi**. 

   Käytettävissä olevat käytäntötyypit ovat **Määrä** ja **Tuntia viikossa**. Valitse **Määrä**, jos haluat syöttää **Kiinteän määrän** maksimi määriin, joita työntekijät voivat ostaa ja myydä. Jos valitset **Tunteja viikossa** -käytännön, enimmäismäärä määritetään käyttämällä työntekijän määritettyä työaikaa työaikakalenterissa. 

6. Valitse käytännön **Alkamispäivämäärä** ja **Päättymispäivämäärä**. Osto- tai myyntipyynnöt ovat käytettävissä vain tämän aikajakson aikana. 

7. Valitse käytännön **Työnkulkutunnus**. Kaikki osto-ja myyntipyynnöt arvioidaan ja hyväksytään tämän työnkulun avulla. 

8. Valitse **Ostokäytäntö**-kohdasta **Koko ajan vastaavuus** (FTE), jos haluat määrittää enimmäisarvon työntekijän toimessa määritetyn FTE-arvon perusteella. Jos käytäntötyyppi on **Määrä**, määritä **Enimmäismäärä**. 

9. Valitse **Lisää**, kun haluat lisätä lomatyypit työntekijöille, jotka ostavat lomaa. Voit lisätä käytäntöön useita lomatyyppejä. 

10. Syötä lomatyypin **palvelukuukaudet**, jotta eri kuukaudet voivat määrittää työntekijän ostaman enimmäishinnan. 

11. Kirjoita lomatyypin **enimmäismäärä**. 

12. Kirjoita **taksa**, jolla työntekijä ostaa loman. 

13. Vaihtoehtoisesti voit antaa **ansaintakoodin**, jota käytetään loman ostamiseen. 

14. Voit myös määrittää, käytetäänkö FTE-tyyppiä, kun haluat määrittää lomatyypin enimmäismäärän. 

15. Luo ostokäytäntö **Ostokäytäntö**-kohdan vaiheiden 8–14 mukaisesti. 

## <a name="add-the-buy-and-sell-leave-policy-to-a-leave-and-absence-plan"></a>Loman osto- ja myyntikäytännön lisääminen loma- ja poissaolosuunnitelmaan

1. Valitse **loma ja poissaolo** -sivulla loma- ja poissaolosuunnitelma.

2. Valitse **Säännöt**-kohdasta **Loman vaihtaminen rahaksi ja lomapalkan vaihtaminen vapaaksi** -käytäntö.

## <a name="see-also"></a>Lisätietoja

[Lomien ja poissaolojen yhteenveto](hr-leave-and-absence-overview.md)</br>
[Loma- ja poissaolotyyppien määrittäminen](hr-leave-and-absence-types.md)</br>
[Jaksota loma- ja poissaolosuunnitelmat](hr-leave-and-absence-accrue.md)</br>
[Osta ja myy lomaa](hr-employee-self-service-buy-sell-leave.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
