---
title: Jaksota loma- ja poissaolosuunnitelmat
description: Voit jaksottaa lomaa ja poissaoloa Dynamics 365 Human Resourcesissa useille työntekijöille tai yksittäisille henkilöille.
author: andreabichsel
manager: AnnBe
ms.date: 06/01/2020
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
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f045cb7ab9f5e7aa4259f29e1b026f110425c236
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/04/2020
ms.locfileid: "3429056"
---
# <a name="accrue-leave-and-absence-plans"></a>Jaksota loma- ja poissaolosuunnitelmat

Voit jaksottaa lomaa ja poissaoloa Dynamics 365 Human Resourcesissa useille työntekijöille tai yksittäisille henkilöille.

## <a name="accrue-leave-and-absence-for-multiple-employees"></a>Useiden työntekijöiden kertyneet lomat ja poissaolot

1. Valitse **Lomat ja poissaolot** -sivulla **Linkit**-välilehti.

2. Valitse **Hallitse lomia** -kohdassa **Jaksota loma- ja poissaolosuunnitelmat**.

3. **Kertyneiden lomien ja poissaolojen suunnitelmat** -valintaikkuna tulee näyttöön. Valitse **Kertymä**-kohdasta joko **Kuluvan päivän päivämäärä** tai valitse **Mukautettu päivämäärä** ja syötä mukautettu päivämäärä.

4. Jos haluat suorittaa jaksotusprosessin taustalla, valitse **Suorita taustalla** ja tee seuraavat tehtävät:

   1. Määritä jaksotusprosessin tiedot.

   2. Jos haluat määrittää toistuvan työn, valitse **Toistuminen**, kirjoita toistuvuustiedot ja valitse **OK**.

   3. Jos haluat määrittää työpaikkahälytyksen, valitse **Hälytykset**, valitse vastaanotettavat hälytykset ja valitse sitten **OK**.

   4. Valitse **OK**. Jaksotusprosessi suoritetaan määrittämilläsi parametreilla.

## <a name="accrue-leave-and-absence-for-an-employee"></a>Työntekijän kertyneet lomat ja poissaolot

1. Valitse työntekijän tietueesta **Loma**.

2. Valitse **Jaksota lomat ja poissaolot**.

3. **Kertyneiden lomien ja poissaolojen suunnitelmat** -valintaikkuna tulee näyttöön. Valitse **Kertymä**-kohdasta joko **Kuluvan päivän päivämäärä** tai valitse **Mukautettu päivämäärä** ja syötä mukautettu päivämäärä.

4. Jos haluat suorittaa jaksotusprosessin taustalla, valitse **Suorita taustalla** ja tee seuraavat tehtävät:

   1. Määritä jaksotusprosessin tiedot.

   2. Jos haluat määrittää toistuvan työn, valitse **Toistuminen**, kirjoita toistuvuustiedot ja valitse **OK**.

   3. Jos haluat määrittää työpaikkahälytyksen, valitse **Hälytykset**, valitse vastaanotettavat hälytykset ja valitse sitten **OK**.

   4. Valitse **OK**. Jaksotusprosessi suoritetaan määrittämilläsi parametreilla.

## <a name="delete-leave-and-absence-accruals-for-multiple-employees"></a>Poista useiden työntekijöiden kertyneet lomat ja poissaolot

Poista tietyn suunnitelman ja päivämäärävälin jaksotustiedot. Jaksotuspäivämäärät on päivättävä tälle päivälle tai tulevaisuuteen.

1. Valitse **Lomat ja poissaolot** -sivulla **Linkit**-välilehti.

2. Valitse **Hallitse lomia** -kohdassa **Poista loma- ja poissaolosuunnitelmien kertymät**.

3. Valitse **Poista loma- ja poissaolosuunnitelman kertymät** -valintaikkunasta **Lomasuunnitelma**. 

4. Valitse tarvittaessa **Poista saldo-oikaisut**.

5. Kirjoita tai valitse **Loman jaksotuspäivämäärä**. Tämän päivän on oltava joko tänään tai tulevaisuudessa. 

6. Valitse **OK**. Jaksotusprosessi poistaa kertymät määrittämilläsi parametreilla. 

## <a name="delete-leave-and-absence-accruals-for-a-single-employee"></a>Poista yhden työntekijän kertyneet lomat ja poissaolot

1. Valitse työntekijän tietueesta **Loma**.

2. Valitse **Poista loma- ja poissaolosuunnitelman jaksotukset**.

3. Valitse **Poista loma- ja poissaolosuunnitelman kertymät** -valintaikkunasta **Lomasuunnitelma**. 

4. Valitse tarvittaessa **Poista saldo-oikaisut**.

5. Kirjoita tai valitse **Loman jaksotuspäivämäärä**. Tämän päivän on oltava joko tänään tai tulevaisuudessa. 

6. Valitse **OK**. Jaksotusprosessi poistaa kertymät määrittämilläsi parametreilla. 

## <a name="review-leave-accrual-and-deletion-processes"></a>Loman kertymä- ja poistoprosessien tarkasteleminen

**Lomakertymän valvonta** näyttää aina, kun suoritat tai poistat yhden tai kaikkien työntekijöiden kertymän. Myös toimenpiteen päiväys ja suorittanut henkilö näytetään.

1. Valitse **Lomat ja poissaolot** -sivulla **Linkit**-välilehti.

2. Valitse **Hallitse lomia** -kohdassa **Poista lomakertymien valvonta**.

## <a name="configure-preview-features"></a>Esikatseluominaisuuksien määrittäminen

[!include [banner](includes/preview-feature-leave-absence.md)]

Jos olet ottanut käyttöön loman ja poissaolon esikatseluominaisuudet, sinun on määritettävä myös niiden asetukset.

### <a name="accrue-leave-per-company-or-per-leave-plan"></a>Loman jaksottaminen yrityksen tai lomasuunnitelman mukaan

Kun loma- ja poissaolosuunnitelmat kertyvät, voit määrittää, että kaikki yritykset jaksotetaan. Jos valitset kaikki yritykset, et voi valita yksittäistä lomasuunnitelmaa. Jos valitset, että kaikkia yrityksiä ei kerrytetä, voit jaksottaa tietyn lomasuunnitelman. 

Nämä vaihtoehdot ovat käytettävissä, kun ne kertyvät kaikille työntekijöille tai yksittäisille työntekijöille. 

## <a name="see-also"></a>Lisätietoja

[Lomien ja poissaolojen yhteenveto](hr-leave-and-absence-overview.md)</br>
[Loma- ja poissaolosuunnitelman luominen](hr-leave-and-absence-plans.md)
