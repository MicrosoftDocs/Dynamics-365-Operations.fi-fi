---
title: Lähetyksen rahdinkuljettajien määrittäminen
description: Tässä menettelyssä kuvataan, kuinka voit asettaa rahdinkuljettajan ja määrittää tiedot, kuten palvelu, lähetystila, kuljetuksen maksuväline, kuljetusrajoitukset ja lähetyshinta.
author: ShylaThompson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6c5ac13d17c97f20ee79e7faf57c570f02158424
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "314483"
---
# <a name="set-up-shipping-carriers"></a>Lähetyksen rahdinkuljettajien määrittäminen

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tässä menettelyssä kuvataan, kuinka voit asettaa rahdinkuljettajan ja määrittää tiedot, kuten palvelu, lähetystila, kuljetuksen maksuväline, kuljetusrajoitukset ja lähetyshinta. Kuljetuskoordinaattori voi sitten määrittää lähtevälle tai saapuvalle kuormalle rahdinkuljettajan.


## <a name="create-a-new-shipping-carrier"></a>Uuden lähetyksen rahdinkuljettajan luominen
1. Valitse Kuljetustenhallinta > Asetukset > Rahdinkuljettajat > Lähetyksen rahdinkuljettajat.
2. Valitse Uusi.
3. Syötä Lähetyksen rahdinkuljettaja -kenttään arvo.
4. Kirjoita arvo Nimi-kenttään.
5. Avaa haku Valitsemalla Tila-kentässä avattavan valikon painike.
6. Etsi haluamasi tietue luettelosta ja valitse se.
7. Napsauta luettelossa valitulla rivillä olevaa linkkiä.

## <a name="fill-in-the-general-information-for-the-shipping-carrier"></a>Lähetyksen rahdinkuljettajan yleistietojen täyttäminen
1. Ota käyttöön Yleiskuvaus-osan laajennus.
2. Valitse Aktivoi lähetyksen rahdinkuljettaja -valintaruutu tai poista sen valinta.
3. Avaa haku valitsemalla Toimittaja-kentässä avattavan valikon painike.
    * Valitse toimittajan tili, johon lähetyksen rahdinkuljettaja liitetään.  
4. Etsi haluamasi tietue luettelosta ja valitse se.
5. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
6. Valitse vaihtoehto Kuljetuksen maksuvälineen tyyppi -kentässä.
    * Valitse Manuaalinen kuljetuksen maksuvälineen käyttö -sivu tai valitse EDI, kun haluat päivittää maksuvälineen sähköistä tiedonsiirtoa (EDI = Electronic Data Interchange).  
7. Valitse Aktivoi rahdinkuljettajan luokitus -valintaruutu tai poista sen valinta.

## <a name="create-the-necessary-services-for-the-shipping-carrier"></a>Lähetyksen rahdinkuljettajan tarvitsemien palveluiden luominen
1. Ota käyttöön Palvelut-osan laajennus.
2. Valitse Uusi.
3. Merkitse valittu rivi luettelossa.
4. Syötä Rahdinkuljettajan palvelu -kenttään arvo.
5. Kirjoita arvo Nimi-kenttään.
6. Avaa haku valitsemalla Kuljetusmenetelmä-kentässä avattavan valikon painike.
7. Etsi haluamasi tietue luettelosta ja valitse se.
8. Napsauta luettelossa valitulla rivillä olevaa linkkiä.

## <a name="set-up-the-address-for-the-carrier-optional"></a>Rahdinkuljettajan osoitteen määrittäminen (valinnainen)
1. Ota käyttöön Osoitteet-osan laajennus.
2. Valitse Uusi.
3. Kirjoita Nimi tai kuvaus -kenttään arvo.
4. Avaa haku valitsemalla Maa/alue-kentässä avattavan valikon painike.
5. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
6. Avaa haku valitsemalla Postinumero-kentässä avattavan valikon painike.
7. Etsi haluamasi tietue luettelosta ja valitse se.
8. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
9. Kirjoita arvo Katuosoite-kenttään.
10. Valitse OK.

## <a name="set-up-the-rating-profile-for-the-shipping-carrier"></a>Lähetyksen rahdinkuljettajan luokituksen profiilin määrittäminen
1. Ota Luokituksen profiilit -osan laajennus käyttöön.
2. Valitse Uusi.
3. Merkitse valittu rivi luettelossa.
4. Syötä Luokituksen profiili -kenttään arvo.
5. Kirjoita arvo Nimi-kenttään.
6. Avaa haku napsauttamalla Toimipaikka-kentässä avattavan valikon painiketta.
7. Etsi haluamasi tietue luettelosta ja valitse se.
8. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
9. Avaa haku valitsemalla Varasto-kentässä avattavan valikon painike.
10. Etsi haluamasi tietue luettelosta ja valitse se.
11. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
12. Avaa haku valitsemalla Hinnan laskenta -kentässä avattavan valikon painike.
    * Valitse hinnan laskenta rahdinkuljettajan yhteystietojen perusteella.  
13. Etsi haluamasi tietue luettelosta ja valitse se.
14. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
15. Avaa haku valitsemalla Hinnan päätiedot -kentässä avattavan valikon painike.
16. Etsi haluamasi tietue luettelosta ja valitse se.
17. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
18. Avaa haku valitsemalla Siirtoajan laskenta -kentässä avattavan valikon painike.
19. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
20. Valitse Tallenna.

