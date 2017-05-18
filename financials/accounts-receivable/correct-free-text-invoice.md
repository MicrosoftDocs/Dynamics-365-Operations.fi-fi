---
title: Vapaatekstilaskun korjaus
description: "Tässä artikkelissa kerrotaan, miten kirjattu vapaatekstilasku korjataan ja luodaan uudelleen korjattuna laskuna."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13991
ms.assetid: 2a0a4789-8619-4974-bef9-0923cc848420
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: df94cf12accd2b18c1f8cfd43d7de5dff16e7aea
ms.contentlocale: fi-fi
ms.lasthandoff: 04/25/2017


---

# <a name="correct-a-free-text-invoice"></a>Vapaatekstilaskun korjaus

[!include[banner](../includes/banner.md)]


Tässä artikkelissa kerrotaan, miten kirjattu vapaatekstilasku korjataan ja luodaan uudelleen korjattuna laskuna.

Voit korjata kirjatun vapaatekstilaskun avaamalla kirjatun vapaatekstilaskun. Valitse **Lasku**-sivulla **Peruuta** ja sitten **Korjaa lasku**. Valitse syykoodi, lisää kommentit ja valitse päivämäärä uudelle korjatulle laskulle. Voit muokata korjattua laskua ja kirjata sen. 

Kun kirjaat korjatun laskun, hyvityssummalle luodaan alkuperäisen laskun suuruinen peruutuslasku. Alkuperäisen laskun ja peruutuslasku yhteissaldo onkin tämän vuoksi 0 (nolla). Peruutuslasku tilitetään alkuperäiseen laskuun. 

Korjatun laskun kirjaamisen jälkeen sinulla on kolme laskua:

-   **Alkuperäinen lasku** – lasku, joka sisältää korjattavat tiedot.
-   **Peruutuslasku** – järjestelmän luoma hyvityslasku, joka on luotiin peruuttamaan viimeksi korjattu lasku.
-   **Korjattu lasku** – lasku, joka sisältää korjatut laskutiedot.

Peruutuslaskun ja korjaavan laskun voi tunnistaa kahdella tavalla:

-   **Kaikki vapaamuotoiset laskut** -sivulla on **Korjaus**-sarake, josta näet, mitkä laskut ovat peruutuslaskuja ja mitkä korjattuja laskuja.
-   Vapaatekstilaskun otsikon tila on joko **Peruutuslasku \[laskunumero\]** tai **Korjattu lasku \[laskunumero\]**.

> [!NOTE]
> Tämä toiminto on käytettävissä vain, jos **Tekstimuotoisen laskun korjaus** -määritysavain on valittu.




