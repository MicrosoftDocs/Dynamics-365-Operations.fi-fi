---
title: Vähennysten määrittäminen
description: Microsoft Dynamics 365 Human Resourcesin vähennysten avulla voit määrittää, kuinka paljon (jos mitään) vähennetään työntekijän palkasta kunkin edun osalta.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
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
ms.openlocfilehash: 5e645c3f098163626cb686aba347897781d7ebc0
ms.sourcegitcommit: a9461650d11d6845e1942865ebf7e35f75f61ad3
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/06/2020
ms.locfileid: "3230059"
---
# <a name="configure-deductions"></a>Vähennysten määrittäminen

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
   | **Muutoksen voimaantulopäivämäärä** | Edun vähennysmuutoksen voimaantulon päivämäärä. Tänä päivämääränä järjestelmä muuttaa edun vähennyksen automaattisesti ja päivittää kaikki tähän vähennykseen liittyvät etuussuunnitelmat, kunhan suoritat **Vähennysmuutoksen päivitys** -käsittelyn. |
   | **Vähennyksen muutos valmis** | **Vähennysmuutos suoritettu** -valintaruutu valitaan automaattisesti sen jälkeen, kun edun vähennysmuutokset on tehty vähennyksen päivityksen muutoskäsittelyn jälkeen. |
   
4. Voit seurata ja ylläpitää etuuskurssimäärityksen muutoksia valitsemalla **Toiminnot**ja sitten **Versioiden ylläpito**.

5. Valitse **Tallenna**. 
