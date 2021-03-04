---
title: IoT-analytiikan Azure-resurssien määrittäminen
description: Tässä ohjeaiheessa käsitellään IoT-analytiikkaa varten tarvittavien Microsoft Azure -resurssien luontia ja määrittämistä.
author: robinarh
manager: tfehr
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1277d2ab8bb1f2925874f7469250e164f6bde62d
ms.sourcegitcommit: 092ef6a45f515b38be2a4481abdbe7518a636f85
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4427387"
---
# <a name="set-up-azure-resources-for-iot-intelligence"></a>IoT-analytiikan Azure-resurssien määrittäminen

[!include [banner](../../includes/banner.md)]

Tässä ohjeaiheessa käsitellään IoT-analytiikkaa varten tarvittavien Microsoft Azure -resurssien luontia ja määrittämistä.

## <a name="create-azure-resources"></a>Azure-resurssien luominen

Luo seuraavien ohjeiden avulla IoT-keskitin, Redis-välimuisti ja avainsäilö, jota Microsoft Dynamics 365 Supply Chain Management voi käyttää.

### <a name="verify-that-the-microsoft-dynamics-erp-microservices-first-party-app-id-is-in-your-tenant"></a>Vuokraajan Microsoft Dynamics ERP Microservices -sovellustunnuksen varmistaminen

Seuraavien ohjeiden avulla varmistaa, että Microsoft Dynamics ERP Microservices -sovelluksen sovellustunnus on vuokraajassa.

1. Kirjaudu Azure-portaalin osoitteessa <https://portal.azure.com>.
2. Siirry osoitteeseen **Azure Active Directory**.
3. Valitse **Yrityssovellukset**.
4. Valitse **Sovelluksen tyyppi** -kentässä **Microsoft-sovellukset**.
5. Kirjoita hakukenttään **Microsoft Dynamics ERP Microservices**.
6. Varmista, että **Microsoft Dynamics ERP Microservices** on luettelossa. Muilla sovelluksilla on samankaltaisia nimiä. Varmista tämän vuoksi, että löydät oikean sovelluksen. Sovelluksen tunnus on **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.

    Jos sovellus ei ole luettelossa, se on lisättävä vuokraajaan:

    1. Valitse Azure-portaalin työkalurivillä painike, jolla Azure-pilviliittymä avataan.
    2. Suorita komento **Install-Module AzureAD**. Asenna moduuli kirjoittamalla **Y**.
    3. Varmista, että moduuli on asennettu suorittamalla komento **Get-InstalledModule -Name "AzureAD"**.
    4. Suorita todennus suorittamalla komento **Connect-AzureAD -Confirm**.
    5. Suorita komento **New-AzureADServicePrincipal -AppId 0cdb527f-a8d1-4bf8-9436-b352c68682b2**.

    Toistamalla vaiheet 1–6 voit nyt varmistaa, että sovellustunnus on vuokraajassa.

### <a name="create-a-key-vault-resource"></a>Avainsäilöresurssin luominen

Voit luoda avainsäilöresurssin seuraavien ohjeiden avulla.

1. Luo resurssiryhmä Azure-portaalissa tai siirry siihen.
2. Valitse **Lisää**.
3. Kirjoita **Uusi**-sivun hakukenttään **Avainsäilö**. Valitse sitten **Luo**.
4. Anna nimi **Luo avainsäilö** -sivun **Avainsäilön nimi** -kentässä.
5. Tarkista oletusarvot ja valitse sitten **Tarkista ja luo**.
6. Valitse **Luo**.

Avainsäilö luodaan taustalla.

### <a name="create-an-iot-hub-resource"></a>IoT-resurssin luominen

Voit luoda IoT-keskitinresurssin seuraavien ohjeiden avulla.

1. Luo resurssiryhmä tai siirry siihen.
2. Valitse **Lisää**.
3. Kirjoita **Uusi**-sivun hakukenttään **IoT-keskitin**. Valitse sitten **Luo**.
4. Anna **IoT-keskittimen nimi**-kenttään nimi.
5. Tarkista oletusarvot ja valitse sitten **Tarkista ja luo**.
6. Valitse **Luo**.

IoT-keskitin luodaan taustalla.

> [!NOTE]
> Kutakin ympäristöä varten kannattaa luoda vain yksi IoT-keskitinresurssi.

### <a name="create-a-redis-cache-resource"></a>Redis-välimuistiresurssin luominen

Voit luoda Redis-välimuistiresurssin seuraavien ohjeiden avulla.

1. Luo resurssiryhmä tai siirry siihen.
2. Valitse **Lisää**.
3. Kirjoita **Uusi**-sivun hakukenttään **Azuren Redis-välimuisti**. Valitse sitten **Luo**.
4. Anna nimi **DNS-nimi**-kenttään.
5. Tarkista oletusarvot ja valitse sitten **Luo**.

Redis-välimuisti luodaan taustalla.

> [!NOTE]
> Kutakin ympäristöä varten kannattaa luoda vain yksi Redis-välimuisti.

Kaikki resurssit on nyt luotu.

## <a name="configure-the-azure-resources"></a>Azure-resurssien määrittäminen

### <a name="configure-the-iot-hub"></a>IoT-keskittimen määrittäminen

IoT-keskitin määritetään seuraavasti:

1. Valitse resursseissa IoT-keskitinresurssi.
2. Valitse vasemmassa siirtymisruudussa **Sisäiset päätepisteet**.
3. Liitä seuraavat kuluttajaryhmät **Kuluttajaryhmät**-kohdassa. Nämä kuluttajaryhmät vastaavat heti käytettävissä olevia skenaarioita.

    + microsoft.dynamics.iotintelligence-1
    + microsoft.dynamics.iotintelligence-2
    + microsoft.dynamics.iotintelligence-3

### <a name="configure-the-key-vault"></a>Avainsäilön määrittäminen

Avainsäilö määritetään seuraavasti:

1. Valitse resursseissa avainsäilöresurssi.
2. Valitse vasemmassa siirtymisruudussa **Käyttöoikeuskäytännöt**.
3. Valitse **Lisää käyttöoikeuskäytäntö**.
4. Valitse **Lisää käyttöoikeuskäytäntö** -sivun **Salauskoodin käyttöoikeudet** -kentässä **Hae** ja **Luettelo**.
5. Valitse **Valitse päänimi**.
6. Hae ja valitse **Päänimi**-valintaikkunassa **Microsoft Dynamics ERP Microservices**. Valitse sitten **Valitse**.
7. Valitse **Lisää**.
8. Valitse **Tallenna**.

Sovelluksen on nyt avainsäilön salauskoodien käyttöoikeus.

### <a name="save-the-iot-hub-connection-string-secret"></a>IoT-keskittimen yhteysmerkkijonon salauskoodin tallentaminen

IoT-keskittimen yhteysmerkkijonon salauskoodi tallennetaan seuraavasti:

1. Valitse resursseissa IoT-keskitinresurssi.
2. Valitse vasemmassa siirtymisruudussa **Sisäiset päätepisteet**.
3. Kopioi **Tapahtuman keskittimen kanssa yhteensopiva päätepiste** -kentän arvo.
4. Siirry avainsäilöresurssiin.
5. Valitse vasemmassa siirtymisruudussa **Salauskoodit**.
6. Valitse **Luo tai tuo**.
7. Anna nimi **Nimi**-kenttään.
8. Liitä **Arvo**-kenttään aiemmin kopioitu päätepisteen arvo.
9. Valitse **Luo**.

### <a name="save-the-redis-cache-connection-string-secret"></a>Redis-välimuistin yhteysmerkkijonon salauskoodin tallentaminen

Redis-välimuistin yhteysmerkkijonon salauskoodi tallennetaan seuraavasti:

1. Valitse resursseissa Redis-välimuistiresurssi.
2. Valitse **Käyttöoikeusavaimet**.
3. Kopioi **Ensisijainen yhteysmerkkijono** -kentän arvo.
4. Siirry avainsäilöresurssiin.
5. Valitse vasemmassa siirtymisruudussa **Salauskoodit**.
6. Valitse **Luo tai tuo**.
7. Anna nimi **Nimi**-kenttään.
8. Liitä **Arvo**-kenttään aiemmin kopioitu yhteysmerkkijono.
9. Valitse **Luo**.

> [!NOTE]
> Aina kun yhteysmerkkijono päivitetään, myös salauskoodin arvo on päivitettävä.

Pakolliset Azure-resurssit on nyt valmisteltu. Seuraavaksi [asennetaan IoT-analytiikkalisäosa Microsoft Dynamics Lifecycle Servicesiin (LCS)](iot-lcs-setup.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]