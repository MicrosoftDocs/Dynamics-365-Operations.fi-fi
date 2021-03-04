---
title: Asiakasluottoryhmät
description: Tässä ohjeaiheessa on tietoja asiakasluottoryhmistä
author: mikefalkner
manager: AnnBe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 1ddf41d88d085b102a7d69eeeff0ec463d8b4137
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4442733"
---
# <a name="customer-credit-groups"></a>Asiakasluottoryhmät

[!include [banner](../includes/banner.md)]

Voit määrittää asiakasryhmiä, joilla on jaettu luottoraja. Lisäksi otetaan huomioon myyntilaskutilille määritetty yksittäinen luottoraja.

Asiakasluottoryhmään voidaan valita jäseniä eri yrityksistä. Kun lisäät asiakkaan asiakasluottoryhmän asiakasluetteloon, kunkin asiakkaan luottorajan vanhentumispäivä muutetaan ryhmälle määritetyksi vanhentumispäiväksi.

Voit määrittää asiakasluottoryhmiä **Asiakasluottoryhmät**-sivulla (**Luotonhallinta \> Asiakasluottoryhmät \> Asiakasluottoryhmät**).

1. Anna **Ryhmän numero**- ja **Kuvaus**-kenttiin ryhmän tunniste ja kuvaus.
2. Anna **Luottoraja**- ja **Valuutta**-kenttiin luottoraja ja valuutta, jotka käytetään, kun järjestelmä tarkistaa jonkin ryhmän jäsenen luottorajan.
3. Anna **Luottoraja päivämäärään** -kenttään päivämäärä, jolloin luottoraja vanhenee. Asiakasluottoryhmillä on oltava vanhentumispäivä.

Kun asiakasluottoryhmä on määritetty, voit lisätä siihen asiakkaita määrittämällä niiden yrityksen ja asiakkaan tilitunnuksen. Kun lisäät uuden asiakkaan asiakasluottoryhmään, järjestelmä hakee saman asiakkaan tiliä kaikista yrityksistä ja pyytää sinua lisäämään sen asiakasluottoryhmään.

Voit tarkastella **Erääntyneet saldot** -valikossa kaikkien asiakasluottoryhmän laskutusasiakkaiden erääntymissaldon tietoja. **Erääntymissaldo**-sivulla on laskutusasiakastilien erääntyneiden saldojen yhteenveto.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]