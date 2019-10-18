---
title: Toimittajien maksujen luominen ja tuonti ISO20022-maksumuodossa
description: Näiden ohjeiden avulla voit luoda maksurivit toimittajan maksukirjauskansioon sekä luoda toimittajan maksutiedostot ISO2022-pankkisiirtoesimerkin avulla.
author: mrolecki
manager: AnnBe
ms.date: 01/17/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendPaym, SysQueryForm, VendPaymProposalEdit, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b70ad94014587ba8e55735192dbe0ab2e4adf4ee
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185816"
---
# <a name="create-and-export-vendor-payments-using-iso20022-payment-format"></a>Toimittajien maksujen luominen ja tuonti ISO20022-maksumuodossa

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tässä ohjeaiheessa käsitellään, miten voit luoda maksurivit toimittajan maksukirjauskansioon sekä luoda toimittajan maksutiedostot ISO2022-pankkisiirtoesimerkin avulla.

Tämä on viides viidestä tehtävästä, joilla esitellään toimittajamaksujen prosessi, jossa käytetään sähköisen raportoinnin määrityksiä. Käytä tämän esimerkin täyttämiseen DEMF-demotietoja.

## <a name="example"></a>Esimerkki

1.  Valitse **Ostoreskontra > Maksut > Maksukirjauskansio**.
2.  Valitse **Uusi**.
3.  Anna tai valitse arvo **Nimi**-kentässä.
4.  Valitse**Rivit > Maksuehdotus -> Luo maksuehdotus**.
5.  Laajenna **Sisällytettävät tietueet** -osa.
6.  Valitse **Suodatin**.
7.  Valitse luettelossa **Toimittajat-taulukon** ja **Toimittajan tili -kentän** rivi.
8.  Anna tai valitse arvo **Ehdot**-kentässä. Voit käyttää kaikkia maksettavien toimittajatapahtumien valintaehtoja, tässä esimerkissä toimittajan tilinä käytetään arvoa DE-001.
12. Napsauta **OK**.
13. Napsauta **OK**.
14. Valitse **Luo maksut**.
15. Luo ISO20022-maksutiedosto.
    1.  Valitse **Muodosta maksut**.
    2.  Anna tai valitse arvo **Maksutapa**-kentässä.
    3.  Kirjoita arvo **Tiedostonimi**-kenttään. Koska tässä merkissä käytetään EUR-maksua, muodostettu tiedosto on SEPA-yhteensopiva. Maksuja voidaan luoda muilla valuutoilla myös ISO20022-tilisiirtona ja muina toimittaja maksumuotoina.
    4.  Anna tai valitse arvo **Pankkitili**-kentässä.

