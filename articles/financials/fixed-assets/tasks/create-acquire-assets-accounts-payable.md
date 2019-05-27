---
title: Käyttöomaisuuserien luominen ja hankkiminen ostoreskontrasta
description: Tässä tehtävän ohjauksessa esitellään käyttöomaisuuden luominen ja hankinta ostoprosessissa.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetParameters, VendInvoiceWorkspace, VendEditInvoice, VendTableLookup, InventItemIdLookupSimple, AssetTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e6c36338cc67855c79ec97d88bb8b633417b85c7
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1562458"
---
# <a name="create-and-acquire-assets-from-accounts-payable"></a>Käyttöomaisuuserien luominen ja hankkiminen ostoreskontrasta

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tässä tehtävän ohjauksessa esitellään käyttöomaisuuden luominen ja hankinta ostoprosessissa.  Siinä tarvitaan kirjanpitäjää ja ostoreskontran käsittelijää sekä esittely-yritystä USMF.


## <a name="set-fixed-assets-parameters"></a>Käyttöomaisuusparametrien määrittäminen
1. Siirry kohtaan Käyttöomaisuus > Asetukset > Käyttöomaisuuden parametrit.
2. Laajenna tai tiivistä Ostotilaukset-osa.
3. Valitse Salli käyttöomaisuuserän hankinta ostosta -valintaruutu.
4. Valitse Luo käyttöomaisuuserä tuotteen vastaanoton tai laskun kirjaamisen aikana -valintaruutu.

## <a name="create-a-new-vendor-invoice"></a>Uuden toimittajan laskun luominen
1. Siirry kohtaan Ostoreskontra > Työtilat > Toimittajan laskun syöttö.
2. Valitse Uusi toimittajan lasku.
3. Avaa haku valitsemalla Laskutustili-kentässä avattavan valikon painike.
4. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
5. Kirjoita arvo Numero-kenttään.
6. Syötä päivämäärä Kirjauspäivämäärä-kenttään.
7. Valitse Lisää rivi.
8. Avaa haku valitsemalla Nimiketunnus-kentässä avattavan valikon painike.
    * Muita kuin varastoituja nimikkeitä ja hankintaluokkia voi käyttää käyttöomaisuuden hankinnassa.  
9. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
10. Kirjoita numero Määrä-kenttään.
    * Yksi laskurivi voi luoda vain yhden käyttöomaisuuden määrästä riippumatta.  Laskun määrä -kentän arvo siirretään käyttöomaisuuden määrään.  
11. Syötä Yksikköhinta-kenttään numero.
12. Laajenna tai tiivistä Rivitiedot-osa.
13. Valitse Käyttöomaisuus-välilehti.
14. Valitse Luo uusi käyttöomaisuus -valintaruutu.
15. Avaa haku valitsemalla Käyttöomaisuusryhmä-kentässä avattavan valikon painike.
16. Valitse luettelosta käyttöomaisuusryhmä, jota käytetään uuden käyttöomaisuuden luomisessa.
17. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
18. Valitse Kirjaa.
    * Käyttöomaisuus luodaan ja hankitaan, kun lasku on kirjattu.  

