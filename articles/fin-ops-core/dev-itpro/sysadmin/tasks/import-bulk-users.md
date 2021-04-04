---
title: Tuo käyttäjiä Azure Active Directorysta
description: Näiden ohjeiden avulla järjestelmänvalvoja voi tuoda manuaalisesti valitut käyttäjät tai suuren määrän käyttäjiä Azure Active Directorysta.
author: peakerbl
manager: AnnBe
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
ms.openlocfilehash: 0c2600ad8f441e6b73b143c27afa08ad0a5c2748
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5571002"
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