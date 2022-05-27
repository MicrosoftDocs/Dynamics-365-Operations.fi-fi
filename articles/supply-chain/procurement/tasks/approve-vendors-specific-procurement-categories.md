---
title: Toimittajien hyväksyminen tiettyihin hankintaluokkiin
description: Tässä ohjeaiheessa selitetään, miten tiettyjen hankintaluokkien toimittajat hyväksytään Dynamics 365 Supply Chain Managementissa.
author: GalynaFedorova
ms.date: 07/30/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendTable, DirPartyEcoResCategory, EcoResCategorySingleLookup, ProcCategoryHierarchyManagement
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4247833a011704a9e3c83ad4a2b464ee49d6b3f5
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/03/2022
ms.locfileid: "8670185"
---
# <a name="approve-vendors-for-specific-procurement-categories"></a>Toimittajien hyväksyminen tiettyihin hankintaluokkiin

[!include [banner](../../includes/banner.md)]

Tässä ohjeaiheessa selitetään, miten tiettyjen hankintaluokkien toimittajat hyväksytään Dynamics 365 Supply Chain Managementissa. Ostoehdotusta luotaessa saattaa olla tarpeen valita hyväksytty tai ensisijainen toimittaja sen mukaan, miten ostokäytännöt on määritetty. Seuraavassa menettelyssä kuvataan, miten toimittaja määritetään hyväksytyksi tai ensisijaiseksi tietylle hankintaluokalle. Yleensä hankinta-asiantuntijat suorittavat tämän tehtävän. Voit käyttää tätä menettelyä esittely-yrityksessä USMF.

1. Siirry siirtymisruudussa kohtaan **Moduulit > Hankinta > Toimittajat > Kaikki toimittajat**.
2. Valitse toimittaja, jonka haluat määrittää hyväksytyksi tai ensisijaiseksi tietylle luokalle.
3. Valitse toimintoruudussa **Yleiset**.
4. Valitse **Luokat**.
5. Valitse **Lisää luokka**.
6. Valitse **Luokka**-kenttään **TOIMISTON JA TYÖPÖYDÄN LISÄVARUSTEET (TOIMISTON JA TYÖPÖYDÄN LISÄVARUSTEET)**.
7. Valitse **Toimittajaluokan tila** -kenttään **Ensisijainen**. Luokalle on mahdollista määrittää useampi kuin yksi ensisijainen toimittaja.  
8. Valitse **Tallenna**.
9. Siirry siirtymisruudussa kohtaan **Moduulit > Hankinta > Hankintaluokat**.
10. Valitse puusta **CORP PROCUREMENT CATEGORIES\OFFICE AND DESK ACCESSORIES**.
11. Laajenna **Toimittajat**-osa. Tarkista, että valitsemasi toimittaja näkyy ensisijaisten toimittajien luettelossa Toimiston ja työpöydän lisävarusteet -luokassa. Jos käytät tätä menettelyä tehtäväoppaana, saatat joutua napsauttamaan **Poista lukitus** -painiketta voidaksesi selata alas toimittajaluetteloon.  On myös mahdollista lisätä ensisijaisia ja hyväksyttyjä toimittajia tällä sivulla.  
12. Laajenna puurakenteessa **OFFICE AND DESK ACCESSORIES** ja valitse **Scissors**.
13. Valitse **Ei** **Peri toimittajat ylemmän tason luokalta** -kenttään.
14. Valitse **Kyllä** **Peri toimittajat ylemmän tason luokalta** -kenttään.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]