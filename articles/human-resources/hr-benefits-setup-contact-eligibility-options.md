---
title: Henkilökohtaisten yhteyshenkilöiden oikeutusasetusten määrittäminen
description: Tässä artikkelissa käsitellään henkilökohtaisten yhteyshenkilöiden kelpoisuusasetusten määrittämistä Microsoft Dynamics 365 Human Resourcesissa.
author: twheeloc
ms.date: 11/22/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e3e393002901f31c035a54bd8036ed20ecdf9e00
ms.sourcegitcommit: 81bb8e51951395be3f18f45212e47e6c41656f6a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/23/2022
ms.locfileid: "9803881"
---
# <a name="configure-personal-contact-eligibility-options"></a>Henkilökohtaisten yhteyshenkilöiden oikeutusasetusten määrittäminen


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tässä artikkelissa kerrotaan, miten voit määrittää henkilökohtaisten yhteyshenkilöiden tyyppejä käytettäviksi Microsoft Dynamics 365 Human Resourcesissa. Henkilökohtaiset yhteyshenkilöt ovat henkilöitä, jotka kuuluvat palvelupakettiesi piiriin (riippuvaiset) tai jotka hyötyvät palvelupaketeistasi (edunsaajat). Riippuvaiset ovat tyypillisesti puolisoita tai lapsia. Edunsaajat voivat olla puolisoita, lapsia, säätiöitä tai vanhempia.

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
   | **Ikä** |Määrittää kelvollisen henkilökohtaisen yhteyshenkilön yläikärajan etuussuunnitelmassa. Tämä kenttä on käytettävissä vain, jos valitset suhteen. Tätä ikää verrataan henkilökohtaisen yhteyshenkilön laskettuun ikään. Laskettu ikä on: (kattavuuspäivämäärä – henkilökohtaisen yhteyshenkilön syntymäaika / 365). Tämä luku on aina kokonaisluku.
Yhteyshenkilöiden **Ylitys - huollettava** -oikeutusvaihtoehdon tapauksessa tässä kentässä oleva ikä on vähimmäisikä. Esimerkki: jos iäksi on määritetty 18 vaihtoehdossa **Ylitys - huollettava**, huollettavat, jotka on merkitty yli-ikäisiksi huollettaviksi ja jotka ovat 18-vuotiaita tai vanhempia, kuuluvat kelpoisuusasetuksen piiriin.  |

4. Valitse **Tallenna**. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
