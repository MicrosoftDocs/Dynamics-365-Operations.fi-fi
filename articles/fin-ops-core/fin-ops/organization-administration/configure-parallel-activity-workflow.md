---
title: Rinnakkaisten tehtävien määrittäminen työnkulussa
description: Rinnakkaisen tehtävän määrittämiseksi pitää suorittaa seuraavat toiminnot työnkulun editorissa .
author: ChrisGarty
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 195753
ms.assetid: 6d0656df-b5af-4001-96e6-6f0fcc44d022
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 450420d44ad4aab233afc5a116369e993aa7a15b
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570611"
---
# <a name="configure-parallel-activities-in-a-workflow"></a>Rinnakkaisten tehtävien määrittäminen työnkulussa

[!include [banner](../includes/banner.md)]

Rinnakkaisen tehtävän määrittämiseksi pitää suorittaa seuraavat toiminnot työnkulun editorissa .

Rinnakkainen tehtävä sisältää työnkulun haarat, jotka suoritetaan samaan aikaan.

## <a name="name-a-parallel-activity"></a>Nimeä rinnakkainen tehtävä

Kirjoita näiden ohjeiden avulla nimi rinnakkaiselle tehtävälle.

1. Napsauta rinnakkaista tehtävää hiiren kakkospainikkeella ja valitse sitten **Ominaisuudet**, joka avaa **Ominaisuudet** -lomakkeen.
2. Napsauta vasemmassa ruudussa **Perusasetukset**.
3. Kirjoita rinnakkaisen tehtävän yksilöivä nimi **Nimi**-kenttään.
4. Valitse **Sulje**.

## <a name="configure-the-branches-of-a-parallel-activity"></a>Määritä rinnakkaisen tehtävän haarat

Voit lisätä ja konfiguroida rinnakkaisen tehtävän haaroja seuraavasti.

1. Kaksoisnapsauttamalla rinnakkaista tehtävää saat näkyviin sen haarat.
2. Lisää haara vetämällä **haara**-elementti **Työnkulkuelementit** alueesta alustan lisäyspisteeseen. Lisäyspiste näkyy seuraavassa kuvassa.

    ![Lisäyspiste](./media/workflow_insertionpoint.gif)

    > [!NOTE]
    > Haarojen järjestyksellä ei ole merkitystä, koska rinnakkaisen tehtävän haarat suoritetaan samaan aikaan.

3. Lisätietoja haarojen määrittämisestä on kohdassa [Työnkulun rinnakkaishaarojen määrittäminen](configure-parallel-branch-workflow.md).


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]