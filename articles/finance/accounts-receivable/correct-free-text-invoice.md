---
title: Vapaatekstilaskun korjaus
description: Tässä artikkelissa kerrotaan, miten kirjattu vapaatekstilasku korjataan ja luodaan uudelleen korjattuna laskuna.
author: abruer
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: twheeloc
ms.custom: 13991
ms.assetid: 2a0a4789-8619-4974-bef9-0923cc848420
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6c83ac47bc5e7f7ed223c772591cf8a7c1e63a40
ms.sourcegitcommit: 0d5c07ba91a9ceb2eeb11db032fd28037216789d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/25/2022
ms.locfileid: "9715494"
---
# <a name="correct-a-free-text-invoice"></a>Vapaatekstilaskun korjaus

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kerrotaan, miten kirjattu vapaatekstilasku korjataan ja luodaan uudelleen korjattuna laskuna.

Voit korjata kirjatun vapaatekstilaskun avaamalla kirjatun vapaatekstilaskun. Valitse **Lasku**-sivulla **Peruuta** ja sitten **Korjaa lasku**. Valitse syykoodi, lisää kommentit ja valitse päivämäärä uudelle korjatulle laskulle. Voit muokata korjattua laskua ja kirjata sen. 

Kun kirjaat korjatun laskun, hyvityssummalle luodaan alkuperäisen laskun suuruinen peruutuslasku. Alkuperäisen laskun ja peruutuslasku yhteissaldo onkin tämän vuoksi 0 (nolla). Peruutuslasku tilitetään alkuperäiseen laskuun. 

Korjatun laskun kirjaamisen jälkeen sinulla on kolme laskua:

-   **Alkuperäinen lasku** – lasku, joka sisältää korjattavat tiedot.
-   **Peruutuslasku** – järjestelmän luoma hyvityslasku, joka on luotiin peruuttamaan viimeksi korjattu lasku.
-   **Korjattu lasku** – lasku, joka sisältää korjatut laskutiedot.

Peruutuslaskun ja korjaavan laskun voi tunnistaa kahdella tavalla:

-   **Kaikki vapaamuotoiset laskut** -sivulla on **Korjaus**-sarake, josta näet, mitkä laskut ovat peruutuslaskuja ja mitkä korjattuja laskuja.
-   Vapaatekstilaskun otsikon tila on joko **Peruutuslasku \[laskunumero\]** tai **Korjattu lasku \[laskunumero\]**.

> [!NOTE]
> Tämä toiminto on käytettävissä vain, jos **Tekstimuotoisen laskun korjaus** -määritysavain on valittu. Lisätietoja määritysavainten käyttöönotoista on aiheen [Ylläpitotila](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md) -artikkelin Ota käyttöön (tai poista käytöstä) määritysavaimia -osassa. 





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
