---
title: Invoice Capture -ratkaisun lisäasetukset
description: Tässä artikkelissa on tietoja Invoice Capture -ratkaisun lisäasetuksista.
author: sunfzam
ms.date: 09/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "13971"
- intro-internal
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: zezhangzhao
ms.search.validFrom: 2022-09-28
ms.dyn365.ops.version: ''
ms.openlocfilehash: a1e24b700d0f30fd90f2619dd6e6687736a86774
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691157"
---
# <a name="invoice-capture-solution-advanced-settings"></a>Invoice Capture -ratkaisun lisäasetukset

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Tässä artikkelissa on tietoja Invoice Capture -ratkaisun lisäasetuksista.

## <a name="create-additional-connections-for-channels"></a>Lisäyhteyksien luominen kanavia varten

Luo yhteyksiä sähköposti- tai tiedostotallennustilaan, jotta eri kanavista saapuvien laskujen valvonta on mahdollista. Yhteydet on rekisteröitävä alussa, jotta ratkaisussa käytettäville automaattisille työnkuluille annetaan käyttöoikeus.

Laskujen tuonnissa käytetään alla olevia yhteystyyppejä.

- Office 365 Outlook
- Outlook.com
- OneDrive
- SharePoint

Laskujen tuomisessa käytettävä kanava käyttää yhteyksiä määrityksen lisävaiheissa. Ennen kuin käyttäjät voivat luoda kanavan tietyllä yhteydellä, heille on myönnettävä **järjestelmänvalvojan** käyttöoikeusrooli ja heidän on luotava yhteyksiä.

Voit luoda yhteyden Microsoft Dataverseen alla olevien ohjeiden avulla.

1. Siirry kohtaan **Hallintajärjestelmä \> Oletusratkaisu**.
2. Valitse **Uusi** ja valitse sitten **Yhteysviite**.
3. Kirjoita **Näyttönimi**-kenttään nimi.
4. Valitse yhdistimeksi **Microsoft Dataverse**.
5. Jos määrität yhteyttä ensimmäistä kertaa, valitse **Uusi yhteys**.
6. Luo näkyviin tulevassa valintaikkunassa Dataverse-yhteys ja valitse **Luo**.
7. Syötä Dataverse-tili ja -salasana.
8. Kun vahvistus on tehty, siirry yhteyssivulla, valitse **Päivitä** ja valitse sitten tili. Valitse lopuksi **Luo**.

Voit luoda sähköpostiviesti- tai tiedostotallennustilan yhteyden alla olevien ohjeiden avulla.

1. Valitse **Yhteyden luonti** -sivulla **Yhteystyyppi**-kentässä **Office 365 Outlook**.
2. Sähköpostiyhteydelle voit valita yhdistimeksi **Outlook.com**- tai **Office 365 Outlook** -vaihtoehdon. Tiedostotallennustilan yhteydeksi voit valita **OneDrive**- tai **SharePoint**-vaihtoehdon.

Voit tarkistaa olemassa olevat yhteydet siirtymällä kohtaan **Oletusratkaisu \> Objektit \> Yhteysviitteet**. Kanavat luoneella käyttäjällä on oltava vähintään yksi Dataverse-yhteys määritettyjen sähköpostiviesti- tai tiedostotallennustilan yhteyksien lisäksi. Uuden kanavan tekijän on oltava yhteyden omistaja.
