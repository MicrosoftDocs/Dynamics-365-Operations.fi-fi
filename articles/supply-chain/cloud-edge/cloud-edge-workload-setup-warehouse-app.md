---
title: Warehouse Management -mobiilisovelluksen konfiguroiminen pilven ja reunan vaakayksiköitä varten
description: Tässä aiheessa kerrotaan, miten Warehouse Management -mobiilisovellukset määritetään varastoille, joita käytetään pilven tai reunan skaalausyksiköiden avulla.
author: perlynne
ms.date: 12/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysAADClientTable, SysUserManagement
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2022-01-31
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: 1fa00b40db2f6246029876964dca9d3229567848
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/31/2022
ms.locfileid: "8071637"
---
# <a name="configure-the-warehouse-management-mobile-app-for-cloud-and-edge-scale-units"></a>Warehouse Management -mobiilisovelluksen konfiguroiminen pilven ja reunan vaakayksiköitä varten

[!include [banner](../includes/banner.md)]

Tässä aiheessa kerrotaan, miten Warehouse Management -mobiilisovellukset määritetään käytettäviksi varastoille, joita käytetään pilven tai reunan skaalausyksiköiden avulla.

## <a name="prerequisites"></a>Edellytykset

Ennen kuin alat määrittää matkapuhelimista yhteyttä pilven tai reunan vaakayksikköön, vahvista, että ne voivat muodostaa yhteyden yritystoimintoon. Lisätietoja on kohdassa [Warehouse Management -mobiilisovelluksen asentaminen ja yhdistäminen](../warehousing/install-configure-warehouse-management-app.md).

## <a name="additional-setup-when-you-run-the-warehouse-management-mobile-app-against-a-scale-unit"></a>Lisäasetukset, kun Warehouse Management -mobiilisovellusta suoritetaan skaalausyksikölle

[Varaston vaakayksikköjen kuormituksen käyttöönoton](cloud-edge-landing-page.md#scale-unit-manager-portal) osana useimmat Warehouse Management -mobiilisovelluksen laitteiden yhteyden edellyttämistä tiedoista synkronoidaan automaattisesti yritystoiminnosta vaakayksikköön. Tiedot on kuitenkin syötettävä **Azure Active Directory -sovellukset** -sivulle (**Järjestelmänvalvonta \> Määritys \> Azure Active Directory -sovellukset**) Scale Unitin käyttöönotossa. Lisäksi saatat joutua päivittämään käyttäjätunnuksen **yrityksen** oletusarvon tai luomaan uuden käyttäjän. Käyttäjät, jotka on liitetty yritykseen, jota ei ole skaalausyksikköjen käytössä, eivät voi kirjautua sisään, kun Warehouse Management -mobiilisovellus on liitetty tähän skaalausyksikköön.

> [!NOTE]
> Koska **Azure Active Directory -sovellukset** -sivun tietoja ei synkronoida, nämä tiedot on ylläpidettävä manuaalisesti, jos haluat siirtää varaston kuormituksen toiseen skaalausyksikköön.

Muista, että osana kunkin Warehouse Management -mobiilisovelluksen yhteysasetuksia määritetyn Azure Active Directory -resurssin URL-osoitteen on oltava Scale Unitille yritystoiminnon asemesta.
