---
title: Työaikakalenterin luominen
description: Määritä työaikakalenteri, vapaapäivät ja muut kuin työajat Dynamics 365 Human Resources -järjestelmässä.
author: andreabichsel
manager: tfehr
ms.date: 04/01/2020
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
ms.openlocfilehash: ecabac54134629074ac01944963a037c2cdc63c9
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467166"
---
# <a name="create-a-working-time-calendar"></a>Työaikakalenterin luominen

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dynamics 365 Human Resourcesin työaikakalenterissa näkyvät työntekijöiden työpäivät ja -tunnit organisaatiossa. Kun työntekijä lähettää lomapyynnön, hänen ei tarvitse huolehtia juhlapäivistä ja sulkemisista.

Jos haluat tehostaa lomapyyntöjä, määritä nämä nimikkeet organisaatiollesi:

- Työaikakalenteri
- Lomat ja sulkemiset
- Muu kuin työaika

Voit lisätä kaksi viimeistä nimikettä työaikakalenteria määrittäessäsi. Voit myös määrittää tai päivittää ne erikseen.

## <a name="set-up-a-working-time-calendar"></a>Määritä työaikakalenteri

Määritä vähintään yksi työaikakalenteri, joka näyttää päivät ja työtunnit. Jos sinulla on sijainteja useissa maissa ja tietyillä alueilla, haluat ehkä määrittää kullekin alueelle työaikakalenterin.

1. Valitse **Organisaation hallinto** -sivulta **Kalenterit**.

2. Valitse **Uusi** ja kirjoita kalenterisi nimi ja kuvaus.

3. Valitse **Luonnin asetukset**-kohdasta organisaation työpäivät ja määritä työajat. 
   - Jos haluat lisätä loman tai sulkemisen, valitse **Lomien ja sulkemisten** vieressä oleva **Lisää**-painike.
   - Jos haluat lisätä muun kuin työajan, kuten lounaan tai tauon, valitse **Lisää** **Muu kuin työaika** -kohdassa ja kirjoita nimi ja aikaväli.

4. Valitse **Päivät**-kohdassa **Luo** päivien luomiseksi kalenteriin. Kirjoita kalenterin päivämääräväli ja valitse **Luo päiviä**.

5. Jos haluat lisätä työaikatauluja, valitse **Työaikataulu**-kohdasta **Lisää** ja kirjoita sitten kunkin työaikataulun ajat.

## <a name="configure-holidays-and-closures"></a>Määritä lomat ja sulkemiset

Voit lisätä tai muuttaa lomia ja sulkemisia erillään työaikakalenterista.

1. Valitse **Organisaation hallinto** -sivulta **Lomat ja sulkemiset**.

2. Valitse **Uusi** ja kirjoita loman tai sulkemisen nimi ja päivämäärä.

## <a name="configure-non-work-time"></a>Määritä muu kuin työaika

Voit lisätä tai muuttaa muita kuin työaikoja erillään työaikakalenterista.

1. Valitse **Organisaation hallinto** -sivulta **Muu kuin työaika**.

2. Valitse **Uusi** ja kirjoita vapaa-ajan nimi ja aika-alue.

Jos olet ottanut loma- ja poissaolopäivän korjausten esikatselutoiminnon käyttöön, henkilöstöhallinto käyttää loma- ja sulkemispäiviä määrittääkseen päivien määrän, jota mukautetaan kalenteriin ilmoitettujen työntekijöiden osalta.

## <a name="see-also"></a>Lisätietoja

- [Lomien ja poissaolojen yhteenveto](hr-leave-and-absence-overview.md)
- [Määritä loman ja poissaolon tyypit](hr-leave-and-absence-types.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]