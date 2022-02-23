---
title: ER Taloushallinnon dimensioiden käyttö tietolähteenä (Osa 4 – Raportin suorittaminen)
description: Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooliin määritetty käyttäjä voi konfiguroida sähköisen raportoinnin (ER) tietomallin käyttämään taloushallinnon dimensioita tietolähteenä ER-raporteissa.
author: NickSelin
manager: AnnBe
ms.date: 05/27/2020
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
ms.openlocfilehash: fb7f49310aa25ff7c17ab4bcd50e1842be84fe2d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684736"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-4---run-the-report"></a>ER Taloushallinnon dimensioiden käyttö tietolähteenä (Osa 4 – Raportin suorittaminen)

[!include [banner](../../includes/banner.md)]

Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooliin määritetty käyttäjä voi konfiguroida sähköisen raportoinnin (ER) tietomallin käyttämään taloushallinnon dimensioita tietolähteenä ER-raporteissa. Nämä vaiheet voidaan suorittaa DEMF-yrityksessä.

Jotta voisit suorittaa nämä vaiheet, "ER Taloushallinnon dimensioiden käyttäminen tietolähteenä (Osa 3: raportin suunnittelu)" -menettelyn vaiheiden on oltava suoritettuna. Sähköisen raportoinnin parametrit -sivulla on myös määritettävä asiakirjojen oletustyypit. Asiakirjojen oletustyypit asetetaan myös, kun lataat ja tuot ER-kokoonpanon. 


## <a name="run-report"></a>Aja raportti
1. Valitse Organisaation hallinto > Sähköinen raportointi > Konfiguraatiot.
2. Laajenna puussa "Taloushallinnon dimensioiden esimerkkimalli".
3. Valitse puussa "Taloushallinnon dimensioiden esimerkkimalli\Kirjanpitokansion raportti".
4. Valitse Suorita.
![Sähköisen raportoinnin konfiguroinnit -sivu](../media/er-financial-dimensions-guides-run1.png)
5. Syötä tai valitse Dimension nimi -kentän arvo.
    * Jos haluat valita kaikki nykyisen yrityksen dimensiot, kirjoita seuraavat tiedot: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project  
![Sähköisen raportoinnin konfiguroinnit -sivu](../media/er-financial-dimensions-guides-run2.png)
6. Laajenna Tietueet-kohta ja sisällytä osaan.
7. Valitse Suodatin.
8. Valitse Kirjanpidon kirjauskansio -taulukon rivi ja Kirjauskansion eränumero -kenttä.
9. Kirjoita Ehdot-kenttään 00057.
10. Valitse OK.
11. Valitse OK.
![Sähköisen raportoinnin konfiguroinnit -sivu](../media/er-financial-dimensions-guides-run3.png)
    * Tarkista aikaansaatu tuotos. Jokaiselle valitun erän tapahtumalle esitetään vastaavan dimensiojoukon taloushallinnon dimensiot. Aja raportti ja valitse eri dimensioita, jotta näet, että raportti ei ole riippuvainen valittujen dimensioiden määrästä tai tälle esiintymälle konfiguroitujen dimensioden määrästä.  
![Sähköisen raportoinnin konfiguroinnit -sivu](../media/er-financial-dimensions-guides-run4.png)
