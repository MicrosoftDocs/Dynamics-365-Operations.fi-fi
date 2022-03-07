---
title: Määritä asiakkaan maksutapa
description: Tässä ohjeaiheessa käsitellään, kuinka maksutapa luodaan asiakasmaksuille.
author: ShivamPandey-msft
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustPaymMode, BankAccountTableLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0dd9fb37c733730360c78b702c62adadfdc6bd476ba4c436da08c86a9ad7ff55
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6762136"
---
# <a name="establish-customer-method-of-payment"></a>Määritä asiakkaan maksutapa

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]