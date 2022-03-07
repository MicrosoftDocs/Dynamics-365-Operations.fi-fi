---
title: Azure-tallennustilin ja avainsäilön luominen
description: Tässä ohjeaiheessa kerrotaan, miten luodaan Azure-tallennustili ja avainsäilö.
author: gionoder
ms.date: 08/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 23fec7a00d800719e1a7d2c90f9d0977d56be038
ms.sourcegitcommit: baf82100f0aa7d5f5f47c7f54bc155d8a07beab5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/31/2021
ms.locfileid: "7463854"
---
# <a name="create-an-azure-storage-account-and-a-key-vault"></a>Azure-tallennustilin ja avainsäilön luominen

[!include [banner](../includes/banner.md)]

## <a name="prerequisites"></a>Edellytykset

Ennen kuin voit suorittaa tämän ohjeaiheen vaiheet on varmistettava, että seuraavat tehtävät on suoritettu:

- Avainsäilöresurssin luominen Azuressa. Lisätietoja: [Tietoja Azure Key Vaultista](/azure/key-vault/general/overview).
- Azure-tallennustilin (Blob-tallennustila) luominen. Lisätietoja: [Azure-tallennustilin ylläpito ](/azure/storage/blobs/).

## <a name="overview"></a>Yleiskuvaus

Tässä aiheessa suoritetaan kaksi päävaihetta:

- Azure-tallennustilin määrittäminen tallennustilin URI-tunnuksen saamista varten.
- Avainsäilön määrittäminen tallennustilin URI-tunnuksen tallentamista varten.

## <a name="set-up-the-azure-storage-account-to-get-the-storage-account-uri"></a>Azure-tallennustilin määrittäminen tallennustilin URI-tunnuksen saamista varten

1. Avaa tallennustili, jota aiot käyttää sähköisen laskutuksen kanssa.
2. Siirry kohtaan **Tietojen tallennus** > **Kontit** ja luo uusi kontti.
3. Anna säilölle nimi ja määritä **Julkinen käyttöoikeustaso** -kentän arvoksi **Yksityinen (ei anonyymia käyttöä)**.
4. Avaa kontti ja siirry kohtaan **Asetukset** > **Käyttöoikeuskäytäntö**.
5. Valitse **Lisää käytäntö** lisätäksesi tallennetun käyttöoikeuskäytännön.
6. Määritä kentät **Tunnus** ja **Oikeudet** tarpeen mukaan. **Oikeudet**-kentässä valitaan kaikki oikeudet.

    ![Blob-tallennustilan oikeuksien myöntäminen.](media/e-Invoicing-services-create-azure-resources-grant-blob-permissions.png)

7. Määritä alkamis- ja päättymispäivät. Päättymispäivän on oltava tulevaisuudessa.
8. Tallenna käytäntö valitsemalla **OK** ja tallenna muutoksesi säilöön.
9. Siirry kohtaan **Asetukset** > **Jaetut käyttöoikeustietueet** ja määritä kenttien arvot. 
10. Määritä alkamis- ja päättymispäivät. Päättymispäivän on oltava tulevaisuudessa.
11. Valitse **Oikeudet**-kentässä seuraavat oikeudet: **Luku**, **Lisäys**, **Luonti**, **Kirjoitus**, **Poisto** ja **Luettelointi**. 
12. Valitse **Luo SAS-tunnus ja URL**.
13. Kopioi arvo ja tallenna se **Blob-SAS-URL**-kenttään. Tätä arvoa käytetään seuraavassa menettelyssä, ja sitä kutsutaan *jaetun käyttöoikeuden allekirjoituksen URI-tunnukseksi*.

## <a name="set-up-the-key-vault-to-store-the-storage-account-uri"></a>Avainsäilön määrittäminen tallennustilin URI-tunnuksen tallentamista varten

1. Avaa avainsäilö, jota aiot käyttää sähköisen laskutuksen kanssa.
2. Siirry kohtaan **Asetukset** \> **Salasanat** ja luo sitten uusi salasana valitsemalla **Luo/tuo**.
3. Valitse **Luo salasana** -sivun **Lataa asetuksia** -kentässä **Manuaalinen**.
4. Anna salasanan nimi. Tätä nimeä käytetään palvelun määrittämiseen RCS:ssä (Regulatory Configuration Service) ja sitä kutsutaan *avainsäilön salasananimeksi*.
5. Kirjoita **Arvo**-kenttään jaetun käyttöoikeuden allekirjoituksen URI-tunnus, jonka kopioit edellisessä menettelyssä, ja valitse sitten **Luo**.
6. Määritä käyttöoikeuskäytäntö, jolla sähköiselle laskutukselle myönnetään asianmukainen suojattu käyttöoikeus luomaasi salasanaan. Siirry kohtaan **Asetukset \> Käyttöoikeuskäytäntö** ja valitse **Lisää käyttöoikeuskäytäntö**.
7. Määritä salasanaoikeudet toiminnoille **Hae** ja **Luetteloi**.

    ![Palvelun käyttöoikeuksien myöntäminen.](media/e-Invoicing-services-create-azure-resources-grant-service-access.png)

8. Määritä varmenneoikeudet toiminnoille **Hae** ja **Luetteloi**.

    ![Varmenneoikeuksien myöntäminen.](media/e-Invoicing-services-create-azure-resources-grant-certificate-permission.png)

9. Valitse **Objekti** -kentässä **Mitään ei valittu**.
10. Valitse **Objekti**-valintaikkunassa objekti lisäämällä **Sähköisen laskutuksen palvelu**.
11. Valitse ensin **Lisää** ja sitten **Tallenna**.
12. Kopioi **Yhteenveto**-sivulla avainsäilön **DNS nimi** -arvo. Tätä arvoa käytetään palvelun RCS:ssä määrittämiseen ja sitä kutsutaan *avainsäilön URI-tunnukseksi*.

> [!NOTE]
> Jos haluat lisäsuojausominaisuuksia tallennustilille, määritä Azure Defender for Storage.
> 
> Lisätietoja on kohdassa [Azure Defender for Storagen esittely](/azure/security-center/defender-for-storage-introduction).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
