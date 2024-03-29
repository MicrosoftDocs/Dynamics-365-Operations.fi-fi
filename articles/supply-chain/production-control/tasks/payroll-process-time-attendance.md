---
title: Ota käyttöön työajanseurantaan perustuva palkanlaskentaprosessi
description: Tässä menettelyssä kerrotaan, miten palkanlaskentaprosessi otetaan käyttöön työajan seurannassa.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: JmgPayTable, JmgPayRate, JmgPayAgreementTable, JmgPayAgreementLine, HcmWorker
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d3b196e25699c43dbac06e950aae0ad8a9457a8d
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/29/2021
ms.locfileid: "7566548"
---
# <a name="enable-the-payroll-process-for-time-and-attendance"></a>Ota käyttöön työajanseurantaan perustuva palkanlaskentaprosessi

[!include [banner](../../includes/banner.md)]

Tässä menettelyssä kerrotaan, miten palkanlaskentaprosessi otetaan käyttöön työajan seurannassa. Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.


## <a name="create-a-pay-type-with-a-related-pay-rate"></a>Maksulajin ja liittyvän maksumäärän luominen
1. Työajan seuranta > Asetukset > Palkanlaskenta > Maksutyypit
2. Valitse Uusi.
3. Kirjoita Maksulaji-kenttään arvo.
4. Kirjoita arvo Kuvaus-kenttään.
5. Valitse Tallenna.
6. Valitse Taksat.
    * Maksulajien taksat määritetään erillisille ajanjaksoille. Työntekijöille voidaan erillisiä yksilöllisiä taksoja. Taksoja ei aina tarvitse luoda maksulajeihin työajan seurannassa. Tiedot voivat jo olla palkkajärjestelmässä, jonka avulla palkat luodaan. Taksoja ei aina tarvitse luoda maksulajeihin työajan seurannassa. Tiedot voivat jo olla palkkajärjestelmässä, jonka avulla palkat luodaan.  
7. Valitse Uusi.
8. Merkitse valittu rivi luettelossa.
9. Syötä Taksa-kenttään numero.
10. Valitse Tallenna.

## <a name="create-a-pay-agreement"></a>Maksusopimuksen luominen
1. Sulje sivu.
2. Sulje sivu.
3. Siirry Maksusopimukset-kohtaan.
    * Työajan seuranta > Asetukset > Maksusopimukset  
4. Valitse Uusi.
5. Kirjoita Maksusopimus-kenttään arvo.
6. Kirjoita arvo Kuvaus-kenttään.
7. Valitse Tallenna.
8. Valitse Sopimusrivit.
9. Valitse Uusi.
10. Merkitse valittu rivi luettelossa.
11. Syötä tai valitse arvo Profiilityyppi-kenttään.
12. Syötä tai valitse arvo Maksulaji-kenttään.

## <a name="set-up-pay-agreement-for-time-and-registration-worker"></a>Työajan seurannan työntekijän maksusopimuksen määrittäminen
1. Sulje sivu.
2. Sulje sivu.
3. Siirry Aikarekisteröinnin työntekijät -kohtaan.
    * Työajan seuranta > Asetukset > Aikarekisteröinnin työntekijät  
4. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
5. Valitse Työsuhde-välilehti.
6. Laajenna Aikarekisteröinti-osa.
7. Valitse Muokkaa.
8. Syötä tai valitse arvo Maksusopimus-kenttään.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]