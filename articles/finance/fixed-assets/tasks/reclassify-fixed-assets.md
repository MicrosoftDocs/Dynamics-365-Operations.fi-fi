---
title: Luokittele käyttöomaisuuserät uudelleen
description: Tässä artikkelissa kerrotaan käyttöomaisuuserän uudelleenluokitteluprosessista. Voit luokitella käyttöomaisuuserän uudelleen siirtämällä sen uuteen käyttöomaisuusryhmään tai määrittämällä sille uuden samaan ryhmään kuuluvan käyttöomaisuuserän numeron.
author: moaamer
ms.date: 05/14/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4bd901b1709f0b006cecfbbf6d8c170b56f89d19
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9284360"
---
# <a name="reclassify-fixed-assets"></a>Luokittele käyttöomaisuus uudelleen

[!include [banner](../../includes/banner.md)]

Voit luokitella käyttöomaisuuserän uudelleen siirtämällä sen uuteen käyttöomaisuusryhmään tai määrittämällä sille uuden samaan ryhmään kuuluvan käyttöomaisuuserän numeron. 

Kun käyttöomaisuuserä luokitellaan uudelleen:

- Kaikki aiemman käyttöomaisuuserän kirjat luodaan myös uudelle käyttöomaisuuserälle. Alkuperäiselle käyttöomaisuuserälle mahdollisesti määritetyt tiedot kopioidaan uuteen käyttöomaisuuserään. Alkuperäisen käyttöomaisuuserän kirjojen tila on Suljettu. 

- Uuden käyttöomaisuuserän kirjoissa on uudelleenluokittelupäivä **Hankintapäivämäärä**-kentässä. **Poiston suorituspäivä** -kenttä kopioidaan alkuperäisen käyttöomaisuuden tiedoista. Jos poistot on jo aloitettu, **Viimeisen poiston suorituspäivä** -kentässä näkyy uudelleenluokittelun päivämäärä. 

- Alkuperäisen käyttöomaisuuserän aiemmin luodut käyttöomaisuustapahtumat peruutetaan ja luodaan uudelleen uudelle käyttöomaisuuserälle.

- Kun käyttöomaisuuserä, jolla on siirtotapahtuma, on luokiteltu uudelleen, järjestelmä näyttää **toimintokeskuksessa** sanoman, jossa ilmoitetaan, ettei siirtotapahtumaa ole suoritettu uudelleenluokitteluprosessin aikana. Siirtotapahtuma on suoritettava valmiiksi, jotta olemassa olevat uudelleenluokittelutapahtumat voidaan siirtää asianmukaisiin taloushallinnon dimensioihin. 

   Uudelleenluokittelun aikana järjestelmä luokittelee käyttöomaisuussaldon alkuperäisestä käyttöomaisuuserästä uuteen käyttöomaisuuserään uudelleen seuraavasti: 
   
   - Uudelleenluokitteluprosessi kopioi tiedot alkuperäisestä käyttöomaisuuskirjasta uuteen käyttöomaisuuskirjaan.

   - Uudelleenluokittelutapahtuma käyttää alkuperäisen kirjatun hankinnan tietoja, jotka sisältävät hankintatapahtumaan sisältyviä kirjanpitodimensiotietoja.  
   
   - Uudelleenluokitteluprosessi palauttaa samalla alkuperäisen käyttöomaisuuden hankinta- ja käyttöomaisuussiirtotapahtuman. 

Seuraavassa kaaviossa ja menettelyssä on esimerkki uudelleenluokitteluprosessista. 

[![Kaavio, jossa näkyy uudelleenluokitteluprosessi.](../media/reclassification-process-01.png)](../media/reclassification-process-01.png)

Luokittele käyttöomaisuuserä uudelleen noudattamalla seuraavia vaiheita:

1. Valitse **Käyttöomaisuus > Kausittaiset tehtävät > Uudelleenluokittelu.**
2. Valitse **Käyttöomaisuusryhmä**-kentässä uudelleenluokiteltava ryhmä.
3. Valitse **Käyttöomaisuuserän numero** -kentässä uudelleen luokiteltava käyttöomaisuuserä.
4. Valitse **Uusi käyttöomaisuuserä** -kentässä ryhmä, johon käyttöomaisuuserä siirretään.
    * Jos uusi käyttöomaisuusryhmä on liitetty numerosarjaan, **Uusi käyttöomaisuuserän numero** -kenttä päivitetään uuden käyttöomaisuuserän numerosarjan numerolla. Muussa tapauksessa **Uusi käyttöomaisuuserän numero** -kenttä päivitetään **Käyttöomaisuuserien parametrit** -sivulla määritetyn numerosarjan numerolla. Jos numerosarjaa ei ole määritetty **Käyttöomaisuuserien parametrit** -sivulla, anna numero **Uusi käyttöomaisuuserän numero** -kentässä.  
5. Anna **Uudelleenluokittelupäivä** -kentässä päivämäärä.
6. Anna tai valitse **Tositesarja**-kentässä arvo.
7. Valitse **OK**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
