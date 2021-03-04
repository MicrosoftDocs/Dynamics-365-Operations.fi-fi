---
title: ER Käytä vaakasuunnassa laajennettavia alueita sarakkeiden dynaamiseen lisäämiseen Excel-raportteihin (Osa 2 – Muodon suorittaminen)
description: Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooliin määritetty käyttäjä voi määrittää sähköisen raportoinnin (ER) muodon luomaan raportteja OPENXML-työkirjamuodossa (Excel), joissa pakolliset sarakkeet voi lyödä dynaamisesti vaakasuunnassa laajenevilla alueilla.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4596f7d7789ea44d49d7e7f273e4a52ee38dd90f
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684520"
---
# <a name="er-use-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports-part-2---run-format"></a>ER Käytä vaakasuunnassa laajennettavia alueita sarakkeiden dynaamiseen lisäämiseen Excel-raportteihin (Osa 2 – Muodon suorittaminen)

[!include [banner](../../includes/banner.md)]

Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooliin määritetty käyttäjä voi määrittää sähköisen raportoinnin (ER) muodon luomaan raportteja OPENXML-työkirjamuodossa (Excel), joissa pakolliset sarakkeet voi lyödä dynaamisesti vaakasuunnassa laajenevilla alueilla. Nämä vaiheet voidaan suorittaa DEMF-yrityksessä.

Näiden toimien suorittamisen edellytys on, että "ER Luo vaakasuunnassa laajennettavia alueita dynaamisten Excel-sarakkeiden luomista varten (osa 1: suunnittele muoto)" -menettelyn vaiheet on suoritettu.

Nämä ohjeet koskevat toimintoa, joka lisättiin Dynamics 365 for Operations -versiossa 1611.


## <a name="find-created-format"></a>Etsi luotu muoto
1. Valitse Organisaation hallinto > Sähköinen raportointi > Konfiguraatiot.
2. Laajenna puussa "Taloushallinnon dimensioiden esimerkkimalli".
3. Valitse puussa "Financial dimensions sample model\Sample report with horizontally expandable ranges".

## <a name="execute-format-to-create-excel-output"></a>Luo Excel-tuotos suorittamalla muoto
1. Valitse Suorita.
2. Kirjoita Dimension nimi -kenttään "BusinessUnit;CostCenter;Department".
    * Syötä tai valitse Dimension nimi -kentän arvo.  Jos haluat valita kaikki nykyisen yrityksen dimensiot, kirjoita seuraavat: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project  
3. Laajenna Tietueet-kohta ja sisällytä osaan.
4. Valitse Suodatin.
5. Valitse Kirjanpidon kirjauskansio -taulukon rivi ja Kirjauskansion eränumero -kenttä.
6. Syötä Ehdot-kenttään "00057..00058".
    * 00057..00058  
7. Valitse OK.
8. Valitse OK.
    * Tarkista aikaansaatu tuotos. Huomaa, että juuri luotu Excel-tiedosto sisältää saman määrän sarakkeita, jotka valittiin taloushallinnon dimensioille. Näiden sarakkeiden ylätunniste edustaa taloushallinnon dimensioiden nimiä. Näiden sarakkeiden tapahtumarivit edustavat taloushallinnon dimensioita. Aja raportti ja valitse eri dimensioita, jotta näet, että raportti ei ole riippuvainen valittujen dimensioiden määrästä tai tälle esiintymälle konfiguroitujen dimensioden määrästä.  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]