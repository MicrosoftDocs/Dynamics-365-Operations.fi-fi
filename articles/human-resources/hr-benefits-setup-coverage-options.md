---
title: Kattavuusasetusten luominen
description: Microsoft Dynamics 365 Human Resources -ohjelman kattavuustasot osallistujan valitsemiselle etuussuunnitelmassa tai -ohjelmassa.
author: andreabichsel
ms.date: 04/06/2020
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
ms.openlocfilehash: d9f67a97ec57bade840e1035c6011b94427a77c4
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/18/2021
ms.locfileid: "6055577"
---
# <a name="create-coverage-options"></a>Kattavuusasetusten luominen

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Microsoft Dynamics 365 Human Resources -ohjelman kattavuustasot osallistujan valitsemiselle etuussuunnitelmassa tai -ohjelmassa. Kattavuusvaihtoehdot voivat olla esimerkiksi **Vain työntekijä** lääketieteellisessä suunnitelmassa tai **2 x palkka** henkivakuutussuunnitelmaa varten. Voit käyttää kattavuusasetuksia uudelleen hyödyksi, kun ne on määritetty. Voit liittää vaihtoehdon yhteen tai useaan suunnitelmaan.

Kun kattavuusasetukset on määritetty, liitä kattavuusasetukset etuussuunnitelmatyyppiin. Tämän jälkeen suunnitelmatyyppi yhdistetään etuussuunnitelmaan tai -ohjelmaan. Suunnitelmatyyppiin yhdistetyt kattavuusasetukset ovat käytettävissä kaikissa suunnitelmissa, jotka luodaan kyseisellä suunnitelmatyypillä. 

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]