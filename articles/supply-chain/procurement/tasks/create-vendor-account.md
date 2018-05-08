--- 
title: Toimittajatilin luominen
description: "Tässä menetelmässä selvitetään toimittajatili luominen sekä lisätään osoite- ja yhteystiedot."
author: mkirknel
manager: AnnBe
ms.date: 06/06/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 6ff2357d5266c45be2f403e463c72089d73db21b
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-vendor-account"></a>Toimittajatilin luominen

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tässä menetelmässä selvitetään toimittajatili luominen sekä lisätään osoite- ja yhteystiedot. Menettelyssä ei näytetä miten kaikki osto- ja rahoitustarkoitusten kentät täytetään. Kenttien kuvauksissa on lisätietoja kyseistä kentistä. Voit käyttää tätä menettelyä USMF-demoyrityksen tiedoilla tai omilla tiedoillasi. Yleensä hankinta-asiantuntija tai myyntireskontran henkilökunta luo toimittajatilit.


## <a name="create-a-vendor-account"></a>Toimittajatilin luominen
1. Valitse Hankinta > Toimittajat > Kaikki toimittajat.
2. Valitse Uusi.
3. Kirjoita arvo Toimittajan tili -kenttään.
    * Arvo voidaan lisätä automaattisesti. Siinä tapauksessa voit ohittaa tämän vaiheen.  
    * Toimittajatilin voi luoda henkilölle tai organisaatiolle. Käytettävissä olevat kentät määräytyvät tämän mukaan. Tässä esimerkissä luodaan organisaation toimittajatili.   
4. Syötä tai valitse arvo Nimi-kenttään.
    * Jos toimittaja jo rekisteröity osapuoleksi järjestelmään, voit valita toimittajan tässä kentässä vetämällä ja pudottamalla, jolloin uusi toimittajatili perii jo rekisteröidyn osoitteen ja yhteystiedot.  
5. Syötä tai valitse Ryhmä-kentän arvo.
    * Toimittajaryhmän avulla ryhmitetään toimittajat, joille jokin seuraavista parametreista on yhteinen: maksuehdot, selvityskausi, varastokirjauksen kirjanpitotilit – mukaan lukien arvonlisäveroryhmä, oletuskirjanpitotilit, tuotteen suodatinkoodit ja tarjontaennustemääritys.  
6. Täytä Työntekijämäärä-kenttään numero.
7. Kirjoita Organisaatiotunnus-kenttään arvo.

## <a name="add-an-address"></a>Lisää osoite
1. Laajenna osa Osoitteet.
2. ValitseLisää.
3. Syötä tai valitse Tarkoitus-kentän arvo.
    * Voit valita useita tarkoituksia. Näiden avulla voit valita tietylle tarkoitukselle oikean osoitteen. Esimerkiksi jos tarkoitus on "lasku", tätä osoitetta käytetään lähetettävissä laskuissa.  
4. Kirjoita Nimi tai kuvaus -kenttään arvo.
5. Syötä tai valitse arvo Maa/alue-kentässä.
    * Anna osoitetiedot. Valitsemasi maa tai alue määrittää näkyviin tulevat kentät, sillä ne vastaavat kyseisen maan tai alueen osoitemuotoa.   
6. Valitse OK.

## <a name="add-contact-information"></a>Lisää yhteystiedot
1. ValitseLisää.
2. Kirjoita arvo Kuvaus-kenttään.
3. Valitse vaihtoehto Tyyppi-kentässä.
4. Kirjoita arvo Yhteyshenkilön puhelinnumero/osoite -kenttään.
    * Valitse Ensisijainen-valintaruutu, jos tämä on yhteyshenkilön ensisijainen osoite.  
5. Valitse Tallenna.
6. Sulje sivu.
7. Sulje sivu.


