---
title: Vapaatekstilaskun korjaus
description: Tässä artikkelissa kerrotaan, miten kirjattu vapaatekstilasku korjataan ja luodaan uudelleen korjattuna laskuna.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 13991
ms.assetid: 2a0a4789-8619-4974-bef9-0923cc848420
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c8c1b90b7b2c02a53e53cc13d70445a237b126d4
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1559776"
---
# <a name="correct-a-free-text-invoice"></a>Vapaatekstilaskun korjaus

[!include [banner](../includes/banner.md)]

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



