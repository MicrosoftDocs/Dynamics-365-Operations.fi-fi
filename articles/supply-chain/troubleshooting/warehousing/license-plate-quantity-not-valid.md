---
title: Määrä ei ole kelvollinen saapuvien tilausten rekisteröinnissä
description: Jos rekisterikilvelle määritetty määrä ylittää määrän, joka on vielä vastaanotettava, näyttöön tulee virhesanoma "Määrä ei ole kelvollinen".
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 5099b320447bf59c72f5017564ea660f19c690a5
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476268"
---
# <a name="license-plate-quantity-is-not-valid-when-registering-inbound-orders"></a>Rekisterikilven määrä ei ole kelvollinen rekisteröitäessä tulevia tilauksia

## <a name="symptoms"></a>Oireet

Kun rekisteröit saapuvia tilauksia, näyttöön voi tulla seuraava virhesanoma:

> Määrä ei kelpaa.

Jos saapuvien tilausten rekisteröimiseen käytettävässä mobiililaitteen valikkokohteessa on määritetty **rekisterikilpien ryhmittelykäytäntö** -kentän arvoksi *Käyttäjän määrittämä*, näkyviin tulee virhe, etkä voi tehdä rekisteröintiä valmiiksi.

## <a name="cause"></a>Syy

Kun *Käyttäjän määrittämä* -arvoa käytetään rekisterikilpien ryhmittelykäytäntönä, järjestelmä jakaa saapuvan varaston erillisiksi rekisterikilviksi, kuten yksikköjärjestysryhmä määrittää. Jos vastaanotettavan nimikkeen jäljittämiseen käytetään erä- tai sarjanumeroita, kunkin erän tai sarja määrät on määritettävä rekisteröityä rekisterikilpeä kohden. Jos rekisterikilvelle määritetty määrä ylittää määrän, joka on vielä vastaanotettava nykyisille dimensioille, näyttöön tulee virhesanoma.

## <a name="resolution"></a>Ratkaisu

Kun rekisteröit nimikkeen käyttämällä kannettavan laitteen valikkonimikettä, jossa **Rekisterikilpien ryhmittelykäytäntö** -kentän arvoksi on määritetty *Käyttäjän määrittämä*, järjestelmä saattaa edellyttää, että vahvistat tai määrität rekisterikilpinumerot, eränumerot tai sarjanumerot.

Järjestelmä näyttää rekisterikilven vahvistussivulla määrän, joka on varattu nykyiselle rekisterikilvelle. Järjestelmä näyttää erä- tai sarjavahvistussivuilla määrän, joka on edelleen vastaanotettava nykyiselle rekisterikilvelle. Siihen sisältyy myös kenttä, johon voit syöttää rekisteröitävän määrän tätä rekisterikilven ja erä- tai sarjanumeron yhdistelmää varten. Varmista tässä tapauksessa, että rekisterikilvelle rekisteröitävä määrä ei ylitä vielä vastaanotettavaa määrää.

Vaihtoehtoisesti, jos saapuvan tilauksen rekisteröinnissä luodaan liian monta rekisterikilpeä, **Rekisterikilpien ryhmittelykäytäntö** -kentän arvoksi voidaan muuttaa *Rekisterikilpien ryhmittely*, nimikkeelle voi määrittää uuden yksikköjärjestysryhmän tai yksikköjärjestysryhmän **Rekisterikilpien ryhmittely** -vaihtoehdon aktivointi voidaan poistaa käytöstä.
