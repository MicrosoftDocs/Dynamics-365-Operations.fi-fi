---
title: Määritä toimittajat ja toimittajien pankkitilit ISO20022-tilisiirtoja varten
description: Tässä menettelyssä kerrotaan, miten ISO20022-pankkisiirron tai minkä tahansa muun toimittajan maksutiedoston luomisessa vaadittava toimittaja ja toimittajakohtaisen pankkitilin tiedot määritetään.
author: mrolecki
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendTable, VendBankAccounts
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 47735d41fde4c5f71ec1c3209446a593e1f4180c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5813416"
---
# <a name="set-up-vendors-and-vendor-bank-accounts-for-iso20022-credit-transfers"></a>Määritä toimittajat ja toimittajien pankkitilit ISO20022-tilisiirtoja varten

[!include [banner](../../includes/banner.md)]

Tässä menettelyssä kerrotaan, miten ISO20022-pankkisiirron tai minkä tahansa muun toimittajan maksutiedoston luomisessa vaadittava toimittaja ja toimittajakohtaisen pankkitilin tiedot määritetään. 

Tämän menettelyn luomisessa käytetty esittely-yritys on DEMF.
Tämä on neljäs viidestä tehtävästä, joilla esitellään toimittajamaksujen prosessi, jossa käytetään sähköisen raportoinnin määrityksiä. Nämä ohjeet koskevat toimintoa, joka lisättiin Dynamics 365 for Operations -versiossa 1611.


## <a name="set-up-bank-details"></a>Pankin tietojen määrittäminen
1. Siirry kohtaan Ostoreskontra > Toimittajat > Kaikki toimittajat.
2. Käytä pikasuodatinta tietueiden etsimiseen. Voit esimerkiksi suodattaa Toimittajan tili -kenttää arvolla DE-001.
3. Avaa toimittajan tiedot valitsemalla DE-001.
4. Valitse toimintoruudussa Toimittaja.
5. Valitse Pankkitilit.
6. Valitse Muokkaa.
    * Jos pankkitiliä ei ole käytettävissä, tili on luotava.  
7. Syötä SWIFT-koodi-kenttään COBADEFFXXX.
8. Kirjoita IBAN-kenttään DE36200400000628808808.
9. Sulje sivu.

## <a name="set-up-a-method-of-payment-for-the-vendor"></a>Toimittajan maksutavan määrittäminen
1. Valitse Muokkaa.
2. Laajenna tai tiivistä Maksu-osa.
3. Avaa haku valitsemalla Maksutapa-kentässä avattavan valikon painike.
4. Valitse luettelosta SEPA CT -rivillä oleva linkki.
5. Valitse Tallenna.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]