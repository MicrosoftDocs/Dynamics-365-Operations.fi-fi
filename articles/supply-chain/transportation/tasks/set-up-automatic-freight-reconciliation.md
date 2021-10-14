---
title: Rahdin automaattisen täsmäytyksen määrittäminen
description: Tässä menettelyssä kuvataan, miten automaattisen rahdintäsmäytyksen tiedot määritetään.
author: Henrikan
ms.date: 10/16/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TMSFreightBillType, TMSFreightBillTypeAssignment, TMSCarrierCodeLookup, DefaultDashboard, TMSAuditMaster
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d1dbe3c683d869f86bc7231c68839f431cc61d6b
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/29/2021
ms.locfileid: "7574830"
---
# <a name="set-up-automatic-freight-reconciliation"></a>Rahdin automaattisen täsmäytyksen määrittäminen

[!include [banner](../../includes/banner.md)]

Tässä menettelyssä kuvataan, miten automaattisen rahdintäsmäytyksen tiedot määritetään. Yleensä tämän prosessin tekee varastopäällikkö. Voit käyttää tätä menettelyä esittely-yrityksessä USMF.


## <a name="set-up-the-freight-bill-type"></a>Määritä rahtilaskun tyyppi
1. Siirry kohtaan Kuljetustenhallinta > Asetukset > Rahdin täsmäytys > Rahtilaskun tyyppi.
    * Rahtilaskun tyyppi määrittää, miten rahtilaskut ja kuljettajan laskut täsmäytetään.  
2. Valitse Uusi.
3. Kirjoita arvo Rahtilaskun tyyppi -kenttään.
4. Kirjoita Laskennan kokoonpano -kenttään Microsoft.Dynamics.Ax.Tms.dll.
    * Tämä on standardi Kuljetuksenhallinnan kohdistusmoduulin koodikirjasto.  
5. Kirjoita Moduulin luokka -kenttään Microsoft.Dynamics.Ax.Tms.Bll.GenericNormalizer.
    * Tämä on standardi Kuljetuksenhallinnan kohdistusmoduulin luokka.  
6. Valitse Uusi.
7. Valitse kuvaus-kenttään arvo, jonka tulee täsmätä sekä rahti- että kuljettajan laskulla.  
8. Valitse Täsmäytys vaaditaan -kentässä Kyllä.
    * Jos määrität tämän kentän arvoksi Kyllä, se tarkoittaa, että Kuvaus-kenttään valitun arvon on vastattava sekä rahtikirjaa että kuljettajan laskua. Jos asetat arvoksi Ei, toinen näistä kentistä voi olla tyhjä.  
9. Valitse Tallenna.

## <a name="set-up-the-freight-bill-type-assignment"></a>Aseta rahtilaskun määritys
1. Sulje sivu.
2. Siirry kohtaan Kuljetustenhallinta > Asetukset > Rahdin täsmäytys > Rahtilaskun tyyppimääritykset.
    * Rahtilaskun tyyppimääritystä käytetään tietyn kuljettajan rahtilaskutyypin määrittämiseen.   
3. Valitse Uusi.
4. Syötä tai valitse arvo Menetelmä-kentässä.
5. Syötä tai valitse arvo Lähetyksen rahdinkuljettaja -kentässä.
6. Valitse Rahtilaskun tyyppi -kentässä aiemmin luomasi rahtilaskun tyyppi.
7. Sulje sivu.

## <a name="set-up-the-audit-master"></a>Aseta päätarkastus
1. Siirry kohtaan Kuljetustenhallinta > Asetukset > Rahdin täsmäytys > Päätarkistus.
    * Päätarkistuksessa määritetään automaattisen rahtitäsmäytyksen toleranssitaso. Se määrittää kuinka paljon rahtilasku ja kuljettajan laskun rahasummat voivat poiketa toisistaan, että täsmäytys on edelleen sallittua. Se määrittää myös, miten ristiriidat käsitellään.  
2. Valitse Uusi.
3. Kirjoita arvo Tarkistuksen päätunnus -kenttään.
4. Valitse Lähetyksen rahdinkuljettaja -kenttään saman lähetyksen rahdinkuljettaja, jonka valitsit aikaisemmin.
5. Valitse Rahtilaskun tyyppi -kentässä aiemmin luomasi rahtilaskun tyyppi.
6. Laajenna Toleranssi-osa.
7. Syötä Vähimmäistoleranssitaso-kenttään numero.
8. Syötä Enimmäistoleranssitaso-kenttään numero.
9. Laajenna Tulos-osa.
10. Anna tai valitse Liikamaksun syykoodi -kentässä arvo.
    * Jos rahtilaskun ja kuljettajan laskun rahasummat eroavat toisistaan, liika- ja alimaksujen syykoodit määrittävät tilit, joille ero tulisi kirjata, kunhan ero on toleranssitasojen puitteissa.  
11. Anna tai valitse Alimaksun syykoodi -kentässä arvo.
12. Sulje sivu.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]