---
title: Toimitustavan muuttaminen myyntipisteessä
description: Tässä ohjeaiheessa kuvataan, miten voit määrittää ja käyttää myyntipisteen toimitustilan toimintoa.
author: hhainesms
manager: annbe
ms.date: 03/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: ''
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhainesms
ms.search.validFrom: 2020-02-20
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 26e798c664844b575de6f019ad8f5349ed92be98
ms.sourcegitcommit: 141e0239b6310ab4a6a775bc0997120c31634f79
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/10/2020
ms.locfileid: "3114401"
---
# <a name="change-mode-of-delivery-in-pos"></a>Toimitustavan muuttaminen myyntipisteessä

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Tässä ohjeaiheessa kerrotaan, miten myyntipisteympäristön toimitustilan muutostoiminto määritetään ja miten sitä käytetään. 

Dynamics 365 Commercen versiossa 10.0.10 ja myöhemmissä versioissa **Muuta toimitustilaa** -toiminto (647) on käytettävissä ja lisättävissä myyntipisteen näyttöjen asetteluihin.

Muuta toimitustilaa -toiminnon avulla voit muuttaa toimitustilaa yhdellä tai usealla lähetyksen määrittämällä myyntirivillä myyntipisteen tapahtumassa. Commercen edellisissä versioissa piti käyttää koko **Lähetä kaikki**- tai **Lähetä valitut** -konfigutointityönkulkuja, jos toimitustilaa haluttiin muuttaa lähetykselle määritetyllä olemassa olevalla rivillä. Tämä prosessi vei paljon aikaa ja tuloksena saattoi olla tahattomia muutoksia rivin toimituksen alkuperään tai toimituspäiviin. Uusi toiminto tarjoaa vaihtoehtoisen tavan näiden myyntirivien toimitustilan tehokkaaseen päivittämiseen.

Lisätietoja toiminnon lisäämisestä painikkeeseen myyntipisteen painikeruudukossa on kohdassa [Myyntipisteen näyttöjen asettelut](https://docs.microsoft.com/dynamics365/commerce/pos-screen-layouts).

Kun tämä toiminto on määritetty myyntipisteessä ja valitset **Muuta toimitustilaa**, näyttöön tulee luettelosivu, jonka avulla voit valita sen tapahtuman rivit, joiden toimitustilaa haluat muuttaa. Voit valita osan riveistä tai kaikki rivit tai poistua tekemättä muutoksia. Myyntirivit, jotka määritettiin aiemmin lähetykselle, ovat luettelon ainoat muutettavissa olevat rivit. Jos haluat muuttaa riviä, joka on määritetty keräykseen tai liikkeestä noudettavaksi, käytä **Lähetä kaikki**- tai **Lähetä valitut** -toimintoja. Vastaavasti jos haluat muuttaa riviä, joka on määritetty kerättäväksi tai liikkeestä noudettavaksi lähetykseksi, käytä **Kerää kaikki**-, **Kerää valitut**-, **Nouda kaikki**- tai **Nouda valitut** -toimintoja.

Kun olet valinnut muutettavan rivin, valitse **Muuta toimitustilaa**. Tällöin sinua pyydetään valitsemaan toimitustilavaihtoehdot. Jos valitsit useita muutettavia rivejä, myyntipiste näyttää vain toimitustilat, jotka on määritetty sallituksi kaikille valituille tuotteille. Toimitustilat voidaan määrittää tukemaan tiettyjä tuotteita ja toimitusosoitteita. Jos olemassa on toimitustila, joka on sallittu yhdelle tuotteen ja osoitteen yhdistelmälle, mutta ei toiselle valitun tuotteen ja osoitteen yhdistelmälle, toimitustila ei ole käytettävissä. Sinun on ehkä valittava rivit yksitellen ja muutettava toimitustila jokaiselle riville erikseen, jos haluat valita toimitustilan yhdelle tuotteelle, jota toinen tuote ei tue.  

Kun olet valinnut uuden toimitustilan, näkyviin tulee tapahtumasivu. Voit tarkistaa uudet toimitustilavalinnat valitsemalla tapahtumaluettelosta **Toimitus**-välilehden.   