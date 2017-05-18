---
title: "Rinnakkaisen tehtävän määrittäminen työnkulussa"
description: "Rinnakkaisen tehtävän määrittämiseksi pitää suorittaa seuraavat toiminnot työnkulun editorissa ."
author: sericks007
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 195753
ms.assetid: 6d0656df-b5af-4001-96e6-6f0fcc44d022
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: ce3fca9d2dbca046232365b1375bfd920d5b10fd
ms.contentlocale: fi-fi
ms.lasthandoff: 04/25/2017


---

# <a name="configure-a-parallel-activity-in-a-workflow"></a>Rinnakkaisen tehtävän määrittäminen työnkulussa

[!include[banner](../includes/banner.md)]


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
1.  Kaksoisnapsauttamalla rinnakkaista tehtävää saat näkyviin sen haarat.
2.  Lisää haara vetämällä **haara**-elementti **Työnkulkuelementit** alueesta alustan lisäyspisteeseen. Lisäyspiste näkyy seuraavassa kuvassa. ![Lisäyspiste](./media/workflow_insertionpoint.gif)
    | **Huomautus**                                                                                                         |
    |------------------------------------------------------------------------------------------------------------------|
    | Haarojen järjestyksellä ei ole merkitystä, koska rinnakkaisen tehtävän haarat suoritetaan samaan aikaan. |

3.  Lisätietoja haarojen määrittämisestä on kohdassa [Määritä rinnakkaishaara](configure-parallel-branch-workflow.md).






