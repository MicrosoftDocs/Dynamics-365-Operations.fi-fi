---
title: Vähennysten määrittäminen
description: Microsoft Dynamics 365 Human Resourcesin vähennysten avulla voit määrittää, kuinka paljon (jos mitään) vähennetään työntekijän palkasta kunkin edun osalta.
author: twheeloc
ms.date: 08/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: bf7ddbfb8717c0311fab7388f346f03618a7b43d
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/31/2022
ms.locfileid: "8065840"
---
# <a name="configure-deductions"></a>Vähennysten määrittäminen


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Microsoft Dynamics 365 Human Resourcesin vähennysten avulla voit määrittää, kuinka paljon (jos mitään) vähennetään työntekijän palkasta kunkin edun osalta. Vähennyksillä on voimassaoloaika, joten voit ylläpitää vähennystietojen historiatietoja. 

1. VValitse **Etujen hallinta** -työtilassa **Asetukset**-kohdasta **Vähennykset**.

2. Valitse **Uusi**.

3. Määritä seuraavien kenttien arvot.

   | Kenttä | Kuvaus |
   | --- | --- |
   | **Pidätys** | Yksilöllinen tunnus, jota käytetään edun vähennyksen tunnistamisessa. |
   | **Kuvaus** | Vähennyksen kuvaus. |
   | **Voimassa** | Alkamispäivämäärä. Oletusarvo on nykyinen järjestelmän päivämäärä. |
   | **Vanhentumisaika** | Päättymispäivämäärä. Oletusarvona on 12/31/2154, joka tarkoittaa ei koskaan. |
   | **Otsikko** | Palkanlaskentajärjestelmän otsikkokoodi, jota tämä vähennys käyttää vähennyksen työntekijäosuudesta, kun etuja käsitellään palkanlaskennassa. Tätä käytetään, kun käytetään kolmannen osapuolen palkanlaskennan tarjoajaa. |
   | **Työntekijän palkanlaskennan vähennyksen viite** | Palkanlaskentajärjestelmän vähennyskoodi, jota tämä vähennys käyttää vähennyksen työntekijän osassa, kun etuja käsitellään palkanlaskentaa varten. |
   | **Summan otsikko** | Palkanlaskentajärjestelmän otsikkokoodi, jota tämä vähennysmäärä käyttää vähennyksen työntekijäosuudesta, kun etuja käsitellään palkanlaskennassa. Tätä käytetään yleensä, kun käytetään kolmannen osapuolen palkanlaskennan tarjoajaa. |
   | **Voi poistaa** | Määrittää, voiko Dynamics 365 for Finance and Operationsista viety arvo aiheuttaa arvon poistamisen palkanlaskentajärjestelmässä. |
   | **Yhdistetyt sarakkeet** | Määrittää, viedäänkö otsikko ja vähennysmäärä palkanlaskentajärjestelmä vierekkäisissä sarakkeissa. |
   | **Muutoksen voimaantulopäivämäärä** | Edun vähennysmuutoksen voimaantulon päivämäärä. Tänä päivämääränä edun vähennys muuttuu ja kaikki tähän vähennykseen liittyvät etuussuunnitelmat päivitetään, kunhan **Vähennysmuutoksen päivitys** -käsittelyn suoritetaan. |
   | **Vähennyksen muutos valmis** | **Vähennysmuutos suoritettu** -valintaruutu valitaan automaattisesti sen jälkeen, kun edun vähennysmuutokset on tehty vähennyksen päivityksen muutoskäsittelyn jälkeen. |
   
4. Voit seurata ja ylläpitää etuuskurssimäärityksen muutoksia valitsemalla **Toiminnot** ja sitten **Versioiden ylläpito**.

5. Valitse **Tallenna**. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
