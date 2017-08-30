--- 
title: Tuotantotilauksen ilmoittaminen valmiiksi
description: "Tässä menettelyssä näytetään, miten tuotantotilaus ilmoitetaan valmiiksi."
author: johanhoffmann
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: ff651be006b4bbe205aa9937bd7927e37a83a558
ms.contentlocale: fi-fi
ms.lasthandoff: 07/27/2017

---
# <a name="report-a-production-order-as-finished"></a>Tuotantotilauksen ilmoittaminen valmiiksi

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tässä menettelyssä näytetään, miten tuotantotilaus ilmoitetaan valmiiksi. Tämän menettelyn luomisessa käytetty esittely-yritys on USMF. Tämä on kuudesta seitsemästä tuotantotilauksen elinkaaresta kertovasta menettelystä.


## <a name="report-a-production-order-as-finished"></a>Tuotantotilauksen ilmoittaminen valmiiksi
1. Siirry kohtaan Tuotannonhallinta > Tuotantotilaukset > Kaikki tuotantotilaukset.
    * Valitse tuotantotilaus, jonka tila on Aloitettu.  
2. Valitse toimintoruudussa Tuotantotilaus.
3. Valitse Ilmoita automaattisesti valmiiksi.
    * Voit vahvistaa tällä sivulla valmiiksi ilmoitettavan lopullisen tuotteen määrän.  
4. Valitse Yleiset-välilehti.
5. Määritä Hyväksytty määrä -asetukseksi 18.
6. Määritä Virhemäärä-asetukseksi 2.
7. Valitse Virheen syy -kentässä Materiaali.
8. Valitse Lopeta työ -valintaruutu tai poista sen valinta.
9. Valitse Hyväksy virhe -valintaruutu tai poista sen valinta.
10. Valitse OK.

## <a name="verify-the-report-as-finished-journal"></a>Tarkista valmiiksi ilmoitettujen kirjauskansio
1. Valitse toimintoruudussa Näytä.
2. Valitse Ilmoitettu valmiiksi.
3. Merkitse valittu rivi luettelossa.
4. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
    * Valmiiksi ilmoitettujen kirjauskansio on kirjattu. Jos haluat tehdä oikaisuja kirjauskansioon, voit luoda manuaalisesti uuden kirjauskansion muutosten tekemistä varten.  

