---
title: Tervetuloa-sähköpostia ei lähetetä, kun uusia asiakkaita luodaan
description: Tämä artikkeli antaa vianmääritysohjeet, jotka voivat auttaa, jos Tervetuloa-sähköposti-ilmoitusta ei lähetetä, kun uusi asiakas luodaan Microsoft Dynamics 365 Commercessa.
author: gvrmohanreddy
ms.date: 02/24/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-02-10
ms.openlocfilehash: 8e95b33d4b8a9af13c613ab89dd33de6b4934694
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8853680"
---
# <a name="welcome-email-is-not-sent-when-new-customers-are-created"></a>Tervetuloa-sähköpostia ei lähetetä, kun uusia asiakkaita luodaan

[!include [banner](../../includes/banner.md)]

Tämä artikkeli antaa vianmääritysohjeet, jotka voivat auttaa, jos Tervetuloa-sähköposti-ilmoitusta ei lähetetä, kun uusi asiakas luodaan Microsoft Dynamics 365 Commercessa.

## <a name="description"></a>Kuvaus

Kun uusi asiakas luodaan Commerce headquarters -sovelluksessa, asiakkaalle ei lähetetä tervetulosähköpostiviestiä, vaikka sähköposti-ilmoitus olisi määritetty **Asiakas luotu** -sähköposti-ilmoitustyypille.

## <a name="resolution"></a>Ratkaisu

### <a name="set-the-correct-email-id-value-for-the-customer-created-email-notification-type"></a>Oikean sähköpostitunnusarvon määrittäminen Asiakas luotu -sähköposti-ilmoitustyypille

Noudattamalla seuraavia ohjeita voit määrittää oikean **sähköpostitunnuksen** **arvon** Asiakas luotu -sähköposti-ilmoitustyypille Headquartersissa.

1. Siirry kohtaan **Retail ja Commerce \> Headquarters-asetukset \> Kaupan sähköposti-ilmoitusprofiili**.
1. Valitse vasemmasta siirtymisruudusta sähköposti-ilmoitusprofiili.
1. Määritä kohdassa **Vähittäismyyntitapahtuman ilmoitusasetukset** **Asiakas luotu** -sähköposti-ilmoitustyypille **Sähköpostitunnus**-kentän arvoksi **NewCust**.

## <a name="additional-resources"></a>Lisäresurssit

[Sähköposti-ilmoitusprofiilin määrittäminen](../email-notification-profiles.md)
