---
title: Invoice Capture -ratkaisun asentaminen
description: Tässä artikkelissa on tietoja Invoice Capture -ratkaisun asentamisesta ja integroinnista Microsoft Dynamics 365 Financen kanssa.
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
ms.openlocfilehash: d853e347c833345f34b65760fd7ee35cbb38c9a3
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691172"
---
# <a name="install-the-invoice-capture-solution"></a>Invoice Capture -ratkaisun asentaminen

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!IMPORTANT]
> Jos olet asentanut ratkaisun yksityisessä esikatselussa, poista vanhan ratkaisun asennus ennen jatkamista.

## <a name="prerequisites"></a>Edellytykset

Ennen kuin voit asentaa Invoice Capture -ratkaisun, seuraavien edellytysten on toteuduttava:

1. Rekisteröi sovellus ja lisää asiakasohjelman salasana Microsoft Azure Active Directoryyn (Azure AD) Azure-tilauksessa. Lisätietoja on kohdassa [Verkkosovelluksen rekisteröiminen AAD:n avulla](../../dev-itpro/data-entities/services-home-page.md#register-a-web-application-with-aad).

    > [!NOTE]
    > Kirjoita **Sovelluksen (asiakasohjelman) tunnus**-, **Asiakasohjelman salasana**- ja **Vuokraajan tunnus** -arvot muistiin, sillä niitä tarvitaan myöhemmin.

2. Rekisteröi Azure-sovellus Dynamics 365 Finance -ympäristössä. Lisätietoja on kohdassa [Ulkoisen sovelluksen rekisteröiminen](../../dev-itpro/data-entities/services-home-page.md#register-your-external-application).

## <a name="install-and-set-up-the-solution"></a>Ratkaisun asentaminen ja määrittäminen

Voit asentaa Invoice Capture -ratkaisun siirtymällä AppSourceen ja valitsemalla [Dynamics 365 Invoice Capture](https://appsource.microsoft.com/product/dynamics-365/mscrm.dynamics365-invoice-capture-preview?flightCodes=invoicecapture) -ratkaisun esiversion linkin. Kun asennus on valmis, ratkaisu näkyy asennettuna valitussa ympäristössä Power Appsissa.

Viimeiste määritys noudattamalla alla olevia ohjeita.

1. Lataa [avustajaratkaisu](https://github.com/InvoiceCapture/InstallationTools/releases/download/latest/msdyn_InvoiceCaptureIntallationTools.zip) ja määritä seuraavat tiedot:

    - Microsoft Power Platformin ja Finance-ympäristön välinen viestintä
    - Dataversen ja Office 365 Outlookin välinen yhteysviite, jota käytetään kanavassa

2. Siirry Power Appsissa ympäristöön ja valitse **Tuo ratkaisu**.
3. Valitse **Selaa** ja valitse sitten lataamasi avustajaratkaisupaketti. Valitse **Seuraava**.
4. Valitse **Seuraava**.
5. Liitä olemassa oleva yhteys tai luo uusi yhteys valitsemalla **Uusi yhteys**.
6. Kun paketin tuonti onnistuu, avaa **Dynamics 365 Invoice Capture – asennustyökalut**.
7. Suorita pilvityönkulku ja määritä Microsoft Power Platformin Invoice Capture -ratkaisun ja Financen välinen yhteys.
8. Valitse **Suorita** ja määritä seuraavat parametrit:

    - **Dynamics 365 Financen URL-osoite** Finance-ympäristön URL-osoite, johon haluat integroida.
    - **Vuokraajan tunnus** – Finance-ympäristön vuokraajan tunnus.
    - **Asiakasohjelman tunnus** – Rekisteröidyn Azure-sovelluksen tunnus.
    - **Asiakasohjelman salasana** – Asiakasohjelman salasana, joka luotiin Azure-sovellukselle.
