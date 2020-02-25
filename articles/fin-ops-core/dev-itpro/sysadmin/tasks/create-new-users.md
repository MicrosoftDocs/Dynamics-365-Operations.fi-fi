---
title: Uusien käyttäjien luominen
description: Käyttäjät ovat organisaation sisäisiä käyttäjiä tai ulkoisia asiakkaita ja toimittajia, jotka tarvitsevat järjestelmän käyttöoikeuden töidensä tekemiseen.
author: maertenm
manager: AnnBe
ms.date: 02/06/2020
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
ms.openlocfilehash: 6d884dfe30be5684a90925d4d2d9ab7eebca5b44
ms.sourcegitcommit: 13c4a6f98ccce243d6befde90992aefcf562bdab
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/06/2020
ms.locfileid: "3029806"
---
# <a name="create-new-users"></a>Uusien käyttäjien luominen

[!include [task guide banner](../../includes/task-guide-banner.md)]

Käyttäjät ovat organisaation sisäisiä käyttäjiä tai ulkoisia asiakkaita ja toimittajia, jotka tarvitsevat järjestelmän käyttöoikeuden töidensä tekemiseen.

## <a name="associate-a-user-with-a-license-new-license-types-only"></a>Käyttäjän liittäminen käyttöoikeuteen (vain uudet käyttöoikeustyypit)
Sellaisten asiakkaiden käyttäjiin, joilla on jokin lokakuussa 2019 lisätyistä uusista käyttöoikeustyypeistä, on liitettävä käyttöoikeus. Käyttöoikeuteen liitetyt käyttäjät lisätään roolittomina järjestelmäkäyttäjinä, kun he kirjautuvat sisään ensimmäisen kerran.

Järjestelmänvalvojat voivat [määrittää käyttöoikeuksia käyttäjille](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) [Microsoft 365 -hallintakeskuksessa](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).

## <a name="associate-an-external-user-with-a-license-new-license-types-only"></a>Ulkoisen käyttäjän liittäminen käyttöoikeuteen (vain uudet käyttöoikeustyypit)
Sen vuokraajan ulkopuolisten käyttäjien, jolla ympäristö otettiin käyttöön, on oltava edustettuna isännän vuokraajahakemistossa (Azure Active Directory (Azure AD)), jotta käyttäjille voidaan myöntää käyttöoikeuksia. Nämä ulkoiset käyttäjät on lisättävä vuokraajalle Azure AD:ssä vieraskäyttäjinä, minkä jälkeen käyttäjille on määritettävä asianmukaiset käyttöoikeudet. Lisätietoja on kohdassa [Lisää Azure Active Directoryn B2B-yhteistyön käyttäjiä Azure-portaaliin](https://docs.microsoft.com/azure/active-directory/b2b/add-users-administrator).

## <a name="add-a-new-user"></a>Lisää uusi käyttäjä
1. Valitse **Järjestelmänvalvojat \> Käyttäjät \> Käyttäjät**.
2. Valitse toimintoruudussa **Uusi**.
3. Anna käyttäjän yksilöivä tunnus **Käyttäjätunnus**-kenttään. Käyttäjätunnus on pakollinen.  
4. Kirjoita käyttäjän nimi **Käyttäjän nimi** -kenttään toimittajan nimi.  
5. Kirjoita käyttäjän toimialue **Toimialue**-kenttään.  
6. Kirjoita käytättäjän alias **Alias**-kenttään.  
7. Valitse yritys **Yritys**-kentässä. 
8. Määritä käyttöoikeusroolit käyttäjille valitsemalla **Käyttäjän rooli** -pikavälilehdessä **Määritä rooleja**. Lisätietoja on kohdassa [Käyttäjien määrittäminen käyttöoikeusrooleille](assign-users-security-roles.md).
9. Valitse **OK**.
10. Valitse **Tallenna**.

## <a name="import-users"></a>Tuo käyttäjiä
1. Valitse toimintoruudussa **Tuo käyttäjiä**.
2. Merkitse valittu rivi luettelossa.
3. Valitse **Tuo käyttäjiä**.
4. Valitse **Sulje**.

