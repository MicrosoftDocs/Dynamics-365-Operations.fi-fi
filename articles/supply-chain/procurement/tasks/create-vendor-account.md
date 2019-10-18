---
title: Toimittajatilin luominen
description: Tässä menetelmässä selvitetään toimittajatili luominen sekä lisätään osoite- ja yhteystiedot.
author: mkirknel
manager: AnnBe
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, LogisticsPostalAddressGrid, DirPartyLookup, LogisticsPostalAddress, SysLookupMultiSelectGrid
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 116085a71e872c13bbf2820f4408e3c7d1261d17
ms.sourcegitcommit: 62d66f98d4bbf916e19184506b90055bb68d219f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/28/2019
ms.locfileid: "1924416"
---
# <a name="create-a-vendor-account"></a>Toimittajatilin luominen

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tässä menetelmässä selvitetään toimittajatili luominen sekä lisätään osoite- ja yhteystiedot. Menettelyssä ei näytetä miten kaikki osto- ja rahoitustarkoitusten kentät täytetään. Kenttien kuvauksissa on lisätietoja kyseistä kentistä. Voit käyttää tätä menettelyä USMF-demoyrityksen tiedoilla tai omilla tiedoillasi. Yleensä hankinta-asiantuntija tai myyntireskontran henkilökunta luo toimittajatilit.


## <a name="create-a-vendor-account"></a>Toimittajatilin luominen
1. Siirry kohtaan **siirtymisruutu > Moduulit > Hankinta > Toimittajat > Kaikki toimittajat**.
2. Valitse **Uusi**.
3. Kirjoita arvo **Toimittajan tili** -kenttään.
    - Arvo voidaan lisätä automaattisesti. Siinä tapauksessa voit ohittaa tämän vaiheen.  
    - Toimittajatilin voi luoda henkilölle tai organisaatiolle. Käytettävissä olevat kentät määräytyvät tämän mukaan. Tässä esimerkissä luodaan organisaation toimittajatili.   
4. Anna tai valitse arvo **Nimi**-kentässä. Jos toimittaja jo rekisteröity osapuoleksi järjestelmään, voit valita toimittajan tässä kentässä vetämällä ja pudottamalla, jolloin uusi toimittajatili perii jo rekisteröidyn osoitteen ja yhteystiedot.
5. Anna tai valitse arvo **Ryhmä**-kentässä. Toimittajaryhmän avulla ryhmitetään toimittajat, joille jokin seuraavista parametreista on yhteinen: maksuehdot, selvityskausi, varastokirjauksen kirjanpitotilit – mukaan lukien arvonlisäveroryhmä, oletuskirjanpitotilit, tuotteen suodatinkoodit ja tarjontaennustemääritys.
6. Anna **Työntekijämäärä**-kentässä numero.
7. Kirjoita **Organisaatiotunnus**-kenttään arvo.

## <a name="add-an-address"></a>Lisää osoite
1. Laajenna **Osoitteet**-osa.
2. Valitse **Lisää**.
3. Anna tai valitse arvo **Tarkoitus**-kentässä. Voit valita useita tarkoituksia. Näiden avulla voit valita tietylle tarkoitukselle oikean osoitteen. Esimerkiksi jos tarkoitus on "lasku", tätä osoitetta käytetään lähetettävissä laskuissa.
4. Kirjoita **Nimi tai kuvaus** -kenttään arvo.
5. Syötä tai valitse arvo **Maa/alue**-kentässä. Anna osoitetiedot. Valitsemasi maa tai alue määrittää näkyviin tulevat kentät, sillä ne vastaavat kyseisen maan tai alueen osoitemuotoa. 
6. Valitse **OK**.

## <a name="add-contact-information"></a>Lisää yhteystiedot
1. Laajenna **Yhteystiedot**-osa.
2. Valitse **Lisää**.
3. Kirjoita **Kuvaus**-kenttään arvo.
4. Valitse vaihtoehto **Tyyppi**-kentässä.
5. Kirjoita arvo **Yhteyshenkilön puhelinnumero/osoite** -kenttään. Valitse Ensisijainen-valintaruutu, jos tämä on yhteyshenkilön ensisijainen osoite.  
6. Valitse **Tallenna**.
7. Sulje sivu.
8. Sulje sivu.

