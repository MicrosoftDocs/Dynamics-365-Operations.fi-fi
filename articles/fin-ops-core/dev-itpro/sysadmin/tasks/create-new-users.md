---
title: Uusien käyttäjien luominen
description: Käyttäjät ovat organisaation sisäisiä käyttäjiä tai ulkoisia asiakkaita ja toimittajia, jotka tarvitsevat järjestelmän käyttöoikeuden töidensä tekemiseen.
author: maertenm
manager: AnnBe
ms.date: 08/30/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, SysDataAreaSelectLookup, SysSecUserAddRoles, SysUserMSODSUserImport
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4a5635f96132b2e52227b569e7e480fa55e82d61
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180941"
---
# <a name="create-new-users"></a>Uusien käyttäjien luominen

[!include [task guide banner](../../includes/task-guide-banner.md)]
[!include [banner](../../includes/preview-banner.md)]

Käyttäjät ovat organisaation sisäisiä käyttäjiä tai ulkoisia asiakkaita ja toimittajia, jotka tarvitsevat järjestelmän käyttöoikeuden töidensä tekemiseen.

## <a name="associate-a-user-with-a-license-new-license-types-only"></a>Käyttäjän liittäminen käyttöoikeuteen (vain uudet käyttöoikeustyypit)
Sellaisten asiakkaiden käyttäjiin, joilla on jokin lokakuussa 2019 lisätyistä uusista käyttöoikeustyypeistä, on liitettävä käyttöoikeus. Käyttöoikeuteen liitetyt käyttäjät lisätään roolittomina järjestelmäkäyttäjinä, kun he kirjautuvat sisään ensimmäisen kerran. Käyttäjät, joihin ei ole liitetty käyttöoikeutta, saavat varoitussanoman.

Järjestelmänvalvojat voivat [määrittää käyttöoikeuksia käyttäjille](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) [Microsoft 365 -hallintakeskuksessa](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).

## <a name="add-a-new-user"></a>Lisää uusi käyttäjä
1. Valitse **Järjestelmänvalvojat \> Käyttäjät \> Käyttäjät**.
2. Valitse toimintoruudussa **Uusi**.
3. Anna käyttäjän yksilöivä tunnus **Käyttäjätunnus**-kenttään. Käyttäjätunnus on pakollinen.  
4. Kirjoita käyttäjän nimi **Käyttäjän nimi** -kenttään toimittajan nimi.  
5. Kirjoita käyttäjän toimialue **Toimialue**-kenttään.  
6. Kirjoita käytättäjän alias **Alias**-kenttään.  
7. Valitse yritys **Yritys**-kentässä. 
8. [Määritä käyttöoikeusroolit käyttäjille](assign-users-security-roles.md) valitsemalla **Käyttäjän rooli** -pikavälilehdessä **Määritä rooleja**.
9. Valitse **OK**.
10. Valitse **Tallenna**.

## <a name="import-users"></a>Tuo käyttäjiä
1. Valitse toimintoruudussa **Tuo käyttäjiä**.
2. Merkitse valittu rivi luettelossa.
3. Valitse **Tuo käyttäjiä**.
4. Valitse **Sulje**.

