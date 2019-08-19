---
title: Kansainvälisen tilinumero (IBAN) tarkistuksen hallinta
description: Tässä ohjeaiheessa käsitellään kansainvälisen tilinumero (IBAN) tarkistuksen hallintaa.
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 70c497ec575ffcaa6f2fdc3fe77bae7b41dc02fb
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/01/2019
ms.locfileid: "1842422"
---
# <a name="manage-international-bank-account-number-iban-validation"></a>Kansainvälisen tilinumeron (IBAN) tarkistuksen hallinta

[!include [banner](../includes/banner.md)]

Kansainvälisen tilinumeron (IBAN) tarkistus täydentää tarkistusta, joka tehdään, kun lisäät IBAN-numeron pankkitiliin.

Microsoft Dynamics 365 for Finance and Operationsiin on tallennettu tietoja IBAN-rakenteesta. Nämä tiedot ladataan automaattisesti, kun käytät IBAN-numeroa ensimmäisen kerran pankkitileissä. Tiedot sisältävät IBAN-numeron pituuden, tilinumeron ja pankkikoodin aloituskohdat sekä tilinumeron ja pankkikoodin pituuden.

## <a name="set-up-iban-structures"></a>IBAN-rakenteiden määrittäminen

1. Valitse **Maksuliikenteen hallinta \> Asetukset \> IBAN-rakenteet**.
2. Huomaa, että kunkin maan tai alueen IBAN-rakenteet on määritetty automaattisesti.
3. Jos haluat mukauttaa tietyn maan tai alueen rakenteita, voit muokata niitä.
4. Rakenteen määritykset sisältyvät jokaiseen uuteen julkaisuun. Voit ladata uusimmat määritelmät kunkin päivityksen jälkeen **Palauta rakenteet** -valikosta.

## <a name="validate-the-iban-structure-in-a-bank-account"></a>Pankkitilin IBAN-rakenteen tarkistaminen

1. Valitse **Maksuliikenteen hallinta \> Pankkitilit \> Pankkitilit**.
2. Luo pankkitili.
3. Anna IBAN-numero **Lisätiedot**-pikavälilehdessä.

    Jos IBAN-numeron pituus ei vastaa kullekin maalle tai alueelle määritettyä pituutta, saat siitä ilmoituksen. Et voi jatkaa, jos IBAN-numeron pituus ei vastaa IBAN-rakenteessa määritettyä pituutta.

    Tarkistus vahvistaa myös, että pankkitilin numero vastaa IBAN-numeron pankkitilin numeroa vastaavaa osaa. Jos pankkitilin numero ei vastaa sitä, siitä varoitetaan. Tämä sanoma on vain varoitus. Voit jatkaa, vaikka ei pankkitilin numero ei vastaa IBAN-numeroa.

    Tarkistus vahvistaa myös, että pankkikoodi vastaa IBAN-numeron pankkikoodia vastaavaa osaa. Pankkikoodi sisältää pankin numeron ja usein myös toinen pankin konttori. Jos pankkikoodi numero ei vastaa sitä, siitä varoitetaan. Tämä sanoma on vain varoitus. Voit jatkaa, vaikka pankkikoodi ei vastaa IBAN-numeroa.
