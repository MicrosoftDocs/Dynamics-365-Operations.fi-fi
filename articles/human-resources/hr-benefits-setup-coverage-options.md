---
title: Kattavuusasetusten luominen
description: Microsoft Dynamics 365 Human Resourcesin kattavuusasetukset ovat osallistujan valitsemia kattavuustasoja etuussuunnitelmassa tai -ohjelmassa, kuten Vain työntekijä terveydenhoitosuunnitelman osalta tai 2 x palkka henkivakuutussuunnitelman osalta.
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
ms.openlocfilehash: 0af2b6ae0853b4c7f64c4d4f04299c87089d622b
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092703"
---
# <a name="create-coverage-options"></a>Kattavuusasetusten luominen

[!include [banner](includes/preview-feature.md)]

Microsoft Dynamics 365 Human Resourcesin kattavuusasetukset ovat osallistujan valitsemia kattavuustasoja etuussuunnitelmassa tai -ohjelmassa, kuten Vain työntekijä terveydenhoitosuunnitelman osalta tai 2 x palkka henkivakuutussuunnitelman osalta. Kun etujen kattavuusasetukset on määritetty, niitä voidaan käyttää uudelleen, ja voit kohdistaa astuksen yhdelle tai useammalle suunnitelmalle.

Kun kattavuus setukset on määritetty, liitä kattavuusasetukset etuussuunnitelmatyyppiin. Tämän jälkeen suunnitelmatyyppi yhdistetään etuussuunnitelmaan tai -ohjelmaan. Suunnitelmatyyppiin yhdistetyt kattavuusasetukset ovat käytettävissä kaikissa suunnitelmissa, jotka luodaan kyseisellä suunnitelmatyypillä. 

1. Valitse **Etujen hallinta** -työtilassa **Asetukset**-kohdasta **Kattavuusasetukset**.

2. Valitse **Uusi**.

3. Määritä seuraavien kenttien arvot.

   | Kenttä | Kuvaus |
   | --- | --- |
   | **Kattavuusasetus** | Yksilöllinen kattavuusasetuksen nimi. |
   | **Kuvaus** | Kattavuusasetuksen kuvaus. |
   | **Kattavuuskoodi** | Kattavuuskoodit määrittävät kullekin kelvolliselle katetulle henkilötyypille enimmäis- ja vähimmäismäärät. Kattavuuskoodi ilmaisee, kenet katetaan tai suunnitelmatyypille sallitun kattavuusmäärän. Voit ilmaista kattavuusmäärän dollarisummana tai prosenttiosuutenta. Esimerkki:</br></br>- **Työnt+1** – Täyttääkseen kelpoisuusvaatimuksen työntekijällä on oltava valittuna yksi huollettava (tämän määrän ylittävät huollettavat eivät enää kuulu suunnitelman piitiin).</br></br>- **Työnt+perhe** – Täyttääkseen kelpoisuusvaatimukset työntekijällä on oltava valittuna vähintään kaksi huollettavaa. |
   | **Enimmäismäärä** | Huollettavien enimmäismäärä. |
   | **Tila** | Kattavuusasetuksen tila. Jos kattavuusasetuksen tilaksi asetetaan Passiivinen, kyseistä kattavuusasetusta ei voida valita suunnitelmatyypeissä. |
   | **Prosenttia** | Prosenttiosuus. Tämä kenttä on aktiivinen vain, jos kattavuuskoodikentässä on valittu % x palkka. |
   | **Jakaja** | Laskennassa käytettävä jalkaja, kun valitaan kattavuuskoodi % x palkka. |
   | **Vähimmäisprosenttiosuus** | Vähimmäisprosenttiosuus, kun valitset Prosenttiosuus-kattavuuskoodin. |
   | **Enimmäisprosenttiosuus** | Enimmäisprosenttiosuus, kun valitset Prosenttiosuus-kattavuuskoodin. |

4. Liitä kohtaan **Henkilökohtaisen yhteyshenkilön kelpoisuusvaihtoehdot** asianmukainen henkilökohtaisen yhteyshenkilön kelpoisuusasetus kullekin kattavuusasetukselle.

5. Määritä **Itsepalvelu**-kohdassa seuraavien kenttien arvot:

   | Kenttä | Kuvaus |
   | --- | --- |
   | **Salli työntekijän korvaussumma** | Määrittää, saavatko työntekijät muokata etujen itsepalvelun maksumäärää, kun he valitsevat etuja. Jos valitset tämän valintaruudun, järjestelmä laskee etuussuunnitelman parametrit sen maksumäärän perusteella, jonka työntekijä syöttää etujen itsepalveluun. |
   | **Salli työntekijän kattavuussumma** | Määrittää, saavatko työntekijät muokata etujen itsepalvelun kattavuusmäärää, kun he valitsevat etuja. Jos valitset tämän valintaruudun, järjestelmä laskee etuussuunnitelman parametrit sen kattavuusmäärän perusteella, jonka työntekijä syöttää työntekijän itsepalveluun. |

6. Valitse **Tallenna**. 
