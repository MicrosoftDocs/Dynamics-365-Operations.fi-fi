---
title: Määritä Lean-aikatauluryhmät
description: Lean-aikatauluryhmät on määritetty ryhmittelemään ja erottamaan kanban-ajoituksen tuotteet.
author: cvocph
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanScheduleGroup, GanttColorTableLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a9ad470d81d94a0af1c4c4dc6c5072354cfd96d2
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/10/2020
ms.locfileid: "3975845"
---
# <a name="define-lean-schedule-groups"></a>Määritä Lean-aikatauluryhmät

[!include [banner](../../includes/banner.md)]

Lean-aikatauluryhmät on määritetty ryhmittelemään ja erottamaan kanban-ajoituksen tuotteet. Ryhmittely voidaan tehdä yleisenä yrityskohtaisena liitoksena tai työsolukohtaisena liitoksena. Kullekin ryhmälle määritetään väri, jolla se tunnistetaan kanban-ajoituksen luettelosivulla. Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.


## <a name="define-lean-scheduling-group"></a>Määritä Lean-aikatauluryhmä
1. Valitse Tuotetietojen hallinta > Lean-valmistus > Lean-aikatauluryhmät.
2. Valitse Uusi.
3. Kirjoita arvo Aikatauluryhmä-kenttään.
    * Aikatauluryhmä voidaan määrittää yleisenä tai työsolukohtaisena ryhmänä. Tässä yksinkertaisessa esimerkissä määritetään yleinen ryhmä määrittää ja työsolu jää tyhjäksi. Tämän ryhmän asetuksia käytetään kaikissa työsoluissa, joille ei ole määritettyjä aikatauluryhmiä.  
4. Valitse väri värivalikoimasta.
    * Kanban-aikataulun luettelosivun tai kanban-prosessitaulun työt korostetaan värien avulla.  
5. Merkitse valittu rivi luettelossa.
6. Napsauta luettelossa valitulla rivillä olevaa linkkiä.

## <a name="associate-product"></a>Liitä tuote
1. Liitä tietty tuote
    * Tuotteet voidaan liittää Lean-aikatauluryhmään kahdella tavalla: kyse voi olla joko määritetystä tuotteesta (nimikkeen suhdetyyppi = nimike) tai tuotteet ovat osa nimikkeenkohdistustunnusta (nimikkeen suhdetyyppi = ryhmä).    
2. Valitse Nimikkeen suhdetyyppi -kentässä Nimike.
3. Kirjoita arvo Nimiketunnus-kenttään.
4. Lisää numero Tuotantokapasiteetin suhdeluku -kenttään.
    * Tuotantokapasiteetin oletusaste on 1, jolloin liittyvät tuotteet kuluttavat täsmälleen tuotantovirtojen prosessitehtävissä määritetyn kapasiteetin. Jos tuotantokapasiteettiaste on > 1, resursseja kulutetaan enemmän, ja jos tuotantokapasiteettiaste on < 1, resursseja kulutetaan vähemmän. Astetta käytetään kustannuslaskennassa ja kanban-työn kulutuksen laskennassa.  

## <a name="associate-item-allocation-key"></a>Liitä nimikkeen kohdistustunnus
1. Liitä nimikkeen kohdistustunnus.
    * Lisää liitos nimikkeenkohdistustunnukseen käyttämällä käyttäen nimikkeen suhdetyyppinä ryhmää.   Huomaa, että tätä prosessia varten tietoihin on määritettävä ennusteen nimikkeenkohdistustunnus.  
2. Valitse Nimikkeen suhdetyyppi -kentässä Ryhmä.
3. Avaa haku napsauttamalla Nimikkeenkohdistustunnus-kentässä avattavan valikon painiketta.
4. Napsauta luettelossa valitulla rivillä olevaa linkkiä.

