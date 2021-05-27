---
title: Tuoterakennerivien materiaaliottosäännön asetuksia ei ole noudateta
description: Tuoterakennerivien materiaaliottosäännön asetuksia ei ole noudateta.
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: PurchTable,ProdParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 84a84728016119a2a02f59f6903171afbceb48e7
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026475"
---
# <a name="flushing-principle-settings-on-bom-lines-arent-respected"></a>Tuoterakennerivien materiaaliottosäännön asetuksia ei ole noudateta

Tietopankin numero: 4612725

## <a name="symptoms"></a>Oireet

Tämä ongelma ilmenee, kun **Automaattinen tuoterakennekulutus** -kenttä **Automaattinen päivitys** -välilehdellä **Tuotannonhallinnan parametrit** -sivulla määritetään arvoon *Materiaaliottosääntö*. Tämä asetus ilmaisee, että kaikki tuoterakennerivit tulee kuluttaa automaattisesti, kun ostotilaus vastaanotetaan. Jos tuoterakennerivien **Materiaaliottosääntö**-kentän arvoksi on nimenomaisesti määritetty *Manuaalinen*, voit odottaa, ettei tuoterakennerivejä kuluteta automaattisesti. Kuitenkin kun tämä ongelma ilmenee, tuoterakennerivit, joissa **Materiaaliottosääntö**-kentän arvoksi on määritetty *Manuaalinen*, kulutetaan automaattisesti joka tapauksessa.

## <a name="resolution"></a>Ratkaisu

Jos tämä ongelma ilmenee, tuotannonhallintaparametrit voidaan määrittää ohittamaan tuoterakennerivien **Materiaaliottosääntö**-asetus. Tarkista **Tuotannonhallinnan parametrit** -sivun **Automaattinen päivitys** -välilehdessä **Automaattinen tuoterakennekulutus** -arvo. Jos asetukseksi on määritetty *Aina*, järjestelmä ohittaa kaikkien tuoterakennerivien **Materiaaliottosääntö**-asetuksen ja tyhjentää rivit aina. Jos haluat, että järjestelmä noudattaa tuoterakennerivien **Materiaaliottosääntö**-asetusta, muuta **Automaattinen tuoterakennekulutus** -kentän arvoksi *Materiaaliottosääntö*.
