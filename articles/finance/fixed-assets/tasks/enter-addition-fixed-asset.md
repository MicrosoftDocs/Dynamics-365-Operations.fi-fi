---
title: Käyttöomaisuuden lisäyksen määrittäminen
description: Tässä menettelyssä kerrotaan, miten aiemmin määritettyyn käyttöomaisuuserään lisätään lisäys.
author: saraschi2
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetAddition
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dc1e13863ae13daaa641f52f7a55e01fc1353dc1
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142751"
---
# <a name="enter-an-addition-to-a-fixed-asset"></a>Käyttöomaisuuden lisäyksen määrittäminen

[!include [banner](../../includes/banner.md)]

Tässä menettelyssä kerrotaan, miten aiemmin määritettyyn käyttöomaisuuserään lisätään lisäys. Käyttöomaisuuden lisäysten tarkoitus on seurata käyttöomaisuuserän nimikelisäyksiä, huoltoa tai parannuksia. Tämä kohta on tarkoitettu vain tiedoksi. Kaikki käyttöomaisuuden arvon tai käyttöiän muutokset on tehtävä erikseen.   

Menettelyssä käytetään kirjanpitäjän roolia ja USMF-yrityksen esittelytietoja.

1. Siirry siirtymisruudussa kohtaan **Moduulit > Käyttöomaisuuserät > Käyttöomaisuuserät > Käyttöomaisuuserät**.
2. Etsi ja valitse luettelosta käyttöomaisuus lisäystä varten.
3. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
4. Valitse toimintoruudussa **Käyttöomaisuus**.
5. Valitse **Käyttöomaisuuden lisäykset**.
6. Valitse **Uusi**.
7. Kirjoita arvo **Nimi**-kenttään.
8. Määritä **Hankintapäivä**-kentässä oston tai palvelun lisäämisen päivämäärä.
9. Syötä resurssin nimikkeen, huollon tai muun parannuksen kustannus **Yksikkökustannus**-kenttään.
10. Anna **Määrä**-kentässä numero. Kokonaiskustannuksilla ei ole vaikutusta käyttöomaisuuserän arvoon. Se on tarkoitettu vain seuranta- ja tiedotustarkoitukseen. Jos kustannukset aktivoidaan, kirjanpitoarvon korotustapahtuma on kirjattava erikseen.  
11. Valitse **Yleiset**-välilehti.

    * Määritä **Pidentää käyttöikää** -kohdan arvoksi **Kyllä**, jos lisäys pidentää resurssin käyttöikää.  
    * Tämä kenttä on vain tiedoksi. Voit lisätä käyttöikää muokkaamalla käyttöomaisuuserän arvomallien ja/tai poistokirjojen käyttöikää.  

