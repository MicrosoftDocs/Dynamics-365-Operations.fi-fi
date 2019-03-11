---
title: Käyttöomaisuuden poistokirjojen määrittäminen (Toukokuu 2016)
description: Tässä tehtävän ohjauksessa luodaan uusi poistokirja ja liitetään se käyttöomaisuusryhmään.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepBookTable, AssetGroupDepBookSetup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1fd53ea1dff9b116d19c525c5d6967ece0993b6f
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "355561"
---
# <a name="set-up-depreciation-books-may-2016"></a>Käyttöomaisuuden poistokirjojen määrittäminen (Toukokuu 2016)

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tässä tehtävän ohjauksessa luodaan uusi poistokirja ja liitetään se käyttöomaisuusryhmään.  Siinä käytetään kirjanpitäjän roolia ja USMF-yrityksen esittelytietoja.


## <a name="create-a-depreciation-book"></a>Poistokirjan luominen
1. Siirry kohtaan Käyttöomaisuus > Asetukset > Poistokirjat.
2. Valitse Uusi.
3. Kirjoita arvo Poistokirja-kenttään.
4. Kirjoita arvo Kuvaus-kenttään.
5. Valitse Laske poisto -valintaruutu tai poista sen valinta.
6. Avaa haku valitsemalla Poistoprofiili-kentässä avattavan valikon painike.
7. Etsi haluamasi poistoprofiili luettelosta ja valitse se.
8. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
9. Avaa haku valitsemalla Vaihtoehtoinen poistoprofiili -kentässä avattavan valikon painike.
10. Valitse luettelosta haluamasi poistoprofiili.
11. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
    * Lisäpoistoprofiilia käytetään käyttöomaisuuserän lisäpoistoon erityisissä tilanteissa. Voit esimerkiksi käyttää tätä luonnonkatastrofista johtuvan poiston kirjaamiseen.  
12. Valitse Luo poistojen oikaisut käyttäen perusoikaisuja -valintaruutu tai poista sen valinta.
13. Avaa haku valitsemalla Kalenteri-kentässä avattavan valikon painike.
14. Napsauta luettelossa valitulla rivillä olevaa linkkiä.

## <a name="associate-the-depreciation-book-with-a-fixed-asset-group"></a>Poistokirjan liittäminen käyttöomaisuusryhmään
1. Valitse Käyttöomaisuusryhmät.
2. Avaa haku valitsemalla Käyttöomaisuusryhmä-kentässä avattavan valikon painike.
3. Etsi haluamasi tietue luettelosta ja valitse se.
4. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
5. Valitse vaihtoehto Poistomenetelmä-kentässä.
6. Syötä Käyttöikä-kenttään numero.
    * Ota huomioon, että Poistokaudet-kentän arvo lasketaan käyttöiän määrittämisen jälkeen.  

