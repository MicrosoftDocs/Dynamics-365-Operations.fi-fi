---
title: Määritä tuotantovirran versiolle viimeinen myyntipäivä
description: Tuotantovirran version voimassaolon ja käsittelyn voi päättää tiettynä päivänä asettamalla versiolle vanhentumispäivän. Sama pätee aktiivisen version korvaamiseen uudella versiolla.
author: cvocph
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 97ac33d28a49ad0f2a3956ad65b159e4ec4785c7
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/10/2020
ms.locfileid: "3983251"
---
# <a name="define-an-expiry-date-for-a-production-flow-version"></a>Määritä tuotantovirran versiolle viimeinen myyntipäivä

[!include [banner](../../includes/banner.md)]

Tuotantovirran version voimassaolon ja käsittelyn voi päättää tiettynä päivänä asettamalla versiolle vanhentumispäivän. Sama pätee aktiivisen version korvaamiseen uudella versiolla. Versiota ei ole tarpeen poistaa käytöstä.


## <a name="set-an-expiration-date-to-end-a-production-flow-version"></a>Vanhentumispäivän määrittäminen tuotantovirran version päättämiseksi
1. Valitse Tuotannonhallinta > Asetukset > Lean-tuotantovirta > Tuotantovirrat.
2. Etsi haluamasi tietue luettelosta ja valitse se.
    * Valitse tuotantovirta, jolla on jo määritelty versio.  
3. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
4. Valitse Muokkaa.
5. Merkitse valittu rivi luettelossa.
6. Anna päivämäärä ja kellonaika Vanhentumispäivä-kenttään.
    * Vanhentumispäivästä alkaen uusi versio ei käynnisty tai aktivoidu. Töiden käynnistäminen tai luonti tähän tuotantovirtaan ei ole myöskään enää mahdollista. Käynnistetyt työt voi saattaa valmiiksi vanhentumispäivän jälkeenkin.  

