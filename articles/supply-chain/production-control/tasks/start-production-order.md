---
title: "Käynnistä tuotantotilaus"
description: "Tässä menettelyssä selvitetään, miten tuotantotilaus aloitetaan työnohjauksessa."
author: johanhoffmann
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: dadf0e87eac8522f61bb094c146e37f46a21fc09
ms.openlocfilehash: 3b5657e5eb2719702eae3a3c5178b3a04f7545e3
ms.contentlocale: fi-fi
ms.lasthandoff: 02/06/2018

---
# <a name="start-a-production-order"></a>Käynnistä tuotantotilaus

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tässä menettelyssä selvitetään, miten tuotantotilaus aloitetaan työnohjauksessa. Tämän prosessin ajan ja materiaalin kulutus raportoidaan. Tämän menettelyn luomisessa käytetty esittely-yritys on USMF. Tämä on viides seitsemästä tuotantotilauksen elinkaaresta kertovasta menettelystä.


## <a name="start-a-production-order"></a>Käynnistä tuotantotilaus
1. Siirry kohtaan Tuotannonhallinta > Tuotantotilaukset > Kaikki tuotantotilaukset.
    * Valitse tuotantotilaus, jonka tila on Vapautettu.  
2. Valitse toimintoruudussa Tuotantotilaus.
3. Valitse Käynnistys.
    * Voit vahvistaa tällä sivulla tuotantotilauksen alkamisen.  
4. Valitse Yleiset-välilehti.
5. Lisää Työvaiheen Nro -kenttään 10.
6. Valitse Automaattinen reitityksen kulutus -kentässä Aina.
7. Valitse Kirjaa reitityskortti nyt -valintaruutu.
8. Valitse Automaattinen tuoterakennekulutus -kentässä Aina.
9. Valitse Kirjaa keräysluettelo nyt -valintaruutu.
10. Valitse Tulosta keräysluettelo -valintaruutu.
11. Valitse OK.
    * Tämä tulostettu keräysluettelo sisältää tuotantotilauksessa käytetyt materiaalit.  
12. Sulje sivu.

## <a name="validate-the-picking-list"></a>Vahvista keräysluettelo.
1. Valitse toimintoruudussa Näytä.
2. Valitse Keräysluettelo.
3. Etsi haluamasi tietue luettelosta ja valitse se.
4. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
5. Valitse Muokkaa.
6. Lisää Kulutus-kenttään luku.
7. Valitse Kirjaa.
8. Valitse OK.
    * Tuotantotilauksen kuluttamat materiaalit kirjataan keräysluettelon kirjauskansioon. Voit tehdä ennen kirjauskansioon kirjausta oikaisuja, jos arvioidun määrän ja todellisen kulutetun määrän välillä on ero.  
9. Valitse Ruudukkoruutu-välilehti.
10. Sulje sivu.

## <a name="verify-the-route-card-journal"></a>Tarkista reitityskorttikirjauskansio
1. Valitse toimintoruudussa Näytä.
2. Valitse Reitityskortti.
3. Etsi haluamasi tietue luettelosta ja valitse se.
4. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
5. Valitse Muokkaa.
6. Lisää Tunnit-kenttään luku.
7. Valitse Kirjaa.
8. Valitse OK.
    * Yksittäisiin toimintoihin käytetty aika kirjataan reitityskorttikirjauskansioon Myös hyväksyttyjen ja virheellisten määrä voidaan raportoida.  

