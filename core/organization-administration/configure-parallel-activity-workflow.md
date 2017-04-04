---
title: "Rinnakkainen tehtävä työnkulun määrittäminen"
description: "Rinnakkaisen tehtävän määrittämiseksi pitää suorittaa seuraavat toiminnot työnkulun editorissa ."
author: sericks007
manager: AnnBe
ms.date: 2017-04-04
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
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 818fb054742b935d002a7341e54a37eca0bb4761
ms.lasthandoff: 03/31/2017


---

# <a name="configure-a-parallel-activity-in-a-workflow"></a>Rinnakkainen tehtävä työnkulun määrittäminen

Rinnakkaisen tehtävän määrittämiseksi pitää suorittaa seuraavat toiminnot työnkulun editorissa .

Rinnakkainen tehtävä sisältää työnkulun haarat, jotka suoritetaan samaan aikaan.

## <a name="name-a-parallel-activity"></a>Nimeä rinnakkainen tehtävä
Kirjoita näiden ohjeiden avulla nimi rinnakkaiselle tehtävälle.
1.  Rinnakkaiselle tehtävälle hiiren kakkospainikkeella ja valitse sitten **ominaisuudet** avaamiseen **ominaisuudet** muodossa.
2.  Napsauta vasemmassa ruudussa **Perusasetukset**.
3.  Kirjoita rinnakkaisen tehtävän yksilöivä nimi **Nimi**-kenttään.
4.  Valitse **Sulje**.

## <a name="configure-the-branches-of-a-parallel-activity"></a>Määritä rinnakkaisen tehtävän haarat
Voit lisätä ja konfiguroida rinnakkaisen tehtävän haaroja seuraavasti.
1.  Kaksoisnapsauttamalla rinnakkaista tehtävää saat näkyviin sen haarat.
2.  Lisää haara vetämällä **haara**-elementti **Työnkulkuelementit** alueesta alustan lisäyspisteeseen. Lisäyspiste näkyy seuraavassa kuvassa. ![Lisäyspiste](./media/workflow_insertionpoint.gif)
    | **Huomautus **                                                                                                         |
    |------------------------------------------------------------------------------------------------------------------|
    | Haarojen järjestyksellä ei ole merkitystä, koska rinnakkaisen tehtävän haarat suoritetaan samaan aikaan. |

3.  Lisätietoja haarojen määrittämisestä on kohdassa [Määritä rinnakkaishaara](http://axhelp.dynamics.com/en/wiki/configure-a-parallel-branch/).




