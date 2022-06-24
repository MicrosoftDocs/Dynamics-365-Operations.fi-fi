---
title: Warehouse Management -mobiilisovelluksen konfiguroiminen pilven ja reunan vaakayksiköitä varten
description: Tässä artikkelissa kerrotaan, miten Warehouse Management -mobiilisovellukset määritetään varastoille, joita käytetään pilven tai reunan skaalausyksiköiden avulla.
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
ms.openlocfilehash: 86edef2dfa6e9c71c04d50f185148be3a622fea1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8865235"
---
# <a name="configure-the-warehouse-management-mobile-app-for-cloud-and-edge-scale-units"></a>Warehouse Management -mobiilisovelluksen konfiguroiminen pilven ja reunan vaakayksiköitä varten

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kerrotaan, miten Warehouse Management -mobiilisovellukset määritetään käytettäviksi varastoille, joita käytetään pilven tai reunan skaalausyksiköiden avulla.

## <a name="prerequisites"></a>Edellytykset

Ennen kuin alat määrittää matkapuhelimista yhteyttä pilven tai reunan vaakayksikköön, vahvista, että ne voivat muodostaa yhteyden yritystoimintoon. Lisätietoja on kohdassa [Warehouse Management -mobiilisovelluksen asentaminen ja yhdistäminen](../warehousing/install-configure-warehouse-management-app.md).

## <a name="additional-setup-when-you-run-the-warehouse-management-mobile-app-against-a-scale-unit"></a>Lisäasetukset, kun Warehouse Management -mobiilisovellusta suoritetaan skaalausyksikölle

[Varaston vaakayksikköjen kuormituksen käyttöönoton](cloud-edge-landing-page.md#scale-unit-manager-portal) osana useimmat Warehouse Management -mobiilisovelluksen laitteiden yhteyden edellyttämistä tiedoista synkronoidaan automaattisesti yritystoiminnosta vaakayksikköön. Tiedot on kuitenkin syötettävä **Azure Active Directory -sovellukset** -sivulle (**Järjestelmänvalvonta \> Määritys \> Azure Active Directory -sovellukset**) Scale Unitin käyttöönotossa. Lisäksi saatat joutua päivittämään käyttäjätunnuksen **yrityksen** oletusarvon tai luomaan uuden käyttäjän. Käyttäjät, jotka on liitetty yritykseen, jota ei ole skaalausyksikköjen käytössä, eivät voi kirjautua sisään, kun Warehouse Management -mobiilisovellus on liitetty tähän skaalausyksikköön.

> [!NOTE]
> Koska **Azure Active Directory -sovellukset** -sivun tietoja ei synkronoida, nämä tiedot on ylläpidettävä manuaalisesti, jos haluat siirtää varaston kuormituksen toiseen skaalausyksikköön.

Muista, että osana kunkin Warehouse Management -mobiilisovelluksen yhteysasetuksia määritetyn Azure Active Directory -resurssin URL-osoitteen on oltava Scale Unitille yritystoiminnon asemesta.
