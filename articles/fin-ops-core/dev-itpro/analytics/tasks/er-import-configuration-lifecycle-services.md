---
title: Konfiguraation tuominen Lifecycle Services -palvelusta
description: Tässä aiheessa käsitellään sähköisen raportoinnin (ER) määrityksen uuden version tuontia Microsoft Dynamics Lifecycle Servicesista (LCS).
author: NickSelin
manager: AnnBe
ms.date: 09/14/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 602886b0dd729b8ec52940f42bd1c393dac8acda
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093692"
---
# <a name="import-a-configuration-from-lifecycle-services"></a>Konfiguraation tuominen Lifecycle Services -palvelusta

[!include [banner](../../includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooli voi tuoda uuden [sähköisen raportoinnin konfiguraation](../general-electronic-reporting.md#Configuration) version ja ladata sen [projektitason resurssikirjastosta](../../lifecycle-services/asset-library.md) Microsoft Dynamics Lifecycle Services (LCS) -sovelluksessa.

Tässä esimerkissä valitaan sopiva ER-konfiguraatio ja tuodaan se malliyritykselle nimeltä Litware, Inc. Nämä vaiheet voidaan suorittaa mille tahansa yritykselle, koska kaikki yritykset jakavat sähköisen raportoinnin konfiguraatiot. Jos haluat tehdä nämä vaiheet, tee ensin vaiheet kohdassa [Konfiguraation lataaminen Lifecycle Services -palveluun](er-upload-configuration-into-lifecycle-services.md). LCS:n käyttöoikeus vaaditaan myös.

1. Kirjaudu sovellukseen yhdellä seuraavista rooleista:

    - Sähköisen raportoinnin kehittäjä
    - Järjestelmänvalvoja

2. Valitse **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.
3. Valitse **Konfiguraatiot**.

<a name="accessconditions"></a>
> [!NOTE]
> Varmista, että nykyinen Dynamics 365 Finance -käyttäjä on sellaisen LCS-projektin jäsen, joka sisältää sen resurssikirjaston, jonka [käyttöoikeuden](../../lifecycle-services/asset-library.md#asset-library-support) käyttäjä haluaa sähköisen raportoinnin konfiguraatioiden tuomista varten.
>
> LCS-projektia ei voi käyttää sähköisen raportoinnin säilöstä, jos se on eri toimialueella kuin Financen käyttämä toimialue. Jos yrität tehdä niin, näkyviin tulee LCS-projektien tyhjä luettelo. Et voi tuoda sähköisen raportoinnin konfiguraatioita proektitason resurssikirjastosta LCS:ään. Jos haluat käyttää projektitason resurssikirjastoja sähköisen raportoinnin säilöstä, jota käytetään sähköisen raportoinnin konfiguraatioiden tuomiseen, kirjaudu sisään sen Finance-esiintymän vuokraajaan (toimialue) kuuluvan käyttäjän valtuustiedoilla, joka on valmisteltu.

## <a name="delete-a-shared-version-of-a-data-model-configuration"></a>Poista tietomallin konfiguraation jaettu versio

1. Valitse **Konfiguraatiot**-sivun konfiguraatiopuussa **Näytemallikonfiguraatio**.

    Ensimmäinen näytetietomallin konfiguraatio luotiin ja julkaistiin LCS:ään, kun kohdan [Konfiguraation lataaminen Lifecycle Services -palveluun](er-upload-configuration-into-lifecycle-services.md) vaiheet suoritettiin. Tässä menettelyssä poistetaan kyseinen ER-konfiguraation versio. Tämän jälkeen voit tuoda version LCS:stä myöhemmin tähän aiheeseen.

2. Etsi haluamasi tietue luettelosta ja valitse se.

    Valitse tässä esimerkissä konfiguraation versio, jonka tila on **Jaettu**. Tämä tila ilmaisee, että konfiguraatio on julkaistu LCS:ään.

3. Valitse **Muutoksen tila**.
4. Valitse **Keskeytä**.

    Jos muutat valitun version tilan **Jaettu**-tilasta **Keskeytetty**-tilaksi, versio voidaan poistaa.

5. Valitse **OK**.
6. Etsi haluamasi tietue luettelosta ja valitse se.

    Valitse tässä esimerkissä konfiguraation versio, jonka tila on **Keskeytetty**.

7. Valitse **Poista**.
8. Valitse **Kyllä**.

    Huomaa, että vain valitun tietomallin konfiguraation luonnosversio 2 on nyt käytettävissä.

9. Sulje sivu.

## <a name="import-a-shared-version-of-a-data-model-configuration-from-lcs"></a>Tuo tietomallin konfiguraation jaettu versio LCS:stä

1. Siirry kohtaan **Organisaation hallinto \> Työtilat \> Sähköinen raportointi**.

2. Valitse **Konfiguraation lähteet** -osassa **Litware, Inc.** -ruutu.

3. Valitse **Litware, Inc.** -ruudusta **Säilöt**.

    Nyt voit avata Litware, Inc. -konfiguraatiolähteen säilöluettelon.

4. Valitse **Avaa**.

    Valitse tässä esimerkissä **LCS**-säilötietue ja avaa se.«» Sinulla on oltava [käyttöoikeus](#accessconditions) LCS-projektiin ja resurssikirjastoon, jota valittu sähköisen raportoinnin säilö käyttää.

5. Merkitse valittu rivi luettelossa.

    Valitse tässä esimerkissä versioluettelosta ensimmäinen **näytemallikonfiguraatio**.

6. Valitse **Tuo**.
7. Vahvista valitun version tuonti LCS:stä valitsemalla **Kyllä**.

    Tietosanoma vahvistaa, että valittu versio on tuotu.

8. Sulje sivu.
9. Sulje sivu.
10. Valitse **Konfiguraatiot**.
11. Valitse puussa **Näytemallikonfiguraatio**.
12. Etsi haluamasi tietue luettelosta ja valitse se.

    Valitse tässä esimerkissä konfiguraation versio, jonka tila on **Jaettu**.

    Huomaa, että valitun tietomallin konfiguraation jaettu versio 1 on nyt myös käytettävissä.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]