---
title: Ostosopimuksen käyttö ostotilausta luotaessa
description: Tässä menettelyssä selvitetään, miten ostosopimusta voi käyttää ostotilauksen luomiseen.
author: kamaybac
ms.date: 08/09/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1913181e85929951ce240ac31a0ac3f1351f6ae51f6ed2790bae577b2100b308
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6731244"
---
# <a name="apply-a-purchase-agreement-when-creating-a-purchase-order"></a>Ostosopimuksen käyttö ostotilausta luotaessa

[!include [banner](../../includes/banner.md)]

Tässä menettelyssä selvitetään, miten ostosopimusta voi käyttää ostotilauksen luomiseen. Ostosopimusta on käytettävä ostotilauksen luomiseen, koska sen yleisehdot on kopioitava ostotilauksen otsikkoon. Yleensä ostoedustaja tekee tämän tehtävän. Ennen tämän opastuksen käyttöä tarvitset voimassaolevan ostosopimuksen, jossa on toimittajan tuotemääräsitoutuminen ja nimikkeitä. Samaa menettelyä voidaan käyttää, jos sinulla muun tyyppisiä sitoutumisia sisältävä ostosopimus.

## <a name="create-a-purchase-order"></a>Ostotilauksen luominen

1. Siirry kohtaan **Tuotanto ja hankita \> Työtilat \> Ostotilauksen valmistelu**.
1. Valitse toimintoruudussa **Uusi ostotilaus**.
1. **Luo ostotilaus** -valintaikkuna avautuu. Valitse **Toimittajan tili**. Tarkista ja muokkaa muita osoitekenttiä tarpeen mukaan.
1. Laajenna **Yleinen**-pikavälilehti.
1. Etsi ja valitse **Ostosopimus**-kentästä voimassa oleva sopimus, jota haluat käyttää. Kaikki toiminnot käytettävissä olevat sopimukset ovat tässä luettelossa.  
1. Valitse **Kyllä**.
1. Valitse **OK**.

## <a name="add-a-line"></a>Lisää rivi

1. Kirjoita arvo **Nimiketunnus**-kenttään. Jos sitoutumisessa on tietty varasto- tai toimipaikkasijainti, samat arvot on annettava ostotilausriville, jotta sopimusta voisi käyttää.
1. Valitse **Toimipaikka**-kentässä avattavan valikon painiketta avataksesi haun. Sijainti on ehkä jo täytetty tilauksen tai toimittajan oletusarvolla. Voit siinä tapauksessa ohittaa tämän vaiheen.  
1. Etsi haluamasi tietue luettelosta ja valitse se.
1. Valitse luettelossa valitulla rivillä oleva linkki.
1. Anna **Määrä**-kentässä numero. Tarkista, että hinta on kopioitu sitoutumisesta.  

## <a name="look-up-the-commitment"></a>Hae sitoutuminen

1. Valitse **Päivitä rivi**.
1. Valitse **Liitetty**. Tässä on lisätietoja ostosopimuksesta. Näet esimerkiksi hinnan ja tiedon siitä, ovatko hinta ja alennus kiinteitä. Jos näin on ja vaihdat hinnan tai alennuksen ostotilauksessa sitoutumisesta poikkeavaan hintaan, järjestelmä poistaa linkin, jolloin ostotilausrivi ei täytä sitoutumista. Näet myös, onko Maksimi pakotetaan -vaihtoehto valittu. Jos näin on, sitoutumisen määrää ei voi ylittää, kun kaikki sitoutumisen täyttävät ostot lasketaan yhteen.  
1. Sulje sivu.

## <a name="look-up-the-purchase-agreement"></a>Hae ostosopimus

1. Valitse **Toimintoruutu**-osiosta **Yleiset**.
1. Valitse **Ostosopimus**.
1. Sulje sivu.
1. Sulje sivu.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]