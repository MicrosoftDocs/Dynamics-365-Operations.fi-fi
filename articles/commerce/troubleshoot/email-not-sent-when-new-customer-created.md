---
title: Tervetuloa-sähköpostia ei lähetetä, kun uusia asiakkaita luodaan
description: Tämä artikkeli antaa vianmääritysohjeet, jotka voivat auttaa, jos Tervetuloa-sähköposti-ilmoitusta ei lähetetä, kun uusi asiakas luodaan Microsoft Dynamics 365 Commercessa.
author: gvrmohanreddy
ms.date: 08/01/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-02-10
ms.openlocfilehash: 5aa7d864555f96194500989e2d7ad200d8892121
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/02/2022
ms.locfileid: "9219401"
---
# <a name="welcome-email-isnt-sent-when-new-customers-are-created"></a>Tervetuloa-sähköpostia ei lähetetä, kun uusia asiakkaita luodaan

[!include [banner](../../includes/banner.md)]

Tämä artikkeli antaa vianmääritysohjeet, jotka voivat auttaa, jos Tervetuloa-sähköposti-ilmoitusta ei lähetetä, kun uusi asiakas luodaan Microsoft Dynamics 365 Commercessa.

## <a name="description"></a>Kuvaus

Kun uusi asiakas luodaan Commerce headquarters -sovelluksessa, asiakkaalle ei lähetetä tervetulosähköpostiviestiä, vaikka sähköposti-ilmoitus olisi määritetty **Asiakas luotu** -sähköposti-ilmoitustyypille.

## <a name="resolution"></a>Ratkaisu

### <a name="associate-an-email-notification-profile-under-commerce-parameters"></a>Sähköposti-ilmoitusprofiilin liittäminen Commerce-parametreihin

1. Valitse pääkonttorissa **Retail ja Commerce \> Pääkonttorin asetukset \> Parametrit \> Commercen parametrit \> Yleinen**.
2. Valitse avattavasta **Sähköposti-ilmoitusprofiili**-luettelosta sähköposti-ilmoitusprofiili, joka sisältää määrityksen asiakkaan luoman ilmoitustyypin ja asiakkaan luoman sähköpostimallin välillä.  

> [!NOTE] 
> Kun otat käyttöön asiakkaan luomat ilmoitukset, asiakkaille, jotka luodaan yrityksen kaikissa kanavissa, lähetetään asiakkaan luoma sähköposti. Asiakkaan luomat ilmoitukset eivät tällä hetkellä rajoitu yhteen kanavaan.

Lue lisätietoja kohdasta [Tapahtuman tapahtumien sähköpostimallien luominen](../email-templates-transactions.md). 

## <a name="additional-resources"></a>Lisäresurssit

[Sähköposti-ilmoitusprofiilin määrittäminen](../email-notification-profiles.md)
