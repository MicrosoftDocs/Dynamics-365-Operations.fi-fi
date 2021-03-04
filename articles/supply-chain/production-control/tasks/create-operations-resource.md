---
title: Luo operatiivinen resurssi
description: Operatiivinen resurssi suorittaa projektin tai tuotantoprosessin aktiviteetit.
author: sorenva
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WrkCtrTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e2e59b1e6a83d902df98a0b40ee6c572a6567f05
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426791"
---
# <a name="create-an-operations-resource"></a>Luo operatiivinen resurssi

[!include [banner](../../includes/banner.md)]

Operatiivinen resurssi suorittaa projektin tai tuotantoprosessin aktiviteetit. Tässä menettelyssä kerrotaan, miten operatiivinen resurssi määritetään. Voit käydä tämän menettelyn läpi emotietojen yrityksen USMF avulla tai käyttää omia tietojasi.

1. Siirry Resurssit-kohtaan.
2. Valitse Uusi.
3. Kirjoita arvo Resurssi-kenttään.
4. Kirjoita arvo Kuvaus-kenttään.

## <a name="define-capacity-and-consumption-parameters"></a>Kapasiteetin ja kulutuksen parametrien määrittäminen
1. Laajenna Työvaihe-osa.
2. Syötä numero Hävikkiprosentti-kenttään.
3. Syötä tai valitse arvo Asetusluokka-kenttään.
    * Määritä kustannusluokka, joka määrittää asetusten kustannusten tilitystavan.  
4. Syötä tai valitse arvo Ajoaikaluokka-kenttään.
    * Määritä kustannusluokka, joka määrittää ajoajan kustannusten tilitystavan.  
5. Syötä tai valitse arvo Määrä-kenttään.
    * Määritä kustannusluokka, joka määrittää tuotoksen määrään perustuvan resurssikustannusten tilitystavan.  
6. Valitse Kapasiteettiyksikkö-kentässä vaihtoehto.
    * Määritä yksikkö, jossa operatiivisen resurssin kapasiteetti ilmoitetaan.  
7. Syötä Kapasiteetti-kenttään numero.
8. Syötä Tehokkuusprosentti-kenttään numero.
    * Määritä operatiiviselta resurssilta odotettava tehokkuus. Tehokkuusprosentti muokkaa operatiivisen resurssin tuotantokapasiteettia ja vaikuttaa resurssille varattavaan aikaan.  
9. Syötä numero Työvaiheen karkeasuunnittelun prosenttiosuus -kenttään.
    * Määritä työvaiheiden ajoituksessa käytettävän operatiivisen resurssin kapasiteetin enimmäisprosentti.  
10. Valitse Rajallinen kapasiteetti -kentässä Kyllä.
    * Määritä tämän vaihtoehdon arvoksi Kyllä, jos operatiivinen resurssi tulee ajoittaa käytettävissä olevan toteutuneen kapasiteetin perusteella ja aiemmin määritetyt kapasiteettivaraukset tulee ottaa huomioon. Jos tämän asetuksen arvoksi on määritetty Ei, operatiivisella resurssin kapasiteetin oletetaan olevan rajaton, ja resurssi saatetaan ylivarata.  
11. Valitse Pullonkaularesurssi-kentässä Kyllä.

## <a name="define-working-times"></a>Työaikojen määrittäminen
1. Laajenna Kalenterit-osa.
2. ValitseLisää.
3. Syötä tai valitse arvo Kalenteri-kenttään.
    * Määritä työaikakalenteri, joka määrittää resurssin kapasiteetin (tunteina).  
4. Etsi haluamasi tietue luettelosta ja valitse se.
5. Napsauta luettelossa valitulla rivillä olevaa linkkiä.

## <a name="define-resource-capabilities"></a>Määritä resurssin ominaisuudet
1. Laajenna Ominaisuudet-osa.
2. ValitseLisää.
    * Toiminto on operatiivisen resurssin kyky suorittaa tietty aktiviteetti. Ajoitusmoduuli kohdistaa resurssit kohdistamalla kunkin aktiviteetin resurssivaatimukset käytettävissä olevien operatiivisten resurssien ominaisuuksiin.  
3. Syötä tai valitse arvo Ominaisuus-kenttään.
4. Syötä numero Taso-kenttään.
    * Määritä pätevyystaso, jonka mukaan resurssi käsittelee ominaisuuden.  
5. Syötä numero Prioriteetti-kenttään.
    * Määritä ominaisuuteen liittyvä operatiivisen resurssin prioriteetti. Kun ajoitus tehdään prioriteetin mukaan, ensimmäiseksi valitaan korkeimman prioriteetin omaava operatiivinen resurssi (pienin numeerinen arvo).  

## <a name="assign-resource-to-resource-group"></a>Resurssin määrittäminen resurssiryhmään
1. Laajenna Resurssiryhmät-osa.
2. ValitseLisää.
    * Resurssiryhmä määrittää operatiivisten resurssien toimipaikan, tuotantoyksikön ja varaston kontekstin. Operatiivinen resurssi voidaan ajoittaa vain, kun se on määritetty resurssiryhmään. Ajoitus voidaan tehdä vain resurssiryhmän toimipaikassa.  
3. Syötä tai valitse arvo Resurssiryhmä-kenttään.
4. Syötä tai valitse arvo Syötön sijainti -kenttään.
    * Määritä varaston sijainti, josta operatiivinen resurssi käyttää materiaaleja.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]