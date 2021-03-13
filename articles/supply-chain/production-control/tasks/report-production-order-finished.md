---
title: Tuotantotilauksen ilmoittaminen valmiiksi
description: Tässä menettelyssä näytetään, miten tuotantotilaus ilmoitetaan valmiiksi.
author: johanhoffmann
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdParmReportFinished, ProdJournalTransProd, ProdSetupReportFinished
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5d9dcdbcb89df6430fb286c253ebecfc6d885af8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "5011144"
---
# <a name="report-a-production-order-as-finished"></a>Tuotantotilauksen ilmoittaminen valmiiksi

[!include [banner](../../includes/banner.md)]

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

