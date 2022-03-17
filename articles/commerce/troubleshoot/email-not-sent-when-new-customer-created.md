---
title: Tervetuloa-sähköpostia ei lähetetä, kun uusia asiakkaita luodaan
description: Tämä ohjeaihe antaa vianmääritysohjeet, jotka voivat auttaa, jos Tervetuloa-sähköposti-ilmoitusta ei lähetetä, kun uusi asiakas luodaan Microsoft Dynamics 365 Commercessa.
author: gvrmohanreddy
ms.date: 02/24/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-02-10
ms.openlocfilehash: 1a4faf6cd189f69232e7f9ab8d0e79b320cfe2d9
ms.sourcegitcommit: d2e5d38ed1550287b12c90331fc4136ed546b14c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/25/2022
ms.locfileid: "8349945"
---
# <a name="welcome-email-is-not-sent-when-new-customers-are-created"></a>Tervetuloa-sähköpostia ei lähetetä, kun uusia asiakkaita luodaan

[!include [banner](../../includes/banner.md)]

Tämä ohjeaihe antaa vianmääritysohjeet, jotka voivat auttaa, jos Tervetuloa-sähköposti-ilmoitusta ei lähetetä, kun uusi asiakas luodaan Microsoft Dynamics 365 Commercessa.

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
