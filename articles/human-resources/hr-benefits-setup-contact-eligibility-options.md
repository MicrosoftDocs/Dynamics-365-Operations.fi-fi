---
title: Henkilökohtaisen yhteyshenkilön kelpoisuusasetusten määrittäminen
description: Määritä henkilökohtaisten yhteyshenkilöiden kelpoisuusasetuksia Microsoft Dynamics 365 Human Resourcesissa. Henkilökohtaiset yhteyshenkilöt voivat olla edunsaajia tai huollettavia.
author: andreabichsel
ms.date: 06/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 071523e2a1e9de6f0ed2b77e4ad6802efb0073f7
ms.sourcegitcommit: 08797bc43e93ea05711c5a70dd7cdb82cada667a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/13/2021
ms.locfileid: "6558246"
---
# <a name="configure-personal-contact-eligibility-options"></a>Henkilökohtaisten yhteyshenkilöiden oikeutusasetusten määrittäminen

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tässä aiheessa kerrotaan, miten voit määrittää henkilökohtaisten yhteyshenkilöiden tyyppejä käytettäviksi Microsoft Dynamics 365 Human Resourcesissa. Henkilökohtaiset yhteyshenkilöt ovat henkilöitä, jotka kuuluvat palvelupakettiesi piiriin (riippuvaiset) tai jotka hyötyvät palvelupaketeistasi (edunsaajat). Riippuvaiset ovat tyypillisesti puolisoita tai lapsia. Edunsaajat voivat olla puolisoita, lapsia, säätiöitä tai vanhempia.

1. Valitse **Etujen hallinta** -työtilassa **Asetukset**-kohdasta **Henkilökohtaisen yhteyshenkilön kelpoisuusasetukset**.

2. Valitse **Uusi**.

3. Määritä seuraavien kenttien arvot.

   | Kenttä | Kuvaus |
   | --- | --- |
   | **Kelpoisuusvaihtoehto** | Yksilöllinen kelpoisuusasetuksen nimi tai koodi kelpoisuusasetuksen tunnistamista varten. |
   | **Kuvaus** | Kelpoisuusasetuksen lyhyt kuvaus. |
   | **Yhteyshenkilön kelpoisuuskoodi** | Järjestelmäkoodi, joka kuvaa parhaiten henkilökohtaista kelpoisuusvaihtoehtoa. Voit valita jonkin seuraavista: <ul><li>Suhde</li><li>Opiskelija</li><li>Ylitys - huollettava</li><li>Yli-ikäinen vammainen huollettava</li></ul> |
   | **Tila** | Kelpoisuusasetuksen tila. Jos kelpoisuusasetuksen tilaksi on määritetty passiivinen, et voi valita kyseistä henkilökohtaisen yhteyshenkilön kelpoisuusasetusta henkilökohtaisille yhteyshenkilöille. |
   | **Suhde** | Määrittää suhteen henkilökohtaisen yhteyshenkilön ja työntekijän välillä. Tämä kenttä on käytettävissä vain, jos yhteyshenkilön kelpoisuuskoodiksi on määritetty Suhde. |
   | **Ikä** | Kelvollisen henkilökohtaisen yhteyshenkilön yläikäraja etuussuunnitelmassa. Tämä kenttä on käytettävissä vain, jos valitset suhteen. Tätä ikää verrataan henkilökohtaisen yhteyshenkilön laskettuun ikään. Laskettu ikä on: (kattavuuspäivämäärä – henkilökohtaisen yhteyshenkilön syntymäaika / 365). Tämä luku on aina kokonaisluku. |

4. Valitse **Tallenna**. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
