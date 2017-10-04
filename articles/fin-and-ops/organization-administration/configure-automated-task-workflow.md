---
title: "Automaattisen tehtävän määrittäminen työnkulkuun"
description: "Tässä ohjeaiheessa kerrotaan, miten automaattisen tehtävän ominaisuudet määritetään."
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 192061
ms.assetid: c0aceb57-b5e6-4ef3-91e7-89a21c9f048a
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 66f1b8e03cc0da5d21fea9b3c795d8f4097c8cfc
ms.contentlocale: fi-fi
ms.lasthandoff: 06/13/2017

---

# <a name="configure-an-automated-task-in-a-workflow"></a>Automaattisen tehtävän määrittäminen työnkulkuun

[!include[banner](../includes/banner.md)]


Tässä ohjeaiheessa kerrotaan, miten automaattisen tehtävän ominaisuudet määritetään.

Automaattinen tehtävä konfiguroidaan työnkulkueditorissa napsauttamalla tehtävää hiiren kakkospainikkeella ja valitsemalla **Ominaisuudet**, joka avaa **Ominaisuudet**-sivun. Sitten voit määrittää seuraavien ohjeiden avulla automaattisen tehtävän ominaisuudet.

## <a name="name-the-task"></a>Tehtävän nimeäminen
Kirjoita näiden ohjeiden avulla nimi automaattiselle tehtävälle.

1.  Napsauta vasemmassa ruudussa **Perusasetukset**.
2.  Kirjoita tehtävän yksilöivä nimi **Nimi**-kenttään.

## <a name="specify-when-notifications-are-sent"></a>Määritä, milloin ilmoitukset lähetetään
Voit lähettää käyttäjille ilmoituksia, kun automaattinen tehtävä on suoritettu tai peruutettu. Toimi seuraavasti määrittääksesi, milloin ilmoitukset lähetetään, ja kenelle ne lähetetään.

1.  Valitse vasemmasta ruudusta **Ilmoitukset**.
2.  Valitse tapahtuman vieressä oleva valintaruutu, jos haluat lähettää siihen liittyviä ilmoituksia:
    -   **Suoritus** – Ilmoitus lähetetään, kun tehtävä on suoritettu.
    -   **Peruutettu** – Ilmoitus lähetetään, kun tehtävä on peruutettu.

3.  Valitse sen tapahtuman rivi, jonka valitsit vaiheessa 2.
4.  Kirjoita **Ilmoitusteksti**-välilehden tekstiruutuun ilmoituksen leipäteksti.
5.  Voit mukauttaa ilmoitusta lisäämällä paikkamerkkejä. Kun käyttäjät tarkastelevat ilmoitusta, paikkamerkit korvataan asianmukaisilla tiedoilla. Paikkamerkkejä voit lisätä seuraavasti:
    1.  Napsauta tekstiruudussa kohtaa, johon haluat lisätä paikkamerkin.
    2.  Napsauta **Lisää paikkamerkki** -painiketta.
    3.  Valitse esiin tulevasta luettelosta lisättävä paikkamerkki.
    4.  Valitse **Lisää**.

6.  Ilmoitusten käännökset voit lisätä seuraavasti:
    1.  Napsauta **Käännökset**-painiketta.
    2.  Valitse esiin tulevalla sivulla **Lisää**.
    3.  Valitse esiin tulevasta luettelosta kieli, jolla kirjoitat tekstin.
    4.  Kirjota tekstisi **Käännetty teksti** -kenttään.
    5.  Voit mukauttaa tekstiä lisäämällä paikkamerkkejä vaiheen 5 mukaisesti.
    6.  Valitse **Sulje**.

7.  Valitse **Vastaanottaja**-välilehdellä käyttäjät, joille ilmoitukset lähetetään. Valitse jokin seuraavan taulukon vaihtoehdoista ja noudata vaihtoehdon toimia ennen siirtymistä vaiheeseen 8.
    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Vaihtoehto</th>
    <th>Ilmoituksen vastaanottajat</th>
    <th>Lisävaiheet</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>Osallistuja</td>
    <td>Käyttäjät, jotka on määritetty tiettyyn ryhmään tai rooliin</td>
    <td><ol>
    <li>Valittuasi <strong>osallistujan</strong>, valitse <strong>Rooliperustainen</strong>-välilehdellä <strong>Osallistujan tyyppi</strong> -luettelosta ryhmän tai roolin tyyppi, jolle ilmoituksia lähetetään.</li>
    <li>Valitse <strong>Osallistuja</strong>-luettelosta, ryhmä tai rooli, jolle ilmoituksia lähetetään.</li>
    </ol></td>
    </tr>
    <tr class="even">
    <td>Työnkulun käyttäjä</td>
    <td>Nykyiseen työnkulkuun osallistuvat käyttäjät</td>
    <td><ul>
    <li>Valittuasi <strong>työnkulun käyttäjän</strong>, valitse <strong>Työnkulun käyttäjä</strong> -välilehdessä <strong>Työnkulun käyttäjä</strong> -luettelosta käyttäjä, joka osallistuu työnkulun.</li>
    </ul></td>
    </tr>
    <tr class="odd">
    <td>Käyttäjä</td>
    <td>Tietyt Microsoft Dynamics 365 for Finance and Operations -käyttäjät</td>
    <td><ol>
    <li>Valittuasi <strong>käyttäjän</strong>, napsauta <strong>Käyttäjä</strong>-välilehteä.</li>
    <li><strong>Käytettävissä olevat käyttäjät</strong>: luettelo sisältää kaikki Finance and Operations -käyttäjät. Valitse käyttäjät, joille ilmoituksia lähetetään ja siirrä nämä käyttäjät <strong>Valitut käyttäjät</strong> -luetteloon.</li>
    </ol></td>
    </tr>
    </tbody>
    </table>

8.  Toista vaiheet 3-7 kullekin tapahtumalle, jonka valitsit vaiheessa 2.




