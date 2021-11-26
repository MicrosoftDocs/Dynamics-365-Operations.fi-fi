---
title: Kansainvälisen tilinumero (IBAN) tarkistuksen hallinta
description: Tässä ohjeaiheessa käsitellään kansainvälisen tilinumero (IBAN) tarkistuksen hallintaa.
author: roscholm
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 2c992d1df0f363960caa363a514a3c6f6d51e78d
ms.sourcegitcommit: 408786b164b44bee4e16ae7c3d956034d54c3f80
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/05/2021
ms.locfileid: "7753607"
---
# <a name="manage-international-bank-account-number-iban-account-validation"></a>Kansainvälisen tilinumero (IBAN) tarkistuksen hallinta

[!include [banner](../includes/banner.md)]

Kansainvälisen tilinumeron (IBAN) tarkistus täydentää tarkistusta, joka tehdään, kun lisäät IBAN-numeron pankkitiliin.

Microsoft Dynamics 365 Financeen on tallennettu tietoja IBAN-rakenteesta. Nämä tiedot ladataan automaattisesti, kun käytät IBAN-numeroa ensimmäisen kerran pankkitileissä. Tiedot sisältävät IBAN-numeron pituuden, tilinumeron ja pankkikoodin aloituskohdat sekä tilinumeron ja pankkikoodin pituuden.

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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
