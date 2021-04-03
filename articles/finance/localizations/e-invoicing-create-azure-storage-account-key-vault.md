---
title: Azure-tallennustilin ja avainsäilön luominen
description: Tässä ohjeaiheessa kerrotaan, miten luodaan Azure-tallennustili ja avainsäilö.
author: gionoder
manager: AnnBe
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 14463abe7782d786d286fcc619dee00ce85bb620
ms.sourcegitcommit: 4adc57b0e43d9627dca70762ac941762ec4934e2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/22/2021
ms.locfileid: "5479342"
---
# <a name="create-an-azure-storage-account-and-a-key-vault"></a><span data-ttu-id="f6a21-103">Azure-tallennustilin ja avainsäilön luominen</span><span class="sxs-lookup"><span data-stu-id="f6a21-103">Create an Azure storage account and a key vault</span></span>

[!include [banner](../includes/banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="f6a21-104">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="f6a21-104">Prerequisites</span></span>

<span data-ttu-id="f6a21-105">Ennen kuin voit suorittaa tämän ohjeaiheen vaiheet on varmistettava, että seuraavat tehtävät on suoritettu:</span><span class="sxs-lookup"><span data-stu-id="f6a21-105">Before you can complete the steps in this topic, you must make sure that the following tasks have been completed:</span></span>

- <span data-ttu-id="f6a21-106">Avainsäilöresurssin luominen Azuressa.</span><span class="sxs-lookup"><span data-stu-id="f6a21-106">Create a key vault resource in Azure.</span></span> <span data-ttu-id="f6a21-107">Lisätietoja: [Tietoja Azure Key Vaultista](https://docs.microsoft.com/azure/key-vault/general/overview).</span><span class="sxs-lookup"><span data-stu-id="f6a21-107">For more information, see [About Azure Key Vault](https://docs.microsoft.com/azure/key-vault/general/overview).</span></span>
- <span data-ttu-id="f6a21-108">Azure-tallennustilin (Blob-tallennustila) luominen.</span><span class="sxs-lookup"><span data-stu-id="f6a21-108">Create an Azure storage account (Blob storage).</span></span> <span data-ttu-id="f6a21-109">Lisätietoja: [Azure-tallennustilin ylläpito ](https://docs.microsoft.com/azure/storage/blobs/).</span><span class="sxs-lookup"><span data-stu-id="f6a21-109">For more information, see [Maintaining Azure Storage Account](https://docs.microsoft.com/azure/storage/blobs/).</span></span>

## <a name="overview"></a><span data-ttu-id="f6a21-110">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="f6a21-110">Overview</span></span>

<span data-ttu-id="f6a21-111">Tässä aiheessa suoritetaan kaksi päävaihetta:</span><span class="sxs-lookup"><span data-stu-id="f6a21-111">In this topic, you will complete two main steps:</span></span>

- <span data-ttu-id="f6a21-112">Azure-tallennustilin määrittäminen tallennustilin URI-tunnuksen saamista varten.</span><span class="sxs-lookup"><span data-stu-id="f6a21-112">Set up the Azure storage account to get the storage account URI.</span></span>
- <span data-ttu-id="f6a21-113">Avainsäilön määrittäminen tallennustilin URI-tunnuksen tallentamista varten.</span><span class="sxs-lookup"><span data-stu-id="f6a21-113">Set up the key vault to store the storage account URI.</span></span>

## <a name="set-up-the-azure-storage-account-to-get-the-storage-account-uri"></a><span data-ttu-id="f6a21-114">Azure-tallennustilin määrittäminen tallennustilin URI-tunnuksen saamista varten</span><span class="sxs-lookup"><span data-stu-id="f6a21-114">Set up the Azure storage account to get the storage account URI</span></span>

1. <span data-ttu-id="f6a21-115">Avaa tallennustili, jota aiot käyttää sähköisen laskutuksen lisäosan kanssa.</span><span class="sxs-lookup"><span data-stu-id="f6a21-115">Open the storage account that you plan to use with the Electronic invoicing add-on.</span></span>
2. <span data-ttu-id="f6a21-116">Siirry kohtaan **Blob-palvelu** \> **Säilöt** ja luo uusi säilö.</span><span class="sxs-lookup"><span data-stu-id="f6a21-116">Go to **Blob service** \> **Containers**, and create a new container.</span></span>
3. <span data-ttu-id="f6a21-117">Anna säilölle nimi ja määritä **Julkinen käyttöoikeustaso** -kentän arvoksi **Yksityinen (ei anonyymia käyttöä)**.</span><span class="sxs-lookup"><span data-stu-id="f6a21-117">Enter a name for the container, and set the **Public access level** field to **Private (no anonymous access)**.</span></span>
4. <span data-ttu-id="f6a21-118">Avaa säilö ja siirry kohtaan **Asetukset \> Käyttöoikeuskäytäntö**.</span><span class="sxs-lookup"><span data-stu-id="f6a21-118">Open the container, and go to **Settings \> Access policy**.</span></span>
5. <span data-ttu-id="f6a21-119">Valitse **Lisää käytäntö** lisätäksesi tallennetun käyttöoikeuskäytännön.</span><span class="sxs-lookup"><span data-stu-id="f6a21-119">Select **Add policy** to add a stored access policy.</span></span>
6. <span data-ttu-id="f6a21-120">Määritä kentät **Tunnus** ja **Oikeudet** tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="f6a21-120">Set the **Identifier** and **Permissions** fields as appropriate.</span></span> <span data-ttu-id="f6a21-121">**Oikeudet**-kentässä valitaan kaikki oikeudet.</span><span class="sxs-lookup"><span data-stu-id="f6a21-121">In the **Permissions** field, you should select all permissions.</span></span>

    ![Blob-tallennustilan oikeuksien myöntäminen](media/e-Invoicing-services-create-azure-resources-grant-blob-permissions.png)

7. <span data-ttu-id="f6a21-123">Määritä alkamis- ja päättymispäivät.</span><span class="sxs-lookup"><span data-stu-id="f6a21-123">Enter the start and expiry dates.</span></span> <span data-ttu-id="f6a21-124">Päättymispäivän on oltava tulevaisuudessa.</span><span class="sxs-lookup"><span data-stu-id="f6a21-124">The expiry date should be in future.</span></span>
8. <span data-ttu-id="f6a21-125">Tallenna käytäntö valitsemalla **OK** ja tallenna muutoksesi säilöön.</span><span class="sxs-lookup"><span data-stu-id="f6a21-125">Select **OK** to save the policy, and then save your changes to the container.</span></span>
9. <span data-ttu-id="f6a21-126">Palaa tallennustilille ja avaa **Tallennustilan hallinta (esikatselu)**.</span><span class="sxs-lookup"><span data-stu-id="f6a21-126">Return to the storage account, and open **Storage Explorer (preview)**.</span></span>
10. <span data-ttu-id="f6a21-127">Napsauta säilöä hiiren kakkospainikkeella ja valitse sitten **Hae jaetun käyttöoikeuden allekirjoitus**.</span><span class="sxs-lookup"><span data-stu-id="f6a21-127">Right-click the container, and then select **Get Shared Access Signature**.</span></span>
11. <span data-ttu-id="f6a21-128">Kopioi **Jaetun käyttöoikeuden allekirjoitus** -valintaikkunan arvo ja tallenna se **URI**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="f6a21-128">In the **Shared Access Signature** dialog box, copy and store the value in the **URI** field.</span></span> <span data-ttu-id="f6a21-129">Tätä arvoa käytetään seuraavassa menettelyssä, ja sitä kutsutaan *jaetun käyttöoikeuden allekirjoituksen URI-tunnukseksi*.</span><span class="sxs-lookup"><span data-stu-id="f6a21-129">This value will be used in the next procedure and will be referred to as the *shared access signature URI*.</span></span>

    ![URI-arvon valitseminen ja kopioiminen](media/e-Invoicing-services-create-azure-resources-select-and-copy-uri.png)

## <a name="set-up-the-key-vault-to-store-the-storage-account-uri"></a><span data-ttu-id="f6a21-131">Avainsäilön määrittäminen tallennustilin URI-tunnuksen tallentamista varten</span><span class="sxs-lookup"><span data-stu-id="f6a21-131">Set up the key vault to store the storage account URI</span></span>

1. <span data-ttu-id="f6a21-132">Avaa avainsäilö, jota aiot käyttää sähköisen laskutuksen lisäosan kanssa.</span><span class="sxs-lookup"><span data-stu-id="f6a21-132">Open the key vault that you intend to use with the Electronic invoicing add-on.</span></span>
2. <span data-ttu-id="f6a21-133">Siirry kohtaan **Asetukset** \> **Salasanat** ja luo sitten uusi salasana valitsemalla **Luo/tuo**.</span><span class="sxs-lookup"><span data-stu-id="f6a21-133">Go to **Settings** \> **Secrets**, and then select **Generate/Import** to create a new secret.</span></span>
3. <span data-ttu-id="f6a21-134">Valitse **Luo salasana** -sivun **Lataa asetuksia** -kentässä **Manuaalinen**.</span><span class="sxs-lookup"><span data-stu-id="f6a21-134">On the **Create a secret** page, in the **Upload options** field, select **Manual**.</span></span>
4. <span data-ttu-id="f6a21-135">Anna salasanan nimi.</span><span class="sxs-lookup"><span data-stu-id="f6a21-135">Enter the name of the secret.</span></span> <span data-ttu-id="f6a21-136">Tätä nimeä käytetään palvelun määrittämiseen RCS:ssä (Regulatory Configuration Service) ja sitä kutsutaan *avainsäilön salasananimeksi*.</span><span class="sxs-lookup"><span data-stu-id="f6a21-136">This name will be used during setup of the service in Regulatory Configuration Service (RCS) and will be referred to as the *key vault secret name*.</span></span>
5. <span data-ttu-id="f6a21-137">Valitse **Arvo**-kentässä **Jaetun käyttöoikeuden allekirjoituksen URI-tunnus** ja sitten **Luo**.</span><span class="sxs-lookup"><span data-stu-id="f6a21-137">In the **Value** field, select **Shared Access Signature URI**, and then select **Create**.</span></span>
6. <span data-ttu-id="f6a21-138">Määritä käyttöoikeuskäytäntö, jolla sähköisen laskutuksen lisäosalle myönnetään asianmukainen suojattu käyttöoikeus luomaasi salasanaan.</span><span class="sxs-lookup"><span data-stu-id="f6a21-138">Set up the access policy to grant the Electronic invoicing add-on the correct level of secure access to the secret you created.</span></span> <span data-ttu-id="f6a21-139">Siirry kohtaan **Asetukset \> Käyttöoikeuskäytäntö** ja valitse **Lisää käyttöoikeuskäytäntö**.</span><span class="sxs-lookup"><span data-stu-id="f6a21-139">Go to **Settings \> Access policy**, and select **Add Access Policy**.</span></span>
7. <span data-ttu-id="f6a21-140">Määritä salasanaoikeudet toiminnoille **Hae** ja **Luetteloi**.</span><span class="sxs-lookup"><span data-stu-id="f6a21-140">Set the secret permissions for the **Get** and **List** operations.</span></span>

    ![Palvelun käyttöoikeuksien myöntäminen](media/e-Invoicing-services-create-azure-resources-grant-service-access.png)

8. <span data-ttu-id="f6a21-142">Määritä varmenneoikeudet toiminnoille **Hae** ja **Luetteloi**.</span><span class="sxs-lookup"><span data-stu-id="f6a21-142">Set the certificate permissions for **Get** and **List** operations.</span></span>

    ![Varmenneoikeuksien myöntäminen](media/e-Invoicing-services-create-azure-resources-grant-certificate-permission.png)

9. <span data-ttu-id="f6a21-144">Valitse **Objekti** -kentässä **Mitään ei valittu**.</span><span class="sxs-lookup"><span data-stu-id="f6a21-144">In the **Select principal** field, select **None selected**.</span></span>
10. <span data-ttu-id="f6a21-145">Valitse **Objekti**-valintaikkunassa objekti lisäämällä **Sähköisen laskutuksen palvelu**.</span><span class="sxs-lookup"><span data-stu-id="f6a21-145">In the **Principal** dialog box, select the principal by adding **e-Invoicing Service**.</span></span>
11. <span data-ttu-id="f6a21-146">Valitse **Lisää** ja sitten **Tallenna avainsäilön muutokset**.</span><span class="sxs-lookup"><span data-stu-id="f6a21-146">Select **Add**, and then select **Save Key Vault changes**.</span></span>
12. <span data-ttu-id="f6a21-147">Kopioi **Yhteenveto**-sivulla avainsäilön **DNS nimi** -arvo.</span><span class="sxs-lookup"><span data-stu-id="f6a21-147">On the **Overview** page, copy the **DNS name** value for the key vault.</span></span> <span data-ttu-id="f6a21-148">Tätä arvoa käytetään palvelun RCS:ssä määrittämiseen ja sitä kutsutaan *avainsäilön URI-tunnukseksi*.</span><span class="sxs-lookup"><span data-stu-id="f6a21-148">This value will be used during setup of the service in RCS and will be referred as the *key vault URI*.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]

