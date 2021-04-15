---
title: Määritä poistokirjat
description: Tämä menettely käy läpi uuden poistokirjan luomisprosessin ja liittää sen käyttöomaisuus ryhmään.
author: saraschi2
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetDepBookTable, AssetGroupDepBookSetup
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b0ab7f9332e3224c3dadd62aae532ccffb05c82a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815593"
---
# <a name="set-up-depreciation-books"></a>Määritä poistokirjat 

[!include [banner](../../includes/banner.md)]

Tämä menettely käy läpi uuden poistokirjan luomisprosessin ja liittää sen käyttöomaisuus ryhmään. 

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]