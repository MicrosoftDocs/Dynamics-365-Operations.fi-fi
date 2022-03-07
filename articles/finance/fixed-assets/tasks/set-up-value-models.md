---
title: Arvomallien asetukset
description: Näiden ohjeiden avulla voit luoda uuden käyttöomaisuuskirjan ja liittää sen käyttöomaisuusryhmään.
author: moaamer
ms.date: 12/03/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetBookTable, AssetGroupBookSetup
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: be3b5578bd6509859c36f6a50ea9730e9ef1780e
ms.sourcegitcommit: c85eac17fbfbd311288b50664f9e2bae101c1fe6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/03/2021
ms.locfileid: "7890709"
---
# <a name="set-up-value-models"></a>Arvomallien asetukset

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../../includes/preview-banner.md)]

Näiden ohjeiden avulla voit luoda uuden käyttöomaisuuskirjan ja liittää sen käyttöomaisuusryhmään.

## <a name="create-a-book"></a>Luo uusi kirja
1. Valitse **Käyttöomaisuudet \> Asetukset \> Kirjanpito**.
2. Valitse **Uusi**.
3. Anna **Kirjanpito**-kentässä arvo.
4. Anna arvo **Kuvaus**-kentässä.
5. Määritä **Laske poisto** -asetukseksi **Kyllä**.

    Jos **Laske poisto** -vaihtoehdoksi on määritetty **Kyllä**, liittyvä käyttöomaisuuskirja sisällytetään poistoehdotuksiin. Jos sen arvoksi on asetettu **Ei**, käyttöomaisuuskirjalle ei tehdä automaattisesti poistoa.

6. Syötä tai valitse arvo **Poistoprofiili**-kenttään.

    * Vaihtoehtoinen poistoprofiili tunnetaan myös poiston vaihdosmenetelmänä. Poistoehdotus vaihtaa tämän profiilin, kun vaihtoehtoinen profiili laskee poistosumman, joka on sama tai suurempi kuin oletuspoistoprofiili.
    * Lisäpoistoprofiilia käytetään käyttöomaisuuserän lisäpoistoon erityisissä tilanteissa. Voit esimerkiksi käyttää tätä luonnonkatastrofista johtuvan poiston kirjaamiseen.
    * Jos valitset **Luo poistojen oikaisut käyttäen perusoikaisuja** -kohdan, poiston oikaisut luodaan automaattisesti, kun käyttöomaisuuserän arvo päivitetään. Muutoin päivitetty käyttöomaisuuserän arvo vaikuttaa vain tuleviin poistolaskelmiin.

7. Valitse **Luo poistojen oikaisut käyttäen perusoikaisuja** -valinnan arvoksi **Kyllä**.

    * Oletusarvon mukaan käyttöomaisuuskirjan tapahtumat kirjataan pääkirjanpitoon. Joka tapauksessa kirjanpitokirjaukset voi poistaa käytöstä asettamalla **Kirjaa kirjanpitoon** -vaihtoehdon arvoksi **Ei**. Kirjoja, joita ei kirjata pääkirjanpitoon, käytetään yleensä veroraportoinnissa. Tämä vaihtoehto antaa sinulle enemmän joustavuutta menneiden tapahtumien poistamiseen omaisuuskirjasta, koska tapahtumia ei ole sidottu pääkirjaan.
    * Oletusarvoisesti **Kirjanpitotaso**-kentän arvoksi on asetettu **Nykyinen taso**, jos kirja kirjataan pääkirjaan, ja **Ei mitään**, jos kirjaa ei ole kirjattu pääkirjaan. Päivitä **Kirjanpitotaso**-kentän arvo, jos haluat kirjata tämän kirjan tapahtumia toiselle tasolle.

8. Laske positiivinen poisto.

    * Oletusarvon mukaan **Laske positiivinen poisto** -asetukseksi on valittu **Ei**. Tämä asetus ilmaisee, että poisto hyvittää valittua käyttöomaisuuskirjaa. Lisäksi **Salli nettokirjanpidon arvo on suurempi kuin hankintahinta** ja **Salli negatiivisen nettokirjanpidon arvo** -asetuksen arvoksi on määritetty **Ei,** ja asetuksia voi muuttaa erikseen. 
    * Laskeaksesi positiivisen poiston, aseta **Laske positiivinen poisto** -kohdan asetukseksi **Kyllä**. Tämä asetus ilmaisee, että poisto veloittaa käyttöomaisuuskirjaa. Kun **Laske positiivinen poisto** -asetus on **Kyllä**, **Salli hankintahintaa suurempi nettokirjanpidon arvo** ja **Salli negatiivisen nettokirjanpidon arvo** -asetuksen arvoksi määritetään automaattisesti **Kyllä**, ja ne lukitaan. Tämän lukituksen avulla voit varmistaa, että positiivista poistoa käytetään vain negatiivisella kirjanpitoarvolla (hyvitys) hankituille käyttöomaisuuserille. 

10. Syötä tai valitse arvo **Kalenteri**-kenttään.

    Johdettujen kirjojen tapahtumat kirjataan eri kirjoihin samanaikaisesti. Voit luoda tapahtumia ensisijaiseen kirjaan, joista luodaan kirjauksen aikana tarkka kopio johdettuun kirjaan. Johdettujen kirjojen tapahtumille ei suoriteta uudelleenlaskentaa, joten niitä ei tule käyttää poistotapahtumiin.

## <a name="associate-the-book-with-a-fixed-asset-group"></a>Kirjan liittäminen käyttöomaisuusryhmään

1. Valitse **Käyttöomaisuusryhmät**.
2. Syötä tai valitse arvo **Käyttöomaisuusryhmä**-kentässä.
3. Syötä **Käyttöikä**-kenttään numero.

    * Poistokaudet lasketaan käyttöomaisuuden käyttöiän antamisen jälkeen.
    * Poistomenetelmä voidaan määrittää verotustarpeen mukaan.
    * Vuokrasopimuksiin liitettyjen käyttöomaisuuserien **Käyttöikä**-kentän arvo ohitetaan käyttöomaisuuskirjan vuokra-ajan ja käyttöomaisuuden käyttöiän arvolla sen mukaan, kumpi on lyhyempi. Jos **Omistajuuden siirto** -valinnan arvoksi on määritetty käyttöomaisuuskirjassa **Kyllä**, **Käyttöikä**-kentän arvo on aina käyttöomaisuuden käyttöikä.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
