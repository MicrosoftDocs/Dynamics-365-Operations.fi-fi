---
title: Lisää maksun summan tyyppejä
description: Tässä artikkelissa kerrotaan, kuinka maksun summa -tyypit määritetään resurssien vuokrauksessa.
author: moaamer
ms.date: 01/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseIndexRevaluation
audience: Application User
ms.reviewer: twheeloc
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 03fc903e6cfe78ef2fed7e3a0744a8f809f6892d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8891606"
---
# <a name="add-payment-amount-types"></a>Lisää maksun summan tyyppejä

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kuvataan, kuinka maksun summa -tyypit määritetään resurssien vuokrauksessa. Tällä tavoin voit eritellä vuokran maksusumman sen sijaan, että lisäisit kertakorvauksen summan maksusuunnitelmariveille.

Voit lisätä maksun summa -tyypit seuraavasti.

1. Siirry kohtaan **Resurssin vuokraus \> Asetukset \> Maksun summa -tyypit**.
2. Valitse **Uusi**.
3. Kirjoita uusi maksutyyppi ja kuvaus.

> [!NOTE]
> IFRS 16 -indeksin uudelleenarvostuksessa on luotava yksi maksusummatyyppi ja merkittävä se **käytetyksi IRFS 16 -indeksin uudelleenarvostuksessa**. Tätä maksusummatyyppiä käytetään, kun indeksin uudelleenarvostusprosessi suoritetaan IFRS 16 -kirjaa vastaan, ja se ottaa huomioon indeksin uudelleenarvostusprosessin vuoksi tapahtuneet muutokset.
>
> Kun vuokrasopimuksen **Maksuerittely**-asetuksena on **Kyllä**, jos IFRS 16:n indeksin uudelleenarvostus suoritetaan, mutta IFRS 16:lle ei ole maksutyyppiä, prosessia ei suoriteta loppuun.

Vain yksi tietue voidaan merkitä **käytetyksi IFRS 16 -indeksin uudelleenarvostuksessa**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
