---
title: Azure-tallennustilin ja avainsäilön luominen
description: Tässä ohjeaiheessa kerrotaan, miten luodaan Azure-tallennustili ja avainsäilö.
author: gionoder
manager: AnnBe
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 5a883011bbff6d82504497d739c07f1ada9e5f69
ms.sourcegitcommit: f860ac2b18f6bbbfc4a46b497baec2477105b116
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/19/2020
ms.locfileid: "4442946"
---
# <a name="create-an-azure-storage-account-and-a-key-vault"></a>Azure-tallennustilin ja avainsäilön luominen

[!include [banner](../includes/banner.md)]



Sähköisen laskutuksen lisäosapalvelu ottaa vastuun kaikkien liiketoimintatietojen tallentamisesta yrityksen omistamiin Microsoft Azure -resursseihin. Sen varmistamiseksi, että palvelu toimii oikein ja että kaikki sähköisen laskutuksen lisäosaa varten tarvittavat ja sen luomat liiketoimintatiedot ovat vain lisäosan käytettävissä, on luotava kaksi keskeistä Azure-resurssia:

- Azure-tallennustili (Blob-tallennus) sähköisten laskujen tallentamista varten
- Azure-avainsäilö, johon tallennetaan tallennustilin tallennusvarmenteet ja Uniform Resource Identifier (URI)

> [!NOTE]
> Erillinen avainsäilöresurssi ja asiakkaan Blob-tallennustila on määritettävä nimenomaisesti käytettäväksi sähköisen laskutuksen lisäosan kanssa.

## <a name="prerequisites"></a>Edellytykset

Ennen kuin voit suorittaa tämän ohjeaiheen vaiheet on varmistettava, että seuraavat tehtävät on suoritettu:

- Avainsäilöresurssin luominen Azuressa. Lisätietoja: [Tietoja Azure Key Vaultista](https://docs.microsoft.com/azure/key-vault/general/overview).
- Azure-tallennustilin (Blob-tallennustila) luominen. Lisätietoja: [Azure-tallennustilin ylläpito ](https://docs.microsoft.com/azure/storage/blobs/).

## <a name="overview"></a>Yleiskuvaus

Tässä aiheessa suoritetaan kaksi päävaihetta:

- Azure-tallennustilin määrittäminen tallennustilin URI-tunnuksen saamista varten.
- Avainsäilön määrittäminen tallennustilin URI-tunnuksen tallentamista varten.

## <a name="set-up-the-azure-storage-account-to-get-the-storage-account-uri"></a>Azure-tallennustilin määrittäminen tallennustilin URI-tunnuksen saamista varten

1. Avaa tallennustili, jota aiot käyttää sähköisen laskutuksen lisäosan kanssa.
2. Siirry kohtaan **Blob-palvelu** \> **Säilöt** ja luo uusi säilö.
3. Anna säilölle nimi ja määritä **Julkinen käyttöoikeustaso** -kentän arvoksi **Yksityinen (ei anonyymia käyttöä)**.
4. Avaa säilö ja siirry kohtaan **Asetukset \> Käyttöoikeuskäytäntö**.
5. Valitse **Lisää käytäntö** lisätäksesi tallennetun käyttöoikeuskäytännön.
6. Määritä kentät **Tunnus** ja **Oikeudet** tarpeen mukaan. **Oikeudet**-kentässä valitaan kaikki oikeudet.

    ![Blob-tallennustilan oikeuksien myöntäminen](media/e-Invoicing-services-create-azure-resources-grant-blob-permissions.png)

7. Määritä alkamis- ja päättymispäivät. Päättymispäivän on oltava tulevaisuudessa.
8. Tallenna käytäntö valitsemalla **OK** ja tallenna muutoksesi säilöön.
9. Palaa tallennustilille ja avaa **Tallennustilan hallinta (esikatselu)**.
10. Napsauta säilöä hiiren kakkospainikkeella ja valitse sitten **Hae jaetun käyttöoikeuden allekirjoitus**.
11. Kopioi **Jaetun käyttöoikeuden allekirjoitus** -valintaikkunan arvo ja tallenna se **URI**-kenttään. Tätä arvoa käytetään seuraavassa menettelyssä, ja sitä kutsutaan *jaetun käyttöoikeuden allekirjoituksen URI-tunnukseksi*.

    ![URI-arvon valitseminen ja kopioiminen](media/e-Invoicing-services-create-azure-resources-select-and-copy-uri.png)

## <a name="set-up-the-key-vault-to-store-the-storage-account-uri"></a>Avainsäilön määrittäminen tallennustilin URI-tunnuksen tallentamista varten

1. Avaa avainsäilö, jota aiot käyttää sähköisen laskutuksen lisäosan kanssa.
2. Siirry kohtaan **Asetukset** \> **Salasanat** ja luo sitten uusi salasana valitsemalla **Luo/tuo**.
3. Valitse **Luo salasana** -sivun **Lataa asetuksia** -kentässä **Manuaalinen**.
4. Anna salasanan nimi. Tätä nimeä käytetään palvelun määrittämiseen RCS:ssä (Regulatory Configuration Service) ja sitä kutsutaan *avainsäilön salasananimeksi*.
5. Valitse **Arvo**-kentässä **Jaetun käyttöoikeuden allekirjoituksen URI-tunnus** ja sitten **Luo**.
6. Määritä käyttöoikeuskäytäntö, jolla sähköisen laskutuksen lisäosalle myönnetään asianmukainen suojattu käyttöoikeus luomaasi salasanaan. Siirry kohtaan **Asetukset \> Käyttöoikeuskäytäntö** ja valitse **Lisää käyttöoikeuskäytäntö**.
7. Määritä salasanaoikeudet toiminnoille **Hae** ja **Luetteloi**.

    ![Palvelun käyttöoikeuksien myöntäminen](media/e-Invoicing-services-create-azure-resources-grant-service-access.png)

8. Määritä varmenneoikeudet toiminnoille **Hae** ja **Luetteloi**.

    ![Varmenneoikeuksien myöntäminen](media/e-Invoicing-services-create-azure-resources-grant-certificate-permission.png)

9. Valitse **Objekti**-valintaikkunassa objekti lisäämällä **Sähköisen laskutuksen lisäosa**.
10. Valitse **Lisää** ja sitten **Tallenna avainsäilön muutokset**.
11. Kopioi **Yhteenveto**-sivulla avainsäilön **DNS nimi** -arvo. Tätä arvoa käytetään palvelun RCS:ssä määrittämiseen ja sitä kutsutaan *avainsäilön URI-tunnukseksi*.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]