---
title: "Rinnakkaisten tehtävien määrittäminen työnkulussa"
description: "Rinnakkaisen tehtävän määrittämiseksi pitää suorittaa seuraavat toiminnot työnkulun editorissa ."
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195753
ms.assetid: 6d0656df-b5af-4001-96e6-6f0fcc44d022
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 764d4c9049d94ebcd55c61654aa2f4133b35bae6
ms.openlocfilehash: 64cd387f8a6ab693d159cd659fca51fa6568ee39
ms.contentlocale: fi-fi
ms.lasthandoff: 08/08/2018

---

# <a name="configure-parallel-activities-in-a-workflow"></a>Rinnakkaisten tehtävien määrittäminen työnkulussa

[!include [banner](../includes/banner.md)]

Rinnakkaisen tehtävän määrittämiseksi pitää suorittaa seuraavat toiminnot työnkulun editorissa .

Rinnakkainen tehtävä sisältää työnkulun haarat, jotka suoritetaan samaan aikaan.

## <a name="name-a-parallel-activity"></a>Nimeä rinnakkainen tehtävä
Kirjoita näiden ohjeiden avulla nimi rinnakkaiselle tehtävälle.
1.  Napsauta rinnakkaista tehtävää hiiren kakkospainikkeella ja valitse sitten **Ominaisuudet**, joka avaa **Ominaisuudet** -lomakkeen.
2.  Napsauta vasemmassa ruudussa **Perusasetukset**.
3.  Kirjoita rinnakkaisen tehtävän yksilöivä nimi **Nimi**-kenttään.
4.  Valitse **Sulje**.

## <a name="configure-the-branches-of-a-parallel-activity"></a>Määritä rinnakkaisen tehtävän haarat
Voit lisätä ja konfiguroida rinnakkaisen tehtävän haaroja seuraavasti.
1. Kaksoisnapsauttamalla rinnakkaista tehtävää saat näkyviin sen haarat.
2. Lisää haara vetämällä **haara**-elementti **Työnkulkuelementit** alueesta alustan lisäyspisteeseen. Lisäyspiste näkyy seuraavassa kuvassa. ![Lisäyspiste](./media/workflow_insertionpoint.gif)

   |                                              <strong>Huomautus</strong>                                               |
   |------------------------------------------------------------------------------------------------------------------|
   | Haarojen järjestyksellä ei ole merkitystä, koska rinnakkaisen tehtävän haarat suoritetaan samaan aikaan. |


3. Lisätietoja haarojen määrittämisestä on kohdassa [Määritä rinnakkaishaara](configure-parallel-branch-workflow.md).






