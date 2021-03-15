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
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1df738e3925dc23e7723d93f33acf6a9d811b113
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4964538"
---
# <a name="create-and-export-vendor-payments-using-iso20022-payment-format"></a>Toimittajien maksujen luominen ja tuonti ISO20022-maksumuodossa

[!include [banner](../../includes/banner.md)]

Tässä ohjeaiheessa käsitellään, miten voit luoda maksurivit toimittajan maksukirjauskansioon sekä luoda toimittajan maksutiedostot ISO2022-pankkisiirtoesimerkin avulla.

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