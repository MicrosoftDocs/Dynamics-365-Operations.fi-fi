---
title: Varaston näkyvyyden apuohjelman yleiskatsaus
description: Tässä aiheessa käsitellään varaston näkyvyyden sisältöä ja sen ominaisuuksia.
author: yufeihuang
ms.date: 10/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 1ea1d8c1b0e8c996ead8461005960fa756ce6ca7
ms.sourcegitcommit: 1e5a46271bf7fae2f958d2b1b666a8d2583e04a8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/25/2021
ms.locfileid: "7678906"
---
# <a name="inventory-visibility-add-in-overview"></a>Varaston näkyvyyden apuohjelman yleiskatsaus

[!include [banner](../includes/banner.md)]

Varaston näkyvyyden apuohjelma (eli *varaston näkyvyyssovellus*) on itsenäinen ja erittäin skaalautuva mikropalvelu, joka antaa mahdollisuuden reaaliaikaiseen varastosaldon seurantaan. Niinpä sen avulla saadaan yleinen varastonäkymä.

Ulkoiset järjestelmät käyttävät palvelua RESTful API -ohjelmointirajapintojen avulla. Tällä tavoin ne voi joko tehdä kyselyjä varastosaldon tiedoissa annetuilla dimensioilla tai tehdä muutoksia varastoon erilaisissa mukautetuissa tietolähteissä.

Varaston näkyvyyssovelluksen on Microsoft Dataverseen perustuva mikrosovellus, joka on laajennettavissa. Sovelluksia voi muodostaa Power Appsin avulla. Lisäksi Power BI:n avulla saa mukautettuja, liiketoiminnan tarpeita vastaavia toimintoja.

Varaston näkyvyyssovelluksen voi integroida useisiin kolmannen osapuolen järjestelmiin määrittämällä standardoitujen varastodimensioiden määritysvaihtoehdot ja määrittämällä tapahtumatyypit. Varaston näkyvyyssovellus tukee myös mukautettua laajennettavuutta määritettävien laskennallisten määrien kautta.

## <a name="inventory-visibility-integration-with-dynamics-365-supply-chain-management"></a>Varaston näkyvyyssovelluksen ja Dynamics 365 Supply Chain Managementin integrointi

Integroitu ratkaisu noutaa tietoja Dynamics 365 Supply Chain Managementista ja seuraa jatkuvasti varaston muutoksia. Lisätietoja: [Asenna ja määritä varaston näkyvyys](inventory-visibility-setup.md) ja [Määritä varaston näkyvyys](inventory-visibility-configuration.md).

## <a name="get-a-global-view-of-inventory"></a>Varaston yleisen näkymän hakeminen

Integroidun ratkaisun avulla voidaan määrittää omat tietolähteet ja keskittää varastotiedot. Lisätietoja: [Varaston näkyvyyden määritys](inventory-visibility-configuration.md).

Varastoa voi tarkastella kahdella tavalla:

- Kyselyn lähettäminen tehokkaan ohjelmointirajapinnan avulla. Tämä ohjelmointirajapinta voi palauttaa lähes reaaliaikaiset varastotiedot suoraan välimuistiin tallennetusta esiintymästä. Sopimuksia ja esimerkkejä on kohdassa [Varaston näkyvyyden julkiset ohjelmointirajapinnat](inventory-visibility-api.md).
- Varastosaldoluettelon raakatietojen tarkasteleminen. Tämä luettelo synkronoidaan säännöllisesti välimuistiin tallennetusta esiintymistä ja näkyy Dataversessa. Lisätietoja on kohdassa [Varaston näkyvyyssovellus](inventory-visibility-power-platform.md).

## <a name="soft-reservations"></a>Alustavat varaukset

Alustavaa varausta käytetään, kun yrityksen on varattava tietty määrä tuotteita tukemaan esimerkiksi myyntitilauksen täyttämistä siten, että ylimyynniltä vältytään. Kun myyntitilaus luodaan ja vahvistetaan Supply Chain Managementissa tai muissa tilausten hallintajärjestelmissä, tietyn määrän varauspyyntö lähetetään varaston näkyvyyssovellukseen. Varaston näkyvyyssovelluksessa voidaan varata tuotteita, joissa on dimensiotiedot, ja tiettyjä varastotapahtumatyyppejä. (Lisätietoja on kohdassa [Varaston näkyvyyssovellus](inventory-visibility-power-platform.md).) Kun määrän varaus on onnistunut, varaustunnus palautetaan. Tämän varaustunnuksen avulla voidaan muodostaa linkki takaisin Supply Chain Managementin tai muiden tilausten hallintajärjestelmien alkuperäiseen tilaukseen.

Toiminnot on suunniteltu siten, että varaston näkyvyyssovelluksen varaus ei muuta kokonaismäärään. Sen sijaan se vain merkitsee varatun määrän. (Tämän vuoksi tällaista varausta kutsutaan *alustavan varauksen*.) Alustava varausmäärälle voidaan tehdä vastakirjaus, kun Supply Chain Management tai kolmannen osapuolen järjestelmä käyttää tuotteet kutsumalla ohjelmointirajapinnan uudelleen. Määrä vähennetään silloin ja kokonaismäärä päivitetään varaston näkyvyyssovelluksessa. Lisätietoja on kohdassa [Varaston näkyvyyden varaukset](inventory-visibility-reservations.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
