---
title: Vähennysten määritys
description: ''
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
ms.openlocfilehash: 7ee9e8f3bc0e9027e41d3aa91bd097a3f046cbb4
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008904"
---
# <a name="configure-deductions"></a>Vähennysten määritys

[!include [banner](includes/preview-feature.md)]

Microsoft Dynamics 365 Human Resourcesin vähennysten avulla voit määrittää, kuinka paljon (jos mitään) vähennetään työntekijän palkasta kunkin edun osalta. Vähennyksillä on voimassaoloaika, joten voit ylläpitää vähennystietojen historiatietoja. 

1. VValitse **Etujen hallinta** -työtilassa **Asetukset**-kohdasta **Vähennykset**.

2. Valitse **Uusi**.

3. Määritä seuraavien kenttien arvot.

   | Kenttä | Kuvaus |
   | --- | --- |
   | Pidätys | Yksilöllinen tunnus, jota käytetään edun vähennyksen tunnistamisessa. |
   | Kuvaus | Vähennyksen kuvaus. |
   | Voimassa | Alkamispäivämäärä. Oletusarvo on nykyinen järjestelmän päivämäärä. |
   | Vanhentumisaika | Päättymispäivämäärä. Oletusarvona on 12/31/2154, joka tarkoittaa ei koskaan. |
   | Otsikko | Palkanlaskentajärjestelmän otsikkokoodi, jota tämä vähennys käyttää vähennyksen työntekijäosuudesta, kun etuja käsitellään palkanlaskennassa. Tätä käytetään, kun käytetään kolmannen osapuolen palkanlaskennan tarjoajaa. |
   | Työntekijän palkanlaskennan vähennyksen viite | Palkanlaskentajärjestelmän vähennyskoodi, jota tämä vähennys käyttää vähennyksen työntekijän osassa, kun etuja käsitellään palkanlaskentaa varten. |
   | Summan otsikko | Palkanlaskentajärjestelmän otsikkokoodi, jota tämä vähennysmäärä käyttää vähennyksen työntekijäosuudesta, kun etuja käsitellään palkanlaskennassa. Tätä käytetään yleensä, kun käytetään kolmannen osapuolen palkanlaskennan tarjoajaa. |
   | Voi poistaa | Määrittää, voiko Dynamics 365 for Finance and Operationsista viety arvo aiheuttaa arvon poistamisen palkanlaskentajärjestelmässä. |
   | Yhdistetyt sarakkeet | Määrittää, viedäänkö otsikko ja vähennysmäärä palkanlaskentajärjestelmä vierekkäisissä sarakkeissa. |
   | Muutoksen voimaantulopäivämäärä | Edun vähennysmuutoksen voimaantulon päivämäärä. Tänä päivämääränä järjestelmä muuttaa edun vähennyksen automaattisesti ja päivittää kaikki tähän vähennykseen liittyvät etuussuunnitelmat, kunhan suoritat vähennysmuutoksen päivityskäsittelyn. |
   | Vähennyksen muutos valmis | Vähennysmuutos suoritettu -valintaruutu valitaan automaattisesti sen jälkeen, kun edun vähennysmuutokset on tehty vähennyksen päivityksen muutoskäsittelyn jälkeen. |
   
4. Voit seurata ja ylläpitää etuuskurssimäärityksen muutoksia valitsemalla **Toiminnot**ja sitten **Versioiden ylläpito**.

5. Valitse **Tallenna**. 
