---
title: Sähköisen laskutuksen Azure-resurssien määrittäminen
description: Tämä artikkeli sisältää yhteenvedon sähköisen laskutuksen Microsoft Azure -resurssien määritysprosessista.
author: dkalyuzh
ms.date: 01/26/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: c5b7b2ca4d7733fb1c75ded8798655699284fe1a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8907726"
---
# <a name="set-up-azure-resources-for-electronic-invoicing"></a>Sähköisen laskutuksen Azure-resurssien määrittäminen

[!include [banner](../includes/banner.md)]

Microsoft Azure -resurssien määrittämisessä sähköistä laskutusta varten on kolme vaihetta. Kaksi ensimmäistä vaihetta, "Azure Key Vaultin luominen Azure-portaalissa" ja "Luo Azure-tallennustili Azure-portaalissa", ovat pakollisia. Kolmas vaihe "Määritä SharePoint-yhteys" on valinnainen.

## <a name="create-an-azure-key-vault-in-the-azure-portal"></a>Luo Azure Key Vault Azure-portaalissa

Luo avainsäilö Azure-tilauksessasi. On suositeltavaa luoda erillinen Key Vault sähköiselle laskutukselle ja ettei salaisuuksia yhdistetä muihin sovelluksiin. Luo sähköisten tiedostojen skenaarioita varten niin monta salaisuutta ja varmennetta kuin sähköisten asiakirjojen käyttö edellyttää. Tässä vaiheessa on luotava vähintään yksi salaisuus jaettu allekirjoituksen tunnus (SAS) -tunnukselle, joka on Azure-tallennustilille, jonka luot seuraavassa vaiheessa.

Lisätietoja tämän vaiheen suorittamisesta on kohdassa [Luo Azure Key Vault Azure-portaalissa](e-invoicing-create-azure-key-vault-azure-portal.md).

## <a name="create-an-azure-storage-account-in-the-azure-portal"></a>Luo Azure-tallennustili Azure-portaalissa

Omistat kaikki sähköiset asiakirjat ja tiedostot, jotka sähköinen laskutuspalvelu luo tai jotka syötät palveluun. Nämä asiakirjat ja tiedostot tallentuvat Azure-tallennustilille, jonka luot Azure-tilauksessasi. Palvelu käyttää tallennustiliäsi SAS-tunnuksen avulla, joka on peräisin Key Vaultin salaisuudesta.

Lisätietoja tämän vaiheen suorittamisesta on kohdassa [Luo Azure-tallennustili Azure-portaalissa](e-invoicing-create-azure-storage-account-azure-portal.md).

## <a name="configure-a-sharepoint-connection"></a>SharePoint-yhteyden konfiguroiminen

Joissakin tilanteissa on ehkä tallennettava sähköiset tiedostot SharePointiin ja noudettava ne SharePointista. Voit varmistaa, että sähköisen laskutuksen palvelu voi käyttää SharePoint-kansioitasi, määrittämällä niiden SharePointin käyttöoikeudet.

Lisätietoja tämän vaiheen suorittamisesta on kohdassa [SharePoint-yhteyden konfiguroiminen](e-invoicing-create-sharepoint-connection.md).
