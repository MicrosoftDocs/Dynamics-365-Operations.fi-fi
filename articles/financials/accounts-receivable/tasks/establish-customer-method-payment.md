---
title: Määritä asiakkaan maksutapa
description: Tässä ohjeaiheessa käsitellään, kuinka maksutapa luodaan asiakasmaksuille.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPaymMode, BankAccountTableLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 22680a3033c1518735eb9edb4c6f22f310509aba
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867628"
---
# <a name="establish-customer-method-of-payment"></a>Määritä asiakkaan maksutapa

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tässä ohjeaiheessa käsitellään, kuinka maksutapa luodaan asiakasmaksuille. Tässä tehtävässä käytetään esittely-yritystä USMF.

1. Siirry kohtaan **Siirtymisruutu > Moduulit > Myyntireskontra >Maksujen asetukset > Maksutavat**.
2. Valitse **Uusi**.
3. Syötä **Maksutapa**-kenttään maksutavan tunnus. Laskuissa ja maksuissa näkyy maksutavan tunnus. Tee siitä riittävän kuvaava, jolloin siitä selviää tallennettavan maksun tyyppi ja pankkitili.  
4. Syötä **Kuvaus**-kenttään kuvaus.
5. Määritä, minkä maksun tilan maksujen kirjaaminen vaatii. Asiakkaan maksu voidaan kirjata luonnin yhteydessä vain silloin, kun maksun tila on sama kuin tässä määrittämäsi maksun tila.  
6. Määritä, miten asiakkaan maksut luodaan laskuille. Tätä asetusta käytetään vain maksuehdotuksen suorituksen yhteydessä. Maksuehdotusta voidaan käyttää asiakkaan maksuissa suoraveloituksissa ja haettaessa varoja asiakkaiden pankkitileiltä.  
7. Valitse maksutapa. Maksutyypin avulla määritetään, vaatiiko maksu tarkistuksen.  
8. Määritä tilityyppi, jolle maksut kirjataan. Yleensä arvoksi valitaan Pankki.  
9. Valitse pankkitili, jolle tämä maksu kirjataan.
10. Syötä pankkitapahtuman tyyppi, jonka avulla pankin käyttämä maksutyyppi tunnistetaan. Pankkitapahtumalajia käytetään pankkitilin täsmäytysprosessin aikana. Sen avulla täsmäytys on helpompi tehdä.  
11. Määritä, kirjataanko tämä maksu väliaikaisesti välitilille. Jos haluat kokeilla maksulle kellutusaikaa pankin selvityksessä, käytä välitiliöintitoimintoa. Maksu kirjataan väliaikaisesti kirjanpitotilille, kunnes selvitys on tehty. Tällöin maksu siirretään tässä määrittämällesi pankkitilille.  
12. Syötä päätili välitiöintiä varten. Tämä on päätili, jolle maksu kirjataan väliaikaisesti välitiliöinnin avulla.  
13. Määritä sähköisten maksujen asetukset **Tiedostomuoto**-välilehden avulla.
14. Määritä pakolliset kentät **Maksunvalvonta**-välilehden avulla. Jos esimerkiksi haluat käyttää kaikkien maksujen tallentamisessa tätä tapaa, voit valita tämän välilehden kyseisen asetuksen.  
15. Määritä **Maksun määritteet** -välilehden avulla, mitä maksumääritteitä haluat käyttää tässä maksutavassa.
16. Valitse **Tallenna**.

