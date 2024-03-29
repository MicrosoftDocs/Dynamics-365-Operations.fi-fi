---
title: Toimittajien maksujen luominen ja tuonti ISO20022-maksumuodossa
description: Näiden ohjeiden avulla voit luoda maksurivit toimittajan maksukirjauskansioon sekä luoda toimittajan maksutiedostot ISO2022-pankkisiirtoesimerkin avulla.
author: mrolecki
ms.date: 01/17/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendPaym, SysQueryForm, VendPaymProposalEdit, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ac84055586eff678ea489b35198b1c2dfab13658
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8856464"
---
# <a name="create-and-export-vendor-payments-using-iso20022-payment-format"></a>Toimittajien maksujen luominen ja tuonti ISO20022-maksumuodossa

[!include [banner](../../includes/banner.md)]

Tässä artikkelissa käsitellään, miten voit luoda maksurivit toimittajan maksukirjauskansioon sekä luoda toimittajan maksutiedostot ISO2022-pankkisiirtoesimerkin avulla.

Tämä on viides viidestä tehtävästä, joilla esitellään toimittajamaksujen prosessi, jossa käytetään sähköisen raportoinnin määrityksiä. Käytä tämän esimerkin täyttämiseen DEMF-demotietoja.

## <a name="example"></a>Esimerkki

1.    Valitse **Ostoreskontra > Maksut > Maksukirjauskansio**.
2.    Valitse **Uusi**.
3.    Anna tai valitse arvo **Nimi**-kentässä.
4.    Valitse **Rivit > Maksuehdotus -> Luo maksuehdotus**.
5.    Laajenna **Sisällytettävät tietueet** -osa.
6.    Valitse **Suodatin**.
7.    Valitse luettelossa **Toimittajat-taulukon** ja **Toimittajan tili -kentän** rivi.
8.    Anna tai valitse arvo **Ehdot**-kentässä. Voit käyttää kaikkia maksettavien toimittajatapahtumien valintaehtoja, tässä esimerkissä toimittajan tilinä käytetään arvoa DE-001.
12.    Napsauta **OK**.
13.    Napsauta **OK**.
14.    Valitse **Luo maksut**.
15. Luo ISO20022-maksutiedosto.
    1.    Valitse **Muodosta maksut**.
    2.    Anna tai valitse arvo **Maksutapa**-kentässä.
    3.    Kirjoita arvo **Tiedostonimi**-kenttään. Koska tässä merkissä käytetään EUR-maksua, muodostettu tiedosto on SEPA-yhteensopiva. Maksuja voidaan luoda muilla valuutoilla myös ISO20022-tilisiirtona ja muina toimittaja maksumuotoina.
    4.    Anna tai valitse arvo **Pankkitili**-kentässä.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]