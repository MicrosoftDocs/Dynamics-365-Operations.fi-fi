---
title: Vapautustilauksen luominen ostosopimuksesta
description: Tässä menettelyssä selvitetään, miten ostosopimusta voi käyttää ostotilauksen luomiseen.
author: RichardLuan
manager: tfehr
ms.date: 08/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7c095eaf1a93d6f1a803c6c9618c930fb2eda2d2
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/16/2021
ms.locfileid: "5021061"
---
# <a name="create-a-purchase-release-order-from-a-purchase-agreement"></a>Vapautustilauksen luominen ostosopimuksesta

[!include [banner](../../includes/banner.md)]

Tässä menettelyssä selvitetään, miten ostosopimusta voi käyttää ostotilauksen luomiseen. Ostosopimusta on käytettävä ostotilauksen luomiseen, koska sen yleisehdot on kopioitava ostotilauksen otsikkoon. Yleensä ostoedustaja tekee tämän tehtävän. Ennen tämän opastuksen käyttöä tarvitset voimassaolevan ostosopimuksen, jossa on toimittajan tuotemääräsitoutuminen ja nimikkeitä. Samaa menettelyä voidaan käyttää, jos sinulla muun tyyppisiä sitoutumisia sisältävä ostosopimus. Voit suorittaa tämän ohjauksen esittely-tietojen USMF-yrityksessä. Jos käytössä on USMF, määritä tämän opastuksen tarvitsemat ennakkoehdot suorittamalla ensin ostosopimuksen luontiopastus.


## <a name="create-a-purchase-order"></a>Ostotilauksen luominen
1. Siirry **siirtymisruudussa** kohtaan **Työtilat > Ostotilauksen valmistelu.** 
2. Valitse **Uusi ostotilaus**.
3. Avaa haku valitsemalla **Toimittajan tili** -kentässä avattavan valikon painike.
4. Etsi haluamasi tietue luettelosta ja valitse se.
5. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
6. Laajenna **Yleiset**-pikavälilehti.
7. Avaa haku napsauttamalla **Ostosopimus**-kentässä avattavan valikon painiketta. Kaikki toiminnot käytettävissä olevat sopimukset ovat tässä luettelossa. Etsi voimassaoleva sopimus, jota haluat käyttää.  
8. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
9. Valitse **Kyllä**.
10. Valitse **OK**.

## <a name="add-a-line"></a>Lisää rivi
1. Kirjoita arvo **Nimiketunnus**-kenttään. Jos sitoutumisessa on tietty varasto- tai toimipaikkasijainti, samat arvot on annettava ostotilausriville, jotta sopimusta voisi käyttää.  
2. Klikkaa **Toimipaikka**-kentässä avattavan valikon painiketta avataksesi haun. Sijainti on ehkä jo täytetty tilauksen tai toimittajan oletusarvolla. Voit siinä tapauksessa ohittaa tämän vaiheen.  
3. Etsi haluamasi tietue luettelosta ja valitse se.
4. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
5. Anna **Määrä**-kentässä numero. Tarkista, että hinta on kopioitu sitoutumisesta.  

## <a name="look-up-the-commitment"></a>Hae sitoutuminen
1. Valitse **Päivitä rivi**.
2. Valitse **Liitetty**. Tässä on lisätietoja ostosopimuksesta. Näet esimerkiksi hinnan ja tiedon siitä, ovatko hinta ja alennus kiinteitä. Jos näin on ja vaihdat hinnan tai alennuksen ostotilauksessa sitoutumisesta poikkeavaan hintaan, järjestelmä poistaa linkin, jolloin ostotilausrivi ei täytä sitoutumista. Näet myös, onko Maksimi pakotetaan -vaihtoehto valittu. Jos näin on, sitoutumisen määrää ei voi ylittää, kun kaikki sitoutumisen täyttävät ostot lasketaan yhteen.  
3. Sulje sivu.

## <a name="look-up-the-purchase-agreement"></a>Hae ostosopimus
1. Valitse **toimintoruudussa** **Yleiset**.
2. Valitse **Ostosopimus**.
3. Sulje sivu.
4. Sulje sivu.

