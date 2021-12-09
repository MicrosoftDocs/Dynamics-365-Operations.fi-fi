---
title: Erätyön luominen
description: Erätyö on joukko tehtäviä, jotka lähetetään Application Object Server -palvelinesiintymään (AOS) automaattista käsittelyä varten.
author: maertenm
ms.date: 11/22/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BatchJob, SysRecurrence, BatchAlerts
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 76c6c68f7effad0c40282b22ea2a6bf991862cf5
ms.sourcegitcommit: d7d997ad84623ad952672411c0eb6740972ae0b1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/24/2021
ms.locfileid: "7864170"
---
# <a name="create-a-batch-job"></a>Erätyön luominen

[!include [banner](../../includes/banner.md)]

Erätyö on joukko tehtäviä, jotka lähetetään Application Object Server -palvelinesiintymään (AOS) automaattista käsittelyä varten. Erätyöt suoritetaan sen käyttäjän käyttöoikeustiedoilla, joka on luonut työn. Luo erätyö seuraavien ohjeiden mukaan. Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.


## <a name="create-the-batch-job"></a>Luo erätyö
1. Valitse **Siirtymisruutu > Moduulit > Järjestelmänhallinta > Kyselyt > Erätyöt**.
2. Valitse **Uusi**.
3. Anna **Työn kuvaus**-kentässä erätyön kuvaus.
4. Kirjoita **Ajoitettu aloituspäivämäärä/-aika** -kenttään erätyön suorituspäivämäärä ja -kellonaika.
5. Valitse **Tallenna**.

## <a name="create-a-recurrence"></a>Luo toistuvuus
1. Valitse toimintoruudussa **Erätyö**.
2. Valitse **Toistuminen**. Aseta toistumisalue ja -kuvio näiden asetusten avulla.  
3. Valitse **OK**.

## <a name="add-alerts"></a>Lisää hälytyksiä
1. Valitse toimintoruudussa **Erätyö**.
2. Valitse **Hälytykset**. Ilmaise, haluatko lähettää hälytysviestin, kun erätyö on päättynyt tai peruutettu, tai jos siinä on kohdattu virhe. Määritä sitten, haluatko ilmoitukset ponnahdussanomina.   
3. Valitse **OK**.

## <a name="add-a-task-to-a-batch-job"></a>Tehtävän lisääminen erätyöhön
1.  Valitse **Erätyöt**-sivulla **Näytä tehtävät**.
2.  Luo tehtävä painamalla näppäinyhdistelmää **CTRL+N**.
3.  Syötä erätyön kuvaus.
4.  Valitse **Yritystilit**-kentässä yritystietokanta, jossa tehtävä on suoritettava.
5.  Valitse **Luokan nimi** -kentässä prosessi, joka tehtävän pitäisi suorittaa. 
6.  Valitse tehtävälle tarvittaessa eräryhmä.

    Asiakasohjelmien tehtävät täytyy määrittää eräryhmään. Ne määritetään automaattisesti oletuseräryhmään (kutsutaan myös tyhjäksi eräryhmäksi).

7.  Tallenna tehtävä painamalla näppäinyhdistelmää **CTRL+S**.
8.  Voit määrittää, että valittu tehtävä on riippuvainen toisesta työn tehtävästä, valitsemalla **On ehtoja** -ruudukon ja noudattamalla seuraavia ohjeita jokaiselle määritettävälle ehdolle:

    1. Luo ehto painamalla näppäinyhdistelmää **CTRL+N**.
    2. Valitse päätehtävän tehtävätunnus.
    3. Valitse tila, joka päätehtävän täytyy saavuttaa, ennen kuin sidonnainen tehtävä voidaan suorittaa.
    4. Tallenna ehto painamalla näppäinyhdistelmää **CTRL+S**.

    Jos määrität useita ehtoja, joiden *kaikkien* täytyy täyttyä ennen sidonnaisen tehtävän suorittamista, valitse ehdon tyypiksi **Kaikki**. Valitse ehdon tyypiksi **Mikä tahansa**, jos sidonnaiset tehtävät voi suorittaa, kun *jokin* ehdoista täyttyy.

9.  Valitse, miten tehtävävirheet käsitellään. Jos haluat ohittaa tietyn tehtävän virheen, valitse **Yleiset**-välilehdestä **Ohita tehtävän virhe** -asetus kyseiselle tehtävälle. Jos tämä asetus on valittuna, tehtävän epäonnistuminen ei aiheuta työn epäonnistumista. **Uusien yritysten enimmäismäärä** -kentän avulla voit määrittää, kuinka monta kertaa tehtävää yritetään, ennen kuin se katsotaan epäonnistuneeksi. Parhaan käytännön mukaisesti on suositeltavaa, että **Uusien yritysten enimmäismäärä** -arvoksi ei ole määritetty yli **5**.

    Lisätietoja erän uudelleenyrityksistä on kohdassa [uudelleenyritysten ottaminen käyttöön erissä](../retryable-batch.md).

## <a name="adjust-batch-job-status"></a>Erätyön tilan säätäminen
1. Valitse **Järjestelmän hallinta > Kyselyt > Erätyöt**.
2. Valitse soveltuva erätyö.
3. Valitse toimintoruudussa **Erätyö > Toiminnot > Muuta tila**.
4. Valitse sopiva tila:
    - **Pidätä**: Määritä erätyö **pidätettynä**, jolloin sitä ei anneta erätyön ajastukseen. Vastaa *pysäyttämistä*.
    - **Odottaa**: Määritä erätyö **odottavaksi**, jolloin se odottaa erätyön ajastuksen tekemään poimimista. Vastaa *siirtymistä*.
5. Valitse **OK**.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
