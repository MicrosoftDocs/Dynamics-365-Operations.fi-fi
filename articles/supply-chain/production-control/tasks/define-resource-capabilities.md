---
title: Määritä resurssin ominaisuudet
description: Resurssin ominaisuudet kertovat, mitä operatiiviset resurssit voivat tehdä.
author: sorenva
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WrkCtrCapability
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 93b30cbe660d224f0a92f4e412d2b1ba33af3f9b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977835"
---
# <a name="define-resource-capabilities"></a>Määritä resurssin ominaisuudet

[!include [banner](../../includes/banner.md)]

Resurssin ominaisuudet kertovat, mitä operatiiviset resurssit voivat tehdä. Ajoituksen aikana kunkin työn ja työvaiheen vaatimukset kohdistetaan käytettävissä olevien resurssien ominaisuuksiin. Tämä tehtävän ohjaus auttaa resurssin ominaisuuden luomisessa ja ominaisuuden liittämisessä resurssiin. Tämän tehtävän luomisessa käytetty esittely-yritys on USMF.


## <a name="create-a-resource-capability"></a>Resurssin ominaisuuden luominen
1. Siirry Resurssin ominaisuudet -kohtaan.
2. Valitse Uusi.
3. Kirjoita resurssin ominaisuuden tunnus Ominaisuus-kenttään.
    * Ominaisuuden tunnuksen avulla voit määrittää annetun työvaiheen ne resurssit, joilla on oltava tämä ominaisuus työvaiheen suorittamista varten.  
4. Syötä ominaisuuden kuvaus Kuvaus-kenttään.

## <a name="assign-capability-to-a-resource"></a>Ominaisuuden määrittäminen resurssille
1. ValitseLisää.
2. Kirjoita resurssin tunnus Resurssi-kenttään.
    * Resurssin ominaisuus voidaan määrittää yhteen tai useaan resurssiin.  
3. Syötä päivämäärä Päättyminen-kenttään.
    * Tämän kentän avulla voit määrittää resurssin, jolla on ominaisuus vain rajoitetun ajan.  
4. Syötä numero Prioriteetti-kenttään.
    * Töiden ja työvaiheiden ajoittamisen yhteydessä voit määrittää, valitaanko resurssit prioriteetin mukaan. Jos tämä on valittu ja usea resurssi voi suorittaa työn tai työvaiheen vaadittuun päivämäärään mennessä, valitaan resurssi, jolla on liittyvän pakollisen ominaisuuden alhaisin prioriteetti.  
5. Syötä numero Taso-kenttään.
    * Kun määrität, että työ tai työvaihe vaatii tietyn ominaisuuden, voit määrittää myös vaadittavan vähimmäistason. Ominaisuuden tason avulla voit erotella resurssit, jotka voivat suorittaa saman työn, mutta jotka käyttävät erilaista nopeutta, voimaa jne.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]