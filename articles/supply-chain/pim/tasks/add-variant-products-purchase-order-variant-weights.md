---
title: Lisää tuotevariantteja ostotilauksiin käyttämällä muuttuvia painotuksia
description: Tässä menettelyssä kerrotaan, miten kunkin tuotevariantin ostotilausrivit täytetään automaattisesti variantin painojen avulla.
author: ShylaThompson
manager: tfehr
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0199f4b05c23eec5c03c770c37111a6ee6d13efe
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208383"
---
# <a name="add-variant-products-to-purchase-orders-using-variant-weights"></a>Lisää tuotevariantteja ostotilauksiin käyttämällä muuttuvia painotuksia

[!include [banner](../../includes/banner.md)]

Tässä menettelyssä kerrotaan, miten kunkin tuotevariantin ostotilausrivit täytetään automaattisesti variantin painojen avulla. Kun ostettavan tuotteen määrä on valittu, kaikille tuotevarianteille luodaan ostotilausrivit. Ne sisältävät ehdotetut määrät tuotevariantille määritettyjen painojen perusteella. Tämä menettely ei sisällä tuotedimensioiden ja tuotevarianttien painoarvojen määrityksen vaiheita. Menettely käyttää esittelytietojen USRT-yritystä.

1. Valitse Ostoreskontra > Ostotilaukset > Kaikki ostotilaukset.
2. Valitse Uusi.
3. Avaa haku valitsemalla Toimittajan tili -kentässä avattavan valikon painike.
4. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
5. Ota käyttöön Yleinen-osan laajennus.
6. Avaa haku napsauttamalla Toimipaikka-kentässä avattavan valikon painiketta.
7. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
8. Avaa haku valitsemalla Varasto-kentässä avattavan valikon painike.
9. Etsi haluamasi tietue luettelosta ja valitse se.
10. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
11. Valitse OK.
12. Ota käyttöön Rivitiedot-osan laajennus.
13. Valitse Variantit-välilehti.
14. Valitse Lisää rivi.
15. Merkitse valittu rivi luettelossa.
16. Kirjoita Nimiketunnus-kenttään 0140.
17. Valitse määräksi 1000.
18. Valitse Tallenna.

