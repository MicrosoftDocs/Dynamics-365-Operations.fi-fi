---
title: Kattavuusasetusten luominen
description: Tässä artikkelissa käsitellään Microsoft Dynamics 365 Human Resourcesin kattavuusvaihtoehtoja, joilla osallistujan valinnalle etuussuunnitelmassa tai -ohjelmassa.
author: twheeloc
ms.date: 08/24/2021
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
ms.openlocfilehash: f9c107e31e58ba1302cd02e2e82aa405dda0fdef
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/23/2022
ms.locfileid: "9336900"
---
# <a name="create-coverage-options"></a>Kattavuusasetusten luominen


Kattavuusvaihtoehdot määrittävät, kuka katetaan tai kuinka paljon vakuutuspaketissa on vakuutusturvaa. Esimerkiksi lääketieteellisessä palvelupaketissa sinulla voi olla **Vain työntekijä** -vaihtoehto, **Työntekijä + 1** -vaihtoehto ja **Perhe**-vaihtoehto. Henkivakuutuksen osalta voit tarjota vakuutusturvaa **1 x palkalla** tai **2 x palkalla**.

Voit käyttää kattavuusasetuksia uudelleen, kun ne on määritetty. Voit liittää vaihtoehdon yhteen tai useaan suunnitelmaan.

> [!IMPORTANT]
> Kun kattavuusasetukset on määritetty, liitä ne etuuspakettityyppiin. Tämän jälkeen suunnitelmatyyppi yhdistetään etuussuunnitelmaan tai -ohjelmaan. Palvelupakettityyppiin yhdistetyt kattavuusasetukset ovat käytettävissä kaikissa saman tyyppisissä palvelupaketeissa, jotka luodaan.

## <a name="create-coverage-options"></a>Kattavuusasetusten luominen
1. Valitse **Etujen hallinta** -työtilassa **Asetukset**-kohdasta **Kattavuusasetukset**.

2. Valitse **Uusi**.

3. Määritä seuraavien kenttien arvot.

   | Kenttä | Kuvaus |
   | --- | --- |
   | **Kattavuusasetus** | Yksilöllinen kattavuusasetuksen nimi. |
   | **Kuvaus** | Kattavuusasetuksen kuvaus. |
   | **Kattavuuskoodi** | Kattavuuskoodit määrittävät kullekin kelvolliselle katetulle henkilötyypille enimmäis- ja vähimmäismäärät. Kattavuuskoodi ilmaisee, kenet katetaan tai suunnitelmatyypille sallitun kattavuusmäärän. Voit ilmaista kattavuusmäärän dollarisummana tai prosenttiosuutenta. Esimerkki:<ul><li>**Työnt+1** – Täyttääkseen kelpoisuusvaatimuksen työntekijällä on oltava valittuna yksi huollettava (tämän määrän ylittävät valitut huollettavat eivät enää kuulu suunnitelman piiriin).</li><li>**Työnt+perhe** – Täyttääkseen kelpoisuusvaatimukset työntekijällä on oltava valittuna vähintään kaksi huollettavaa.</li></ul> |
   | **Enimmäismäärä** | Huollettavien enimmäismäärä. |
   | **Tila** | Kattavuusasetuksen tila. Jos kattavuusasetuksen tilaksi määritetään **Passiivinen**, kyseistä kattavuusasetusta ei voida valita suunnitelmatyypeissä. |
   | **Prosenttia** | Prosenttiosuus. Tämä kenttä on aktiivinen vain, jos kattavuuskoodikentässä on valittu % x palkka. |
   | **Jakaja** | Laskennassa käytettävä jalkaja, kun valitaan kattavuuskoodi % x palkka. |
   | **Vähimmäisprosenttiosuus** | Vähimmäisprosenttiosuus, kun valitset Prosenttiosuus-kattavuuskoodin. |
   | **Enimmäisprosenttiosuus** | Enimmäisprosenttiosuus, kun valitset Prosenttiosuus-kattavuuskoodin. |

4. Liitä kohtaan **Henkilökohtaisen yhteyshenkilön kelpoisuusvaihtoehdot** asianmukainen henkilökohtaisen yhteyshenkilön kelpoisuusasetus kullekin kattavuusasetukselle.

5. Määritä **Itsepalvelu**-kohdassa seuraavien kenttien arvot:

   | Kenttä | Kuvaus |
   | --- | --- |
   | **Salli työntekijän korvaussumma** | Määrittää, saavatko työntekijät muokata etujen itsepalvelun maksumäärää, kun he valitsevat etuja. Jos valitset tämän valintaruudun, järjestelmä laskee etuussuunnitelman parametrit sen maksumäärän perusteella, jonka työntekijä antaa etujen itsepalveluun. |
   | **Salli työntekijän kattavuussumma** | Määrittää, saavatko työntekijät muokata etujen itsepalvelun kattavuusmäärää, kun he valitsevat etuja. Jos valitset tämän valintaruudun, järjestelmä laskee etuussuunnitelman parametrit sen kattavuusmäärän perusteella, jonka työntekijä syöttää työntekijän itsepalveluun. |

6. Valitse **Tallenna**. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
