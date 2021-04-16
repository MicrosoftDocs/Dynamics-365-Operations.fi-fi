---
title: Konfiguraation lataaminen Lifecycle Services -palveluun
description: Tässä aiheessa käsitellään uuden sähköisen raportoinnin (ER) määrityksen luontia ja lataamista Microsoft Dynamics Lifecycle Servicesiin (LCS).
author: NickSelin
ms.date: 09/14/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0211fea7af303fe1dd7dce26f887bed4ed3b0f1e
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744912"
---
# <a name="upload-a-configuration-into-lifecycle-services"></a>Konfiguraation lataaminen Lifecycle Services -palveluun

[!include [banner](../../includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooli voi luoda uuden [sähköisen raportoinnin konfiguraation](../general-electronic-reporting.md#Configuration) ja ladata sen [projektitason resurssikirjastoon](../../lifecycle-services/asset-library.md) Microsoft Dynamics Lifecycle Services (LCS) -sovelluksessa.

Tässä esimerkissä luodaan konfiguraatio malliyritykselle nimeltä Litware, Inc. ja ladataan sen LCS-palveluun. Nämä vaiheet voidaan suorittaa mille tahansa yritykselle, koska kaikki yritykset jakavat sähköisen raportoinnin konfiguraatiot. Näitä vaiheita varten on ensin suoritettava kohdassa [Konfiguroinnin tarjoajien luominen ja merkitseminen aktiivisiksi](er-configuration-provider-mark-it-active-2016-11.md) käsitellyt vaiheet. LCS:n käyttöoikeus vaaditaan myös.

1. Kirjaudu sovellukseen yhdellä seuraavista rooleista:

    - Sähköisen raportoinnin kehittäjä
    - Järjestelmänvalvoja

2. Valitse **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.
3. Valitse **Litware, Inc.** ja merkitse se **aktiiviseksi**.
4. Valitse **Konfiguraatiot**.

<a name="accessconditions"></a>
> [!NOTE]
> Varmista, että nykyinen Dynamics 365 Finance -käyttäjä on sellaisen LCS-projektin jäsen, joka sisältää sähköisen raportoinnin konfiguraatioiden tuomisessa käytettävän[resurssikirjaston](../../lifecycle-services/asset-library.md#asset-library-support).
>
> LCS-projektia ei voi käyttää sähköisen raportoinnin säilöstä, jos se on eri toimialueella kuin Financen käyttämä toimialue. Jos yrität tehdä niin, näkyviin tulee LCS-projektien tyhjä luettelo. Et voi tuoda sähköisen raportoinnin konfiguraatioita proektitason resurssikirjastosta LCS:ään. Jos haluat käyttää projektitason resurssikirjastoja sähköisen raportoinnin säilöstä, jota käytetään sähköisen raportoinnin konfiguraatioiden tuomiseen, kirjaudu sisään sen Finance-esiintymän vuokraajaan (toimialue) kuuluvan käyttäjän valtuustiedoilla, joka on valmisteltu.

## <a name="create-a-new-data-model-configuration"></a>Uuden tietomallin konfiguraation luominen

1. Siirry kohtaan **Organisaation hallinto \> Sähköinen raportointi \> Konfiguraatiot**.
2. Valitse **Konfiguraatiot**-sivulla **Luo konfiguraatio** ja avaa avattava valintaikkuna.

    Tässä esimerkissä luodaan konfiguraatio, joka sisältää tietomalliesimerkin sähköisiä asiakirjoja varten. Tämä tietomallin konfiguraatio ladataan LCS:ään myöhemmin.

3. Syötä **Nimi**-kenttään **Näytemallikonfiguraatio**.
4. Syötä **Kuvaus**-kenttään **Näytemallikonfiguraatio**.
5. Valitse **Luo konfiguraatio**.
6. Valitse **Mallin suunnittelutoiminto**.
7. Valitse **Uusi**.
8. Kirjoita **Nimi**-kenttään **Aloituspiste**.
9. Valitse **Lisää**.
10. Valitse **Tallenna**.
11. Sulje sivu.
12. Valitse **Muutoksen tila**.
13. Valitse **Valmis**.
14. Valitse **OK**.
15. Sulje sivu.

## <a name="register-a-new-repository"></a>Rekisteröi uusi säilö

1. Siirry kohtaan **Organisaation hallinto \> Työtilat \> Sähköinen raportointi**.

2. Valitse **Konfiguraation lähteet** -osassa **Litware, Inc.** -ruutu.

3. Valitse **Litware, Inc.** -ruudusta **Säilöt**.

    Nyt voit avata Litware, Inc. -konfiguraatiolähteen säilöluettelon.

4. Avaa avattava valintaikkuna valitsemalla **Lisää**.

    Nyt voit lisätä uuden säilön.

5. Valitse **Konfiguraatiosäilön syöttö** -kentässä **LCS**.
6. Valitse **Luo säilö**.
7. Syötä arvo **Projekti**-kenttään tai valitse kentässä arvo.

    Tässä esimerkissä valitaan haluttu LCS-projekti. Sinulla on oltava projektin [käyttöoikeus](#accessconditions).

8. Valitse **OK**.

    Luo uusi säilön merkintä.

9. Merkitse valittu rivi luettelossa.

    Valitse tässä esimerkissä **LCS**-säilötietue.

    Huomaa, että rekisteröity säilö on merkitty nykyisellä palveluntarjoalla. Toisin sanoen vain kyseisen palveluntarjoajan omistamat konfiguraatiot voidaan sijoittaa tähän säilöön. Tämän vuoksi ne ladataan valittuun LCS-projektiin.

10. Valitse **Avaa**.

    Avaa säilö, jotta voit tarkastella sähköisen raportoinnin konfiguraatioiden luetteloa. Jos valittua projektia ei ole vielä käytetty sähköisen raportoinnin konfiguraatioiden jakamiseen, luettelo on tyhjä.

11. Sulje sivu.
12. Sulje sivu.

## <a name="upload-a-configuration-into-lcs"></a>Lataa konfiguraatio LCS-järjestelmään

1. Siirry kohtaan **Organisaation hallinto \> Sähköinen raportointi \> Konfiguraatiot**.
2. Valitse **Konfiguraatiot**-sivun konfiguraatiopuussa **Näytemallikonfiguraatio**.

    Valitse luotu konfiguraatio, joka on jo valmis.

3. Etsi haluamasi tietue luettelosta ja valitse se.

    Valitse tässä esimerkissä valitun konfiguraation versio, jonka tila on **Valmis**.

4. Valitse **Muutoksen tila**.
5. Valitse **Jaa**.

    Konfiguraation tila muutetaan **Valmis**-tilasta **Jaettu**-tilaksi, kun konfiguraatio julkaistaan LCS:ssä.

6. Valitse **OK**.
7. Etsi haluamasi tietue luettelosta ja valitse se.

    Valitse tässä esimerkissä konfiguraation versio, jonka tila on **Jaettu**.

    Huomaa, että valitun version on tila on muutetaan **Valmis**-tilasta **Jaettu**-tilaan.

8. Sulje sivu.
9. Valitse **Säilöt**.

    Nyt voit avata Litware, Inc. -konfiguraatiolähteen säilöluettelon.

10. Valitse **Avaa**.

    Valitse tässä esimerkissä **LCS**-säilötietue ja avaa se.«»

    Huomaa, että valittu konfiguraatio näytetään resurssina valitussa LCS-projektissa.

11. Avaa LCS siirtymällä osoitteeseen <https://lcs.dynamics.com>.
12. Avaa projekti, jota käytettiin aiemmin säilön rekisteröinnissä.
13. Avaa projektin resurssikirjasto.
14. Valitse **GER-konfiguraatio**-resurssityyppi.

    Ladattu sähköisen raportoinnin konfiguraatio näkyy luettelossa.

    Huomaa, että ladattu LCS-konfiguraatio voidaan tuoda toiseen esiintymään, jos tarjoajilla on käyttöoikeus tähän LCS-projektiin.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]