---
title: Arvomallien asetukset
description: Näiden ohjeiden avulla voit luoda uuden käyttöomaisuuskirjan ja liittää sen käyttöomaisuusryhmään.
author: moaamer
ms.date: 08/12/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetBookTable, AssetGroupBookSetup
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 46c26e5fad3c5c60d87c2fea2b29043c69b82b5d
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/13/2021
ms.locfileid: "7344655"
---
# <a name="set-up-value-models"></a>Arvomallien asetukset

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../../includes/preview-banner.md)]


Näiden ohjeiden avulla voit luoda uuden käyttöomaisuuskirjan ja liittää sen käyttöomaisuusryhmään. Siinä käytetään kirjanpitäjän roolia ja USMF-yrityksen esittelytietoja.

## <a name="create-a-book"></a>Luo uusi kirja
1. Valitse Käyttöomaisuudet > Asetukset > Kirjat.
2. Valitse Uusi.
3. Kirjoita arvo Kirja-kenttään.
4. Kirjoita arvo Kuvaus-kenttään.
    * Jos Laske poisto -kohta on valittuna, liittyvän käyttöomaisuuserän kirja sisällytetään poistoehdotuksiin. Jos sitä ei ole valittu, käyttöomaisuuskirjalle ei tehdä automaattisesti poistoa.  
5. Valitse Laske poisto -kentässä Kyllä.
6. Syötä tai valitse arvo Poistoprofiili-kenttään.
    * Vaihtoehtoinen poistoprofiili tunnetaan myös poiston vaihdosmenetelmänä. Poistoehdotus vaihtaa tämän profiilin, kun vaihtoehtoinen profiili laskee poistosumman, joka on sama tai suurempi kuin oletuspoistoprofiili.  
    * Lisäpoistoprofiilia käytetään käyttöomaisuuserän lisäpoistoon erityisissä tilanteissa. Voit esimerkiksi käyttää tätä luonnonkatastrofista johtuvan poiston kirjaamiseen.  
    * Jos Luo poistojen oikaisut käyttäen perusoikaisuja -kohta on valittuna, poiston oikaisut luodaan automaattisesti, kun käyttöomaisuuserän arvo päivitetään. Jos sitä ei ole valittu, päivitetty käyttöomaisuuserän arvo vaikuttaa vain tuleviin poistolaskelmiin.  
7. Valitse Luo poistojen oikaisut käyttäen perusoikaisuja -valintaruudun arvoksi Kyllä.
    * Oletusarvon mukaan käyttöomaisuuskirjan tapahtumat kirjataan pääkirjanpitoon. Kirjanpitokirjaukset voi poistaa käytöstä asettamalla Kirjaa kirjanpitoon -kentän arvoksi Ei. Kirjat, joita ei kirjata pääkirjanpitoon ovat yleensä veroraportointia varten. Näin voit poistaa menneitä tapahtumia käyttöomaisuuskirjasta, koska niitä ei ole vahvistettu kirjanpitoon.  
    * Oletuskirjaustaso on nykyinen taso, jos kirjan kirjaukset tehdään kirjanpidon ja Ei mitään, jos kirjanpitokirjauksia ei tehdä. Päivitä kirjanpitotaso, jos haluat kirjata tämän kirjan tapahtumia toiselle tasolle.  
8. Syötä tai valitse arvo Kalenteri-kenttään.
    * Johdettujen kirjojen tapahtumat kirjataan eri kirjoihin samanaikaisesti. Voit luoda tapahtumia ensisijaiseen kirjaan, joista luodaan kirjauksen aikana tarkka kopio johdettuun kirjaan. Johdettujen kirjojen tapahtumille ei suoriteta uudelleenlaskentaa, joten niitä ei tule käyttää poistotapahtumiin.  

## <a name="associate-the-book-with-a-fixed-asset-group"></a>Kirjan liittäminen käyttöomaisuusryhmään
1. Valitse Käyttöomaisuusryhmät.
2. Syötä tai valitse arvo Käyttöomaisuusryhmä-kentässä.
3. Syötä Käyttöikä-kenttään numero.

  - Poistokaudet lasketaan käyttöomaisuuden käyttöiän antamisen jälkeen.  
  - Poistomenetelmä voidaan määrittää verotustarpeen mukaan.
  - Vuokrasopimuksiin liitettyjen käyttöomaisuuserien **Käyttöikä**-kentän arvo ohitetaan joko käyttöomaisuuskirjan vuokra-ajan tai käyttöomaisuuden käyttöiän arvolla sen mukaan, kumpi on lyhyempi. Jos **Omistajuuden siirto** -kentän arvoksi on määritetty käyttöomaisuuskirjassa **Kyllä**, **Käyttöikä**-kentän arvo on aina käyttöomaisuuden käyttöikä.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
