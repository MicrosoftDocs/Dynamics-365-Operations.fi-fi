---
title: Oston vapautustilauksen luominen ostotilausta luotaessa
description: Tässä menettelyssä selvitetään, miten ostosopimusta voi käyttää ostotilauksen luomiseen.
author: kamaybac
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d2f02961f5f7da9bff389737b447e3b143dd72e3
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5812268"
---
# <a name="create-a-purchase-release-order-when-creating-the-purchase-order"></a>Oston vapautustilauksen luominen ostotilausta luotaessa

[!include [banner](../../includes/banner.md)]

Tässä menettelyssä selvitetään, miten ostosopimusta voi käyttää ostotilauksen luomiseen. Ostosopimusta on käytettävä ostotilauksen luomiseen, koska sen yleisehdot on kopioitava ostotilauksen otsikkoon. Yleensä ostoedustaja tekee tämän tehtävän. Ennen tämän opastuksen käyttöä tarvitset voimassaolevan ostosopimuksen, jossa on toimittajan tuotemääräsitoutuminen ja nimikkeitä. Samaa menettelyä voidaan käyttää, jos sinulla muun tyyppisiä sitoutumisia sisältävä ostosopimus. Voit suorittaa tämän ohjauksen esittely-tietojen USMF-yrityksessä. Jos käytössä on USMF, määritä tämän opastuksen tarvitsemat ennakkoehdot suorittamalla ensin ostosopimuksen luontiopastus.


## <a name="create-a-purchase-order"></a>Luo ostotilaus
1. Avaa ostotilauksen valmistelun työtila.
2. Valitse Uusi ostotilaus.
3. Avaa haku valitsemalla Toimittajan tili -kentässä avattavan valikon painike.
4. Etsi haluamasi tietue luettelosta ja valitse se.
5. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
6. Ota käyttöön Yleinen-osan laajennus.
7. Avaa haku napsauttamalla Ostosopimus-kentässä avattavan valikon painiketta.
    * Kaikki toiminnot käytettävissä olevat sopimukset ovat tässä luettelossa. Etsi voimassaoleva sopimus, jota haluat käyttää.  
8. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
9. Valitse Kyllä.
10. Valitse OK.

## <a name="add-a-line"></a>Lisää rivi
1. Kirjoita arvo Nimiketunnus-kenttään.
    * Jos sitoutumisessa on tietty varasto- tai toimipaikkasijainti, samat arvot on annettava ostotilausriville, jotta sopimusta voisi käyttää.  
2. Avaa haku napsauttamalla Toimipaikka-kentässä avattavan valikon painiketta.
    * Sijainti on ehkä jo täytetty tilauksen tai toimittajan oletusarvolla. Voit siinä tapauksessa ohittaa tämän vaiheen.  
3. Etsi haluamasi tietue luettelosta ja valitse se.
4. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
5. Kirjoita numero Määrä-kenttään.
    * Tarkista, että hinta on kopioitu sitoutumisesta.  

## <a name="look-up-the-commitment"></a>Hae sitoutuminen
1. Valitse Päivitä rivi.
2. Valitse Liitetty.
    * Tässä on lisätietoja ostosopimuksesta. Näet esimerkiksi hinnan ja tiedon siitä, ovatko hinta ja alennus kiinteitä. Jos näin on ja vaihdat hinnan tai alennuksen ostotilauksessa sitoutumisesta poikkeavaan hintaan, järjestelmä poistaa linkin, jolloin ostotilausrivi ei täytä sitoutumista. Näet myös, onko Maksimi pakotetaan -vaihtoehto valittu. Jos näin on, sitoutumisen määrää ei voi ylittää, kun kaikki sitoutumisen täyttävät ostot lasketaan yhteen.  
3. Sulje sivu.

## <a name="look-up-the-purchase-agreement"></a>Hae ostosopimus
1. Valitse toimintoruudussa Yleiset.
2. Valitse Ostosopimus.
3. Sulje sivu.
4. Sulje sivu.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]