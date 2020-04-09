---
title: Määritä tuotantovirran versiolle viimeinen myyntipäivä
description: Tuotantovirran version voimassaolon ja käsittelyn voi päättää tiettynä päivänä asettamalla versiolle vanhentumispäivän. Sama pätee aktiivisen version korvaamiseen uudella versiolla.
author: cvocph
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5d8df396abc3ac4a2c3920e6bf2b21d8a4463df2
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/18/2020
ms.locfileid: "3146856"
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

