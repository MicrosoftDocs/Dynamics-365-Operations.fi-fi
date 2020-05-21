---
title: Projektibudjettien ennustemallien luominen
description: Tässä aiheessa kuvataan, miten jäljellä oleville budjeteille luodaan ennustemalli.
author: RadhikaRS
manager: AnnBe
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 07e540f23a668b40a54906a67d87552fe991825a
ms.sourcegitcommit: 5de75c61c33e57c813944f1ab6100aceb020d432
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/29/2020
ms.locfileid: "3321776"
---
# <a name="create-forecast-models-for-project-budgets"></a>Projektibudjettien ennustemallien luominen 

[!include [banner](../includes/banner.md)]

Tässä aiheessa kuvataan, miten jäljellä oleville budjeteille luodaan ennustemalli. Budjetin hallinnan alainen projekti käyttää kahta budjettia: alkuperäistä ja jäljellä olevaa. Kun luot projektibudjetin, sinun on määritettävä alkuperäisen ja jäljellä olevan budjetin ennustemallit, jotka luotiin   **Ennustemallit**-sivulla. Tiettyihin malleihin perustuvat projektibudjetit luodaan, kun toteutat projektibudjetin.

> [!NOTE]
> Budjetin hallinnassa käytettävällä ennustemallilla ei voi olla osamallia eikä sitä voi käyttää osamallina.

1. Valitse kohta **Projektinhallinta- ja kirjanpito** > **Määritys** > **Ennusteet**  > **Ennustemallit**.
2. Valitse **Uusi** luodaksesi uuden ennustemallin ja kirjoita sitten uuden mallin tunnusnumero ja nimi. 
3. Voit estää ennustemallin ennusterivien muuttamisen määrittämällä **Pysäytetty** -asetuksen arvoksi **Kyllä**. 
4. Jos malliin liitettyjen ennusterivien tulisi luoda kassavirtaennusteita kirjanpidossa, aseta **Sisällytä kassavirtaennusteisiin** -valinnan arvoksi **Kyllä**. 
5. Jos haluat käyttää projektin päivää laskun päivämääränä, määritä **Ennustepäivämäärä**-valinnan arvoksi **Kyllä**. 
6. Valitse  **Budjettityyppi**-kenttään jokin seuraavista mallityypeistä:

   - **Alkuperäinen budjetti**: Käytä alkuperäisiä budjettisummia, jotka on toteutettu, kun alkuperäinen budjetti on luotu ja hyväksytty.
   - **Jäljellä oleva budjetti**: Käytä jäljellä olevia budjettisummia projektin elinkaaren aikana. Tämän ennustemallin saldoja vähennetään todellisilla tapahtumilla ja kasvatetaan tai vähennetään budjetin versioilla.
   - **Tehtävä siirtokirjaus**: Käytä tehtävää siirtokirjausta projektin budjettisummien kirjausten siirtämiseen. Kirjausten siirtäminen on valinnainen prosessi, joka voidaan suorittaa käyttämättömien budjettisummien siirtämiseksi tilikaudelta toiselle.

7. Määritä seuraavat asetukset tarvittaessa:

   - Ota käyttöön **Ennustepäivämäärä** käyttääksesi projektin päivää laskun päivämääränä.
   - Ota käyttöön **Ennuste, jossa KET** ennustaaksesi keskeneräisten töiden (KET) perusteella, ja valitse sitten KET-tyyppi. 
   - Voit säilyttää oletuksena olevan **budjettityypin** muodossa **Ei mitään** tai määrittää uuden tyypin. Budjettityyppiä ei voi muuttaa, kun tietuetta on muutettu.     
    > [!NOTE]
    > Jos muutat oletusbudjettityyppiä, kaikki muut asetukset eivät ole käytettävissä päivityksissä, eikä tätä ennustemallia voi käyttää uudelleen. 
   


 

