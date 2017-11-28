--- 
title: "Luokittele käyttöomaisuus uudelleen"
description: "Voit luokitella käyttöomaisuuserän uudelleen siirtämällä sen uuteen käyttöomaisuusryhmään tai määrittämällä sille uuden samaan ryhmään kuuluvan käyttöomaisuuserän numeron."
author: saraschi2
manager: AnnBe
ms.date: 10/30/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: cafd499e849570cae7b7f58bf2d487a7ac0093e6
ms.openlocfilehash: 6bce294329c7ec6dc436c3d3baf6597e0283c9bd
ms.contentlocale: fi-fi
ms.lasthandoff: 10/30/2017

---
# <a name="reclassify-fixed-assets"></a>Luokittele käyttöomaisuus uudelleen

[!include[task guide banner](../../includes/task-guide-banner.md)]

Voit luokitella käyttöomaisuuserän uudelleen siirtämällä sen uuteen käyttöomaisuusryhmään tai määrittämällä sille uuden samaan ryhmään kuuluvan käyttöomaisuuserän numeron. 

Kun käyttöomaisuuserä luokitellaan uudelleen:

• Kaikki aiemman käyttöomaisuuserän arvomallit luodaan myös uudelle käyttöomaisuuserälle. Alkuperäiselle käyttöomaisuuserälle mahdollisesti määritetyt tiedot kopioidaan uuteen käyttöomaisuuserään. Alkuperäisen käyttöomaisuuserän tila on Suljettu. 

• Uuden käyttöomaisuuserän arvomalleissa on uudelleenluokittelupäivä Hankintapäivämäärä-kentässä. Poiston suorituspäivä -kenttä kopioidaan alkuperäisen käyttöomaisuuden tiedoista. Jos poistot on jo aloitettu, Viimeisen poiston suorituspäivä -kentässä näkyy uudelleenluokittelun päivämäärä. 

• Alkuperäisen käyttöomaisuuserän aiemmin luodut käyttöomaisuustapahtumat peruutetaan ja luodaan uudelleen uudelle käyttöomaisuuserälle.

1. Valitse Käyttöomaisuus > Kausittaiset tehtävät > Uudelleenluokittelu.
2. Valitse Käyttöomaisuusryhmä-kentässä uudelleenluokiteltava ryhmä.
3. Valitse Käyttöomaisuuserän numero -kentässä uudelleen luokiteltava käyttöomaisuuserä.
4. Valitse Uusi käyttöomaisuuserä -kentässä ryhmä, johon käyttöomaisuuserä siirretään.
    * Jos uusi käyttöomaisuusryhmä on liitetty numerosarjaan, Uusi käyttöomaisuuserän numero -kenttä päivitetään uuden käyttöomaisuuserän numerosarjan numerolla. Muussa tapauksessa Uusi käyttöomaisuuserän numero -kenttä päivitetään Käyttöomaisuuserien parametrit -sivulla määritetyn numerosarjan numerolla. Jos numerosarjaa ei ole määritetty Käyttöomaisuuserien parametrit -sivulla, anna numero Uusi käyttöomaisuuserän numero -kentässä.  
5. Anna Uudelleenluokittelupäivä-kentässä päivämäärä.
6. Anna tai valitse Tositesarja-kentässä arvo.
7. Valitse OK.


