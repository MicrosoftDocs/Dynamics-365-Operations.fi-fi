---
title: Toimitustavan muuttaminen myyntipisteessä
description: Tässä artikkelissa kuvataan, miten voit määrittää ja käyttää myyntipisteen toimitustilan toimintoa.
author: hhainesms
ms.date: 03/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhaines
ms.search.validFrom: 2020-02-20
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 583f568164d0de70e22998bf5ded5f4616b00bd2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8855818"
---
# <a name="change-mode-of-delivery-in-pos"></a>Toimitustavan muuttaminen myyntipisteessä

[!include [banner](includes/banner.md)]

Tässä artikkelissa kerrotaan, miten myyntipisteympäristön toimitustilan muutostoiminto määritetään ja miten sitä käytetään. 

Dynamics 365 Commercen versiossa 10.0.10 ja myöhemmissä versioissa **Muuta toimitustilaa** -toiminto (647) on käytettävissä ja lisättävissä myyntipisteen näyttöjen asetteluihin.

Muuta toimitustilaa -toiminnon avulla voit muuttaa toimitustilaa yhdellä tai usealla lähetyksen määrittämällä myyntirivillä myyntipisteen tapahtumassa. Commercen edellisissä versioissa piti käyttää koko **Lähetä kaikki**- tai **Lähetä valitut** -konfigutointityönkulkuja, jos toimitustilaa haluttiin muuttaa lähetykselle määritetyllä olemassa olevalla rivillä. Tämä prosessi vei paljon aikaa ja tuloksena saattoi olla tahattomia muutoksia rivin toimituksen alkuperään tai toimituspäiviin. Uusi toiminto tarjoaa vaihtoehtoisen tavan näiden myyntirivien toimitustilan tehokkaaseen päivittämiseen.

Lisätietoja toiminnon lisäämisestä painikkeeseen myyntipisteen painikeruudukossa on kohdassa [Myyntipisteen näyttöjen asettelut](pos-screen-layouts.md).

Kun tämä toiminto on määritetty myyntipisteessä ja valitset **Muuta toimitustilaa**, näyttöön tulee luettelosivu, jonka avulla voit valita sen tapahtuman rivit, joiden toimitustilaa haluat muuttaa. Voit valita osan riveistä tai kaikki rivit tai poistua tekemättä muutoksia. Myyntirivit, jotka määritettiin aiemmin lähetykselle, ovat luettelon ainoat muutettavissa olevat rivit. Jos haluat muuttaa riviä, joka on määritetty keräykseen tai liikkeestä noudettavaksi, käytä **Lähetä kaikki**- tai **Lähetä valitut** -toimintoja. Vastaavasti jos haluat muuttaa riviä, joka on määritetty kerättäväksi tai liikkeestä noudettavaksi lähetykseksi, käytä **Kerää kaikki**-, **Kerää valitut**-, **Nouda kaikki**- tai **Nouda valitut** -toimintoja.

Kun olet valinnut muutettavan rivin, valitse **Muuta toimitustilaa**. Tällöin sinua pyydetään valitsemaan toimitustilavaihtoehdot. Jos valitsit useita muutettavia rivejä, myyntipiste näyttää vain toimitustilat, jotka on määritetty sallituksi kaikille valituille tuotteille. Toimitustilat voidaan määrittää tukemaan tiettyjä tuotteita ja toimitusosoitteita. Jos olemassa on toimitustila, joka on sallittu yhdelle tuotteen ja osoitteen yhdistelmälle, mutta ei toiselle valitun tuotteen ja osoitteen yhdistelmälle, toimitustila ei ole käytettävissä. Sinun on ehkä valittava rivit yksitellen ja muutettava toimitustila jokaiselle riville erikseen, jos haluat valita toimitustilan yhdelle tuotteelle, jota toinen tuote ei tue.  

Kun olet valinnut uuden toimitustilan, näkyviin tulee tapahtumasivu. Voit tarkistaa uudet toimitustilavalinnat valitsemalla tapahtumaluettelosta **Toimitus**-välilehden.

## <a name="additional-resources"></a>Lisäresurssit

[Puhelinkeskustilausten luominen](tasks/create-call-center-orders.md)

[Tapahtumasähköpostien mukauttaminen toimitustilan mukaan](customize-email-delivery-mode.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]