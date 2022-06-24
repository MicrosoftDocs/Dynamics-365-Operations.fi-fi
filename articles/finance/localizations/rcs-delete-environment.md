---
title: Regulatory Configuration Service (RCS) – poista RCS-ympäristö
description: Tässä artikkelissa on tietoja siitä, miten RCS (Regulatory Configuration Service) -järjestelmänvalvoja voi poistaa RCS-ympäristön ja siihen liittyvät tiedot.
author: JaneA07
ms.date: 06/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization, Global
audience: Application User, System Admin
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2021-01-01
ms.dyn365.ops.version: AX 10.0.15
ms.openlocfilehash: 21e7ee546bb2b712d9424c6bd95e9f9227831bd1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8908887"
---
# <a name="regulatory-configuration-service-rcs---delete-an-rcs-environment"></a>Regulatory Configuration Service (RCS) – poista RCS-ympäristö

[!include [banner](../includes/banner.md)]

Tässä artikkelissa on tietoja siitä, miten RCS (Regulatory Configuration Service) -järjestelmänvalvoja voi poistaa RCS-ympäristön ja siihen liittyvät tiedot.

Ennen kuin voit suorittaa tämän artikkelin vaiheet, seuraavien edellytysten on toteuduttava:

- Sinulle on oltava määritetty **järjestelmänvalvojan** rooli RCS-ympäristöä varten.
- **Järjestelmänvalvojan** rooliin on oltava määritettynä **RCSDeleteEnvironmentDuty**-rooli.

## <a name="delete-an-rcs-environment"></a>Poista RCS-ympäristö

1. Avaa RCS ja valitse **Sähköinen raportointi** -työtilaruutu.
2. Valitse **Aiheeseen liittyviä linkkejä** -osassa **Poista RCS-ympäristö**.

    ![Poista RCS-ympäristön linkki Aiheeseen liittyviä linkkejä -osassa.](media/01_RCS-Delete-Environ-Related-Link.PNG)

3. Tarkista näyttöön tulevassa valintaikkunassa ympäristön poistoalueen sanomat.

    ![Sanomat Poista RCS-ympäristö -valintaikkunassa.](media/01_RCS-Delete-Environ-Msg_noGUID.PNG)

    > [!IMPORTANT]
    > RCS-ympäristön poistoa ei voi peruuttaa.
    >
    > Toiminto poistaa valitun RCS-ympäristön ja siihen liittyvät tiedot, mukaan lukien toiminnot ja konfiguraatiot, jotka on tallennettu yleistietovarastoon. Muille organisaatioille jaetut toiminnot ja konfiguraatiot poistetaan, jos niillä ei ole riippuvuuksia. Toiminnot ja konfiguraatiot, joista on riippuvuuksia, merkitään lopetetuiksi.

4. Kirjoita annettuun kenttään RCS-ympäristön yleinen yksilöivä tunnus (RCS-ympäristö), joka vahvistaa, että haluat poistaa sen. Ympäristön GUID on liitetty poistosanomaan.
5. Valitse **Poista ympäristö**.
    
RCS-ympäristösi ja kaikki siihen liittyvät tiedot poistetaan nyt.

> [!IMPORTANT]
> Kun olet poistanut RCS-ympäristön, tietoja ei voi palauttaa. Voit luoda uuden RCS-ympäristön missä tahansa käytettävissä olevalla RCS-alueella.
