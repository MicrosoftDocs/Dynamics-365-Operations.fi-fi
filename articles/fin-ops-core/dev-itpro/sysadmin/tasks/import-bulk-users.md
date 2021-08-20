---
title: Tuo käyttäjiä Azure Active Directorysta
description: Näiden ohjeiden avulla järjestelmänvalvoja voi tuoda manuaalisesti valitut käyttäjät tai suuren määrän käyttäjiä Azure Active Directorysta.
author: peakerbl
ms.date: 07/07/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ce8c98add0c6d5fb07b3ba5338037d9a12b1d8e50a2d2039b0231d3d305c9ebe
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6748285"
---
# <a name="import-users-from-azure-active-directory"></a>Tuo käyttäjiä Azure Active Directorysta

[!include [banner](../../includes/banner.md)]

## <a name="import-select-users"></a>Tuo valitut käyttäjät

Näiden ohjeiden avulla järjestelmänvalvoja voi tuoda valitut käyttäjät Azure Active Directorysta (Azure AD).

1. Tuodun käyttäjän oletusyrityksenä on nykyisen istunnon yritys. Muuta nykyistä yritystä tarvittaessa ennen käyttäjien tuomista.
2. Valitse **Järjestelmänhallinta > Käyttäjät > Käyttäjä** t.
3. Valitse **Tuo käyttäjiä**.
4. Valitse tuotavat käyttäjät ja valitse sitten **Tuo käyttäjät**.

Kun tuonti on päättynyt, käyttäjien roolien määrittäminen on pakollista.

## <a name="import-users-in-bulk"></a>Käyttäjien joukkotuonti

Näiden ohjeiden avulla järjestelmänvalvoja voi tuoda suuren määrän käyttäjiä Azure Active Directorysta.
Huomaa, että käyttäjiä ei voi valita Erätuonti-vaihtoehtoa käytettäessä.

## <a name="run-the-import-as-a-batch-job"></a>Suorita tuonti erätyönä
1. Tuodun käyttäjän oletusyrityksenä on nykyisen istunnon yritys. Muuta nykyistä yritystä tarvittaessa ennen käyttäjien tuomista.
2. Valitse **Järjestelmänhallinta > Käyttäjät > Käyttäjä**.
3. Valitse **Erätuonti**.
4. Laajenna **Suorita taustalla** -osa.
4. Valitse **Eräkäsittely**-kentässä **Kyllä**.
6. Syötä tai valitse arvo **Eräryhmä**-kentässä. Tämä on valinnainen vaihe.  
7. Valitse **Kyllä** **Yksityinen**-kentässä. Tämä on valinnainen vaihe.  
8. Valitse **Kyllä** **Kriittinen työ** -kentässä. Tämä on valinnainen vaihe.  
9. Valitse vaihtoehto **Valvontaluokka**-kentässä.
10. Valitse **OK**.

Kun tuonti on päättynyt, käyttäjien roolien määrittäminen on pakollista.

## <a name="run-in-a-sandbox-environment"></a>Eristysympäristön suorittaminen
1. Valitse **Erätuonti**.
2. Valitse **OK**.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]