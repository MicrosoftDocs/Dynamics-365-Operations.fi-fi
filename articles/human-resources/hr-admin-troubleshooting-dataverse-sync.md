---
title: Dataverse-synkronoinnin nollaaminen
description: Tässä aiheessa käsitellään sellaisten tietueiden vianmääritystä, jotka eivät synkronoidu oikein Microsoft Dynamics 365 Human Resourcesin ja henkilöstöresurssien hallinnan (HCM) yleisen ratkaisun välillä Microsoft Dataversessa.
author: jaredha
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-09-27
ms.dyn365.ops.version: Platform update 42
ms.openlocfilehash: d6b20b6b2ae4fdbbfb27a765dfb7a1dc82fe7981
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/31/2022
ms.locfileid: "8071157"
---
# <a name="reset-dataverse-synchronization"></a>Dataverse-synkronoinnin nollaaminen


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

## <a name="issue"></a>Ongelma

Tietueet eivät synkronoidu Microsoft Dynamics 365 Human Resourcesin ja henkilöstöresurssien hallinnan (HCM) yleisen ratkaisun välillä Microsoft Dataversessa. Lisätietoja synkronoinnista on kohdassa [Dataverse-integroinnin määrittäminen](hr-admin-integration-common-data-service.md). Synkronointi voi epäonnistua, kun **Dataversen integroinnin uudelleenyritys**- tai **Dataversen integroinnin toteutumattoman pyynnön synkronointi** -erätyöt jumiutuvat **Suoritetaan**-tilaan.

## <a name="resolution"></a>Ratkaisu

Jos **Dataversen integroinnin uudelleenyritys**- tai **Dataversen integroinnin toteutumattoman pyynnön synkronointi** -erätyöt jumiutuvat **Suoritetaan**- tai **Peruutetaan**-tilaan, tila voidaan nollata. Se voidaan tehdä peruuttamalla erätyö kohdan [Jumittuneiden erätöiden nollaaminen](hr-admin-troubleshooting-batch-execution.md) ohjeita. Kun erätyö on peruutettu, erätyö voidaan nollata määrittämällä sen tilaksi **Odottaa**. Erätyö suoritetaan sitten seuraavan ajoitetun suorituskerran yhteydessä.

1. Jos sitä ei ole vielä tehty, ota **Laajennetun kerän keskeytys** -ominaisuus käyttöön **ominaisuuksien hallinnassa**.
   1. Siirry **Ominaisuuksien hallinta** -sivulle (**Järjestelmän hallinta** > **Yhteenveto** > **Ominaisuuksien hallinta**).
   2. Valitse **Kaikki**-välilehti.
   3. Valitse **Ominaisuuden nimi** -sarake ja suodatusperusteeksi **Laajennetun erän keskeytys**.
   4. Valitse **Ota käyttöön** -toiminto, jos sitä ei ole vielä tehty.

2. Poista Dataverse-Integrointi käytöstä.
   1. Siirry **Microsoft Dataverse -integrointi** -sivulle (**Järjestelmän hallinta**, valitse **Linkit** > **Integraatiot** > **Dataversen määritys**).
   2. Määritä **Ota Dataverse-integrointi käyttöön** -asetukseksi **Ei**.

3. Peruuta **Dataversen integroinnin uudelleenyritys** -erätyö.
   1. Siirry **Erätyöt**-sivulle (**Järjestelmän hallinta** valitse **Linkit** > **Erätyöt** > **Erätyöt**).
   2. Valitse **Työn kuvaus** -sarakkeen suodatusperusteeksi **Integraatio**.
   3. Valitse **Dataversen integroinnin uudelleenyritys** -erätyö.
   4. Valitse toimintonauhassa ensin **Erätyö**, sitten **Pakota peruutus** ja vahvista lopuksi valitsemalla **Kyllä**.

   > [!NOTE]
   > Sen perusteella milloin integraatio otettiin ensimmäisen kerran käyttöön, etätyössä voi olla kuvaus **Common Data Servicen integraation uudelleenyritys**. Jos tämä erätyö on luettelossa, valitse se eikä **Dataversen integraation uudelleenyritys**.

4. Poista kaikki Dataversen integraation erätyöt.
   1. Valitse **Erätyöt**-sivulla **Dataversen integraation toteutumattoman pyynnön synkronointi**-, **Dataversen integraation uudelleenyritys**- ja **Dataversen integraation ensimmäinen synkronointi** -erätyöt.
   2. Valitse toimintovalintanauhassa **Muuta tila** -toiminto. 
   3. Valitse ensin **Pidätä** ja sitten **OK**.
   4. Valitse toimintovalintanauhassa **Poista**-toiminto ja vahvista toiminto sitten valitsemalla **Kyllä**.

5. Ota Dataversen integraation erätyöt käyttöön.
   1. Siirry **Microsoft Dataverse -integrointi** -sivulle (**Järjestelmän hallinta** > **Linkit** > **Integraatio** > **Dataversen määritys**).
   2. Määritä **Ota Dataverse-integrointi käyttöön** -asetukseksi **Kyllä**.

6. Siirry **Erätyöt**-sivulla ja varmista, että **Dataversen integraation uudelleenyritys**- ja **Dataversen integraation toteutumattoman pyynnön synkronointi** -erätyöt on luotu.

Kun erätyöt on luotu uudelleen, **Dataversen integraation uudelleenyritys** -erätyötä seuraamalla voi selvittää, kuinka kauan työn suorittaminen kestää. Sen jälkeen voidaan varmistaa, että tietueet on synkronoitu oikein HCM:n yleiseen ratkaisuun Microsoft Dataversessa.

## <a name="see-also"></a>Lisätietoja

[Dataverse -integroinnin määritys](hr-admin-integration-common-data-service.md)<br>
[Jumittuneiden erätöiden nollaaminen](hr-admin-troubleshooting-batch-execution.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
