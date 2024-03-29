---
title: Rekisteröintikelpoisuuden käsittely
description: Tässä artikkelissa kerrotaan, miten rekisteröintikelpoisuusprosessi suoritetaan.
author: twheeloc
ms.date: 08/23/2021
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
ms.openlocfilehash: bd05585f691a4c6aa55a7aec7ceaaf0273f0abcb
ms.sourcegitcommit: 66d129874635d34a8b29c57762ecf1564e4dc233
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/23/2022
ms.locfileid: "9323478"
---
# <a name="process-enrollment-eligibility"></a>Rekisteröintikelpoisuuden käsittely

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tässä artikkelissa kerrotaan, miten rekisteröintikelpoisuusprosessi suoritetaan.

1. Valitse **Etujen hallinta** -työtilassa **Käsittely**-kohdasta **Rekisteröintikelpoisuuden käsittely**.

2. Määritä **Suorita edun rekisteröintikelpoisuusprosessi** -valintaruudussa arvot seuraaville kentille:

   | Kenttä | Kuvaus |
   | --- | --- |
   | **Rekisteröitymiskausi** | Rekisteröintijakso, jonka rekisteröintikelpoisuus käsitellään. |
   | **Oikeushenkilö** | Yritys, jonka rekisteröintikelpoisuus käsitellään. |
   | **Työntekijä** | Työntekijä, jonka rekisteröintikelpoisuus käsitellään. Jos jätät tämän kentän tyhjäksi, käsitellään kaikkien työntekijöiden rekisteröintikelpoisuus. |
   | **Etuussuunnitelma** | Etuussuunnitelma, jonka rekisteröintikelpoisuus käsitellään.

3. Jos haluat suorittaa prosessin taustalla, valitse **Suorita taustalla** ja tee seuraavat tehtävät:

   1. Määritä prosessin tiedot.

   2. Jos haluat määrittää toistuvan työn, valitse **Toistuminen**, kirjoita toistuvuustiedot ja valitse **OK**.

   3. Jos haluat määrittää työpaikkahälytyksen, valitse **Hälytykset**, valitse vastaanotettavat hälytykset ja valitse sitten **OK**.

   4. Valitse **OK**. Prosessi suoritetaan määrittämilläsi parametreilla.

4. Valitse **OK**.

## <a name="view-process-results"></a>Näytä prosessitulokset

Tässä artikkelissa kerrotaan, miten kelpoisuusprosessitulokset näytetään.

1.  Valitse **Etujen hallinta** -työtilassa **Käsittely**-kohdasta **Prosessitulokset**.

2.  **Prosessitulokset**-sivulla määritetään seuraavat kentät:

   | Kenttä | kuvaus |
   | --- | --- |
   | **Prosessitunnus** | Työntekijän, yrityksen ja prosessiajon yksilöivä tunnus. |
   | **Prosessityyppi** | Tämä määrittää suoritettavan prosessin. Esimerkiksi: Ilmoittautuminen. |
   | **Aikaleima** | Kelpoisuusprosessin suoritusaika. |
   | **Yritys** | Rekisteröintiprosessin aikana määritetty yritys. |
   | **Työntekijä** | Käsitelty työntekijä. |
   | **Suunnitelma | Etuussuunnitelma, johon rekisteröintiä yritettiin. |
   | **Kelpoisuussääntö** | Käsiteltävä oikeutussääntö. Jos virhe ilmeni ennen tukikelpoisuuden suorittamista, se on tyhjä. Esimerkki: Jos kompensaatiota ei ole määritetty työntekijälle, oikeutusprosessia ei suoriteta, ja tämä kenttä jätetään tyhjäksi. |
   | **Tuloksen tila** | Tämä on kelvollinen tai kelpaamaton. Tulostila ei ole käytettävissä, jos työntekijä ei täytä kelpoisuussäännön ehtoja, jos työntekijästä puuttuu pakollisia tietoja, kuten maksutiheys tai kiinteämääräinen kompensaatio, tai jos etuussuunnitelmasta puuttuu tietoja, jotka estävät työntekijöitä ilmoittautumasta. |
   | **Tulossanoma** | Ilmaisee, miksi työntekijä ei ole oikeutettu etuusjärjestelyyn tai jos oikeutussääntö on kulunut. |



[!INCLUDE[footer-include](../includes/footer-banner.md)]
