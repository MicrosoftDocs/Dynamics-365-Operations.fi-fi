---
title: Azure-tallennustilin ja avainsäilön luominen
description: Tässä ohjeaiheessa kerrotaan, miten luodaan Azure-tallennustili ja avainsäilö.
author: gionoder
ms.date: 04/29/2021
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
ms.openlocfilehash: a0fe265c75138f3ecfbf08de3c30b2c824463afc35414986e21c4a27bf84bb61
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6770533"
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
2. Siirry kohtaan **Blob-palvelu** \> **Säilöt** ja luo uusi säilö.
3. Anna säilölle nimi ja määritä **Julkinen käyttöoikeustaso** -kentän arvoksi **Yksityinen (ei anonyymia käyttöä)**.
4. Avaa säilö ja siirry kohtaan **Asetukset \> Käyttöoikeuskäytäntö**.
5. Valitse **Lisää käytäntö** lisätäksesi tallennetun käyttöoikeuskäytännön.
6. Määritä kentät **Tunnus** ja **Oikeudet** tarpeen mukaan. **Oikeudet**-kentässä valitaan kaikki oikeudet.

    ![Blob-tallennustilan oikeuksien myöntäminen.](media/e-Invoicing-services-create-azure-resources-grant-blob-permissions.png)

7. Määritä alkamis- ja päättymispäivät. Päättymispäivän on oltava tulevaisuudessa.
8. Tallenna käytäntö valitsemalla **OK** ja tallenna muutoksesi säilöön.
9. Palaa tallennustilille ja avaa **Tallennustilan hallinta (esikatselu)**.
10. Napsauta säilöä hiiren kakkospainikkeella ja valitse sitten **Hae jaetun käyttöoikeuden allekirjoitus**.
11. Kopioi **Jaetun käyttöoikeuden allekirjoitus** -valintaikkunan arvo ja tallenna se **URI**-kenttään. Tätä arvoa käytetään seuraavassa menettelyssä, ja sitä kutsutaan *jaetun käyttöoikeuden allekirjoituksen URI-tunnukseksi*.

    ![URI-arvon valitseminen ja kopioiminen.](media/e-Invoicing-services-create-azure-resources-select-and-copy-uri.png)

## <a name="set-up-the-key-vault-to-store-the-storage-account-uri"></a>Avainsäilön määrittäminen tallennustilin URI-tunnuksen tallentamista varten

1. Avaa avainsäilö, jota aiot käyttää sähköisen laskutuksen kanssa.
2. Siirry kohtaan **Asetukset** \> **Salasanat** ja luo sitten uusi salasana valitsemalla **Luo/tuo**.
3. Valitse **Luo salasana** -sivun **Lataa asetuksia** -kentässä **Manuaalinen**.
4. Anna salasanan nimi. Tätä nimeä käytetään palvelun määrittämiseen RCS:ssä (Regulatory Configuration Service) ja sitä kutsutaan *avainsäilön salasananimeksi*.
5. Valitse **Arvo**-kentässä **Jaetun käyttöoikeuden allekirjoituksen URI-tunnus** ja sitten **Luo**.
6. Määritä käyttöoikeuskäytäntö, jolla sähköiselle laskutukselle myönnetään asianmukainen suojattu käyttöoikeus luomaasi salasanaan. Siirry kohtaan **Asetukset \> Käyttöoikeuskäytäntö** ja valitse **Lisää käyttöoikeuskäytäntö**.
7. Määritä salasanaoikeudet toiminnoille **Hae** ja **Luetteloi**.

    ![Palvelun käyttöoikeuksien myöntäminen.](media/e-Invoicing-services-create-azure-resources-grant-service-access.png)

8. Määritä varmenneoikeudet toiminnoille **Hae** ja **Luetteloi**.

    ![Varmenneoikeuksien myöntäminen.](media/e-Invoicing-services-create-azure-resources-grant-certificate-permission.png)

9. Valitse **Objekti** -kentässä **Mitään ei valittu**.
10. Valitse **Objekti**-valintaikkunassa objekti lisäämällä **Sähköisen laskutuksen palvelu**.
11. Valitse **Lisää** ja sitten **Tallenna avainsäilön muutokset**.
12. Kopioi **Yhteenveto**-sivulla avainsäilön **DNS nimi** -arvo. Tätä arvoa käytetään palvelun RCS:ssä määrittämiseen ja sitä kutsutaan *avainsäilön URI-tunnukseksi*.

> [!NOTE]
> Jos haluat lisäsuojausominaisuuksia tallennustilille, määritä Azure Defender for Storage.
> 
> Lisätietoja on kohdassa [Azure Defender for Storagen esittely](/azure/security-center/defender-for-storage-introduction).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
