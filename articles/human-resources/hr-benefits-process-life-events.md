---
title: Elämäntapahtumien käsittely
description: Microsoft Dynamics 365 Human Resourcesin työntekijäelinkaaren aikana kukin työntekijä voi kohdata erilaisia elämäntapahtumamuutoksia.
author: twheeloc
ms.date: 08/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitLifeEventTypes, BenefitEligibilityProcessResultViewer
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9155795edf657d6589539e58d4c1536f7e9d64c3
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/31/2022
ms.locfileid: "8069652"
---
# <a name="process-life-events"></a>Elämäntapahtumien käsittely


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Microsoft Dynamics 365 Human Resourcesin työntekijäelinkaaren aikana kukin työntekijä voi kohdata erilaisia elämäntapahtumamuutoksia. Esimerkiksi avioliitto, muutos työsuhteessa tai huollettavan/edunsaajan muutos. Jos haluat käyttää elämäntapahtumia, elämäntapahtumat on otettava käyttöön **Etuusparametrit**-sivulla sekä elämäntapahtumatyypit ja suunnitelmatyyppien elämäntapahtuma-asetukset määritettävä.

Ennen kuin voit käsitellä elämäntapahtumia, avoin rekisteröinti on suoritettava vähintään kerran palkkausjakson aikana. Yhdysvalloissa avoin rekisteröityminen järjestetään tyypillisesti kerran vuodessa. Yhdysvaltojen ulkopuolella avoin rekisteröityminen saatetaan suorittaa palkkauksen yhteydessä. Työn tekijän ei tarvitse valita etuussuunnitelmaa, jotta elämäntapahtumia voidaan käsitellä, mutta heidän on oltava olleita mukana avoimen rekisteröitymisen käsittelyssä. 

Käytä elämäntapahtumien käsittelyä, kun sinulla on työntekijöitä, joilla on tulevaisuudessa toteutuvia elämäntapahtumia. Tämä tapahtuma käsittelee kaikki elämäntapahtumat, joita ei ole käsitelty (kuten tulevat elämäntapahtumat tai lisätyt elämäntapahtumat, jotka eivät ole työntekijäkohtaisia – esimerkki tästä on uusi etu). Reaaliaikaiset elämäntapahtumat ovat piilotettuja.

Jos esimerkiksi tänään on 1. helmikuuta ja työntekijä Joe Smithin on tarkoitus vaihtaa yritystä 14. helmikuuta, järjestelmä käsittelee kaikki tapahtumat 15. helmikuuta saakka, jos suoritat elämäntapahtumien käsittelyn 15. helmikuuta osalta. 

1. Valitse **Etujen hallinta** -työtilassa **Käsittely**-kohdasta **Elämäntapahtumien käsittely**.

2. Määritä **Suorita elämäntapahtumaprosessi** -valintaruudussa arvot seuraaville kentille:

   | Kenttä | Kuvaus |
   | --- | --- |
   | **Rekisteröitymiskausi** | Rekisteröintijakso, jonka elämäntapahtumat käsitellään. |
   | **Oikeushenkilö** | Yritys, jonka elämäntapahtumat käsitellään. |
   | **Elinkaaritapahtuman päivämäärä** | Järjestelmä käsittelee kaikki rekisteröintijakson aikana tähän päivämäärään mennessä toteutuneet tapahtumat. |
   | **Työntekijä** | Työntekijä, jonka elämäntapahtumat käsitellään. Jos jätät tämän kentän tyhjäksi, käsitellään kaikkien työntekijöiden elämäntapahtumat. |

3. Jos haluat suorittaa prosessin taustalla, valitse **Suorita taustalla** ja tee seuraavat tehtävät:

   1. Määritä prosessin tiedot.

   2. Jos haluat määrittää toistuvan työn, valitse **Toistuminen**, kirjoita toistuvuustiedot ja valitse **OK**.

   3. Jos haluat määrittää työpaikkahälytyksen, valitse **Hälytykset**, valitse vastaanotettavat hälytykset ja valitse sitten **OK**.

   4. Valitse **OK**. Prosessi suoritetaan määrittämilläsi parametreilla.

4. Valitse **OK**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
