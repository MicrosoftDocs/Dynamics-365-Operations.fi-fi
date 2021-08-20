---
title: Käyttöomaisuuserien luominen ja hankkiminen ostoreskontrasta
description: Tässä tehtävän ohjauksessa esitellään käyttöomaisuuden luominen ja hankinta ostoprosessissa.
author: saraschi2
ms.date: 08/13/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetParameters, VendInvoiceWorkspace, VendEditInvoice, VendTableLookup, InventItemIdLookupSimple, AssetTable
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 035fa86f0ff09faaa21c561cf7934455a6883cd8a7f917ac95bc7d096294d824
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6742998"
---
# <a name="create-and-acquire-assets-from-accounts-payable"></a>Käyttöomaisuuserien luominen ja hankkiminen ostoreskontrasta

[!include [banner](../../includes/banner.md)]

Tässä tehtävän ohjauksessa esitellään käyttöomaisuuden luominen ja hankinta ostoprosessissa.  Siinä tarvitaan kirjanpitäjää ja ostoreskontran käsittelijää sekä esittely-yritystä USMF.


## <a name="set-fixed-assets-parameters"></a>Käyttöomaisuusparametrien määrittäminen
1. Siirry **siirtymisruudussa** kohtaan **Moduulit > Käyttöomaisuuserät > Asetukset > Käyttöomaisuusparametrit**.
2. Laajenna **Ostotilaukset**-pikavälilehti.
3. Valitse **Salli käyttöomaisuuserän hankinta ostosta** -valintaruutu.
4. Valitse **Luo käyttöomaisuuserä tuotteen vastaanoton tai laskun kirjaamisen aikana** -valintaruutu.

## <a name="create-a-new-vendor-invoice"></a>Uuden toimittajan laskun luominen
1. Siirry **siirtymisruudussa** kohtaan **Moduulit > Ostoreskontra > Työtilat > Toimittajan laskun syöttö**.
2. Valitse **Uusi toimittajan lasku**.
3. Avaa haku valitsemalla **Laskutustili**-kentässä avattavan valikon painike.
4. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
5. Kirjoita arvo **Numero**-kenttään.
6. Syötä päivämäärä **Kirjauspäivämäärä**-kenttään.
7. Valitse **Lisää rivi**.
8. Avaa haku valitsemalla **Nimiketunnus**-kentässä avattavan valikon painike. Muita kuin varastoituja nimikkeitä ja hankintaluokkia voi käyttää käyttöomaisuuden hankinnassa.  
9. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
10. Anna **Määrä**-kentässä numero. Yksi laskurivi voi luoda vain yhden käyttöomaisuuden määrästä riippumatta. Laskun määrä -kentän arvo siirretään käyttöomaisuuden määrään.  
11. Syötä **Yksikköhinta**-kenttään numero.
12. Laajenna **Rivin erittely** -pikavälilehti.
13. Valitse **Käyttöomaisuus**-välilehti.
14. Valitse **Luo uusi käyttöomaisuus** -valintaruutu.
15. Avaa haku valitsemalla **Käyttöomaisuusryhmä**-kentässä avattavan valikon painike.
16. Valitse luettelosta käyttöomaisuusryhmä, jota käytetään uuden käyttöomaisuuden luomisessa.
17. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
18. Valitse **Kirjaa**. Käyttöomaisuus luodaan ja hankitaan, kun lasku on kirjattu.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]