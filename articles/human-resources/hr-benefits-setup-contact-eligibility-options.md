---
title: Henkilökohtaisen yhteyshenkilön kelpoisuusasetusten määrittäminen
description: Määritä henkilökohtaisten yhteyshenkilöiden kelpoisuusasetuksia Microsoft Dynamics 365 Human Resourcesissa. Henkilökohtaiset yhteyshenkilöt voivat olla edunsaajia tai huollettavia.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a50c5e54d224a2f8607284eb105381ffb6ef7ad9
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008905"
---
# <a name="configure-personal-contact-eligibility-options"></a>Henkilökohtaisen yhteyshenkilön kelpoisuusasetusten määrittäminen

[!include [banner](includes/preview-feature.md)]

Tässä artikkelissa kerrotaan, miten voit määrittää henkilökohtaisten yhteyshenkilöiden tyyppejä käytettäväksi Microsoft Dynamics 365 Human Resourcesissa. Henkilökohtaiset yhteyshenkilöt voivat olla edunsaajia tai huollettavia. 

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
